---
title: IAgentCharacter GetPosition
description: IAgentCharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357793"
---
# <a name="iagentcharactergetposition"></a><span data-ttu-id="affcc-103">IAgentCharacter:: GetPosition</span><span class="sxs-lookup"><span data-stu-id="affcc-103">IAgentCharacter::GetPosition</span></span>

<span data-ttu-id="affcc-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="affcc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

<span data-ttu-id="affcc-105">Recupera la posición del marco de animación del carácter.</span><span class="sxs-lookup"><span data-stu-id="affcc-105">Retrieves the character's animation frame position.</span></span>

-   <span data-ttu-id="affcc-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="affcc-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="affcc-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="affcc-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="affcc-108">Dirección de una variable que recibe la coordenada de pantalla del borde izquierdo del marco de la animación de caracteres, en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="affcc-108">Address of a variable that receives the screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="affcc-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="affcc-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="affcc-110">Dirección de una variable que recibe la coordenada de pantalla del borde superior del fotograma de la animación de caracteres en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="affcc-110">Address of a variable that receives the screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="affcc-111">Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en el marco de la animación rectangular.</span><span class="sxs-lookup"><span data-stu-id="affcc-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="affcc-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="affcc-112">See Also</span></span>

<span data-ttu-id="affcc-113">[**IAgentCharacter:: SetPosition**](iagentcharacter--setposition.md), [ **IAgentCharacter:: se obtiene**](iagentcharacter--getsize.md)</span><span class="sxs-lookup"><span data-stu-id="affcc-113">[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md), [**IAgentCharacter::GetSize**](iagentcharacter--getsize.md)</span></span>


 

 




