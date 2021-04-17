---
title: IAgentPropertySheet GetPosition
description: IAgentPropertySheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704669"
---
# <a name="iagentpropertysheetgetposition"></a><span data-ttu-id="67d3c-103">IAgentPropertySheet:: GetPosition</span><span class="sxs-lookup"><span data-stu-id="67d3c-103">IAgentPropertySheet::GetPosition</span></span>

<span data-ttu-id="67d3c-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="67d3c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

<span data-ttu-id="67d3c-105">Recupera la posición de la ventana de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="67d3c-105">Retrieves the Microsoft Agent's property sheet window position.</span></span>

-   <span data-ttu-id="67d3c-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="67d3c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="67d3c-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="67d3c-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="67d3c-108">Dirección de una variable que recibe la coordenada de pantalla del borde izquierdo de la hoja de propiedades en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="67d3c-108">Address of a variable that receives the screen coordinate of the left edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="67d3c-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="67d3c-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="67d3c-110">Dirección de una variable que recibe la coordenada de pantalla del borde superior de la hoja de propiedades en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="67d3c-110">Address of a variable that receives the screen coordinate of the top edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="67d3c-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="67d3c-111">See Also</span></span>

[<span data-ttu-id="67d3c-112">**IAgentPropertySheet:: obtiene**</span><span class="sxs-lookup"><span data-stu-id="67d3c-112">**IAgentPropertySheet::GetSize**</span></span>](iagentpropertysheet--getsize.md)


 

 




