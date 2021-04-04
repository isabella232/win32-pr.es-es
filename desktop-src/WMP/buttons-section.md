---
title: Sección botones
description: Sección botones
ms.assetid: fa413bb4-e04a-4e3d-9754-cd4c2d82de6e
keywords:
- Aspectos de Windows Media Player Mobile, sección de botones
- aspectos, sección de botones
- crear máscaras, sección de botones
- escribir código para máscaras, sección de botones
- botones en máscaras, sección botones
- archivos de definición de máscara, sección de botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f994225154e3f4cc55070351c32c654d5ad616c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075942"
---
# <a name="buttons-section"></a><span data-ttu-id="5cc9d-109">Sección botones</span><span class="sxs-lookup"><span data-stu-id="5cc9d-109">Buttons Section</span></span>

<span data-ttu-id="5cc9d-110">A continuación, debe definir los botones que se van a usar:</span><span class="sxs-lookup"><span data-stu-id="5cc9d-110">Next, you must define the buttons you will be using:</span></span>


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   100,20,110,100 Pushed @ 100,20   Disabled @ 100,20    0,255,255  Pushed @ 270,20     Pushed @ 270,130
    Stop       PushHit    20,20,45,45    Pushed @ 20,20    Disabled @ 20,20   255,255,  0
    Next       PushHit    20,80,45,45    Pushed @ 20,80    Disabled @ 20,80   255,  0,  0
    Prev       PushHit    20,140,45,45   Pushed @ 20,140   Disabled @ 20,130    0,  0,255

```



<span data-ttu-id="5cc9d-111">En esta sección se definen cuatro botones.</span><span class="sxs-lookup"><span data-stu-id="5cc9d-111">There are four buttons defined in this section.</span></span> <span data-ttu-id="5cc9d-112">La página que está viendo puede ajustar estas líneas, pero cuando escribe en el código, no debe ajustar las líneas; es decir, cada línea debe estar completa y terminar con una marca de párrafo.</span><span class="sxs-lookup"><span data-stu-id="5cc9d-112">The page you are viewing may wrap these lines, but when you type in the code, you must not wrap lines; that is, each line must be complete and end with a paragraph mark.</span></span>

> [!Note]  
> <span data-ttu-id="5cc9d-113">Los tipos de botones están desusados en las máscaras de Windows Media Player 10 Mobile o posterior.</span><span class="sxs-lookup"><span data-stu-id="5cc9d-113">Buttons types are deprecated in Windows Media Player 10 Mobile or later skins.</span></span> <span data-ttu-id="5cc9d-114">En lugar de un tipo de botón declarado en el archivo de máscara, escriba "NA" para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="5cc9d-114">Instead of a button type declared in your skin file, enter "NA" for each type.</span></span>

 

<span data-ttu-id="5cc9d-115">Para cada botón debe definir la función, el tipo, la ubicación, el origen de la imagen insertada, el origen deshabilitado y el color (para los botones de tipo de acceso).</span><span class="sxs-lookup"><span data-stu-id="5cc9d-115">For each button you must define the function, type, location, pushed image source, disabled source, and color (for hit-type buttons).</span></span> <span data-ttu-id="5cc9d-116">Además, para el botón PlayPause, debe definir los orígenes de imagen normales e insertados para el estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="5cc9d-116">In addition, for the PlayPause button, you must define the normal and pushed image sources for the paused state.</span></span>

<span data-ttu-id="5cc9d-117">Para obtener más información sobre la sección de botones del archivo de definición de máscara, vea [botones](buttons.md) en la referencia de máscara.</span><span class="sxs-lookup"><span data-stu-id="5cc9d-117">For more about the Buttons section of the skin definition file, see [Buttons](buttons.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cc9d-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5cc9d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cc9d-119">**Escritura del código**</span><span class="sxs-lookup"><span data-stu-id="5cc9d-119">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




