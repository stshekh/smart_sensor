# Учебный план: создание IoT-устройства для измерения загрязнённости воздуха

## 🎯 Цель
Создать MVP устройства, максимально близкого к промышленному варианту: измерение PM2.5/PM10, CO₂, VOC, температура, влажность, Wi-Fi/Ethernet/PoE, передача данных на сервер, настройка с телефона, GPS-метки.  
Есть опыт Java и базовый C++ → акцент на Embedded/IoT.

---

# 1. Основы Embedded и микроконтроллеров

## Литература
- **Programming Embedded Systems in C and C++ (O’Reilly)**  
  https://www.oreilly.com/library/view/programming-embedded-systems/0596009836/
- **Making Embedded Systems — Elecia White**  
  https://www.oreilly.com/library/view/making-embedded-systems/9781449308889/
- **The Definitive Guide to ARM Cortex-M3 and Cortex-M4 — Joseph Yiu**  
  https://www.elsevier.com/books/the-definitive-guide-to-arm-cortex-m3-and-cortex-m4-processors/yiu/978-0-12-408082-9

## Видео
- Основы embedded:  
  https://youtube.com/playlist?list=PLZyvi_9gamL-EE3aF2RZQBPdZi8WixP0j
- EEForEveryone (электроника):  
  https://www.youtube.com/@EEforEveryone

---

# 2. Платформы для быстрого старта: ESP32 и STM32

## Литература
- **Kolban's Book on ESP32 (бесплатно)**  
  https://leanpub.com/kolban-ESP32
- **Mastering STM32 — Carmine Noviello**  
  https://leanpub.com/mastering-stm32
- **Embedded Systems Architecture — Daniele Lacamera (2nd Edition)**
  Отличная книга для понимания архитектуры, RTOS, IoT протоколов и построения профессиональных прошивок.
  https://www.packtpub.com/product/embedded-systems-architecture-second-edition/9781788832502
  https://www.oreilly.com/library/view/embedded-systems-architecture/9781803239545/

## Видео
- ESP32 полный курс:  
  https://www.youtube.com/watch?v=8KehQy2bFqY
- STM32 bare metal:  
  https://www.youtube.com/playlist?list=PLnMKNibPkDnGg-h1PzvAn4y1nGWu29B8J

---

# 3. C/C++ для Embedded

## Литература
- **K&R — The C Programming Language**  
  https://archive.org/details/the-c-programming-language-2nd-edition
- **Modern C — Jens Gustedt**  
  https://modernc.gforge.inria.fr/

## Видео
- Harvard CS50:  
  https://cs50.harvard.edu/x/2024/
- C Programming Playlist:  
  https://youtu.be/KJgsSFOSQv0

---

# 4. Электроника и схемотехника

## Литература
- **Practical Electronics for Inventors**  
  https://www.mhprofessional.com/practical-electronics-for-inventors-9781259587542-usa
- **Make: Electronics — Charles Platt**  
  https://www.oreilly.com/library/view/make-electronics-3rd/9781680456939/

## Видео
- GreatScott!  
  https://www.youtube.com/@greatscottlab
- Afrotechmods  
  https://www.youtube.com/@afrotechmods

---

# 5. Датчики: PM, CO₂, VOC, t/h

## Рекомендуемые сенсоры
- PM2.5/PM10: **PMS5003**, **SPS30**  
- CO₂: **SCD30**, **SCD41**  
- VOC: **CCS811**, **BME688**  
- Температура/влажность: **SHT31/35**, **BME280/680**

## Документация
- SPS30:  
  https://sensirion.com/products/catalog/SPS30
- SCD41:  
  https://sensirion.com/products/catalog/SCD41

## Видео
- PM sensors explained:  
  https://youtu.be/_5vz6H0XN1k

---

# 6. Связь: Wi-Fi, BLE, PoE, MQTT, HTTP

## Литература
- **MQTT Essentials** (бесплатно)  
  https://www.hivemq.com/mqtt-essentials/
- **Designing Connected Products**  
  https://www.oreilly.com/library/view/designing-connected-products/9781449320539/

## Видео
- MQTT course:  
  https://www.youtube.com/playlist?list=PLRMyLrP--5E9yJzN6FIuV2wP7L8GkS6hf
- ESP32 Wi-Fi/BLE:  
  https://www.youtube.com/watch?v=wN0ekqT0qPw

---

# 7. ПО сервера (Backend, MQTT broker, БД)

### Рекомендуемый стек:
- MQTT broker: **Mosquitto**  
- База: **InfluxDB** или **PostgreSQL**  
- Backend: **Java + Spring Boot**  
- Dashboard: **Grafana** или собственное приложение

## Видео
- InfluxDB + Grafana:  
  https://youtu.be/vJZ6el7dBFM
- MQTT → InfluxDB pipeline:  
  https://youtu.be/QxpluZb3IIE

---

# 8. UX: настройка устройства с телефона

## Подходы для MVP
1. Wi-Fi provisioning через ESP32 SoftAP  
2. BLE provisioning  
3. QR-код добавления устройства  
4. GPS от мобильного приложения

## Видео
- ESP32 provisioning demo:  
  https://youtu.be/Ok0U4xUeyFE

---

# 9. Корпус и сборка устройства

## Литература
- **Designing Embedded Hardware — O’Reilly**  
  https://www.oreilly.com/library/view/designing-embedded-hardware/0596007558/
- Thermal и airflow основы:  
  https://www.electronics-cooling.com/

## Видео
- Введение в 3D-печать:  
  https://www.youtube.com/watch?v=D5nwz3pT0b0

---

# 10. Архитектура и список задач для MVP

## MVP устройства
- MCU: **ESP32 или ESP32-C6**  
- Сенсоры: PMS5003 + SHT31 + CCS811 (или BME688)  
- Питание: USB 5В или PoE через сплиттер  
- Протокол: **MQTT**  
- OTA-обновления  
- Wi-Fi SoftAP настройка  
- GPS с мобильного приложения  
- Backend на Spring Boot  
- UI: веб (React) + мобильный (Expo/FlutterFlow)

---

# План обучения по неделям

## Недели 1–2
- База embedded + C  
- Читаешь: K&R, Kolban ESP32  
- Практика: GPIO, I2C, UART

## Недели 3–4
- Подключение датчиков  
- Архитектура прошивки  
- OTA обновления

## Недели 3–4 (дополнение)
- Чтение "Embedded Systems Architecture — Lacamera"
- Проработка архитектуры прошивки, RTOS, планировщики
- Разработка каркаса прошивки для будущего MVP

## Недели 5–6
- MQTT  
- Provisioning  
- Логирование, буферизация данных

## Недели 7–8
- Backend + InfluxDB/PostgreSQL  
- MQTT ingestion  
- UI для визуализации данных

## Недели 9–10
- Корпус  
- Питание (включая PoE)  
- Финальная сборка MVP

## Недели 11–12
- Тестирование  
- Оптимизация  
- Подготовка к полевым испытаниям
