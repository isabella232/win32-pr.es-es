---
description: Los hosts y clientes de Perfil de dispositivo para servicios web (DPWS) se comunican a través de la red mediante una serie de mensajes SOAP a través de UDP y HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Patrones de mensajes de Exchange de detección y metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1b41267e86358a9d6e263f4bc8971632f1061eb1c94d1e64cc76d65020ce255
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856804"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a>Patrones de mensajes de Exchange de detección y metadatos

Los hosts y clientes de Perfil de dispositivo para servicios web (DPWS) se comunican a través de la red mediante una serie de mensajes SOAP a través de UDP y HTTP.

En el diagrama siguiente se muestra información general del tráfico UDP y HTTP esperado entre un host y un cliente de DPWS.

![Diagrama que muestra el tráfico UDP y HTTP entre un host y un cliente de DPWS.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

[Los](hello-message.md)mensajes Hello , [Bye](bye-message.md), [Probe,](probe-message.md) [Resolve](resolve-message.md)y [Get](get--metadata-exchange--http-request-and-message.md) se generan sin solicitud de red; estos mensajes se usan para anunciar el estado del dispositivo o para emitir una solicitud de búsqueda. [Los mensajes ProbeMatches,](probematches-message.md) [ResolveMatches](resolvematches-message.md)y [GetResponse](getresponse--metadata-exchange--message.md) se generan en respuesta a los mensajes Probe, Resolve y Get.

[Los](hello-message.md)mensajes Hello , [Bye,](bye-message.md) [Resolve](resolve-message.md)y [ResolveMatches](resolvematches-message.md) siempre se producirán a través de UDP. De forma similar, [los mensajes de](get--metadata-exchange--http-request-and-message.md) metadatos Get y [GetResponse](getresponse--metadata-exchange--message.md) siempre se producirán a través de HTTP o HTTPS. [Los](probe-message.md) mensajes [Probe y ProbeMatches](probematches-message.md) normalmente se transmiten a través de UDP, pero tienen lugar a través de una conexión HTTP o HTTPS en un escenario de detección dirigida. Para obtener más información sobre los patrones de mensajes de detección dirigida, vea [Solución de problemas de aplicaciones mediante la detección dirigida.](troubleshooting-applications-using-directed-discovery.md)

En la lista siguiente se muestra la secuencia típica de mensajes en la conexión. No todos los mensajes son obligatorios.

1.  [Hello](hello-message.md)
2.  [Sondeo](probe-message.md)
3.  [ProbeMatches](probematches-message.md)
4.  [Resolver](resolve-message.md)
5.  [ResolveMatches](resolvematches-message.md)
6.  [Get](get--metadata-exchange--http-request-and-message.md) (solicitud de intercambio de metadatos)
7.  [GetResponse](getresponse--metadata-exchange--message.md)
8.  [Adiós](bye-message.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los servicios web en dispositivos](about-web-services-for-devices.md)
</dt> </dl>

 

 



