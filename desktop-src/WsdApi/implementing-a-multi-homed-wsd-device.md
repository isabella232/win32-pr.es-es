---
description: En este tema se describe la compatibilidad con dispositivos de host múltiple en WSDAPI y se proporcionan recomendaciones de implementación para desarrolladores de cliente y de dispositivo.
ms.assetid: d30ed536-d477-4f50-8c80-aacc35f948b9
title: Implementación de un dispositivo WSD de host múltiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac3537b96a577db47419d55cb5c6f732f8f7906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278966"
---
# <a name="implementing-a-multi-homed-wsd-device"></a>Implementación de un dispositivo WSD de host múltiple

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) y el [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) no describen la implementación de dispositivos de host múltiple. En este tema se describe la compatibilidad con dispositivos de host múltiple en WSDAPI y se proporcionan recomendaciones de implementación para desarrolladores de cliente y de dispositivo. En este tema se supone que los mensajes de detección se envían a través de IPv4 e IPv6 (si está disponible) con el mismo identificador de mensaje e información de secuenciación de aplicaciones.

## <a name="discovery-in-a-multi-homed-environment"></a>Detección en un entorno de host múltiple

Como se mencionó en la sección [Hello](hello-message.md) y [XAddrs](xaddr-validation-rules.md) de [funcionalidad adicional de WS-Discovery](additional-ws-discovery-functionality.md), WSDAPI nunca proporciona XAddrs en un mensaje Hello. Esto significa que se puede enviar el mismo mensaje de saludo en todas las interfaces de red con el mismo identificador de mensaje e información de secuenciación de aplicaciones. Esto hace que sea más fácil para la detección de colisiones de cliente descartar varios mensajes de saludo del mismo dispositivo cuando un cliente y el dispositivo comparten más de una subred.

Dado que los [XAddrs](xaddr-validation-rules.md) no se envían en el mensaje de [Hola](hello-message.md) , las implementaciones de cliente deben enviar un mensaje de [resolución](resolve-message.md) para obtener la dirección del dispositivo pertinente. La resolución se debe enviar en todas las interfaces de cliente con el mismo identificador de mensaje y el dispositivo debe filtrar los mensajes duplicados según sea necesario. El uso del mismo identificador de mensaje para el mensaje de resolución permite que el dispositivo elija una interfaz preferida para comunicarse con los clientes si es necesario.

Al enviar un mensaje [ResolveMatch](resolvematches-message.md) , un dispositivo debe proporcionar [XAddrs](xaddr-validation-rules.md) relacionados con la interfaz de red a través de la cual se transmite el mensaje de unidifusión. Esta práctica ayuda a evitar varios intentos de conexión de cliente y lógica de reintento complicada.

## <a name="metadata-exchange-in-a-multi-homed-environment"></a>Intercambio de metadatos en un entorno de host múltiple

Implementar el intercambio de metadatos en un entorno de host múltiple es más difícil que implementar la detección debido a las versiones de los metadatos. Si un cliente solicita metadatos a través de varias interfaces, el cliente puede recibir varios mensajes [GetResponse](getresponse--metadata-exchange--message.md) a través de distintas interfaces. Estos mensajes GetResponse pueden contener diferentes secciones de metadatos de **relación** con la misma versión de metadatos. Esto reduce el valor del número de versión de los metadatos.

Existe un enfoque alternativo, en el que se envía un solo mensaje de [GetResponse](getresponse--metadata-exchange--message.md) en respuesta con todas las direcciones del servicio. El inconveniente de este método es que se puede divulgar información privada, como la topología de redes accesibles indirectamente.

En Windows Vista, los metadatos proporcionados por WSDAPI solo contienen direcciones que son válidas para la interfaz en la que se recibió la solicitud de metadatos.

 

 



