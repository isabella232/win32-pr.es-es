---
description: La introducción de E/S superpuesta requiere un mecanismo para que las aplicaciones asocien de forma inequívoca las solicitudes de envío y recepción con sus indicaciones de finalización posteriores.
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: Objetos de evento (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34820d7df92704d86f7dbdc100816789488426e2fdd553456be94da921811c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132598"
---
# <a name="event-objects-windows-sockets-2"></a>Objetos de evento (Windows Sockets 2)

La introducción de E/S superpuesta requiere un mecanismo para que las aplicaciones asocien de forma inequívoca las solicitudes de envío y recepción con sus indicaciones de finalización posteriores. En Windows Sockets 2, esto se logra con objetos de evento que se modela después de Windows eventos. Windows Los objetos de evento sockets son construcciones bastante sencillas que se pueden crear y cerrar, establecer y borrar, y esperar y sondear. Su utilidad principal es la capacidad de una aplicación de bloquear y esperar hasta que se establezcan uno o varios objetos de evento.

Las aplicaciones usan [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) para obtener un identificador de objeto de evento que luego se puede proporcionar como parámetro necesario a las versiones superpuestas de las llamadas de envío y recepción ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)). Los proveedores de transporte establecen el objeto de evento, que se borra cuando se crea por primera vez, cuando se ha completado la operación de E/S superpuesta asociada (ya sea correctamente o con errores). Cada objeto de evento creado **por WSACreateEvent** debe tener un [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) correspondiente para destruirlo.

Los objetos de evento también se usan [**en WSAEventSelect para**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) asociar uno o varios eventos de red \_ FD XXX a un objeto de evento. Esto se describe en [Notificación asincrónica mediante objetos de evento](asynchronous-notification-using-event-objects-2.md).

En entornos de 32 bits, las funciones relacionadas con objetos de evento, incluidas [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent,**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) [**WSASetEvent,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent) [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)y [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) se asignan directamente a las funciones Windows nativas correspondientes, con el mismo nombre de función, pero sin el prefijo WSA.

 

 



