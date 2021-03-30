---
title: IAgentBalloon GetVisible
description: IAgentBalloon GetVisible
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55fd8dbf6792d34b15f82ab6c402e9a0e7eb3ad3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903839"
---
# <a name="iagentballoongetvisible"></a><span data-ttu-id="62ebd-103">IAgentBalloon:: GetVisible</span><span class="sxs-lookup"><span data-stu-id="62ebd-103">IAgentBalloon::GetVisible</span></span>

<span data-ttu-id="62ebd-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="62ebd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

<span data-ttu-id="62ebd-105">Determina si el globo de palabras está visible u oculto.</span><span class="sxs-lookup"><span data-stu-id="62ebd-105">Determines whether the word balloon is visible or hidden.</span></span>

-   <span data-ttu-id="62ebd-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="62ebd-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="62ebd-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="62ebd-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="62ebd-108">Dirección de una variable que recibe **true** si el globo de palabras está visible y **false** si está oculto.</span><span class="sxs-lookup"><span data-stu-id="62ebd-108">Address of a variable that receives **True** if the word balloon is visible and **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="62ebd-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="62ebd-109">See Also</span></span>

[<span data-ttu-id="62ebd-110">**IAgentBalloon:: SetVisible**</span><span class="sxs-lookup"><span data-stu-id="62ebd-110">**IAgentBalloon::SetVisible**</span></span>](iagentballoon--setvisible.md)


 

 




