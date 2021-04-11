---
description: Hay dos maneras de determinar el procedimiento de diagnóstico que se va a usar.
ms.assetid: d6877063-6cf9-48dc-8208-0f3fc85b6d6b
title: Introducción con la solución de problemas de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12396ea656423772d35dbd4ca237c7c536dcdaf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276237"
---
# <a name="getting-started-with-wsdapi-troubleshooting"></a>Introducción con la solución de problemas de WSDAPI

Esta guía de solución de problemas contiene un conjunto de [procedimientos de diagnóstico](wsdapi-diagnostic-procedures.md) que pueden usarse para ayudar a identificar la causa de los problemas de la aplicación. Una vez que la causa del problema se ha identificado correctamente, se pueden aplicar las soluciones sugeridas en el procedimiento de diagnóstico para resolver el problema.

Hay dos maneras de determinar el procedimiento de diagnóstico que se va a usar. Una manera consiste en ir a la página de solución de problemas del tipo de cliente para ver una lista paso a paso de los procedimientos de diagnóstico que se van a usar para solucionar problemas del cliente. La otra forma es ir a la siguiente referencia rápida de solución de problemas para ver las tablas de resumen que muestran problemas comunes con las aplicaciones de WSDAPI y los procedimientos que se usan para diagnosticar los problemas.

## <a name="troubleshooting-by-type-of-client"></a>Solución de problemas por tipo de cliente

En los temas siguientes se muestran los procedimientos de diagnóstico correspondientes por tipo de cliente. En estos temas también se muestran los patrones de mensajes asociados con el tipo de cliente.

-   [Solución de problemas de aplicaciones WSDAPI mediante la detección dirigida](troubleshooting-applications-using-directed-discovery.md)
-   [Solución de problemas de clientes de detección de funciones](troubleshooting-function-discovery-clients.md)
-   [Solución de problemas de equipos a mi alrededor/reuniones cerca de mí](troubleshooting-people-near-me-meetings-near-me.md)
-   [Solucionar problemas del Asistente para agregar impresoras](troubleshooting-the-add-printer-wizard.md)
-   [Solución de problemas del explorador de red](troubleshooting-the-network-explorer.md)
-   [Solución de problemas del asistente de proyector](troubleshooting-the-projector-wizard.md)
-   [Solucionar problemas de otras aplicaciones de WSDAPI](troubleshooting-wsdapi-applications.md)

## <a name="troubleshooting-quick-reference"></a>Referencia rápida para la solución de problemas

En las tablas siguientes se muestran algunos problemas que pueden impedir que los clientes y los hosts de WSDAPI se vean entre sí en la red y que se intercambien los metadatos del dispositivo. Las tablas también muestran los procedimientos de diagnóstico que se deben ejecutar y los criterios que se van a usar para evaluar si la aplicación se ve afectada por un problema determinado.

### <a name="network-environment-problems"></a>Problemas del entorno de red



