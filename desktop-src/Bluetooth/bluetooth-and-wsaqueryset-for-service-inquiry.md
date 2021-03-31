---
title: Bluetooth y WSAQUERYSET para la consulta de servicio
description: Uso de la estructura WSAQUERYSET con las funciones WSALookupServiceBegin y WSALookupServiceNext para obtener información sobre el proceso de consulta de servicio.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth y WSAQUERYSET para la consulta de servicio Bluetooth
- WSAQUERYSET Bluetooth, para la consulta de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656fa407829112005c9c54c5ab84c9c1bf2f4e33
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795303"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth y WSAQUERYSET para la consulta de servicio

Bluetooth usa la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , con varias funciones, para facilitar la detección de dispositivos y servicios en el espacio de nombres Bluetooth, NS \_ BTH.

Las funciones [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) y [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usan la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para obtener datos sobre el proceso de consulta de servicio. En la tabla siguiente se describe cómo establecer los valores de miembro de la estructura **WSAQUERYSET** para este propósito.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Miembro</th>
<th>Entrada en WSALookupServiceBegin</th>
<th>Valor devuelto de WSALookupServiceNext</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>Debe establecerse en <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</td>
<td><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) devuelto por System.</td>
</tr>
<tr class="even">
<td><strong>dwOutputFlags</strong></td>
<td>No se utiliza.</td>
<td>No se utiliza.</td>
</tr>
<tr class="odd">
<td><strong>lpszServiceInstanceName</strong></td>
<td>No se utiliza.</td>
<td>Nombre para mostrar del servicio, convertido en una cadena codificada en UTF-8 de la codificación de idioma predeterminada del atributo SDP de Bluetooth ServiceName. Se devuelve si se especifica LUP_RETURN_NAME.</td>
</tr>
<tr class="even">
<td><strong>lpServiceClassId</strong></td>
<td>Obligatorio. El UUID de Bluetooth único más específico para los servicios para los que se realiza la búsqueda. Por ejemplo, si este valor se establece en el UUID del protocolo L2CAP, devuelve todos los servicios que usan el protocolo L2CAP en el dispositivo de destino. Si se establece en el UUID de un servicio específico, solo devolverá las instancias de ese servicio.</td>
<td>No se utiliza.</td>
</tr>
<tr class="odd">
<td><strong>lpVersion</strong></td>
<td>No se utiliza.</td>
<td>No se utiliza.</td>
</tr>
<tr class="even">
<td><strong>lpszComment</strong></td>
<td>No se utiliza.</td>
<td>Descripción del servicio, convertido como una cadena codificada en UTF-8 de la codificación de idioma predeterminada del atributo de SDP de Bluetooth. Se devuelve si se especifica <strong>LUP_RETURN_COMMENT</strong> .</td>
</tr>
<tr class="odd">
<td><strong>dwNameSpace</strong></td>
<td>Debe ser NS_BTH.</td>
<td>Devuelve NS_BTH.</td>
</tr>
<tr class="even">
<td><strong>lpNSProviderId</strong></td>
<td>No se utiliza.</td>
<td>No se utiliza.</td>
</tr>
<tr class="odd">
<td><strong>lpszContext</strong></td>
<td>Obligatorio. La dirección del dispositivo Bluetooth con la que se establece una conexión SDP y se consultan los servicios. Este valor debe ser una cadena convertida mediante la llamada a la función <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> . Si se proporciona la dirección del dispositivo Bluetooth local, se busca en la base de datos SDP local.</td>
<td>No se utiliza.</td>
</tr>
<tr class="even">
<td><strong>dwNumberOfProtocols</strong></td>
<td>No se utiliza.</td>
<td>No se utiliza.</td>
</tr>
<tr class="odd">
<td><strong>lpafpProtocols</strong></td>
<td>No se utiliza.</td>
<td>No se utiliza.</td>
</tr>
<tr class="even">
<td><strong>lpszQueryString</strong></td>
<td>No se utiliza.</td>
<td>No se utiliza.</td>
</tr>
<tr class="odd">
<td><strong>dwNumberOfCsAddrs</strong></td>
<td>No se utiliza.</td>
<td>Indica el número de elementos de la matriz de estructuras de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>lpcsaBuffer</strong></td>
<td>No se utiliza.</td>
<td>Puntero a una estructura de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> cuyo miembro <strong>LocalAddr. lpSockaddr</strong> señala a un <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> que contiene la dirección completa conectable del servicio remoto, convertida a partir de la primera entrada del atributo SDP de Bluetooth ProtocolDescriptorList. Se devuelve si se especifica <strong>LUP_RETURN_ADDR</strong> .</td>
</tr>
<tr class="odd">
<td><strong>lpBlob</strong></td>
<td>Opcional. Puntero a una estructura de <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> que contiene parámetros avanzados para limitar los resultados de la búsqueda. Si se proporciona, se omite <strong>lpServiceClassId</strong> y las consultas en caché no se realizan correctamente.</td>
<td><ul>
<li>Si se realiza una búsqueda de servicio: puntero a una estructura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> que devuelve los identificadores de servicio. (<strong>BLOB. cbSize</strong>)/<strong>sizeof</strong>(ulong) calcula el número de identificadores. <strong>BLOB. pBlobData</strong> es una matriz de valores ulong que representan los identificadores de servicio.</li>
<li>Si se realiza una búsqueda de atributos o serviceAttribute: puntero a una estructura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> que devuelve el registro SDP binario. <strong>BLOB. cbSize</strong> es el tamaño del registro SDP binario. <strong>BLOB. pBlobData</strong> apunta al propio registro. El registro SDP binario es necesario en muchos casos porque solo se puede convertir un número limitado de atributos SDP en la estructura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> y solo se convierten las cadenas UTF-8 codificadas de forma predeterminada. Las funciones que ayudan a analizar el registro SDP binario se proporcionan en la sección de <a href="bluetooth-reference.md">referencia de Bluetooth</a> .</li>
<li>Se devuelve si se especifica LUP_RETURN_BLOB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bluetooth y WSAQUERYSET para Set Service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth y WSAQUERYSET para la consulta de dispositivo](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Bluetooth y BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

Bluetooth y WSALookupServiceNext
</dt> <dt>

[Referencia de Bluetooth](bluetooth-reference.md)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_servicio de consulta de BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**información de CSADDR \_**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 