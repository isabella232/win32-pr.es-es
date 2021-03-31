---
description: Establecer preferencias de desentrelazado
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Establecer preferencias de desentrelazado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be52ae3023c8e4bc83c3305a104c389f423cffd6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805204"
---
# <a name="setting-deinterlace-preferences"></a><span data-ttu-id="9f062-103">Establecer preferencias de desentrelazado</span><span class="sxs-lookup"><span data-stu-id="9f062-103">Setting Deinterlace Preferences</span></span>

<span data-ttu-id="9f062-104">El representador de mezcla de vídeo (VMR) admite desentrelazado acelerado por hardware, lo que mejora la calidad de representación de vídeo entrelazado.</span><span class="sxs-lookup"><span data-stu-id="9f062-104">The Video Mixing Renderer (VMR) supports hardware-accelerated deinterlacing, which improves rendering quality for interlaced video.</span></span> <span data-ttu-id="9f062-105">Las características exactas que están disponibles dependen del hardware subyacente.</span><span class="sxs-lookup"><span data-stu-id="9f062-105">The exact features that are available depend on the underlying hardware.</span></span> <span data-ttu-id="9f062-106">La aplicación puede consultar las funcionalidades de desentrelazado de hardware y establecer preferencias de desentrelazado a través de la interfaz [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) o de la interfaz [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) (VMR-9).</span><span class="sxs-lookup"><span data-stu-id="9f062-106">The application can query for the hardware deinterlacing capabilities and set deinterlacing preferences through the [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) interface (VMR-7) or [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) interface (VMR-9).</span></span> <span data-ttu-id="9f062-107">El desentrelazado se realiza por secuencia.</span><span class="sxs-lookup"><span data-stu-id="9f062-107">Deinterlacing is performed on a per-stream basis.</span></span>

<span data-ttu-id="9f062-108">Existe una diferencia importante en el comportamiento de entrelazado entre el VMR-7 y el VMR-9.</span><span class="sxs-lookup"><span data-stu-id="9f062-108">There is one important difference in interlacing behavior between the VMR-7 and the VMR-9.</span></span> <span data-ttu-id="9f062-109">En los sistemas en los que el hardware gráfico no admite el desentrelazado avanzado, VMR-7 puede revertir a la superposición de hardware y indicarle que use un desentrelazado de estilo BOB.</span><span class="sxs-lookup"><span data-stu-id="9f062-109">On systems where the graphics hardware doesn't support advanced deinterlacing, the VMR-7 can fall back to the hardware overlay and instruct it to use a BOB style deinterlace.</span></span> <span data-ttu-id="9f062-110">En este caso, aunque el VMR está informando de 30 fps, el vídeo se está representando realmente en 60 volteo por segundo.</span><span class="sxs-lookup"><span data-stu-id="9f062-110">In this case, although the VMR is reporting 30fps the video is actually being rendered at 60 flips per second.</span></span>

<span data-ttu-id="9f062-111">Excepto en el caso de VMR-7 mediante la superposición de hardware, el mezclador de VMR realiza el desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="9f062-111">Except in the case of the VMR-7 using hardware overlay, deinterlacing is performed by the VMR's mixer.</span></span> <span data-ttu-id="9f062-112">El mezclador usa la interfaz de controlador de dispositivo (DDI) de desentrelazado de DirectX video Acceleration (DXVA) para realizar el desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="9f062-112">The mixer uses the DirectX Video Acceleration (DXVA) deinterlacing device driver interface (DDI) to perform the deinterlacing.</span></span> <span data-ttu-id="9f062-113">Las aplicaciones no pueden llamar a este DDI y las aplicaciones no pueden reemplazar la funcionalidad de desentrelazado de VMR.</span><span class="sxs-lookup"><span data-stu-id="9f062-113">This DDI is not callable by applications, and applications cannot replace the VMR's deinterlacing functionality.</span></span> <span data-ttu-id="9f062-114">Sin embargo, una aplicación puede seleccionar el modo de desentrelazado deseado, tal como se describe en esta sección.</span><span class="sxs-lookup"><span data-stu-id="9f062-114">However, an application can select the desired deinterlacing mode, as described in this section.</span></span>

