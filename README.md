# Monitoreo de Temperatura con Raspberry Pi Pico W y ThingSpeak

Este proyecto implementa un sistema IoT para medir temperatura usando una Raspberry Pi Pico W y un sensor LM35. Los datos son enviados a ThingSpeak para su almacenamiento y visualización. Además, se utiliza MathWorks en ThingSpeak para analizar los datos y generar alertas si la temperatura supera los 35°C.

## 📌 Características
✅ Monitoreo de temperatura en la nube.  
✅ Uso de **ThingSpeak** para visualización.  
✅ Análisis de datos con **MathWorks**.  
✅ Alertas cuando la temperatura supera los 35°C.  

## 🛠 Requisitos
- Raspberry Pi Pico W
- Sensor de temperatura LM35
- Cables de conexión
- Fuente de alimentación USB para la Raspberry Pi Pico W
- Cuenta en ThingSpeak
- MicroPython instalado en la Raspberry Pi Pico W
- MATLAB en ThingSpeak para análisis de datos

## 🛠 Instalacion del Dispositivo
1. Conecta el pin [1] VCC del LM35 al pin 40 (VBUS, 5V) de la Raspberry Pi Pico W.
2. Conecta el pin [2] VOUT del LM35 al GP26 (ADC0) de la Raspberry Pi Pico W.
3. Conecta el pin [3] GND del LM35 al GND (Pin 38) de la Raspberry Pi Pico W.
4. Verificar las conexiones antes de alimentar la Raspberry Pi Pico W.

## 📌 Consideraciones Importantes
- El LM35 opera con 5V, por lo que debe conectarse a VBUS (5V) y no a 3.3V.
- El GP26 es un pin ADC (convertidor analógico-digital), lo que permite leer la salida del LM35 correctamente.
- Verifica que las conexiones sean firmes y que los cables estén bien sujetos para evitar lecturas erróneas.

## 💻 Configuración del Código en MicroPython
1.Descargar los códigos desde la carpeta "Codigos" de este repositorio.
2. Modificar los parámetros en el archivo correspondiente:
    - Wi-Fi SSID y contraseña.
    - API Key y Channel ID de ThingSpeak.
3. Subir y ejecutar el código en la Raspberry Pi Pico W.

## 📊 Visualización en ThingSpeak
1. Crear una cuenta en ThingSpeak.
2. Crear un nuevo canal y asignar un campo para la temperatura.
3. Copiar y configurar el API_KEY y CHANNEL_ID en el código.
4. Configurar gráficos en ThingSpeak para visualizar los datos en tiempo real.

## 📈 Configuración en MathWorks

1. Ir a Apps → MATLAB Analysis en ThingSpeak.
2. Crear un nuevo análisis y copiar el código desde la carpeta "Codigos".
3. Modificar channelID y readAPIKey con los valores correctos.
4. Guardar y ejecutar el análisis para obtener el promedio de temperatura y recibir alertas si supera 35°C.
