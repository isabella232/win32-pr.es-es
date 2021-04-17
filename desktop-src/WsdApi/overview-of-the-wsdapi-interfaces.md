---
description: Servicios web en la API de dispositivos (WSDAPI) se usa para desarrollar aplicaciones cliente que encuentren y accedan a dispositivos, y para desarrollar hosts de dispositivos y servicios asociados que se ejecuten en Windows Vista y Windows Server 2008.
ms.assetid: 2b23d7d3-3b06-48c8-993e-49c72b139624
title: Información general de las interfaces de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3e728971741f97707c1dc72effdaf0ca17dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696904"
---
# <a name="overview-of-the-wsdapi-interfaces"></a>Información general de las interfaces de WSDAPI

Servicios web en la API de dispositivos (WSDAPI) se usa para desarrollar aplicaciones cliente que encuentren y accedan a dispositivos, y para desarrollar hosts de dispositivos y servicios asociados que se ejecuten en Windows Vista y Windows Server 2008. La API de [detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) y la herramienta [WsdCodeGen](web-services-for-devices-code-generator.md) son herramientas adicionales que se pueden usar para el cliente, el host de dispositivo y el desarrollo del servicio. Las interfaces WSDAPI se pueden usar directamente para exponer la funcionalidad avanzada.

## <a name="major-wsdapi-interfaces"></a>Principales interfaces WSDAPI

Las cuatro interfaces principales de WSDAPI son [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider), [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher), [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)y [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost). Para obtener una lista de todas las interfaces de WSDAPI, consulte [servicios web en interfaces de dispositivos](web-services-for-devices-interfaces.md).

## <a name="iwsdiscoveryprovider"></a>IWSDiscoveryProvider

[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) se usa para implementar la funcionalidad de WS-Discovery en los clientes.

[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) emite WS-Discovery [sondear](probe-message.md) y [resolver](resolve-message.md) mensajes, y recibe mensajes [Hello](hello-message.md), [bye](bye-message.md), [ProbeMatches](probematches-message.md)y [ResolveMatches](resolvematches-message.md) . Use la información recuperada a través de la interfaz **IWSDiscoveryProvider** al crear una interfaz [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) que se usa para describir y controlar un dispositivo DPWS específico.

Una interfaz [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) no es necesaria cuando se resuelve simplemente una dirección de dispositivo DPWS determinada antes de crear un proxy de dispositivo. [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) resolverá automáticamente la dirección del dispositivo si es necesario.

La API de [detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) se puede usar para la detección de dispositivos y servicios genéricos, ya que la API puede detectar dispositivos DPWS y también dispositivos que usan otros protocolos. Considere la posibilidad de usar la detección de funciones al escribir una aplicación de detección genérica.

## <a name="iwsdiscoverypublisher"></a>IWSDiscoveryPublisher

[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) se usa para implementar la funcionalidad de WS-Discovery en los servicios de destino, como los dispositivos.

[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) permite que una aplicación publique su presencia mediante WS-Discovery mensajes Hello y bye. Esta interfaz permite a una aplicación recibir solicitudes de sondeo y resolución, y construir y enviar respuestas ProbeMatches y ResolveMatches.

Una interfaz [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) no es necesaria al publicar simplemente la existencia de un objeto [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) . **IWSDDeviceHost** administra su propia presencia WS-Discovery.

## <a name="iwsddeviceproxy"></a>IWSDDeviceProxy

[**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) se usa para implementar la funcionalidad WS-Discovery, WS-MetadataExchange y control del lado cliente. Esta funcionalidad incluye capacidades opcionales de canal seguro, WS-Eventing y datos adjuntos.

La interfaz [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) tiene los tres usos siguientes.

-   Resuelve las direcciones lógicas del dispositivo, si es necesario.
-   Inicia solicitudes de metadatos a los dispositivos para enumerar los tipos y las direcciones de los servicios.
-   Proporciona un origen para los objetos [**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy) , que se puede usar para emitir mensajes de control a servicios específicos en un dispositivo.

Normalmente, el objeto [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) se crea y se usa completamente dentro del código generado por [WsdCodeGen](web-services-for-devices-code-generator.md).

## <a name="iwsddevicehost"></a>IWSDDeviceHost

[**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) se usa para implementar la funcionalidad de hospedaje de WS-Discovery, WS-MetadataExchange y Service del lado del dispositivo. Los servicios hospedados pueden responder a los mensajes de control y pueden admitir las capacidades de canal seguro, WS-Eventing y Attachment.

La interfaz [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) tiene los siguientes usos.

-   Hospeda objetos de servicio.
-   Anuncia la presencia de un host de dispositivo en la red mediante WS-Discovery.
-   Responde a solicitudes de WS-MetadataExchange y describe los tipos y las ubicaciones de los servicios hospedados.
-   Envía las solicitudes de red a los objetos de servicio.

La funcionalidad de administración de suscripciones de WS-Discovery, WS-MetadataExchange y WS-Eventing se controla completamente dentro del objeto host del dispositivo. Para poder hospedar un servicio dentro de un host de dispositivo, deben cumplirse los siguientes requisitos.

-   El host debe crearse mediante una llamada a [**WSDCreateDeviceHost**](/windows/desktop/api/WsdHost/nf-wsdhost-wsdcreatedevicehost).
-   Los metadatos asociados con el servicio deben estar registrados.
-   El propio servicio debe estar registrado.
-   Se debe iniciar el host del dispositivo.

Normalmente, el objeto [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) se crea y se usa dentro del código generado por [WsdCodeGen](web-services-for-devices-code-generator.md).

 

 
