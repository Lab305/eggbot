<html>
<body>
                                                  <h2>Операционная система Windows 7,10</h2>
<p>1) Скачиваем Arduino IDE с оффициального сайта https://www.arduino.cc/en/Main/Software. 
    В разделе "Download the Arduino IDE" выбираем "Windows installer ..."<br>
2) Устанавливаем "Arduino-#.#.#-windows.exe" (#-цифровое обозначение версии программы).<br>
    В процессе установки будет установлен драйвер для Arduino.<br>
3) Подключаем Сферобота к компьютеру через кабель USB-B.<br>
4) Открываем "Диспетчер устройств" и проверяем, что драйвер установился корректно.<br>
    Нажимаем клавишесочетание Win+R и вводим devmgmt.msc<br>
    Далее открываем пункт "Порты (COM и LPT)", в нём должно показаться устройство "Arduino Uno (COM3)" (Номер порта может быть другим).
5) Обновление прошивки.
   Переходим по ссылке и скачиваем файл. https://github.com/ProbotXYZ/EggBot/blob/master/Firmware/Firmware.zip<br>
   	Теперь надо разархивировать архив.<br>
  	Открываем установленную программу Arduino IDE.<br>
   	Если открылась пустая программа, то нужно нажать вверху на вкладку "Файл->Открыть", выбрать место, куда сохранился файл прошивки и выбрать EggDuino.ino<br>
   	Далее нужно нажать на вкладку "Инструменты", выбрать во вкладке "Плата" пункт "Arduino/Genuino Uno" и во вкладке "Порт" выбрать устройство, которое совпадает с тем, что было открыто в "Диспетчере устройств".<br>
   	На последок нужно залить прошивку в сферобота нажав на стрелочку "->" в программе. Прошивка должна залиться успешно.<br>
6) Скачиваем векторный редактор "Inkscape" и плагин для работы с Eggbot.<br>
		Скачиваем Inkscape с оффициального сайта https://inkscape.org/release/inkscape-0.92.4/ <br>
		Устанавливаем Inkscape.<br>
		Скачиваем по ссылке плагин. https://github.com/ProbotXYZ/EggBot/blob/master/Software/Inkscape_extension_only.zip <br>
		Разархивируем архив.<br>
		В папке "extensions" нужно отредактировать файл "ebb_serial.py", сделать это проще всего через редактор "Notepad++". Находим строчку с надписью "USB-SERIAL CH340" в скобках и меняем данные на "Arduino Uno (COM3)". (номер порта может отличаться)<br>
		Всё содержимое папки "extensions" нужно переместить в папку по пути C:\Program Files\Inkscape\share\extensions<br>
		Аналогично поступаем с содержимым папки "templates" в папку по пути C:\Program Files\Inkscape\share\templates<br>
7) Проверка работы Сферобота.<br>
		Запускаем Inkscape.<br>
		Нажимаем на вкладку "Файл" и выбираем "Создать по шаблону...".<br>
		В открывшемся окне выбираем "EggBot".<br>
		Рисуем что-нибудь, что помещается на шаблон и не выходит за его рамки.<br>
		Нажимаем на вкладку "Расширение" и выбираем "EggBot".
		Далее в появившемся окне выбираем "Применить". Сферобот должен начать двигаться.
</p>
                                                  <h2>Операционная система Raspbian</h2>
<p>1) Установим Arduino IDE.<br>
			sudo apt install arduino -y<br>
2) Скачаем xarchiver.<br>
			sudo apt install xarchiver -y <br>
3) Скачаем прошивку с сайта https://github.com/ProbotXYZ/EggBot/blob/master/Firmware/Firmware.zip <br>
		Разархивируем архив, нажав правой кнопкой мыши по нему и выбрав "Разархивировать в текущую папку".<br>
4) Заливаем прошивку в Сферобота. <br>
		Захожим в папку "EggDuino" и нажав правой кнопкой мыши по файлу "EggDuino.ino" выбираем пункт "Arduino IDE"<br>
		Нажимаем на стрелочку "->", чтобы залить прошивку. Прошивка должна залиться успешно.<br>
5) Скачиваем Inkscape.
			sudo apt inkscape -y
6) Скачиваем расширение с сайта https://github.com/ProbotXYZ/EggBot/blob/master/Software/Inkscape_extension_only.zip<br>
		Разархивируем архив.<br>
7) Отредактируем файл "ebb_serial.py"<br>
		Откроем файл.<br>
			nano /home/pi/Загрузки/extensions/ebb_serial.py <br>
		Находим строчку с надписью "USB-SERIAL CH340" и меняем данные на "/dev/ttyACM0/".<br>
		Нажимаем X, затем Y, затем Enter.
8) Переместим файлы с плагинами.
			sudo cp -r /home/pi/Загрузки/extensions/* /usr/share/inkscape/extensions/
			sudo cp -r /home/pi/Загрузки/templates/* /usr/share/inkscape/templates/
																								
<h1>Далее всё ломается, как раньше не получается	</h1>
		
</body>
</html>
