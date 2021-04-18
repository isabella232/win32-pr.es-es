---
description: El descodificador MP3 de Windows Media descodifica archivos de audio que se han codificado en los siguientes formatos.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Descodificador MP3 de Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700212"
---
# <a name="windows-media-mp3-decoder"></a><span data-ttu-id="a13eb-103">Descodificador MP3 de Windows Media</span><span class="sxs-lookup"><span data-stu-id="a13eb-103">Windows Media MP3 Decoder</span></span>

<span data-ttu-id="a13eb-104">El descodificador MP3 de Windows Media descodifica archivos de audio que se han codificado en los siguientes formatos.</span><span class="sxs-lookup"><span data-stu-id="a13eb-104">The Windows Media MP3 decoder decodes audio files that have been encoded in the following formats.</span></span>

-   <span data-ttu-id="a13eb-105">ISO/IEC 11172-3 (audio MPEG-1) capa 3</span><span class="sxs-lookup"><span data-stu-id="a13eb-105">ISO/IEC 11172-3 (MPEG-1 Audio) Layer 3</span></span>
-   <span data-ttu-id="a13eb-106">ISO/IEC 13818-3 (MPEG-2 audio) de nivel 3, extensión de frecuencia de muestreo bajo</span><span class="sxs-lookup"><span data-stu-id="a13eb-106">ISO/IEC 13818-3 (MPEG-2 Audio) Layer 3, low sampling frequency extension</span></span>

## <a name="class-identifier"></a><span data-ttu-id="a13eb-107">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="a13eb-107">Class Identifier</span></span>

<span data-ttu-id="a13eb-108">El identificador de clase (CLSID) para el descodificador MP3 de Windows Media se representa mediante la **constante \_ CMP3DecMediaObject de CLSID**.</span><span class="sxs-lookup"><span data-stu-id="a13eb-108">The class identifier (CLSID) for the Windows Media MP3 decoder is represented by the constant **CLSID\_CMP3DecMediaObject**.</span></span> <span data-ttu-id="a13eb-109">Puede crear una instancia del descodificador MP3 llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="a13eb-109">You can create an instance of the MP3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="a13eb-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a13eb-110">Interfaces</span></span>

<span data-ttu-id="a13eb-111">Un objeto descodificador MP3 expone la interfaz **IMediaObject** para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y expone la interfaz **IMFTransform** para que el objeto se pueda usar como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="a13eb-111">An MP3 decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="a13eb-112">Un descodificador MP3 de Windows Media se comporta como un DMO o una MFT en función de las interfaces que se obtengan y de la versión de Windows que se esté ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a13eb-112">A Windows Media MP3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="a13eb-113">En la tabla siguiente se muestran las condiciones en las que un descodificador MP3 de Windows Media se comporta como un DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="a13eb-113">The following table shows the conditions under which a Windows Media MP3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="a13eb-114">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a13eb-114">Operating system</span></span> | <span data-ttu-id="a13eb-115">Comportamiento del descodificador</span><span class="sxs-lookup"><span data-stu-id="a13eb-115">Decoder behavior</span></span>                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a13eb-116">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a13eb-116">Windows XP</span></span>       | <span data-ttu-id="a13eb-117">Un descodificador MP3 de Windows Media siempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="a13eb-117">A Windows Media MP3 decoder always behaves as a DMO.</span></span>                                                                                                                                           |
| <span data-ttu-id="a13eb-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a13eb-118">Windows Vista</span></span>    | <span data-ttu-id="a13eb-119">De forma predeterminada, un descodificador MP3 de Windows Media se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="a13eb-119">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="a13eb-120">Si obtiene una interfaz **IMFTransform** o una interfaz **IPropertyStore** en un descodificador MP3 de Windows Media, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="a13eb-120">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="a13eb-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a13eb-121">Windows 7</span></span>        | <span data-ttu-id="a13eb-122">De forma predeterminada, un descodificador MP3 de Windows Media se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="a13eb-122">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="a13eb-123">Si obtiene una interfaz **IMFTransform** en un descodificador MP3 de Windows Media, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="a13eb-123">If you obtain an **IMFTransform** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="input-formats"></a><span data-ttu-id="a13eb-124">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="a13eb-124">Input Formats</span></span>

<span data-ttu-id="a13eb-125">En la tabla siguiente se muestra la etiqueta de formato de audio que representa el tipo de entrada que admite el descodificador MP3 de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a13eb-125">The following table shows the audio format tag that represents the input type supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="a13eb-126">Format (constante de etiqueta)</span><span class="sxs-lookup"><span data-stu-id="a13eb-126">Format tag constant</span></span>      | <span data-ttu-id="a13eb-127">Valor de etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="a13eb-127">Format tag value</span></span> | <span data-ttu-id="a13eb-128">Formato de audio</span><span class="sxs-lookup"><span data-stu-id="a13eb-128">Audio format</span></span>     |
|--------------------------|------------------|------------------|
| <span data-ttu-id="a13eb-129">Formato de onda \_ \_ MPEGLAYER3</span><span class="sxs-lookup"><span data-stu-id="a13eb-129">WAVE\_FORMAT\_MPEGLAYER3</span></span> | <span data-ttu-id="a13eb-130">0x55</span><span class="sxs-lookup"><span data-stu-id="a13eb-130">0x55</span></span>             | <span data-ttu-id="a13eb-131">ISO MPEG nivel 3</span><span class="sxs-lookup"><span data-stu-id="a13eb-131">ISO MPEG Layer 3</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="a13eb-132">Formatos de salida</span><span class="sxs-lookup"><span data-stu-id="a13eb-132">Output Formats</span></span>

