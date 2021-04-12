---
description: Servicios web en la API de dispositivos (WSDAPI) proporciona compatibilidad con el perfil de dispositivos para servicios web (DPWS) en Windows Vista, que permite la comunicación de servicios web (WS) entre equipos basados en Windows y dispositivos conectados a la red.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Compatibilidad con la especificación WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276960"
---
# <a name="wsdapi-specification-compliance"></a>Compatibilidad con la especificación WSDAPI

Servicios web en la API de dispositivos (WSDAPI) proporciona compatibilidad con el [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) en Windows Vista, que permite la comunicación de servicios web (WS) entre equipos basados en Windows y dispositivos conectados a la red. DPWS ensambla especificaciones básicas de WS, como [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)y [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), y las mejora o las limita para proporcionar un conjunto básico de funcionalidades para dispositivos restringidos por recursos. Esta especificación de línea de base contiene la funcionalidad necesaria, como la capacidad de describir las propiedades del dispositivo a través de metadatos, y la funcionalidad opcional, como la capacidad de rechazar mensajes específicos por motivos de seguridad.

La implementación de WSDAPI en Windows Vista es la primera versión de la compatibilidad explícita con DPWS y es una implementación no administrada de DPWS que es independiente y distinta de otras implementaciones de servicios web (como el [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) o [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).

Los temas siguientes son de interés para los fabricantes de dispositivos y otros implementadores de dispositivos que crean dispositivos que interoperan con clientes y hosts de WSDAPI basados en Windows sin usar WSDAPI. En estos temas se describe la implementación de WSDAPI en relación con las especificaciones subyacentes. Cubren la implementación de la funcionalidad necesaria, la funcionalidad opcional y la funcionalidad adicional no definida en la especificación.

-   [Compatibilidad con la especificación DPWS](dpws-specification-compliance.md)
-   [Compatibilidad con la especificación de WS-Discovery](ws-discovery-specification-compliance.md)
-   [Cumplimiento de especificación de WS-MetadataExchange y WS-Transfer](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Funcionalidad de WS-Discovery adicional](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de dispositivos WSD](wsd-device-development.md)
</dt> <dt>

[Recomendaciones de implementación de dispositivos WSD](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
