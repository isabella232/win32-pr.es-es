---
title: IAgentNotifySink inactivo
description: IAgentNotifySink inactivo
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704775"
---
# <a name="iagentnotifysinkidle"></a><span data-ttu-id="2eabc-103">IAgentNotifySink:: idle</span><span class="sxs-lookup"><span data-stu-id="2eabc-103">IAgentNotifySink::Idle</span></span>

<span data-ttu-id="2eabc-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2eabc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

<span data-ttu-id="2eabc-105">Notifica a una aplicación cliente cuando ha cambiado el estado de **ralentí** de un carácter.</span><span class="sxs-lookup"><span data-stu-id="2eabc-105">Notifies a client application when a character's **Idling** state has changed.</span></span>

-   <span data-ttu-id="2eabc-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2eabc-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="2eabc-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="2eabc-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="2eabc-108">Identificador de la solicitud iniciada.</span><span class="sxs-lookup"><span data-stu-id="2eabc-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="2eabc-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bInicio*</span><span class="sxs-lookup"><span data-stu-id="2eabc-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*</span></span>
</dt> <dd>

<span data-ttu-id="2eabc-110">Marca de inicio.</span><span class="sxs-lookup"><span data-stu-id="2eabc-110">Start flag.</span></span> <span data-ttu-id="2eabc-111">Este valor booleano es **true** cuando el carácter comienza a ralentí y **false** cuando detiene el ralentí.</span><span class="sxs-lookup"><span data-stu-id="2eabc-111">This Boolean value is **True** when the character begins idling and **False** when it stops idling.</span></span>

</dd> </dl>

<span data-ttu-id="2eabc-112">Este evento le permite realizar un seguimiento cuando el servidor de agente de Microsoft inicia o detiene el procesamiento inactivo de un carácter.</span><span class="sxs-lookup"><span data-stu-id="2eabc-112">This event enables you to track when the Microsoft Agent server starts or stops idle processing for a character.</span></span>

## <a name="see-also"></a><span data-ttu-id="2eabc-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2eabc-113">See Also</span></span>

<span data-ttu-id="2eabc-114">[**IAgentCharacter:: GetIdleOn**](iagentcharacter--getidleon.md), [ **IAgentCharacter:: SetIdleOn**](iagentcharacter--setidleon.md)</span><span class="sxs-lookup"><span data-stu-id="2eabc-114">[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md), [**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)</span></span>


 

 




