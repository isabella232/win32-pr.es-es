---
title: Transiciones de imagen de vídeo
description: Transiciones de imagen de vídeo
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Media Format, transiciones de vídeo
- Formatos de sistema avanzado (ASF), transiciones de imagen de vídeo
- ASF (formato de sistemas avanzados), transiciones de imagen de vídeo
- transiciones de imagen de vídeo
- Códec de imagen V2 de Windows Media Video 9
- códecs, códec de Windows Media Video 9 Image V2
- secuencias de vídeo, códec de Windows Media Video 9 Image V2
- secuencias de vídeo, transiciones de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfd02628a78196a73750c2c0ff6b9e9c3d6729c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075530"
---
# <a name="video-image-transitions"></a><span data-ttu-id="12b0a-111">Transiciones de imagen de vídeo</span><span class="sxs-lookup"><span data-stu-id="12b0a-111">Video Image Transitions</span></span>

<span data-ttu-id="12b0a-112">El códec Windows Media Video 9 Image V2 anima una serie de imágenes, lo que da lugar a una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="12b0a-112">The Windows Media Video 9 Image v2 codec animates a series of images, resulting in a video stream.</span></span> <span data-ttu-id="12b0a-113">El códec puede manipular dos imágenes a la vez, combinarlas y crear una transición de una a otra según la configuración proporcionada.</span><span class="sxs-lookup"><span data-stu-id="12b0a-113">The codec can manipulate two images at once, blending them together and creating a transition from one to the other according to the configuration you supply.</span></span> <span data-ttu-id="12b0a-114">En esta sección se describen las transiciones admitidas y los parámetros que requieren.</span><span class="sxs-lookup"><span data-stu-id="12b0a-114">This section describes the supported transitions and the parameters they require.</span></span>

<span data-ttu-id="12b0a-115">Las transiciones se muestran en la siguiente tabla por sus identificadores globales.</span><span class="sxs-lookup"><span data-stu-id="12b0a-115">The transitions are listed in the following table by their global identifiers.</span></span>



