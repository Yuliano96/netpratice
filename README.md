*This project has been created as part of the 42 curriculum by ypacileo.*

## Description
This project is a networking training exercise focused on understanding and applying core TCP/IP concepts.
The goal is to correctly configure IP addresses, subnet masks, gateways, and routing rules so that all devices in a given network topology can communicate properly.

Through multiple levels, the project reinforces fundamental networking knowledge such as subnetting, routing logic, and the role of different network devices.

## Instructions

To solve this project, the student must:

* Download the file attached to the project's page.
* Extract the files in any folder they choose.
* In this folder, run the run.sh file (a shell script that will launch a webserver and open the dedicated page in their preferred web browser).
* Once the interface is open, the student should input their login to begin practicing with their personal configuration.
* The student will have to complete 10 levels and, for each level, export their configuration using the 'Get my config' button. Those files will later be turned in at the root of the repository, as mentioned in the submission part.

## Resources

### modelo TCP/IP

El modelo TCP/IP define cómo los dispositivos deben transmitir datos entre ellos y permite la comunicación a través de redes y grandes distancias. El modelo representa cómo se intercambian y organizan los datos en las redes. Se divide en cuatro capas, que establecen los estándares para el intercambio de datos y representan cómo se manejan y empaquetan los datos cuando se los entrega entre aplicaciones, dispositivos y servidores.

Las cuatro capas del modelo TCP/IP son las siguientes:

1. **Capa de enlace de datos:** la capa de enlace de datos define cómo se deben enviar los datos, maneja el acto físico de enviar y recibir datos y es responsable de transmitir datos entre aplicaciones o dispositivos en una red. Esto incluye definir cómo el hardware y otros dispositivos de transmisión deben señalar los datos en una red, como el controlador de dispositivo de una computadora, un cable Ethernet, una tarjeta de interfaz de red (NIC) o una red inalámbrica. Se la conoce también como la capa de enlace, capa de acceso a la red, capa de interfaz de red o capa física, y es la combinación de las capas de enlace físico y de datos del modelo de Interconexión de Sistemas Abiertos (OSI), que estandariza las funciones de comunicaciones en los sistemas informáticos y de telecomunicaciones.
2. **Capa de Internet:** La capa de Internet es responsable de enviar paquetes desde una red y controlar su movimiento a través de una red para garantizar que lleguen a su destino. Proporciona las funciones y los procedimientos para transferir secuencias de datos entre aplicaciones y dispositivos a través de las redes.
3. **Capa de transporte:** La capa de transporte es responsable de proporcionar una conexión de datos sólida y confiable entre la aplicación o el dispositivo original y su destino previsto. Este es el nivel en el que los datos se dividen en paquetes y se numeran para crear una secuencia. Luego la capa de transporte determina cuántos datos deben enviarse, a dónde deben enviarse y a qué velocidad. Garantiza que los paquetes de datos se envíen sin errores y en secuencia, y obtiene la confirmación de que el dispositivo de destino ha recibido los paquetes de datos.
4. **Capa de aplicación:** La capa de aplicación se refiere a programas que necesitan TCP/IP para ayudarlos a comunicarse entre sí. Este es el nivel con el cual los usuarios interactúan normalmente, como sistemas de correo electrónico y plataformas de mensajería. Combina las capas de sesión, presentación y aplicación del modelo OSI.

### modelo OSI

El modelo de interconexión de sistemas abiertos (OSI), también llamado modelo de referencia OSI, es un modelo conceptual que divide la comunicación y la interoperabilidad de la red en siete capas abstractas. Proporciona un modelo estandarizado que permite que diferentes aplicaciones, sistemas informáticos y redes se comuniquen.

En cada capa de la pila, que suele mostrarse en orden inverso para ilustrar cómo se mueven los datos a través de una red, el modelo OSI proporciona directrices y criterios para los componentes de la red y sus funciones informáticas únicas.

Las capas son:

1. **Capa 7:** la capa de aplicación inicia la comunicación con la red, incluidos los protocolos y los procesos de manipulación de datos que convierten los datos de red legibles por ordenador en respuestas legibles por el usuario.
2. **Capa 6:** la capa de presentación prepara los datos para la capa de aplicación, incluyendo la traducción de datos, la compresión y el cifrado.
3. **Capa 5:** la capa de sesión inicia y termina las conexiones entre dos dispositivos que interactúan en la red, asegurándose de que los recursos no se utilicen en exceso ni se infrautilicen.
4. **Capa 4:** la capa de transporte transmite datos de extremo a extremo entre dos dispositivos que interactúan en la red, asegurándose de que los datos no se pierdan, no estén mal configurados ni se dañen.
5. **Capa 3:** la capa de red gestiona los procesos de dirección, enrutamiento y reenvío de datos para los dispositivos que interactúan en diferentes redes. Si los dispositivos están en la misma red, no necesitan la capa de red para interactuar.
6. **Capa 2:** a diferencia de la capa de red, la capa de enlace de datos gestiona el enrutamiento de datos entre dos dispositivos que interactúan en la misma red.
7. **Capa 1:** la capa física comprende los activos físicos, como enrutadores y cables USB, que convierten los datos en cadenas de 1 y 0 para su transmisión a capas superiores.

