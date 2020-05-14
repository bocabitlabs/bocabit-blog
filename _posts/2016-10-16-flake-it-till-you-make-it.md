---
layout: post
title: Bloquea anuncios utilizando una Raspberry PI
subtitle: Páginas web sin publicidad. Sin bloqueadores de anuncios.
cover-img: /assets/img/pi-hole-admin.png
tags: [internet, raspberry-pi]
---

Cada vez es mayor el número de **páginas que nos obligan a desactivar los bloqueadores de anuncios** para acceder a sus contenidos. En cierta medida es comprensible puesto que no deja de ser una manera de obtener ingresos, pero cuando esta publicidad se convierte en abusiva y resulta imposible identificar el contenido entre toda ella.

La solución que yo propongo se llama Pi-Hole y es bastante efectiva, aunque no infalible. Para ella se necesita disponer de una Raspberry PI con Raspbian, en el que instalaremos **Pi-Hole**. Esta aplicación instalará un servidor en la Raspberry, que actuará como DNS y filtrará todo el tráfico de nuestra red, bloqueando los dominios de servidores de anuncios sin necesidad de ninguna configuración en ninguno de nuestros dispositivos.

La instalación es realmente sencilla. Basta con conectarnos por ssh a la Raspberry Pi e instalar Pi-Hole con un simple comando:

```
curl -L https://install.pi-hole.net | bash
````
Durante la instalación podremos elegir qué DNS queremos utilizar: Google, OpenDNS… entre otras cosas muy sencillas. Una vez terminado, solamente deberemos **establecer la IP de la Raspberry PI como DNS** en nuestro router o nuestros dispositivos et voilá, todo listo.

Una vez instalado y configurado, podremos acceder a su panel de administración en la IP de la Raspberry /admin para añadir o eliminar manualmente dominios, comprobar las estadísticas, etc.

Más información sobre Pi-Hole | [Página oficial de Pi-Hole](https://pi-hole.net/)

Página de instalación de Raspbian | [Página oficial de Raspberry PI](https://www.raspberrypi.org/documentation/installation/installing-images/README.md)
