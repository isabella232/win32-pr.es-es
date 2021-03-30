---
title: Bluetooth y WSALookupServiceBegin para la detección de servicios
description: Para detectar la existencia de un servicio determinado en un servidor Bluetooth, los clientes usan las funciones WSALookupServiceBegin, WSALookupServiceNext y WSALookupServiceEnd.
ms.assetid: d9961600-cdca-42ec-92eb-118b8186ed2e
keywords:
- Bluetooth y WSALookupServiceBegin para detección de servicios Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274b3beb3de7683bd43a0f99350db6e1a347f51e
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103904875"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-service-discovery"></a>Bluetooth y WSALookupServiceBegin para la detección de servicios

Para detectar la existencia de un servicio determinado en un servidor Bluetooth, los clientes usan las funciones [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)y [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) . Las consultas se pueden realizar para las direcciones locales y remotas, pero las conexiones solo se pueden establecer con direcciones remotas. Los identificadores de servicio detectados durante esta operación no se pueden usar para eliminar el servicio a través de [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea). El bucle invertido no es compatible con RFCOMM.

Se pueden realizar dos tipos básicos de consultas de detección de servicios:

-   Consultas de uno o más servicios en el dispositivo local
-   Consultas de uno o más servicios en un dispositivo del mismo nivel especificado

La función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) recibe una estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) en su parámetro *lpqsRestrictions* . **WSALookupServiceBegin** realiza una consulta de cliente basada en el conjunto de restricciones de búsqueda que contiene **WSAQUERYSET** . Los clientes Bluetooth deben especificar las restricciones que se indican en la siguiente tabla, en la estructura **WSAQUERYSET** al usar la función **WSALookupServiceBegin** para consultar los servicios.



| Miembro WSAQUERYSET    | Restricción                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**            | Establezca en **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                                                                                                                                                                                                    |
| **lpServiceClassId**  | Se establece en el UUID de Bluetooth más específico que se puede usar para determinar el ámbito de la consulta. Por ejemplo, si se establece **lpServiceClassId** en el UUID del protocolo L2CAP, se devuelven todos los servicios de L2CAP, lo que básicamente enumera todos los registros SD en el destino. Sin embargo, al establecer el UUID en un servicio específico, solo se devuelven las instancias de ese servicio.<br/> |
| **dwNameSpace**       | Establezca en **NS \_ BTH**.                                                                                                                                                                                                                                                                                                                                                             |
| **dwNumberOfCsAddrs** | Establecer en 0.                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**       | Establezca en la dirección del dispositivo Bluetooth con la que desea establecer una conexión SDP para realizar la consulta de servicios. Este miembro debe ser una cadena que se convierte mediante la función [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) . Si se proporciona la dirección de radio local, se busca en los registros SDP locales.<br/>                                             |
| Otros miembros         | Se omiten todos los demás miembros de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .                                                                                                                                                                                                                                                                                        |



 

