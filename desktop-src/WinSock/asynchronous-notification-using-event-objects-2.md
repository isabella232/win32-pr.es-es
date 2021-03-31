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
# <a name="asynchronous-notification-using-event-objects"></a><span data-ttu-id="570ce-103">Notificación asincrónica mediante objetos de eventos</span><span class="sxs-lookup"><span data-stu-id="570ce-103">Asynchronous Notification Using Event Objects</span></span>

<span data-ttu-id="570ce-104">Las funciones [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) y [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) se proporcionan para dar cabida a aplicaciones como demonios y servicios que no tienen ninguna interfaz de usuario (y, por tanto, no usan identificadores de Windows).</span><span class="sxs-lookup"><span data-stu-id="570ce-104">The [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) and [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) functions are provided to accommodate applications such as daemons and services that have no user interface (and hence do not use Windows handles).</span></span> <span data-ttu-id="570ce-105">La función **WSAEventSelect** se comporta exactamente igual que la función [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) .</span><span class="sxs-lookup"><span data-stu-id="570ce-105">The **WSAEventSelect** function behaves exactly like the [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) function.</span></span> <span data-ttu-id="570ce-106">Sin embargo, en lugar de hacer que se envíe un mensaje de Windows en caso de que se produzca un \_ evento de red FD xxx (por ejemplo, FD \_ Read y FD de \_ escritura), se establece un objeto de evento designado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="570ce-106">However, instead of causing a Windows message to be sent on the occurrence of an FD\_XXX network event (for example, FD\_READ and FD\_WRITE), an application-designated event object is set.</span></span>

<span data-ttu-id="570ce-107">Además, el proveedor de servicios recuerda el hecho de que se \_ ha producido un evento de red FD XXX determinado.</span><span class="sxs-lookup"><span data-stu-id="570ce-107">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="570ce-108">La aplicación puede llamar a [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) para que el contenido actual de la memoria de eventos de red se copie en un búfer proporcionado por la aplicación y para que la memoria de eventos de red se borre automáticamente.</span><span class="sxs-lookup"><span data-stu-id="570ce-108">The application can call [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) to have the current contents of the network event memory copied to an application-supplied buffer and to have the network event memory automatically cleared.</span></span> <span data-ttu-id="570ce-109">Si es necesario, la aplicación también puede designar un objeto de evento determinado que se borra junto con la memoria de eventos de red.</span><span class="sxs-lookup"><span data-stu-id="570ce-109">If needed, the application can also designate a particular event object that is cleared along with the network event memory.</span></span>

 

 



