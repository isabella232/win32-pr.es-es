---
title: Registrando para la notificación de cambios
description: Un cliente puede registrarse para recibir notificaciones de cambios en la información de enrutamiento almacenada en el administrador de tablas de enrutamiento. Esta solicitud solo puede realizarse después de que un cliente se ha registrado con el administrador de tablas de enrutamiento.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3a98062fee73c481c1f47c32fa7eeb5465a112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357004"
---
# <a name="registering-for-change-notification"></a><span data-ttu-id="f51b4-104">Registrando para la notificación de cambios</span><span class="sxs-lookup"><span data-stu-id="f51b4-104">Registering for Change Notification</span></span>

<span data-ttu-id="f51b4-105">Un cliente puede registrarse para recibir notificaciones de cambios en la información de enrutamiento almacenada en el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="f51b4-105">A client can register to receive notification of changes to routing information that is stored in the routing table manager.</span></span> <span data-ttu-id="f51b4-106">Esta solicitud solo puede realizarse después de que un cliente se ha registrado con el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="f51b4-106">This request can only be made after a client has registered with the routing table manager.</span></span>

<span data-ttu-id="f51b4-107">Para registrar la notificación de cambios, un cliente debe llamar a [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), especificando los tipos de cambios para los que el cliente debe recibir la notificación.</span><span class="sxs-lookup"><span data-stu-id="f51b4-107">To register for change notification, a client must call [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), specifying the types of changes for which the client must receive notification.</span></span> <span data-ttu-id="f51b4-108">Si se debe notificar al cliente el cambio a destinos específicos, el cliente llama a [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) una vez para cada destino.</span><span class="sxs-lookup"><span data-stu-id="f51b4-108">If the client must be notified of change to specific destinations, the client calls [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) once for each destination.</span></span>

<span data-ttu-id="f51b4-109">El cliente puede dejar de recibir notificaciones de cambios mediante una llamada a [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).</span><span class="sxs-lookup"><span data-stu-id="f51b4-109">The client can stop receiving change notifications by calling [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).</span></span>

<span data-ttu-id="f51b4-110">Para ver el código de ejemplo que muestra cómo usar estas funciones, consulte [registrar para la notificación de cambios](register-for-change-notification.md).</span><span class="sxs-lookup"><span data-stu-id="f51b4-110">For sample code that shows how to use these functions, see [Register For Change Notification](register-for-change-notification.md).</span></span>

 

 




