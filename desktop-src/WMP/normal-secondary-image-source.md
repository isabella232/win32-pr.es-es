---
title: Origen de imagen secundaria normal
description: Origen de imagen secundaria normal
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Máscaras móviles de Windows Media Player, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de las máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff828f6d0f0c8348453cb00fef04ab31718693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695433"
---
# <a name="normal-secondary-image-source"></a><span data-ttu-id="7c54a-108">Origen de imagen secundaria normal</span><span class="sxs-lookup"><span data-stu-id="7c54a-108">Normal Secondary Image Source</span></span>

<span data-ttu-id="7c54a-109">Dependiendo de la función de botón, es posible que tenga que definir la ubicación de la imagen normal para el estado secundario del botón.</span><span class="sxs-lookup"><span data-stu-id="7c54a-109">Depending on the button function, you may need to define the location of the normal image for the secondary state of the button.</span></span> <span data-ttu-id="7c54a-110">Será la imagen que verán los usuarios cuando inserten un botón de función PlayPause la primera vez.</span><span class="sxs-lookup"><span data-stu-id="7c54a-110">This will be the image users see when they push a PlayPause function button the first time.</span></span>

<span data-ttu-id="7c54a-111">Para definir esta imagen, debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio.</span><span class="sxs-lookup"><span data-stu-id="7c54a-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="7c54a-112">A continuación, debe especificar dos enteros positivos que definan las coordenadas superior izquierda (en píxeles) de la imagen que desea usar dentro del tipo de mapa de bits del que está dibujando.</span><span class="sxs-lookup"><span data-stu-id="7c54a-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="7c54a-113">Por ejemplo, para definir la imagen normal para un origen de imagen secundario, si la imagen está dentro del mapa de bits insertado, escriba:</span><span class="sxs-lookup"><span data-stu-id="7c54a-113">For example, to define the normal image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 210,0

```



<span data-ttu-id="7c54a-114">Los Estados secundarios no pueden tener una imagen deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="7c54a-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="7c54a-115">Se supone que las imágenes secundarias tienen el mismo ancho y alto que la imagen principal.</span><span class="sxs-lookup"><span data-stu-id="7c54a-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c54a-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c54a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c54a-117">**Botones**</span><span class="sxs-lookup"><span data-stu-id="7c54a-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




