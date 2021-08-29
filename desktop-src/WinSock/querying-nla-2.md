---
description: Para obtener la notificación de redes lógicas invalidadas, use la función WSANSPIoctl para registrarse para los eventos de cambio de ubicación de red.
ms.assetid: 531b6269-5f35-44c1-ad0f-c5f103029893
title: Consulta de NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f10244eb4d3549db21287f57746a07d5363dc916e70ae141f941a4064e070be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097655"
---
# <a name="querying-nla"></a>Consulta de NLA

Para obtener la notificación de redes lógicas invalidadas, use la función [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) para registrarse para los eventos de cambio de ubicación de red. Se pueden usar dos métodos para determinar si una ubicación de red válida previamente ha quedado no válida: métodos de sondeo o notificación mediante E/S superpuesta o Windows mensajes.

Las consultas se forman mediante las funciones [**WSALookupServiceBegin,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) y [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) para enumerar todas las redes lógicas disponibles. El uso de cada una de estas funciones se explica individualmente a lo largo del resto de esta sección, empezando por la función **WSALookupServiceBegin.**

> [!Note]  
> NLA requiere el archivo de encabezado Mswsock.h, que de forma predeterminada no se incluye en el archivo Winsock2.h.

 

## <a name="step-1-initiate-the-query"></a>Paso 1: Iniciar la consulta

Como referencia rápida, la [**función WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) tiene la sintaxis siguiente:

``` syntax
INT WSALookupServiceBegin(
  LPWSAQUERYSET lpqsRestrictions,
  DWORD dwControlFlags,
  LPHANDLE lphLookup
);
```

NLA admite las siguientes marcas de búsqueda *dwControlFlags:*

<dl> NOMBRE DEVUELTO DE LUP \_ \_  
COMENTARIO DE \_ DEVOLUCIÓN DE LUP \_  
BLOB DE \_ DEVOLUCIÓN DE LUP \_  
LUP \_ RETURN \_ ALL  
LUP \_ DEEP  
</dl>

Estas marcas restringen los conjuntos de resultados devueltos en llamadas posteriores a la función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)a redes que contienen campos del tipo especificado. Por ejemplo, si se especifica LUP RETURN BLOB en el parámetro dwControlFlags de la llamada de función \_ \_ [**WSALookupServiceBegin,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)  se restringen los conjuntos de resultados de las llamadas posteriores a **WSALookupServiceNext** a las redes que contienen información de BLOB. El uso de la marca LUP RETURN ALL equivale a especificar \_ \_ LUP RETURN NAME, LUP RETURN COMMENT y LUP RETURN BLOB, pero no \_ \_ \_ \_ \_ \_ LUP \_ DEEP.

Para obtener una explicación de estas marcas de búsqueda, consulte la página de referencia de la función [**WSALookupServiceBegin.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)

El identificador de búsqueda devuelto por NLA en *el parámetro lphLookup* es privado para NLA y no se debe modificar. Puesto que el identificador devuelto es privado para NLA, funciones como [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) no están disponibles.

NLA devuelve cero tras la finalización correcta, tal como se define en la página de referencia de la función [**WSALookupServiceBegin.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) De lo contrario, NLA admite los siguientes códigos de error.

| Error                    | Significado                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | No se realizó una llamada correcta a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar NLA.                                                   |
| WSAEINVAL                | Uno o varios parámetros no eran válidos o los parámetros especificados en la llamada de función se aplican a protocolos distintos de IP.                                         |
| WSASERVICE \_ NO \_ ENCONTRADO   | El *parámetro lpServiceClassId* de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) pasado en el parámetro *lpqsRestrictions* contiene un GUID no válido. |
| DATOS DE \_ WSANO              | La marca CONTAINERS de LUP \_ se especificó en el *parámetro dwControlFlags.*                                                                                       |
| WSAEFAULT                | Se produjo una infracción de acceso al intentar acceder a los parámetros proporcionados por el usuario.                                                                            |
| WSASYSNOTREADY           | El servicio NLA no está disponible para procesar la solicitud.                                                                                                      |
| WSA \_ NO TIENE MEMORIA \_ \_ SUFICIENTE | NLA o el servicio NLA no pudieron asignar suficiente memoria para procesar esta solicitud.                                                                        |



 

## <a name="step-2-perform-the-query"></a>Paso 2: Realizar la consulta

El siguiente paso para consultar NLA requiere el uso de la [**función WSALookupServiceNext.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) Como referencia rápida, la **función WSALookupServiceNext** tiene la sintaxis siguiente:

``` syntax
INT WSALookupServiceNext(
  HANDLE hLookup,
  DWORD dwControlFlags,
  LPDWORD lpdwBufferLength,
  LPWSAQUERYSET lpqsResults
);
```

