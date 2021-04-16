---
description: Combinación no cuadrada
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Combinación no cuadrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537690"
---
# <a name="non-square-mixing"></a><span data-ttu-id="f0aa9-103">Combinación no cuadrada</span><span class="sxs-lookup"><span data-stu-id="f0aa9-103">Non-Square Mixing</span></span>

<span data-ttu-id="f0aa9-104">Este tema se aplica a Windows XP Service Pack 2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="f0aa9-105">Cuando VMR-9 mezcla dos o más secuencias, hay dos puntos en los que puede producirse el escalado: cuando el mezclador compone los flujos de entrada y cuando el asignador de representador representa la imagen compuesta.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-105">When the VMR-9 mixes two or more streams, there are two points where scaling can occur: When the mixer composites the input streams, and when the allocator-presenter renders the composited image.</span></span>

![operaciones de combinación de VMR](images/vmr-nonsquare-mixing.png)

<span data-ttu-id="f0aa9-107">Las versiones anteriores de VMR-9 componen siempre los flujos de entrada con una relación de aspecto de píxeles cuadrada (1:1), incluso cuando solo había un flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-107">Previous versions of the VMR-9 always composited the input streams using a square (1:1) pixel aspect ratio (PAR), even when there was only a single video stream.</span></span> <span data-ttu-id="f0aa9-108">Si el flujo de entrada tuviera píxeles no cuadrados, esto provocó una operación de escala innecesaria.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-108">If the input stream had non-square pixels, this caused an unnecessary scaling operation.</span></span> <span data-ttu-id="f0aa9-109">El escalado debe evitarse lo máximo posible, por supuesto, porque degrada la calidad final de la imagen.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-109">Scaling should be avoided as much as possible, of course, because it degrades the final image quality.</span></span>

<span data-ttu-id="f0aa9-110">A partir de Windows XP Service Pack 2, VMR-9 admite dos maneras diferentes de evitar el problema del doble escalado:</span><span class="sxs-lookup"><span data-stu-id="f0aa9-110">Starting in Windows XP Service Pack 2, the VMR-9 supports two different ways to avoid the problem of double scaling:</span></span>

-   <span data-ttu-id="f0aa9-111">Implemente un asignador personalizado y admita la interfaz [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) .</span><span class="sxs-lookup"><span data-stu-id="f0aa9-111">Implement a custom allocator-presenter and support the [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) interface.</span></span>
-   <span data-ttu-id="f0aa9-112">Use el modo de combinación no cuadrado.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-112">Use non-square mixing mode.</span></span>

<span data-ttu-id="f0aa9-113">En esta sección se describe el modo de combinación no cuadrado.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-113">This section describes non-square mixing mode.</span></span> <span data-ttu-id="f0aa9-114">Las aplicaciones pueden combinar ambas técnicas.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-114">Applications can combine both techniques.</span></span>

<span data-ttu-id="f0aa9-115">**Cómo funciona la combinación no cuadrada**</span><span class="sxs-lookup"><span data-stu-id="f0aa9-115">**How Non-Square Mixing Works**</span></span>

<span data-ttu-id="f0aa9-116">En el modo de mezcla no cuadrado, VMR-9 selecciona un flujo de entrada para que sea el tamaño y el PAR de destino.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-116">In non-square mixing mode, the VMR-9 selects one input stream to be the target size and PAR.</span></span> <span data-ttu-id="f0aa9-117">El mezclador de VMR no escala el vídeo desde esa secuencia ni desde ningún otro flujo con el mismo tamaño de imagen y PAR.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-117">The VMR's mixer does not scale the video from that stream or from any other streams with the same image size and PAR.</span></span> <span data-ttu-id="f0aa9-118">Los flujos con un tamaño o relación de aspecto diferente se escalan para coincidir con el PAR de destino y se muestran en la panorámica para ajustarse al tamaño de la imagen de salida final.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-118">Streams with a different size or aspect ratio are scaled to match the target PAR and letterboxed to fit the final output image size.</span></span>

<span data-ttu-id="f0aa9-119">La elección de los flujos depende del modo de mezcla actual:</span><span class="sxs-lookup"><span data-stu-id="f0aa9-119">The choice of streams depends on the current mixing mode:</span></span>

-   <span data-ttu-id="f0aa9-120">El modo de mezcla YUV está restringido a un flujo de vídeo en el pin 0.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-120">YUV mixing mode is restricted to one video stream on pin 0.</span></span> <span data-ttu-id="f0aa9-121">(Los otros PIN pueden tener secuencias de subimagen o de subtítulos cerrados). Por lo tanto, VMR-9 selecciona siempre el pin 0 para el tamaño y el PAR de la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-121">(The other pins may have subpicture or closed caption streams.) Therefore, the VMR-9 always selects pin 0 for the target image size and PAR.</span></span>
-   <span data-ttu-id="f0aa9-122">En el modo de combinación RGB, VMR selecciona la secuencia con el tamaño de imagen más grande.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-122">In RGB mixing mode, the VMR selects the stream with the largest image size.</span></span> <span data-ttu-id="f0aa9-123">Si hay más de uno, selecciona el que tiene el orden z más alto; y si sigue habiendo un empate, selecciona la secuencia con el número de PIN más bajo.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-123">If there is more than one, it selects the one with the highest z-order; and if there is still a tie, it selects the stream with the lowest pin number.</span></span>

