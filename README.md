# Получение доступа к микрофону для Minecraft (macOS)
Лаунчер должен быть закрыт.
1. Найти в Finder приложение Minecraft
2. ПКМ -> "Показать содержимое пакета" 
3. Перейти в `/contents/`
4. Открыть `Info.plist ` в редакторе
5. Добавить внутри `<dict></dict>` следующее:
```
<key>NSMicrophoneUsageDescription</key>
<string>Microphone access is required to use voice chat in Minecraft.</string>
```
6. Сохранить, закрыть
7. Открыть терминал и ввести следующую команду:
`codesign --force --deep --sign - <расположение лаунчера>`
(расположение можно указать, перенеся в окно терминала лаунчер)
8. Запустить лаунчер и игру (Minecraft может единоразово потребовать доступ к ключам после ввода предыдущей команды)

# Gaining access to the microphone for Minecraft (macOS)
The Launcher must be closed.
1. Find the Minecraft app in the Finder
2. Right mouse click -> “Show Package Contents” 
3. Go to `/contents/`
4. Open `Info.plist` in editor
5. Add the following inside `<dict></dict>`:
```
<key>NSMicrophoneUsageDescription</key>
<string>Microphone access is required to use voice chat in Minecraft.</string>
```
6. Save, close
7. Open a terminal and enter the following command:
`codesign --force --deep --sign - <launcher path>`
(you can specify the path by moving the Launcher to the terminal window)
8. Launch the Launcher and the game (Minecraft may one-time require access to keys after entering the previous command)
