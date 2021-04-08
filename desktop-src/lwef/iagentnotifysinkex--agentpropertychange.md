---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e27fe9e2318af0642c2df680af3a279ab57253d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994239"
---
# <a name="iagentnotifysinkexagentpropertychange"></a><span data-ttu-id="190f0-103">IAgentNotifySinkEx::AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="190f0-103">IAgentNotifySinkEx::AgentPropertyChange</span></span>

<span data-ttu-id="190f0-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="190f0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT AgentPropertyChange(
);
```

<span data-ttu-id="190f0-105">Notifica a una aplicación cliente cuando el usuario cambia la configuración de la propiedad de un agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="190f0-105">Notifies a client application when the user changes a Microsoft Agent property setting.</span></span>

-   <span data-ttu-id="190f0-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="190f0-106">No return value.</span></span>

<span data-ttu-id="190f0-107">Cuando el usuario cambia la configuración de una propiedad de agente de Microsoft en la hoja de propiedades del agente de Microsoft, el servidor envía este evento a todos los clientes a menos que el servidor esté suspendido actualmente.</span><span class="sxs-lookup"><span data-stu-id="190f0-107">When the user changes a Microsoft Agent property setting in the Microsoft Agent property sheet, the server sends this event to all clients unless the server is currently suspended.</span></span>

## <a name="see-also"></a><span data-ttu-id="190f0-108">Consulte también</span><span class="sxs-lookup"><span data-stu-id="190f0-108">See Also</span></span>

[<span data-ttu-id="190f0-109">**IAgentNotifySinkEx::D efaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="190f0-109">**IAgentNotifySinkEx::DefaultCharacterChange**</span></span>](iagentnotifysinkex--defaultcharacterchange.md)


 

 




