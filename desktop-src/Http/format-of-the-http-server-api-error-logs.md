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
# <a name="format-of-the-http-server-api-error-logs"></a><span data-ttu-id="41ef1-104">Formato de los registros de errores de la API del servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="41ef1-104">Format of the HTTP Server API Error Logs</span></span>

<span data-ttu-id="41ef1-105">En general, los archivos de registro de errores de la API del servidor HTTP tienen el mismo formato que los registros de errores de W3C, salvo que los archivos de registro de errores de la API del servidor HTTP no contienen encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="41ef1-105">In general, HTTP Server API error log files have the same format as W3C error logs except that HTTP Server API error log files do not contain column headings.</span></span> <span data-ttu-id="41ef1-106">Cada línea de un registro de errores de la API del servidor HTTP registra un error con campos en un orden específico.</span><span class="sxs-lookup"><span data-stu-id="41ef1-106">Each line of an HTTP Server API error log records one error with fields in a specific order.</span></span> <span data-ttu-id="41ef1-107">Cada campo está separado del campo anterior por un carácter de espacio único (0x0020).</span><span class="sxs-lookup"><span data-stu-id="41ef1-107">Each field is separated from the preceding field by a single space character (0x0020).</span></span> <span data-ttu-id="41ef1-108">Dentro de cada campo, los caracteres de espacio, las tabulaciones y los caracteres de control no imprimibles se reemplazan por signos más (0x002B).</span><span class="sxs-lookup"><span data-stu-id="41ef1-108">Within each field, space characters, tabs, and unprintable control characters are replaced by plus signs (0x002B).</span></span>

