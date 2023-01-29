# HackNotes
Estos apuntes requieren de poder tener un laboratorio donde testear y cacharrear cada uno de los diferentes herramientas y ataques que se llevan a cabo a través de las `HackNotes`.

**solo modifico esto**
Para esto, se recomienda configurar el conocido [DETECTIONLAB](https://detectionlab.network/deployment/). 

<img width="409" alt="image" src="https://user-images.githubusercontent.com/72032027/215297252-cc721820-c444-4a0c-8ab7-9db4e75bb1bf.png">

A continuacion, se provee un breve manual de instalación de dicho entorno a través de una máquina Windows con VMware. Cualquier otro tipo de instalacíon se puede consultar el manual de despliegue de la herramienta en la página oficial.

**Note:** *Antes de continuar confirma que tu ordenador cuenta con los prerequisitos necesarios para desplegar este laboratorio.*

### VMware Fusion/Workstation
DetectionLab se implementa en la máquina local como máquinas virtuales de VMware individuales.
+ Windows, Linux, and MacOS are all supported
+ VMware Fusion or Workstation (It must be registered, trials will not work)
+ The VMware Desktop Vagrant Plugin
+ The Vagrant VMware Utility must be installed
+ 55GB+ of free disk space
+ 16GB+ of RAM highly recommended
+ Vagrant 2.2.9+
+ Packer 1.6.0+ (only required if building your own boxes)
+ VMware Fusion 11+ or Workstation 15+ (older versions may work but are not tested)

## Vagrant Installation
Para el caso, una de las formas más sencillas de desplegarlo es a través de Vagrant. Para ello deberemos de acudir a su [página](https://developer.hashicorp.com/vagrant/downloads) y descargar el instalador adecuado. En este caso descargaremos el binario para `AMD64`.

![image](https://user-images.githubusercontent.com/72032027/215297340-d7151587-bb3e-4d23-9ff1-46b94ca1e6a7.png)

Una vez descargado, deberemos de instalarlo en nuestro sistema siguiendo las indicaciones del instalador hasta que finalice la instalación de Vagrant (En este punto se recomienda reiniciar el equipo).

### VMWare Desktop Vagrant Plugin Installation
En este punto se debe de tener Vagrant de forma obligatoria. La instalación del plugin para gestionar VMWare a través de Vagrant se puede instalar con el siguiente comando.

```sh
vagrant plugin install vagrant-vmware-desktop
```

Para que el plugin funcione, obligatoriamente debe de estar instalado `Vagrant VMware Utility`.

### Vagrant VMware Utility Installation
Esta utilidad es sencilla de instalar. Unicamente debes de acceder a su [página](https://developer.hashicorp.com/vagrant/downloads/vmware), descargar el instalador y seguir las instrucciones de instalación y esperar hasta que finalice.

![image](https://user-images.githubusercontent.com/72032027/215297816-14d3aa47-9038-4135-a869-547e00875423.png)

`Importante`: Si en tu máquina tienes VirtualBox y VMware, tienes que deshabilitar los adaptadores de red de VirtualBox para poder continuar con esta instalación en VMware.

## Clone Repo and Prepare Environment
En este punto puedes ubicarte en la ruta que más prefieras para poder clonar el repositorio de DetectionLab. Recomiendo crear una carpeta llamada `Lab` en la ruta `C:\User\<user.name>\Lab`.

```sh
git clone https://github.com/clong/DetectionLab.git
```

Una vez clonado correctamente, navega hacia la ruta `DetectionLab/Vagrant` del repositorio y ejecuta `.\prepare.ps1` para verificar si el sistema tiene todos los prerequisitos instalados y correctamente funcionando. ***Deberías de tener una salida similar a la mostrada a continuación***.

![image](https://user-images.githubusercontent.com/72032027/215298199-44d29b23-961c-4912-bc61-95787ed98d95.png)

## Environment Installation

