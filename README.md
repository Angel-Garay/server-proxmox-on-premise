# server-proxmox-on-premise
Este repo tiene la intención de ser la Intro o un Manual de como crear un laboratorio on-premise con Proxmox  
Para trabajar de Administracion de Sistemas por lo general nos piden que sepamos de diferentes herramientas y Proxmox es una de esas herramientas bases en la cual casi todas las demas se sustentan.  
Por eso considero importante hablar en este repo sobre como es Instalar y Configurar Proxmox VE. Luego creame otros repos que sirven para completar este repo principal.

### Contenido
  
#### 1 - Introducción general  
Objetivo del manual 
- Para trabajar como SysAdmin o Administrador de Sistemas nos piden que sepamos de varias aplicaciones, Sistemas Operativos, protocolos, redes, dispositivos y herramientas. Proxmox VE es una de esas herramientas que sirve para trabajar con algunas de esas aplicaciones. Por ejemplo para practicar con un servidor de Linux podemos usar una PC vieja que no usemos y luego de algunos "ajustes" podemos darle el uso de "servidor" a la PC (de hecho tengo un repo que explica como hacerlo).
- En este caso Proxmox VE nos permite crear mas de 1 servidor dentro de 1 PC Server con Proxmox VE instalado  
  
Requisitos básicos y Disclaimer  
- Simplemente ser sincero con el que esta leyendo, si bien 1 PC viejo se puede usar como "server", en el caso de Proxmox VE yo tengo 1 PC con 12 hilos y 16 ram y 1 solo disco de 500 ssd tengo que ser honesto: es escaso y por eso tengo que practicar y crear aplicaciones de forma separada. Esto significa que puede ser que lleguemos a un limite brevemente dependiendo de lo que queramos crear en nuestros laboratorios.
- Quizas nos comentan que para estudiar con cualquier PC es suficiente y yo realmente considero que si bien se puede estudiar con 1 PC humilde en recursos, igual asi no sirve para trabajar con herramientas como las que estoy comentando ahora.
- Proxmox VE nos permite tener dentro de 1 PC varios "nodos" o "VM" maquinas virtuales. Trabajar con ambas a la par considero que es lo importante para saber como se comunican cada una de estas herramientas  
  
Estructura de los tutoriales
- Es muy extenso volcar en un repo todo lo que hay que tener en cuenta. Por eso voy a linkear a este repo "Principal" los demas repos que van a tener la funcion de completar la documentacion
  
### 2 - Proxmox VE  
Instalación y configuración inicial  
- 1: Tener un cable de red (RJ45) y el Router cerca de nuestro Setup, o la Pc-Notebook-MiniPc que hagamos de Servidor hay que dejarla encendida cerca del router
- 2: Descargar la ISO de Proxmox VE
- 3: Tener un Pendrive USB con Proxmox VE instalado (recomiendo mucho hacerlo con Ventoy, si no se conoce sobre la herramienta es importante hacerlo ahora)
- 4: Hacer Backup de los datos que pudieran ser importantes y que estan todavia en el futuro "Servidor"
- 5: Investigar como "bootear desde USB" en la PC que vamos a instalar Proxmox VE (En cada PC se hace de forma distinta)
- 6: Prendemos la PC y tenemos que entrar a la BIOS para:
  - a: Activar la UEFI (si se puede)
  - b: Habilitar virtualizacion (VT-x, AMD-V)
  - c: Desactivar Secure Boot
- 6: Prender la PC y bootear desde el USB vamos a ver Ventoy que nos da a elegir que Sistema Operativo instalar.
- 7: Elegir en que disco se instalara
- 8: Elegir el FyleSystem o Sistema de Archivos: ext4 (recomiendo mucho hacerlo con este sistema al principio)
- 9: Configurar region y contraseña para root: elegir una fuerte contraseña (sin simbolos ni tildes)
- 10: Poner "IP fija" que nos recomienda el Sistema, Gateway del router, DNS de Cloudflare o Google.
- 11: Nos quedaria esperar a que termine la instalacion, cuando termine verificar que entre el reinicio y el encendido nuevamente nos da un tiempo para sacar de forma segura nuestro Pendrive  
Acceso web  
- 12: Desde otra PC ir a: http:IP:8006)
- 13: Poner contraseña de root y una vez dentro en la parte del nombre del servidor hacemos click
- 14: Tenemos que ir a la parte de Updates, luego en Repositories hacer click, tenemos que hacer Updates pero no tenemos los repos correctos
- 15: Tenemos que "Deshabilitar" los repos de Proxmox y "Add repo No-Suscription"
- 16: Luego si vamos a poder hacer el "Update" correctamente  

Canales de Youtube donde encontrar videos de ayuda (poner canal + proxmox):
> **DriveMeca:**  
> https://www.youtube.com/@DriveMeca

> **No Solo Hacking:**  
> https://www.youtube.com/@NoSoloHacking

> **Tecnocratica:**  
> https://www.youtube.com/@TecnocraticaNet

> **Jonatan Castro**  
> https://www.youtube.com/@JonatanCastro

> **Escuela de Informatica**  
> https://www.youtube.com/@escuela_de_informatica

→ Repositorio: proxmox-basico  
  
### 3 - Almacenamiento  
Tipos de almacenamiento en Proxmox  
NFS, CIFS, LVM, ZFS  
Buenas prácticas  
→ Repositorio: almacenamiento-proxmox  
  
### 4 - Cluster en Proxmox  
Creación del cluster  
Gestión de nodos  
Sincronización  
→ Repositorio: cluster-proxmox  
  
### 5 - Quorum y Alta Disponibilidad (HA)  
Conceptos fundamentales  
qDevice, voto, fallos y recuperación  
HA en máquinas virtuales  
→ Repositorio: quorum-ha  
  
### 6 - Escenarios prácticos  
3 nodos con almacenamiento compartido  
Migraciones en vivo  
Pruebas de falla y recuperación  
→ Repositorio: escenarios-3-nodos  
  
