---
description: La introducción de e/s superpuestas requiere un mecanismo para que las aplicaciones asocien de forma inequívoca las solicitudes de envío y recepción con las siguientes indicaciones de finalización.
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: Objetos de eventos (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72b60442f9c56ae2c8e9af905bd14b6536b8e10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360303"
---
# <a name="event-objects-windows-sockets-2"></a>Objetos de eventos (Windows Sockets 2)

La introducción de e/s superpuestas requiere un mecanismo para que las aplicaciones asocien de forma inequívoca las solicitudes de envío y recepción con las siguientes indicaciones de finalización. En Windows Sockets 2, esto se logra con los objetos de evento que se modelan después de los eventos de Windows. Los objetos de evento de Windows Sockets son construcciones bastante simples que se pueden crear y cerrar, establecer y borrar, y se han esperado y sondeado. Su utilidad Prime es la capacidad de una aplicación para bloquearse y esperar a que se establezcan uno o varios objetos de evento.

Las aplicaciones usan [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) para obtener un identificador de objeto de evento que, a continuación, se puede proporcionar como un parámetro necesario a las versiones superpuestas de las llamadas de envío y recepción ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)). Los proveedores de transporte establecen el objeto de evento, que se borra cuando se crea por primera vez, cuando se completa la operación de e/s superpuestas asociada (ya sea correctamente o con errores). Cada objeto de evento creado por **WSACreateEvent** debe tener un [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) correspondiente para destruirlo.

Los objetos de evento también se usan en [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) para asociar uno o más \_ eventos de red FD xxx con un objeto de evento. Esto se describe en [notificación asincrónica mediante objetos de evento](asynchronous-notification-using-event-objects-2.md).

En los entornos de 32 bits, las funciones relacionadas con los objetos de eventos, como [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)y [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) , se asignan directamente a las funciones nativas de Windows correspondientes con el mismo nombre de función, pero sin el prefijo WSA.

 

 



