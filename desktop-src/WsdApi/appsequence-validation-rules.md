---
description: Información de AppSequence contenida en WS-Discovery mensajes de anuncio y respuesta (Hello, ProbeMatches y ResolveMatches).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Reglas de validación de AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f2acec9d9d3858b5d68b0240499d95dba059ac1bcac745f1dc69bebc2056a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738657"
---
# <a name="appsequence-validation-rules"></a>Reglas de validación de AppSequence

Información de AppSequence contenida en WS-Discovery de anuncio y respuesta ([Hello](hello-message.md), [ProbeMatches](probematches-message.md)y [ResolveMatches](resolvematches-message.md)). WSDAPI procesa y valida esta información antes de que estos mensajes se pasen a componentes por encima de la pila (como Explorador de red o una aplicación que llama a WSDAPI).

En el xml siguiente se muestra un elemento AppSequence de ejemplo. El prefijo wsd hace referencia al espacio de nombres `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

WSDAPI omite los mensajes obsoletos. Para cada dispositivo (identificado de forma única por la dirección del punto de conexión en el cuerpo SOAP), WSDAPI omite los mensajes con un valor messageNumber de AppSequence inferior al último mensaje visto.

WSDAPI omite los anuncios obsoletos de XAddr. Si AppSequence InstanceId es menor que el último InstanceId visto, WSDAPI omite los XAddrs anunciados en el cuerpo SOAP. Además, si instanceId es el mismo que el anterior, pero MetadataVersion es menor que el último MetadataVersion, WSDAPI omite los XAddrs.

WSDAPI omite los mensajes WS-Discovery duplicados. Si se envían dos WS-Discovery idénticos a WSDAPI, solo se procesará el primer mensaje recibido. Normalmente, esto solo es relevante para las aplicaciones que llaman directamente a las interfaces [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) o [**IWSDiscoveryProvider.**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Patrones de mensajes de Exchange de detección y metadatos](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



