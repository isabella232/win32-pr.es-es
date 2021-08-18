---
description: 'Más información sobre: Cumplimiento de WS-Discovery especificación'
ms.assetid: b795a385-b48d-4a16-9d91-e48bca120572
title: WS-Discovery cumplimiento de la especificación de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07794140f05a065fb770ae2d5782f24180fb7e7ef66757278d5c5c93a3fd7e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991415"
---
# <a name="ws-discovery-specification-compliance"></a>WS-Discovery cumplimiento de la especificación de datos

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) describe cómo realizar las siguientes tareas:

-   Anuncio de la disponibilidad de servicios en la subred local
-   Búsqueda de servicios en la subred
-   Buscar un servicio al que se hace referencia previamente

Para ello, WS-Discovery dos mensajes unidireccionales, [Hello](hello-message.md) y [Bye](bye-message.md), y dos mensajes de búsqueda bidireccionales, [Probe](probe-message.md) y [Resolve](resolve-message.md).

WS-Discovery también proporciona direcciones y un puerto reservado para la detección local de vínculos IPv4 e IPv6. La especificación también permite definir enlaces alternativos en otra parte, como el enlace De sondeo a través de HTTP definido en el perfil de dispositivos para servicios [web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).

La WS-Discovery especificación describe la funcionalidad optativa mediante los términos MAY o SHOULD en una recomendación o restricción de implementación determinada. La funcionalidad omitida puede ser una funcionalidad descrita como REQUIRED en la especificación de WS-Discovery que no se implementó mediante WSDAPI, o puede ser una funcionalidad que WSDAPI implementó en un método distinto del especificado en la especificación WS-Discovery.

En este tema se describe cómo WS-Discovery las restricciones, los requisitos y la funcionalidad de elección mediante la implementación de WSDAPI. Este tema se lee mejor conjuntamente con la especificación WS-Discovery datos.

## <a name="ws-discovery-and-soap-over-udp-support"></a>WS-Discovery y compatibilidad con SOAP sobre UDP

En SOAP sobre UDP, la sección 3.2 especifica que el mensaje UDP debe caber en un datagrama de 64 000. WSDAPI aceptará mensajes UDP de 64 K, pero la restricción DPWS de MAX \_ ENVELOPE \_ SIZE (32K) restringirá el tamaño del mensaje. Como requiere [WS-Discovery,](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)WSDAPI admite los patrones de mensaje descritos en la sección 4.

WSDAPI puede configurarse para admitir el modelo de seguridad en las secciones 7 y 8. Cuando esté configurado, WSDAPI firmará los mensajes WS-Discovery salida y validará las firmas en los mensajes entrantes.

WSDAPI implementa el algoritmo de retransmisión definido en el Apéndice I tal como lo ha modificado el Apéndice I de DPWS.

En WS-Discovery, WSDAPI usa las direcciones especificadas en la sección 2.4. WSDAPI extiende APP MAX DELAY desde la sección 2.4, pero no en la medida definida en el Apéndice \_ \_ I de DPWS. Para obtener más información sobre APP \_ MAX \_ DELAY, vea [Additional WS-Discovery Functionality](additional-ws-discovery-functionality.md).

WS-Discovery describe la recomendación de formato uri en la `uuid:` sección 2.6, pero WSDAPI invalida esta recomendación. En su lugar, WSDAPI usa el `urn:uuid:` formato uri descrito en DPWS.

En la sección 3 WS-Discovery describe cómo interactúa un cliente con un proxy de detección. WSDAPI no reconoce esta interacción y omite los anuncios de los servidores proxy de detección. En Windows 7, WSDAPI implementa una extensión privada al protocolo WS-Discovery, WS-Discovery Remote Extensions, para permitir que los clientes de detección busquen servicios distribuidos entre muchas redes diferentes mediante el envío de solicitudes a servidores proxy centralizados. Para obtener más información, vea [Additional WS-Discovery Functionality](additional-ws-discovery-functionality.md).

La sección 4.1, párrafo 3 del WS-Discovery requiere que un temporizador transcurra antes de que [se](hello-message.md) envíe un mensaje Hello. La API de hospedaje no espera antes de enviar un mensaje Hello. Si un escenario requiere un retraso antes de que se envíe un mensaje Hello, el desarrollador de la aplicación debe implementar una espera.

WSDAPI implementa todos los mensajes descritos en WS-Discovery secciones 4, 5 y 6. WSDAPI también aplica el tiempo de espera de coincidencia descrito en la sección 7, tal como lo ha modificado el Apéndice I de DPWS. WSDAPI solo protege contra "Replay" de las consideraciones seguras de la \_ sección 9.

WSDAPI implementa la secuenciación de aplicaciones como se describe en WS-Discovery apéndice I.

 

 



