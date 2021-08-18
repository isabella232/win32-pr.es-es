---
description: Web Services on Devices API (WSDAPI) proporciona compatibilidad con el perfil de dispositivos para servicios web (DPWS) en Windows Vista, lo que permite la comunicación de servicios web (WS) entre equipos basados en Windows y dispositivos conectados a la red.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Cumplimiento de la especificación WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dcf649d8d2771d17f24e983a739c0119a0fe8af67f70b706ba35bcddec20d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991395"
---
# <a name="wsdapi-specification-compliance"></a>Cumplimiento de la especificación WSDAPI

Web Services on Devices API (WSDAPI) proporciona compatibilidad con el perfil de dispositivos para servicios web [](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) en Windows Vista, lo que permite la comunicación de servicios web (WS) entre equipos basados en Windows y dispositivos conectados a la red. DPWS ensambla especificaciones básicas de WS, como [WS-Eventing,](https://schemas.xmlsoap.org/ws/2004/08/eventing/) [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)y [WS-MetadataExchange,](https://schemas.xmlsoap.org/ws/2004/09/mex/)y las mejora o restringe para proporcionar un conjunto de funcionalidades de línea de base para dispositivos con restricciones de recursos. Esta especificación de línea base contiene la funcionalidad necesaria, como la capacidad de describir las propiedades del dispositivo a través de metadatos y la funcionalidad opcional, como la capacidad de rechazar mensajes específicos por motivos de seguridad.

La implementación de WSDAPI en Windows Vista es la primera versión de compatibilidad explícita con DPWS y es una implementación no administrada de DPWS que es independiente y distinta de otras implementaciones de servicios web (como [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) o [WS-Management).](https://schemas.xmlsoap.org/ws/2005/06/management/)

Los temas siguientes son de interés para los fabricantes de dispositivos y otros implementadores de dispositivos que crean dispositivos que interoperan con hosts y clientes WSDAPI basados en Windows sin usar WSDAPI. En estos temas se describe la implementación de WSDAPI en relación con las especificaciones subyacentes. Cubren la implementación de la funcionalidad necesaria, la funcionalidad opcional y la funcionalidad adicional no definida en la especificación.

-   [Cumplimiento de la especificación de DPWS](dpws-specification-compliance.md)
-   [Cumplimiento de la especificación de WS-Discovery](ws-discovery-specification-compliance.md)
-   [WS-MetadataExchange y cumplimiento de WS-Transfer especificación](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Funcionalidad de WS-Discovery adicional](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de dispositivos WSD](wsd-device-development.md)
</dt> <dt>

[Implementación de dispositivos WSD Recomendaciones](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
