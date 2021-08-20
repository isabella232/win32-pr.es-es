---
description: NLA es capaz de proporcionar a sus clientes la notificación de los cambios de ubicación de red. El mecanismo que se usa para solicitar la notificación de eventos de cambio es una combinación de las funciones WSALookupServiceBegin, WSANSPIoctl y WSALookupServiceNext.
ms.assetid: fed5a90d-0bc5-46e7-b3d3-edc4b303d305
title: Notificación de NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8e7309fe6845d822702ffd81448999e2472ebdd37a6949812f622110ee9d42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822670"
---
# <a name="notification-from-nla"></a>Notificación de NLA

NLA es capaz de proporcionar a sus clientes la notificación de los cambios de ubicación de red. El mecanismo que se usa para solicitar la notificación de eventos de cambio es una combinación de las funciones [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl)y [**WSALookupServiceNext.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)

Para recibir una notificación de cambio de NLA, un cliente debe llamar primero a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para obtener un identificador de búsqueda de SP de NLA válido. A continuación, el cliente puede [**llamar a WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) o [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) en cualquier orden; Para registrarse para recibir notificaciones, llame a la función **WSANSPIoctl** con el código de control NOTIFY CHANGE de SIO NSP establecido en el \_ \_ parámetro \_ *dwControlCode.*

La [**función WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) devuelve WSA E NO MORE como delimitador \_ de \_ \_ conjunto. Cuando un cliente se ha registrado para la notificación mediante la función [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) y **WSALookupServiceNext** devuelve WSA E NO MORE, la llamada \_ a \_ \_ **WSALookupServiceNext** revela de nuevo si se ha producido un cambio:

-   Si no se ha producido ningún cambio desde el WSA E NO MORE anterior, se devuelve \_ \_ \_ WSA \_ E NO \_ \_ MORE.
-   Si se ha producido un cambio, o si se ha producido un cambio y se realiza una llamada de sondeo, la llamada de función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) devuelve redes como estructuras [**WSAQUERYSET,**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) con una de las marcas siguientes establecidas en su **miembro dwOutputFlags:**

    <dl> SE \_ AGREGA \_ RESULT  
    SE \_ CAMBIA EL \_ RESULTADO  
    SE \_ ELIMINA EL \_ RESULTADO.  
    </dl>

Se proporciona una notificación de cambio para todos los campos que han cambiado desde que el identificador de búsqueda de NLA se obtuvo con la llamada de función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) o desde la última enumeración que produjo el error WSA \_ E NO \_ \_ MORE. Cuando se proporciona toda la información de ubicación de red cambiada, se devuelve WSA \_ E \_ NO \_ MORE. Los clientes pueden volver a emitir una llamada de función [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) en el mismo identificador de consulta en cualquier momento, de uno en uno, con la marca SIO \_ NSP \_ NOTIFY CHANGE \_ establecida. Esta funcionalidad permite a un cliente reciclar el identificador de consulta de forma continua, lo que evita que el cliente tenga que mantener la información de estado de cambio por sí mismo. Una vez que un cliente ya no necesita notificaciones de cambio, debe cerrar el identificador de consulta mediante la [**función WSALookupServiceEnd.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

 

 



