---
layout: post
title: ¿Cómo instalar python3 en un tinkerboard?
---

Por default Linaro incluye **python 2.7**, si queremos instalar **python3.6** debemos seguir los siguientes pasos.

Verificar la versión de python que tenemos instalado usando el siguiente comando:

```
$ python --version
```

Actualizar nuestro sistema:

```
$ sudo apt-get update
$ sudo apt-get upgrade
$ sudo apt-get dist-upgrade
```

Instalar las dependencias para la instalación manual desde el source code:


```
$ sudo apt-get -y install libbz2-dev liblzma-dev libsqlite3-dev libncurses5-dev libgdbm-dev zlib1g-dev libreadline-dev libssl-dev tk-dev build-essential libncursesw5-dev libc6-dev openssl
```

Movernos al directorio home:

```
$ cd ~
```

Descargar python3.6:

```
$ wget https://www.python.org/ftp/python/3.6.0/Python-3.6.0.tgz
```

Descomprimir el archivo:

```
$ tar -zxvf Python-3.6.0.tgz
```

Acceder al nuevo directorio:

```
$ cd Python-3.6.0
```

Configurar:
```
$ ./configure
```

Construir:
```
$ make
$ sudo make install
```

Verificar:
```
$ python3.6 --version
```
