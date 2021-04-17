---
description: PNRP usa la función WSANSPIoctl para recibir notificaciones acerca de los cambios realizados en lo siguiente.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP y WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36dc53fb3d00eeaa2b74be643a7ea62af436e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667390"
---
# <a name="pnrp-and-wsanspioctl"></a>PNRP y WSANSPIoctl

PNRP usa la función [**WSANSPIoctl**](winsock-nsp-reference-links.md) para recibir notificaciones acerca de los cambios realizados en lo siguiente:

-   Una lista de nubes de red
-   Disponibilidad de los resultados de una solicitud de resolución de nombres

La primera llamada a [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) define el tipo de información sobre el que se notifica a un cliente. Se puede notificar a un cliente con un mensaje de Windows, una rutina de finalización, un identificador de un objeto WSAEVENT o un puerto. Para obtener más información sobre las opciones y el establecimiento del parámetro *lpCompletion* , consulte **WSANSPIoctl**.

Para seguir recibiendo notificaciones después de una llamada a [**WSALookupServiceNext**](winsock-nsp-reference-links.md), una aplicación debe llamar de nuevo a **WSANSPIoctl** .

La función [**WSALookupServiceNext**](winsock-nsp-reference-links.md) se bloquea incluso si se llama a **WSANSPIoctl** . Antes de llamar a **WSALookupServiceNext**, una aplicación debe esperar hasta que reciba una notificación, si el bloqueo es un problema.

Cuando se llama a esta función, los parámetros deben tener los siguientes valores:

<dl> <dt>

<span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*VLOOKUP*
</dt> <dd>

Especifica el identificador que devuelve [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) .

</dd> <dt>

<span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*
</dt> <dd>

Debe ser **SiO \_ NSP \_ Notify \_ Change**.

</dd> <dt>

<span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*
</dt> <dd>

Debe ser **null**.

</dd> <dt>

<span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*
</dt> <dd>

Debe ser cero (0).

</dd> <dt>

<span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*
</dt> <dd>

Debe ser **null**.

</dd> <dt>

<span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*
</dt> <dd>

Debe ser cero (0).

</dd> <dt>

<span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*
</dt> <dd>

Debe ser **null**.

</dd> <dt>

<span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*
</dt> <dd>

Especifica **null** o un puntero a una estructura [**WSACOMPLETION**](winsock-nsp-reference-links.md) .

</dd> </dl>

Después de recibir una notificación, llame a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) una vez para obtener los resultados.

Para finalizar una búsqueda, llame a [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).

## <a name="resolution-notifications"></a>Notificaciones de resolución

Se puede notificar a un cliente cada vez que se agrega una entrada de resolución de nombres. Después, el cliente llama a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para obtener los datos de la resolución.

Si el cliente no usa esta técnica, puede bloquearse una llamada a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) hasta que se produzca el tiempo de espera especificado.

## <a name="cloud-list-notifications"></a>Notificaciones de lista de nube

Se puede notificar a un cliente en cualquier momento en que se produzca un cambio en un conjunto de nubes.

La función [**WSALookupServiceNext**](winsock-nsp-reference-links.md) devuelve **WSA \_ E \_ no \_ más** como delimitador de conjunto. La aplicación cliente debe enumerar las nubes existentes hasta que se devuelva este mensaje y, a continuación, utilizar un esquema de notificación para recuperar los cambios posteriores a medida que se producen. Una aplicación cliente también puede llamar a **WSALookupServiceNext**, pero la llamada se bloquea hasta que se produce un cambio.

La función [**WSALookupServiceNext**](winsock-nsp-reference-links.md) devuelve una nube en una estructura **WSAQUERYSET** . En el miembro **dwOutputFlags** se devuelve una de las marcas siguientes.



| Value               | Descripción                                             |
|---------------------|---------------------------------------------------------|
| \_se \_ agrega el resultado   | Se agrega la nube que se devuelve.                    |
| el \_ resultado \_ cambia | Se cambia la nube que se devuelve.                  |
| el resultado \_ se \_ elimina | La nube que se devuelve se elimina y no es válida. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[PNRP y WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[PNRP y WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP y WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[Códigos de error NSP de PNRP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSANSPIoctl**](winsock-nsp-reference-links.md)
</dt> <dt>

**WSALookupServiceBegin**
</dt> <dt>

**WSALookupServiceEnd**
</dt> <dt>

**WSAQUERYSET**
</dt> </dl>

 

 



