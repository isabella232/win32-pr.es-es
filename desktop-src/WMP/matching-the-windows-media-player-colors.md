---
title: Coincidencia de los colores de Media Player de Windows
description: Coincidencia de los colores de Media Player de Windows
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player tiendas en línea, que coinciden con los colores de Media Player de Windows
- tiendas en línea, coincidencia de los colores de Media Player de Windows
- tipo 1 almacenes en línea, que coinciden con los colores de Media Player de Windows
- tipo 2 tiendas en línea, coincidencia de Media Player colores de Windows
- Windows Media Player tiendas en línea, coincidencia de color de Windows Media Player
- tiendas en línea, coincidencia de color de Windows Media Player
- tipo 1 almacenes en línea, coincidencia de color de Windows Media Player
- tipo 2 tiendas en línea, coincidencia de color de Windows Media Player
- Windows Media Player tiendas en línea, coincidencia de color para Windows Media Player
- tiendas en línea, coincidencia de color para Windows Media Player
- tipo 1 tiendas en línea, coincidencia de color para Windows Media Player
- tipo 2 tiendas en línea, coincidencia de color para Windows Media Player
- coincidencia de color para Windows Media Player
- coincidencia de los colores de Media Player de Windows
- Media Player de Windows, colores coincidentes
- Media Player de Windows, coincidencia de color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704759"
---
# <a name="matching-the-windows-media-player-colors"></a><span data-ttu-id="d7950-119">Coincidencia de los colores de Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="d7950-119">Matching the Windows Media Player Colors</span></span>

<span data-ttu-id="d7950-120">Hacer que la Página Web de la tienda en línea coincida con la combinación de colores de Windows Media Player es fácil.</span><span class="sxs-lookup"><span data-stu-id="d7950-120">Making your online store webpage match the Windows Media Player color scheme is easy.</span></span> <span data-ttu-id="d7950-121">Simplemente controle el evento **external. OnColorChange** .</span><span class="sxs-lookup"><span data-stu-id="d7950-121">Simply handle the **External.OnColorChange** event.</span></span> <span data-ttu-id="d7950-122">Para especificar una función que controle el evento, use código similar al siguiente cuando se cargue la página web:</span><span class="sxs-lookup"><span data-stu-id="d7950-122">To specify a function to handle the event, use code like the following when your webpage loads:</span></span>


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



<span data-ttu-id="d7950-123">Cada vez que el usuario cambia la combinación de colores de Windows Media Player, el reproductor llamará a la función.</span><span class="sxs-lookup"><span data-stu-id="d7950-123">Each time the user changes the color scheme of Windows Media Player, the Player will call your function.</span></span> <span data-ttu-id="d7950-124">En el ejemplo siguiente se muestra una función simple que establece el fondo de la página web para que coincida con la propiedad **external. appColorLight** :</span><span class="sxs-lookup"><span data-stu-id="d7950-124">The following example shows a simple function that sets the webpage background to match the **External.appColorLight** property:</span></span>


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



<span data-ttu-id="d7950-125">También hay otras propiedades de color disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="d7950-125">There are other color properties available for your use as well.</span></span> <span data-ttu-id="d7950-126">Vea el [objeto externo para las tiendas en línea de tipo 2](external-object-for-type-2-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="d7950-126">See [External Object for Type 2 Online Stores](external-object-for-type-2-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7950-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7950-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7950-128">**External. appColorLight**</span><span class="sxs-lookup"><span data-stu-id="d7950-128">**External.appColorLight**</span></span>](external-appcolorlight.md)
</dt> <dt>

[<span data-ttu-id="d7950-129">**Evento external. OnColorChange**</span><span class="sxs-lookup"><span data-stu-id="d7950-129">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
</dt> <dt>

[<span data-ttu-id="d7950-130">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="d7950-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




