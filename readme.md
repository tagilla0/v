# Hi there, We are [vfsramfs](https://vk.com/id248266536) ![](https://github.com/blackcater/blackcater/raw/main/images/Hi.gif) 
### Students of Moscow Aviation Institute


## Краткое описание 
Программа на основе ядра Kaspersky OS , которая по  протоколу mqtt управляет alphabot на основе Raspberry Pi 4/

В папке mqtt_subscriber содержится программа в которой работает жесткая логика управления роботом через vодуль GPIO. Реализовали json парсер команд для управления роботом.
программа содержащаяся в файле cam.txt предоставляет доступ к web камере 
Программа PNP.cpp расписана логика калибровки камеры относительно точек 

## Отличительные особенности

Взаимодействие компонентов Kaspersky OS по ipc на основе сущностей.\
Исправлена ошибка взаимодействия GPIO с библиотекой, предоставляющей инструменты для взаимодействия с сетью в Kaspersky OS.\



## Проблемы при разработке 
Модуль GPIO робота под управлением Kaspersky OS содержал в себе одинаковые функции библиотеки работы с сетью.
Решением данной проблемы стало удаление инициализации BSP.\
Следующей проблемой стала неисправность wi-fi модуля в alphabot, что не позволяло подключить и запустить mqtt-брокер.
решением данной проблемы стала замена робота с исправным wi-fi модулем.

## Дальнейшее развитие проекта:
Улучшение политик безопасности \
Обеспечение защиты подключения к wi-fi сети (firewall, закрытое соединение, устойчивость к DDOS атакам, защита от MiTM-атак)\
Улучшение работы компьютерного зрения(калибровка камеры ,построение траектории относительно точек маршрута и сохранение ,пройденного маршрута роботом.

## Инструкции по запуску
![image](https://user-images.githubusercontent.com/117864353/202908165-75ee9150-b18a-426f-b159-dae33a7762d3.png)

forward - движение вперед\
back    - движение назад\
left    - поворот влево \
right   - поворот вправо \
stop    - полная остановка робота