> [!Note]  
> <span data-ttu-id="9f062-115">En esta sección se describen los métodos de **IVMRDeinterlaceControl9** , pero las versiones de VMR-7 son casi idénticas.</span><span class="sxs-lookup"><span data-stu-id="9f062-115">This section describes the **IVMRDeinterlaceControl9** methods, but the VMR-7 versions are almost identical.</span></span>

 

<span data-ttu-id="9f062-116">Para obtener las capacidades de desentrelazado de una secuencia de vídeo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9f062-116">To get the deinterlacing capabilities for a video stream, do the following:</span></span>

1.  <span data-ttu-id="9f062-117">Rellene una estructura [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) con una descripción de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9f062-117">Fill in a [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) structure with a description of the video stream.</span></span> <span data-ttu-id="9f062-118">Más adelante se proporcionan detalles sobre cómo rellenar esta estructura.</span><span class="sxs-lookup"><span data-stu-id="9f062-118">Details of how to fill in this structure are given later.</span></span>
2.  <span data-ttu-id="9f062-119">Pase la estructura al método [**IVMRDeinterlaceControl9:: GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) .</span><span class="sxs-lookup"><span data-stu-id="9f062-119">Pass the structure to the [**IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) method.</span></span> <span data-ttu-id="9f062-120">Llame al método dos veces.</span><span class="sxs-lookup"><span data-stu-id="9f062-120">Call the method twice.</span></span> <span data-ttu-id="9f062-121">La primera llamada devuelve el número de modos de desentrelazado que el hardware admite para el formato especificado.</span><span class="sxs-lookup"><span data-stu-id="9f062-121">The first call returns the number of deinterlace modes the hardware supports for the specified format.</span></span> <span data-ttu-id="9f062-122">Asigne una matriz de GUID de este tamaño y llame de nuevo al método, pasando la dirección de la matriz.</span><span class="sxs-lookup"><span data-stu-id="9f062-122">Allocate an array of GUIDs of this size, and call the method again, passing in the address of the array.</span></span> <span data-ttu-id="9f062-123">La segunda llamada rellena la matriz con GUID.</span><span class="sxs-lookup"><span data-stu-id="9f062-123">The second call fills the array with GUIDs.</span></span> <span data-ttu-id="9f062-124">Cada GUID identifica un modo de desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="9f062-124">Each GUID identifies one deinterlacing mode.</span></span>
3.  <span data-ttu-id="9f062-125">Para obtener el funcionalidades de un modo determinado, llame al método [**IVMRDeinterlaceControl9:: GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) .</span><span class="sxs-lookup"><span data-stu-id="9f062-125">To get the capabiltiies of a particular mode, call the [**IVMRDeinterlaceControl9::GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) method.</span></span> <span data-ttu-id="9f062-126">Pase la misma estructura **VMR9VideoDesc** , junto con uno de los GUID de la matriz.</span><span class="sxs-lookup"><span data-stu-id="9f062-126">Pass in the same **VMR9VideoDesc** structure, along with one of the GUIDs from the array.</span></span> <span data-ttu-id="9f062-127">El método rellena una estructura [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) con las capacidades de modo.</span><span class="sxs-lookup"><span data-stu-id="9f062-127">The method fills a [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) structure with the mode capabilities.</span></span>

<span data-ttu-id="9f062-128">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="9f062-128">The following code shows these steps:</span></span>


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



<span data-ttu-id="9f062-129">Ahora la aplicación puede establecer el modo de desentrelazado para el flujo, mediante los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9f062-129">Now the application can set the deinterlacing mode for the stream, using the following methods:</span></span>

-   <span data-ttu-id="9f062-130">El método [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) establece el modo preferido.</span><span class="sxs-lookup"><span data-stu-id="9f062-130">The [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) method sets the preferred mode.</span></span> <span data-ttu-id="9f062-131">Use GUID \_ null para desactivar el desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="9f062-131">Use GUID\_NULL to turn off deinterlacing.</span></span>
-   <span data-ttu-id="9f062-132">El método [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) especifica el comportamiento si el modo solicitado no está disponible.</span><span class="sxs-lookup"><span data-stu-id="9f062-132">The [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) method specifies the behavior if the requested mode is not available.</span></span>
-   <span data-ttu-id="9f062-133">El método [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) devuelve el modo preferido que establezca.</span><span class="sxs-lookup"><span data-stu-id="9f062-133">The [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) method returns the preferred mode that you set.</span></span>
-   <span data-ttu-id="9f062-134">El método [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) devuelve el modo real en uso, que puede ser un modo de reserva, si el modo preferido no está disponible.</span><span class="sxs-lookup"><span data-stu-id="9f062-134">The [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) method returns the actual mode in use, which might be a fallback mode, if the preferred mode is not available.</span></span>

