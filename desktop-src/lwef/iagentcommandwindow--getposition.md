---
title: IAgentCommandWindow GetPosition
description: IAgentCommandWindow GetPosition
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c036d02c210ecb26da5dfde207bfe56afe8a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994314"
---
# <a name="iagentcommandwindowgetposition"></a><span data-ttu-id="fd02c-103">IAgentCommandWindow:: GetPosition</span><span class="sxs-lookup"><span data-stu-id="fd02c-103">IAgentCommandWindow::GetPosition</span></span>

<span data-ttu-id="fd02c-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fd02c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

<span data-ttu-id="fd02c-105">Recupera la posición de la ventana comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="fd02c-105">Retrieves the Voice Commands Window's position.</span></span>

-   <span data-ttu-id="fd02c-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fd02c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fd02c-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="fd02c-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="fd02c-108">Dirección de una variable que recibe la coordenada de pantalla del borde izquierdo de la ventana comandos de voz en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="fd02c-108">Address of a variable that receives the screen coordinate of the left edge of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="fd02c-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="fd02c-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="fd02c-110">Dirección de una variable que recibe la coordenada de pantalla del borde superior de la ventana comandos de voz en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="fd02c-110">Address of a variable that receives the screen coordinate of the top edge of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="fd02c-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fd02c-111">See Also</span></span>

[<span data-ttu-id="fd02c-112">**IAgentCommandWindow:: obtiene**</span><span class="sxs-lookup"><span data-stu-id="fd02c-112">**IAgentCommandWindow::GetSize**</span></span>](iagentcommandwindow--getsize.md)


 

 