<span data-ttu-id="f0aa9-124">**Ejemplos de operación**</span><span class="sxs-lookup"><span data-stu-id="f0aa9-124">**Examples of Operation**</span></span>

<span data-ttu-id="f0aa9-125">**Ejemplo 1.**</span><span class="sxs-lookup"><span data-stu-id="f0aa9-125">**Example 1.**</span></span> <span data-ttu-id="f0aa9-126">El flujo 0 es 720 x 480 píxeles con una relación de aspecto de imagen de 16:9.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-126">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="f0aa9-127">La secuencia 1 es 640 x 480 píxeles con una relación de aspecto de imagen de 4:3.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-127">Stream 1 is a 640 x 480 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="f0aa9-128">En este ejemplo, la secuencia 0 tiene el tamaño de la imagen más grande, por lo que la VMR elige este flujo, independientemente del modo de mezcla de RGB o el modo de combinación de YUB.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-128">In this example, stream 0 has the largest image size, so the VMR chooses this stream, regardless of RGB mixing mode or YUB mixing mode.</span></span> <span data-ttu-id="f0aa9-129">El PAR es 32:27 (16:9/720:480), lo que significa que la imagen se debe ajustar horizontalmente por esta relación para generar la relación de aspecto de la imagen 16:9 correcta.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-129">The PAR is 32:27 (16:9 / 720:480), meaning the image must be stretched horizontally by this ratio to produce the correct 16:9 picture aspect ratio.</span></span>

<span data-ttu-id="f0aa9-130">Para que coincida con el PAR de destino, el mezclador VMR escala el flujo 1 por la relación inversa (27:32), lo que da como resultado una imagen de 540 x 480.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-130">To match the target PAR, the VMR mixer scales stream 1 by the inverse ratio (27:32), resulting in a 540 x 480 image.</span></span> <span data-ttu-id="f0aa9-131">Los dos flujos se componen en una superficie.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-131">The two streams are then composited onto one surface.</span></span> <span data-ttu-id="f0aa9-132">Para mostrar la imagen resultante correctamente, el presentador del asignador debe expandir la imagen horizontalmente para ajustarse a la relación de aspecto de la imagen 16:9.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-132">To display the resulting image correctly, the allocator presenter must stretch the image horizontally to fit the 16:9 picture aspect ratio.</span></span>

![ejemplo 1:](images/vmr-nonsquare-mixing2.png)

<span data-ttu-id="f0aa9-134">**Ejemplo 2.**</span><span class="sxs-lookup"><span data-stu-id="f0aa9-134">**Example 2.**</span></span> <span data-ttu-id="f0aa9-135">El flujo 0 es 720 x 480 píxeles con una relación de aspecto de imagen de 16:9.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-135">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="f0aa9-136">La secuencia 1 es 1024 x 768 píxeles con una relación de aspecto de imagen de 4:3.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-136">Stream 1 is a 1024 x 768 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="f0aa9-137">Si VMR-9 usa el modo de mezcla YUV, siempre selecciona el flujo 0.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-137">If the VMR-9 is using YUV mixing mode, it always selects stream 0.</span></span> <span data-ttu-id="f0aa9-138">Por lo tanto, ajusta el flujo 1 a 540 x 480 píxeles para que coincida con el PAR de flujo 0.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-138">Therefore, it stretches stream 1 to 540 x 480 pixels, to match the PAR of stream 0.</span></span>

<span data-ttu-id="f0aa9-139">Si VMR-9 usa el modo de combinación RGB, selecciona Stream 1 como destino, ya que ese flujo tiene el tamaño de imagen más grande.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-139">If the VMR-9 is using RGB mixing mode, it selects stream 1 as the target, because that stream has the largest image size.</span></span> <span data-ttu-id="f0aa9-140">Ajusta el flujo 0 a un tamaño de imagen de 1024 x 576 píxeles.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-140">It stretches stream 0 to an image size of 1024 x 576 pixels.</span></span> <span data-ttu-id="f0aa9-141">Tenga en cuenta que, en este caso, la imagen compuesta tiene un PAR de 1:1, por lo que el asignador-Presenter no tiene que corregirse para los píxeles no cuadrados.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-141">Note that in this case, the composited image has a PAR of 1:1, so the allocator-presenter does not have to correct for non-square pixels.</span></span> <span data-ttu-id="f0aa9-142">(Es posible que tenga que ajustar el vídeo para que tenga en cuenta el rectángulo de destino).</span><span class="sxs-lookup"><span data-stu-id="f0aa9-142">(It might still need to stretch the video to account for the destination rectangle.)</span></span>

