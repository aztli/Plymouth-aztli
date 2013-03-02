Tema de Plymouth
======================================


Adecuaciones
--------------------------------------
Por defecto las ruta para acceder al script e imagenes ubicadas en el archivo
con extension plymouth, son especificas para sistemas derivados de ubuntu.
En el caso de que la distro no sea derivada de ubuntu, puedes adecuar las
rutas de acuerdo a tu distro, editando el archivo Kuautli.plymouth, sustituyendo
las rutas correctas al sistema.

### Ubuntu
En distribuciones derivadas de ubuntu la ruta es:

```shell
/lib/plymouth/themes
```

### Arch
En otras como Arch la ruta es:

```shell
/usr/share/plymouth/themes
```

Instalación
--------------------------------------
Coloca la carpeta dentro de la ruta de los temas de plymouth:

### Ubuntu

```shell
cp Kuautli-Plymouth /lib/plymouth/themes
update-alternatives --install /lib/plymouth/themes/default.plymouth default.plymouth /lib/plymouth/themes/Kuautli-Plymouth/Kuautli.plymouth 100
```

### Arch

```shell
cp -r Kuautli-Plymouth /usr/share/plymouth/themes
```

Configuración de tema
-------------------------------

### Ubuntu

Selecciona Kuautli-Plymouth.plymouth

```shell
update-alternatives --config default.plymouth
update-initramfs -u
```

### Arch  

```shell
plymouth-set-default-theme -R Kuautli-Plymouth
```

Licencía
-------------------------------
Copyright (C) 2012 Miguel Angel Gordian

Author: Miguel Angel Gordian os.aioria@gmail.com Keywords: Plymouth-Theme

This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details
