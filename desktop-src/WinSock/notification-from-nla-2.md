---
description: NLA es capaz de proporcionar a sus clientes notificaciones de cambios de ubicación de red. El mecanismo usado para solicitar la notificación de eventos de cambio es una combinación de las funciones WSALookupServiceBegin, WSANSPIoctl y WSALookupServiceNext.
ms.assetid: fed5a90d-0bc5-46e7-b3d3-edc4b303d305
title: Notificación de NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ee0ad0530725db27c8f5df39b6fc573f7e97c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541526"
---
# <a name="notification-from-nla"></a>Notificación de NLA

NLA es capaz de proporcionar a sus clientes notificaciones de cambios de ubicación de red. El mecanismo usado para solicitar la notificación de eventos de cambio es una combinación de las funciones [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl)y [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) .

Para recibir la notificación de cambios de NLA, un cliente debe llamar primero a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para obtener un identificador de búsqueda de SP de NLA válido. A continuación, el cliente puede llamar a [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) o [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) en cualquier orden; para registrarse para recibir notificaciones, llame a la función **WSANSPIoctl** con el código de control de cambio de notificación SiO \_ NSP \_ \_ en el parámetro *dwControlCode* .

La función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) devuelve WSA \_ E \_ no \_ más como delimitador de conjunto. Cuando un cliente se ha registrado para recibir notificaciones mediante la función [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) y **WSALookupServiceNext** devuelve WSA \_ E \_ no \_ más, al llamar a **WSALookupServiceNext** se revela de nuevo si se ha producido un cambio:

-   Si no se ha producido ningún cambio desde el anterior WSA \_ e \_ no \_ más \_ , \_ se devuelve WSA e no \_ más.
-   Si se ha producido un cambio, o si se ha producido un cambio y se realiza una llamada de sondeo, la llamada a la función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) devuelve redes como estructuras [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , con una de las siguientes marcas establecidas en su miembro **dwOutputFlags** :

    <dl> \_se \_ agrega el resultado  
    el \_ resultado \_ cambia  
    el resultado \_ se \_ elimina  
    </dl>

Se proporciona una notificación de cambios para todos los campos que han cambiado desde que se obtuvo el identificador de búsqueda NLA con la llamada de función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) , o desde la última enumeración que dio como resultado el error de WSA \_ E \_ \_ . Cuando se proporciona toda la información de ubicación de red modificada, \_ \_ se devuelve WSA E no \_ más. Los clientes pueden volver a emitir una llamada de función [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) en el mismo identificador de consulta en cualquier momento, de una en una, con el \_ indicador de cambio de notificación SiO NSP \_ \_ establecido. Esta funcionalidad permite a un cliente reciclar el identificador de consulta de manera continua, lo que evita que el cliente tenga que mantener la información de estado de cambio por sí misma. Una vez que un cliente ya no necesita notificaciones de cambio, debe cerrar el identificador de consulta mediante la función [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .

 

 



