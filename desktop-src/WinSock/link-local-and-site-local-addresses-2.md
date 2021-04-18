---
description: Las direcciones locales de vínculo IPv6 y de sitio se denominan direcciones de ámbito.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: Dirección local de vínculo IPv6 y direcciones locales de sitio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80b8e201adf382b10dd31fe5607de903d6c588
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705605"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a>Dirección local de vínculo IPv6 y direcciones locales de sitio

Las direcciones locales de vínculo IPv6 y de sitio se denominan direcciones de ámbito. La API de Windows Sockets (Winsock) admite el miembro de **\_ \_ identificador de ámbito sin6** en la estructura [**\_ IN6 de sockaddr**](sockaddr-2.md) para su uso con direcciones de ámbito. En el caso de las direcciones locales de vínculo (fe80::/10 prefijo), el miembro de **\_ \_ identificador de ámbito sin6** de la estructura **sockaddr \_ IN6** es el número de interfaz. En el caso de las direcciones locales del sitio IPv6 (prefijo FEC0::/10), el miembro **\_ \_ ID. de ámbito sin6** de la estructura **sockaddr \_ IN6** es un identificador de sitio.

Un ejemplo de una dirección IPv6 local de vínculo en \# la interfaz 5 es el siguiente:

``` syntax
fe80::208:74ff:feda:625c%5
```

El siguiente comando está disponible en Windows XP con Service Pack 1 (SP1) y versiones posteriores para consultar y configurar IPv6 en un equipo local:

-   [Netsh.exe](netsh-exe.md)

Los cambios de configuración realizados con los comandos Netsh.exe son permanentes y no se pierden cuando se reinicia el equipo o el protocolo IPv6.

Antes de Windows XP con Service Pack 1 (SP1), la configuración y administración de IPv6 usaba varias herramientas de línea de comandos anteriores (Net.exe, Ipv6.exe y Ipsec6.exe) para configurar y administrar IPv6. Con estas herramientas anteriores, los cambios de IPv6 no son permanentes y se pierden cuando se reinició el equipo o el protocolo IPv6. Estas herramientas de línea de comandos anteriores solo se admiten en Windows XP.

En Windows XP con SP1, el siguiente comando mostrará la lista de interfaces IPv6 en un equipo local, incluidos el índice de la interfaz, el nombre de la interfaz y otras propiedades de la interfaz.

**netsh interface ipv6 show interface**

En Windows XP con SP1, el siguiente comando cambiará el identificador de sitio asociado a un índice de interfaz.

**netsh interface ipv6 set interface <InterfaceIndex or Name> siteID = valor**

En Windows XP, el siguiente comando anterior también cambiará el identificador del sitio asociado a una dirección local del sitio a 3.

**fec0 de RTU de IPv6::/10 3**

Si está enviando o conectándose a una dirección de ámbito, el miembro **de \_ \_ identificador de ámbito sin6** en la estructura [**\_ IN6 de sockaddr**](sockaddr-2.md) se puede dejar sin especificar (cero), lo que representa una dirección de ámbito ambiguo. Por ejemplo, la siguiente dirección local de vínculo es ambigua:

``` syntax
fe80::10
```

Si va a enlazar a una dirección de ámbito, el miembro de **\_ \_ identificador de ámbito sin6** en la estructura [**\_ IN6 de sockaddr**](sockaddr-2.md) debe contener un valor distinto de cero que especifique un número de interfaz válido para una dirección local de vínculo o un identificador de sitio para una dirección local del sitio.

## <a name="ambiguous-scoped-addresses"></a>Direcciones con ámbito ambiguo

Si está enviando o conectándose a una dirección de ámbito y no ha especificado el miembro de **\_ \_ identificador de ámbito sin6** en la estructura [**\_ IN6 de sockaddr**](sockaddr-2.md) , la dirección de ámbito es ambigua. Para resolver este comportamiento, el protocolo IPv6 determina primero si el socket se ha enlazado a una dirección de origen. Si es así, la dirección de origen enlazada resuelve la ambigüedad proporcionando un número de interfaz o un identificador de sitio.

