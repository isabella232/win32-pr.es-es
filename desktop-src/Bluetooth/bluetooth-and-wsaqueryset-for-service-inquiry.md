---
title: Bluetooth y WSAQUERYSET para la consulta de servicios
description: Usar la estructura WSAQUERYSET con las funciones WSALookupServiceBegin y WSALookupServiceNext para obtener información sobre el proceso de consulta del servicio.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth y WSAQUERYSET for Service Inquiry Bluetooth
- WSAQUERYSET Bluetooth , para la consulta de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38bd953f8d205f0afb097ec2d098ee674a01d5fc37cfbaf4109e02cdbb4b395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959164"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth y WSAQUERYSET para la consulta de servicios

Bluetooth usa la estructura [**WSAQUERYSET,**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) con varias funciones, para facilitar la detección de dispositivos y servicios en el espacio de nombres Bluetooth, NS \_ BTH.

Las [**funciones WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) y [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usan la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para obtener datos sobre el proceso de consulta del servicio. En la tabla siguiente se describe cómo establecer los valores de miembro en la **estructura WSAQUERYSET** para este propósito.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Miembro</th>
<th>Entrada a WSALookupServiceBegin</th>
<th>Valor devuelto de WSALookupServiceNext</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>Debe establecerse en <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</td>
<td><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) devuelto por el sistema.</td>
</tr>
<tr class="even">
<td><strong>dwOutputFlags</strong></td>
<td>No se utiliza.</td>
<td>No se utiliza.</td>
</tr>
<tr class="odd">
<td><strong>lpszServiceInstanceName</strong></td>
<td>No se usa.</td>
<td>Nombre para mostrar del servicio, convertido como una cadena codificada en UTF-8 a partir de la codificación de idioma predeterminada del Bluetooth atributo SDP ServiceName. Se devuelve si LUP_RETURN_NAME se especifica .</td>
</tr>
<tr class="even">
<td><strong>lpServiceClassId</strong></td>
<td>Obligatorio. El valor más Bluetooth UUID para los servicios para los que se realiza la búsqueda. Por ejemplo, si este valor se establece en el UUID del protocolo L2CAP, devuelve todos los servicios mediante el protocolo L2CAP en el dispositivo de destino. Si se establece en el UUID de un servicio específico, devolvería solo las instancias de ese servicio.</td>
<td>No se usa.</td>
</tr>
<tr class="odd">
<td><strong>lpVersion</strong></td>
<td>No se utiliza.</td>
<td>No se utiliza.</td>
</tr>
<tr class="even">
<td><strong>lpszComment</strong></td>
<td>No se usa.</td>
<td>Descripción del servicio, convertido como una cadena codificada en UTF-8 a partir de la codificación de idioma predeterminada del Bluetooth servicedescription de SDP. Se devuelve <strong>si LUP_RETURN_COMMENT</strong> se especifica .</td>
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
<td>Obligatorio. Dirección Bluetooth dispositivo con la que establecer una conexión SDP y consultar los servicios. Este valor debe ser una cadena convertida mediante la llamada de función <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString.</strong></a> Si se proporciona Bluetooth de dispositivo local, se busca en la base de datos de SDP local.</td>
<td>No se usa.</td>
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
<td>No se usa.</td>
<td>Indica el número de elementos de la matriz de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> estructura.</td>
</tr>
<tr class="even">
<td><strong>lpcsaBuffer</strong></td>
<td>No se usa.</td>
<td>Puntero a una estructura <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> cuyo miembro <strong>LocalAddr.lpSockaddr</strong> apunta a un <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> que contiene la dirección conectable completa del servicio remoto, convertida desde la primera entrada del atributo SDP protocolDescriptorList de Bluetooth. Se devuelve <strong>si LUP_RETURN_ADDR</strong> especificado.</td>
</tr>
<tr class="odd">
<td><strong>lpBlob</strong></td>
<td>Opcional. Puntero a una <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> estructura que contiene parámetros avanzados para limitar los resultados de la búsqueda. Si se proporciona, <strong>lpServiceClassId</strong> se omite y las consultas almacenadas en caché no se realiza correctamente.</td>
<td><ul>
<li>Si se realiza una búsqueda de servicio: puntero a una <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>estructura BLOB</strong></a> que devuelve los identificadores de servicio. (<strong>BLOB.cbSize</strong>)/<strong>sizeof</strong>(ULONG) calcula el número de identificadores. <strong>BLOB.pBlobData es una</strong> matriz de valores ULONG que representan los identificadores de servicio.</li>
<li>Si se realiza una búsqueda de atributo o serviceAttribute: puntero a una estructura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> que devuelve el registro SDP binario. <strong>BLOB.cbSize</strong> es el tamaño del registro SDP binario. <strong>BLOB.pBlobData</strong> apunta al propio registro. El registro SDP binario es necesario en muchos casos porque solo un número limitado de atributos SDP se pueden convertir a la estructura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> y solo se convierten cadenas UTF-8 codificadas predeterminadas. Las funciones que ayudan a analizar el registro SDP binario se proporcionan en la <a href="bluetooth-reference.md">Bluetooth referencia.</a></li>
<li>Se devuelve LUP_RETURN_BLOB se especifica .</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bluetooth y WSAQUERYSET para set service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth y WSAQUERYSET para la consulta de dispositivos](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Bluetooth y BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

Bluetooth y WSALookupServiceNext
</dt> <dt>

[Bluetooth Referencia](bluetooth-reference.md)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**BTH \_ QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**INFORMACIÓN DE \_ CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 