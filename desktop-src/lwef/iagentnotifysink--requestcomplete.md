---
title: IAgentNotifySink RequestComplete
description: IAgentNotifySink RequestComplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357603"
---
# <a name="iagentnotifysinkrequestcomplete"></a><span data-ttu-id="ddd7b-103">IAgentNotifySink::RequestComplete</span><span class="sxs-lookup"><span data-stu-id="ddd7b-103">IAgentNotifySink::RequestComplete</span></span>

<span data-ttu-id="ddd7b-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ddd7b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

<span data-ttu-id="ddd7b-105">Notifica a una aplicación cliente cuando se completa una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ddd7b-105">Notifies a client application when a request completes.</span></span>

-   <span data-ttu-id="ddd7b-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ddd7b-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="ddd7b-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span><span class="sxs-lookup"><span data-stu-id="ddd7b-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="ddd7b-108">Identificador de la solicitud iniciada.</span><span class="sxs-lookup"><span data-stu-id="ddd7b-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="ddd7b-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span><span class="sxs-lookup"><span data-stu-id="ddd7b-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span></span>
</dt> <dd>

<span data-ttu-id="ddd7b-110">Código de estado.</span><span class="sxs-lookup"><span data-stu-id="ddd7b-110">Status code.</span></span> <span data-ttu-id="ddd7b-111">Este parámetro devuelve el código de estado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ddd7b-111">This parameter returns the status code for the request.</span></span>

</dd> </dl>

<span data-ttu-id="ddd7b-112">Este evento le permite realizar un seguimiento de Cuándo se completa un método en cola mediante su identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="ddd7b-112">This event enables you to track when a queued method completes using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="ddd7b-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ddd7b-113">See Also</span></span>

<span data-ttu-id="ddd7b-114">[**IAgentNotifySink:: RequestStart**](iagentnotifysink--requeststart.md), [**IAgent:: Load**](iagent--load.md), [**IAgentCharacter:: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter:: Hide**](iagentcharacter--hide.md), [**IAgentCharacter:: Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter:: moveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::P reparer**](iagentcharacter--prepare.md), [**IAgentCharacter::P**](iagentcharacter--play.md)poner, [**IAgentCharacter:: show**](iagentcharacter--show.md), [**IAgentCharacter:: Speak**](iagentcharacter--speak.md), [**IAgentCharacter:: wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="ddd7b-114">[**IAgentNotifySink::RequestStart**](iagentnotifysink--requeststart.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 




