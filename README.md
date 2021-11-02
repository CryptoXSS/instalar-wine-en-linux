# instalar-wine-en-linux

# Habilite los paquetes de 32 bits (si aún no lo ha hecho):

$ sudo dpkg --add-architecture i386

# Descargue e instale la clave del repositorio:
wget -nc https://dl.winehq.org/wine-builds/winehq.key

sudo apt-key add winehq.key

# Agregue el repositorio a /etc/apt/sources.list con el siguiente contenido:
$ sudo nano /etc/apt/sources.list

deb https://dl.winehq.org/wine-builds/debian/ buster main

deb https://dl.winehq.org/wine-builds/debian/ bullseye main

deb https://dl.winehq.org/wine-builds/debian/ bookworm main

guardalo con ctrl+X LUEGO TECLEA LA S  Y ENTER PARA SALIR

# Actualiza los paquetes:

$ sudo apt update

# Luego instale uno de los siguientes paquetes:

# Stable branch 

sudo apt install --install-recommends winehq-stable

# Development branch

sudo apt install --install-recommends winehq-devel

# Staging branch 

sudo apt install --install-recommends winehq-staging

# Algunas notas sobre los paquetes de WineHQ:

Los archivos se instalan en / opt / wine-devel o / opt / wine-staging.
Los elementos del menú no se crean para los programas integrados de Wine (winecfg, etc.), y si está actualizando desde un paquete de distribución que los había agregado, se eliminarán. Puede recrearlos usted mismo usando su editor de menú.
WineHQ no empaqueta en la actualidad wine-gecko o wine-mono. Al crear un nuevo prefijo de vino, se le preguntará si desea descargar esos componentes. Para una mejor compatibilidad, se recomienda hacer clic en Sí aquí. Si la descarga no le funciona, siga las instrucciones de las páginas wiki de Gecko y Mono para instalarlas manualmente.
A partir de Wine 5.7, los paquetes WineHQ Debian tienen una configuración debconf opcional para habilitar CAP_NET_RAW para permitir que las aplicaciones que necesitan enviar y recibir paquetes IP sin procesar lo hagan. Esto está deshabilitado de forma predeterminada porque conlleva un riesgo de seguridad potencial y la gran mayoría de las aplicaciones no necesitan esa capacidad. Los usuarios de aplicaciones que lo necesitan pueden habilitar CAP_NET_RAW después de instalar Wine ejecutando.

# Uso: wine PROGRAMA [ARGUMENTOS...]   Ejecuta el programa especificado
  #     wine --ayuda                   Muestre esta ayuda y salga
   #    wine --version                Salida de información de versión y salida
   
   # Descarga los juegos o programas desde a <a href="https://ubuntonic.blogspot.com">Aqui</a> o en otra pagina que conozcas.
   
   # luego de descargar el ejecutable.exe lo instalamos desde la terminal, con el siguiente comando  "wine ejecutable.exe" y listo ya tenemos nuestro juego en linux :D
   
   