La conexión SDP al dispositivo remoto no permanece activa después de que la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) complete una consulta de servicio; la conexión se termina antes de que **WSALookupServiceBegin** devuelva. Las aplicaciones que requieren que la conexión SDP permanezca activa después de completarse una consulta de servicio deben especificar el UUID de clase de servicio al que conectarse mediante el miembro **serviceClassId** de la estructura [**\_ BTH de SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) al emitir la llamada de función de Windows Sockets [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .

Las marcas que se enumeran en la tabla siguiente se usan en el parámetro *dwControlFlags* de las funciones [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) y [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) para controlar los resultados de la consulta. Los **\_ contenedores LUP** y las marcas **\_ FLUSHCACHE LUP** se usan en la función **WSALookupServiceBegin** ; el resto de las marcas se usan en las llamadas a la función **WSALookupServiceNext** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Marca</th>
<th>Resultado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>LUP_CONTAINERS</strong></td>
<td>No se debe establecer.</td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHCACHE</strong></td>
<td>Por lo general, las aplicaciones deben especificar <strong>LUP_FLUSHCACHE</strong>. Esta marca indica al sistema que ignore cualquier información almacenada en memoria caché y establezca una conexión de SDP a través del aire en el dispositivo especificado para realizar la búsqueda de SDP. Esta operación sin almacenamiento en caché puede tardar varios segundos (mientras que una búsqueda almacenada en caché se devuelve rápidamente). En la actualidad, Bluetooth no almacena en caché de forma proactiva los registros SDP de dispositivos cercanos ni almacena actualmente en caché las consultas anteriores. Por lo tanto, las aplicaciones deben prever que las consultas no devuelvan resultados (con un código de error de <strong>WSASERVICE_NOT_FOUND</strong>) si no se especifica <strong>LUP_FLUSHCACHE</strong> . Los datos almacenados en caché que están disponibles mediante la interfaz de Windows Sockets se pueden mejorar en el futuro.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RES_SERVICE</strong></td>
<td>Devuelve información sobre la dirección Bluetooth local. Esta marca solo tiene efecto si también se especifica <strong>LUP_RETURN_ADDR</strong> .</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_NAME</strong></td>
<td>Devuelve el nombre para mostrar del servicio en el miembro <strong>lpszServiceInstanceName</strong> de la estructura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> para cada llamada a la función <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> .</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_TYPE</strong></td>
<td>Devuelve el identificador de la clase de servicio en el miembro <strong>lpServiceClassId</strong> de la estructura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> .
<blockquote>
[!Note]<br />
El uso de esta marca solo es aplicable a la función <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina"><strong>WSALookupServiceBegin</strong></a> . Este valor siempre es cero para <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ADDR</strong></td>
<td>Devuelve una dirección en el miembro <strong>lpcsaBuffer</strong> que se va a usar con llamadas a la función <a href="/windows/desktop/api/winsock2/nf-winsock2-connect"><strong>Connect</strong></a> . La dirección devuelta contiene el número de puerto.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_BLOB</strong></td>
<td>Devuelva los registros SD coincidentes en el miembro <strong>lpBlob</strong> , con el formato de acuerdo con la especificación de registro SDP Bluetooth.</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ALL</strong></td>
<td>Devolver toda la información de marcas anterior.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_COMMENT</strong></td>
<td>Devuelve la descripción del servicio en el miembro <strong>lpszComment</strong> de la estructura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> para cada llamada a la función <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHPREVIOUS</strong></td>
<td>Omitir el siguiente registro disponible y devolver el registro que le sigue.</td>
</tr>
</tbody>
</table>



 

## <a name="advanced-service-queries"></a>Consultas de servicio avanzadas

Las operaciones de consulta que se describen en la sección anterior se pueden usar para devolver todos los resultados de un único GUID, que debe ser suficiente para la mayoría de las aplicaciones. Una consulta avanzada permite a una aplicación crear una consulta más específica; proporciona la capacidad de hacer coincidir los UUID y los atributos de la información devuelta.

Para realizar una consulta avanzada de los servicios, los clientes Bluetooth deben especificar las siguientes restricciones en la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) que se pasa al parámetro *lpqsRestrictions* .



| Miembro WSAQUERYSET   | Restricción                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**           | Establezca en **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                                                                                                                                                        |
| **lpszContext**      | Establezca en la dirección del dispositivo Bluetooth con la que desea establecer una conexión SDP para realizar la consulta de servicios. Este miembro debe ser una cadena que se convierte mediante la función [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) . Si se proporciona la dirección de radio local, se busca en los registros SDP locales.<br/> |
| **lpBlob.pBlobData** | Puntero a una estructura de [**\_ \_ servicio de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) que contiene todos los parámetros que limitan los resultados de la consulta.                                                                                                                                                                                           |
| **dwNameSpace**      | Establezca en **NS \_ BTH**.                                                                                                                                                                                                                                                                                                                 |
| Otros miembros        | Se omiten todos los demás miembros de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .                                                                                                                                                                                                                                            |



 

