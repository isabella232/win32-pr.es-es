---
title: Bluetooth y WSAQUERYSET para la consulta de servicio
description: Uso de la estructura WSAQUERYSET con las funciones WSALookupServiceBegin y WSALookupServiceNext para obtener información sobre el proceso de consulta del servicio.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth y WSAQUERYSET para consultas de servicio Bluetooth
- WSAQUERYSET Bluetooth , para la consulta de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5db9c6cc3b6cc49f968c4eb39821b8b9857b0df
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467102"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth y WSAQUERYSET para la consulta de servicio

Bluetooth usa la estructura [**WSAQUERYSET,**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) con varias funciones, para facilitar la detección de dispositivos y servicios en el espacio de nombres Bluetooth, NS \_ BTH.

Las [**funciones WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) y [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usan la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para obtener datos sobre el proceso de consulta del servicio. En la tabla siguiente se describe cómo establecer los valores de miembro en la **estructura WSAQUERYSET** para este propósito.




| Miembro | Entrada a WSALookupServiceBegin | Valor devuelto de WSALookupServiceNext | 
|--------|--------------------------------|------------------------------------------|
| <strong>dwSize</strong> | Debe establecerse en <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>). | <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) devuelto por el sistema. | 
| <strong>dwOutputFlags</strong> | No se utiliza. | No se utiliza. | 
| <strong>lpszServiceInstanceName</strong> | No se utiliza. | Nombre para mostrar del servicio, convertido como una cadena codificada utf-8 a partir de la codificación de idioma predeterminada del Bluetooth servicename SDP. Se devuelve si LUP_RETURN_NAME se especifica . | 
| <strong>lpServiceClassId</strong> | Necesario. El valor más específico Bluetooth UUID para los servicios para los que se realiza la búsqueda. Por ejemplo, si este valor se establece en el UUID del protocolo L2CAP, devuelve todos los servicios que usan el protocolo L2CAP en el dispositivo de destino. Si se establece en el UUID de un servicio específico, devolvería solo las instancias de ese servicio. | No se utiliza. | 
| <strong>lpVersion</strong> | No se utiliza. | No se utiliza. | 
| <strong>lpszComment</strong> | No se utiliza. | Descripción del servicio, convertida como una cadena codificada en UTF-8 a partir de la codificación de idioma predeterminada del Bluetooth atributo SDP ServiceDescription. Se devuelve <strong>si LUP_RETURN_COMMENT</strong> se especifica . | 
| <strong>dwNameSpace</strong> | Debe ser NS_BTH. | Devuelve NS_BTH. | 
| <strong>lpNSProviderId</strong> | No se utiliza. | No se utiliza. | 
| <strong>lpszContext</strong> | Necesario. La Bluetooth de dispositivo con la que establecer una conexión SDP y consultar los servicios. Este valor debe ser una cadena que se convirtió mediante la llamada de función <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString.</strong></a> Si se proporciona Bluetooth dirección del dispositivo local, se busca en la base de datos de SDP local. | No se utiliza. | 
| <strong>dwNumberOfProtocols</strong> | No se utiliza. | No se utiliza. | 
| <strong>lpafpProtocols</strong> | No se utiliza. | No se utiliza. | 
| <strong>lpszQueryString</strong> | No se utiliza. | No se utiliza. | 
| <strong>dwNumberOfCsAddrs</strong> | No se utiliza. | Indica el número de elementos de la matriz de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> estructura. | 
| <strong>lpcsaBuffer</strong> | No se utiliza. | Puntero a una estructura <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> cuyo miembro <strong>LocalAddr.lpSockaddr</strong> apunta a un <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> que contiene la dirección conectable completa del servicio remoto, convertida desde la primera entrada del atributo SDP protocolDescriptorList de Bluetooth. Se devuelve <strong>si LUP_RETURN_ADDR</strong> se especifica . | 
| <strong>lpBlob</strong> | Opcional. Puntero a una <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> estructura que contiene parámetros avanzados para limitar los resultados de la búsqueda. Si se proporciona, <strong>lpServiceClassId</strong> se omite y las consultas almacenadas en caché no se realizarán correctamente. | <ul><li>Si se realiza una búsqueda de servicio: puntero a una <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>estructura BLOB</strong></a> que devuelve los identificadores de servicio. (<strong>BLOB.cbSize</strong>)/<strong>sizeof</strong>(ULONG) calcula el número de identificadores. <strong>BLOB.pBlobData es una</strong> matriz de valores ULONG que representan los identificadores de servicio.</li><li>Si se realiza una búsqueda de atributo o serviceAttribute: puntero a una <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>estructura BLOB</strong></a> que devuelve el registro SDP binario. <strong>BLOB.cbSize</strong> es el tamaño del registro SDP binario. <strong>BLOB.pBlobData</strong> apunta al propio registro. El registro SDP binario es necesario en muchos casos porque solo un número limitado de atributos SDP se pueden convertir a la estructura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> y solo se convierten cadenas UTF-8 codificadas predeterminadas. Las funciones que ayudan a analizar el registro binario de SDP se proporcionan en <a href="bluetooth-reference.md">la Bluetooth referencia.</a></li><li>Se devuelve si LUP_RETURN_BLOB se especifica .</li></ul> | 




 

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

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
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

 

 
