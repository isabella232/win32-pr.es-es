---
title: Creación de un receptor de notificaciones
description: Creación de un receptor de notificaciones
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481cdd754e545ef87e3c0dc44324d46e48baf044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419115"
---
# <a name="creating-a-notification-sink"></a><span data-ttu-id="a2e83-103">Creación de un receptor de notificaciones</span><span class="sxs-lookup"><span data-stu-id="a2e83-103">Creating a Notification Sink</span></span>

<span data-ttu-id="a2e83-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a2e83-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a2e83-105">Para recibir notificaciones de eventos por el agente de Microsoft, debe implementar la interfaz [**IAgentNotifySink**](events.md)o [**IAgentNotifySinkEx**](iagentnotifysinkex.md) , y crear y registrar un objeto de ese tipo siguiendo las convenciones de com:</span><span class="sxs-lookup"><span data-stu-id="a2e83-105">To be notified of events by Microsoft Agent, you must implement either the [**IAgentNotifySink**](events.md)or the [**IAgentNotifySinkEx**](iagentnotifysinkex.md) interface, and create and register an object of that type following COM conventions:</span></span>


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



<span data-ttu-id="a2e83-106">Recuerde anular el registro del receptor de notificaciones cuando la aplicación se cierra y se liberan las interfaces de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a2e83-106">Remember to unregister your notification sink when your application shuts down and releases Microsoft Agent's interfaces.</span></span>

 

 




