---
description: En este tema se describe la compatibilidad con dispositivos de varios entornos en WSDAPI y se proporcionan recomendaciones de implementación a los desarrolladores de clientes y dispositivos.
ms.assetid: d30ed536-d477-4f50-8c80-aacc35f948b9
title: Implementación de un dispositivo WSD de varios alojamientos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ac83b0fe3b951e02e77ef9efc6241ce5a7e1780106b1e85e4f00b987bbbe05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991745"
---
# <a name="implementing-a-multi-homed-wsd-device"></a>Implementación de un dispositivo WSD de varios alojamientos

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) y el perfil de dispositivos para [servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) no describen la implementación de dispositivos de varios entornos. En este tema se describe la compatibilidad con dispositivos de varios entornos en WSDAPI y se proporcionan recomendaciones de implementación a los desarrolladores de clientes y dispositivos. En este tema, se supone que los mensajes de detección se envían a través de IPv4 e IPv6 (si están disponibles) con el mismo identificador de mensaje y la misma información de secuenciación de la aplicación.

## <a name="discovery-in-a-multi-homed-environment"></a>Detección en un entorno de varias residencias

Como se [mencionó en la](hello-message.md) sección Hello and XAddrs (Hello y [XAddrs)](xaddr-validation-rules.md) de [Additional WS-Discovery Functionality](additional-ws-discovery-functionality.md)(Funcionalidad adicional de WS-Discovery), WSDAPI nunca proporciona XAddrs en un mensaje Hello. Esto significa que se puede enviar el mismo mensaje Hello en todas las interfaces de red con el mismo identificador de mensaje y la misma información de secuenciación de aplicaciones. Esto facilita la detección de colisiones de cliente para descartar varios mensajes Hello del mismo dispositivo cuando un cliente y el dispositivo comparten más de una subred.

Dado que [los XAddrs](xaddr-validation-rules.md) no se envían en el mensaje [Hello,](hello-message.md) las implementaciones de cliente deben enviar un [mensaje Resolver](resolve-message.md) para obtener la dirección de dispositivo correspondiente. Resolver debe enviarse en todas las interfaces de cliente con el mismo identificador de mensaje y el dispositivo debe filtrar los mensajes duplicados según sea necesario. El uso del mismo identificador de mensaje para resolver el mensaje permite al dispositivo elegir una interfaz preferida para comunicarse con los clientes si es necesario.

Al enviar un [mensaje ResolveMatch,](resolvematches-message.md) un dispositivo debe proporcionar [XAddrs](xaddr-validation-rules.md) que se relacionan con la interfaz de red a través de la que se desenvía el mensaje. Esta práctica ayuda a evitar varios intentos de conexión de cliente y una lógica de reintento complicada.

## <a name="metadata-exchange-in-a-multi-homed-environment"></a>Intercambio de metadatos en un entorno de varias propiedades

Implementar el intercambio de metadatos en un entorno de varias propiedades es más difícil que implementar la detección debido al control de versiones de los metadatos. Si un cliente solicita metadatos a través de varias interfaces, el cliente puede recibir varios [mensajes GetResponse](getresponse--metadata-exchange--message.md) a través de interfaces diferentes. Estos mensajes GetResponse pueden contener diferentes secciones **de metadatos** de relación con la misma versión de metadatos. Esto reduce el valor del número de versión de metadatos.

Hay un enfoque alternativo, donde se envía un único [mensaje GetResponse](getresponse--metadata-exchange--message.md) en respuesta con todas las direcciones del servicio. La desventaja de este método es que se puede revelar información privada, como la topología de redes accesibles indirectamente.

En Windows Vista, los metadatos proporcionados por WSDAPI solo contienen direcciones válidas para la interfaz en la que se recibió la solicitud de metadatos.

 

 



