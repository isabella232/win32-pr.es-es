---
description: 6to4 es un método para conectar hosts o sitios IPv6 a través de la infraestructura de Internet IPv4 existente.
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: 'Configuración 2: Tráfico IPv6 entre nodos en subredes diferentes de una red de Internet IPv4 (6to4)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d976aa3ea21d990ea22f861fbf05a816866e6b0d21502211e23a0e331a2f851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112510"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a>Configuración 2: Tráfico IPv6 entre nodos en subredes diferentes de una red de Internet IPv4 (6to4)

6to4 es un método para conectar hosts o sitios IPv6 a través de la infraestructura de Internet IPv4 existente. Usa un prefijo de dirección único para proporcionar a los sitios IPv6 aislados su propio espacio de direcciones IPv6. 6to4 es como un "pseudo-ISP" que proporciona conectividad IPv6. Puede usar 6to4 para comunicarse directamente con otros sitios de 6to4. 6to4 no requiere el uso de enrutadores IPv6 y su tráfico IPv6 se encapsula con un encabezado IPv4.

En la ilustración siguiente se muestra la configuración de dos nodos en subredes independientes mediante 6to4 para comunicarse a través de un enrutador IPv4.

![nodos que usan 6to4 para comunicarse a través de un enrutador ipv4.](images/v6mig-2.png)

El requisito principal para usar 6to4 es una dirección IPv4 enrutable globalmente para el sitio. Supongamos que el sitio consta de una colección de equipos IPv6 que administra (algunos que ejecutan el protocolo IPv6 de Microsoft y otros que ejecutan otras implementaciones de IPv6). Supongamos también que todos los equipos IPv6 están conectados directamente mediante Ethernet o 6 sobre 4. La dirección IPv4 enrutable globalmente debe asignarse a uno de los equipos que ejecutan el protocolo IPv6 de Microsoft. Este equipo será la puerta de enlace 6to4.

