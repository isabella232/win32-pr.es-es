---
description: 'Más información sobre: cumplimiento de especificación de WS-Discovery'
ms.assetid: b795a385-b48d-4a16-9d91-e48bca120572
title: Cumplimiento de especificación de WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcae062448b1913f0cc62dff3b6c86b98280a902
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423592"
---
# <a name="ws-discovery-specification-compliance"></a>Cumplimiento de especificación de WS-Discovery

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) describe cómo realizar las tareas siguientes:

-   Anunciar la disponibilidad de los servicios en la subred local
-   Buscar servicios en la subred
-   Buscar un servicio al que se hace referencia anteriormente

Para ello, WS-Discovery define mensajes 2 1, [Hello](hello-message.md) y [bye](bye-message.md), y dos mensajes de búsqueda bidireccionales, [sondeo](probe-message.md) y [resolución](resolve-message.md).

WS-Discovery también proporciona direcciones y un puerto reservado para la detección local de vínculos IPv4 e IPv6. La especificación también permite definir enlaces alternativos en otro lugar, como el enlace de sondeo en HTTP definido en el [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).

La especificación de WS-Discovery describe la funcionalidad optativa mediante el uso de los términos que se pueden o deben tener en una recomendación o restricción de implementación determinada. La funcionalidad omitida puede ser la que se describe en la especificación de WS-Discovery que no se implementó en WSDAPI, o puede ser una funcionalidad que WSDAPI se implementó en un método que no se ha especificado en la especificación WS-Discovery.

En este tema se describe cómo se administran las restricciones de WS-Discovery, los requisitos y la funcionalidad optativa en la implementación de WSDAPI. Este tema se lee mejor en conjunto con la especificación WS-Discovery.

## <a name="ws-discovery-and-soap-over-udp-support"></a>Compatibilidad con WS-Discovery y SOAP-over-UDP

En SOAP-over-UDP, la sección 3,2 especifica que el mensaje UDP debe caber en un datagrama de 64 KB. WSDAPI aceptará mensajes UDP de 64 KB, pero la restricción DPWS de \_ tamaño de sobre máximo \_ (32k) restringirá el tamaño del mensaje. Tal y como requiere [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf), WSDAPI admite los patrones de mensaje descritos en la sección 4.

WSDAPI puede configurarse para admitir el modelo de seguridad en las secciones 7 y 8. Cuando está configurado, WSDAPI firmará los mensajes de WS-Discovery salientes y validará las firmas en los mensajes entrantes.

WSDAPI implementa el algoritmo de retransmisión definido en el Apéndice I, modificado por DPWS Apéndice I.

En WS-Discovery, WSDAPI usa las direcciones especificadas en la sección 2,4. WSDAPI extiende \_ \_ el retraso máximo de la aplicación desde la sección 2,4, pero no hasta la extensión tal como se define en el Apéndice I de DPWS. Para obtener más información sobre el retraso máximo de la aplicación \_ \_ , consulte [funcionalidad adicional de WS-Discovery](additional-ws-discovery-functionality.md).

WS-Discovery describe la `uuid:` recomendación de formato de URI en la sección 2,6, pero WSDAPI invalida esta recomendación. En su lugar, WSDAPI usa el `urn:uuid:` formato de URI que se describe en DPWS.

En la sección 3 de WS-Discovery se describe cómo interactúa un cliente con un proxy de detección. WSDAPI no reconoce esta interacción y omite los anuncios de los servidores proxy de detección. En Windows 7, WSDAPI implementa una extensión privada para el protocolo de WS-Discovery, WS-Discovery extensiones remotas, para permitir a los clientes de detección buscar servicios distribuidos en varias redes diferentes mediante el envío de solicitudes a servidores proxy centralizados. Para obtener más información, vea [funcionalidad adicional de WS-Discovery](additional-ws-discovery-functionality.md).

En la sección 4,1, el párrafo 3 de WS-Discovery requiere que un temporizador debe transcurrir antes de que se envíe un mensaje [Hello](hello-message.md) . La API de hospedaje no espera antes de enviar un mensaje de saludo. Si un escenario requiere un retraso antes de que se envíe un mensaje de saludo, el desarrollador de la aplicación debe implementar una espera.

WSDAPI implementa todos los mensajes descritos en WS-Discovery secciones 4, 5 y 6. WSDAPI también aplica el tiempo de espera de coincidencia \_ descrito en la sección 7, tal como se ha modificado por DPWS Apéndice I. WSDAPI solo protege contra la "reproducción" de las consideraciones seguras en la sección 9.

WSDAPI implementa la secuenciación de aplicaciones como se describe en WS-Discovery Apéndice I.

 

 



