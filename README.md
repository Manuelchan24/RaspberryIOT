# IoT Temperature Monitoring

Este proyecto permite el monitoreo de temperatura en tiempo real utilizando una Raspberry Pi Pico W y un sensor LM35. Los datos son enviados a **ThingSpeak** y analizados con **MathWorks**.

## 📌 Características
✅ Monitoreo de temperatura en la nube.  
✅ Uso de **ThingSpeak** para visualización.  
✅ Análisis de datos con **MathWorks**.  
✅ Alertas cuando la temperatura supera los 35°C.  

## 🛠 Requisitos
- Raspberry Pi Pico W
- Sensor de temperatura LM35
- Conexión a Internet (Wi-Fi)
- Cuenta en ThingSpeak

## 📊 Visualización en ThingSpeak
1. Crea un canal en **ThingSpeak**.
2. Configura un gráfico para **Field1** (temperatura).
3. Usa **MATLAB Analysis** para calcular el promedio de temperatura.

## 🛠 Instalacion del Dispositivo
1. Conecta el pin [1] VCC del LM35 al pin 40 (VBUS, 5V) de la Raspberry Pi Pico W.
2. Conecta el pin [2] VOUT del LM35 al GP26 (ADC0) de la Raspberry Pi Pico W.
3. Conecta el pin [3] GND del LM35 al GND (Pin 38) de la Raspberry Pi Pico W.

## 📌 Consideraciones Importantes
- El LM35 opera con 5V, por lo que debe conectarse a VBUS (5V) y no a 3.3V.
- El GP26 es un pin ADC (convertidor analógico-digital), lo que permite leer la salida del LM35 correctamente.
- Verifica que las conexiones sean firmes y que los cables estén bien sujetos para evitar lecturas erróneas.

