---
title: Agregar visualizaciones
description: Agregar visualizaciones
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- crear máscaras, visualizaciones
- Máscaras de Windows Media Player, visualizaciones
- máscaras, visualizaciones
- visualizaciones, máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776321"
---
# <a name="adding-visualizations"></a><span data-ttu-id="0b4b6-107">Agregar visualizaciones</span><span class="sxs-lookup"><span data-stu-id="0b4b6-107">Adding Visualizations</span></span>

<span data-ttu-id="0b4b6-108">Puede Agregar una ventana de visualización de la misma manera que agregó una ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0b4b6-108">You can add a visualization window the same way you added a video window.</span></span> <span data-ttu-id="0b4b6-109">Se puede usar la misma máscara, pero se usa un elemento **Effects** .</span><span class="sxs-lookup"><span data-stu-id="0b4b6-109">The same skin can be used, but an **EFFECTS** element is used.</span></span>

<span data-ttu-id="0b4b6-110">En primer lugar, debe agregar el elemento **Effects** y asignarle un identificador y un tamaño:</span><span class="sxs-lookup"><span data-stu-id="0b4b6-110">First you must add the **EFFECTS** element and give it an ID and size:</span></span>


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



<span data-ttu-id="0b4b6-111">A continuación, puede asignar los dos botones a una cadena de código de visualización anterior y siguiente:</span><span class="sxs-lookup"><span data-stu-id="0b4b6-111">Then you can assign the two buttons a previous and next visualization code string:</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



<span data-ttu-id="0b4b6-112">Las capas y los mapas de bits eran los mismos que se usaron en el ejemplo de vídeo, con la excepción de que se ha copiado y volteado horizontalmente la flecha de reproducción.</span><span class="sxs-lookup"><span data-stu-id="0b4b6-112">The layers and bitmaps were the same ones used in the video example, except that the play arrow was copied and flipped horizontally.</span></span>

<span data-ttu-id="0b4b6-113">Por último, se ha agregado un elemento **Player** simple con el atributo **URL** para elegir la canción que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="0b4b6-113">Finally, a simple **PLAYER** element with the **URL** attribute was added to choose a song to play.</span></span>


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



<span data-ttu-id="0b4b6-114">Puede ver una máscara de visualización de trabajo similar en la sección de ejemplo del SDK.</span><span class="sxs-lookup"><span data-stu-id="0b4b6-114">You can see a similar working visualization skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b4b6-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0b4b6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b4b6-116">**Guía de creación de máscaras**</span><span class="sxs-lookup"><span data-stu-id="0b4b6-116">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




