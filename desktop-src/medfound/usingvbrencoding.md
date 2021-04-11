---
description: En esta sección se describe cómo configurar secuencias VBR.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Usar la codificación VBR (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275808"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a><span data-ttu-id="3d9fe-103">Usar la codificación VBR (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="3d9fe-103">Using VBR Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="3d9fe-104">Tal y como se detalla en el tema [métodos de codificación](encodingmethods.md) , se usa la codificación de velocidad de bits variable (VBR) para mejorar la coherencia de la calidad del contenido.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-104">As detailed in the [Encoding Methods](encodingmethods.md) topic, variable bit rate (VBR) encoding is used to improve the consistency of content quality.</span></span> <span data-ttu-id="3d9fe-105">Los flujos VBR se configuran de la misma manera que se codifican secuencias de velocidad de bits constante (CBR), excepto los parámetros de búfer (velocidad de bits y ventana de búfer).</span><span class="sxs-lookup"><span data-stu-id="3d9fe-105">You configure VBR streams in the same way that you encode constant bit rate (CBR) streams, except for the buffer parameters (bit rate and buffer window).</span></span> <span data-ttu-id="3d9fe-106">En esta sección se describe cómo configurar secuencias VBR.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-106">This section describes how to configure VBR streams.</span></span>

## <a name="configuring-quality-based-vbr"></a><span data-ttu-id="3d9fe-107">Configuración de VBR basada en la calidad</span><span class="sxs-lookup"><span data-stu-id="3d9fe-107">Configuring Quality Based VBR</span></span>

<span data-ttu-id="3d9fe-108">La codificación con el método VBR basado en la calidad no requiere ningún parámetro de búfer predefinido.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-108">Encoding using the quality based VBR method does not require any predefined buffer parameters.</span></span> <span data-ttu-id="3d9fe-109">En su lugar, especifique un nivel de calidad (de 0 a 100) que el codificador usa para determinar dinámicamente los parámetros de búfer adecuados.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-109">Instead, you specify a quality level (from 0 to 100) which the encoder uses to determine the appropriate buffer parameters dynamically.</span></span> <span data-ttu-id="3d9fe-110">Este modo de codificación solo usa un paso de codificación.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-110">This encoding mode uses only one encoding pass.</span></span>

<span data-ttu-id="3d9fe-111">Puede enumerar los tipos de salida VBR basados en la calidad admitidos para los códecs de audio.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-111">You can enumerate the supported quality-based VBR output types for the audio codecs.</span></span> <span data-ttu-id="3d9fe-112">Debe usar uno de los tipos devueltos por DMO al establecer el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-112">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="3d9fe-113">Para obtener más información, consulte [enumeración de tipos de audio para modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="3d9fe-113">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="3d9fe-114">Para configurar una secuencia de vídeo VBR basada en la calidad, debe establecer las propiedades que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-114">To configure a quality-based VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="3d9fe-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3d9fe-115">Property</span></span>                                            | <span data-ttu-id="3d9fe-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d9fe-116">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d9fe-117">MFPKEY \_ VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="3d9fe-117">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="3d9fe-118">Establézcalo en VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-118">Set to VARIANT\_TRUE.</span></span>                                                                                                                                   |
| [<span data-ttu-id="3d9fe-119">MFPKEY \_ VBRQUALITY</span><span class="sxs-lookup"><span data-stu-id="3d9fe-119">MFPKEY\_VBRQUALITY</span></span>](mfpkey-vbrqualityproperty.md) | <span data-ttu-id="3d9fe-120">Establezca en el valor de calidad deseado, de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-120">Set to the desired quality value, from 0 to 100.</span></span> <span data-ttu-id="3d9fe-121">No todos los valores de calidad representan valores discretos.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-121">Not all quality values represent discrete settings.</span></span> <span data-ttu-id="3d9fe-122">Vea la descripción de la propiedad para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-122">See the property description for more information.</span></span> |



 

## <a name="configuring-unconstrained-vbr"></a><span data-ttu-id="3d9fe-123">Configuración de VBR sin restricciones</span><span class="sxs-lookup"><span data-stu-id="3d9fe-123">Configuring Unconstrained VBR</span></span>

<span data-ttu-id="3d9fe-124">La codificación VBR no restringida permite que el codificador varíe el tamaño de los ejemplos individuales sin ningún límite explícito de búfer.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-124">Unconstrained VBR encoding enables the encoder to vary the size of individual samples without any explicit buffer limits.</span></span> <span data-ttu-id="3d9fe-125">Sin embargo, la velocidad de bits promedio a lo largo de la duración del contenido resultante debe ser menor o igual que el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-125">However, the average bit rate over the duration of the resulting content must be less than or equal to the specified value.</span></span> <span data-ttu-id="3d9fe-126">La VBR sin restricciones requiere dos pasos de codificación.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-126">Unconstrained VBR requires two encoding passes.</span></span>

<span data-ttu-id="3d9fe-127">Puede enumerar los tipos de salida VBR de dos pasos compatibles para los códecs de audio.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-127">You can enumerate the supported two-pass VBR output types for the audio codecs.</span></span> <span data-ttu-id="3d9fe-128">Debe usar uno de los tipos devueltos por DMO al establecer el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-128">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="3d9fe-129">Para obtener más información, consulte [enumeración de tipos de audio para modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="3d9fe-129">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="3d9fe-130">Para configurar una secuencia de vídeo VBR sin restricciones, debe establecer las propiedades que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-130">To configure an unconstrained VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="3d9fe-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3d9fe-131">Property</span></span>                                            | <span data-ttu-id="3d9fe-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d9fe-132">Description</span></span>                          |
|-----------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="3d9fe-133">MFPKEY \_ VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="3d9fe-133">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="3d9fe-134">Establézcalo en VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-134">Set to VARIANT\_TRUE.</span></span>                |
| [<span data-ttu-id="3d9fe-135">MFPKEY \_ PASSESUSED</span><span class="sxs-lookup"><span data-stu-id="3d9fe-135">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="3d9fe-136">Establezca en 2.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-136">Set to 2.</span></span>                            |
| [<span data-ttu-id="3d9fe-137">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="3d9fe-137">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="3d9fe-138">Establezca en la velocidad de bits promedio deseada.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-138">Set to the desired average bit rate.</span></span> |



 

## <a name="configuring-peak-constrained-vbr"></a><span data-ttu-id="3d9fe-139">Configuración de Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="3d9fe-139">Configuring Peak-Constrained VBR</span></span>

<span data-ttu-id="3d9fe-140">La VBR máxima restringida es como VBR no restringida, ya que se limita a una velocidad de bits promedio a lo largo de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-140">Peak-constrained VBR is like unconstrained VBR in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="3d9fe-141">Además, la VBR máxima restringida se ajusta a un búfer máximo.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-141">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="3d9fe-142">Este búfer se describe con una velocidad de bits máxima y una ventana de búfer máximo, al igual que un búfer CBR se describe mediante una velocidad de bits promedio y una ventana de búfer.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-142">This buffer is described using a peak bit rate and a peak buffer window, just as a CBR buffer is described by an average bit rate and a buffer window.</span></span> <span data-ttu-id="3d9fe-143">Este modo proporciona la flexibilidad del codificador en cómo codifica los ejemplos individuales mientras se respetan las limitaciones máximas.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-143">This mode gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span> <span data-ttu-id="3d9fe-144">Esto es especialmente útil cuando se realiza la descodificación en un chip de un dispositivo, como un reproductor de DVD, donde se deben tener en cuenta limitaciones de hardware.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-144">This is particularly useful when decoding is performed by a chip in a device, like a DVD player, where there are hardware limitations that must be considered.</span></span>

<span data-ttu-id="3d9fe-145">Los tipos de salida del codificador de audio VBR, restringido y máximo admitidos son los mismos tipos enumerados para VBR no restringida.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-145">The supported peak-constrained, VBR audio encoder output types are the same types enumerated for unconstrained VBR.</span></span> <span data-ttu-id="3d9fe-146">Establezca los valores máximos en DMO y use el tipo entregado.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-146">Set the peak values on the DMO and use the delivered type.</span></span> <span data-ttu-id="3d9fe-147">Para obtener más información, consulte [enumeración de tipos de audio para modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="3d9fe-147">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="3d9fe-148">Para configurar una secuencia de vídeo VBR máxima restringida, debe establecer las propiedades que se enumeran en la siguiente tabla mediante el método **IPropertyBag:: Write** .</span><span class="sxs-lookup"><span data-stu-id="3d9fe-148">To configure a peak-constrained VBR video stream, you must set the properties that are listed in the following table using the **IPropertyBag::Write** method.</span></span>



| <span data-ttu-id="3d9fe-149">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3d9fe-149">Property</span></span>                                            | <span data-ttu-id="3d9fe-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d9fe-150">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="3d9fe-151">MFPKEY \_ VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="3d9fe-151">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="3d9fe-152">Establézcalo en VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-152">Set to VARIANT\_TRUE.</span></span>                                           |
| [<span data-ttu-id="3d9fe-153">MFPKEY \_ PASSESUSED</span><span class="sxs-lookup"><span data-stu-id="3d9fe-153">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="3d9fe-154">Establezca en 2.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-154">Set to 2.</span></span>                                                       |
| [<span data-ttu-id="3d9fe-155">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="3d9fe-155">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="3d9fe-156">Establezca en la velocidad de bits promedio deseada.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-156">Set to the desired average bit rate.</span></span>                            |
| [<span data-ttu-id="3d9fe-157">MFPKEY \_ RMAX</span><span class="sxs-lookup"><span data-stu-id="3d9fe-157">MFPKEY\_RMAX</span></span>](mfpkey-rmaxproperty.md)             | <span data-ttu-id="3d9fe-158">Establezca en la velocidad de bits máxima deseada.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-158">Set to the desired peak bit rate.</span></span>                               |
| [<span data-ttu-id="3d9fe-159">MFPKEY \_ Bmax</span><span class="sxs-lookup"><span data-stu-id="3d9fe-159">MFPKEY\_BMAX</span></span>](mfpkey-bmaxproperty.md)             | <span data-ttu-id="3d9fe-160">Se establece en la ventana de búfer que corresponde a la velocidad de bits máxima.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-160">Set to the buffer window that corresponds to the peak bit rate.</span></span> |



 

> [!Note]  
> <span data-ttu-id="3d9fe-161">Se recomienda establecer la velocidad de bits máxima en al menos dos veces la velocidad de bits promedio.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-161">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="3d9fe-162">La configuración de la velocidad máxima en un valor inferior puede hacer que el códec codifique el contenido como CBR de dos pasadas en lugar de VBR máxima restringida.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-162">Setting the peak rate to a lower value may cause the codec to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3d9fe-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d9fe-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d9fe-164">Códecs de Windows Media</span><span class="sxs-lookup"><span data-stu-id="3d9fe-164">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-165">Uso de la codificación de Two-Pass</span><span class="sxs-lookup"><span data-stu-id="3d9fe-165">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-166">Trabajar con audio</span><span class="sxs-lookup"><span data-stu-id="3d9fe-166">Working with Audio</span></span>](workingwithaudio.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-167">Trabajar con vídeo</span><span class="sxs-lookup"><span data-stu-id="3d9fe-167">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



