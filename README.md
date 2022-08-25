# esp32cam-dht11-g7
Este repositorio contiene los archivos para el ejercicio en clase que envía la información del DHT11 por MQTT a NodeRed
Material necesario:

   1. Micro controlador ESP32CAM
   2. Convertidor de niveles FTDI
   3. Cable USB-A a USB-mini
   4. Jumpers MM
   5. Protoboard
   6. Sensor DHT11
Software necesario:

   1. Ubuntu 20.04 o superior 
   2. Arduino IDE
        Gestor de tarjetas ESP32
        Configuración de la IDE de Arduino para trabajar con el ESP32CAM
        Biblioteca PubSubClient
   3. Mosquitto MQTT Broker
        Listener en puerto 1883 para 0.0.0.0 y conexiones no autentificadas activadas
   4. NodeJS
        NPM
        NodeRed
        Nodos Dashboard
Servicios necesarios:

   1. HiveMQ. Broker público.
   2. OpenWeatherMap. Servicio meteorolígico.

Se busca que tenga las siguientes funciones:

   1. Leer el sensor de temperatura y humedad DHT11
   2. Haga una conexión a una red WiFi
   3. Haga una conexión a un broker local (HiveMQ) para mandar mensajes por MQTT
   4. Envie los datos obtenidos del sensor DHT11 y convertirlos a un JSON
   5. Obtener los datos de humedad, temperatura, calidad de aire y UV de OpenWeather
   6. Convertir los datos anteriores a un JSON.
   7. Se recibirán los datos por MQTT en el tema codigoIoT/ejemplo/mqtt
   8. Se publicarán los datos por MQTT en el tema codigoIoT/ejemplo/mqttin
Instrucciones:
   1. Configurar la IDE de arduino para la ESP32CAM
   2. Tener el entorno de NodeJS configurado para trabajar con node-red y agregar los nodos correspondientes
   3. Tener el entorno de Mosquitto configurado para que acepte conexiones externas modificando el archivo mosquitto.conf activando las conexiones anonimas y el listener en el puerto 1883.
   4. Realizar la conexion del circuito conectando el ESP32CAM con el FTDI (GPIO1 a RX y GPIO3 a TX) y el DHT11 con el ESP32CAM (GPIO13 al segundo pin) y proporcionar la alimentacion necesaria para cada componente.
   5. Cargar el programa mediante la IDE de arduino haciendo los cambios correspondientes (red Wifi, pasword, temas al que se envia y recibe y la id del mensaje que se va a enviar).
   6. Arrancar node-red y cargar el flow (puedes acceder desde http://localhost:1880/ui) que se encuentra en este repositorio cambiando el tema de mqtt, la key proporcionada por openweather, coordenadas de donde se quiere obtener la información y la ip del broker.
   7. Observa el funcionamiento abriendo el dashboard de node-red.
Resultados:
Aqui podemos observar una captura de pantalla que muestra el dashboard con los datos del Grupo 7 del diplomado del internet de las cosas de codigoIoT.
![](https://github.com/ManuSV16/esp32cam-dht11-g7/blob/main/Screenshot%20from%202022-08-23%2013-51-33.png)
![](https://github.com/ManuSV16/esp32cam-dht11-g7/blob/main/Screenshot%20from%202022-08-23%2013-51-41.png)
 
   