<span data-ttu-id="9f062-135">Las páginas de referencia de método proporcionan más información.</span><span class="sxs-lookup"><span data-stu-id="9f062-135">The method reference pages give more information.</span></span>

<span data-ttu-id="9f062-136">**Uso de la estructura VMR9VideoDesc**</span><span class="sxs-lookup"><span data-stu-id="9f062-136">**Using the VMR9VideoDesc Structure**</span></span>

<span data-ttu-id="9f062-137">En el procedimiento dado anteriormente, el primer paso es rellenar una estructura **VMR9VideoDesc** con una descripción de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9f062-137">In the procedure given previously, the first step is to fill in a **VMR9VideoDesc** structure with a description of the video stream.</span></span> <span data-ttu-id="9f062-138">Empiece obteniendo el tipo de medio de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9f062-138">Start by getting the media type of the video stream.</span></span> <span data-ttu-id="9f062-139">Para ello, puede llamar a [**IPin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) en el PIN de entrada del filtro VMR.</span><span class="sxs-lookup"><span data-stu-id="9f062-139">You can do this by calling [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) on the VMR filter's input pin.</span></span> <span data-ttu-id="9f062-140">A continuación, confirme si la secuencia de vídeo está entrelazada.</span><span class="sxs-lookup"><span data-stu-id="9f062-140">Then confirm whether the video stream is interlaced.</span></span> <span data-ttu-id="9f062-141">Solo se pueden entrelazar los formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="9f062-141">Only [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats can be interlaced.</span></span> <span data-ttu-id="9f062-142">Si el tipo de formato es FORMAT \_ info, debe ser un fotograma progresivo.</span><span class="sxs-lookup"><span data-stu-id="9f062-142">If the format type is FORMAT\_VideoInfo, it must be a progressive frame.</span></span> <span data-ttu-id="9f062-143">Si el tipo de formato es \_ VideoInfo2, compruebe el campo **dwInterlaceFlags** para la \_ marca AMINTERLACE IsInterlaced.</span><span class="sxs-lookup"><span data-stu-id="9f062-143">If the format type is FORMAT\_VideoInfo2, check the **dwInterlaceFlags** field for the AMINTERLACE\_IsInterlaced flag.</span></span> <span data-ttu-id="9f062-144">La presencia de esta marca indica que el vídeo está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="9f062-144">The presence of this flag indicates the video is interlaced.</span></span>

<span data-ttu-id="9f062-145">Supongamos que la variable **pBMI** es un puntero a la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) en el bloque Format.</span><span class="sxs-lookup"><span data-stu-id="9f062-145">Assume that the variable **pBMI** is a pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the format block.</span></span> <span data-ttu-id="9f062-146">Establezca los siguientes valores en la estructura **VMR9VideoDesc** :</span><span class="sxs-lookup"><span data-stu-id="9f062-146">Set the following values in the **VMR9VideoDesc** structure:</span></span>

