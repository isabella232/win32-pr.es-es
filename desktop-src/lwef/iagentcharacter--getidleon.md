---
title: IAgentCharacter GetIdleOn
description: IAgentCharacter GetIdleOn
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdaf3ea460a76549112741ac77f83e10ec37cd9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780130"
---
# <a name="iagentcharactergetidleon"></a><span data-ttu-id="ec652-103">IAgentCharacter::GetIdleOn</span><span class="sxs-lookup"><span data-stu-id="ec652-103">IAgentCharacter::GetIdleOn</span></span>

<span data-ttu-id="ec652-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ec652-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

<span data-ttu-id="ec652-105">Indica el estado de procesamiento de inactividad automático para un carácter.</span><span class="sxs-lookup"><span data-stu-id="ec652-105">Indicates the automatic idle processing state for a character.</span></span>

-   <span data-ttu-id="ec652-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ec652-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ec652-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span><span class="sxs-lookup"><span data-stu-id="ec652-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="ec652-108">Dirección de una variable que recibe **true** si el servidor de agente de Microsoft reproduce automáticamente animaciones de estado de **ralentí** para un carácter y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ec652-108">Address of a variable that receives **True** if the Microsoft Agent server automatically plays **Idling** state animations for a character and **False** if not.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="ec652-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ec652-109">See Also</span></span>

[<span data-ttu-id="ec652-110">**IAgentCharacter::SetIdleOn**</span><span class="sxs-lookup"><span data-stu-id="ec652-110">**IAgentCharacter::SetIdleOn**</span></span>](iagentcharacter--setidleon.md)


 

 