## Mascara de subred

El segundo elemento necesario para el funcionamiento de TCP/IP es la máscara de subred. El protocolo TCP/IP utiliza esta máscara para determinar si un host está en la subred local o en una red remota.

En TCP/IP, las partes de la dirección IP que se utilizan como direcciones de red y host no son fijas. A menos que se disponga de más información, no se pueden determinar las direcciones de red y host mencionadas. Esta información se proporciona en otro número de 32 bits llamado máscara de subred. En este ejemplo, la máscara de subred es 255.255.255.0. No es evidente el significado de este número a menos que se sepa que 255 en notación binaria equivale a 11111111. Por lo tanto, la máscara de subred es 11111111.111111111.11111111.00000000.

Al alinear la dirección IP y la máscara de subred juntas, las partes de red y host de la dirección se pueden separar:

11000000.10101000.01111011.10000100 - Dirección IP (192.168.123.132)
11111111.11111111.11111111.00000000 - Máscara de subred (255.255.255.0)

Los primeros 24 bits (el número de unos en la máscara de subred) se identifican como la dirección de red. Los últimos 8 bits (el número de ceros restantes en la máscara de subred) se identifican como la dirección de host. Esto proporciona las siguientes direcciones:

11000000.10101000.01111011.00000000 - Dirección de red (192.168.123.0)
00000000.00000000.00000000.10000100 - Dirección de host (000.000.000.132)

# Puertas de enlaces

Si una computadora TCP/IP necesita comunicarse con un host en otra red, generalmente lo hará a través de un dispositivo llamado enrutador. En términos de TCP/IP, un enrutador especificado en un host, que conecta la subred de este con otras redes, se denomina puerta de enlace predeterminada. Esta sección explica cómo TCP/IP determina si envía paquetes a su puerta de enlace predeterminada para llegar a otra computadora o dispositivo en la red.

Cuando un host intenta comunicarse con otro dispositivo mediante TCP/IP, realiza una comparación entre la máscara de subred definida y la dirección IP de destino y la máscara de subred y su propia dirección IP. El resultado de esta comparación indica al equipo si el destino es un host local o remoto.

Si el resultado de este proceso determina que el destino es un host local, el equipo enviará el paquete a la subred local. Si el resultado de la comparación determina que el destino es un host remoto, el equipo reenviará el paquete a la puerta de enlace predeterminada definida en sus propiedades TCP/IP. El enrutador es responsable de reenviar el paquete a la subred correcta.

## Router

Un router es un dispositivo encargado de reenviar los paquetes de datos entre diferentes redes. Generalmente, una de ellas es local (LAN) y la otra externa, la cual utiliza un puerto WAN para establecer conexión con la fibra óptica o la ADSL y desde ahí con internet.

Los routers se utilizan para escoger la ruta más corta para que un paquete de datos llegue a su destino. ¿Cómo lo consiguen? Valiéndose de un protocolo de enrutamiento que posibilita su comunicación con otros enrutadores y les permite compartir información entre sí.

De este modo, este tipo de dispositivos permite que los ordenadores puedan conectarse a redes externas sin limitar su conexión a una red local. Son los dispositivos que posibilitan que los ordenadores se conecten a internet

## Switch

Los switches son dispositivos utilizados para crear redes de conexión locales. Con los switches, los paquetes de datos enviados por el ordenador de origen se dirigen directamente al ordenador de destino, pero no se replican en el resto de ordenadores que haya conectados a la red local. Estos pueden continuar enviándose paquetes de datos entre sí mientras se producen esas mismas transmisiones entre otros ordenadores de la red.

Podríamos decir que el switch se utiliza para conectar directamente diferentes dispositivos entre sí. Simplemente, almacenan el paquete de datos recibido, lo procesan con el fin de establecer su dirección de destino y finalmente, lo reenvían a ese destino determinado. De este modo, se crea un canal de comunicación exclusivo entre el ordenador de origen y el de destino.

Para que la comunicación entre ordenadores sea segura y efectiva, los switches aprovechan las direcciones MAC, las cuales permiten identificar a los PC interconectados y así, evitar errores de red, reducir el tráfico y direccionar de manera más eficiente los enlaces de datos.

## AI tools were used to:

Clarify networking theory (subnetting, routing, gateways).

Validate logical reasoning while solving networking configurations.

Improve explanations and documentation clarity.

AI tools were not used to automatically generate final solutions without understanding.

##Submission details

Because 10 levels are available in the training interface, the student must remember to enter their own login in the training interface, export 1 file per level using the 'Get my config' button, and turn them all in at the root of the repository. Additionally, an English written README.md file for the project must be uploaded in the same folder.

## bibliogragia

- https://www.fortinet.com/lat/resources/cyberglossary/tcp-ip
- https://learn.microsoft.com/en-us/troubleshoot/windows-client/networking/tcpip-addressing-and-subnetting
- https://www.geyma.com/blog/diferencia-router-switch/

##tutoriales

- https://www.youtube.com/watch?v=9k7TteZaXms&list=PLg9145ptuAijivEI4t0cb31FA41zqclwO
- https://www.youtube.com/watch?v=wksPyiU1BvE&list=PLbcS-eIZbbxWSCANJXiXj_5zBriR81m54



