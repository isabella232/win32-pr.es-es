---
title: Origen de imagen terciario normal
description: Origen de imagen terciario normal
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Máscaras móviles de Windows Media Player, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de las máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418995"
---
# <a name="normal-tertiary-image-source"></a><span data-ttu-id="2f692-108">Origen de imagen terciario normal</span><span class="sxs-lookup"><span data-stu-id="2f692-108">Normal Tertiary Image Source</span></span>

<span data-ttu-id="2f692-109">La función del botón PlayPauseStop requiere que defina la ubicación de la imagen normal para el estado terciario del botón.</span><span class="sxs-lookup"><span data-stu-id="2f692-109">The PlayPauseStop button function requires that you define the location of the normal image for the tertiary state of the button.</span></span> <span data-ttu-id="2f692-110">Será la imagen que verán los usuarios después de haber insertado el botón PlayPauseStop para empezar a transmitir una difusión en directo.</span><span class="sxs-lookup"><span data-stu-id="2f692-110">This will be the image users see after they have pushed the PlayPauseStop button to begin streaming a live broadcast.</span></span>

<span data-ttu-id="2f692-111">Para definir esta imagen, debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio.</span><span class="sxs-lookup"><span data-stu-id="2f692-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="2f692-112">A continuación, debe especificar dos enteros positivos que definan las coordenadas superior izquierda (en píxeles) de la imagen que desea usar dentro del tipo de mapa de bits del que está dibujando.</span><span class="sxs-lookup"><span data-stu-id="2f692-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="2f692-113">Por ejemplo, para definir la imagen normal para un origen de imagen terciario, si la imagen está dentro del mapa de bits insertado, escriba:</span><span class="sxs-lookup"><span data-stu-id="2f692-113">For example, to define the normal image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 286,0

```



<span data-ttu-id="2f692-114">Los Estados terciarios no pueden tener una imagen deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="2f692-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="2f692-115">Se supone que las imágenes terciarias tienen el mismo ancho y alto que las imágenes principales y secundarias.</span><span class="sxs-lookup"><span data-stu-id="2f692-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f692-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f692-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f692-117">**Botones**</span><span class="sxs-lookup"><span data-stu-id="2f692-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




