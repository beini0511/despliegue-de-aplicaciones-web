 despliegue-de-aplicaciones-web
# 3.  Analiza los headers de las peticiones cuando inicias sesión en el Moodle y comprende cómo se obtiene el token. Para ello, necesitamos saber de dónde salen TODOS los datos sensibles que se envían.

el token de el index.php se obtiene en el apartado de network, entras dentro del index.php y te vas al apartado de payload y ahi es donde sale el login token
![image](https://github.com/user-attachments/assets/33b20c3a-5298-4b4d-ab8a-d26cb0cfcf73)

# 4. ¿A qué puerto se reciben normalmente las peticiones del protocolo HTTP? ¿A qué capa del modelo TCP/IP se encuentra el protocolo HTTP? ¿Y los protocolos TCP, UDP, e IP?

Puerto del protocolo HTTP: Normalmente, el protocolo HTTP utiliza el puerto 80. El servicio HTTPS se ejecuta en el puerto 443.

Capa en el modelo TCP/IP:

- HTTP reside en la capa de aplicación del modelo TCP/IP.
- TCP y UDP existen en la capa de transporte.
- IP se encuentra en la capa de red.
# 5. ¿Cuál es el significado de la siguiente respuesta de un servidor? HTTP/1.1 302 Found Location: http://www.example.com/test/index2.php

El código de estado 302 Found es una respuesta de redirección. Específicamente, el código indica que el recurso necesitado está ubicada en otra URL de manera temporal. Por consiguiente, el Cliente debe hacer una nueva solicitud a la URL que se encuentra en el header de Location que en este caso es: `http://www.example.com/test/index2.php`. Como se puede entender, esta respuesta no es para que el cliente sepa que la ubicación permanentemente ha cambiado, para el servidor ya que la destino original no es valida, pero en futuro tal vez será valida nuevamente. Un ejemplo de su aplicación es cuando el servidor quiere redirigir al usuario a otra pago temporalmente, tal vez luego de un login exitoso.

# 6.  Utilizando el filtro de captura para la interfaz de red de Wireshark, analiza la petición al host: www.google.com.  Mostrando la cabecera IP, la dirección IP de tu ordenador y la del servidor. Comprueba que, poniendo esa IP en el navegador, accedas a Google.

para este ejercicio lo primero que he hecho ha sido instalar wireshark, dentro de wireshark he entrado en la interfaz de wifi (que es a la que estoy conectada). Luego he ido a la parte de filtro y he puesto DNS y le he dado a filtrar hasta encontrar la linea donde sale google, he ido a mi navegador y he puesto el 8.8.8.8 y me ha entrado en google.

![image](https://github.com/user-attachments/assets/ab5671a1-b10f-460c-b295-fc623c3a9699)
![image](https://github.com/user-attachments/assets/80380fe6-247e-479b-a306-3480e2e00ffa)
