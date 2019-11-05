# DHCP-SERVER-CONFIG
Tutorial de como instalar y configurar servidor DHCP, tanto en Linux como en Ubuntu

## Indice

1. [¿Que es un servidor DHCP?](#¿Que-es-un-servidor-DHCP?)
2. [¿Como funciona?](#¿Como-funciona?)
3. [Rquisitos](#Requisitos).
### ¿Que es un servidor DHCP?

- El DHCP es una extensión del protocolo Bootstrap (BOOTP) desarrollado en 1985 para conectar dispositivos como terminales y estaciones de trabajo sin disco duro con un Bootserver, del cual reciben su sistema operativo. El DHCP se desarrolló como solución para redes de gran envergadura y ordenadores portátiles y por ello complementa a BOOTP, entre otras cosas, por su capacidad para asignar automáticamente direcciones de red reutilizables y por la existencia de posibilidades de configuración adicionales.

### ¿Como funciona?

- El servidor DHCP escucha las solicitudes de los clientes, aparte tiene unas tablas con las posibles direcciones IP a asignar. Cuando un cliente DHCP se conecta a la red envía una solicitud en forma de mensaje de broadcast o difusión. Todos los posibles servidores DHCP que han recibido la solicitud responden al cliente asignandole una direccion IP. El cliente acepta una de ellas (la primera que recibe) y se lo comunica al servidor elegido, el cual le contesta con un mensaje que incluye la cabecera MAC del cliente, la dirección IP y la máscara de subred asignada, la dirección IP del servidor y el período de validez (lease o concesión) de la dirección IP. Esta información continúa asociada al cliente mientras éste no desactive su interfaz de red o no finalice el tiempo de asignación (lease time).

### Requisitos
A poder ser utilizar estos requisitos para que funcione al 100%:
- [Virtual vox](https://www.virtualbox.org/wiki/Downloads).
- Iso Windows 2012 Server.
- [Iso UbuntuServer 18.04 lts](https://ubuntu.com/download/server).

### Configuración con Windows 2012 Server

### Configuración con Ubuntu Server

#### Prepararando la maquina virtual
#### Indice
- [Configuracion principal de la maquina virtual](#Configuracion-principal-de-la-maquina-virtual)
Lo primero es crear la maquina virtual obviamente:

- **Nombre:** EJ(UbuntuServer).
- **Carpeta de máquina(donde se va a almacenar la maquina virtual):** EJ(C:\Users\VuestroUsuario\VirtualBox VMs, es la ruta por defecto yo no la he tocado).
- **Tipo:** Linux.
- **Version:** Ubuntu(64-bit).
- **RAM:** con 1818 MB va sobrado.
- **Tipo de disco duro:** VHD(Virtual Hard Disk).
- **Tipo de almacenamiento:** Reservado Dinamicamente y no hay que esperar a que se cree el disco duro, con unos 15-20 GB de almacenamiento irá perfecto.
##### Configuracion principal de la maquina virtual
![Configuracion de virtual box](Screenshots/ubuntuVBoxConfig1.PNG)
##### Configuracion de la RAM
![Configuracion de virtual box](Screenshots/ubuntuVBoxConfig2.PNG)
##### Configuracion del disco duro
![Configuracion de virtual box](Screenshots/ubuntuVBoxConfig3.PNG)
