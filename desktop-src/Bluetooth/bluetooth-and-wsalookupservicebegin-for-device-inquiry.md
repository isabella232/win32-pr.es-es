---
title: Bluetooth y WSALookupServiceBegin para la consulta de dispositivos
description: En este tema se describe cómo usar la función WSALookupServiceBegin para realizar una consulta de los dispositivos visibles y fantasma. Para obtener más información, vea Detectar Bluetooth dispositivos y servicios.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth y WSALookupServiceBegin para la consulta de dispositivos Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4423b7c1c27124771c518409d9d1393a5f83afb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469192"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>Bluetooth y WSALookupServiceBegin para la consulta de dispositivos

En este tema se describe cómo usar la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para realizar una consulta de los dispositivos visibles y fantasma. Para obtener más información, vea [Detectar Bluetooth dispositivos y servicios.](discovering-bluetooth-devices-and-services.md)

La [**función WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) usa una estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) en su primer parámetro, *lpqsRestrictions,* para definir criterios de búsqueda. Bluetooth proporciona instrucciones específicas para el uso de la **función WSALookupServiceBegin** y **WSAQUERYSET**.

En la tabla siguiente se enumeran las restricciones que se aplican a la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) pasada al parámetro *lpqsRestrictions* al consultar dispositivos.




| Miembro WSAQUERYSET | Restricción | 
|--------------------|-------------|
| <strong>dwSize</strong> | Se establece <strong>en sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>). | 
| <strong>lpBlob</strong> | Este miembro contiene un puntero opcional a una <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>estructura BLOB.</strong></a> Si se especifica este miembro, los parámetros válidos de consulta del <strong>dispositivo LUP_FLUSHCACHE</strong> son los siguientes:<ul><li>El <strong>miembro cbSize</strong> de la <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>estructura BLOB</strong></a> debe ser <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</li><li>El <strong>miembro pBlobData</strong> es un puntero a una estructura <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE,</strong></a> para la que el miembro <strong>LAP</strong> es el código de acceso de consulta de Bluetooth y el miembro de longitud es la longitud, en segundos, de la consulta. <strong></strong></li></ul> | 
| <strong>dwNameSpace</strong> | Se establece <strong>en NS_BTH</strong>. | 
| Otros miembros | Se omiten otros miembros de la <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>estructura WSAQUERYSET.</strong></a> | 




 

Las marcas enumeradas en la tabla siguiente se usan en el *parámetro dwControlFlags* para controlar los resultados de la consulta. La función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) usa las marcas **LUP \_ CONTAINERS** y **LUP \_ FLUSHCACHE;** el resto de las marcas se usan en las llamadas a la función [**WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)

| Marca               | Resultado                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONTENEDORES \_ DE LUP    | Especifica que el propósito de la consulta es obtener una lista de Bluetooth dispositivos y no una lista de servicios. Esta marca debe establecerse.                                                                                                                                                                                                                                                                                       |
| LUP \_ FLUSHCACHE    | Desencadena una consulta de dispositivos locales o hace que se devuelvan los resultados almacenados en caché de consultas anteriores.                                                                                                                                                                                                                                                                                                                |
| TIPO DE VALOR \_ DEVUELTO DE \_ LUP  | Devuelve el Bluetooth COD (clase de bits de dispositivo) directamente en el **miembro lpServiceClassId** de la [**estructura WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) El COD se asigna al miembro **Data1** del GUID.                                                                                                                                                                                                      |
| SERVICIO LUP \_ RES \_  | Devuelve información de la dirección Bluetooth local. Esta marca solo tiene efecto si también se especifica **LUP \_ RETURN \_ ADDR.**                                                                                                                                                                                                                                                                                       |
| NOMBRE DEVUELTO DE LUP \_ \_  | Devuelve el nombre para mostrar del dispositivo en el miembro **lpszServiceInstanceName** de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada llamada a la función [**WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) Esta marca también debe especificarse  para recuperar el miembro de nombre de la estructura [**\_ BTH DEVICE \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) al especificar la marca **LUP \_ RETURN \_ BLOB.** |
| LUP \_ RETURN \_ ADDR  | Devuelve una estructura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) que contiene la dirección de 48 bits del elemento del mismo nivel en el miembro **lpcsaBuffer** de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada llamada a la función [**WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) Otros miembros de la **estructura SOCKADDR \_ BTH** estarán vacíos.                                                            |
| BLOB DEVUELTO DE LUP \_ \_  | Devuelve la [**estructura BTH \_ DEVICE \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) en cada llamada posterior a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).                                                                                                                                                                                                                                                           |
| LUP \_ FLUSHPREVIOUS | Omita el siguiente dispositivo disponible y devuelva el dispositivo que le sigue.                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bluetooth y WSALookupServiceBegin para la detección de servicios](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth y WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth y WSAQUERYSET para la consulta de dispositivos](bluetooth-and-wsaqueryset-for-device-inquiry.md)
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

[**BTH \_ QUERY \_ DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
