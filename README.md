# ADB

 Комманды сделанные на Windows10

1. Отобразить подключённый девайс в консоли.
```txt
./adb devices
```
 2. Вывести адрес приложения todolist в системе Android
```txt
./adb shell pm list packages | grep todolist
```
 3. Установить .apk файл приложениия todolist на телефон с компьютера через  ADB
```txt
./adb install D:/Telegram/001_ToDoList-master/001_ToDoList-master/app/build/outputs/apk/debug/app-debug.apk
```
 4. Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде.
```txt
./adb shell screencap storage/emulated/0/DCIM/group_22.png | ./adb pull storage/emulated/0/DCIM/group_22.png D:/image/group_22.png
```
 5. Вывести в консоль логи приложения todolist
```txt
./adb logcat | grep "todolist"
```
 6. Скопировать логи приложения todolist на компьютер.
```txt
./adb logcat | grep "todolist" > D:/todolist.log
```
 7. Удалить приложение todolist с телефона через ADB
```txt
./adb uninstall com.android.todolist
```