Si tiene una dirección IPv4 que forma parte del espacio de direcciones privadas (10.0.0.0/8, 172.16.0.0/12 o 192.168.0.0/16) o el espacio de direcciones IP privadas automáticas (APIPA) de 169.254.0.0/16 usado por Windows 2000, no es enrutable globalmente. De lo contrario, probablemente sea una dirección IP pública y sea enrutable globalmente. Consulte el [tema Debugging 6to4 Configuration (Configuración de depuración 6to4)](#debugging-6to4-configuration) de este documento para obtener más ayuda para determinar si la conexión de ISP admite 6to4.

## <a name="the-6to4cfgexe-tool"></a>La herramienta 6to4cfg.exe herramientas

La 6to4cfg.exe automatización de la configuración 6to4, detecta automáticamente la dirección IPv4 enrutable globalmente y crea un prefijo 6to4. Realiza la configuración directamente o puede escribir un script de configuración que puede inspeccionar y ejecutar más adelante.

La sintaxis básica 6to4cfg.exe comandos es la siguiente.

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span id="_filename_"></span><span id="_FILENAME_"></span>\[*Nombre*\]
</dt> <dd>

Escribe el script de configuración en un archivo, si especifica un nombre de archivo. El script de configuración usa Ipv6.exe.

Puede especificar con para que el nombre de archivo escriba el script de configuración en la salida de la consola, lo que resulta útil para ver lo que 6to4cfg.exe en un escenario de prueba.

Si no especifica un nombre de archivo, 6to4cfg.exe actualiza directamente la configuración de IPv6 en el equipo.

</dd> <dt>

<span id="-r"></span><span id="-R"></span>-r
</dt> <dd>

Se convierte en un enrutador de puerta de enlace 6to4 para la red local, lo que habilita el enrutamiento en todas las interfaces y los prefijos de subred asignados.

</dd> <dt>

<span id="-s"></span><span id="-S"></span>-s
</dt> <dd>

Habilita el direccionamiento local del sitio en el sitio 6to4. Este comando solo es útil cuando se usa junto con -r.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>-u
</dt> <dd>

Especifica que se va a invertir la configuración 6to4. Por lo tanto, 6to4cfg -u invierte el efecto de 6to4cfg y 6to4cfg -r -u invierte el efecto de 6to4cfg -r, y así sucesivamente.

</dd> <dt>

<span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *Relay*
</dt> <dd>

Especifica el nombre o la dirección IPv4 de un enrutador de retransmisión 6to4. El nombre predeterminado es 6to4.ipv6.microsoft.com, el enrutador de retransmisión 6to4 en Internet.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>-b
</dt> <dd>

Especifica que 6to4cfg.exe la dirección de retransmisión "mejor" en lugar de la primera.

</dd> <dt>

<span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *address*
</dt> <dd>

Especifica la dirección IPv4 local para el prefijo 6to4.

</dd> </dl>

## <a name="manual-6to4-configuration"></a>Configuración manual 6to4

En este ejemplo, la dirección de la puerta de enlace 6to4 es 172.31.42.239. Necesita su propia dirección IPv4 globalmente enrutable para usar 6to4.

> [!Note]  
> La dirección IP 172.31.42.239 solo se usa con fines de ejemplo. Se trata de una dirección privada y no es enrutable globalmente en Internet.

 

La dirección IPv4 global enrutable de 32 bits se combina con el prefijo de 16 bits 2002::/16 para formar un prefijo de dirección IPv6 de 48 bits para el sitio. En este ejemplo, el prefijo de sitio 6to4 es 2002:ac1f:2aef::/48. Tenga en cuenta que ac1f:2aef es la codificación hexadecimal de 172.31.42.239 (por supuesto, usará un prefijo diferente basado en su propia dirección IPv4 enrutable globalmente). Con el prefijo de sitio 6to4, puede asignar direcciones y prefijos de subred dentro del sitio.

En este ejemplo se supone que usa la subred 0 para configurar manualmente una dirección 6to4 en el equipo de puerta de enlace 6to4 y que usa la subred 1 para configurar automáticamente las direcciones en el segmento de red Ethernet. Sin embargo, otras opciones son posibles.

1.  Use Ipv6.exe para habilitar 6to4 en el equipo de puerta de enlace 6to4:

    **ipv6 rtu 2002::/16 2**

    El **comando ipv6 rtu** realiza una actualización de la tabla de enrutamiento. Se puede usar para agregar, quitar o actualizar una ruta. En este caso, está habilitando 6to4.

    El argumento 2002::/16 es el prefijo de la ruta y especifica el prefijo 6to4 único.

    El argumento 2 especifica la interfaz en el vínculo para este prefijo. La \# interfaz 2 es la "pseudo-interfaz" que se usa para túneles configurados, tunelización automática y 6to4. Cuando una dirección de destino IPv6 coincide con el prefijo 2002::/16, los 32 bits que siguen al prefijo en la dirección de destino se extraen para formar una dirección de destino IPv4. El paquete se encapsula con un encabezado IPv4 y se envía a la dirección de destino IPv4.

2.  Configure una dirección 6to4 en el equipo de puerta de enlace 6to4:

    **ipv6 adu 2/2002:ac1f:2aef::ac1f:2aef**

    El **comando ipv6 adu** realiza una actualización de direcciones. Se puede usar para agregar, quitar o actualizar una dirección en una interfaz. En este caso, está configurando la dirección 6to4 del equipo.

    El argumento 2/2002:ac1f:2aef::ac1f:2aef especifica la interfaz y la dirección. Requiere configurar la dirección 2002:ac1f:2aef::ac1f:2aef en la \# interfaz 2. La dirección se crea con el prefijo de sitio 2002:ac1f:2aef::/48, subred 0 para proporcionar un prefijo de subred 2002:ac1f:2aef::/64 y un identificador de interfaz de 64 bits. La convención demostrada usa la dirección IPv4 del equipo para el identificador de interfaz para las direcciones asignadas a la interfaz \# 2. Para su uso, ac1f:2aef debe reemplazarse por la codificación hexadecimal de su propia dirección IPv4 enrutable globalmente.

Los dos comandos anteriores son suficientes para permitir la comunicación con otros sitios 6to4. Por ejemplo, puede intentar hacer ping al sitio de Microsoft 6to4:

**ping6 2002:836b:9820::836b:9820**

Para habilitar la comunicación con la red 6, debe crear un túnel configurado de forma predeterminada a una retransmisión 6to4. Puede usar el enrutador de retransmisión de Microsoft 6to4, 131.107.152.32:

**ipv6 rtu ::/0 2/::131.107.152.32 pub life 1800**

El **comando ipv6 restablecimiento realiza** una actualización de tabla de enrutamiento, estableciendo, en esta instancia, una ruta predeterminada a la retransmisión 6to4.

El argumento ::/0 es el prefijo de ruta. El prefijo de longitud cero indica que es una ruta predeterminada.

El argumento 2/::131.107.152.32 especifica el vecino del próximo salto para este prefijo. Requiere que los paquetes que coincidan con el prefijo se reenván a la dirección ::131.107.152.32 mediante la \# interfaz 2. El reenvío de un paquete a ::131.107.152.32 en la interfaz 2 hace que se encapsula con un encabezado v4 y se envía \# a 131.107.152.32.

El argumento pub hace que sea una ruta publicada. Dado que esto solo es relevante para los enrutadores, no tiene ningún efecto hasta que se habilita el enrutamiento. Del mismo modo, la duración de 30 minutos solo pertenece a si el enrutamiento está habilitado.

Debería poder acceder a sitios de 6 y 6to4 sitios. Puede usar el siguiente comando para probar esto:

**ping6 3ffe:1cff:0:f5::1**

El último paso es habilitar el enrutamiento en la puerta de enlace 6to4. En este ejemplo se supone que la interfaz 3 del equipo de puerta de enlace es una interfaz Ethernet y la \# \# interfaz 4 es 6 sobre 4. El equipo podría numerar sus interfaces de forma diferente. Los dos comandos siguientes asignan prefijos de subred a los dos vínculos. Los prefijos de subred se derivan del prefijo 6to4 del sitio 2002:ac1f:2aef::/48:

**ipv6 rtu 2002:ac1f:2aef:1::/64 3 pub life 1800**

**ipv6 rtu 2002:ac1f:2aef:2::/64 4 pub life 1800**

El **comando ipv6 fan** especifica que el prefijo 2002:ac1f:2aef:1::/64 está en el vínculo a la \# interfaz 3. Está configurando el primer prefijo de subred en la interfaz Ethernet. La ruta se publica con una duración de 30 minutos.

De forma similar, el prefijo 2002:ac1f:2aef:2::/64 está configurado en la interfaz 6 sobre 4.

Los tres comandos siguientes permiten que el equipo de puerta de enlace 6to4 funcione como enrutador:

**ipv6 ifc 2 forw**

**ipv6 ifc 3 forw adv**

**ipv6 ifc 4 forw adv**

El **comando ifc de ipv6** controla los atributos de una interfaz. Un enrutador reenvía paquetes y envía anuncios de enrutador. En la implementación de IPv6 de Microsoft, estos atributos por interfaz se controlan por separado.

La \# interfaz 2 no es necesaria para la publicidad porque es una pseudo interface.

Si el equipo tiene interfaces adicionales, también se deben configurar para reenviar y anunciar.

Después de ejecutar estos comandos, el protocolo IPv6 de Microsoft configurará automáticamente las direcciones en las interfaces 3 y 4 con los prefijos de subred respectivos y las dos interfaces comenzarán a enviar anuncios de enrutador en intervalos de aproximadamente 3 a \# \# 10 minutos.

Los hosts que reciben estos anuncios de enrutador se configurarán automáticamente con una ruta predeterminada y una dirección 6to4 derivada del prefijo de subred de su vínculo. Tendrán comunicación con otros sitios 6to4 y 6-6 a través del equipo de puerta de enlace.

## <a name="debugging-6to4-configuration"></a>Depuración de la configuración 6to4

**Para depurar la configuración 6to4**

1.  Compruebe la conectividad IPv4 con el enrutador de retransmisión 6to4:

    **ping 6to4.ipv6.microsoft.com**

    Si se produce un error, no tendrá conectividad a Internet global.

2.  Compruebe la encapsulación IPv6 mediante la tunelización automática:

    **ping6 ::131.107.152.32**

    Si se produce un error, es posible que tenga un firewall o un traductor de direcciones de red (NAT) entre el equipo e Internet. Si esto se realiza correctamente, la conexión a Internet puede admitir 6to4.

3.  Compruebe la visualización del comando ipv6 rt. Debería ver una ruta 2002::/16 -> 2. Compruebe la visualización del comando ipv6 si 2. Debería ver una dirección preferida con un prefijo 2002::/16.

> [!Note]  
> La dirección IPv4 del enrutador de retransmisión de Microsoft 6to4 de 131.107.152.32 está sujeta a cambios. Si el paso 2 anterior no funciona, compruebe la salida del comando ping del paso 1 para comprobar la dirección IPv4 del enrutador de retransmisión de Microsoft 6to4.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuraciones recomendadas para IPv6](recommended-configurations-2.md)
</dt> <dt>

[Subred única con direcciones locales de vínculo](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Uso de IPsec entre dos hosts de vínculo local](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



