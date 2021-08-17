---
description: El propósito de este tema es describir la funcionalidad de detección implementada por WSDAPI, pero que no se describe de otro modo en las especificaciones de DPWS WS-Discovery.
ms.assetid: ae7eff53-c932-4cba-9e71-c60f308f0e2d
title: Funcionalidad de WS-Discovery adicional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7ee4094950c51ed84724abb9eaea493f7dad7cf7803832fb6e8762fdd99811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106783"
---
# <a name="additional-ws-discovery-functionality"></a>Funcionalidad de WS-Discovery adicional

En algunos casos, el perfil [de dispositivos](https://specs.xmlsoap.org/ws/2006/02/devprof/) para servicios web (DPWS) y las especificaciones relacionadas no definen explícitamente la funcionalidad de implementación. Por ejemplo, la [especificación WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) no define el comportamiento de cliente y host en entornos de varias propiedades. Cuando se implementó WSDAPI, se agregó alguna funcionalidad de detección más allá de la funcionalidad definida en la especificación.

WSDAPI también implementa partes seleccionadas de WS-Discovery v1.1 CD1 para comunicarse con un proxy de detección a través de HTTP.

El propósito de este tema es describir la funcionalidad de detección implementada por WSDAPI, pero que no se describe de otro modo en las especificaciones de DPWS WS-Discovery.

## <a name="ipv6-addresses-and-the-soapudp-uri-format"></a>Direcciones IPv6 y el formato de URI soap.udp

Soap sobre UDP y WS-Discovery no describen explícitamente cómo se representa una dirección IPv6 literal en el formato de URI soap.udp. [RFC 2396,](https://www.ietf.org/rfc/rfc2396.txt)titulado "Identificadores uniformes de recursos (URI): sintaxis genérica", indica que las direcciones IPv6 literales no son compatibles con el formato de URI soap.udp.

Para simplificar, WSDAPI reconoce las direcciones IPv6 entre corchetes en el esquema soap.udp. Por ejemplo, `soap.udp://[2001:abcd:0001:0002:0003:0004:0005:0032]:3702` WSDAPI reconoce la dirección. Esto es similar a cómo se controlan las direcciones IPv6 en HTTP.

## <a name="hello-and-xaddrs"></a>Hello y XAddrs

El objeto de hospedaje DPWS de WSDAPI nunca enviará un WS-Discovery [Hello](hello-message.md) con [XAddrs](xaddr-validation-rules.md) en el cuerpo del mensaje. Un cliente siempre enviará un mensaje [Resolver](resolve-message.md) después de recibir un mensaje Hello si el cliente necesita obtener los XAddrs.

Este enfoque tiene dos ventajas. En primer lugar, un dispositivo basado en WSDAPI nunca expondrá XAddrs que divulguen las direcciones IP de las redes privadas. En segundo lugar, un dispositivo basado en WSDAPI solo expone XAddrs que son accesibles para el cliente, lo que significa que las direcciones IPv6 nunca se envían a un cliente IPv4.

Cuando se [recibe un](probe-message.md) mensaje de sondeo o resolución, solo se envía un solo XAddr en respuesta. El XAddr enviado corresponde a la dirección local en la que se recibió la solicitud. Si la solicitud se recibió entre subredes a través de IPv6, WSDAPI proporcionará una dirección IPv6 global en la respuesta.

## <a name="preferred-addresses"></a>Direcciones preferidas

Un dispositivo puede proporcionar varios XAddrs en un [mensaje Hello](hello-message.md), [ProbeMatch](probematches-message.md)o [ResolveMatch.](resolvematches-message.md) Un servicio también puede estar disponible en varios puntos de conexión con diferentes direcciones de transporte. En estos casos, WSDAPI intentará comunicarse con el dispositivo en la primera dirección utilizable que encuentre. Una dirección es utilizable si es de un protocolo disponible, como IPv4 en un equipo donde está instalado IPv4 o IPv6 en una máquina donde está instalado IPv6. Además, si la dirección provenía de un dispositivo o servicio que no está en la subred local, solo se puede usar si es IPv4, sitio IPv6 local o vínculo IPv6 local.

## <a name="wsdl-in-metadata-exchange"></a>WSDL en el intercambio de metadatos

Los dispositivos y los servicios basados en WSDAPI no proporcionan su WSDL en el intercambio de metadatos, a menos que la aplicación la haya ampliado para proporcionar esta información. De forma predeterminada, el aprovisionamiento de WSDL no forma parte del modelo de programación.

## <a name="app_max_delay"></a>RETRASO \_ MÁXIMO DE LA \_ APLICACIÓN

DPWS define APP MAX DELAY, el intervalo aleatorio que se retrasará entre recibir un sondeo y enviar \_ \_ un [ProbeMatch,](probematches-message.md)como 5000 milisegundos. [](probe-message.md) Windows El firewall requiere que el modelo de solicitud de multidifusión o respuesta de unidifusión para UDP solo funcione dentro de la ventana de firewall de 4 segundos. Como resultado, WSDAPI transmitirá respuestas en 2500 ms o menos, en lugar de la ventana de 5000 ms descrita por APP \_ MAX \_ DELAY.

## <a name="iana-port-reservations"></a>Reservas de puertos de IANA

WSDAPI usa el puerto TCP 5357 para el tráfico HTTP y el puerto TCP 5358 para el tráfico HTTPS de forma predeterminada. Estos puertos están reservados para procesos con privilegios inferiores a través de una reserva de direcciones URL en HTTP.sys y también se reservan con IANA.

## <a name="udp-port-sharing"></a>Uso compartido de puertos UDP

WSDAPI usa el uso compartido de puertos. Es posible que todas las aplicaciones basadas en WSDAPI no controlen correctamente los mensajes de unidifusión enviados al puerto 3702. Si una aplicación se enlaza exclusivamente al puerto 3702, puede impedir que las aplicaciones basadas en WSDAPI usen ese puerto correctamente.

## <a name="ws-discovery-v11-cd1-proxy"></a>WS-Discovery proxy cd1.1 v1

WSDAPI buscará y se comunicará con un proxy de detección que implemente el protocolo de modo administrado WS-Discovery v1.1 CD1. WS-Discovery v1.1 CD1 es la primera revisión de WS-Discovery que incluye una descripción explícita de un protocolo HTTP para la comunicación entre un proxy y un cliente o dispositivo.

Para limitar el número de versiones simultáneas usadas en las solicitudes de multidifusión, WSDAPI envía una solicitud de sondeo de WS-Discovery en el espacio de nombres 2005/04, pero busca el tipo discoveryProxy de WS-Discovery v1.1 CD1. Si un proxy responde, WSDAPI enviará una solicitud Http Probe o Resolve al punto de conexión de proxy especificado, tal como se define en WS-Discovery v1.1 CD1.

 

 



