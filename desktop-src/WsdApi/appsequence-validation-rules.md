---
description: AppSequence información contenida en WS-Discovery anuncios y mensajes de respuesta (Hello, ProbeMatches y ResolveMatches).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Reglas de validación de AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544814"
---
# <a name="appsequence-validation-rules"></a>Reglas de validación de AppSequence

AppSequence información contenida en WS-Discovery anuncios y mensajes de respuesta ([Hello](hello-message.md), [ProbeMatches](probematches-message.md)y [ResolveMatches](resolvematches-message.md)). WSDAPI procesa y valida esta información antes de pasar estos mensajes a los componentes situados por encima de la pila (como el explorador de red o una aplicación que llama a WSDAPI).

En el código XML siguiente se muestra un elemento AppSequence de ejemplo. El prefijo WSD hace referencia al espacio de nombres `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

WSDAPI omite los mensajes obsoletos. Para cada dispositivo (identificado de forma exclusiva por la dirección del punto de conexión en el cuerpo de SOAP), WSDAPI omite los mensajes con un MessageNumber AppSequence inferior al último mensaje que se ha observado.

WSDAPI omite los anuncios XAddr obsoletos. Si el InstanceId AppSequence es inferior al último InstanceId detectado, WSDAPI omite el XAddrs anunciado en el cuerpo de SOAP. Además, si InstanceId es el mismo que el anterior pero el MetadataVersion es inferior al último MetadataVersion, WSDAPI omite XAddrs.

WSDAPI omite los mensajes duplicados de WS-Discovery. Si se envían dos mensajes de WS-Discovery idénticos a WSDAPI, solo se procesará el primero recibido. Normalmente solo es pertinente para las aplicaciones que llaman directamente a las interfaces [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) o [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Patrones de mensajes de intercambio de metadatos y detección](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