| <span data-ttu-id="12b0a-116">Identificador de transición</span><span class="sxs-lookup"><span data-stu-id="12b0a-116">Transition identifier</span></span>                                                                           | <span data-ttu-id="12b0a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="12b0a-117">Description</span></span>                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12b0a-118">**\_ \_ vinculación de lazo de transición de imagen WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-118">**WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE**</span></span>](wmt-videoimage-transition-bow-tie.md)              | <span data-ttu-id="12b0a-119">La nueva imagen se revela en un conjunto de triángulos en lados opuestos del marco.</span><span class="sxs-lookup"><span data-stu-id="12b0a-119">New image is revealed in a set of triangles on opposite sides of the frame.</span></span>                                                                  |
| [<span data-ttu-id="12b0a-120">**Círculo de transición de \_ imagen WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-120">**WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE**</span></span>](wmt-videoimage-transition-circle.md)                 | <span data-ttu-id="12b0a-121">La nueva imagen se revela en un círculo.</span><span class="sxs-lookup"><span data-stu-id="12b0a-121">New image is revealed in a circle.</span></span>                                                                                                           |
| [<span data-ttu-id="12b0a-122">**\_ \_ \_ difuminación cruzada de transición de imagen WMT \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-122">**WMT\_VIDEOIMAGE\_TRANSITION\_CROSS\_FADE**</span></span>](wmt-videoimage-transition-cross-fade.md)        | <span data-ttu-id="12b0a-123">Ninguna transición especial, los coeficientes de mezcla de las dos imágenes determinan el fundido transversal (disolver).</span><span class="sxs-lookup"><span data-stu-id="12b0a-123">No special transition, the blend coefficients of the two images determine the cross-fade (dissolve).</span></span>                                         |
| [<span data-ttu-id="12b0a-124">**DIAGONAL de transición de imagen de videotransmisión WMT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-124">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL**</span></span>](wmt-videoimage-transition-diagonal.md)             | <span data-ttu-id="12b0a-125">La nueva imagen se revela a lo largo de una línea diagonal que se origina en una esquina del fotograma.</span><span class="sxs-lookup"><span data-stu-id="12b0a-125">New image is revealed along a diagonal line originating in one corner of the frame.</span></span>                                                          |
| [<span data-ttu-id="12b0a-126">**diamante de transición de \_ imágenes WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-126">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAMOND**</span></span>](wmt-videoimage-transition-diamond.md)               | <span data-ttu-id="12b0a-127">La nueva imagen se revela en un rombo.</span><span class="sxs-lookup"><span data-stu-id="12b0a-127">New image is revealed in a diamond.</span></span>                                                                                                          |
| [<span data-ttu-id="12b0a-128">**\_ \_ transición de imagen de transmisión de imágenes WMT \_ \_ a \_ color**</span><span class="sxs-lookup"><span data-stu-id="12b0a-128">**WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR**</span></span>](wmt-videoimage-transition-fade-to-color.md) | <span data-ttu-id="12b0a-129">Se resuelve de la imagen en un marco de color sólido.</span><span class="sxs-lookup"><span data-stu-id="12b0a-129">Dissolves from the image to a frame of solid color.</span></span>                                                                                          |
| [<span data-ttu-id="12b0a-130">**\_transición de imagen de vídeo WMT \_ \_ rellenado \_ V**</span><span class="sxs-lookup"><span data-stu-id="12b0a-130">**WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V**</span></span>](wmt-videoimage-transition-filled-v.md)            | <span data-ttu-id="12b0a-131">La nueva imagen se revela en un triángulo que se origina en un lado del marco.</span><span class="sxs-lookup"><span data-stu-id="12b0a-131">New image is revealed in a triangle originating from one side of the frame.</span></span>                                                                  |
| [<span data-ttu-id="12b0a-132">**\_volteo de transición de imagen de videoimágenes WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-132">**WMT\_VIDEOIMAGE\_TRANSITION\_FLIP**</span></span>](wmt-videoimage-transition-flip.md)                     | <span data-ttu-id="12b0a-133">La imagen anterior se gira en un eje y a través del centro del marco.</span><span class="sxs-lookup"><span data-stu-id="12b0a-133">Old image is rotated on a y-axis through the center of the frame.</span></span> <span data-ttu-id="12b0a-134">La nueva imagen se revela como la parte posterior de la imagen anterior.</span><span class="sxs-lookup"><span data-stu-id="12b0a-134">The new image is revealed as the back of the old image.</span></span>                    |
| [<span data-ttu-id="12b0a-135">**\_bajorrelieve de transición de imagen de videoimágenes WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-135">**WMT\_VIDEOIMAGE\_TRANSITION\_INSET**</span></span>](wmt-videoimage-transition-inset.md)                   | <span data-ttu-id="12b0a-136">Una nueva imagen se revela mediante un rectángulo que se origina en una esquina del fotograma.</span><span class="sxs-lookup"><span data-stu-id="12b0a-136">New image is revealed by a rectangle originating from one corner of the frame.</span></span>                                                               |
| [<span data-ttu-id="12b0a-137">**\_iris de transición de imagen de imágenes WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-137">**WMT\_VIDEOIMAGE\_TRANSITION\_IRIS**</span></span>](wmt-videoimage-transition-iris.md)                     | <span data-ttu-id="12b0a-138">La nueva imagen se revela a lo largo de un eje x y un eje y.</span><span class="sxs-lookup"><span data-stu-id="12b0a-138">New image is revealed along an x-axis and a y-axis.</span></span>                                                                                          |
| [<span data-ttu-id="12b0a-139">**\_rollo de página de transición de VIDEOIMAGE WMT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-139">**WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL**</span></span>](wmt-videoimage-transition-page-roll.md)          | <span data-ttu-id="12b0a-140">La imagen antigua se transforma en un efecto de volteo de página y revela la nueva imagen debajo.</span><span class="sxs-lookup"><span data-stu-id="12b0a-140">Old image is transformed in a page-flipping effect, revealing the new image underneath.</span></span>                                                      |
| [<span data-ttu-id="12b0a-141">**\_rectángulo de transición de imagen de videoimágenes WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-141">**WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE**</span></span>](wmt-videoimage-transition-rectangle.md)           | <span data-ttu-id="12b0a-142">Una nueva imagen se revela mediante un rectángulo dentro del marco.</span><span class="sxs-lookup"><span data-stu-id="12b0a-142">New image is revealed by a rectangle within the frame.</span></span>                                                                                       |
| [<span data-ttu-id="12b0a-143">**transición de imagen de transmisión de \_ imágenes WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-143">**WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL**</span></span>](wmt-videoimage-transition-reveal.md)                 | <span data-ttu-id="12b0a-144">La nueva imagen se revela a lo largo de una línea recta que se origina en un lado del marco.</span><span class="sxs-lookup"><span data-stu-id="12b0a-144">New image is revealed along a straight line originating from one side of the frame.</span></span>                                                          |
| [<span data-ttu-id="12b0a-145">**diapositiva de transición de \_ imagen WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-145">**WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE**</span></span>](wmt-videoimage-transition-slide.md)                   | <span data-ttu-id="12b0a-146">La imagen antigua se desliza fuera del fotograma y se revela la nueva imagen debajo.</span><span class="sxs-lookup"><span data-stu-id="12b0a-146">Old image slides out of the frame, revealing the new image underneath.</span></span>                                                                       |
| [<span data-ttu-id="12b0a-147">**División de transición de imagen de videotransmisión WMT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-147">**WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT**</span></span>](wmt-videoimage-transition-split.md)                   | <span data-ttu-id="12b0a-148">La nueva imagen se revela mediante una división horizontal o vertical en la imagen anterior.</span><span class="sxs-lookup"><span data-stu-id="12b0a-148">New image is revealed by a horizontal or vertical split in the old image.</span></span> <span data-ttu-id="12b0a-149">La división aparece a lo largo de una línea recta que comienza dentro del marco.</span><span class="sxs-lookup"><span data-stu-id="12b0a-149">The split appears along a straight line starting inside the frame.</span></span> |
| [<span data-ttu-id="12b0a-150">**estrella de transición de \_ imágenes WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-150">**WMT\_VIDEOIMAGE\_TRANSITION\_STAR**</span></span>](wmt-videoimage-transition-star.md)                     | <span data-ttu-id="12b0a-151">La nueva imagen se revela mediante una estrella de cinco puntas dentro del marco.</span><span class="sxs-lookup"><span data-stu-id="12b0a-151">New image is revealed by a five-pointed star inside the frame.</span></span>                                                                               |
| [<span data-ttu-id="12b0a-152">**\_rueda de transición de VIDEOIMAGE WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b0a-152">**WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL**</span></span>](wmt-videoimage-transition-wheel.md)                   | <span data-ttu-id="12b0a-153">La nueva imagen se revela con cuatro radios rotatorios con un punto de pivote común.</span><span class="sxs-lookup"><span data-stu-id="12b0a-153">New image is revealed by four rotating spokes with a common pivot point.</span></span>                                                                     |



 

<span data-ttu-id="12b0a-154">Cada transición se describe completamente en su propio tema.</span><span class="sxs-lookup"><span data-stu-id="12b0a-154">Each transition is fully described in its own topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12b0a-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12b0a-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12b0a-156">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="12b0a-156">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="12b0a-157">**\_SAMPLE2 de imágenes \_ WMT**</span><span class="sxs-lookup"><span data-stu-id="12b0a-157">**WMT\_VIDEOIMAGE\_SAMPLE2**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