Si se envía o se conecta a una dirección de ámbito y no se especifica el miembro de **\_ \_ identificador de ámbito sin6** ni se enlaza una dirección de origen, el protocolo IPv6 comprueba la tabla de enrutamiento. Por ejemplo, el siguiente comando mostrará la tabla de enrutamiento IPv6 en un equipo local:

**netsh interface ipv6 show route**

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

Esto indica que las direcciones locales de vínculo se tratan como en vínculo a la interfaz \# 13 y \# 14 de forma predeterminada.

La ambigüedad se produce cuando un equipo local tiene varios adaptadores de red. Por ejemplo, el comando **netsh** anterior indica que hay dos interfaces de red (conexión de área local y conexión de red inalámbrica). Cuando una aplicación especifica una dirección local de vínculo de destino (fe80:: 10, por ejemplo) sin un identificador de ámbito, no queda claro qué adaptador usar para enviar el paquete. Solo una unidifusión local de vínculo (fe80::/64) o una dirección de destino IPv6 de multidifusión del ámbito de vínculo (ff00::/8) pueden verse en que no tienen un identificador de ámbito al enviar un paquete.

## <a name="neighbor-discovery"></a>Detección de equipos cercanos

Si no ha especificado el miembro **de \_ \_ identificador de ámbito sin6** en la estructura [**\_ IN6 de sockaddr**](sockaddr-2.md) , no ha enlazado una dirección de origen y no ha especificado una ruta para las direcciones locales del vínculo, el protocolo IPv6 probará la detección de vecinos para resolver la dirección local del vínculo de destino. Para un paquete determinado que se está enviando, se intenta una interfaz. Esta primera interfaz que se intenta se considera la interfaz más preferida. Si la detección de vecinos no puede resolver la dirección local del vínculo en una interfaz, se quita el paquete que se va a enviar y el sistema recuerda que no se puede tener acceso a la dirección local del vínculo de destino a través de esa interfaz. En el siguiente paquete que se va a enviar en todas las condiciones, se intenta una interfaz diferente para la detección de vecinos. Este proceso continúa a través de cada una de las interfaces en un equipo local para cada nuevo paquete hasta que la detección de vecinos responde a la dirección local del vínculo de destino o se han intentado todas las interfaces posibles. Cada vez que se produce un error al intentar resolver el vecino, se elimina una interfaz para ese vecino.

Si se resuelve la dirección local del vínculo de destino, esa interfaz se utiliza para enviar el paquete actual. Esta interfaz también se utiliza para los paquetes posteriores de ámbito ambiguo que se envían a la misma dirección de destino local de vínculo.

Si la detección de vecinos no puede resolver la dirección local del vínculo de destino en todas las interfaces, el sistema intenta enviar el paquete en la interfaz más preferida (la primera interfaz que se ha intentado). La pila de red sigue intentando resolver la dirección local del vínculo de destino en la interfaz más preferida. Después de un período de tiempo después de que se haya producido un error en la detección de vecinos en todas las interfaces, la pila de red reiniciará el proceso de nuevo e intentará resolver la dirección local del vínculo de destino en todas las interfaces. Actualmente, este intervalo de tiempo cuando se intenta de nuevo la detección de vecinos en todas las interfaces es de 60 segundos. Sin embargo, este intervalo de tiempo puede cambiar en las versiones de Windows y no debe ser asumida por una aplicación.

> [!Note]  
> Si una aplicación enlaza la misma dirección local de vínculo a una interfaz diferente después de que la detección de vecinos haya resuelto la dirección local del vínculo, no invalidará la interfaz con la dirección de destino local de vínculo devuelta por la detección de vecinos.

 

Para obtener más información sobre la detección de vecinos para IP versión 6, consulte [RFC4861](https://tools.ietf.org/html/rfc4861) publicado por IETF.

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

 

 



