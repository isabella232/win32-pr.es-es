---
title: IAgentNotifySink RequestStart
description: IAgentNotifySink RequestStart
ms.assetid: acac2bf8-7472-4952-a984-a29654fb8b0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ced12596114214cf712cef8dbbe81edb5af278
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779158"
---
# <a name="iagentnotifysinkrequeststart"></a><span data-ttu-id="976b5-103">IAgentNotifySink::RequestStart</span><span class="sxs-lookup"><span data-stu-id="976b5-103">IAgentNotifySink::RequestStart</span></span>

<span data-ttu-id="976b5-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="976b5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestStart(
   long dwRequestID  // request ID
);                          
```

<span data-ttu-id="976b5-105">Notifica a una aplicación cliente cuando se inicia una solicitud.</span><span class="sxs-lookup"><span data-stu-id="976b5-105">Notifies a client application when a request begins.</span></span>

-   <span data-ttu-id="976b5-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="976b5-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="976b5-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span><span class="sxs-lookup"><span data-stu-id="976b5-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="976b5-108">Identificador de la solicitud iniciada.</span><span class="sxs-lookup"><span data-stu-id="976b5-108">Identifier of the request that started.</span></span>

</dd> </dl>

<span data-ttu-id="976b5-109">Este evento le permite realizar un seguimiento cuando una solicitud en cola comienza a usar su identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="976b5-109">This event enables you to track when a queued request begins using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="976b5-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="976b5-110">See Also</span></span>

<span data-ttu-id="976b5-111">[**IAgentNotifySink:: RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent:: Load**](iagent--load.md), [**IAgentCharacter:: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter:: Hide**](iagentcharacter--hide.md), [**IAgentCharacter:: Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter:: moveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::P reparer**](iagentcharacter--prepare.md), [**IAgentCharacter::P**](iagentcharacter--play.md)poner, [**IAgentCharacter:: show**](iagentcharacter--show.md), [**IAgentCharacter:: Speak**](iagentcharacter--speak.md), [**IAgentCharacter:: wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="976b5-111">[**IAgentNotifySink::RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 




