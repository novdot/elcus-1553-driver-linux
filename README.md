# elcus-1553-driver-linux
Копия драйвера с сайта elcus.ru, собирающаяся под ядра третьей версии (проверено на 3.16.7), дополнено примером.

Драйвер собирается с поддержкой потоков (приложения, использующие драйвер могут быть многопоточными)

Для сборки драйвера выполните

cd driver
chmod +x make3
./make3


В случае удачной компиляции можно загрузить драйвер используя скрипт loaddrv

./loaddrv


В этом случае будет автоматически создано устройство /dev/tmk1553b. Скрипт передает в модуль параметры d0=1 t0="TAI" misc=1 , тем самым предназначен для работы с платами типа TA, для настройки других плат смотрите оригинальные readme