| Problema                                                                                                                                                                                              | Procedimiento de diagnóstico                                                                                                                                                                                                                             | Identificación del problema                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El Firewall bloquea el tráfico de detección de redes.                                                                                                                                                       | [Inspeccionando la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | Al habilitar la excepción de detección de redes en el Firewall se soluciona el problema.                                                                                                                      |
| Las excepciones de Firewall específicas de la aplicación están bloqueando los mensajes.                                                                                                                               | [Inspeccionando la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | Al deshabilitar el Firewall se soluciona el problema. WF. msc muestra las reglas de Firewall específicas de la aplicación.                                                                                                      |
| El dispositivo no responde a las solicitudes UDP mediante el envío de un mensaje [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) de manera puntual (menos de 4 segundos). | [Inspeccionando la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | Al deshabilitar el Firewall se soluciona el problema y un host genérico que responde en menos de 4 segundos funciona correctamente.                                                                            |
| El contexto de seguridad de la aplicación es incorrecto (es decir, el cliente y el host no tienen los permisos adecuados en la red).                                                                 | [Usar un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md) o [el uso de un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md) | La dirección del dispositivo no se muestra en la salida del cliente de depuración WSD. La ejecución de la aplicación como administrador resuelve el problema.                                                                          |
| Una directiva IPSec está bloqueando los mensajes.                                                                                                                                                                | [Usar un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md) o [el uso de un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md) | La dirección del dispositivo no se muestra en la salida del cliente de depuración WSD. El problema no se soluciona deshabilitando el firewall. El problema no se puede reproducir en una máquina que no esté sujeta a ninguna directiva IPSec. |



 

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
<td>Los mensajes <a href="hello-message.md">Hello</a>, <a href="probe-message.md">Probe</a>o <a href="resolve-message.md">Resolve</a> no se transmiten en la red porque la aplicación no enumera correctamente las interfaces de red de multidifusión.</td>
<td><a href="using-wsddebug-client-to-verify-multicast-traffic.md">Usar el cliente de depuración WSD para comprobar el tráfico de multidifusión</a></td>
<td>Los mensajes Hello, probe o Resolve no aparecen en la salida del cliente de depuración WSD. Los paquetes no aparecen en la red. Los paquetes no se generan para la interfaz de bucle invertido ni para otras interfaces.</td>
</tr>
<tr class="even">
<td>Los mensajes de <a href="probe-message.md">sondeo</a> no se envían mediante multidifusión de UDP al puerto 3702 (para aplicaciones que no usan la detección dirigida).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspeccionando los seguimientos de red para WS-Discovery de UDP</a></td>
<td>La inspección del mensaje muestra que se ha enviado al puerto equivocado.</td>
</tr>
<tr class="odd">
<td>El mensaje de <a href="probe-message.md">sondeo</a> no contiene un elemento <strong>Types</strong> o el elemento <strong>Types</strong> está vacío.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspeccionar los seguimientos de red para UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspeccionar los seguimientos de red para las aplicaciones que usan la detección dirigida</a></td>
<td>La inspección del mensaje muestra que el elemento <strong>Types</strong> no está presente o está vacío.</td>
</tr>
<tr class="even">
<td>El elemento <strong>Types</strong> de un mensaje de <a href="probe-message.md">sondeo</a> no contiene los tipos a los que responderá un host.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspeccionar los seguimientos de red para UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspeccionar los seguimientos de red para las aplicaciones que usan la detección dirigida</a></td>
<td>La inspección del mensaje muestra que el elemento <strong>tipos</strong> contiene un valor mal formado o incorrecto.</td>
</tr>
<tr class="odd">
<td>No se envió un mensaje de <a href="probematches-message.md">ProbeMatches</a> de unidifusión al puerto UDP desde el que se envió el <a href="probe-message.md">sondeo</a> .</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspeccionar los seguimientos de red para UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspeccionar los seguimientos de red para las aplicaciones que usan la detección dirigida</a></td>
<td>La inspección de la salida muestra que no se envió ningún mensaje <a href="probematches-message.md">ProbeMatches</a>) o que el mensaje se envió al puerto equivocado.
<blockquote>
[!Note]<br />
En el caso de las aplicaciones que usan la detección dirigida, el <a href="probematches-message.md">ProbeMatches</a> se debe enviar a través de http o https en respuesta al mensaje de <a href="probe-message.md">sondeo</a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>El mensaje de <a href="probematches-message.md">ProbeMatches</a> no contiene un elemento de <strong>reversión</strong> o el elemento de la <strong>reversión</strong> está vacío.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspeccionar los seguimientos de red para UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspeccionar los seguimientos de red para las aplicaciones que usan la detección dirigida</a></td>
<td>La inspección del mensaje muestra que el <strong>elemento</strong> representer no está presente o está vacío.</td>
</tr>
<tr class="odd">
<td>El valor del elemento <strong>latesto</strong> en un mensaje <a href="probematches-message.md">ProbeMatches</a> no coincide con el valor del elemento <strong>MessageId</strong> del mensaje de <a href="probe-message.md">sondeo</a> correspondiente.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspeccionar los seguimientos de red para UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspeccionar los seguimientos de red para las aplicaciones que usan la detección dirigida</a></td>
<td>Al inspeccionar el mensaje, se muestra que el elemento <strong>Retesto</strong> contiene un valor mal formado o incorrecto.</td>
</tr>
<tr class="even">
<td>El elemento <strong>XAddrs</strong> incluido en un mensaje de <a href="probematches-message.md">ProbeMatches</a> no se ajusta a las reglas de <a href="xaddr-validation-rules.md">validación de XAddr</a>.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspeccionar los seguimientos de red para UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspeccionar los seguimientos de red para las aplicaciones que usan la detección dirigida</a></td>
<td>La inspección del mensaje muestra que los <strong>XAddrs</strong> no son válidos.</td>
</tr>
<tr class="odd">
<td>Los mensajes de <a href="resolve-message.md">resolución</a> no se envían mediante multidifusión de UDP al puerto 3702 (para aplicaciones que no usan la detección dirigida).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspeccionar los seguimientos de red para UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspeccionar los seguimientos de red para las aplicaciones que usan la detección dirigida</a></td>
<td>La inspección de la salida muestra que el mensaje de <a href="resolve-message.md">resolución</a> se envió al puerto equivocado.</td>
</tr>
<tr class="even">
<td>No se envió un mensaje de <a href="resolvematches-message.md">ResolveMatches</a> de unidifusión al puerto UDP desde el que se envió un mensaje de <a href="resolve-message.md">resolución</a> .</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspeccionar los seguimientos de red para UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">inspeccionar los seguimientos de red para las aplicaciones que usan la detección dirigida</a></td>
<td>La inspección de la salida muestra que no se envió ningún mensaje <a href="resolvematches-message.md">ResolveMatches</a> o que el mensaje se envió al puerto equivocado.</td>
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
<td><a href="using-a-generic-host-and-client-for-http-metadata-exchange.md">Usar un host y un cliente genéricos para el intercambio de metadatos HTTP</a></td>
<td>La inspección de XAddrs en la salida del cliente de depuración WSD muestra que la dirección de transporte es incorrecta o tiene un formato incorrecto.</td>
</tr>
<tr class="even">
<td>No se pudo establecer una conexión TCP para el intercambio de metadatos.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspeccionando seguimientos de red para el intercambio de metadatos HTTP</a></td>
<td>La salida del analizador de paquetes no muestra el siguiente intercambio de paquetes:
<ul>
<li>Un paquete SYN de TCP enviado desde el cliente</li>
<li>Un paquete TCP SYN/ACK enviado desde el host</li>
<li>Un paquete ACK de TCP enviado desde el cliente</li>
</ul></td>
</tr>
<tr class="odd">
<td>El cliente no envió una solicitud GET de HTTP válida.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspeccionando seguimientos de red para el intercambio de metadatos HTTP</a></td>
<td>No hay ninguna solicitud HTTP GET en la salida del analizador de paquetes o la solicitud tiene un formato incorrecto.</td>
</tr>
<tr class="even">
<td>El cliente no envió un mensaje de <a href="get--metadata-exchange--http-request-and-message.md">obtención</a> de WS-Transfer válido.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspeccionando seguimientos de red para el intercambio de metadatos HTTP</a></td>
<td>No hay WS-Transfer mensaje <a href="get--metadata-exchange--http-request-and-message.md">Get</a> en la salida del analizador de paquetes o el mensaje tiene un formato incorrecto.</td>
</tr>
<tr class="odd">
<td>El host no está escuchando en la ruta de acceso de la dirección URL especificada en la solicitud HTTP GET.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspeccionando seguimientos de red para el intercambio de metadatos HTTP</a></td>
<td>No hay ninguna respuesta HTTP en la salida del analizador de paquetes.</td>
</tr>
<tr class="even">
<td>El WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> Message no contiene un elemento <strong>to</strong> o el elemento <strong>to</strong> está vacío.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspeccionando seguimientos de red para el intercambio de metadatos HTTP</a></td>
<td>La inspección del mensaje muestra que el elemento <strong>to</strong> no está presente o está vacío.</td>
</tr>
<tr class="odd">
<td>El valor del elemento <strong>to</strong> de una WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> Message no coincide con una de las direcciones de punto de conexión del host.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspeccionando seguimientos de red para el intercambio de metadatos HTTP</a></td>
<td>La inspección del mensaje muestra que el valor del elemento <strong>to</strong> no coincide con una de las direcciones de punto de conexión anunciadas en el mensaje <a href="probematches-message.md">ProbeMatches</a> o <a href="resolvematches-message.md">ResolveMatches</a> del host.</td>
</tr>
<tr class="even">
<td>El host no envió un encabezado de respuesta HTTP válido.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspeccionando seguimientos de red para el intercambio de metadatos HTTP</a></td>
<td>No hay ninguna respuesta HTTP en la salida del analizador de paquetes o la solicitud tiene un formato incorrecto.</td>
</tr>
<tr class="odd">
<td>El encabezado de respuesta HTTP enviado por el host indica que no se puede completar la solicitud.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspeccionando seguimientos de red para el intercambio de metadatos HTTP</a></td>
<td>El encabezado de respuesta tiene un código de Estado distinto de HTTP/1.1 200.</td>
</tr>
<tr class="even">
<td>El host no envió un mensaje de <a href="getresponse--metadata-exchange--message.md">GetResponse</a> válido.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspeccionando seguimientos de red para el intercambio de metadatos HTTP</a></td>
<td>No hay ningún mensaje <a href="getresponse--metadata-exchange--message.md">GetResponse</a> en la salida del analizador de paquetes o el mensaje tiene un formato incorrecto.</td>
</tr>
<tr class="odd">
<td>El mensaje <a href="getresponse--metadata-exchange--message.md">GetResponse</a> no contiene un elemento <strong>retesto</strong> o el elemento <strong>retesto</strong> está vacío.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspeccionando seguimientos de red para el intercambio de metadatos HTTP</a></td>
<td>La inspección del mensaje muestra que el <strong>elemento</strong> representer no está presente o está vacío.</td>
</tr>
<tr class="even">
<td>El valor del elemento <strong>latesto</strong> en un mensaje <a href="getresponse--metadata-exchange--message.md">GetResponse</a> no coincide con el valor del elemento <strong>MessageId</strong> del mensaje <a href="get--metadata-exchange--http-request-and-message.md">Get</a> correspondiente.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspeccionando seguimientos de red para el intercambio de metadatos HTTP</a></td>
<td>Al inspeccionar el mensaje, se muestra que el elemento <strong>Retesto</strong> contiene un valor mal formado o incorrecto.</td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de solución de problemas de WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>
