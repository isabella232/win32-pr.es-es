---
description: Enumera los procedimientos de diagnóstico que se deben usar al solucionar problemas de clientes de detección de funciones.
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: Solución de problemas de clientes de detección de funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811401"
---
# <a name="troubleshooting-function-discovery-clients"></a>Solución de problemas de clientes de detección de funciones

Clientes de detección de funciones:

-   Usar siempre WS-Discovery UDP para la detección de dispositivos
-   Iniciar siempre conexiones HTTP o HTTPS para el intercambio de metadatos
-   A veces, usar el descubrimiento dirigido
-   A veces, se usa un canal seguro (HTTPS) para el intercambio de metadatos

En la siguiente lista se muestra la secuencia típica de mensajes enviados y recibidos por los clientes de detección de funciones. No todos los mensajes son obligatorios.

1.  El cliente envía un mensaje de [sondeo](probe-message.md) para detectar dispositivos y servicios. Si el cliente usa la detección dirigida, este mensaje se envía a través de HTTP o HTTPS. de lo contrario, el mensaje se envía mediante multidifusión de UDP al puerto 3702.
2.  El cliente recibe mensajes [ProbeMatches](probematches-message.md) de dispositivos o servicios coincidentes. Los mensajes de detección dirigidos se envían a través de HTTP o HTTPS. de lo contrario, los mensajes se envían por unidifusión UDP y se originan desde el puerto 3702.
3.  Si no se incluyó ningún XAddrs en el mensaje ProbeMatches, el cliente enviará un mensaje de [resolución](resolve-message.md) mediante multidifusión UDP al puerto 3702.
4.  Si se ha enviado un mensaje de [resolución](resolve-message.md) , el cliente recibe un mensaje [ResolveMatches](resolvematches-message.md) de los servicios coincidentes. Este mensaje lo envía la unidifusión UDP desde el puerto 3702 al puerto en el que se originó el mensaje de resolución.
5.  El cliente envía un mensaje [Get](get--metadata-exchange--http-request-and-message.md) para solicitar los metadatos del dispositivo o servicio. HTTP o HTTPS envía este mensaje.
6.  El cliente recibe un mensaje [GetResponse](getresponse--metadata-exchange--message.md) con los metadatos del dispositivo o servicio. HTTP o HTTPS envía este mensaje.

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con un cliente de detección de funciones.

**Para solucionar problemas de un cliente de detección de funciones**

1.  Si se usa la detección dirigida, [solucione los problemas de detección dirigida](troubleshooting-applications-using-directed-discovery.md).
2.  [Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).
3.  [Use un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).
4.  [Use el cliente de depuración WSD para comprobar el tráfico de multidifusión](using-wsddebug-client-to-verify-multicast-traffic.md).
5.  [Inspeccione los seguimientos de red para WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).
6.  [Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
7.  [Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).
8.  [Inspeccione los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md).

Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de [habilitación del seguimiento de WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



