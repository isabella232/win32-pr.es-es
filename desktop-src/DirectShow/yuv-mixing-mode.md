---
description: Modo de mezcla YUV
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: Modo de mezcla YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf4ca6b1ba5317145c410d6e5b899c7cf264f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912102"
---
# <a name="yuv-mixing-mode"></a><span data-ttu-id="cfb9b-103">Modo de mezcla YUV</span><span class="sxs-lookup"><span data-stu-id="cfb9b-103">YUV Mixing Mode</span></span>

<span data-ttu-id="cfb9b-104">Este tema se aplica a Windows XP Service Pack 2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="cfb9b-105">A partir de Windows XP Service Pack 2, VMR admite un modo de combinación denominado modo de mezcla de YUV.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-105">Starting in Windows XP Service Pack 2, the VMR supports a mixing mode called YUV mixing mode.</span></span> <span data-ttu-id="cfb9b-106">Este modo es muy útil para las aplicaciones de TV o DVD avanzadas.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-106">This mode is most useful for advanced TV or DVD applications.</span></span> <span data-ttu-id="cfb9b-107">En él, se compensa parte de la potencia del mezclador VMR para mejorar el rendimiento del hardware de gráficos de bajo consumo que usa un diseño de arquitectura de memoria unificada.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-107">It trades some of the power of the VMR mixer for better performance on low end graphics hardware that uses a unified memory architecture design.</span></span> <span data-ttu-id="cfb9b-108">El modo de mezcla YUV se admite tanto en VMR-7 como en VMR-9.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-108">YUV mixing mode is supported on both the VMR-7 and VMR-9.</span></span>

<span data-ttu-id="cfb9b-109">**Ventajas**</span><span class="sxs-lookup"><span data-stu-id="cfb9b-109">**Advantages**</span></span>

<span data-ttu-id="cfb9b-110">El modo de mezcla YUV tiene varias ventajas relacionadas con el rendimiento de la representación en el modo de combinación RGB original compatible con VMR:</span><span class="sxs-lookup"><span data-stu-id="cfb9b-110">YUV mixing mode has several advantages relating to rendering performance over the original RGB mixing mode supported by the VMR:</span></span>

-   <span data-ttu-id="cfb9b-111">Cuando el VMR está en modo de mezcla YUV, todas las operaciones de composición de secuencias de vídeo y desentrelazado se realizan en el espacio de colores YUV.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-111">When the VMR is in YUV mixing mode, all de-interlacing and video stream composition operations are performed in YUV color space.</span></span> <span data-ttu-id="cfb9b-112">Las superficies YUV suelen requerir del 50% al 60% menos de ancho de banda de memoria que las superficies RGB equivalentes.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-112">YUV surfaces typically require from 50% to 60% less memory bandwidth than equivalent RGB surfaces.</span></span>
-   <span data-ttu-id="cfb9b-113">El desentrelazado y la composición de secuencias se realizan mediante una sola llamada al controlador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-113">The deinterlacing and stream composition are performed by a single call to the graphics driver.</span></span> <span data-ttu-id="cfb9b-114">El controlador puede usar las funcionalidades de múltiples texturas del hardware gráfico, lo que da como resultado un ahorro de ancho de banda de memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-114">The driver can use the graphics hardware's multi-texturing capabilities, resulting in additional memory bandwidth savings.</span></span>

<span data-ttu-id="cfb9b-115">Aunque cualquier aplicación de vídeo puede usar el modo de mezcla YUV, está pensado principalmente para dos tipos de aplicaciones de reproducción de vídeo:</span><span class="sxs-lookup"><span data-stu-id="cfb9b-115">Although any video application can use YUV mixing mode, it is primarily intended for two types of video playback application:</span></span>

1.  <span data-ttu-id="cfb9b-116">Aplicaciones de TV que muestran subtítulos o teletexto.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-116">TV applications that display closed captions or teletext.</span></span>
2.  <span data-ttu-id="cfb9b-117">Las aplicaciones de DVD muestran datos de subimagen de DVD o subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="cfb9b-117">DVD applications display DVD subpicture data or closed captions.</span></span>

<span data-ttu-id="cfb9b-118">**Restricciones**</span><span class="sxs-lookup"><span data-stu-id="cfb9b-118">**Restrictions**</span></span>

<span data-ttu-id="cfb9b-119">El valor de VMR exige un número de restricciones cuando se coloca en el modo de mezcla de YUV:</span><span class="sxs-lookup"><span data-stu-id="cfb9b-119">A number of restrictions are enforced by the VMR when it is put into YUV mixing mode:</span></span>

