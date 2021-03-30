---
description: Los clientes y los hosts de los servicios web (DPWS) se comunican a través de la red mediante una serie de mensajes SOAP a través de UDP y HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Patrones de mensajes de intercambio de metadatos y detección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9a08852c5f25572daf9932afd2ce4b7e03858a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104279758"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a>Patrones de mensajes de intercambio de metadatos y detección

Los clientes y los hosts de los servicios web (DPWS) se comunican a través de la red mediante una serie de mensajes SOAP a través de UDP y HTTP.

En el diagrama siguiente se muestra información general sobre el tráfico UDP y HTTP esperado entre un host y un cliente de DPWS.

![Diagrama que muestra el tráfico UDP y HTTP entre un host y un cliente de DPWS.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

Los mensajes [Hello](hello-message.md), [bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md)y [Get](get--metadata-exchange--http-request-and-message.md) se generan sin la solicitud de red; Estos mensajes se utilizan para anunciar el estado del dispositivo o para emitir una solicitud de búsqueda. Los mensajes [ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md)y [GetResponse](getresponse--metadata-exchange--message.md) se generan como respuesta a sondeo, resolución y obtención de mensajes.

Los mensajes [Hello](hello-message.md), [bye](bye-message.md), [Resolve](resolve-message.md)y [ResolveMatches](resolvematches-message.md) siempre se producirán a través de UDP. Del mismo modo, los mensajes de metadatos [Get](get--metadata-exchange--http-request-and-message.md) y [GetResponse](getresponse--metadata-exchange--message.md) siempre se producirán a través de http o https. Los mensajes de [sondeo](probe-message.md) y [ProbeMatches](probematches-message.md) se transmiten normalmente a través de UDP, pero tienen lugar a través de una conexión http o https en un escenario de detección dirigido. Para obtener más información sobre los patrones de mensajes de detección dirigidos, consulte [solución de problemas de aplicaciones mediante la detección dirigida](troubleshooting-applications-using-directed-discovery.md).

En la siguiente lista se muestra la secuencia típica de mensajes en la conexión. No todos los mensajes son obligatorios.

1.  [Hola](hello-message.md)
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

 

 



