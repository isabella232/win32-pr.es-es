---
title: IAgentPropertySheet se obtiene
description: IAgentPropertySheet se obtiene
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704668"
---
# <a name="iagentpropertysheetgetsize"></a><span data-ttu-id="38ee6-103">IAgentPropertySheet:: obtiene</span><span class="sxs-lookup"><span data-stu-id="38ee6-103">IAgentPropertySheet::GetSize</span></span>

<span data-ttu-id="38ee6-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="38ee6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

<span data-ttu-id="38ee6-105">Recupera el tamaño de la ventana de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="38ee6-105">Retrieves the size of the Microsoft Agent property sheet window.</span></span>

-   <span data-ttu-id="38ee6-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="38ee6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="38ee6-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="38ee6-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="38ee6-108">Dirección de una variable que recibe el ancho de la hoja de propiedades en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="38ee6-108">Address of a variable that receives the width of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="38ee6-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="38ee6-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="38ee6-110">Dirección de una variable que recibe el alto de la hoja de propiedades en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="38ee6-110">Address of a variable that receives the height of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="38ee6-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="38ee6-111">See Also</span></span>

[<span data-ttu-id="38ee6-112">**IAgentPropertySheet:: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="38ee6-112">**IAgentPropertySheet::GetPosition**</span></span>](iagentpropertysheet--getposition.md)


 

 




