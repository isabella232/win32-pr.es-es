---
description: En este tema se describen dos conceptos relacionados, la relación de aspecto de la imagen y la relación de aspecto de píxeles.
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Relación de aspecto de la imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275826"
---
# <a name="picture-aspect-ratio"></a><span data-ttu-id="abe49-103">Relación de aspecto de la imagen</span><span class="sxs-lookup"><span data-stu-id="abe49-103">Picture Aspect Ratio</span></span>

<span data-ttu-id="abe49-104">En este tema se describen dos conceptos relacionados, la relación de aspecto de la imagen y la relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="abe49-104">This topic describes two related concepts, picture aspect ratio and pixel aspect ratio.</span></span> <span data-ttu-id="abe49-105">A continuación, describe cómo se expresan estos conceptos en Microsoft Media Foundation mediante tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="abe49-105">It then describes how these concepts are expressed in Microsoft Media Foundation using media types.</span></span>

-   [<span data-ttu-id="abe49-106">Relación de aspecto de la imagen</span><span class="sxs-lookup"><span data-stu-id="abe49-106">Picture Aspect Ratio</span></span>](#picture-aspect-ratio)
    -   [<span data-ttu-id="abe49-107">Formato letterbox</span><span class="sxs-lookup"><span data-stu-id="abe49-107">Letterboxing</span></span>](#letterboxing)
    -   [<span data-ttu-id="abe49-108">Pan y SCAN</span><span class="sxs-lookup"><span data-stu-id="abe49-108">Pan-and-Scan</span></span>](#pan-and-scan)
-   [<span data-ttu-id="abe49-109">Relación de aspecto de píxeles</span><span class="sxs-lookup"><span data-stu-id="abe49-109">Pixel Aspect Ratio</span></span>](#pixel-aspect-ratio)
-   [<span data-ttu-id="abe49-110">Trabajar con relaciones de aspecto</span><span class="sxs-lookup"><span data-stu-id="abe49-110">Working with Aspect Ratios</span></span>](#working-with-aspect-ratios)
-   [<span data-ttu-id="abe49-111">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="abe49-111">Code Examples</span></span>](#code-examples)
    -   [<span data-ttu-id="abe49-112">Buscar el área de presentación</span><span class="sxs-lookup"><span data-stu-id="abe49-112">Finding the Display Area</span></span>](#finding-the-display-area)
    -   [<span data-ttu-id="abe49-113">Conversión entre proporciones de aspecto de píxeles</span><span class="sxs-lookup"><span data-stu-id="abe49-113">Converting Between Pixel Aspect Ratios</span></span>](#converting-between-pixel-aspect-ratios)
    -   [<span data-ttu-id="abe49-114">Calcular el área de panorámica</span><span class="sxs-lookup"><span data-stu-id="abe49-114">Calculating the Letterbox Area</span></span>](#calculating-the-letterbox-area)
-   [<span data-ttu-id="abe49-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="abe49-115">Related topics</span></span>](#related-topics)

## <a name="picture-aspect-ratio"></a><span data-ttu-id="abe49-116">Relación de aspecto de la imagen</span><span class="sxs-lookup"><span data-stu-id="abe49-116">Picture Aspect Ratio</span></span>

<span data-ttu-id="abe49-117">La *relación de aspecto* de la imagen define la forma de la imagen de vídeo mostrada.</span><span class="sxs-lookup"><span data-stu-id="abe49-117">*Picture aspect ratio* defines the shape of the displayed video image.</span></span> <span data-ttu-id="abe49-118">La relación de aspecto de la imagen es X:Y, donde X:Y es la relación del ancho de la imagen con el alto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="abe49-118">Picture aspect ratio is notated X:Y, where X:Y is the ratio of picture width to picture height.</span></span> <span data-ttu-id="abe49-119">La mayoría de los estándares de vídeo usan una relación de aspecto de imagen 4:3 o 16:9.</span><span class="sxs-lookup"><span data-stu-id="abe49-119">Most video standards use either 4:3 or 16:9 picture aspect ratio.</span></span> <span data-ttu-id="abe49-120">La relación de aspecto 16:9 se denomina normalmente *pantalla panorámica*.</span><span class="sxs-lookup"><span data-stu-id="abe49-120">The 16:9 aspect ratio is commonly called *widescreen*.</span></span> <span data-ttu-id="abe49-121">Película de cine suele usar una relación de aspecto 1:85:1 o 1:66:1.</span><span class="sxs-lookup"><span data-stu-id="abe49-121">Cinema film often uses a 1:85:1 or 1:66:1 aspect ratio.</span></span> <span data-ttu-id="abe49-122">La relación de aspecto de la imagen también se denomina *Mostrar relación de aspecto* (dar).</span><span class="sxs-lookup"><span data-stu-id="abe49-122">Picture aspect ratio is also called *display aspect ratio* (DAR).</span></span>

![diagrama que muestra las relaciones de aspecto 4:3 y 16:9](images/aspect-ratio01.png)

<span data-ttu-id="abe49-124">A veces, la imagen de vídeo no tiene la misma forma que el área de visualización.</span><span class="sxs-lookup"><span data-stu-id="abe49-124">Sometimes the video image does not have the same shape as the display area.</span></span> <span data-ttu-id="abe49-125">Por ejemplo, un vídeo 4:3 podría aparecer en un televisor de pantalla panorámica (16 × 9).</span><span class="sxs-lookup"><span data-stu-id="abe49-125">For example, a 4:3 video might be shown on a widescreen (16×9) television.</span></span> <span data-ttu-id="abe49-126">En el vídeo del equipo, es posible que el vídeo se muestre en una ventana que tenga un tamaño arbitrario.</span><span class="sxs-lookup"><span data-stu-id="abe49-126">In computer video, the video might be shown inside a window that has an arbitrary size.</span></span> <span data-ttu-id="abe49-127">En ese caso, hay tres maneras de crear la imagen para que quepa en el área de presentación:</span><span class="sxs-lookup"><span data-stu-id="abe49-127">In that case, there are three ways the image can be made to fit within the display area:</span></span>

-   <span data-ttu-id="abe49-128">Estire la imagen a lo largo de un eje para ajustarla al área de visualización.</span><span class="sxs-lookup"><span data-stu-id="abe49-128">Stretch the image along one axis to fit the display area.</span></span>
-   <span data-ttu-id="abe49-129">Escale la imagen para que quepa en el área de visualización, manteniendo la relación de aspecto de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="abe49-129">Scale the image to fit the display area, while maintaining the original picture aspect ratio.</span></span>
-   <span data-ttu-id="abe49-130">Recortar la imagen.</span><span class="sxs-lookup"><span data-stu-id="abe49-130">Crop the image.</span></span>

<span data-ttu-id="abe49-131">La ampliación de la imagen para que quepa en el área de presentación casi siempre es incorrecta, ya que no conserva la relación de aspecto de la imagen correcta.</span><span class="sxs-lookup"><span data-stu-id="abe49-131">Stretching the image to fit the display area is almost always wrong, because it does not preserve the correct picture aspect ratio.</span></span>

### <a name="letterboxing"></a><span data-ttu-id="abe49-132">Formato letterbox</span><span class="sxs-lookup"><span data-stu-id="abe49-132">Letterboxing</span></span>

<span data-ttu-id="abe49-133">El proceso de escalado de una imagen de pantalla panorámica para ajustarse a una pantalla 4:3 se denomina *panorámica*, que se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="abe49-133">The process of scaling a widescreen image to fit a 4:3 display is called *letterboxing*, shown in the next diagram.</span></span> <span data-ttu-id="abe49-134">Las áreas de rectanglular resultantes de la parte superior e inferior de la imagen se rellenan normalmente con negro, aunque se pueden usar otros colores.</span><span class="sxs-lookup"><span data-stu-id="abe49-134">The resulting rectanglular areas at the top and bottom of the image are typically filled with black, although other colors can be used.</span></span>

![diagrama que muestra la manera correcta de la panorámica](images/aspect-ratio02.png)

<span data-ttu-id="abe49-136">El caso inverso, el escalado de una imagen 4:3 para ajustarse a una pantalla panorámica, a veces se denomina *pillarboxing*.</span><span class="sxs-lookup"><span data-stu-id="abe49-136">The reverse case, scaling a 4:3 image to fit a widescreen display, is sometimes called *pillarboxing*.</span></span> <span data-ttu-id="abe49-137">Sin embargo, el término *panorámica* también se usa en sentido general, para hacer que el escalado de una imagen de vídeo se ajuste a cualquier área de presentación determinada.</span><span class="sxs-lookup"><span data-stu-id="abe49-137">However, the term *letterbox* is also used in a general sense, to mean scaling a video image to fit any given display area.</span></span>

![diagrama que muestra pillarboxing](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a><span data-ttu-id="abe49-139">Pan y SCAN</span><span class="sxs-lookup"><span data-stu-id="abe49-139">Pan-and-Scan</span></span>

<span data-ttu-id="abe49-140">Pan-and-Scan es una técnica por la que una imagen de pantalla panorámica se recorta a una zona rectangular de 4 × 3, para su presentación en un dispositivo de pantalla 4:3.</span><span class="sxs-lookup"><span data-stu-id="abe49-140">Pan-and-scan is a technique whereby a widescreen image is cropped to a 4×3 rectangular area, for display on a 4:3 display device.</span></span> <span data-ttu-id="abe49-141">La imagen resultante llena toda la presentación, sin necesidad de áreas de pantalla ancha negra, pero las partes de la imagen original se recortan de la imagen.</span><span class="sxs-lookup"><span data-stu-id="abe49-141">The resulting image fills the entire display, without requiring black letterbox areas, but portions of the original image are cropped out of the picture.</span></span> <span data-ttu-id="abe49-142">El área que se recorta puede moverse de un marco a un marco, a medida que el área de interés se desplaza.</span><span class="sxs-lookup"><span data-stu-id="abe49-142">The area that is cropped can move from frame to frame, as the area of interest shifts.</span></span> <span data-ttu-id="abe49-143">El término "pan" en *pan-and-Scan* hace referencia al efecto de movimiento panorámico que se produce al mover el área de desplazamiento y exploración.</span><span class="sxs-lookup"><span data-stu-id="abe49-143">The term "pan" in *pan-and-scan* refers to the panning effect that is caused by moving the pan-and-scan area.</span></span>

![diagrama que muestra la panorámica y el recorrido](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a><span data-ttu-id="abe49-145">Relación de aspecto de píxeles</span><span class="sxs-lookup"><span data-stu-id="abe49-145">Pixel Aspect Ratio</span></span>

<span data-ttu-id="abe49-146">*Relación de aspecto de píxeles* (par) mide la forma de un píxel.</span><span class="sxs-lookup"><span data-stu-id="abe49-146">*Pixel aspect ratio* (PAR) measures the shape of a pixel.</span></span>

<span data-ttu-id="abe49-147">Cuando se captura una imagen digital, la imagen se muestrea tanto vertical como horizontalmente, lo que da como resultado una matriz rectangular de muestras cuantificadas, denominada *píxeles* o *Pels*.</span><span class="sxs-lookup"><span data-stu-id="abe49-147">When a digital image is captured, the image is sampled both vertically and horizontally, resulting in a rectangular array of quantized samples, called *pixels* or *pels*.</span></span> <span data-ttu-id="abe49-148">La forma de la cuadrícula de muestreo determina la forma de los píxeles de la imagen digitalizada.</span><span class="sxs-lookup"><span data-stu-id="abe49-148">The shape of the sampling grid determines the shape of the pixels in the digitized image.</span></span>

<span data-ttu-id="abe49-149">A continuación se muestra un ejemplo en el que se usan pequeños números para simplificar la matemática.</span><span class="sxs-lookup"><span data-stu-id="abe49-149">Here is an example that uses small numbers to keep the math simple.</span></span> <span data-ttu-id="abe49-150">Supongamos que la imagen original es cuadrada (es decir, la relación de aspecto de la imagen es 1:1); y Supongamos que la cuadrícula de muestreo contiene 12 elementos, organizados en una cuadrícula de 4 × 3.</span><span class="sxs-lookup"><span data-stu-id="abe49-150">Suppose that the original image is square (that is, the picture aspect ratio is 1:1); and suppose the sampling grid contains 12 elements, arranged in a 4×3 grid.</span></span> <span data-ttu-id="abe49-151">La forma de cada píxel resultante será más alta de lo ancho.</span><span class="sxs-lookup"><span data-stu-id="abe49-151">The shape of each resulting pixel will be taller than it is wide.</span></span> <span data-ttu-id="abe49-152">En concreto, la forma de cada píxel será 3 × 4.</span><span class="sxs-lookup"><span data-stu-id="abe49-152">Specifically, the shape of each pixel will be 3×4.</span></span> <span data-ttu-id="abe49-153">Los píxeles que no son cuadrados se denominan *píxeles no cuadrados*.</span><span class="sxs-lookup"><span data-stu-id="abe49-153">Pixels that are not square are called *non-square pixels*.</span></span>

![diagrama que muestra una cuadrícula de muestreo no cuadrada](images/aspect-ratio05.png)

<span data-ttu-id="abe49-155">La relación de aspecto de píxeles también se aplica al dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="abe49-155">Pixel aspect ratio also applies to the display device.</span></span> <span data-ttu-id="abe49-156">La forma física del dispositivo de pantalla y la resolución de píxeles físicos (en horizontal y vertical) determinan el PAR del dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="abe49-156">The physical shape of the display device and the physical pixel resolution (across and down) determine the PAR of the display device.</span></span> <span data-ttu-id="abe49-157">Los monitores de equipo suelen usar píxeles cuadrados.</span><span class="sxs-lookup"><span data-stu-id="abe49-157">Computer monitors generally use square pixels.</span></span> <span data-ttu-id="abe49-158">Si el PAR de la imagen y el PAR de la pantalla no coinciden, la imagen se debe escalar en una dimensión, ya sea vertical u horizontalmente, para que se muestre correctamente.</span><span class="sxs-lookup"><span data-stu-id="abe49-158">If the image PAR and the display PAR do not match, the image must be scaled in one dimension, either vertically or horizontally, in order to display correctly.</span></span> <span data-ttu-id="abe49-159">La siguiente fórmula relaciona el PAR, la relación de aspecto de la pantalla (DAR) y el tamaño de la imagen en píxeles:</span><span class="sxs-lookup"><span data-stu-id="abe49-159">The following formula relates PAR, display aspect ratio (DAR), and image size in pixels:</span></span>

<span data-ttu-id="abe49-160">*Dar* = (*ancho de la imagen en píxeles*  /  *alto en píxeles*) × *par*</span><span class="sxs-lookup"><span data-stu-id="abe49-160">*DAR* = (*image width in pixels* / *image height in pixels*) × *PAR*</span></span>

<span data-ttu-id="abe49-161">Tenga en cuenta que el ancho de la imagen y el alto de la imagen en esta fórmula hacen referencia a la imagen en memoria, no a la imagen mostrada.</span><span class="sxs-lookup"><span data-stu-id="abe49-161">Note that image width and image height in this formula refer to the image in memory, not the displayed image.</span></span>

<span data-ttu-id="abe49-162">Este es un ejemplo del mundo real: el vídeo analógico NTSC-M contiene 480 líneas de análisis en el área de la imagen activa.</span><span class="sxs-lookup"><span data-stu-id="abe49-162">Here is a real-world example: NTSC-M analog video contains 480 scan lines in the active image area.</span></span> <span data-ttu-id="abe49-163">ITU-R Rec. BT. 601 especifica una velocidad de muestreo horizontal de 704 píxeles visibles por línea, lo que produce una imagen digital con 704 x 480 píxeles.</span><span class="sxs-lookup"><span data-stu-id="abe49-163">ITU-R Rec. BT.601 specifies a horizontal sampling rate of 704 visible pixels per line, yielding a digital image with 704 x 480 pixels.</span></span> <span data-ttu-id="abe49-164">La relación de aspecto de la imagen deseada es 4:3, lo que da como resultado un PAR de 10:11.</span><span class="sxs-lookup"><span data-stu-id="abe49-164">The intended picture aspect ratio is 4:3, yielding a PAR of 10:11.</span></span>

-   <span data-ttu-id="abe49-165">DAR: 4:3</span><span class="sxs-lookup"><span data-stu-id="abe49-165">DAR: 4:3</span></span>
-   <span data-ttu-id="abe49-166">Ancho en píxeles: 704</span><span class="sxs-lookup"><span data-stu-id="abe49-166">Width in pixels: 704</span></span>
-   <span data-ttu-id="abe49-167">Alto en píxeles: 480</span><span class="sxs-lookup"><span data-stu-id="abe49-167">Height in pixels: 480</span></span>
-   <span data-ttu-id="abe49-168">PAR: 10/11</span><span class="sxs-lookup"><span data-stu-id="abe49-168">PAR: 10/11</span></span>

<span data-ttu-id="abe49-169">4/3 = (704/420) x (10/11)</span><span class="sxs-lookup"><span data-stu-id="abe49-169">4/3 = (704/420) x (10/11)</span></span>

<span data-ttu-id="abe49-170">Para que la imagen se muestre correctamente en un dispositivo de pantalla con píxeles cuadrados, debe escalar el ancho entre el 10/11 y el alto 11/10.</span><span class="sxs-lookup"><span data-stu-id="abe49-170">To display this image correctly on a display device with square pixels, you must scale either the width by 10/11 or the height by 11/10.</span></span>

## <a name="working-with-aspect-ratios"></a><span data-ttu-id="abe49-171">Trabajar con relaciones de aspecto</span><span class="sxs-lookup"><span data-stu-id="abe49-171">Working with Aspect Ratios</span></span>

<span data-ttu-id="abe49-172">La forma correcta de un fotograma de vídeo se define mediante la *relación de aspecto de píxeles* (par) y el área de *visualización*.</span><span class="sxs-lookup"><span data-stu-id="abe49-172">The correct shape of a video frame is defined by the *pixel aspect ratio* (PAR) and the *display area*.</span></span>

-   <span data-ttu-id="abe49-173">El PAR define la forma de los píxeles de una imagen.</span><span class="sxs-lookup"><span data-stu-id="abe49-173">The PAR defines the shape of the pixels in an image.</span></span> <span data-ttu-id="abe49-174">Los píxeles cuadrados tienen una relación de aspecto de 1:1.</span><span class="sxs-lookup"><span data-stu-id="abe49-174">Square pixels have an aspect ratio of 1:1.</span></span> <span data-ttu-id="abe49-175">Cualquier otra relación de aspecto describe un píxel no cuadrado.</span><span class="sxs-lookup"><span data-stu-id="abe49-175">Any other aspect ratio describes a non-square pixel.</span></span> <span data-ttu-id="abe49-176">Por ejemplo, NTSC Television usa un PAR de 10:11.</span><span class="sxs-lookup"><span data-stu-id="abe49-176">For example, NTSC television uses a 10:11 PAR.</span></span> <span data-ttu-id="abe49-177">Suponiendo que está presentando el vídeo en un monitor de equipo, la pantalla tendrá píxeles cuadrados (1:1 PAR).</span><span class="sxs-lookup"><span data-stu-id="abe49-177">Assuming that you are presenting the video on a computer monitor, the display will have square pixels (1:1 PAR).</span></span> <span data-ttu-id="abe49-178">El PAR de contenido de origen se proporciona en el atributo de [**\_ \_ \_ \_ relación de aspecto MF MT**](mf-mt-pixel-aspect-ratio-attribute.md) en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="abe49-178">The PAR of the source content is given in the [**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute on the media type.</span></span>
-   <span data-ttu-id="abe49-179">El área de visualización es la región de la imagen de vídeo que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="abe49-179">The display area is the region of the video image that is intended to be shown.</span></span> <span data-ttu-id="abe49-180">Hay dos áreas de presentación relevantes que pueden especificarse en el tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="abe49-180">There are two relevant display areas that might be specified in the media type:</span></span>
    -   <span data-ttu-id="abe49-181">Abertura de pan y SCAN.</span><span class="sxs-lookup"><span data-stu-id="abe49-181">Pan-and-scan aperture.</span></span> <span data-ttu-id="abe49-182">La abertura de pan-and-Scan es una región de vídeo de 4 × 3 que se debe mostrar en el modo Pan/Scan.</span><span class="sxs-lookup"><span data-stu-id="abe49-182">The pan-and-scan aperture is a 4×3 region of video that should be displayed in pan/scan mode.</span></span> <span data-ttu-id="abe49-183">Se usa para mostrar el contenido de pantalla ancha en una pantalla de 4 x 3 sin el uso de la panorámica.</span><span class="sxs-lookup"><span data-stu-id="abe49-183">It is used to show wide-screen content on a 4×3 display without letterboxing.</span></span> <span data-ttu-id="abe49-184">La abertura de pan-and-Scan se proporciona en el atributo [**MF \_ MT \_ pan \_ scan \_ abertura**](mf-mt-pan-scan-aperture-attribute.md) y debe usarse solo cuando el atributo [**MF \_ MT \_ pan \_ scan \_ habilitado**](mf-mt-pan-scan-enabled-attribute.md) es **true**.</span><span class="sxs-lookup"><span data-stu-id="abe49-184">The pan-and-scan aperture is given in the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute and should be used only when the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute is **TRUE**.</span></span>
    -   <span data-ttu-id="abe49-185">Mostrar abertura.</span><span class="sxs-lookup"><span data-stu-id="abe49-185">Display aperture.</span></span> <span data-ttu-id="abe49-186">Esta abertura se define en algunos estándares de vídeo.</span><span class="sxs-lookup"><span data-stu-id="abe49-186">This aperture is defined in some video standards.</span></span> <span data-ttu-id="abe49-187">Todo lo que esté fuera de la abertura de pantalla es la región de sobrebarrido y no debe mostrarse.</span><span class="sxs-lookup"><span data-stu-id="abe49-187">Anything outside of the display aperture is the overscan region and should not be displayed.</span></span> <span data-ttu-id="abe49-188">Por ejemplo, la televisión NTSC tiene 720 × 480 píxeles con una abertura de pantalla de 704 × 480.</span><span class="sxs-lookup"><span data-stu-id="abe49-188">For example, NTSC television is 720×480 pixels with a display aperture of 704×480.</span></span> <span data-ttu-id="abe49-189">La abertura de pantalla se proporciona en el atributo [**MF \_ MT \_ Minimum \_ Display \_ abertura**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="abe49-189">The display aperture is given in the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span> <span data-ttu-id="abe49-190">Si está presente, se debe usar cuando el modo de desplazamiento y exploración es **falso**.</span><span class="sxs-lookup"><span data-stu-id="abe49-190">If present, it should be used when pan-and-scan mode is **FALSE**.</span></span>

<span data-ttu-id="abe49-191">Si el modo de pan y Can es **false** y no se ha definido ninguna abertura de pantalla, se debe mostrar todo el fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="abe49-191">If pan-and-can mode is **FALSE** and no display aperture is defined, the entire video frame should be displayed.</span></span> <span data-ttu-id="abe49-192">De hecho, este es el caso de la mayoría del contenido de vídeo que no sea el vídeo de televisión y DVD.</span><span class="sxs-lookup"><span data-stu-id="abe49-192">In fact, this is the case for most video content other than television and DVD video.</span></span> <span data-ttu-id="abe49-193">La relación de aspecto de la imagen completa se calcula como *(alto del área de* presentación de la  /  *pantalla*) × *par*.</span><span class="sxs-lookup"><span data-stu-id="abe49-193">The aspect ratio of the entire picture is calculated as (*display area width* / *display area height*) × *PAR*.</span></span>

## <a name="code-examples"></a><span data-ttu-id="abe49-194">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="abe49-194">Code Examples</span></span>

### <a name="finding-the-display-area"></a><span data-ttu-id="abe49-195">Buscar el área de presentación</span><span class="sxs-lookup"><span data-stu-id="abe49-195">Finding the Display Area</span></span>

<span data-ttu-id="abe49-196">En el código siguiente se muestra cómo obtener el área de visualización del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="abe49-196">The following code shows how to get the display area from the media type.</span></span>


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a><span data-ttu-id="abe49-197">Conversión entre proporciones de aspecto de píxeles</span><span class="sxs-lookup"><span data-stu-id="abe49-197">Converting Between Pixel Aspect Ratios</span></span>

<span data-ttu-id="abe49-198">En el código siguiente se muestra cómo convertir un rectángulo de una relación de aspecto de píxel (PAR) a otra, a la vez que se conserva la relación de aspecto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="abe49-198">The following code shows how to convert a rectangle from one pixel aspect ratio (PAR) to another, while preserving the picture aspect ratio.</span></span>


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a><span data-ttu-id="abe49-199">Calcular el área de panorámica</span><span class="sxs-lookup"><span data-stu-id="abe49-199">Calculating the Letterbox Area</span></span>

<span data-ttu-id="abe49-200">En el código siguiente se calcula el área de panorámica, dados un rectángulo de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="abe49-200">The following code calculates the letterbox area, given a source and destination rectangle.</span></span> <span data-ttu-id="abe49-201">Se supone que ambos rectángulos tienen el mismo PAR.</span><span class="sxs-lookup"><span data-stu-id="abe49-201">It is assumed that both rectangles have the same PAR.</span></span>


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a><span data-ttu-id="abe49-202">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="abe49-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abe49-203">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="abe49-203">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="abe49-204">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="abe49-204">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="abe49-205">**\_ \_ apertura mínima de \_ pantalla MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="abe49-205">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="abe49-206">**\_apertura de \_ \_ análisis panorámico MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="abe49-206">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="abe49-207">**examen de pan de MF \_ MT \_ \_ \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="abe49-207">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[<span data-ttu-id="abe49-208">**\_relación de \_ aspecto de píxeles MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="abe49-208">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



