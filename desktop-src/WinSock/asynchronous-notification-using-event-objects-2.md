---
description: Las funciones WSAEventSelect y WSAEnumNetworkEvents se proporcionan para dar cabida a aplicaciones como demonios y servicios que no tienen ninguna interfaz de usuario (y, por tanto, no usan identificadores de Windows).
ms.assetid: 4254937c-7ee6-49a3-9f30-09aebaf2265b
title: Notificación asincrónica mediante objetos de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0495507eacf0960dc98f31594d7f4881d51488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907961"
---
# <a name="asynchronous-notification-using-event-objects"></a>Notificación asincrónica mediante objetos de eventos

Las funciones [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) y [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) se proporcionan para dar cabida a aplicaciones como demonios y servicios que no tienen ninguna interfaz de usuario (y, por tanto, no usan identificadores de Windows). La función **WSAEventSelect** se comporta exactamente igual que la función [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) . Sin embargo, en lugar de hacer que se envíe un mensaje de Windows en caso de que se produzca un \_ evento de red FD xxx (por ejemplo, FD \_ Read y FD de \_ escritura), se establece un objeto de evento designado por la aplicación.

Además, el proveedor de servicios recuerda el hecho de que se \_ ha producido un evento de red FD XXX determinado. La aplicación puede llamar a [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) para que el contenido actual de la memoria de eventos de red se copie en un búfer proporcionado por la aplicación y para que la memoria de eventos de red se borre automáticamente. Si es necesario, la aplicación también puede designar un objeto de evento determinado que se borra junto con la memoria de eventos de red.

 

 