-   <span data-ttu-id="cfb9b-120">Stream 0 (la secuencia conectada a la clavija de entrada 0) puede ser progresiva o entrelazada; todas las demás secuencias deben ser progresivas.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-120">Stream 0 (the stream connected to Input Pin 0) can be progressive or interlaced; all other streams must be progressive.</span></span>
-   <span data-ttu-id="cfb9b-121">GUID \_ null (modo de trama) no permitido para el flujo 0.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-121">GUID\_NULL (weave mode) is not allowed for stream 0.</span></span>
-   <span data-ttu-id="cfb9b-122">\_La trama DeinterlacePref no se puede usar como modo de reserva porque esto podría impedir que se creara un dispositivo de desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-122">DeinterlacePref\_Weave cannot be used as a fallback mode because this could prevent a de-interlace device from being created.</span></span> <span data-ttu-id="cfb9b-123">El modo de mezcla YUV requiere un dispositivo de desentrelazado incluso si el vídeo entrante no está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-123">YUV mixing mode requires a deinterlace device even if the incoming video is not interlaced.</span></span>
-   <span data-ttu-id="cfb9b-124">No se pueden realizar cambios en el valor alfa plano asociado con cada flujo de entrada de VMR.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-124">No changes can be made to the planar alpha value associated with each VMR input stream.</span></span>
-   <span data-ttu-id="cfb9b-125">El usuario no puede modificar el orden Z de las secuencias de vídeo conectadas.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-125">The user cannot alter the Z-order of the connected video streams.</span></span> <span data-ttu-id="cfb9b-126">El orden Z predeterminado se toma del orden de anclaje.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-126">The default Z-order is taken from the pin order.</span></span>
-   <span data-ttu-id="cfb9b-127">No se admite la creación de claves de color.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-127">Color keying is not supported.</span></span>
-   <span data-ttu-id="cfb9b-128">El PIN de entrada 0 debe recibir la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-128">Input pin 0 must receive the video stream.</span></span>
-   <span data-ttu-id="cfb9b-129">Las demás clavijas de entrada solo pueden recibir datos de subsecuencia de vídeo, como subimagen de DVD, subtítulos (CC) o teletexto.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-129">The other inputs pins can only receive video sub-stream data such as DVD sub-picture, closed captions or teletext.</span></span>
-   <span data-ttu-id="cfb9b-130">Las demás clavijas de entrada solo pueden aceptar formatos de alfa YUV por píxel, como AYUV, AI44 y IA44.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-130">The other inputs pins can only accept per-pixel alpha YUV formats, such as AYUV, AI44 and IA44.</span></span>
-   <span data-ttu-id="cfb9b-131">Ninguno de los pin de entrada de VMR puede aceptar cualquier formato RGB.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-131">None of the VMR's input pins can accept any RGB formats.</span></span>
-   <span data-ttu-id="cfb9b-132">Las imágenes de mapa de bits proporcionadas por la aplicación ya no se pueden combinar con el vídeo antes de la presentación en pantalla.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-132">Application supplied bitmap images can no longer be combined with the video prior to presentation to the display.</span></span>
-   <span data-ttu-id="cfb9b-133">Los subprocesos individuales no se pueden invertir horizontal o verticalmente con las funciones de "rectángulo de salida" del mezclador de VMR.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-133">Individual sub-streams cannot be inverted horizontally or vertically using the VMR's mixer "output rectangle" functions.</span></span> <span data-ttu-id="cfb9b-134">Se admite el cambio de posición del flujo "normal" y el cambio de tamaño.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-134">"Normal" stream re-positioning and re-sizing is supported.</span></span>
-   <span data-ttu-id="cfb9b-135">El color de fondo de combinación (especificado por [**IVMRMixerControl:: SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) todavía se especifica en el espacio de colores RGB, al igual que en el modo de combinación RGB.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-135">The mixing background color (specified by [**IVMRMixerControl::SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) is still specified in the RGB color space, just as in RGB mixing mode.</span></span>

<span data-ttu-id="cfb9b-136">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="cfb9b-136">**Configuration**</span></span>

<span data-ttu-id="cfb9b-137">Las aplicaciones deben configurar explícitamente la VMR para aprovechar el modo de mezcla YUV; el modo de combinación RGB original sigue siendo el modo de mezcla predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-137">Applications must explicitly configure the VMR to take advantage of YUV mixing mode; the original RGB mixing mode remains the default mixing mode.</span></span> <span data-ttu-id="cfb9b-138">Para habilitar el modo de mezcla YUV en VMR-7, llame a [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) con la \_ marca MixerPref RenderTargetYUV.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-138">To enable YUV mixing mode in the VMR-7, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_RenderTargetYUV flag.</span></span> <span data-ttu-id="cfb9b-139">Esta llamada debe realizarse antes de que cualquiera de los pin de entrada de VMR esté conectado.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-139">This call must be made before any of the VMR's input pins are connected.</span></span> <span data-ttu-id="cfb9b-140">Para habilitar el modo de mezcla YUV en VMR-9, llame a [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con la \_ marca MixerPref9 RenderTargetYUV.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-140">To enable YUV mixing mode in the VMR-9, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_RenderTargetYUV flag.</span></span>

<span data-ttu-id="cfb9b-141">La única manera de determinar si VMR-7 admite el nuevo modo de mezcla de YUV es intentar establecer la VMR en ese modo.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-141">The only way to determine if the VMR-7 supports the new YUV mixing mode is to try setting the VMR into that mode.</span></span> <span data-ttu-id="cfb9b-142">Si la llamada se realiza correctamente, puede volver a poner la VMR en el modo de mezcla de RGB si es necesario.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-142">If the call succeeds, you can still put the VMR back into RGB mixing mode if necessary.</span></span> <span data-ttu-id="cfb9b-143">Una vez establecido en el modo de mezcla YUV, el VMR solo se puede volver a cambiar al modo de mezcla de RGB después de que todos los pin de entrada se hayan desconectado.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-143">After it is set into YUV mixing mode, the VMR can only be changed back to RGB mixing mode after all input pins have been disconnected.</span></span>

<span data-ttu-id="cfb9b-144">En el modo de mezcla YUV, puede reducir la carga de la unidad de procesamiento de gráficos (GPU) aplicando las siguientes marcas en el método **SetMixingPrefs** :</span><span class="sxs-lookup"><span data-stu-id="cfb9b-144">In YUV mixing mode, you can reduce the load on the graphics processing unit (GPU) by applying the following flags in the **SetMixingPrefs** method:</span></span>



| <span data-ttu-id="cfb9b-145">Marca</span><span class="sxs-lookup"><span data-stu-id="cfb9b-145">Flag</span></span>                                                                                 | <span data-ttu-id="cfb9b-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="cfb9b-146">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="cfb9b-147">VMR-7: MixerPref \_ DynamicSwitchToBOBVMR-9: MixerPref9 \_ DynamicSwitchToBOB</span><span class="sxs-lookup"><span data-stu-id="cfb9b-147">VMR-7: MixerPref\_DynamicSwitchToBOBVMR-9: MixerPref9\_DynamicSwitchToBOB</span></span><br/> | <span data-ttu-id="cfb9b-148">Cambie a un desentrelazado de Bob.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-148">Switch to bob deinterlacing.</span></span>                                     |
| <span data-ttu-id="cfb9b-149">VMR-7: MixerPref \_ DynamicDecimateBy2VMR-9: MixerPref \_ DynamicDecimateBy2</span><span class="sxs-lookup"><span data-stu-id="cfb9b-149">VMR-7: MixerPref\_DynamicDecimateBy2VMR-9: MixerPref\_DynamicDecimateBy2</span></span><br/>  | <span data-ttu-id="cfb9b-150">Diezmar la imagen por un factor de 2 horizontal y verticalmente.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-150">Decimate the image by a factor of 2 horizontally and vertically.</span></span> |



 

<span data-ttu-id="cfb9b-151">Puede Agregar o quitar estas marcas mientras se está ejecutando el gráfico de filtros; el cambio se aplica cuando el mezclador VMR compone el siguiente fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-151">You can add or remove these flags while the filter graph is running; the change is applied when the VMR mixer composes the next video frame.</span></span> <span data-ttu-id="cfb9b-152">Las marcas no son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-152">The flags are not mutually exclusive.</span></span> <span data-ttu-id="cfb9b-153">Esta configuración reduce la calidad de la imagen, por lo que normalmente se aplican solo cuando la calidad del vídeo es menos importante, por ejemplo, si el vídeo se reproduce en una pequeña parte de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="cfb9b-153">These settings reduce the quality of the image, so typically you would apply them only when video quality is less important — for example, if video is playing in a small portion of the user interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfb9b-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cfb9b-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfb9b-155">Usar el modo de mezcla de VMR</span><span class="sxs-lookup"><span data-stu-id="cfb9b-155">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




