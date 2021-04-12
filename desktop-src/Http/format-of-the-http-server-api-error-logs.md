---
title: Formato de los registros de errores de la API del servidor HTTP
description: En general, los archivos de registro de errores de la API del servidor HTTP tienen el mismo formato que los registros de errores de W3C, salvo que los archivos de registro de errores de la API del servidor HTTP no contienen encabezados de columna.
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- API de servidor HTTP, formato de registro de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2eb914251a809178adef28c8a61b1a174c6e86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268472"
---
# <a name="format-of-the-http-server-api-error-logs"></a>Formato de los registros de errores de la API del servidor HTTP

En general, los archivos de registro de errores de la API del servidor HTTP tienen el mismo formato que los registros de errores de W3C, salvo que los archivos de registro de errores de la API del servidor HTTP no contienen encabezados de columna. Cada línea de un registro de errores de la API del servidor HTTP registra un error con campos en un orden específico. Cada campo está separado del campo anterior por un carácter de espacio único (0x0020). Dentro de cada campo, los caracteres de espacio, las tabulaciones y los caracteres de control no imprimibles se reemplazan por signos más (0x002B).

En la tabla siguiente se identifican los campos y el orden de los campos en un registro de errores.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Date"></span><span id="date"></span><span id="DATE"></span>Posteriormente<br/></td>
<td>El campo de fecha sigue el formato del W3C y se basa en la hora universal coordinada (UTC). El campo de fecha tiene siempre 10 caracteres en formato &quot; AAAA-MM-DD &quot; . Por ejemplo, el 1 de mayo de 2003 se expresa como &quot; 2003-05-01 &quot; .<br/></td>
</tr>
<tr class="even">
<td><span id="Time"></span><span id="time"></span><span id="TIME"></span>Tiempo<br/></td>
<td>El campo de hora sigue el formato del W3C y se basa en la hora UTC. El campo de hora siempre tiene 8 caracteres en formato &quot; mm: HH: SS &quot; . Por ejemplo, 5:30 PM (UTC) se expresa como &quot; 17:30:00 &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Dirección IP del cliente<br/></td>
<td>Dirección IP del cliente afectado que puede ser una dirección IPv4 o una dirección IPv6. Si la dirección IP del cliente es una dirección IPv6, el campo ScopeId también se incluye en la dirección.<br/></td>
</tr>
<tr class="even">
<td><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Puerto de cliente<br/></td>
<td>El número de puerto del cliente afectado.<br/></td>
</tr>
<tr class="odd">
<td><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Dirección IP del servidor<br/></td>
<td>Dirección IP del servidor afectado que puede ser una dirección IPv4 o una dirección IPv6. Si la dirección IP del servidor es una dirección IPv6, el campo ScopeId también se incluye en la dirección.<br/></td>
</tr>
<tr class="even">
<td><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Puerto de servidor<br/></td>
<td>El número de puerto del servidor afectado.<br/></td>
</tr>
<tr class="odd">
<td><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Versión de protocolo<br/></td>
<td>La versión del protocolo que se está usando. <br/>
<ul>
<li>Si la conexión no se ha analizado lo suficiente para determinar la versión del Protocolo, se usa un guión (0x002D) como marcador de posición para el campo vacío.</li>
<li>Si el número de versión principal o secundaria analizado es mayor o igual que 10, la versión se registra como &quot; http/?.? &quot; .</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Solicitud<br/></td>
<td>El estado de verbo pasado por la última solicitud analizada. Se incluyen verbos desconocidos, pero cualquier verbo que tenga más de 255 bytes se trunca a esta longitud. Si un verbo no está disponible, se usa un guión (0x002D) como marcador de posición para el campo vacío.<br/></td>
</tr>
<tr class="odd">
<td><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + consulta<br/></td>
<td>La dirección URL y cualquier consulta asociada a ella se registran como un campo, separados por un signo de interrogación (0x3F). Este campo se trunca en el límite de longitud de 4096 bytes.
<ul>
<li>Si esta dirección URL se ha analizado ( &quot; cocida &quot; ), se registra con la conversión de página de códigos local y se trata como un campo Unicode.</li>
<li>Si esta dirección URL no se ha analizado ( &quot; cocido &quot; ) en el momento del registro, se copia exactamente, sin ninguna conversión Unicode.</li>
<li>Si la API del servidor HTTP no puede analizar esta dirección URL, se usa un guión (0x002D) como marcador de posición para el campo vacío.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Estado del Protocolo<br/></td>
<td>El estado del Protocolo no puede superar 999. <br/>
<ul>
<li>Si el estado del Protocolo de la respuesta a una solicitud está disponible, se registra en este campo.</li>
<li>Si el estado del Protocolo no está disponible, se usa un guión (0x002D) como marcador de posición para el campo vacío.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>Cuyo<br/></td>
<td>No se usa en esta versión de la API del servidor HTTP. En este campo siempre aparece un guion de marcador de posición (0x002D).<br/></td>
</tr>
<tr class="even">
<td><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Frase del motivo<br/></td>
<td>Este campo contiene una cadena que identifica el tipo de error que se está registrando. Nunca se deja vacío.<br/></td>
</tr>
</tbody>
</table>



 

Las siguientes líneas de ejemplo proceden de un registro de errores de la API del servidor HTTP:

``` syntax
2002-07-05 18:45:09 172.31.77.6 2094 172.31.77.6 80 
                    HTTP/1.1 GET /qos/1kbfile.txt 503 - ConnLimit
2002-07-05 19:51:59 127.0.0.1 2780 127.0.0.1 80 
                    HTTP/1.1 GET /ThisIsMyUrl.htm 400 - Hostname
2002-07-05 19:53:00 127.0.0.1 2894 127.0.0.1 80 
                    HTTP/2.0 GET / 505 - Version_N/S
2002-07-05 20:06:01 172.31.77.6 64388 127.0.0.1 80 
                    - - - - - Timer_MinBytesPerSecond
```

 

 