<span data-ttu-id="f0aa9-143">**Usar el modo de combinación no cuadrado**</span><span class="sxs-lookup"><span data-stu-id="f0aa9-143">**Using Non-Square Mixing Mode**</span></span>

<span data-ttu-id="f0aa9-144">Se recomienda el modo de mezcla no cuadrado si se cumple alguna de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="f0aa9-144">Non-square mixing mode is recommended if either of the following conditions are true:</span></span>

-   <span data-ttu-id="f0aa9-145">La aplicación nunca envía más de una secuencia de vídeo a VMR-9.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-145">Your application never sends more than one video stream to the VMR-9.</span></span>
-   <span data-ttu-id="f0aa9-146">La aplicación representa archivos de DVD, televisión o MS-DVR.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-146">Your application renders DVD, television, or ms-dvr files.</span></span> <span data-ttu-id="f0aa9-147">También debe usar el modo de mezcla YUV en este caso, si el hardware de gráficos lo admite.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-147">You should also use YUV mixing mode in this case, if the graphics hardware supports it.</span></span>

<span data-ttu-id="f0aa9-148">Si la aplicación mezcla varias secuencias de vídeo que pueden tener distintos tamaños de imagen o relaciones de aspecto de píxeles, se recomienda usar el modo de combinación de cuadrados predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-148">If your application mixes multiple video streams that may have varying image sizes or pixel aspect ratios, the default square mixing mode is recommended.</span></span>

<span data-ttu-id="f0aa9-149">Para configurar el modo de mezcla no cuadrado, el gráfico de filtro debe detenerse y todos los pin de entrada se desconectarán en la VMR-9.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-149">To configure non-square mixing mode, the filter graph must be stopped and all input pins disconnected on the VMR-9.</span></span> <span data-ttu-id="f0aa9-150">Después, llame a [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con la \_ marca MixerPref9 NonSquareMixing:</span><span class="sxs-lookup"><span data-stu-id="f0aa9-150">Then call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_NonSquareMixing flag:</span></span>


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> <span data-ttu-id="f0aa9-151">Si combina la marca MixerPref9 \_ NonSquareMixing con la marca MixerPref9 \_ ARADJUSTXORY, VMR-9 omite la \_ marca MixerPref9 ARAdjustXorY.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-151">If you combine the MixerPref9\_NonSquareMixing flag with the MixerPref9\_ARAdjustXorY flag, the VMR-9 ignores the MixerPref9\_ARAdjustXorY flag.</span></span>

 

<span data-ttu-id="f0aa9-152">Si la aplicación usa un asignador personalizado con el modo de mezcla sin cuadrado, tenga en cuenta que la imagen compuesta puede tener un PAR no cuadrado.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-152">If your application uses a custom allocator-presenter with non-square mixing mode, be aware that the composited image may have a non-square PAR.</span></span> <span data-ttu-id="f0aa9-153">Allocator-Presenter debe escalar la imagen a un PAR cuadrado (1:1).</span><span class="sxs-lookup"><span data-stu-id="f0aa9-153">The allocator-presenter must scale the image to a square (1:1) PAR.</span></span>

<span data-ttu-id="f0aa9-154">**Mapas de bits estáticos**</span><span class="sxs-lookup"><span data-stu-id="f0aa9-154">**Static Bitmaps**</span></span>

<span data-ttu-id="f0aa9-155">Si usa la interfaz [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) para mezclar un mapa de bits estático en el vídeo, debe considerar que el mapa de bits es una segunda secuencia de vídeo para los fines del modo de mezcla de VMR.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-155">If you use the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface to blend a static bitmap onto the video, you should consider the bitmap to be a second video stream for purposes of the VMR mixing mode.</span></span>

<span data-ttu-id="f0aa9-156">VMR trata el mapa de bits con el mismo PAR que el destino.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-156">The VMR treats the bitmap as having the same PAR as the target.</span></span> <span data-ttu-id="f0aa9-157">No escala el mapa de bits para ajustarse a la relación de aspecto de píxeles del destino.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-157">It does not scale the bitmap to adjust for the target's pixel aspect ratio.</span></span> <span data-ttu-id="f0aa9-158">En la configuración predeterminada de VMR, el destino tiene un PAR de 1:1, que coincide con la mayoría de los mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-158">In the VMR's default configuration, the target has a 1:1 PAR, which matches most bitmaps.</span></span> <span data-ttu-id="f0aa9-159">En el modo de mezcla no cuadrado, el destino puede tener píxeles no cuadrados.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-159">In non-square mixing mode, the target might have non-square pixels.</span></span> <span data-ttu-id="f0aa9-160">Para asegurarse de que el mapa de bits se muestre correctamente, la aplicación debe proporcionar una imagen cuyo PAR coincida con el PAR de destino.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-160">To ensure that the bitmap is displayed correctly, the application should supply an image whose PAR matches the target PAR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0aa9-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f0aa9-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0aa9-162">Usar el modo de mezcla de VMR</span><span class="sxs-lookup"><span data-stu-id="f0aa9-162">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



