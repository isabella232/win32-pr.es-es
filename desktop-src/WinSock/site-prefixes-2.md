---
description: especifica un prefijo que está en el vínculo a la interfaz \# 4.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: Prefijos de sitio IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed8a21c59f9b6727c98ccb7fdacf4e9ec6ea5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715112"
---
# <a name="ipv6-site-prefixes"></a>Prefijos de sitio IPv6

El comando RTU de IPv6 permite configurar prefijos en vínculo publicados con una longitud de prefijo de sitio. Si se especifica, la longitud del prefijo del sitio se coloca en una opción de información de prefijo en anuncios de enrutador. Por ejemplo:

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

especifica un prefijo que está en el vínculo a la interfaz \# 4. El prefijo está publicado, lo que significa que se incluye en los anuncios de enrutador si la interfaz \# 4 es una interfaz de publicidad. La duración de la opción de información de prefijo es de 1800 segundos (30 minutos). La longitud del prefijo del sitio en la opción información de prefijo es 48.

La recepción de una opción de información de prefijo que especifica un prefijo de sitio hace que se cree una entrada en la tabla de prefijos de sitio, que se puede mostrar mediante el comando de acceso a través de IPv6. La tabla de prefijos de sitio se usa para quitar las direcciones locales de sitio inadecuadas de las devueltas por [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y las funciones relacionadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dirección local de vínculo IPv6 y direcciones locales de sitio](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> </dl>

 

 



