---
description: El descodificador de audio MPEG de Microsoft es una transformación de Media Foundation sincrónica (MFT) que permite descodificar formatos de secuencia elementales de audio MPEG mediante la canalización de Media Foundation (MF).
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: Descodificador de audio MPEG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001449"
---
# <a name="mpeg-audio-decoder"></a><span data-ttu-id="e8dda-103">Descodificador de audio MPEG</span><span class="sxs-lookup"><span data-stu-id="e8dda-103">MPEG Audio Decoder</span></span>

<span data-ttu-id="e8dda-104">El descodificador de audio MPEG de Microsoft es una [transformación de Media Foundation](media-foundation-transforms.md) sincrónica (MFT) que permite descodificar formatos de secuencia elementales de audio MPEG mediante la canalización de Media Foundation (MF).</span><span class="sxs-lookup"><span data-stu-id="e8dda-104">The Microsoft MPEG Audio Decoder is a synchronous [Media Foundation Transform](media-foundation-transforms.md) (MFT) that enables decoding MPEG audio elementary stream formats using the Media Foundation (MF) pipeline.</span></span>

<span data-ttu-id="e8dda-105">El descodificador admite los siguientes formatos de flujo elemental de MPEG.</span><span class="sxs-lookup"><span data-stu-id="e8dda-105">The decoder supports the following MPEG elementary stream formats.</span></span>

