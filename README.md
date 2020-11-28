# Hackathon-MSTU-STANKIN

[![N|Solid](https://images-ext-1.discordapp.net/external/NdmgWy6xtpQzabOfffVcNDvS8tPiwunbaRklhy5TbzQ/http/s.pmelikov.ru/stankin_logo.png)](https://stankin.ru/)

## Описанние

Cистема прогнозирования потребления электроэнергии за счет плановых экономических и погодных данных.
Уникальность: Используем интеграцию в ERP системы предприятий для сбора плановых показателей производства, а также парсим погодные данные для прогноза потребления электроэнерги

**Стек решения:** *python, flask, grapghana, InfluxDB, JS, TensorFlow*

## Необходимое окружение

#обновление системы
sudo apt-get update

#Установка интерпретатора и менеджера пакетов pip языка Python
sudo apt-get install -y python3-dev=3.6.7-1\~18.04 python3-pip=9.0.1-2.3\~ubuntu1.18.04.1 graphviz=2.40.1-2

pip3 install --user 'tensorflow==2.0.0b1' 'matplotlib==3.1.2' 'keras== 2.3.1' 'numpy==1.16.4' 'pydot==1.4.1' 'testresources'




•	Интерпретатор Python3 (версия 3.6.7);
•	Pip3 – менеджер пакетов языка Python3 (версия 9.0.1);
•	Утилита визуализации графов Graphviz – graphviz (версия 2.40.1).
•	Git – распределенная система управления версиями (любая версия);
•	Virtualenv – утилита, которая позволяет создавать изолированные виртуальные окружения для Python и работать с ними (любая версия);
•	Pillow – расширенная версия стандартной библиотеки для работы с изображениями в Python (англ. Imaging Library Python), которая добавляет некоторые возможности обработки изображений для интерпретатора (версия 5.1.0);
•	Jupyter notebook – графическая веб-оболочка для Python, которая расширяет идею консольного подхода к интерактивным вычислениям (версия 1.0.0);
•	Matplotlib – библиотека для визуализации данных 2D и 3D графики (версия 3.1.2);
•	numpy – математическая библиотека (поддержка многомерных массивов и высокоуровневых математических функций над ними, версия 1.16.4);
•	keras – нейросетевая библиотека, являющаяся надстройкой над фреймворками Deeplearning4j, TensorFlow и Theano (версия 2.3.1);
•	numpy – математическая библиотека (поддержка многомерных массивов и высокоуровневых математических функций над ними, версия 1.16.4);
•	pydot – интерфейс для работы Graphviz (визуализация графов, версия 1.4.1).

### UBUNTU 18.04
1) Обновление системы
sudo apt-get update

2) Установка интерпретатора и менеджера пакетов pip языка Python
sudo apt-get install -y python3-dev=3.6.7-1\~18.04 python3-pip=9.0.1-2.3\~ubuntu1.18.04.1 graphviz=2.40.1-2

3) Установка необходимых пакетов(!!!ВНУТРИ ВИРТУАЛЬНОЙ СРЕДЫ!!!)
pip3 install 'tensorflow==2.0.0b1' 'matplotlib==3.1.2' 'keras== 2.3.1' 'numpy==1.16.4' 'pydot==1.4.1' 'testresources' 'matplotlib==3.2.1' 'cython==0.29.16' 'contextlib2==0.6.0' 'jupyter==1.0.0' 'numpy==1.16.4' 'pandas==1.0.3'

4) Graphana
sudo apt-get install -y apt-transport-https
sudo apt-get install -y software-properties-common wget
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
sudo apt-get update
sudo apt-get install grafana

5) influx
wget -qO- https://repos.influxdata.com/influxdb.key | sudo apt-key add -
source /etc/lsb-release
echo "deb https://repos.influxdata.com/${DISTRIB_ID,,} ${DISTRIB_CODENAME} stable" | sudo tee /etc/apt/sources.list.d/influxdb.list
sudo apt-get update && sudo apt-get install influxdb
sudo service influxdb start

## Скрипты

### 1_create_train_and_save_pretrained_model
Скрпит для: создания, обучения нейросети, сохранение её полной модели и результатов зависимостей

### 2_DB_WRITER

Скрипт парсинга данных с различных источников, записи их в БД и записи предсказаний в БД

### 3_load_model

Скрипт загрузки обученной модели, и интерактивного предсказания по требуемым входным параметрам

## Дашборд

Импортировтаь Dashboard.json в графану

## Файлы настроек

### graphana

Заменить /etc/graphana/grafana.ini на предложенный

### influxdb

Заменить /etc/influxdb/influxdb.conf на предложенный

## Файлы данных
WEATHER.csv - погода за 2 года
predictions.txt - предсказания из обученной нейросети на год

