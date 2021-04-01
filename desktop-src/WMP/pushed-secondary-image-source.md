---
title: Origen de la imagen secundaria insertada
description: Origen de la imagen secundaria insertada
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Máscaras móviles de Windows Media Player, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de las máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de50f72c8af34fa4f3e44507e172cae6890dc47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075797"
---
# <a name="pushed-secondary-image-source"></a><span data-ttu-id="12ded-108">Origen de la imagen secundaria insertada</span><span class="sxs-lookup"><span data-stu-id="12ded-108">Pushed Secondary Image Source</span></span>

<span data-ttu-id="12ded-109">Dependiendo de la función de botón, es posible que tenga que definir la ubicación de la imagen insertada para el estado secundario del botón.</span><span class="sxs-lookup"><span data-stu-id="12ded-109">Depending on the button function, you may need to define the location of the pushed image for the secondary state of the button.</span></span> <span data-ttu-id="12ded-110">Será la imagen que verán los usuarios cuando inserten un botón de función PlayPause la segunda vez.</span><span class="sxs-lookup"><span data-stu-id="12ded-110">This will be the image users see when they push a PlayPause function button the second time.</span></span>

<span data-ttu-id="12ded-111">Para definir esta imagen, debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio.</span><span class="sxs-lookup"><span data-stu-id="12ded-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="12ded-112">A continuación, debe especificar dos enteros positivos que definan las coordenadas de la parte superior izquierda (en píxeles) de la imagen que desea usar dentro del tipo de imagen del que está dibujando.</span><span class="sxs-lookup"><span data-stu-id="12ded-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the image type you are drawing from.</span></span>

<span data-ttu-id="12ded-113">Por ejemplo, para definir la imagen insertada para un origen de imagen secundario, si la imagen está dentro del mapa de bits insertado, escriba:</span><span class="sxs-lookup"><span data-stu-id="12ded-113">For example, to define the Pushed image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 248,0

```



<span data-ttu-id="12ded-114">Los Estados secundarios no pueden tener una imagen deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="12ded-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="12ded-115">Se supone que las imágenes secundarias tienen el mismo ancho y alto que la imagen principal.</span><span class="sxs-lookup"><span data-stu-id="12ded-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12ded-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12ded-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12ded-117">**Botones**</span><span class="sxs-lookup"><span data-stu-id="12ded-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




