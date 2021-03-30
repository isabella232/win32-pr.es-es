---
title: Origen de la imagen terciaria insertada
description: Origen de la imagen terciaria insertada
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Máscaras móviles de Windows Media Player, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de las máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a37f79ab3c5fbf02eed1f0a02219a517b12ce1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994253"
---
# <a name="pushed-tertiary-image-source"></a><span data-ttu-id="6009e-108">Origen de la imagen terciaria insertada</span><span class="sxs-lookup"><span data-stu-id="6009e-108">Pushed Tertiary Image Source</span></span>

<span data-ttu-id="6009e-109">La función del botón PlayPauseStop requiere que defina la ubicación de la imagen insertada para el estado terciario del botón.</span><span class="sxs-lookup"><span data-stu-id="6009e-109">The PlayPauseStop button function requires that you define the location of the pushed image for the tertiary state of the button.</span></span> <span data-ttu-id="6009e-110">Será la imagen que verán los usuarios cuando inserten el botón PlayPauseStop durante el streaming de una difusión en directo.</span><span class="sxs-lookup"><span data-stu-id="6009e-110">This will be the image users see when they push the PlayPauseStop button while streaming a live broadcast.</span></span>

<span data-ttu-id="6009e-111">Para definir esta imagen, debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio.</span><span class="sxs-lookup"><span data-stu-id="6009e-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="6009e-112">A continuación, debe especificar dos enteros positivos que definan las coordenadas superior izquierda (en píxeles) de la imagen que desea usar dentro del tipo de mapa de bits del que está dibujando.</span><span class="sxs-lookup"><span data-stu-id="6009e-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="6009e-113">Por ejemplo, para definir la imagen insertada para un origen de imagen terciario, si la imagen está dentro del mapa de bits insertado, escriba:</span><span class="sxs-lookup"><span data-stu-id="6009e-113">For example, to define the pushed image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 324,0

```



<span data-ttu-id="6009e-114">Los Estados terciarios no pueden tener una imagen deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="6009e-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="6009e-115">Se supone que las imágenes terciarias tienen el mismo ancho y alto que las imágenes principales y secundarias.</span><span class="sxs-lookup"><span data-stu-id="6009e-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6009e-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6009e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6009e-117">**Botones**</span><span class="sxs-lookup"><span data-stu-id="6009e-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




