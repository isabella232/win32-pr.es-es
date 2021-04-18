---
description: Para obtener la notificación de redes lógicas invalidadas, use la función WSANSPIoctl para registrar los eventos de cambio de ubicación de red.
ms.assetid: 531b6269-5f35-44c1-ad0f-c5f103029893
title: Consultando NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac7a4f57e14bb967b04d3a9fd6fe66717da3878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706197"
---
# <a name="querying-nla"></a>Consultando NLA

Para obtener la notificación de redes lógicas invalidadas, use la función [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) para registrar los eventos de cambio de ubicación de red. Se pueden usar dos métodos para determinar si una ubicación de red válida previamente ha dejado de ser válida: métodos de sondeo o notificación con e/s superpuestas o mensajería de Windows.

Las consultas se crean mediante las funciones [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) y [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) para enumerar todas las redes lógicas disponibles. El uso de cada una de estas funciones se explica individualmente en el resto de esta sección, comenzando por la función **WSALookupServiceBegin** .

> [!Note]  
> NLA requiere el archivo de encabezado mswsock. h, que, de forma predeterminada, no se incluye en el archivo WinSock2. h.

 

## <a name="step-1-initiate-the-query"></a>Paso 1: iniciar la consulta

Para una referencia rápida, la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) tiene la siguiente sintaxis:

``` syntax
INT WSALookupServiceBegin(
  LPWSAQUERYSET lpqsRestrictions,
  DWORD dwControlFlags,
  LPHANDLE lphLookup
);
```

NLA admite las siguientes marcas de búsqueda de *dwControlFlags* :

<dl> \_nombre devuelto de LUP \_  
LUP \_ Comentario devuelto \_  
LUP \_ devolver \_ BLOB  
LUP \_ devolver \_ todo  
LUP \_ Deep  
</dl>

Estas marcas restringen los conjuntos de resultados devueltos en las llamadas subsiguientes a [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), la función a redes que contienen campos del tipo especificado. Por ejemplo, si se especifica LUP \_ Return \_ BLOB en el parámetro *dwControlFlags* de la llamada a la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) , se restringen los conjuntos de resultados de las llamadas posteriores a **WSALookupServiceNext** a las redes que contienen información de BLOB. El uso de la \_ marca LUP Return \_ All es equivalente a especificar LUP \_ Return \_ Name, LUP REturn \_ \_ comment y LUP \_ Return \_ BLOB, pero no LUP \_ Deep.

Para obtener una explicación de estas marcas de búsqueda, consulte la página de referencia de la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) .

El identificador de búsqueda devuelto por NLA en el parámetro *lphLookup* es privado a NLA y no debe modificarse. Puesto que el identificador devuelto es privado para NLA, las funciones como [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) no están disponibles.

NLA devuelve cero cuando se completa correctamente, tal como se define en la página de referencia de la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) . De lo contrario, NLA admite los siguientes códigos de error.

| Error                    | Significado                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | No se realizó una llamada correcta a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar NLA.                                                   |
| WSAEINVAL                | Uno o varios parámetros no eran válidos o los parámetros especificados en la llamada de función se aplican a protocolos distintos de IP.                                         |
| \_no \_ se encontró WSASERVICE   | El parámetro *lpServiceClassId* de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) pasada en el parámetro *lpqsRestrictions* contiene un GUID no válido. |
| datos de WSANO \_              | La \_ marca de contenedores LUP se especificó en el parámetro *dwControlFlags* .                                                                                       |
| WSAEFAULT                | Se ha producido una infracción de acceso al intentar obtener acceso a los parámetros proporcionados por el usuario.                                                                            |
| WSASYSNOTREADY           | El servicio NLA no está disponible para procesar la solicitud.                                                                                                      |
| WSA \_ no \_ hay suficiente \_ memoria | NLA o el servicio NLA no pudo asignar suficiente memoria para procesar esta solicitud.                                                                        |



 

## <a name="step-2-perform-the-query"></a>Paso 2: realizar la consulta

El siguiente paso para consultar NLA requiere el uso de la función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) . Para una referencia rápida, la función **WSALookupServiceNext** tiene la siguiente sintaxis:

``` syntax
INT WSALookupServiceNext(
  HANDLE hLookup,
  DWORD dwControlFlags,
  LPDWORD lpdwBufferLength,
  LPWSAQUERYSET lpqsResults
);
```

El parámetro *lLookup* es el identificador de búsqueda devuelto de la llamada anterior a la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) .