-   <span data-ttu-id="9f062-147">**dwSize**: establezca este campo en `sizeof(VMR9VideoDesc)` .</span><span class="sxs-lookup"><span data-stu-id="9f062-147">**dwSize**: Set this field to `sizeof(VMR9VideoDesc)`.</span></span>
-   <span data-ttu-id="9f062-148">**dwSampleWidth**: establezca este campo en `pBMI->biWidth` .</span><span class="sxs-lookup"><span data-stu-id="9f062-148">**dwSampleWidth**: Set this field to `pBMI->biWidth`.</span></span>
-   <span data-ttu-id="9f062-149">**dwSampleHeight**: establezca este campo en `abs(pBMI->biHeight)` .</span><span class="sxs-lookup"><span data-stu-id="9f062-149">**dwSampleHeight**: Set this field to `abs(pBMI->biHeight)`.</span></span>
-   <span data-ttu-id="9f062-150">**SampleFormat**: este campo describe las características de entrelazado del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="9f062-150">**SampleFormat**: This field describes the interlace characteristics of the media type.</span></span> <span data-ttu-id="9f062-151">Compruebe el campo **dwInterlaceFlags** en la estructura **VIDEOINFOHEADER2** y establezca **SampleFormat** en el valor de la marca [**VMR9 \_ SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) equivalente.</span><span class="sxs-lookup"><span data-stu-id="9f062-151">Check the **dwInterlaceFlags** field in the **VIDEOINFOHEADER2** structure, and set **SampleFormat** equal to the equivalent [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) flag.</span></span> <span data-ttu-id="9f062-152">A continuación se proporciona una función auxiliar para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="9f062-152">A helper function to do this is given below.</span></span>
-   <span data-ttu-id="9f062-153">**InputSampleFreq**: este campo proporciona la frecuencia de entrada, que se puede calcular a partir del campo **AvgTimePerFrame** de la estructura **VIDEOINFOHEADER2** .</span><span class="sxs-lookup"><span data-stu-id="9f062-153">**InputSampleFreq**: This field gives the input frequency, which can be calculated from the **AvgTimePerFrame** field in the **VIDEOINFOHEADER2** structure.</span></span> <span data-ttu-id="9f062-154">En el caso general, establezca **dwNumerator** en 10 millones y establezca **dwDenominator** en **AvgTimePerFrame**.</span><span class="sxs-lookup"><span data-stu-id="9f062-154">In the general case, set **dwNumerator** to 10000000, and set **dwDenominator** to **AvgTimePerFrame**.</span></span> <span data-ttu-id="9f062-155">Sin embargo, también puede buscar algunas velocidades de fotogramas conocidas:</span><span class="sxs-lookup"><span data-stu-id="9f062-155">However, you can also check for some well-known frame rates:</span></span>

    | <span data-ttu-id="9f062-156">Promedio de tiempo por fotograma</span><span class="sxs-lookup"><span data-stu-id="9f062-156">Average time per frame</span></span> | <span data-ttu-id="9f062-157">Velocidad de fotogramas (FPS)</span><span class="sxs-lookup"><span data-stu-id="9f062-157">Frame rate (fps)</span></span> | <span data-ttu-id="9f062-158">Numera</span><span class="sxs-lookup"><span data-stu-id="9f062-158">Numerator</span></span> | <span data-ttu-id="9f062-159">Denominador</span><span class="sxs-lookup"><span data-stu-id="9f062-159">Denominator</span></span> |
    |------------------------|------------------|-----------|-------------|
    | <span data-ttu-id="9f062-160">166833</span><span class="sxs-lookup"><span data-stu-id="9f062-160">166833</span></span>                 | <span data-ttu-id="9f062-161">59,94 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="9f062-161">59.94 (NTSC)</span></span>     | <span data-ttu-id="9f062-162">60000</span><span class="sxs-lookup"><span data-stu-id="9f062-162">60000</span></span>     | <span data-ttu-id="9f062-163">1001</span><span class="sxs-lookup"><span data-stu-id="9f062-163">1001</span></span>        |
    | <span data-ttu-id="9f062-164">333667</span><span class="sxs-lookup"><span data-stu-id="9f062-164">333667</span></span>                 | <span data-ttu-id="9f062-165">29,97 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="9f062-165">29.97 (NTSC)</span></span>     | <span data-ttu-id="9f062-166">30000</span><span class="sxs-lookup"><span data-stu-id="9f062-166">30000</span></span>     | <span data-ttu-id="9f062-167">1001</span><span class="sxs-lookup"><span data-stu-id="9f062-167">1001</span></span>        |
    | <span data-ttu-id="9f062-168">417188</span><span class="sxs-lookup"><span data-stu-id="9f062-168">417188</span></span>                 | <span data-ttu-id="9f062-169">23,97 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="9f062-169">23.97 (NTSC)</span></span>     | <span data-ttu-id="9f062-170">24000</span><span class="sxs-lookup"><span data-stu-id="9f062-170">24000</span></span>     | <span data-ttu-id="9f062-171">1001</span><span class="sxs-lookup"><span data-stu-id="9f062-171">1001</span></span>        |
    | <span data-ttu-id="9f062-172">200000</span><span class="sxs-lookup"><span data-stu-id="9f062-172">200000</span></span>                 | <span data-ttu-id="9f062-173">50,00 (PAL)</span><span class="sxs-lookup"><span data-stu-id="9f062-173">50.00 (PAL)</span></span>      | <span data-ttu-id="9f062-174">50</span><span class="sxs-lookup"><span data-stu-id="9f062-174">50</span></span>        | <span data-ttu-id="9f062-175">1</span><span class="sxs-lookup"><span data-stu-id="9f062-175">1</span></span>           |
    | <span data-ttu-id="9f062-176">400000</span><span class="sxs-lookup"><span data-stu-id="9f062-176">400000</span></span>                 | <span data-ttu-id="9f062-177">25,00 (PAL)</span><span class="sxs-lookup"><span data-stu-id="9f062-177">25.00 (PAL)</span></span>      | <span data-ttu-id="9f062-178">25</span><span class="sxs-lookup"><span data-stu-id="9f062-178">25</span></span>        | <span data-ttu-id="9f062-179">1</span><span class="sxs-lookup"><span data-stu-id="9f062-179">1</span></span>           |
    | <span data-ttu-id="9f062-180">416667</span><span class="sxs-lookup"><span data-stu-id="9f062-180">416667</span></span>                 | <span data-ttu-id="9f062-181">24,00 (película)</span><span class="sxs-lookup"><span data-stu-id="9f062-181">24.00 (Film)</span></span>     | <span data-ttu-id="9f062-182">24</span><span class="sxs-lookup"><span data-stu-id="9f062-182">24</span></span>        | <span data-ttu-id="9f062-183">1</span><span class="sxs-lookup"><span data-stu-id="9f062-183">1</span></span>           |

    

     