<span data-ttu-id="41ef1-109">En la tabla siguiente se identifican los campos y el orden de los campos en un registro de errores.</span><span class="sxs-lookup"><span data-stu-id="41ef1-109">The following table identifies the fields and the order of the fields in an error log record.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="41ef1-110">Campo</span><span class="sxs-lookup"><span data-stu-id="41ef1-110">Field</span></span></th>
<th><span data-ttu-id="41ef1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="41ef1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41ef1-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Posteriormente</span><span class="sxs-lookup"><span data-stu-id="41ef1-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Date</span></span><br/></td>
<td><span data-ttu-id="41ef1-113">El campo de fecha sigue el formato del W3C y se basa en la hora universal coordinada (UTC). El campo de fecha tiene siempre 10 caracteres en formato &quot; AAAA-MM-DD &quot; .</span><span class="sxs-lookup"><span data-stu-id="41ef1-113">The Date field follows the W3C format and is based on Coordinated Universal Time (UTC).The Date field is always 10 characters in the form of &quot;YYYY-MM-DD&quot;.</span></span> <span data-ttu-id="41ef1-114">Por ejemplo, el 1 de mayo de 2003 se expresa como &quot; 2003-05-01 &quot; .</span><span class="sxs-lookup"><span data-stu-id="41ef1-114">For example, May 1, 2003 is expressed as &quot;2003-05-01&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ef1-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Tiempo</span><span class="sxs-lookup"><span data-stu-id="41ef1-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Time</span></span><br/></td>
<td><span data-ttu-id="41ef1-116">El campo de hora sigue el formato del W3C y se basa en la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="41ef1-116">The Time field follows the W3C format and is based on UTC.</span></span> <span data-ttu-id="41ef1-117">El campo de hora siempre tiene 8 caracteres en formato &quot; mm: HH: SS &quot; .</span><span class="sxs-lookup"><span data-stu-id="41ef1-117">The time field is always 8 characters in the form of &quot;MM:HH:SS&quot;.</span></span> <span data-ttu-id="41ef1-118">Por ejemplo, 5:30 PM (UTC) se expresa como &quot; 17:30:00 &quot; .</span><span class="sxs-lookup"><span data-stu-id="41ef1-118">For example, 5:30 PM (UTC) is expressed as &quot;17:30:00&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ef1-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Dirección IP del cliente</span><span class="sxs-lookup"><span data-stu-id="41ef1-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Client IP Address</span></span><br/></td>
<td><span data-ttu-id="41ef1-120">Dirección IP del cliente afectado que puede ser una dirección IPv4 o una dirección IPv6.</span><span class="sxs-lookup"><span data-stu-id="41ef1-120">The IP address of the affected client that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="41ef1-121">Si la dirección IP del cliente es una dirección IPv6, el campo ScopeId también se incluye en la dirección.</span><span class="sxs-lookup"><span data-stu-id="41ef1-121">If the client IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ef1-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Puerto de cliente</span><span class="sxs-lookup"><span data-stu-id="41ef1-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Client Port</span></span><br/></td>
<td><span data-ttu-id="41ef1-123">El número de puerto del cliente afectado.</span><span class="sxs-lookup"><span data-stu-id="41ef1-123">The port number for the affected client.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ef1-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Dirección IP del servidor</span><span class="sxs-lookup"><span data-stu-id="41ef1-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Server IP Address</span></span><br/></td>
<td><span data-ttu-id="41ef1-125">Dirección IP del servidor afectado que puede ser una dirección IPv4 o una dirección IPv6.</span><span class="sxs-lookup"><span data-stu-id="41ef1-125">The IP address of the affected server that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="41ef1-126">Si la dirección IP del servidor es una dirección IPv6, el campo ScopeId también se incluye en la dirección.</span><span class="sxs-lookup"><span data-stu-id="41ef1-126">If the server IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ef1-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Puerto de servidor</span><span class="sxs-lookup"><span data-stu-id="41ef1-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Server Port</span></span><br/></td>
<td><span data-ttu-id="41ef1-128">El número de puerto del servidor afectado.</span><span class="sxs-lookup"><span data-stu-id="41ef1-128">The port number of the affected server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ef1-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Versión de protocolo</span><span class="sxs-lookup"><span data-stu-id="41ef1-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Protocol Version</span></span><br/></td>
<td><span data-ttu-id="41ef1-130">La versión del protocolo que se está usando.</span><span class="sxs-lookup"><span data-stu-id="41ef1-130">The version of the protocol that is being used.</span></span> <br/>
<ul>
<li><span data-ttu-id="41ef1-131">Si la conexión no se ha analizado lo suficiente para determinar la versión del Protocolo, se usa un guión (0x002D) como marcador de posición para el campo vacío.</span><span class="sxs-lookup"><span data-stu-id="41ef1-131">If the connection has not been parsed enough to determine the protocol version, then a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
<li><span data-ttu-id="41ef1-132">Si el número de versión principal o secundaria analizado es mayor o igual que 10, la versión se registra como &quot; http/?.? &quot; .</span><span class="sxs-lookup"><span data-stu-id="41ef1-132">If either the major or minor version number parsed is greater than or equal to 10, the version is logged as &quot;HTTP/?.?&quot;.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ef1-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Solicitud</span><span class="sxs-lookup"><span data-stu-id="41ef1-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span><br/></td>
<td><span data-ttu-id="41ef1-134">El estado de verbo pasado por la última solicitud analizada.</span><span class="sxs-lookup"><span data-stu-id="41ef1-134">The verb state passed by the last request parsed.</span></span> <span data-ttu-id="41ef1-135">Se incluyen verbos desconocidos, pero cualquier verbo que tenga más de 255 bytes se trunca a esta longitud.</span><span class="sxs-lookup"><span data-stu-id="41ef1-135">Unknown verbs are included, but any verb that is more than 255 bytes is truncated to this length.</span></span> <span data-ttu-id="41ef1-136">Si un verbo no está disponible, se usa un guión (0x002D) como marcador de posición para el campo vacío.</span><span class="sxs-lookup"><span data-stu-id="41ef1-136">If a verb is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ef1-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + consulta</span><span class="sxs-lookup"><span data-stu-id="41ef1-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + Query</span></span><br/></td>
<td><span data-ttu-id="41ef1-138">La dirección URL y cualquier consulta asociada a ella se registran como un campo, separados por un signo de interrogación (0x3F).</span><span class="sxs-lookup"><span data-stu-id="41ef1-138">The URL and any query associated with it are logged as one field, separated by a question mark (0x3F).</span></span> <span data-ttu-id="41ef1-139">Este campo se trunca en el límite de longitud de 4096 bytes.</span><span class="sxs-lookup"><span data-stu-id="41ef1-139">This field is truncated at its length limit of 4096 bytes.</span></span>
<ul>
<li><span data-ttu-id="41ef1-140">Si esta dirección URL se ha analizado ( &quot; cocida &quot; ), se registra con la conversión de página de códigos local y se trata como un campo Unicode.</span><span class="sxs-lookup"><span data-stu-id="41ef1-140">If this URL has been parsed (&quot;cooked&quot;), it is logged with local code page conversion, and is treated as a Unicode field.</span></span></li>
<li><span data-ttu-id="41ef1-141">Si esta dirección URL no se ha analizado ( &quot; cocido &quot; ) en el momento del registro, se copia exactamente, sin ninguna conversión Unicode.</span><span class="sxs-lookup"><span data-stu-id="41ef1-141">If this URL has not been parsed (&quot;cooked&quot;) at the time of logging, it is copied exactly, without any Unicode conversion.</span></span></li>
<li><span data-ttu-id="41ef1-142">Si la API del servidor HTTP no puede analizar esta dirección URL, se usa un guión (0x002D) como marcador de posición para el campo vacío.</span><span class="sxs-lookup"><span data-stu-id="41ef1-142">If the HTTP Server API cannot parse this URL, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ef1-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Estado del Protocolo</span><span class="sxs-lookup"><span data-stu-id="41ef1-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Protocol Status</span></span><br/></td>
<td><span data-ttu-id="41ef1-144">El estado del Protocolo no puede superar 999.</span><span class="sxs-lookup"><span data-stu-id="41ef1-144">The protocol status cannot exceed 999.</span></span> <br/>
<ul>
<li><span data-ttu-id="41ef1-145">Si el estado del Protocolo de la respuesta a una solicitud está disponible, se registra en este campo.</span><span class="sxs-lookup"><span data-stu-id="41ef1-145">If the protocol status of the response to a request is available, it is logged in this field.</span></span></li>
<li><span data-ttu-id="41ef1-146">Si el estado del Protocolo no está disponible, se usa un guión (0x002D) como marcador de posición para el campo vacío.</span><span class="sxs-lookup"><span data-stu-id="41ef1-146">If the protocol status is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ef1-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>Cuyo</span><span class="sxs-lookup"><span data-stu-id="41ef1-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId</span></span><br/></td>
<td><span data-ttu-id="41ef1-148">No se usa en esta versión de la API del servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="41ef1-148">Not used in this version of the HTTP Server API.</span></span> <span data-ttu-id="41ef1-149">En este campo siempre aparece un guion de marcador de posición (0x002D).</span><span class="sxs-lookup"><span data-stu-id="41ef1-149">A placeholder hyphen (0x002D) always appears in this field.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ef1-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Frase del motivo</span><span class="sxs-lookup"><span data-stu-id="41ef1-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Reason Phrase</span></span><br/></td>
<td><span data-ttu-id="41ef1-151">Este campo contiene una cadena que identifica el tipo de error que se está registrando.</span><span class="sxs-lookup"><span data-stu-id="41ef1-151">This field contains a string that identifies the kind of error that is being logged.</span></span> <span data-ttu-id="41ef1-152">Nunca se deja vacío.</span><span class="sxs-lookup"><span data-stu-id="41ef1-152">It is never left empty.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="41ef1-153">Las siguientes líneas de ejemplo proceden de un registro de errores de la API del servidor HTTP:</span><span class="sxs-lookup"><span data-stu-id="41ef1-153">The following sample lines are from an HTTP Server API error log:</span></span>

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

 

 





