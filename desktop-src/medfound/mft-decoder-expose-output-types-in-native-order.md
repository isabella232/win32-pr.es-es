---
description: Especifica si un descodificador expone los tipos de salida IYUV/i420 (adecuados para la transcodificación) antes de otros formatos.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ecf074fa0767552a48e3238374dbd02f077404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812608"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a><span data-ttu-id="43273-103">\_DEScodificador \_ de MFT \_ exponer \_ tipos \_ de salida en el \_ atributo de \_ orden nativo</span><span class="sxs-lookup"><span data-stu-id="43273-103">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER attribute</span></span>

<span data-ttu-id="43273-104">Especifica si un descodificador expone los tipos de salida IYUV/i420 (adecuados para la transcodificación) antes de otros formatos.</span><span class="sxs-lookup"><span data-stu-id="43273-104">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span>

## <a name="data-type"></a><span data-ttu-id="43273-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="43273-105">Data type</span></span>

<span data-ttu-id="43273-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="43273-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="43273-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43273-107">Remarks</span></span>

<span data-ttu-id="43273-108">Este atributo es una sugerencia para que el descodificador organice su lista de tipos de salida en un orden determinado, en función del uso previsto, ya sea de reproducción o de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="43273-108">This attribute is a hint for the decoder to arrange its list of output types in a particular order, depending on the intended use, either playback or transcode.</span></span>

<span data-ttu-id="43273-109">Para la mayoría de los formatos de codificación (H. 264, MPEG-2, WMV), los descodificadores de vídeo de Microsoft Media Foundation admiten varias salidas YUV comunes, como NV12, YV12, YUY2, IYUV y i420.</span><span class="sxs-lookup"><span data-stu-id="43273-109">For most encoding formats (H.264, MPEG-2, WMV), the video decoders in Microsoft Media Foundation support several common YUV outputs, including NV12, YV12, YUY2, IYUV, and I420.</span></span> <span data-ttu-id="43273-110">El descodificador ofrece una lista ordenada de tipos de salida a través de su método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) .</span><span class="sxs-lookup"><span data-stu-id="43273-110">The decoder offers an ordered list of output types through its [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

<span data-ttu-id="43273-111">Para la reproducción, NV12 es el formato más eficaz y ampliamente compatible.</span><span class="sxs-lookup"><span data-stu-id="43273-111">For playback, NV12 is the most efficient and widely supported format.</span></span> <span data-ttu-id="43273-112">Por consiguiente, de forma predeterminada, los descodificadores suelen ofrecer NV12 como primer tipo de salida en la lista.</span><span class="sxs-lookup"><span data-stu-id="43273-112">Therefore, by default, decoders typically offer NV12 as the first output type in the list.</span></span> <span data-ttu-id="43273-113">Esto minimiza el tiempo necesario para resolver el tipo de medio al compilar una topología de reproducción.</span><span class="sxs-lookup"><span data-stu-id="43273-113">This minimizes the time needed to resolve the media type when building a playback topology.</span></span> <span data-ttu-id="43273-114">Para la transcodificación, sin embargo, IYUV o i420 son más eficaces para la CPU y suelen ser preferidas por los codificadores.</span><span class="sxs-lookup"><span data-stu-id="43273-114">For transcoding, however, IYUV or I420 are more efficient for the CPU and are typically preferred by encoders.</span></span>

<span data-ttu-id="43273-115">Si un descodificador admite este atributo, el atributo tiene el siguiente comportamiento:</span><span class="sxs-lookup"><span data-stu-id="43273-115">If a decoder supports this attribute, the attribute has the following behavior:</span></span>

-   <span data-ttu-id="43273-116">Si el atributo tiene un valor distinto de cero, IYUV y i420 aparecen en primer lugar en la lista de tipos de medios de salida.</span><span class="sxs-lookup"><span data-stu-id="43273-116">If the attribute has a non-zero value, IYUV and I420 appear first in the list of output media types.</span></span> <span data-ttu-id="43273-117">Esta configuración es más eficaz para la transcodificación.</span><span class="sxs-lookup"><span data-stu-id="43273-117">This setting is most efficient for transcoding.</span></span>
-   <span data-ttu-id="43273-118">Si el atributo es cero, NV12 aparece en primer lugar en la lista de tipos de medios de salida.</span><span class="sxs-lookup"><span data-stu-id="43273-118">If the attribute is zero, NV12 appears first in the list of output media types.</span></span> <span data-ttu-id="43273-119">Esta configuración es la más eficaz para la reproducción y es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="43273-119">This setting is most efficient for playback, and is the default.</span></span>

<span data-ttu-id="43273-120">Para establecer este atributo:</span><span class="sxs-lookup"><span data-stu-id="43273-120">To set this attribute:</span></span>

1.  <span data-ttu-id="43273-121">Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el descodificador para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="43273-121">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="43273-122">Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para agregar el atributo.</span><span class="sxs-lookup"><span data-stu-id="43273-122">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="43273-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43273-123">Requirements</span></span>



| <span data-ttu-id="43273-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="43273-124">Requirement</span></span> | <span data-ttu-id="43273-125">Value</span><span class="sxs-lookup"><span data-stu-id="43273-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43273-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43273-126">Minimum supported client</span></span><br/> | <span data-ttu-id="43273-127">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="43273-127">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="43273-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43273-128">Minimum supported server</span></span><br/> | <span data-ttu-id="43273-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="43273-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="43273-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43273-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="43273-131"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="43273-131"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43273-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="43273-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43273-133">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="43273-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




