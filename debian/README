# Paquete DEB vx-dga-l-mimetypes

Paquete encargado de configurar asociaciones entre aplicaciones (*.desktop) y mimetypes de archivos.
En concreto se puede hacer lo siguiente:

[Default Applications] : asociación entre mimetype y aplicación (Desktop) que la abrirá por defecto (si se pincha doble click)
[Added Associations] : asociación entre mimetypes y aplicaciones (desktop) que aparecerá como opciones al pinchar con el botón derecho y elegir "abrir con"

El formato sería de la siguiente forma:

```
[Default Applications]
application/x-shockwave-flash=vx-firefox-swf.desktop

[Added Associations]
application/x-shockwave-flash=vx-firefox-swf.desktop;otro.desktop;...
```

# Usuarios Destinatarios

Usuarios que requieren obligar asociaciones entre aplicaciones y mimetypes de archivos

# Aspectos Interesantes:

Para poder configurar lo anterior se ha creado un programa en python **/usr/bin/vx-configparser** haciendo uso del módulo **configparser**.  El uso de esta aplicación sería la siguiente:

```
ARCHIVO="/usr/share/applications/mimeapps.list" 
vx-configparser "${ARCHIVO}" "Default Applications" "image/pb;video/px;" "app1.desktop" 
vx-configparser "${ARCHIVO}" "Added Associations" "image/pb;video/px;" "app1.desktop;app2.desktop;app3.desktop;..."
```

# Como Crear o Descargar el paquete DEB a partir del codigo de GitHub
Para crear el paquete DEB será necesario encontrarse dentro del directorio donde localizan los directorios que componen el paquete.  Una vez allí, se ejecutará el siguiente comando (es necesario tener instalados los paquetes apt-get install debhelper devscripts):

```
apt-get install debhelper devscripts
/usr/bin/debuild --no-tgz-check -us -uc
```

En caso de no querer crear el paquete para tu distribución, puedes hacer uso del que está disponible para Vitalinux (*Lubuntu 14.04*) desde el siguiente repositorio:

[Respositorio de paquetes DEB de Vitalinux](http://migasfree.educa.aragon.es/repo/Lubuntu-14.04/STORES/base/)

# Como Instalar el paquete vx-dga-l-*.deb:

Para la instalación de paquetes que estan en el equipo local puede hacerse uso de ***dpkg*** o de ***gdebi***, siendo este último el más aconsejado para que se instalen de manera automática también las dependencias correspondientes.
```
gdebi vx-dga-l-*.deb
```
