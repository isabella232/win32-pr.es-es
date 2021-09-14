---
title: Bluetooth y WSALookupServiceBegin para la detección de servicios
description: Para detectar la existencia de un servicio determinado en un servidor Bluetooth, los clientes usan las funciones WSALookupServiceBegin, WSALookupServiceNext y WSALookupServiceEnd.
ms.assetid: d9961600-cdca-42ec-92eb-118b8186ed2e
keywords:
- Bluetooth y WSALookupServiceBegin para la detección de Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e6da97e8277478da7102bf21d33c68f9d1b8a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261951"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-service-discovery"></a>Bluetooth y WSALookupServiceBegin para la detección de servicios

Para detectar la existencia de un servicio determinado en un servidor de Bluetooth, los clientes usan las funciones [**WSALookupServiceBegin,**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)y [**WSALookupServiceEnd.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) Las consultas se pueden realizar para direcciones locales y remotas, pero las conexiones solo se pueden establecer con direcciones remotas. Los identificadores de servicio detectados durante esta operación no se pueden usar para eliminar el servicio a través [**de WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea). RFCOMM no admite bucles bucles.

Se pueden realizar dos tipos básicos de consultas de detección de servicios:

-   Consultas de uno o varios servicios en el dispositivo local
-   Consultas de uno o varios servicios en un dispositivo del mismo nivel especificado

La [**función WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) recibe una estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) en su *parámetro lpqsRestrictions.* **WSALookupServiceBegin** realiza una consulta de cliente basada en el conjunto de restricciones de búsqueda que **contiene WSAQUERYSET.** Bluetooth clientes deben especificar las restricciones, enumeradas en la tabla siguiente, en la estructura **WSAQUERYSET** cuando se usa la función **WSALookupServiceBegin** para consultar los servicios.



| Miembro WSAQUERYSET    | Restricción                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**            | Se establece **en sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                                                                                                                                                                                                    |
| **lpServiceClassId**  | Establezca en el uuid más Bluetooth que se puede usar para determinar el ámbito de la consulta. Por ejemplo, si se establece **lpServiceClassId** en el UUID del protocolo L2CAP, se devuelven todos los servicios L2CAP, en esencia se enumeran todos los registros SD del destino. Sin embargo, al establecer el UUID en un servicio específico, solo se devuelven las instancias de ese servicio.<br/> |
| **dwNameSpace**       | Establezca en **NS \_ BTH**.                                                                                                                                                                                                                                                                                                                                                             |
| **dwNumberOfCsAddrs** | Establecer en 0.                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**       | Establezca en la Bluetooth de dispositivo con la que establecer una conexión SDP para realizar la consulta de servicios. Este miembro debe ser una cadena que se convierta mediante la [**función WSAAddressToString.**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Si se proporciona la dirección de radio local, se busca en los registros SDP locales.<br/>                                             |
| Otros miembros         | Se omiten todos los demás miembros de la estructura [**WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)                                                                                                                                                                                                                                                                                        |



 

La conexión de SDP al dispositivo remoto no permanece activa después de que la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) complete una consulta de servicio; La conexión finaliza antes de **que WSALookupServiceBegin** devuelva . Las aplicaciones que requieren que la conexión SDP permanezca activa una vez completada una consulta de servicio deben especificar la clase de servicio UUID a la que se va a conectar mediante el miembro **serviceClassId** de la estructura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) al emitir la llamada a la función connect de Windows [**Sockets.**](/windows/desktop/api/winsock2/nf-winsock2-connect)

Las marcas, enumeradas en la tabla siguiente, se usan en el parámetro *dwControlFlags* de las funciones [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) y [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) para controlar los resultados de la consulta. La función **WSALookupServiceBegin** usa las marcas **LUP \_ CONTAINERS** y **LUP \_ FLUSHCACHE;** el resto de las marcas se usan en las llamadas a la función **WSALookupServiceNext.**


