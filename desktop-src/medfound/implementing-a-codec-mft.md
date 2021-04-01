---
description: En este tema se proporcionan algunas directrices para implementar un descodificador o codificador como una transformación de Media Foundation (MFT).
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: Implementar un MFT de códec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279050"
---
# <a name="implementing-a-codec-mft"></a><span data-ttu-id="59845-103">Implementar un MFT de códec</span><span class="sxs-lookup"><span data-stu-id="59845-103">Implementing a Codec MFT</span></span>

<span data-ttu-id="59845-104">En este tema se proporcionan algunas directrices para implementar un descodificador o codificador como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="59845-104">This topic provides some guidelines for implementing a decoder or encoder as a Media Foundation Transform (MFT) .</span></span>

-   [<span data-ttu-id="59845-105">Codificadores</span><span class="sxs-lookup"><span data-stu-id="59845-105">Encoders</span></span>](#encoders)
    -   [<span data-ttu-id="59845-106">Negociación del formato del codificador</span><span class="sxs-lookup"><span data-stu-id="59845-106">Encoder Format Negotiation</span></span>](#encoder-format-negotiation)
-   [<span data-ttu-id="59845-107">Descodificadores</span><span class="sxs-lookup"><span data-stu-id="59845-107">Decoders</span></span>](#decoders)
    -   [<span data-ttu-id="59845-108">Descodificadores de solo transcodificación</span><span class="sxs-lookup"><span data-stu-id="59845-108">Transcode-Only Decoders</span></span>](#transcode-only-decoders)
    -   [<span data-ttu-id="59845-109">Atributos de telecine</span><span class="sxs-lookup"><span data-stu-id="59845-109">Telecine Attributes</span></span>](#telecine-attributes)
-   [<span data-ttu-id="59845-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59845-110">Related topics</span></span>](#related-topics)

## <a name="encoders"></a><span data-ttu-id="59845-111">Codificadores</span><span class="sxs-lookup"><span data-stu-id="59845-111">Encoders</span></span>

### <a name="encoder-format-negotiation"></a><span data-ttu-id="59845-112">Negociación del formato del codificador</span><span class="sxs-lookup"><span data-stu-id="59845-112">Encoder Format Negotiation</span></span>

<span data-ttu-id="59845-113">El siguiente procedimiento se usa para inicializar un codificador:</span><span class="sxs-lookup"><span data-stu-id="59845-113">The following procedure is used to initialize an encoder:</span></span>

1.  <span data-ttu-id="59845-114">Consulte la MFT para la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="59845-114">Query the MFT for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
2.  <span data-ttu-id="59845-115">Llame a [**ICodecAPI:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) para establecer las propiedades de codificación.</span><span class="sxs-lookup"><span data-stu-id="59845-115">Call [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) to set encoding properties.</span></span>
3.  <span data-ttu-id="59845-116">Llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer el formato de codificación.</span><span class="sxs-lookup"><span data-stu-id="59845-116">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the encoding format.</span></span>
4.  <span data-ttu-id="59845-117">Llame a [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) para obtener una lista de tipos de entrada compatibles.</span><span class="sxs-lookup"><span data-stu-id="59845-117">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to get a list of compatible input types.</span></span> <span data-ttu-id="59845-118">(Este paso se podría omitir).</span><span class="sxs-lookup"><span data-stu-id="59845-118">(This step might be skipped.)</span></span>
5.  <span data-ttu-id="59845-119">Llame a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para establecer el formato de entrada sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="59845-119">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed input format.</span></span>

<span data-ttu-id="59845-120">Después de establecer el tipo de salida en el paso 3, el método [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) debe devolver una lista de tipos de entrada que sean compatibles con el tipo de salida actual.</span><span class="sxs-lookup"><span data-stu-id="59845-120">After the output type is set in step 3, the [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) method must return a list of input types that are compatible with the current output type.</span></span> <span data-ttu-id="59845-121">En otras palabras, los tipos devueltos por **GetInputAvailableType** en este punto deben ser válidos para [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="59845-121">In other words, any types returned by **GetInputAvailableType** at this point must be valid for [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="59845-122">En el caso de los descodificadores, se invierte el orden en el que se establecen los tipos: el tipo de entrada se establece primero, seguido del tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="59845-122">For decoders, the order in which types are set is reversed: The input type is set first, followed by the output type.</span></span> <span data-ttu-id="59845-123">Una vez establecido el tipo de entrada, el método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) debe devolver una lista de tipos que se pueden pasar al método [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) .</span><span class="sxs-lookup"><span data-stu-id="59845-123">After the input type is set, the [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method must return a list of types that can be passed to the [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method.</span></span>

<span data-ttu-id="59845-124">Los codificadores y descodificadores deben admitir NV12 como un formato no comprimido común.</span><span class="sxs-lookup"><span data-stu-id="59845-124">Encoders and decoders should support NV12 as a common uncompressed format.</span></span> <span data-ttu-id="59845-125">Esto garantiza que los componentes de canalización pueden interoperar con conversiones mínimas de ColorSpace.</span><span class="sxs-lookup"><span data-stu-id="59845-125">This ensures that pipeline components can interoperate with minimal colorspace conversions.</span></span> <span data-ttu-id="59845-126">Por supuesto, también se pueden admitir otros formatos.</span><span class="sxs-lookup"><span data-stu-id="59845-126">Of course, other formats can be supported as well.</span></span>

## <a name="decoders"></a><span data-ttu-id="59845-127">Descodificadores</span><span class="sxs-lookup"><span data-stu-id="59845-127">Decoders</span></span>

### <a name="transcode-only-decoders"></a><span data-ttu-id="59845-128">Descodificadores Transcode-Only</span><span class="sxs-lookup"><span data-stu-id="59845-128">Transcode-Only Decoders</span></span>

<span data-ttu-id="59845-129">Algunos descodificadores están optimizados para la transcodificación (descodificación y recodificación de una secuencia) y no son adecuados para su uso durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="59845-129">Some decoders are optimized for transcoding (decoding and then re-encoding a stream) and are not suitable for use during playback.</span></span>

<span data-ttu-id="59845-130">Si una MFT del descodificador está destinada únicamente a la transcodificación, establezca la marca de **\_ enumeración de MFT \_ \_ \_ solo Transcode** Flag al registrar la MFT.</span><span class="sxs-lookup"><span data-stu-id="59845-130">If a decoder MFT is intended only for transcoding, set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when you register the MFT.</span></span> <span data-ttu-id="59845-131">(Consulte [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)).</span><span class="sxs-lookup"><span data-stu-id="59845-131">(See [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)</span></span>

<span data-ttu-id="59845-132">De forma predeterminada, la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) no devuelve los descodificadores de Transcode.</span><span class="sxs-lookup"><span data-stu-id="59845-132">By default, transcode decoders are not returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="59845-133">Para enumerar los descodificadores de transcodificación, llame a **MFTEnumEx** y establezca la marca de **\_ enumeración de MFT \_ \_ \_ solo** en el parámetro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="59845-133">To enumerate transcode decoders, call **MFTEnumEx** and set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in *Flags* parameter.</span></span> <span data-ttu-id="59845-134">Cuando se usa en la función **MFTEnumEx** , este marcador enumera los descodificadores de transcodificación y otros descodificadores.</span><span class="sxs-lookup"><span data-stu-id="59845-134">When used in the **MFTEnumEx** function, this flag enumerated both transcode decoders and other decoders.</span></span>



| <span data-ttu-id="59845-135">MFTRegister **\_ marca de enumeración de MFT \_ \_ \_ solo Transcode**</span><span class="sxs-lookup"><span data-stu-id="59845-135">MFTRegister **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="59845-136">MFTEnumEx **\_ marca de enumeración de MFT \_ \_ \_ solo Transcode**</span><span class="sxs-lookup"><span data-stu-id="59845-136">MFTEnumEx **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="59845-137">¿Se ha enumerado MFT?</span><span class="sxs-lookup"><span data-stu-id="59845-137">Is MFT Enumerated?</span></span> |
|--------------------------------------------------|------------------------------------------------|--------------------|
| <span data-ttu-id="59845-138">1</span><span class="sxs-lookup"><span data-stu-id="59845-138">1</span></span>                                                | <span data-ttu-id="59845-139">1</span><span class="sxs-lookup"><span data-stu-id="59845-139">1</span></span>                                              | <span data-ttu-id="59845-140">Sí</span><span class="sxs-lookup"><span data-stu-id="59845-140">Yes</span></span>                |
| <span data-ttu-id="59845-141">1</span><span class="sxs-lookup"><span data-stu-id="59845-141">1</span></span>                                                | <span data-ttu-id="59845-142">0</span><span class="sxs-lookup"><span data-stu-id="59845-142">0</span></span>                                              | <span data-ttu-id="59845-143">No</span><span class="sxs-lookup"><span data-stu-id="59845-143">No</span></span>                 |
| <span data-ttu-id="59845-144">0</span><span class="sxs-lookup"><span data-stu-id="59845-144">0</span></span>                                                | <span data-ttu-id="59845-145">1</span><span class="sxs-lookup"><span data-stu-id="59845-145">1</span></span>                                              | <span data-ttu-id="59845-146">Sí</span><span class="sxs-lookup"><span data-stu-id="59845-146">Yes</span></span>                |
| <span data-ttu-id="59845-147">0</span><span class="sxs-lookup"><span data-stu-id="59845-147">0</span></span>                                                | <span data-ttu-id="59845-148">0</span><span class="sxs-lookup"><span data-stu-id="59845-148">0</span></span>                                              | <span data-ttu-id="59845-149">Sí</span><span class="sxs-lookup"><span data-stu-id="59845-149">Yes</span></span>                |



 

### <a name="telecine-attributes"></a><span data-ttu-id="59845-150">Atributos de telecine</span><span class="sxs-lookup"><span data-stu-id="59845-150">Telecine Attributes</span></span>

<span data-ttu-id="59845-151">El origen multimedia podría adjuntar los siguientes atributos de telecine a los ejemplos de medios que ofrece.</span><span class="sxs-lookup"><span data-stu-id="59845-151">The media source might attach the following telecine attributes to the media samples that it delivers.</span></span>



| <span data-ttu-id="59845-152">Atributo</span><span class="sxs-lookup"><span data-stu-id="59845-152">Attribute</span></span>                                                                                   | <span data-ttu-id="59845-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="59845-153">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="59845-154">**MFSampleExtension \_ RepeatFirstField**</span><span class="sxs-lookup"><span data-stu-id="59845-154">**MFSampleExtension\_RepeatFirstField**</span></span>](mfsampleextension-repeatfirstfield-attribute.md) | <span data-ttu-id="59845-155">Equivalente a la marca "repetir primer campo" (RFF).</span><span class="sxs-lookup"><span data-stu-id="59845-155">Equivalent to "repeat first field" (RFF) flag.</span></span> |
| [<span data-ttu-id="59845-156">**MFSampleExtension \_ BottomFieldFirst**</span><span class="sxs-lookup"><span data-stu-id="59845-156">**MFSampleExtension\_BottomFieldFirst**</span></span>](mfsampleextension-bottomfieldfirst-attribute.md) | <span data-ttu-id="59845-157">Inversa del marcador "primer campo primero" (TFF).</span><span class="sxs-lookup"><span data-stu-id="59845-157">Inverse of "top field first" (TFF) flag.</span></span>       |



 

<span data-ttu-id="59845-158">Estas marcas proporcionan una sugerencia al representador de vídeo mejorado (EVR) cuando realiza el desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="59845-158">These flags provide a hint to the enhanced video renderer (EVR) when it performs deinterlacing.</span></span> <span data-ttu-id="59845-159">Un descodificador debe propagar estas marcas de nivel inferior copiándolas a los ejemplos de salida, de modo que lleguen a EVR.</span><span class="sxs-lookup"><span data-stu-id="59845-159">A decoder should propagate these flags downstream by copying them to the output samples, so that they reach the EVR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59845-160">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59845-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59845-161">Escribir una MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="59845-161">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
