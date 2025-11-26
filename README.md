# server-proxmox-on-premise
Este repo tiene la intención de ser la Intro o un Manual de como crear un laboratorio on-premise con Proxmox  
Para trabajar de Administracion de Sistemas por lo general nos piden que sepamos de diferentes herramientas y Proxmox es una de esas herramientas bases en la cual casi todas las demas se sustentan.  
Por eso considero importante hablar en este repo sobre como es Instalar y Configurar Proxmox VE.

### Contenido
  
#### 1 - Introducción general  
Objetivo del manual 
- Para trabajar como SysAdmin o Administrador de Sistemas nos piden que sepamos de varias aplicaciones, protocolos, dispositivos y herramientas. Proxmox VE es una de esas herramientas que sirve para trabajar con algunas de esas aplicaciones. Por ejemplo para practicar con un servidor de Linux podemos usar una PC vieja que no usemos y luego de algunos "ajustes" podemos darle el uso de "servidor" a la PC (de hecho tengo un repo que explica como hacerlo).
- En este caso Proxmox VE nos permite crear mas de 1 servidor dentro de 1 PC Server con Proxmox VE instalado  
  
Requisitos básicos  
- Simplemente ser sincero con el que esta leyendo, si bien 1 PC viejo se puede usar como "server" en el caso de Proxmox VE yo tengo 1 PC con 12 hilos y 16 ram y me quedo muy escaso para crecer en el estudio practico.
- Quizas nos comentan que para estudiar con cualquier PC es suficiente y yo realmente considero que si bien se puede estudiar con 1 PC humilde en recursos, igual asi no sirve para trabajar con herramientas como las que estoy comentando ahora.
- Proxmox VE nos permite tener dentro de 1 PC varios "nodos" o "VM" maquinas virtuales. Trabajar con ambas a la par considero que es lo importante para saber como se comunicacn cada una de estas herramientas  
  
Estructura de los tutoriales
- Es muy extenso volcar en un repo todo lo que hay que tener en cuenta. Por eso voy a linkear a este repo Principal los demas repos que van a tener la funcion de completar la documentacion
  
### 2 - Proxmox VE  
Instalación y configuración inicial  
Gestión de red  
Acceso web  
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
  