<span data-ttu-id="a13eb-133">En la tabla siguiente se muestran las etiquetas de formato de audio que representan los tipos de salida admitidos por el descodificador MP3 de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a13eb-133">The following table shows the audio format tags that represent the output types supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="a13eb-134">Format (constante de etiqueta)</span><span class="sxs-lookup"><span data-stu-id="a13eb-134">Format tag constant</span></span>       | <span data-ttu-id="a13eb-135">Valor de etiqueta de formato</span><span class="sxs-lookup"><span data-stu-id="a13eb-135">Format tag value</span></span> | <span data-ttu-id="a13eb-136">Formato de audio</span><span class="sxs-lookup"><span data-stu-id="a13eb-136">Audio format</span></span>                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a13eb-137">\_PCM con formato de onda \_</span><span class="sxs-lookup"><span data-stu-id="a13eb-137">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="a13eb-138">0x0001</span><span class="sxs-lookup"><span data-stu-id="a13eb-138">0x0001</span></span>           | <span data-ttu-id="a13eb-139">Formato PCM (cuando se usa como DMO o MFT)</span><span class="sxs-lookup"><span data-stu-id="a13eb-139">PCM format (when used as a DMO or an MFT)</span></span>                                   |
| <span data-ttu-id="a13eb-140">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="a13eb-140">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="a13eb-141">0x0003</span><span class="sxs-lookup"><span data-stu-id="a13eb-141">0x0003</span></span>           | <span data-ttu-id="a13eb-142">Punto flotante IEEE (cuando se usa como MFT)</span><span class="sxs-lookup"><span data-stu-id="a13eb-142">IEEE floating point (when used as an MFT)</span></span>                                   |
| <span data-ttu-id="a13eb-143">formato de onda \_ \_ extensible</span><span class="sxs-lookup"><span data-stu-id="a13eb-143">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="a13eb-144">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="a13eb-144">0xFFFE</span></span>           | <span data-ttu-id="a13eb-145">Formato PCM/IEEE en la estructura **WAVEFORMATEXTENSIBLE** (cuando se usa como MFT)</span><span class="sxs-lookup"><span data-stu-id="a13eb-145">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure (when used as an MFT)</span></span> |



 

<span data-ttu-id="a13eb-146">El descodificador MP3 de Windows Media admite y enumera los siguientes tipos de medios de salida.</span><span class="sxs-lookup"><span data-stu-id="a13eb-146">The Windows Media MP3 decoder supports and enumerates the following output media types.</span></span>

-   <span data-ttu-id="a13eb-147">Un tipo de salida que tiene la misma velocidad de muestreo y número de canales que el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a13eb-147">An output type that has the same sampling rate and number of channels as the input type.</span></span>
-   <span data-ttu-id="a13eb-148">Salida mono para entrada estéreo.</span><span class="sxs-lookup"><span data-stu-id="a13eb-148">Mono output for stereo input.</span></span>
-   <span data-ttu-id="a13eb-149">Tipos de salida con profundidades de bits de 8 y 16.</span><span class="sxs-lookup"><span data-stu-id="a13eb-149">Output types with bit depths of 8 and 16.</span></span>
-   <span data-ttu-id="a13eb-150">Salida de punto flotante, si el descodificador se comporta como MFT.</span><span class="sxs-lookup"><span data-stu-id="a13eb-150">Floating point output, if the decoder is behaving as an MFT.</span></span>

<span data-ttu-id="a13eb-151">El descodificador MP3 de Windows Media admite, pero no enumera, los siguientes tipos de medios de salida.</span><span class="sxs-lookup"><span data-stu-id="a13eb-151">The Windows Media MP3 decoder supports, but does not enumerate, the following output media types.</span></span>

-   <span data-ttu-id="a13eb-152">Tipo de salida que tiene la mitad de la frecuencia de muestreo del tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a13eb-152">An output type that has half the sampling rate of the input type.</span></span>
-   <span data-ttu-id="a13eb-153">Un tipo de salida que tiene un cuarto de la frecuencia de muestreo del tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a13eb-153">An output type that has one fourth the sampling rate of the input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a13eb-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a13eb-154">Requirements</span></span>



| <span data-ttu-id="a13eb-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="a13eb-155">Requirement</span></span> | <span data-ttu-id="a13eb-156">Value</span><span class="sxs-lookup"><span data-stu-id="a13eb-156">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a13eb-157">Remoto</span><span class="sxs-lookup"><span data-stu-id="a13eb-157">Client</span></span><br/> | <span data-ttu-id="a13eb-158">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="a13eb-158">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="a13eb-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a13eb-159">Header</span></span><br/> | <dl> <span data-ttu-id="a13eb-160"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a13eb-160"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="a13eb-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a13eb-161">DLL</span></span><br/>    | <dl> <span data-ttu-id="a13eb-162"><dt>Mp3dmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a13eb-162"><dt>Mp3dmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a13eb-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="a13eb-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a13eb-164">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="a13eb-164">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="a13eb-165">Implementación de códecs</span><span class="sxs-lookup"><span data-stu-id="a13eb-165">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