-   <span data-ttu-id="9f062-184">**OutputFrameFreq**: este campo proporciona la frecuencia de salida, que se puede calcular a partir del valor **InputSampleFreq** y las características de intercalación del flujo de entrada:</span><span class="sxs-lookup"><span data-stu-id="9f062-184">**OutputFrameFreq**: This field gives the output frequency, which can be calculated from the **InputSampleFreq** value and the interleaving characteristics of the input stream:</span></span>
    -   <span data-ttu-id="9f062-185">Establezca **OutputFrameFreq. dwDenominator** en **InputSampleFreq. dwDenominator**.</span><span class="sxs-lookup"><span data-stu-id="9f062-185">Set **OutputFrameFreq.dwDenominator** equal to **InputSampleFreq.dwDenominator**.</span></span>
    -   <span data-ttu-id="9f062-186">Si el vídeo de entrada está entrelazado, establezca **OutputFrameFreq. dwNumerator** en 2 x **InputSampleFreq. dwNumerator**.</span><span class="sxs-lookup"><span data-stu-id="9f062-186">If the input video is interleaved, set **OutputFrameFreq.dwNumerator** to 2 x **InputSampleFreq.dwNumerator**.</span></span> <span data-ttu-id="9f062-187">(Después de desentrelazar, se duplica la velocidad de fotogramas). De lo contrario, establezca el valor en **InputSampleFreq. dwNumerator**.</span><span class="sxs-lookup"><span data-stu-id="9f062-187">(After deinterlacing, the frame rate is doubled.) Otherwise, set the value to **InputSampleFreq.dwNumerator**.</span></span>
-   <span data-ttu-id="9f062-188">**dwFourCC**: establezca este campo en `pBMI->biCompression` .</span><span class="sxs-lookup"><span data-stu-id="9f062-188">**dwFourCC**: Set this field to `pBMI->biCompression`.</span></span>

<span data-ttu-id="9f062-189">La siguiente función auxiliar convierte marcas AMINTERLACE \_ *X* en valores [**\_ SampleFormat de VMR9**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) :</span><span class="sxs-lookup"><span data-stu-id="9f062-189">The following helper function converts AMINTERLACE\_*X* flags to [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) values:</span></span>


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



