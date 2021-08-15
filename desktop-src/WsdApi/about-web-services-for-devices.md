---
description: Web Service on Devices API (WSDAPI) es una implementación del perfil de dispositivos para servicios web (DPWS) para Windows Vista y Windows Server 2008.
ms.assetid: 8eaeacb3-43db-4a57-8548-e5b81213269c
title: Acerca de los servicios web en dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7facef3bfed004a834e151db0c58c83a1576e515ed89fa0d690813bc4c18bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552523"
---
# <a name="about-web-services-on-devices"></a>Acerca de los servicios web en dispositivos

Web Service on Devices API (WSDAPI) es una implementación del perfil de dispositivos para servicios [web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) para Windows Vista y Windows Server 2008. DPWS restringe las especificaciones de servicios web para que los clientes puedan detectar fácilmente los dispositivos. Una vez detectado un dispositivo, un cliente puede recuperar una descripción de los servicios hospedados en ese dispositivo y usar esos servicios.

## <a name="devices-and-services"></a>Dispositivos y servicios

*Los* dispositivos son componentes, normalmente hardware, que están conectados a la red. Algunos ejemplos son impresoras, cámaras web y sistemas de vídeo.

Los dispositivos pueden incluir cero o más *servicios.* Por ejemplo, un dispositivo de vídeo puede incluir servicios que admiten encendido y apagado, control de reproducción, expulsión multimedia y streaming de vídeo. El control de reproducción puede admitir acciones como reproducir, pausar, rebobinar y avanzar rápidamente.

## <a name="discovering-and-manipulating-a-device"></a>Detectar y manipular un dispositivo

WSDAPI amplía el modelo de Plug and Play local al permitir que un cliente detecte y acceda a un dispositivo remoto y sus servicios asociados a través de una red. Admite la detección, la mensajería de control un solo sentido y la mensajería de control de dos vías, y eventos.

![Diagrama que muestra cómo WSDAPI permite que un cliente detecte y acceda a un dispositivo remoto.](images/overview01.png)

Los dispositivos DPWS anuncian su presencia y exponen servicios (si los hay) mediante una dirección única y un conjunto estandarizado de mensajes XML. Los clientes de DPWS pueden usar el proceso de detección para encontrar el dispositivo, enumerar sus servicios y conectarse a esos servicios para realizar acciones específicas.

Un cliente de WSDAPI consulta primero el dispositivo para obtener descripciones completas de sus servicios, incluidos los tipos de servicio (como un tipo de servicio de impresora o un tipo de servicio de escáner). A continuación, el cliente controla el dispositivo mediante una llamada a comandos definidos por un tipo de servicio (por ejemplo, llamando a **CreatePrintJob** en un dispositivo con un tipo de servicio de impresora). Opcionalmente, el cliente también puede supervisar los cambios de estado en cada servicio mediante la suscripción a eventos que se producen durante la ejecución del comando.

![Diagrama que muestra cómo un cliente de WSDAPI consulta e interactúa con un dispositivo.](images/netdevice01.png)

Para obtener más información sobre los patrones de mensajería de dispositivos, vea [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).

## <a name="logical-and-physical-addressing"></a>Direccionamiento lógico y físico

El direccionamiento lógico se usa para identificar de forma única los dispositivos independientes de sus direcciones físicas. WS-Discovery proporciona un mecanismo para resolver direcciones lógicas en direcciones físicas, lo que permite que se lleve a cabo la mensajería de cliente a dispositivo. Un ejemplo es el almacenamiento conectado a la red (NAS) que lleva con usted. Si tiene un portátil y un NAS, el portátil debe ser capaz de reconocer que es el mismo dispositivo, independientemente de la dirección física (dirección IP) que el NAS obtenga a medida que se mueve entre subredes. Para ello, es necesario que el dispositivo tenga una identidad independiente de la dirección IP que obtenga. puesto que los mecanismos tradicionales como DNS no están disponibles en un escenario de itinerancia normal, WS-Addressing y WS-Discovery proporcionan direccionamiento lógico y resolución como alternativa ad hoc.

Cuando se fabrica un dispositivo, se le da un identificador único global, representado como un URI uuid. Este identificador nunca cambiará para el dispositivo. Cuando el dispositivo está encendido, siempre anunciará su dirección lógica a través de un mensaje de WS-Discovery [Hello](hello-message.md) y aceptará solicitudes para convertirla en una dirección física (normalmente HTTP) a través de mensajes de WS-Discovery [Resolve](resolve-message.md) [o Probe.](probe-message.md) Una vez que se obtiene una dirección física válida (dirección IP), toda la mensajería se produce a través de esa dirección y WS-Discovery solo se usa si la dirección cambia, el dispositivo cambia de estado y es necesario notificar a los clientes o el dispositivo se queda sin conexión.

## <a name="building-applications"></a>Creación de aplicaciones

WSDAPI proporciona una pila SOAP de DPWS genérica para que la usen las aplicaciones cliente y de servicio. El [Generador de](web-services-for-devices-code-generator.md) código de servicios web en dispositivos (WsdCodeGen.exe) se puede usar para convertir una descripción del servicio (WSDL) en código proxy y de código auxiliar al que las aplicaciones pueden llamar directamente. Este código generado transforma automáticamente las llamadas de función y los parámetros en mensajes SOAP y campos XML y, a continuación, llama a WSDAPI para emitir solicitudes al dispositivo o cliente remoto.

La detección de funciones se puede usar al compilar aplicaciones WSDAPI para crear y activar instancias de función devueltas por PnP. Estas instancias de función contienen datos que se pueden usar para obtener más información a través de las API de PnP cuando se requiere algo más que una simple detección. Para obtener más información, vea [Detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) [y PnP-X.](/previous-versions/windows/desktop/fundisc/pnp-x)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Patrones de mensaje de Exchange de detección y metadatos](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Cumplimiento de la especificación WSDAPI](wsdapi-specification-compliance.md)
</dt> <dt>

[Introducción a las interfaces de WSDAPI](overview-of-the-wsdapi-interfaces.md)
</dt> </dl>

 

 