El *parámetro lLookup* es el identificador de búsqueda devuelto por la llamada anterior a la [**función WSALookupServiceBegin.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)

El *parámetro dwControlFlags* admite las marcas siguientes:

<dl> NOMBRE DEVUELTO DE LUP \_ \_  
COMENTARIO DE \_ DEVOLUCIÓN DE LUP \_  
BLOB DE \_ DEVOLUCIÓN DE LUP \_  
LUP \_ RETURN \_ ALL  
LUP \_ FLUSHPREVIOUS  
</dl>

Estas marcas son independientes de las marcas admitidas en la [**llamada de función WSALookupServiceBegin.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) Tenga en cuenta que las restricciones especificadas en la llamada anterior a la función **WSALookupServiceBegin** restringen la búsqueda; Agregar marcas con la función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) en un intento de ampliar la consulta más allá de las restricciones especificadas en la llamada **a WSALookupServiceBegin** se omiten en modo silencioso. Sin embargo, se permite especificar un conjunto de marcas más restrictivo que el especificado en la **llamada a WSALookupServiceBegin.**

Si la red detallada en *lpqsResults* es una red activa, se anexa una serie de estructuras **\_ BLOB** de NLA como se especifica en el miembro **lpBlob** de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) devuelta en *lpqsResults*. Estas **estructuras BLOB \_ de NLA** se pueden encadenar y se pueden enumerar recorriendo la lista mientras que NLA \_ BLOB.header.nextOffset es distinto de cero. Para obtener los resultados de toda la información de ubicación de red, siga llamando a la función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)hasta que se devuelva el error WSA E NO MORE, como se explica en la página de referencia de \_ \_ \_ **WSALookupServiceNext.**

La [**función WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) también se usa junto con la función [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) para recibir la notificación de los cambios de red. Consulte [Notificación de NLA](notification-from-nla-2.md) para obtener más información.

NLA devuelve cero tras la finalización correcta. Los clientes de NLA deben seguir llamando a la función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)hasta que se devuelva WSA E NO MORE, lo que indica que se ha devuelto toda la información sobre las redes \_ \_ \_ disponibles.

De lo contrario, al [**llamar a WSALookupServiceNext,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)la función para NLA admite los siguientes códigos de error.

| Error                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | No se realizó una llamada correcta a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) que inicializó NLA.                                                                                                                                                                                                                                                                                                |
| IDENTIFICADOR NO VÁLIDO DE WSA \_ \_     | El identificador de búsqueda proporcionado en *el parámetro hLookup* no era un identificador de SP de NLA válido. Los clientes deben llamar primero a [**la función WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) y recibir un identificador de SP de NLA válido para obtener los resultados de la consulta.                                                                                                                                                               |
| WSAESYSNOTREADY          | El servicio NLA no está disponible para procesar esta solicitud.                                                                                                                                                                                                                                                                                                                                                     |
| WSAEFAULT                | El tamaño de búfer especificado en el parámetro *lpdwBufferLength* no era suficiente para contener los resultados a los que *apunta lpqsResults*. El búfer necesario se especifica en *lpdwBufferLength*; Si el cliente no puede proporcionar un búfer lo suficientemente grande, el cliente puede llamar a la función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) con *dwControlFlags* establecido en LUP FLUSHPREVIOUS para omitir la \_ entrada. |
| WSA \_ NO TIENE MEMORIA \_ \_ SUFICIENTE | NLA no puede obtener información de red del servicio del sistema NLA debido a memoria insuficiente en el proceso de llamada.                                                                                                                                                                                                                                                                                  |
| WSA \_ E \_ NO \_ MORE         | No hay redes adicionales para enumerar para la consulta.                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="step-3-terminate-the-query"></a>Paso 3: Finalizar la consulta

Cuando se completen todas las consultas a NLA y una aplicación ya no requiera el uso de NLA, se debe realizar una llamada a la función [**WSALookupServiceEnd.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) No llame a **WSALookupServiceEnd si** la aplicación recibirá una notificación de cambio basada en la consulta enviada. Consulte [Notificación de NLA](notification-from-nla-2.md) para obtener más información sobre la recepción de notificaciones. Al igual Windows proveedores de servicios sockets, NLA mantiene un recuento de referencias para sus clientes. Llamar a **la función WSALookupServiceEnd** cuando se completan las consultas a NLA permite liberar los recursos del sistema que ya no necesita NLA.

NLA admite los siguientes códigos de error para [**las llamadas de función WSALookupServiceEnd.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

| Error                | Significado                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED    | No se realizó una llamada correcta a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar NLA. |
| IDENTIFICADOR NO VÁLIDO DE WSA \_ \_ | El identificador proporcionado en el *parámetro hLookup* no era un identificador de SP de NLA válido.                             |



 

 

 