El parámetro *dwControlFlags* admite las marcas siguientes:

<dl> \_nombre devuelto de LUP \_  
LUP \_ Comentario devuelto \_  
LUP \_ devolver \_ BLOB  
LUP \_ devolver \_ todo  
LUP \_ FLUSHPREVIOUS  
</dl>

Estas marcas son independientes de las marcas admitidas en la llamada a la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) . Tenga en cuenta que las restricciones especificadas en la llamada anterior a la función **WSALookupServiceBegin** restringen la búsqueda; la adición de marcas con la función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) en un intento de ampliar la consulta más allá de las restricciones especificadas en la llamada a **WSALookupServiceBegin** se pasa por alto de forma silenciosa. Sin embargo, se permite especificar un conjunto de marcas más restrictivo que el especificado en la llamada **WSALookupServiceBegin** .

Si la red detallada en *lpqsResults* es una red activa, se anexa una serie de estructuras de **\_ blobs NLA** tal como se especifica en el miembro **lpBlob** de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) devuelta en *lpqsResults*. Estas estructuras de **\_ blobs NLA** se pueden encadenar y se pueden enumerar recorriendo la lista mientras que NLA \_ BLOB. header. nextOffset es distinto de cero. Para obtener los resultados de toda la información de ubicación de red, siga llamando a [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), función hasta que \_ \_ no \_ se devuelva el error WSA E, tal como se explica en la página de referencia de **WSALookupServiceNext**.

La función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) también se utiliza junto con la función [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) para recibir la notificación de cambios en la red. Vea la [notificación de NLA](notification-from-nla-2.md) para obtener más información.

NLA devuelve cero tras una finalización correcta. Los clientes de NLA deben seguir llamando a [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), función hasta \_ que \_ \_ se devuelva WSA E, lo que indica que se ha devuelto toda la información sobre las redes disponibles.

De lo contrario, al llamar a la función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)para NLA, se admiten los siguientes códigos de error.

| Error                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | No se realizó una llamada correcta a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) que no se ha inicializado NLA.                                                                                                                                                                                                                                                                                                |
| \_identificador no válido de WSA \_     | El identificador de búsqueda proporcionado en el parámetro *BUSCARH* no era un identificador de SP NLA válido. Los clientes deben llamar primero a la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) y recibir un identificador de SP NLA válido para obtener los resultados de la consulta.                                                                                                                                                               |
| WSAESYSNOTREADY          | El servicio NLA no está disponible para procesar esta solicitud.                                                                                                                                                                                                                                                                                                                                                     |
| WSAEFAULT                | El tamaño de búfer especificado en el parámetro *lpdwBufferLength* era insuficiente para contener los resultados a los que apunta *lpqsResults*. El búfer necesario se especifica en *lpdwBufferLength*; Si el cliente no puede proporcionar un búfer suficientemente grande, el cliente puede llamar a la función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) con *DWCONTROLFLAGS* establecido en LUP \_ FLUSHPREVIOUS para omitir la entrada. |
| WSA \_ no \_ hay suficiente \_ memoria | NLA no puede obtener información de red del servicio de sistema NLA debido a que no hay memoria suficiente en el proceso de llamada.                                                                                                                                                                                                                                                                                  |
| WSA \_ E \_ no \_ más         | No hay ninguna red adicional que enumerar para la consulta.                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="step-3-terminate-the-query"></a>Paso 3: finalizar la consulta

Cuando se completan todas las consultas a NLA y una aplicación ya no requiere el uso de NLA, se debe realizar una llamada a la función [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) . No llame a **WSALookupServiceEnd** si la aplicación va a recibir la notificación de cambios basada en la consulta enviada. Consulte [notificación desde NLA](notification-from-nla-2.md) para obtener más información sobre la recepción de notificaciones. Como la mayoría de los proveedores de servicios de Windows Sockets, NLA mantiene un recuento de referencias para sus clientes. La llamada a la función **WSALookupServiceEnd** cuando se completan las consultas a NLA habilita los recursos del sistema que NLA ya no necesita para liberarlos.

NLA admite los siguientes códigos de error para las llamadas a funciones [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .

| Error                | Significado                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED    | No se realizó una llamada correcta a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar NLA. |
| \_identificador no válido de WSA \_ | El identificador proporcionado en el parámetro *BUSCARH* no era un identificador SP de NLA válido.                             |



 

 

 



