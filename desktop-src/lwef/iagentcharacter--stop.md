---
title: IAgentCharacter detener
description: IAgentCharacter detener
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356c81996a9410eccb2007dc5261913e30a1b414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418956"
---
# <a name="iagentcharacterstop"></a><span data-ttu-id="df25e-103">IAgentCharacter:: Stop</span><span class="sxs-lookup"><span data-stu-id="df25e-103">IAgentCharacter::Stop</span></span>

<span data-ttu-id="df25e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="df25e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

<span data-ttu-id="df25e-105">Detiene la animación especificada (solicitud) y la quita de la cola de animaciones del carácter.</span><span class="sxs-lookup"><span data-stu-id="df25e-105">Stops the specified animation (request) and removes it from the character's animation queue.</span></span>

-   <span data-ttu-id="df25e-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="df25e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="df25e-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="df25e-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="df25e-108">IDENTIFICADOR de la solicitud que se va a detener.</span><span class="sxs-lookup"><span data-stu-id="df25e-108">The ID of the request to stop.</span></span>

</dd> </dl>

<span data-ttu-id="df25e-109">**Detener** también puede usarse para detener cualquier llamada de [**preparación**](iagentcharacter--prepare.md) en cola.</span><span class="sxs-lookup"><span data-stu-id="df25e-109">**Stop** can also be used to halt any queued [**Prepare**](iagentcharacter--prepare.md) calls.</span></span>

## <a name="see-also"></a><span data-ttu-id="df25e-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="df25e-110">See Also</span></span>

<span data-ttu-id="df25e-111">[**IAgentCharacter::P reparer**](iagentcharacter--prepare.md), [ **IAgentCharacter:: stopAll**](iagentcharacter--stopall.md)</span><span class="sxs-lookup"><span data-stu-id="df25e-111">[**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md)</span></span>


 

 




