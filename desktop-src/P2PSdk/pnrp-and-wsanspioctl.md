---
description: PNRP usa la función WSANSPIoctl para recibir notificaciones sobre los cambios realizados a continuación.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP y WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cc07415fb483e75af8d836274d45a2c53f205e3aae15f893f909d2363c0d15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553315"
---
# <a name="pnrp-and-wsanspioctl"></a>PNRP y WSANSPIoctl

PNRP usa la [**función WSANSPIoctl**](winsock-nsp-reference-links.md) para recibir notificaciones sobre los cambios en lo siguiente:

-   Una lista de nube de red
-   Disponibilidad de los resultados de una solicitud de resolución de nombres

La primera llamada a [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) define el tipo de información sobre la que se notifica a un cliente. Se puede notificar a un cliente con un mensaje Windows, una rutina de finalización, un identificador para un objeto WSAEVENT o un puerto. Para obtener más información sobre las opciones y establecer *el parámetro lpCompletion,* vea **WSANSPIoctl**.

Para seguir recibiendo notificaciones después de una llamada a [**WSALookupServiceNext,**](winsock-nsp-reference-links.md)una aplicación debe llamar de nuevo a **WSANSPIoctl.**

La [**función WSALookupServiceNext se**](winsock-nsp-reference-links.md) bloquea incluso si se llama a **WSANSPIoctl.** Antes de llamar a **WSALookupServiceNext,** una aplicación debe esperar hasta que reciba una notificación, si el bloqueo es un problema.

Al llamar a esta función, los parámetros deben tener los siguientes valores:

<dl> <dt>

<span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*
</dt> <dd>

Especifica el identificador que [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) devuelve.

</dd> <dt>

<span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*
</dt> <dd>

Debe ser **SIO \_ NSP \_ NOTIFY \_ CHANGE**.

</dd> <dt>

<span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*
</dt> <dd>

Debe ser **NULL.**

</dd> <dt>

<span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*
</dt> <dd>

Debe ser cero (0).

</dd> <dt>

<span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*
</dt> <dd>

Debe ser **NULL.**

</dd> <dt>

<span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*
</dt> <dd>

Debe ser cero (0).

</dd> <dt>

<span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*
</dt> <dd>

Debe ser **NULL.**

</dd> <dt>

<span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*
</dt> <dd>

Especifica NULL **o** un puntero a una [**estructura WSACOMPLETION.**](winsock-nsp-reference-links.md)

</dd> </dl>

Después de recibir una notificación, llame a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) una vez para obtener los resultados.

Para finalizar una búsqueda, llame a [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).

## <a name="resolution-notifications"></a>Notificaciones de resolución

Se puede notificar a un cliente cada vez que se agrega una entrada de resolución de nombres. A continuación, el [**cliente llama a WSALookupServiceNext**](winsock-nsp-reference-links.md) para obtener los datos de resolución.

Si el cliente no usa esta técnica, se puede bloquear una llamada a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) hasta que se agote el tiempo de espera especificado.

## <a name="cloud-list-notifications"></a>Notificaciones de lista de nube

Se puede notificar a un cliente cada vez que se cambie un conjunto de nubes.

La [**función WSALookupServiceNext**](winsock-nsp-reference-links.md) devuelve **WSA \_ E NO \_ \_ MORE** como delimitador de conjunto. La aplicación cliente debe enumerar las nubes existentes hasta que se devuelva este mensaje y, a continuación, usar un esquema de notificación para recuperar los cambios posteriores a medida que se producen. Una aplicación cliente también puede llamar a **WSALookupServiceNext,** pero la llamada se bloquea hasta que se produce un cambio.

La [**función WSALookupServiceNext**](winsock-nsp-reference-links.md) devuelve una nube en una **estructura WSAQUERYSET.** Se devuelve una de las marcas siguientes en el **miembro dwOutputFlags.**



| Valor               | Descripción                                             |
|---------------------|---------------------------------------------------------|
| SE \_ AGREGA \_ RESULT   | Se agrega la nube que se devuelve.                    |
| SE \_ CAMBIA EL \_ RESULTADO | La nube que se devuelve cambia.                  |
| SE \_ ELIMINA EL \_ RESULTADO. | La nube que se devuelve se elimina y no es válida. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[PNRP y WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[PNRP y WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP y WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[Códigos de error de PNRP NSP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSANSPIoctl**](winsock-nsp-reference-links.md)
</dt> <dt>

**WSALookupServiceBegin**
</dt> <dt>

**WSALookupServiceEnd**
</dt> <dt>

**WSAQUERYSET**
</dt> </dl>

 

 