Las marcas siguientes se pasan en el parámetro *dwControlFlags* de [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para controlar los resultados de una consulta avanzada.

| Marca                     | Resultado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **contenedores de LUP \_**      | No se debe establecer.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **LUP \_ FLUSHCACHE**      | Por lo general, las aplicaciones deben especificar **LUP \_ FLUSHCACHE**. Esta marca indica al sistema que ignore cualquier información almacenada en memoria caché y establezca una conexión de SDP a través del aire en el dispositivo especificado para realizar la búsqueda de SDP. Esta operación sin almacenamiento en caché puede tardar varios segundos (mientras que una búsqueda almacenada en caché se devuelve rápidamente). Bluetooth no almacena en caché de forma proactiva los registros SDP de dispositivos cercanos ni almacena en caché de forma agresiva las consultas anteriores. Por lo tanto, las aplicaciones deberían esperar que las consultas no devuelvan resultados con frecuencia (**\_ no \_ se encontró WSASERVICE**) si no se especifica **LUP \_ FLUSHCACHE** . Los datos almacenados en caché que están disponibles mediante la interfaz de Windows Sockets se pueden mejorar en el futuro. |
| **\_servicio res de LUP \_**    | Devuelve información de la dirección Bluetooth local. El establecimiento de esta marca solo tiene efecto si también se especifica **LUP \_ Return \_** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **\_nombre devuelto de LUP \_**    | Devuelve el nombre para mostrar del servicio. Esta marca se omite para **la \_ \_ \_ solicitud de búsqueda de Servicio SDP**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_tipo de valor devuelto LUP \_**    | Devuelve el identificador de la clase de servicio. Esta marca se omite para **la \_ \_ \_ solicitud de búsqueda de Servicio SDP**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LUP \_ devolver \_ dirección**    | Devuelve una dirección en el miembro **lpcsaBuffer** que se va a usar con llamadas a la función [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) . La dirección devuelta contiene el número de puerto. Esta marca se omite para **la \_ \_ \_ solicitud de búsqueda de Servicio SDP**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **LUP \_ devolver \_ BLOB**    | Devuelva los registros SD coincidentes en un formato que se ajuste a la especificación de registro SDP Bluetooth. Para **la \_ \_ \_ solicitud de búsqueda de Servicio SDP**, el resultado de **LpBlob** para la llamada subsiguiente a [**WSALOOKUPSERVICENEXT**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) es una matriz de identificadores de SDP Bluetooth. Para la solicitud de **atributo de \_ servicio \_ \_ SDP** y la **solicitud de atributo de \_ búsqueda de servicio \_ \_ \_ SDP**, el resultado de cada llamada subsiguiente a **WSALookupServiceNext** es un registro SDP de Bluetooth binario cuyos atributos están restringidos a los especificados por el miembro **pRange** de la consulta. Esta marca es necesaria para **la \_ \_ \_ solicitud de búsqueda de Servicio SDP**.                                                               |
| **LUP \_ Comentario devuelto \_** | Devuelve la descripción del servicio en el miembro **lpszComment** de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada llamada a la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **LUP \_ FLUSHPREVIOUS**   | Omitir el siguiente registro disponible y devolver el registro que le sigue.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

En la entrada, **lpBlob** -> **pBlobData** apunta a una estructura de [**\_ \_ servicio de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) que contiene los valores que se muestran en la tabla siguiente.

> [!Note]  
> La solicitud de búsqueda inicial debe ser capaz de encajar en un paquete L2CAP. La respuesta, sin embargo, puede dividirse en muchos paquetes L2CAP.

 



| Miembro            | Valor                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**          | Tipo de búsqueda que se va a realizar. Este valor puede ser una solicitud **de \_ \_ búsqueda de \_ Servicio SDP**, una **\_ solicitud de \_ atributo \_ de Servicio SDP** o una **solicitud de atributo de \_ búsqueda de servicio \_ \_ \_ SDP**. Cada tipo de búsqueda está asociado a un mecanismo de búsqueda subyacente definido por la especificación SDP de Bluetooth. Cada valor devuelto produce el formato descrito por la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) que se define anteriormente en esta sección (consultas de servicio avanzadas). |
| **serviceHandle** | Se utiliza para las búsquedas de atributos. Este valor especifica el identificador de servicio con el que se van a consultar los atributos del miembro **pRange** .                                                                                                                                                                                                                                                                                                                                            |
| **UUID**         | Se usa para las búsquedas de servicio y **serviceAttribute** . Este valor especifica el UUID que debe contener un registro para que coincida con la búsqueda. Si se van a consultar menos de los **UUID máximos en el UUID \_ \_ de \_ consulta** , este valor establece el elemento SdpQueryUuid que sigue inmediatamente al último UUID válido en todos los ceros.                                                                                                                                                                       |
| **numRange**      | Se usa para las búsquedas de atributos y **serviceAttribute** . Este valor especifica el número de elementos de **pRange**.                                                                                                                                                                                                                                                                                                                                                             |
| **pRange**        | Se usa para las búsquedas de atributos y **serviceAttribute** . Este valor especifica los valores de atributo que se van a recuperar para los registros coincidentes.                                                                                                                                                                                                                                                                                                                                        |



 

Después de cada llamada correcta a la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) , **lpBlob** -> **pBlobData** apunta a un bloque de datos que contiene los valores que se muestran en la tabla siguiente.

| Value                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_solicitud de \_ búsqueda de Servicio SDP \_**                                                    | Una matriz de identificadores de registro SDP que es idéntico a la **ServiceRecordHandleList** definida por Bluetooth 1,1 SDP 4.5.2. El número de identificadores de SDP devueltos se calcula mediante (**lpBlob**->cbSize)/**sizeof**(ulong). Todos los resultados se devuelven en una sola llamada a la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) . |
| **SDP \_ Solicitud \_ de \_ atributo de servicio** o **solicitud de atributo de \_ búsqueda de servicio \_ \_ \_ SDP** | Un registro SDP de Bluetooth binario. Para **la \_ \_ \_ solicitud de atributo de Servicio SDP**, todos los resultados se devuelven en una sola llamada a la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .                                                                                                                                                       |



 

> [!Note]  
> Si el miembro **lpBlob** no se especifica durante la entrada de una consulta de servicio, se realiza una búsqueda de servicio y atributo para el servicio especificado en el miembro **lpServiceClassId** en atributos de 0 a 0xFFFF.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bluetooth y WSAQUERYSET para la consulta de servicio](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Detección de dispositivos y servicios Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth y WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin para la consulta de dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[**\_servicio de consulta de BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**conéctelo**](/windows/desktop/api/winsock2/nf-winsock2-connect)
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

