---
description: El propósito de este tema es describir la funcionalidad de detección implementada por WSDAPI, pero que no se describe en las especificaciones de DPWS o WS-Discovery.
ms.assetid: ae7eff53-c932-4cba-9e71-c60f308f0e2d
title: Funcionalidad de WS-Discovery adicional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9856605273bec9c757e0b29c389991bf061309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278548"
---
# <a name="additional-ws-discovery-functionality"></a>Funcionalidad de WS-Discovery adicional

En algunos casos, el [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) y las especificaciones relacionadas no definen explícitamente la funcionalidad de implementación. Por ejemplo, la especificación [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) no define el comportamiento del cliente y del host en entornos de host múltiple. Cuando se implementó WSDAPI, se agregó alguna funcionalidad de detección más allá de la funcionalidad definida en la especificación.

WSDAPI también implementa algunas partes seleccionadas del CD1 de WS-Discovery v 1.1 para comunicarse con un proxy de detección a través de HTTP.

El propósito de este tema es describir la funcionalidad de detección implementada por WSDAPI, pero que no se describe en las especificaciones de DPWS o WS-Discovery.

## <a name="ipv6-addresses-and-the-soapudp-uri-format"></a>Direcciones IPv6 y el formato de URI de SOAP. UDP

SOAP-over-UDP y WS-Discovery no describen explícitamente cómo se representa una dirección IPv6 literal en el formato de URI de SOAP. UDP. [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), titulado "identificadores uniformes de recursos (URI): Sintaxis genérica", indica que las direcciones IPv6 literales no son compatibles con el formato URI de SOAP. UDP.

Para simplificar, WSDAPI reconoce las direcciones IPv6 entre corchetes en el esquema SOAP. UDP. Por ejemplo, `soap.udp://[2001:abcd:0001:0002:0003:0004:0005:0032]:3702` WSDAPI reconoce la dirección. Esto es similar al modo en que se administran las direcciones IPv6 en HTTP.

## <a name="hello-and-xaddrs"></a>Hello y XAddrs

El objeto de hospedaje DPWS de WSDAPI nunca enviará un mensaje WS-Discovery [Hola](hello-message.md) con [XAddrs](xaddr-validation-rules.md) en el cuerpo del mensaje. Un cliente siempre enviará un mensaje de [resolución](resolve-message.md) después de recibir un mensaje de saludo si el cliente necesita obtener el XAddrs.

Este enfoque tiene dos ventajas. En primer lugar, un dispositivo generado en WSDAPI nunca expondrá XAddrs que revelen las direcciones IP de las redes privadas. En segundo lugar, un dispositivo generado en WSDAPI solo expone XAddrs que son accesibles para el cliente, lo que significa que las direcciones IPv6 no se envían nunca a un cliente IPv4.

Cuando se recibe un [sondeo](probe-message.md) o un mensaje de resolución, solo se envía un único XAddr en respuesta. El XAddr enviado corresponde a la dirección local en la que se recibió la solicitud. Si la solicitud se recibió entre subredes a través de IPv6, WSDAPI proporcionará una dirección IPv6 global en la respuesta.

## <a name="preferred-addresses"></a>Direcciones preferidas

Un dispositivo puede proporcionar varios XAddrs en un mensaje [Hello](hello-message.md), [ProbeMatch](probematches-message.md)o [ResolveMatch](resolvematches-message.md) . Un servicio también puede estar disponible en varios puntos de conexión con diferentes direcciones de transporte. En estos casos, WSDAPI intentará comunicarse con el dispositivo en la primera dirección utilizable que encuentre. Se puede usar una dirección si procede de un protocolo disponible, como IPv4 en un equipo donde está instalado IPv4 o IPv6 en un equipo en el que está instalado IPv6. Además, si la dirección procedía de un dispositivo o servicio que no está en la subred local, solo se puede usar si es IPv4, un sitio IPv6 local o un vínculo IPv6 local.

## <a name="wsdl-in-metadata-exchange"></a>WSDL en intercambio de metadatos

Los dispositivos y servicios compilados en WSDAPI no proporcionan su WSDL en el intercambio de metadatos a menos que la aplicación lo extienda para proporcionar esta información. De forma predeterminada, el aprovisionamiento de WSDL no forma parte del modelo de programación.

## <a name="app_max_delay"></a>\_retraso máximo de la aplicación \_

DPWS define \_ \_ el retraso máximo de la aplicación, el intervalo aleatorio para retrasar la recepción de un [sondeo](probe-message.md) y el envío de un [ProbeMatch](probematches-message.md), como 5.000 milisegundos. El Firewall de Windows requiere que el modelo de respuesta de unidifusión/solicitud de multidifusión para UDP solo funcione dentro de la ventana del firewall de 4 segundos. Como resultado, WSDAPI transmitirá respuestas en 2.500 ms o menos, en lugar de la ventana de 5.000 MS descrita por retraso máximo de la aplicación \_ \_ .

## <a name="iana-port-reservations"></a>Reservas de Puerto IANA

WSDAPI usa el puerto TCP 5357 para el tráfico HTTP y el puerto TCP 5358 para el tráfico HTTPS de forma predeterminada. Estos puertos se reservan para los procesos con menos privilegios a través de una reserva de direcciones URL en HTTP.sys y también se reservan con IANA.

## <a name="udp-port-sharing"></a>Uso compartido de puertos UDP

WSDAPI utiliza el uso compartido de puertos. Es posible que todas las aplicaciones basadas en WSDAPI no controlen correctamente los mensajes de unidifusión enviados al puerto 3702. Si una aplicación se enlaza exclusivamente al puerto 3702, puede impedir que las aplicaciones basadas en WSDAPI utilicen correctamente ese puerto.

## <a name="ws-discovery-v11-cd1-proxy"></a>Proxy CD1 de WS-Discovery v 1.1

WSDAPI buscará y se comunicará con un proxy de detección que implementa el protocolo de modo administrado del CD1 de WS-Discovery v 1.1. WS-Discovery v 1.1 CD1 es la primera revisión de WS-Discovery para incluir una descripción explícita de un protocolo HTTP para la comunicación entre un proxy y un cliente o dispositivo.

Para limitar el número de versiones simultáneas usadas en las solicitudes de multidifusión, WSDAPI envía una solicitud de sondeo WS-Discovery en el espacio de nombres 2005/04, pero busca el tipo DiscoveryProxy de la WS-Discovery v 1.1. Si un proxy responde, WSDAPI enviará un sondeo HTTP o resolverá la solicitud al extremo proxy especificado, tal como se define en el CD1 de WS-Discovery v 1.1.

 

 



