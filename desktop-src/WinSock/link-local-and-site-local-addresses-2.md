---
description: Las direcciones IPv6 link-local y site-local se denominan direcciones con ámbito.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: Direcciones IPv6 Link-local y Site-local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22220adb2c1b0338462f7ed87b3937a97c3d0b8a8b0aa2d9858d5c5efc8b4f54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794785"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a>Direcciones IPv6 Link-local y Site-local

Las direcciones IPv6 link-local y site-local se denominan direcciones con ámbito. La API Windows Sockets (Winsock) admite el miembro de identificador de ámbito **sin6 \_ \_** en la estructura [**sockaddr \_ in6**](sockaddr-2.md) para su uso con direcciones con ámbito. Para las direcciones locales de vínculo IPv6 (prefijo fe80::/10), el miembro de identificador de ámbito **sin6 \_ \_** de la estructura **sockaddr \_ in6** es el número de interfaz. Para las direcciones locales de sitio IPv6 (prefijo fec0::/10), el miembro de identificador de ámbito **sin6 \_ \_** de la estructura **sockaddr \_ in6** es un identificador de sitio.

A continuación se muestra un ejemplo de una dirección IPv6 local de vínculo \# en la interfaz 5:

``` syntax
fe80::208:74ff:feda:625c%5
```

El siguiente comando está disponible en Windows XP con Service Pack 1 (SP1) y versiones posteriores para consultar y configurar IPv6 en un equipo local:

-   [Netsh.exe](netsh-exe.md)

Los cambios de configuración realizados mediante Netsh.exe comandos son permanentes y no se pierden cuando se reinicia el equipo o el protocolo IPv6.

Antes de Windows XP con Service Pack 1 (SP1), la configuración y administración de IPv6 usaba varias herramientas de línea de comandos anteriores (Net.exe, Ipv6.exe y Ipsec6.exe) para configurar y administrar IPv6. Con estas herramientas anteriores, los cambios de IPv6 no son permanentes y se pierden cuando se reinicia el equipo o el protocolo IPv6. Estas herramientas de línea de comandos anteriores solo se admiten en Windows XP.

En Windows XP con SP1, el comando siguiente mostrará la lista de interfaces IPv6 en un equipo local, incluido el índice de interfaz, el nombre de la interfaz y otras propiedades de interfaz.

**interfaz netsh ipv6 show interface**

En Windows XP con SP1, el siguiente comando cambiará el identificador de sitio asociado a un índice de interfaz.

**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid=value**

En Windows XP, el siguiente comando anterior también cambiará el identificador de sitio asociado a una dirección local del sitio a 3.

**ipv6 rtu fec0::/10 3**

Si va a enviar o conectarse a una dirección con ámbito, el miembro de identificador de ámbito **sin6 \_ \_** de la estructura [**sockaddr \_ in6**](sockaddr-2.md) se puede dejar sin especificar (cero), que representa una dirección con ámbito ambigua. Por ejemplo, la siguiente dirección local de vínculo es ambigua:

``` syntax
fe80::10
```

Si va a enlazar a una dirección con ámbito, el miembro de identificador de ámbito **sin6 \_ \_** de la estructura [**sockaddr \_ in6**](sockaddr-2.md) debe contener un valor distinto de cero que especifique un número de interfaz válido para una dirección local de vínculo o un identificador de sitio para una dirección local de sitio.

## <a name="ambiguous-scoped-addresses"></a>Direcciones con ámbito ambiguo

Si va a enviar o conectarse a una dirección con ámbito y no ha especificado el miembro de identificador de ámbito **sin6 \_ \_** en la estructura [**sockaddr \_ in6,**](sockaddr-2.md) la dirección con ámbito es ambigua. Para resolver este problema, el protocolo IPv6 determina primero si ha enlazado el socket a una dirección de origen. Si es así, la dirección de origen enlazada resuelve la ambigüedad al proporcionar un número de interfaz o un identificador de sitio.

