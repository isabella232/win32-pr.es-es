---
title: Formato de los registros de errores de LA API del servidor HTTP
description: En general, los archivos de registro de errores de LA API del servidor HTTP tienen el mismo formato que los registros de errores de W3C, salvo que los archivos de registro de errores de LA API del servidor HTTP no contienen encabezados de columna.
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- API de servidor HTTP, formato de registro de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5747e172aa19720a0ae992117000b08402e78d88a66501a9af7b12859a0ac88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014803"
---
# <a name="format-of-the-http-server-api-error-logs"></a>Formato de los registros de errores de LA API del servidor HTTP

En general, los archivos de registro de errores de LA API del servidor HTTP tienen el mismo formato que los registros de errores de W3C, salvo que los archivos de registro de errores de LA API del servidor HTTP no contienen encabezados de columna. Cada línea de un registro de errores de LA API del servidor HTTP registra un error con campos en un orden específico. Cada campo está separado del campo anterior por un solo carácter de espacio (0x0020). Dentro de cada campo, los caracteres de espacio, las pestañas y los caracteres de control no imprimibles se reemplazan por signos más (0x002B).

En la tabla siguiente se identifican los campos y el orden de los campos en una entrada de registro de errores.



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
<td><span id="Date"></span><span id="date"></span><span id="DATE"></span>Fecha<br/></td>
<td>El campo Fecha sigue el formato W3C y se basa en la hora universal coordinada (UTC). El campo Date siempre tiene 10 caracteres en forma &quot; de YYYY-MM-DD. &quot; Por ejemplo, el 1 de mayo de 2003 se expresa como &quot; 2003-05-01 &quot; .<br/></td>
</tr>
<tr class="even">
<td><span id="Time"></span><span id="time"></span><span id="TIME"></span>hora<br/></td>
<td>El campo Hora sigue el formato W3C y se basa en UTC. El campo de tiempo siempre tiene 8 caracteres en forma de &quot; MM:HH:SS. &quot; Por ejemplo, 5:30 p. m. (UTC) se expresa como &quot; 17:30:00 &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Dirección IP del cliente<br/></td>
<td>Dirección IP del cliente afectado que puede ser una dirección IPv4 o una dirección IPv6. Si la dirección IP del cliente es una dirección IPv6, el campo ScopeId también se incluye en la dirección.<br/></td>
</tr>
<tr class="even">
<td><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Puerto de cliente<br/></td>
<td>Número de puerto del cliente afectado.<br/></td>
</tr>
<tr class="odd">
<td><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Dirección IP del servidor<br/></td>
<td>Dirección IP del servidor afectado que puede ser una dirección IPv4 o una dirección IPv6. Si la dirección IP del servidor es una dirección IPv6, el campo ScopeId también se incluye en la dirección.<br/></td>
</tr>
<tr class="even">
<td><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Puerto del servidor<br/></td>
<td>Número de puerto del servidor afectado.<br/></td>
</tr>
<tr class="odd">
<td><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Versión del protocolo<br/></td>
<td>Versión del protocolo que se está utilizando. <br/>
<ul>
<li>Si la conexión no se ha analizado lo suficiente como para determinar la versión del protocolo, se usa un guion (0x002D) como marcador de posición para el campo vacío.</li>
<li>Si el número de versión principal o secundaria que se analiza es mayor o igual que 10, la versión se registra como &quot; HTTP/?.? &quot; .</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verbo<br/></td>
<td>Estado del verbo pasado por la última solicitud analizada. Se incluyen verbos desconocidos, pero cualquier verbo de más de 255 bytes se trunca a esta longitud. Si un verbo no está disponible, se usa un guion (0x002D) como marcador de posición para el campo vacío.<br/></td>
</tr>
<tr class="odd">
<td><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + Query<br/></td>
<td>La dirección URL y cualquier consulta asociada a ella se registran como un campo, separados por un signo de interrogación (0x3F). Este campo se trunca con su límite de longitud de 4096 bytes.
<ul>
<li>Si esta dirección URL se ha analizado (preparado), se registra con la conversión de página de códigos local y se &quot; trata como un campo &quot; Unicode.</li>
<li>Si esta dirección URL no se ha analizado (preparado) en el momento del registro, se copia exactamente, sin &quot; &quot; ninguna conversión Unicode.</li>
<li>Si la API del servidor HTTP no puede analizar esta dirección URL, se usa un guion (0x002D) como marcador de posición para el campo vacío.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Estado del protocolo<br/></td>
<td>El estado del protocolo no puede superar 999. <br/>
<ul>
<li>Si el estado del protocolo de la respuesta a una solicitud está disponible, se registra en este campo.</li>
<li>Si el estado del protocolo no está disponible, se usa un guion (0x002D) como marcador de posición para el campo vacío.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId<br/></td>
<td>No se usa en esta versión de la API de servidor HTTP. Un guion de marcador de posición (0x002D) siempre aparece en este campo.<br/></td>
</tr>
<tr class="even">
<td><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Frase de motivo<br/></td>
<td>Este campo contiene una cadena que identifica el tipo de error que se está registrando. Nunca se deja vacío.<br/></td>
</tr>
</tbody>
</table>



 

Las siguientes líneas de ejemplo son de un registro de errores de LA API del servidor HTTP:

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

 

 