-   <span data-ttu-id="e8dda-106">MPEG-1 capas de audio I y II (ISO/IEC 11172-3).</span><span class="sxs-lookup"><span data-stu-id="e8dda-106">MPEG-1 audio layers I and II (ISO/IEC 11172-3).</span></span> <span data-ttu-id="e8dda-107">2.</span><span class="sxs-lookup"><span data-stu-id="e8dda-107">2.</span></span> <span data-ttu-id="e8dda-108">MPEG-2 compatible con versiones anteriores, las capas I y II (ISO</span><span class="sxs-lookup"><span data-stu-id="e8dda-108">MPEG-2 backward-compatible, layers I and II (ISO</span></span>

-   <span data-ttu-id="e8dda-109">MPEG-2 compatible con versiones anteriores, las capas I y II (ISO/IEC 13818-3), mono y estéreo únicamente</span><span class="sxs-lookup"><span data-stu-id="e8dda-109">MPEG-2 backward-compatible, layers I and II (ISO/IEC 13818-3), mono and stereo only</span></span>

## <a name="class-identifier"></a><span data-ttu-id="e8dda-110">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="e8dda-110">Class Identifier</span></span>

<span data-ttu-id="e8dda-111">El identificador de clase (CLSID) del descodificador de audio MPEG es **CLSID \_ MSMPEGAudDecMFT**, definido en el archivo de encabezado wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="e8dda-111">The class identifier (CLSID) of the MPEG Audio decoder is **CLSID\_MSMPEGAudDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-media-types"></a><span data-ttu-id="e8dda-112">Tipos de medios de entrada</span><span class="sxs-lookup"><span data-stu-id="e8dda-112">Input Media Types</span></span>

<span data-ttu-id="e8dda-113">El descodificador de audio MPEG admite los siguientes atributos de tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="e8dda-113">The MPEG Audio decoder supports the following input media type attributes.</span></span>



| <span data-ttu-id="e8dda-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="e8dda-114">Attribute</span></span>                                                                               | <span data-ttu-id="e8dda-115">Value</span><span class="sxs-lookup"><span data-stu-id="e8dda-115">Value</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8dda-116">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="e8dda-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="e8dda-117">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e8dda-117">**MFMediaType\_Audio**</span></span>                                                                                                                                                                                                                                                |
| [<span data-ttu-id="e8dda-118">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="e8dda-118">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="e8dda-119">**MFAudioFormat \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="e8dda-119">**MFAudioFormat\_MPEG**</span></span>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="e8dda-120">**\_canales de \_ número de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8dda-120">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="e8dda-121">Opta Normalmente 1 para mono o 2 para estéreo, pero puede tener hasta 6 canales.</span><span class="sxs-lookup"><span data-stu-id="e8dda-121">(Optional) Usually 1 for mono or 2 for stereo, but can be up to 6 channels.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="e8dda-122">**\_máscara de \_ canal de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8dda-122">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="e8dda-123">Opta Normalmente, 0x4 para mono o 0X3 para estéreo, pero también puede ser cualquiera de las máscaras de canal asociadas a un máximo de 6 canales (3/2/1, 3/2, 3/1, 2/2, 2/1).</span><span class="sxs-lookup"><span data-stu-id="e8dda-123">(Optional) Usually 0x4 for mono or 0x3 for stereo, but can also be any one of the channel masks associated with up to 6 channels (3/2/1, 3/2, 3/1, 2/2, 2/1).</span></span> <span data-ttu-id="e8dda-124">Si está presente, la máscara de canal debe ser coherente con el número de canales de entrada especificado.</span><span class="sxs-lookup"><span data-stu-id="e8dda-124">If present, the channel mask must be consistent with the specified input number of channels.</span></span><br/> |
| [<span data-ttu-id="e8dda-125">**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="e8dda-125">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="e8dda-126">Opta Uno de los siguientes: 16000, 22050, 24000, 32000, 44100, 48000.</span><span class="sxs-lookup"><span data-stu-id="e8dda-126">(Optional) One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span> <span data-ttu-id="e8dda-127">Si se especifica, la frecuencia de muestreo de entrada debe ser una de las velocidades de muestreo de MPEG válidas.</span><span class="sxs-lookup"><span data-stu-id="e8dda-127">If specified, the input sampling rate must be one of the valid MPEG sampling rates.</span></span><br/>                                                                                             |



 

## <a name="output-media-types"></a><span data-ttu-id="e8dda-128">Tipos de medios de salida</span><span class="sxs-lookup"><span data-stu-id="e8dda-128">Output Media Types</span></span>

<span data-ttu-id="e8dda-129">El descodificador de audio MPEG admitirá hasta cuatro subtipos de medios de salida, en el orden siguiente.</span><span class="sxs-lookup"><span data-stu-id="e8dda-129">The MPEG Audio decoder will support up to four output media subtypes, in the following order.</span></span>

<dl> 1. <span data-ttu-id="e8dda-130">Estéreo, punto flotante.</span><span class="sxs-lookup"><span data-stu-id="e8dda-130">Stereo, floating point.</span></span>  
2. <span data-ttu-id="e8dda-131">PCM de 16 bits estéreo.</span><span class="sxs-lookup"><span data-stu-id="e8dda-131">Stereo, 16-bit PCM.</span></span>  
3. <span data-ttu-id="e8dda-132">Mono, punto flotante (solo si la entrada es mono o dual mono).</span><span class="sxs-lookup"><span data-stu-id="e8dda-132">Mono, floating point (only if the input is mono or dual-mono).</span></span>  
4. <span data-ttu-id="e8dda-133">Mono de 16 bits, PCM (solo si la entrada es mono o dual mono).</span><span class="sxs-lookup"><span data-stu-id="e8dda-133">Mono, 16-bit PCM (only if the input is mono or dual-mono).</span></span>  
</dl>

<span data-ttu-id="e8dda-134">El descodificador siempre admite la salida estéreo y se enumera como el primer tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="e8dda-134">The decoder always supports stereo output and it is enumerated as the first output media type.</span></span>

<span data-ttu-id="e8dda-135">El descodificador admite los siguientes atributos de tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="e8dda-135">The decoder supports the following output media type attributes.</span></span>



| <span data-ttu-id="e8dda-136">Atributo</span><span class="sxs-lookup"><span data-stu-id="e8dda-136">Attribute</span></span>                                                                           | <span data-ttu-id="e8dda-137">Value</span><span class="sxs-lookup"><span data-stu-id="e8dda-137">Value</span></span>                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="e8dda-138">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="e8dda-138">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="e8dda-139">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e8dda-139">**MFMediaType\_Audio**</span></span>                                                     |
| [<span data-ttu-id="e8dda-140">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="e8dda-140">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="e8dda-141">**MFAudioFormat \_ PCM** o **MFAudioFormat \_ float**</span><span class="sxs-lookup"><span data-stu-id="e8dda-141">Either **MFAudioFormat\_PCM** or **MFAudioFormat\_Float**</span></span>                  |
| [<span data-ttu-id="e8dda-142">MF \_ MT \_ audio \_ bits \_ por \_ muestra</span><span class="sxs-lookup"><span data-stu-id="e8dda-142">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="e8dda-143">16 o 32</span><span class="sxs-lookup"><span data-stu-id="e8dda-143">16 or 32</span></span>                                                                   |
| [<span data-ttu-id="e8dda-144">\_canales de \_ número de audio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="e8dda-144">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="e8dda-145">1 o 2</span><span class="sxs-lookup"><span data-stu-id="e8dda-145">1 or 2</span></span>                                                                     |
| [<span data-ttu-id="e8dda-146">\_máscara de \_ canal de audio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="e8dda-146">MF\_MT\_AUDIO\_CHANNEL\_MASK</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="e8dda-147">0x4 para mono o 0X3 para estéreo</span><span class="sxs-lookup"><span data-stu-id="e8dda-147">0x4 for mono or 0x3 for stereo</span></span>                                             |
| [<span data-ttu-id="e8dda-148">\_muestras de audio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="e8dda-148">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="e8dda-149">Uno de los siguientes: 16000, 22050, 24000, 32000, 44100, 48000.</span><span class="sxs-lookup"><span data-stu-id="e8dda-149">One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span><br/> |



 

## <a name="transform-attributes"></a><span data-ttu-id="e8dda-150">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="e8dda-150">Transform Attributes</span></span>

<span data-ttu-id="e8dda-151">El descodificador de audio MPEG implementa el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="e8dda-151">The MPEG Audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="e8dda-152">Las aplicaciones pueden utilizar este método para obtener o establecer los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e8dda-152">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="e8dda-153">Atributo</span><span class="sxs-lookup"><span data-stu-id="e8dda-153">Attribute</span></span>                                                                               | <span data-ttu-id="e8dda-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8dda-154">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8dda-155">**CODECAPI \_ AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="e8dda-155">**CODECAPI\_AVDecAudioDualMono**</span></span>](../directshow/avdecaudiodualmono-property.md)                   | <span data-ttu-id="e8dda-156">Especifica si el audio de 2 canales que se está descodificando es dual mono o no.</span><span class="sxs-lookup"><span data-stu-id="e8dda-156">Specifies whether 2-channel audio being decoded is dual mono or not.</span></span> <span data-ttu-id="e8dda-157">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e8dda-157">Read-only.</span></span> <span data-ttu-id="e8dda-158">Establecido por la MFT.</span><span class="sxs-lookup"><span data-stu-id="e8dda-158">Set by the MFT.</span></span> <span data-ttu-id="e8dda-159">Para obtener más información, consulte [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span><span class="sxs-lookup"><span data-stu-id="e8dda-159">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span>                                                                                                                               |
| [<span data-ttu-id="e8dda-160">**CODECAPI \_ AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="e8dda-160">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>](../directshow/avdecaudiodualmonorepromode-property.md) | <span data-ttu-id="e8dda-161">Especifica cómo el descodificador Reproduce audio mono dual.</span><span class="sxs-lookup"><span data-stu-id="e8dda-161">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="e8dda-162">El valor predeterminado es **eAVDecAudioDualMonoReproMode \_ \_** a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="e8dda-162">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span><br/> <span data-ttu-id="e8dda-163">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e8dda-163">Read/Write.</span></span> <span data-ttu-id="e8dda-164">Las aplicaciones pueden establecer esta propiedad para cambiar el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e8dda-164">Applications can set this property to change the default behavior.</span></span> <span data-ttu-id="e8dda-165">Para obtener más información, consulte [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span><span class="sxs-lookup"><span data-stu-id="e8dda-165">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span><br/> |
| [<span data-ttu-id="e8dda-166">**CODECAPI \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="e8dda-166">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>](../directshow/avenccommonmeanbitrate-property.md)           | <span data-ttu-id="e8dda-167">Especifica la velocidad de bits de flujo comprimido.</span><span class="sxs-lookup"><span data-stu-id="e8dda-167">Specifies the compressed stream bit rate.</span></span> <span data-ttu-id="e8dda-168">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e8dda-168">Read-only.</span></span> <span data-ttu-id="e8dda-169">Establecido por la MFT.</span><span class="sxs-lookup"><span data-stu-id="e8dda-169">Set by the MFT.</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="e8dda-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8dda-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8dda-171">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="e8dda-171">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