Si va a enviar o conectarse a una dirección con ámbito y no ha especificado el miembro de identificador de ámbito **sin6 \_ \_** ni ha enlazado una dirección de origen, el protocolo IPv6 comprueba la tabla de enrutamiento. Por ejemplo, el comando siguiente mostrará la tabla de enrutamiento IPv6 en un equipo local:

**netsh interface ipv6 show route**

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

Esto indica que las direcciones locales de vínculo se tratan como en el vínculo a las interfaces \# 13 y \# 14 de forma predeterminada.

La ambigüedad surge cuando un equipo local tiene varios adaptadores de red. Por ejemplo, el **comando netsh** anterior indica que hay dos interfaces de red (Conexión de área local y Conexión de red inalámbrica). Cuando una aplicación especifica una dirección local de vínculo de destino (fe80::10, por ejemplo) sin un identificador de ámbito, no está claro qué adaptador usar para enviar el paquete. Solo un unidifusión local de vínculo (fe80::/64) o una dirección de destino IPv6 de ámbito de vínculo (ff00::/8) puede sufrir que no tenga un identificador de ámbito al enviar un paquete.

## <a name="neighbor-discovery"></a>Detección de equipos cercanos

Si no ha especificado el miembro de identificador de ámbito **sin6 \_ \_** en la estructura [**sockaddr \_ in6,**](sockaddr-2.md) no ha enlazado una dirección de origen y no ha especificado una ruta para las direcciones locales del vínculo, el protocolo IPv6 intentará la detección de vecinos para resolver la dirección local del vínculo de destino. Para enviar un paquete determinado, se intenta una interfaz. Esta primera interfaz que se intenta se considera la interfaz más preferida. Si la detección de vecinos no puede resolver la dirección local del vínculo en una interfaz, se descarta el paquete que se va a enviar y el sistema recuerda que la dirección local del vínculo de destino no es accesible a través de esa interfaz. En el siguiente paquete que se va a enviar en las mismas condiciones, se intenta usar una interfaz diferente para la detección de vecinos. Este proceso continúa a través de cada una de las interfaces de un equipo local para cada paquete nuevo hasta que la detección de vecinos responde para la dirección local del vínculo de destino o todas las interfaces posibles se han intentado y se ha dado error. Cada vez que se produce un error en un intento de resolver el vecino, se elimina una interfaz para ese vecino.

Si se resuelve la dirección local del vínculo de destino, esa interfaz se usa para enviar el paquete actual. Esta interfaz también se usa para los paquetes de ámbito ambiguo subsiguientes que se envían a la misma dirección de destino local del vínculo.

Si la detección de vecinos no resuelve la dirección local del vínculo de destino en todas las interfaces, el sistema intenta enviar el paquete en la interfaz más preferida (la primera interfaz intentó). La pila de red sigue intentando resolver la dirección local del vínculo de destino en la interfaz más preferida. Después de un período de tiempo después de que la detección de vecinos haya dado error en todas las interfaces, la pila de red reiniciará el proceso de nuevo e intentará resolver la dirección local del vínculo de destino en todas las interfaces. Actualmente, este intervalo de tiempo cuando se vuelve a intentar la detección de vecinos en todas las interfaces es de 60 segundos. Sin embargo, este intervalo de tiempo puede cambiar en las versiones Windows y no debe ser asumido por una aplicación.

> [!Note]  
> Si una aplicación enlaza la misma dirección local de vínculo a una interfaz diferente después de que la detección de vecinos haya resuelto la dirección local del vínculo, no invalidará la interfaz con la dirección de destino local del vínculo devuelta por la detección de vecinos.

 

Para obtener más información sobre la detección de vecinos para ip versión 6, vea [RFC4861](https://tools.ietf.org/html/rfc4861) publicado por IETF.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Prefijos de sitio IPv6](site-prefixes-2.md)
</dt> <dt>

[Ipv6.exe](ipv6-exe-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> <dt>

[Usar IPv6](using-ipv6-2.md)
</dt> </dl>

 

 