| Marca | Resultado | 
|------|--------|
| <strong>LUP_CONTAINERS</strong> | No se debe establecer. | 
| <strong>LUP_FLUSHCACHE</strong> | Por lo general, las <strong>aplicaciones LUP_FLUSHCACHE</strong>. Esta marca indica al sistema que ignore cualquier información almacenada en caché y establezca una conexión SDP por vía inalámbrica al dispositivo especificado para realizar la búsqueda de SDP. Esta operación no almacenada en caché puede tardar varios segundos (mientras que una búsqueda almacenada en caché se devuelve rápidamente). Bluetooth almacena en caché de forma proactiva los registros SDP de dispositivos cercanos, ni almacena en caché actualmente consultas anteriores de forma agresiva. Por lo tanto, las aplicaciones deben prever que las consultas pueden no devolver ningún resultado (con un código de error <strong>de WSASERVICE_NOT_FOUND</strong>) si <strong>no LUP_FLUSHCACHE</strong> especificado. Los datos almacenados en caché que están disponibles mediante la interfaz Windows sockets se pueden mejorar en el futuro. | 
| <strong>LUP_RES_SERVICE</strong> | Devuelve información sobre la dirección Bluetooth local. Esta marca tiene un efecto solo <strong>si LUP_RETURN_ADDR</strong> también se especifica . | 
| <strong>LUP_RETURN_NAME</strong> | Devuelve el nombre para mostrar del servicio en el miembro <strong>lpszServiceInstanceName</strong> de la estructura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> para cada llamada a la función <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext.</strong></a> | 
| <strong>LUP_RETURN_TYPE</strong> | Devuelve el identificador de clase de servicio <strong>en el miembro lpServiceClassId</strong> de la <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>estructura WSAQUERYSET.</strong></a><blockquote>[!Note]<br />El uso de esta marca solo es aplicable a la <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina"><strong>función WSALookupServiceBegin.</strong></a> Este valor siempre es cero para <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext.</strong></a></blockquote><br /> | 
| <strong>LUP_RETURN_ADDR</strong> | Devuelve una dirección en el miembro <strong>lpcsaBuffer que</strong> se va a usar con las <a href="/windows/desktop/api/winsock2/nf-winsock2-connect"><strong>llamadas a la función connect.</strong></a> La dirección devuelta contiene el número de puerto. | 
| <strong>LUP_RETURN_BLOB</strong> | Devuelve los registros SD correspondientes en el <strong>miembro lpBlob,</strong> con formato según la especificación Bluetooth registro SDP. | 
| <strong>LUP_RETURN_ALL</strong> | Devuelve toda la información de las marcas anteriores. | 
| <strong>LUP_RETURN_COMMENT</strong> | Devuelve la descripción del servicio en el <strong>miembro lpszComment</strong> de la estructura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> para cada llamada a la función <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext.</strong></a> | 
| <strong>LUP_FLUSHPREVIOUS</strong> | Omita el siguiente registro disponible y devuelva el registro que le sigue. | 




 

## <a name="advanced-service-queries"></a>Consultas de servicio avanzadas

Las operaciones de consulta que se describen en la sección anterior se pueden usar para devolver todos los resultados de un único GUID, lo que debería ser suficiente para la mayoría de las aplicaciones. Una consulta avanzada permite a una aplicación crear una consulta más específica. proporciona la capacidad de hacer coincidir los UUID y los atributos en la información devuelta.

Para realizar una consulta avanzada de servicios, Bluetooth clientes deben especificar las restricciones siguientes en la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) que se pasa al parámetro *lpqsRestrictions.*



