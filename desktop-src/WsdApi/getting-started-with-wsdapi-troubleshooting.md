---
description: Hay dos maneras de determinar el procedimiento de diagnóstico que se debe usar.
ms.assetid: d6877063-6cf9-48dc-8208-0f3fc85b6d6b
title: Tareas iniciales solución de problemas de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 413146288e6c7fc6e513f994fbe24d6ee9940897f22bcd5a715ae41f77f83c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738621"
---
# <a name="getting-started-with-wsdapi-troubleshooting"></a>Tareas iniciales solución de problemas de WSDAPI

Esta guía de solución de problemas contiene un conjunto de [procedimientos de diagnóstico](wsdapi-diagnostic-procedures.md) que se pueden usar para ayudar a identificar la causa de los problemas de la aplicación. Una vez que la causa del problema se ha identificado correctamente, se pueden aplicar las soluciones sugeridas en el procedimiento de diagnóstico para resolver el problema.

Hay dos maneras de determinar el procedimiento de diagnóstico que se debe usar. Una manera consiste en ir a la página de solución de problemas del tipo de cliente para ver una lista paso a paso de los procedimientos de diagnóstico que se van a usar para solucionar problemas del cliente. La otra manera es ir a la referencia rápida de solución de problemas siguiente para ver tablas de resumen que muestran problemas comunes con las aplicaciones de WSDAPI y los procedimientos que se usan para diagnosticar los problemas.

## <a name="troubleshooting-by-type-of-client"></a>Solución de problemas por tipo de cliente

En los temas siguientes se muestran los procedimientos de diagnóstico pertinentes por tipo de cliente. En estos temas también se muestran los patrones de mensaje asociados al tipo de cliente.

-   [Solución de problemas de aplicaciones WSDAPI mediante la detección dirigida](troubleshooting-applications-using-directed-discovery.md)
-   [Solución de problemas de clientes de detección de funciones](troubleshooting-function-discovery-clients.md)
-   [Solución de problemas Equipos a mi alrededor/meetings near me](troubleshooting-people-near-me-meetings-near-me.md)
-   [Solución de problemas del Asistente para agregar impresoras](troubleshooting-the-add-printer-wizard.md)
-   [Solución de problemas de Explorador de red](troubleshooting-the-network-explorer.md)
-   [Solución de problemas del Asistente para proyectores](troubleshooting-the-projector-wizard.md)
-   [Solución de problemas de otras aplicaciones WSDAPI](troubleshooting-wsdapi-applications.md)

## <a name="troubleshooting-quick-reference"></a>Referencia rápida de solución de problemas

En las tablas siguientes se muestran algunos problemas que pueden impedir que los clientes y hosts de WSDAPI se vean entre sí en la red y que intercedan los metadatos del dispositivo. Las tablas también muestran los procedimientos de diagnóstico que se deben ejecutar y los criterios que se deben usar para evaluar si la aplicación sufre un problema determinado.

### <a name="network-environment-problems"></a>Problemas del entorno de red



