                                                  Операционная система Windows 7,10
1) Скачиваем Arduino IDE с оффициального сайта https://www.arduino.cc/en/Main/Software. 
    В разделе "Download the Arduino IDE" выбираем "Windows installer ..."
2) Устанавливаем "Arduino-#.#.#-windows.exe" (#-цифровое обозначение версии программы).<br>
    В процессе установки будет установлен драйвер для Arduino.
3) Подключаем Яйцебота к компьютеру через кабель USB-B.
4) Открываем "Диспетчер устройств" и проверяем, что драйвер установился корректно.<br>
    Нажимаем клавишесочетание Win+R и вводим devmgmt.msc<br>
    Далее открываем пункт "Порты (COM и LPT)", в нём должно показаться устройство "Arduino Uno (COM3)" (Номер порта может быть другим).
5) Обновление прошивки.
   	Переходим по ссылке и скачиваем файл. https://github.com/ProbotXYZ/EggBot/blob/master/Firmware/Firmware.zip<br>
   	Теперь надо разархивировать архив.<br>
  	Открываем установленную программу Arduino IDE.<br>
   	Если открылась пустая программа, то нужно нажать вверху на вкладку "Файл->Открыть", выбрать место, куда сохранился файл прошивки и выбрать EggDuino.ino<br>
   	Далее нужно нажать на вкладку "Инструменты", выбрать во вкладке "Плата" пункт "Arduino/Genuino Uno" и во вкладке "Порт" выбрать устройство, которое совпадает с тем, что было открыто в "Диспетчере устройств".<br>
   	На последок нужно залить прошивку в яйцебота нажав на стрелочку "->" в программе. Прошивка должна залиться успешно.<br>
6) Скачиваем векторный редактор "Inkscape" и плагин для работы с Eggbot.<br>
		Скачиваем Inkscape с оффициального сайта https://inkscape.org/release/inkscape-0.92.4/<br>
		Установим программу.<br>
		Скачиваем по ссылке плагин. https://github.com/ProbotXYZ/EggBot/blob/master/Software/Inkscape_extension_only.zip<br>
		
		