| Miembro WSAQUERYSET   | Restricción                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**           | Se establece **en sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                                                                                                                                                        |
| **lpszContext**      | Establezca en la Bluetooth de dispositivo con la que establecer una conexión SDP para realizar la consulta de servicios. Este miembro debe ser una cadena que se convierta mediante la [**función WSAAddressToString.**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Si se proporciona la dirección de radio local, se busca en los registros SDP locales.<br/> |
| **lpBlob.pBlobData** | Puntero a una [**estructura \_ BTH QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) que contiene todos los parámetros que limitan los resultados de la consulta.                                                                                                                                                                                           |
| **dwNameSpace**      | Establezca en **NS \_ BTH**.                                                                                                                                                                                                                                                                                                                 |
| Otros miembros        | Se omiten todos los demás miembros de la estructura [**WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)                                                                                                                                                                                                                                            |



 

Las marcas siguientes se pasan en el parámetro *dwControlFlags* de [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para controlar los resultados de una consulta avanzada.

| Marca                     | Resultado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CONTENEDORES \_ DE LUP**      | No se debe establecer.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **LUP \_ FLUSHCACHE**      | Por lo general, las aplicaciones deben **especificar LUP \_ FLUSHCACHE.** Esta marca indica al sistema que ignore cualquier información almacenada en caché y establezca una conexión SDP por vía inalámbrica al dispositivo especificado para realizar la búsqueda de SDP. Esta operación no almacenada en caché puede tardar varios segundos (mientras que una búsqueda almacenada en caché se devuelve rápidamente). Bluetooth almacena en caché de forma proactiva los registros de SDP desde dispositivos cercanos, ni almacena en caché de forma agresiva las consultas anteriores. Por lo tanto, las aplicaciones deben esperar que las consultas no devuelvan resultados con frecuencia **(WSASERVICE \_ NOT \_ FOUND**) si no se especifica **LUP \_ FLUSHCACHE.** Los datos almacenados en caché que están disponibles mediante la interfaz Windows sockets se pueden mejorar en el futuro. |
| **SERVICIO LUP \_ RES \_**    | Devuelve información para la dirección Bluetooth local. Establecer esta marca solo tiene efecto si también se especifica **LUP \_ RETURN \_ ADDRR.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **NOMBRE DEVUELTO \_ DE \_ LUP**    | Devuelve el nombre para mostrar del servicio. Esta marca se omite para **SDP \_ SERVICE SEARCH \_ \_ REQUEST**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **TIPO DE VALOR \_ DEVUELTO DE \_ LUP**    | Devuelve el identificador de clase de servicio. Esta marca se omite para **SDP \_ SERVICE SEARCH \_ \_ REQUEST**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LUP \_ RETURN \_ ADDR**    | Devuelve una dirección en el miembro **lpcsaBuffer que** se usará con las llamadas a la [**función connect.**](/windows/desktop/api/winsock2/nf-winsock2-connect) La dirección devuelta contiene el número de puerto. Esta marca se omite para **SDP \_ SERVICE SEARCH \_ \_ REQUEST**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **BLOB DE \_ DEVOLUCIÓN DE LUP \_**    | Devuelve los registros SD correspondientes en un formato que se ajuste a la especificación Bluetooth registro SDP correspondiente. Para **SDP \_ SERVICE SEARCH \_ \_ REQUEST**, el resultado en **lpBlob** para la llamada posterior a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) es una matriz de identificadores Bluetooth SDP. Para **SDP \_ SERVICE ATTRIBUTE \_ \_ REQUEST** y **SDP SERVICE SEARCH ATTRIBUTE \_ \_ \_ \_ REQUEST**, el resultado de cada llamada posterior a **WSALookupServiceNext** es un registro SDP de Bluetooth binario cuyos atributos están restringidos a los especificados por el **miembro pRange** de la consulta. Esta marca es necesaria para **SDP \_ SERVICE SEARCH \_ \_ REQUEST**.                                                               |
| **COMENTARIO DE \_ DEVOLUCIÓN DE LUP \_** | Devuelve la descripción del servicio en el miembro **lpszComment** de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada llamada a la [**función WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **LUP \_ FLUSHPREVIOUS**   | Omita el siguiente registro disponible y devuelva el registro que le sigue.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

En la entrada, **lpBlob** -> **pBlobData** apunta a una estructura [**\_ BTH QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) que contiene los valores enumerados en la tabla siguiente.

> [!Note]  
> La solicitud de búsqueda inicial debe ser capaz de caber en un paquete L2CAP. Sin embargo, la respuesta se puede dividir en muchos paquetes L2CAP.

 



| Miembro            | Valor                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**          | Tipo de búsqueda que se realizará. Este valor puede ser uno de **SDP \_ SERVICE SEARCH \_ \_ REQUEST**, **SDP SERVICE ATTRIBUTE \_ \_ \_ REQUEST** o **SDP SERVICE SEARCH ATTRIBUTE \_ \_ \_ \_ REQUEST**. Cada tipo de búsqueda está asociado a un mecanismo de búsqueda subyacente definido por la especificación Bluetooth SDP. Cada devolución da como resultado el formulario descrito por la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) que se definió anteriormente en esta sección (Consultas avanzadas de servicio). |
| **serviceHandle** | Se usa para las búsquedas de atributos. Este valor especifica el identificador de servicio con el que se consultan los atributos del **miembro pRange.**                                                                                                                                                                                                                                                                                                                                            |
| **Uuid**         | Se usa para las búsquedas **de service y serviceAttribute.** Este valor especifica los UUID que debe contener un registro para que coincidan con la búsqueda. Si se van a consultar **\_ uuids \_ \_** max en la consulta, este valor establece el elemento SdpQueryUuid que sigue inmediatamente al último UUID válido en todos los ceros.                                                                                                                                                                       |
| **numRange**      | Se usa para las búsquedas **de atributos y serviceAttribute.** Este valor especifica el número de elementos de **pRange**.                                                                                                                                                                                                                                                                                                                                                             |
| **Prange**        | Se usa para las búsquedas **de atributos y serviceAttribute.** Este valor especifica los valores de atributo que se recuperarán para los registros que coincidan.                                                                                                                                                                                                                                                                                                                                        |



 

Después de cada llamada correcta a la función [**WSALookupServiceNext,**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) **lpBlob** -> **pBlobData** apunta a un bloque de datos que contiene los valores enumerados en la tabla siguiente.

| Value                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SOLICITUD DE \_ BÚSQUEDA DEL SERVICIO \_ \_ SDP**                                                    | Matriz de identificadores de registros SDP idénticos a **ServiceRecordHandleList** definido por Bluetooth 1.1 SDP 4.5.2. El número de identificadores de SDP devueltos se calcula mediante (**lpBlob**->cbSize)/**sizeof**(ULONG). Todos los resultados se devuelven en una sola llamada a la [**función WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) |
| **SDP \_ SOLICITUD \_ DE ATRIBUTO DE SERVICIO \_ o** SOLICITUD DE ATRIBUTO DE BÚSQUEDA DE SERVICIO **\_ \_ DE \_ \_ SDP** | Un archivo Bluetooth registro SDP. Para **SDP \_ SERVICE ATTRIBUTE \_ \_ REQUEST**, todos los resultados se devuelven en una sola llamada a la [**función WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)                                                                                                                                                       |



 

> [!Note]  
> Si no se especifica el miembro **lpBlob** durante la entrada de una consulta de servicio, se realiza una búsqueda de servicio y atributo para el servicio especificado en el miembro **lpServiceClassId** en atributos de 0 a 0xFFFF.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bluetooth y WSAQUERYSET para la consulta de servicios](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Detección de dispositivos y servicios Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth y WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin para la consulta de dispositivos](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[**BTH \_ QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**Conectar**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