| Problema                                                                                                                                                                                              | Procedimiento de diagnóstico                                                                                                                                                                                                                             | Identificación del problema                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El firewall bloquea el tráfico de detección de redes.                                                                                                                                                       | [Inspección de adaptadores y firewalls Configuración](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | La habilitación de la excepción de detección de redes en el firewall soluciona el problema.                                                                                                                      |
| Las excepciones de firewall específicas de la aplicación bloquean los mensajes.                                                                                                                               | [Inspección de adaptadores y firewalls Configuración](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | Deshabilitar el firewall resuelve el problema. WF.msc muestra reglas de firewall específicas de la aplicación.                                                                                                      |
| El dispositivo no responde a las solicitudes UDP mediante el envío de un mensaje [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) a tiempo (menos de 4 segundos). | [Inspección de adaptadores y firewalls Configuración](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | Deshabilitar el firewall resuelve el problema y un host genérico que responde en menos de 4 segundos funciona correctamente.                                                                            |
| El contexto de seguridad de la aplicación es incorrecto (es decir, el cliente y el host no tienen los permisos adecuados en la red).                                                                 | [Usar un host y un cliente genéricos para la](using-a-generic-host-and-client-for-udp-ws-discovery.md) detección de WS udp o usar un host y un cliente genéricos para la detección de [metadatos HTTP Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) | La dirección del dispositivo no se muestra en la salida del cliente de depuración de WSD. La ejecución de la aplicación como administrador soluciona el problema.                                                                          |
| Una directiva IPSec está bloqueando los mensajes.                                                                                                                                                                | [Usar un host y un cliente genéricos para la](using-a-generic-host-and-client-for-udp-ws-discovery.md) detección de WS udp o usar un host y un cliente genéricos para la detección de [metadatos HTTP Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) | La dirección del dispositivo no se muestra en la salida del cliente de depuración de WSD. El problema no se resuelve deshabilitando el firewall. El problema no se puede reproducir en una máquina que no esté sujeta a ninguna directiva IPSec. |



 

### <a name="discovery-traffic-problems"></a>Problemas de tráfico de detección



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Problema</th>
<th>Procedimiento de diagnóstico</th>
<th>Identificación del problema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="hello-message.md">Los</a>mensajes Hello , <a href="probe-message.md">Probe</a>o <a href="resolve-message.md">Resolve</a> no se transmiten en la red porque la aplicación no enumera correctamente las interfaces de red de multidifusión.</td>
<td><a href="using-wsddebug-client-to-verify-multicast-traffic.md">Uso del cliente de depuración de WSD para comprobar el tráfico de multidifusión</a></td>
<td>Los mensajes Hello, Probe o Resolve no aparecen en la salida del cliente de depuración de WSD. Los paquetes no aparecen en la red. Los paquetes no se generan para la interfaz de bucleback ni para otras interfaces.</td>
</tr>
<tr class="even">
<td><a href="probe-message.md">La</a> multidifusión UDP no envía mensajes de sondeo al puerto 3702 (para aplicaciones que no usan la detección dirigida).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspección de seguimientos de red para la detección de WS de UDP</a></td>
<td>La inspección del mensaje muestra que se envió al puerto incorrecto.</td>
</tr>
<tr class="odd">
<td>El <a href="probe-message.md">mensaje</a> Probe no contiene un <strong>elemento Types</strong> o el elemento <strong>Types</strong> está vacío.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspección de seguimientos de red para la detección de WS udp</a> o inspección de seguimientos de <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">red para aplicaciones mediante la detección dirigida</a></td>
<td>La inspección del mensaje muestra que el <strong>elemento Types</strong> no está presente ni está vacío.</td>
</tr>
<tr class="even">
<td>El <strong>elemento Types</strong> de un mensaje <a href="probe-message.md">probe</a> no contiene los tipos a los que responderá un host.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspección de seguimientos de red para la detección de WS udp</a> o inspección de seguimientos de <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">red para aplicaciones mediante la detección dirigida</a></td>
<td>La inspección del mensaje muestra que el <strong>elemento Types</strong> contiene un valor incorrecto o incorrecto.</td>
</tr>
<tr class="odd">
<td>No se envió un mensaje <a href="probematches-message.md">ProbeMatches</a> al puerto UDP desde el <a href="probe-message.md">que</a> se envió el sondeo.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspección de seguimientos de red para la detección de WS udp</a> o inspección de seguimientos de <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">red para aplicaciones mediante la detección dirigida</a></td>
<td>La inspección de la salida muestra que no se envió ningún mensaje <a href="probematches-message.md">ProbeMatches</a>) o que el mensaje se envió al puerto incorrecto.
<blockquote>
[!Note]<br />
En el caso de las aplicaciones que usan la detección dirigida, <a href="probematches-message.md">ProbeMatches</a> debe enviarse a través de HTTP o HTTPS en respuesta al <a href="probe-message.md">mensaje probe.</a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>El <a href="probematches-message.md">mensaje ProbeMatches</a> no contiene un <strong>elemento RelatesTo</strong> o el <strong>elemento RelatesTo</strong> está vacío.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspección de seguimientos de red para la detección de WS udp</a> o inspección de seguimientos de <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">red para aplicaciones mediante la detección dirigida</a></td>
<td>La inspección del mensaje muestra que <strong>el elemento RelatesTo</strong> no está presente ni está vacío.</td>
</tr>
<tr class="odd">
<td>El valor del <strong>elemento RelatesTo</strong> de un mensaje <a href="probematches-message.md">ProbeMatches</a> no coincide con el valor del <strong>elemento MessageId</strong> del mensaje <a href="probe-message.md">Probe</a> correspondiente.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspección de seguimientos de red para la detección de WS udp</a> o inspección de seguimientos de <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">red para aplicaciones mediante la detección dirigida</a></td>
<td>La inspección del mensaje muestra que <strong>el elemento RelatesTo</strong> contiene un valor incorrecto o incorrecto.</td>
</tr>
<tr class="even">
<td>El <strong>elemento XAddrs</strong> incluido en un <a href="probematches-message.md">mensaje ProbeMatches</a> no se ajusta a las <a href="xaddr-validation-rules.md">reglas de validación de XAddr</a>.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspección de seguimientos de red para la detección de WS udp</a> o inspección de seguimientos de <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">red para aplicaciones mediante la detección dirigida</a></td>
<td>La inspección del mensaje muestra que <strong>los XAddrs no</strong> son válidos.</td>
</tr>
<tr class="odd">
<td><a href="resolve-message.md">La</a> multidifusión UDP no envía mensajes de resolución al puerto 3702 (para aplicaciones que no usan la detección dirigida).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspección de seguimientos de red para la detección de WS udp</a> o inspección de seguimientos de <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">red para aplicaciones mediante la detección dirigida</a></td>
<td>La inspección de la salida muestra que el <a href="resolve-message.md">mensaje Resolver</a> se envió al puerto incorrecto.</td>
</tr>
<tr class="even">
<td>No se envió un mensaje <a href="resolvematches-message.md">ResolveMatches</a> al puerto UDP desde el que se envió un <a href="resolve-message.md">mensaje</a> Resolver.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspección de seguimientos de red para la detección de WS udp</a> o inspección de seguimientos de <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">red para aplicaciones mediante la detección dirigida</a></td>
<td>La inspección de la salida muestra que no se envió ningún mensaje <a href="resolvematches-message.md">ResolveMatches</a> o que el mensaje se envió al puerto incorrecto.</td>
</tr>
</tbody>
</table>



 

### <a name="metadata-exchange-problems"></a>Problemas de intercambio de metadatos



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Problema</th>
<th>Procedimiento de diagnóstico</th>
<th>Identificación del problema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>La dirección de transporte anunciada por el host es incorrecta.</td>
<td><a href="using-a-generic-host-and-client-for-http-metadata-exchange.md">Uso de un host y un cliente genéricos para metadatos HTTP Exchange</a></td>
<td>La inspección de XAddrs en la salida del cliente de depuración de WSD muestra que la dirección de transporte es incorrecta o tiene un formato incorrecto.</td>
</tr>
<tr class="even">
<td>No se pudo establecer una conexión TCP para el intercambio de metadatos.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspección de seguimientos de red para los metadatos HTTP Exchange</a></td>
<td>La salida del analizador de paquetes no muestra el siguiente intercambio de paquetes:
<ul>
<li>Un paquete TCP SYN enviado desde el cliente</li>
<li>Un paquete TCP SYN/ACK enviado desde el host</li>
<li>Un paquete TCP ACK enviado desde el cliente</li>
</ul></td>
</tr>
<tr class="odd">
<td>El cliente no envió una solicitud HTTP GET válida.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspección de seguimientos de red para los metadatos HTTP Exchange</a></td>
<td>No hay ninguna solicitud HTTP GET en la salida del analizador de paquetes o la solicitud tiene un formato mal.</td>
</tr>
<tr class="even">
<td>El cliente no envió un mensaje WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">get</a> válido.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspección de seguimientos de red para los metadatos HTTP Exchange</a></td>
<td>No hay ninguna WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Obtener mensaje</a> en la salida del analizador de paquetes o el mensaje tiene un formato mal.</td>
</tr>
<tr class="odd">
<td>El host no escucha en la ruta de acceso URL especificada en la solicitud HTTP GET.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspección de seguimientos de red para los metadatos HTTP Exchange</a></td>
<td>No hay ninguna respuesta HTTP en la salida del analizador de paquetes.</td>
</tr>
<tr class="even">
<td>El WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">get</a> no contiene un <strong>elemento To</strong> o el elemento <strong>To</strong> está vacío.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspección de seguimientos de red para los metadatos HTTP Exchange</a></td>
<td>La inspección del mensaje muestra que el <strong>elemento To</strong> no está presente ni está vacío.</td>
</tr>
<tr class="odd">
<td>El valor del elemento <strong>To</strong> de un WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">get</a> no coincide con una de las direcciones de punto de conexión del host.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspección de seguimientos de red para los metadatos HTTP Exchange</a></td>
<td>La inspección del mensaje muestra que el valor del elemento <strong>To</strong> no coincide con una de las direcciones de punto de conexión anunciadas en el mensaje <a href="probematches-message.md">ProbeMatches</a> o <a href="resolvematches-message.md">ResolveMatches del</a> host.</td>
</tr>
<tr class="even">
<td>El host no envió un encabezado de respuesta HTTP válido.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspección de seguimientos de red para los metadatos HTTP Exchange</a></td>
<td>No hay ninguna respuesta HTTP en la salida del analizador de paquetes o la solicitud tiene un formato mal.</td>
</tr>
<tr class="odd">
<td>El encabezado de respuesta HTTP enviado por el host indica que la solicitud no se puede completar.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspección de seguimientos de red para los metadatos HTTP Exchange</a></td>
<td>El encabezado de respuesta tiene un código de estado distinto de HTTP/1.1 200.</td>
</tr>
<tr class="even">
<td>El host no envió un mensaje <a href="getresponse--metadata-exchange--message.md">GetResponse</a> válido.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspección de seguimientos de red para los metadatos HTTP Exchange</a></td>
<td>No hay ningún <a href="getresponse--metadata-exchange--message.md">mensaje GetResponse en</a> la salida del analizador de paquetes o el mensaje tiene un formato mal.</td>
</tr>
<tr class="odd">
<td>El <a href="getresponse--metadata-exchange--message.md">mensaje GetResponse</a> no contiene un <strong>elemento RelatesTo</strong> o el <strong>elemento RelatesTo</strong> está vacío.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspección de seguimientos de red para los metadatos HTTP Exchange</a></td>
<td>La inspección del mensaje muestra que <strong>el elemento RelatesTo</strong> no está presente ni está vacío.</td>
</tr>
<tr class="even">
<td>El valor del <strong>elemento RelatesTo</strong> de un mensaje <a href="getresponse--metadata-exchange--message.md">GetResponse</a> no coincide con el valor del elemento <strong>MessageId</strong> del <a href="get--metadata-exchange--http-request-and-message.md">mensaje Get</a> correspondiente.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspección de seguimientos de red para los metadatos HTTP Exchange</a></td>
<td>La inspección del mensaje muestra que <strong>el elemento RelatesTo</strong> contiene un valor incorrecto o incorrecto.</td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de solución de problemas de WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>
