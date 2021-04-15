---
title: Carátula de álbum
description: Carátula de álbum
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Aspectos móviles de Windows Media Player, carátulas de álbum
- máscaras, carátulas de álbum
- referencia para máscaras, carátulas de álbum
- archivos de imagen para máscaras, carátulas de álbum
- carátula de álbum en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0974f8683da98469e75a4472d086dcb1a244c75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695269"
---
# <a name="album-art"></a><span data-ttu-id="9e3cd-108">Carátula de álbum</span><span class="sxs-lookup"><span data-stu-id="9e3cd-108">Album Art</span></span>

<span data-ttu-id="9e3cd-109">Cuando se crea una máscara para Windows Media Player 10 Mobile o posterior, es posible que desee mostrar carátulas de álbum relacionada con el elemento multimedia que se está reproduciendo.</span><span class="sxs-lookup"><span data-stu-id="9e3cd-109">When you create a skin for Windows Media Player 10 Mobile or later, you may want to display album art that relates to the currently playing media item.</span></span> <span data-ttu-id="9e3cd-110">Al diseñar la máscara, querrá reservar espacio en la imagen de fondo para que contenga la carátula del álbum.</span><span class="sxs-lookup"><span data-stu-id="9e3cd-110">When you design your skin, you will want to reserve space in the Background image to contain the album art.</span></span>

<span data-ttu-id="9e3cd-111">La sección carátula de álbum del archivo de definición de máscara debe comenzar con la línea siguiente:</span><span class="sxs-lookup"><span data-stu-id="9e3cd-111">The Album Art section of the skin definition file must begin with the following line:</span></span>


```C++
[ Album Art ]

```



<span data-ttu-id="9e3cd-112">A continuación, debe agregar información que especifique la ubicación y el tamaño de la carátula del álbum en la máscara.</span><span class="sxs-lookup"><span data-stu-id="9e3cd-112">You then must add information that specifies the location and size of the album art in your skin.</span></span> <span data-ttu-id="9e3cd-113">Debe escribir cuatro enteros positivos, separados por comas que definan la izquierda, la parte superior, el ancho y el alto de la carátula del álbum, en píxeles, con respecto a la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="9e3cd-113">You must enter four positive integers, separated by commas that define the left, top, width, and height of the album art, in pixels, relative to the background image.</span></span> <span data-ttu-id="9e3cd-114">En el ejemplo siguiente se muestra cómo especificar dimensiones:</span><span class="sxs-lookup"><span data-stu-id="9e3cd-114">The following example shows how to specify dimensions:</span></span>


```C++
//  <Location>
//  ----------
   5,37,230,155

```



<span data-ttu-id="9e3cd-115">Si planea incluir una sección de vídeo en la máscara, puede usar el mismo tamaño y la misma ubicación que la carátula de álbum para ahorrar espacio.</span><span class="sxs-lookup"><span data-stu-id="9e3cd-115">If you plan on including a video section in your skin, you can use the same size and location for your album art to conserve space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e3cd-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e3cd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e3cd-117">**Referencia de máscara**</span><span class="sxs-lookup"><span data-stu-id="9e3cd-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




