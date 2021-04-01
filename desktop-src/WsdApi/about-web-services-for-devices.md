---
description: El servicio Web de la API de dispositivos (WSDAPI) es una implementación del perfil de dispositivos para servicios web (DPWS) para Windows Vista y Windows Server 2008.
ms.assetid: 8eaeacb3-43db-4a57-8548-e5b81213269c
title: Acerca de los servicios web en dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca7f7dc97dabd3dde7af12f3cece992b4f0ef6d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "103914018"
---
# <a name="about-web-services-on-devices"></a>Acerca de los servicios web en dispositivos

El servicio Web de la API de dispositivos (WSDAPI) es una implementación del [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) para Windows Vista y windows Server 2008. DPWS restringe las especificaciones de los servicios web para que los clientes puedan detectar fácilmente los dispositivos. Una vez que se detecta un dispositivo, un cliente puede recuperar una descripción de los servicios hospedados en ese dispositivo y usar esos servicios.

## <a name="devices-and-services"></a>Dispositivos y servicios

Los *dispositivos* son componentes, normalmente hardware, que están conectados a la red. Algunos ejemplos son las impresoras, las cámaras Web y los sistemas de vídeo.

Los dispositivos pueden incluir cero o más *servicios*. Por ejemplo, un dispositivo de vídeo puede incluir servicios que admiten el encendido y apagado, el control de reproducción, la extracción multimedia y el streaming de vídeo. El control de reproducción puede admitir acciones como reproducir, pausar, rebobinar y avance rápido.

## <a name="discovering-and-manipulating-a-device"></a>Detección y manipulación de un dispositivo

WSDAPI amplía el modelo de Plug and Play local permitiendo que un cliente detecte y acceda a un dispositivo remoto y sus servicios asociados a través de una red. Admite la detección, la mensajería de control unidireccional y bidireccional, y el evento.

![Diagrama que muestra cómo WSDAPI permite a un cliente detectar y tener acceso a un dispositivo remoto.](images/overview01.png)

Los dispositivos DPWS anuncian su presencia y exponen servicios (si existen) mediante una dirección única y un conjunto normalizado de mensajes XML. Los clientes de DPWS pueden usar el proceso de detección para buscar el dispositivo, enumerar sus servicios y conectarse a esos servicios para realizar acciones específicas.

Un cliente WSDAPI primero consulta el dispositivo para obtener descripciones completas de sus servicios, incluidos los tipos de servicio (como un tipo de servicio de impresora o un tipo de servicio de analizador). A continuación, el cliente controla el dispositivo mediante una llamada a comandos definidos por un tipo de servicio (por ejemplo, mediante una llamada a **CreatePrintJob** en un dispositivo con un tipo de servicio de impresora). Opcionalmente, el cliente también puede supervisar los cambios de estado en cada servicio suscribiéndose a los eventos que se producen durante la ejecución del comando.

![Diagrama que muestra cómo un cliente de WSDAPI consulta e interactúa con un dispositivo.](images/netdevice01.png)

Para obtener más información acerca de los patrones de mensajería de dispositivos, consulte [patrones de mensajes de intercambio de metadatos y detección](discovery-and-metadata-exchange-message-patterns.md).

## <a name="logical-and-physical-addressing"></a>Direcciones lógicas y físicas

El direccionamiento lógico se usa para identificar de forma exclusiva los dispositivos independientes de sus direcciones físicas. WS-Discovery proporciona un mecanismo para resolver direcciones lógicas en direcciones físicas, lo que permite que se lleve a cabo la mensajería de cliente a dispositivo. Un ejemplo es el almacenamiento conectado a la red (NAS) que le lleva. Si tiene un portátil y un NAS, el portátil debe ser capaz de reconocer que es el mismo dispositivo, independientemente de la dirección física (dirección IP) que el NAS obtiene a medida que se mueve entre subredes. Para ello, es necesario que el dispositivo tenga una identidad que sea independiente de la dirección IP que obtenga; Dado que los mecanismos tradicionales como DNS no están disponibles en un escenario de itinerancia normal, WS-Addressing y WS-Discovery proporcionan direccionamiento lógico y resolución como alternativa ad hoc.

Cuando se fabrica un dispositivo, se le asigna un identificador único global, que se representa como un URI de UUID. Este identificador nunca cambiará para el dispositivo. Cuando el dispositivo se enciende, siempre anunciará su dirección lógica a través de un mensaje de WS-Discovery [Hello](hello-message.md) y aceptará solicitudes para convertirlos en una dirección física (normalmente http) a través de WS-Discovery mensajes de [sondeo](probe-message.md) o de [resolución](resolve-message.md) . Una vez que se obtiene una dirección física (dirección IP) válida, toda la mensajería se realiza a través de esa dirección y WS-Discovery se usa solo si cambia la dirección, el dispositivo cambia de estado y los clientes deben recibir una notificación, o el dispositivo se queda sin conexión.

## <a name="building-applications"></a>Creación de aplicaciones

WSDAPI proporciona una pila SOAP DPWS genérica para su uso por parte de aplicaciones de cliente y de servicio. El [generador de código de servicios web en dispositivos](web-services-for-devices-code-generator.md) (WsdCodeGen.exe) se puede usar para convertir una descripción del servicio (WSDL) en código auxiliar y proxy que las aplicaciones pueden llamar directamente. Este código generado transforma automáticamente las llamadas a funciones y los parámetros en los mensajes SOAP y los campos XML y, a continuación, llama a WSDAPI para emitir solicitudes al cliente o dispositivo remoto.

La detección de funciones se puede usar al compilar aplicaciones de WSDAPI para crear y activar instancias de función devueltas por PnP. Estas instancias de función contienen datos que se pueden usar para obtener más información a través de las API de PnP cuando se requiere algo más que simplemente la detección simple. Para obtener más información, vea [detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) y [PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Patrones de mensajes de intercambio de metadatos y detección](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Compatibilidad con la especificación WSDAPI](wsdapi-specification-compliance.md)
</dt> <dt>

[Información general de las interfaces de WSDAPI](overview-of-the-wsdapi-interfaces.md)
</dt> </dl>

 

 
