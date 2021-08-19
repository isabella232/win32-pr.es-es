---
description: especifica un prefijo que está en el vínculo a la interfaz \# 4.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: Prefijos de sitio IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd37370aa14bd6883f83e93d661f10b96d804dc3b85cf47173da4b1f0ee0f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111299"
---
# <a name="ipv6-site-prefixes"></a>Prefijos de sitio IPv6

El comando ipv6 rtu permite configurar los prefijos publicados en el vínculo con una longitud de prefijo de sitio. Si se especifica, la longitud del prefijo del sitio se coloca en una opción de información de prefijo en los anuncios de enrutador. Por ejemplo:

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

especifica un prefijo que está en el vínculo a la interfaz \# 4. El prefijo se publica, lo que significa que se incluye en los anuncios de enrutador si la \# interfaz 4 es una interfaz de publicidad. La duración de la opción de información de prefijo es de 1800 segundos (30 minutos). La longitud del prefijo del sitio en la opción de información de prefijo es 48.

La recepción de una opción de información de prefijo que especifica un prefijo de sitio hace que se cree una entrada en la tabla de prefijos de sitio, que se puede mostrar mediante el comando spt de ipv6. La tabla de prefijos de sitio se usa para quitar las direcciones locales de sitio inapropiadas de las devueltas por [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y las funciones relacionadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Direcciones IPv6 Link-local y Site-local](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> </dl>

 

 



