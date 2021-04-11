---
title: Bluetooth y WSALookupServiceBegin para la consulta de dispositivo
description: En este tema se describe cómo usar la función WSALookupServiceBegin para realizar una consulta de dispositivos visibles y fantasma. Para obtener más información, vea detección de dispositivos y servicios Bluetooth.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth y WSALookupServiceBegin para la consulta de dispositivos Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfbcab2a3134289630b4b301390f85e83d1d3d0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104149690"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>Bluetooth y WSALookupServiceBegin para la consulta de dispositivo

En este tema se describe cómo usar la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para realizar una consulta de dispositivos visibles y fantasma. Para obtener más información, vea [detección de dispositivos y servicios Bluetooth](discovering-bluetooth-devices-and-services.md).

La función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) usa una estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) en su primer parámetro, *lpqsRestrictions*, para definir los criterios de búsqueda. Bluetooth proporciona instrucciones específicas para el uso de la función **WSALookupServiceBegin** y **WSAQUERYSET**.

En la tabla siguiente se enumeran las restricciones que se aplican a la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) que se pasa al parámetro *lpqsRestrictions* al consultar los dispositivos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Miembro WSAQUERYSET</th>
<th>Restricción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>Establezca en <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</td>
</tr>
<tr class="even">
<td><strong>lpBlob</strong></td>
<td>Este miembro contiene un puntero opcional a una estructura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>blobs</strong></a> . Si se especifica este miembro, los parámetros de consulta de dispositivo válidos para <strong>LUP_FLUSHCACHE</strong> son los siguientes:
<ul>
<li>El miembro <strong>cbSize</strong> de la estructura del <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> debe ser <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</li>
<li>El miembro <strong>pBlobData</strong> es un puntero a una estructura de <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> , para la que el miembro <strong>LAP</strong> es el código de acceso de la consulta Bluetooth y el miembro de <strong>longitud</strong> es la longitud, en segundos, de la consulta.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>dwNameSpace</strong></td>
<td>Establezca en <strong>NS_BTH</strong>.</td>
</tr>
<tr class="even">
<td>Otros miembros</td>
<td>Se omiten otros miembros de la estructura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> .</td>
</tr>
</tbody>
</table>



 

Las marcas que se muestran en la tabla siguiente se usan en el parámetro *dwControlFlags* para controlar los resultados de la consulta. Los **\_ contenedores LUP** y las marcas **\_ FLUSHCACHE LUP** se usan en la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ; el resto de las marcas se usan en las llamadas a la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .

| Marca               | Resultado                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| contenedores de LUP \_    | Especifica que el propósito de la consulta es obtener una lista de dispositivos Bluetooth y no una lista de servicios. Se debe establecer esta marca.                                                                                                                                                                                                                                                                                       |
| LUP \_ FLUSHCACHE    | Desencadena una consulta de dispositivos locales o hace que se devuelvan los resultados almacenados en caché de las consultas anteriores.                                                                                                                                                                                                                                                                                                                |
| \_tipo de valor devuelto LUP \_  | Devuelve el COD Bluetooth (clase de bits de dispositivo) directamente en el miembro **lpServiceClassId** de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) . El COD se asigna al miembro **data1** del GUID.                                                                                                                                                                                                      |
| \_servicio res de LUP \_  | Devuelve información de la dirección Bluetooth local. Esta marca solo tiene efecto si también se especifica **LUP \_ Return \_ addr** .                                                                                                                                                                                                                                                                                       |
| \_nombre devuelto de LUP \_  | Devuelve el nombre para mostrar del dispositivo en el miembro **lpszServiceInstanceName** de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada llamada a la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . Esta marca también se debe especificar para recuperar el miembro **Name** de la estructura de [**\_ \_ información del dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) al especificar la marca **LUP \_ Return \_ BLOB** . |
| LUP \_ devolver \_ dirección  | Devuelve una [**estructura \_ SOCKADDR BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) que contiene la dirección de 48 bits del elemento del mismo nivel en el miembro **LpcsaBuffer** de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada llamada a la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . Otros miembros de la estructura **SOCKADDR \_ BTH** estarán vacíos.                                                            |
| LUP \_ devolver \_ BLOB  | Devuelve la estructura de [**\_ \_ información del dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) en cada llamada subsiguiente a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).                                                                                                                                                                                                                                                           |
| LUP \_ FLUSHPREVIOUS | Omitir el siguiente dispositivo disponible y devolver el dispositivo que le sigue.                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bluetooth y WSALookupServiceBegin para la detección de servicios](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth y WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth y WSAQUERYSET para la consulta de dispositivo](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Detección de dispositivos y servicios Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_dispositivo de consulta de BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 