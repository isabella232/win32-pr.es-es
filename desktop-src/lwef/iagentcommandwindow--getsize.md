---
title: IAgentCommandWindow se obtiene
description: IAgentCommandWindow se obtiene
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cf42d98f811905590209b6fed70b28a5728903
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714193"
---
# <a name="iagentcommandwindowgetsize"></a><span data-ttu-id="e5871-103">IAgentCommandWindow:: obtiene</span><span class="sxs-lookup"><span data-stu-id="e5871-103">IAgentCommandWindow::GetSize</span></span>

<span data-ttu-id="e5871-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e5871-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

<span data-ttu-id="e5871-105">Recupera el tamaño actual de la ventana comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="e5871-105">Retrieves the current size of the Voice Commands Window.</span></span>

-   <span data-ttu-id="e5871-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e5871-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e5871-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="e5871-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="e5871-108">Dirección de una variable que recibe el ancho de la ventana comandos de voz en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="e5871-108">Address of a variable that receives the width of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="e5871-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="e5871-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="e5871-110">Dirección de una variable que recibe el alto de la ventana comandos de voz en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="e5871-110">Address of a variable that receives the height of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="e5871-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e5871-111">See Also</span></span>

[<span data-ttu-id="e5871-112">**IAgentCommandWindow:: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="e5871-112">**IAgentCommandWindow::GetPosition**</span></span>](iagentcommandwindow--getposition.md)


 

 




