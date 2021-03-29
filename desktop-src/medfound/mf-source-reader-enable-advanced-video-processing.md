---
description: Permite el procesamiento de vídeo avanzado por el lector de origen, incluida la conversión del espacio de colores, el desentrelazado, el cambio de tamaño de vídeo y la conversión de velocidad de fotogramas.
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541355"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a><span data-ttu-id="86df0-103">\_Lector de código fuente MF \_ \_ Habilitar atributo de \_ \_ procesamiento de vídeo avanzado \_</span><span class="sxs-lookup"><span data-stu-id="86df0-103">MF\_SOURCE\_READER\_ENABLE\_ADVANCED\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="86df0-104">Permite el procesamiento de vídeo avanzado por el [lector de origen](source-reader.md), incluida la conversión del espacio de colores, el desentrelazado, el cambio de tamaño de vídeo y la conversión de velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="86df0-104">Enables advanced video processing by the [Source Reader](source-reader.md), including color space conversion, deinterlacing, video resizing, and frame-rate conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="86df0-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="86df0-105">Data type</span></span>

<span data-ttu-id="86df0-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="86df0-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="86df0-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86df0-107">Remarks</span></span>

<span data-ttu-id="86df0-108">Si este atributo es **true**, el lector de origen puede insertar un procesador de vídeo en la canalización de procesamiento, lo que permite los siguientes tipos de conversión de formato:</span><span class="sxs-lookup"><span data-stu-id="86df0-108">If this attribute is **TRUE**, the Source Reader can insert a video processor into the processing pipeline, which enables the following types of format conversion:</span></span>

-   <span data-ttu-id="86df0-109">Conversión de espacio de colores (YUV a RGB-32)</span><span class="sxs-lookup"><span data-stu-id="86df0-109">Color space conversion (YUV to RGB-32)</span></span>
-   <span data-ttu-id="86df0-110">Desentrelazado</span><span class="sxs-lookup"><span data-stu-id="86df0-110">Deinterlacing</span></span>
-   <span data-ttu-id="86df0-111">Cambio de tamaño de vídeo</span><span class="sxs-lookup"><span data-stu-id="86df0-111">Video resizing</span></span>
-   <span data-ttu-id="86df0-112">Conversión de velocidad de fotogramas</span><span class="sxs-lookup"><span data-stu-id="86df0-112">Frame-rate conversion</span></span>

<span data-ttu-id="86df0-113">Si este atributo es **true**, el atributo [MF \_ ReadWrite \_ Disable \_ Converters](mf-readwrite-disable-converters.md) debe ser **false**.</span><span class="sxs-lookup"><span data-stu-id="86df0-113">If this attribute is **TRUE**, the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute must be **FALSE**.</span></span>

<span data-ttu-id="86df0-114">El lector de origen busca los procesadores de vídeo que están registrados en la categoría de **\_ \_ \_ procesador de vídeo categoría de MFT** , incluidos los MFTs registrados para el proceso local.</span><span class="sxs-lookup"><span data-stu-id="86df0-114">The Source Reader looks for video processors that are registered in the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category, including MFTs that are registered for the local process.</span></span> <span data-ttu-id="86df0-115">(Consulte [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) para obtener más información sobre el registro local de MFTs). El lector de origen usa el procesador de vídeo de Transcode (XVP) si no se encuentra ningún otro procesador de vídeo adecuado.</span><span class="sxs-lookup"><span data-stu-id="86df0-115">(See [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) for more information about local registration of MFTs.) The Source Reader uses the Transcode Video Processor (XVP) if no other suitable video processor is found.</span></span>

<span data-ttu-id="86df0-116">La aplicación especifica el tipo de salida deseado llamando a [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="86df0-116">The application specifies the desired output type by calling [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span> <span data-ttu-id="86df0-117">Cuando el lector de origen configura el procesador de vídeo, intenta coincidir con los siguientes atributos del tipo de salida:</span><span class="sxs-lookup"><span data-stu-id="86df0-117">When the Source Reader configures the video processor, it attempts to match the following attributes of the output type:</span></span>

-   <span data-ttu-id="86df0-118">Velocidad de fotogramas ([ \_ \_ \_ velocidad de fotogramas MF MT](mf-mt-frame-rate-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="86df0-118">Frame rate ([MF\_MT\_FRAME\_RATE](mf-mt-frame-rate-attribute.md))</span></span>
-   <span data-ttu-id="86df0-119">Tamaño de marco ([MF \_ MT \_ Frame \_ size](mf-mt-frame-size-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="86df0-119">Frame size ([MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md))</span></span>
-   <span data-ttu-id="86df0-120">Modo entrelazado[( \_ \_ \_ modo entrelazado MF MT](mf-mt-interlace-mode-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="86df0-120">Interlace mode ([MF\_MT\_INTERLACE\_MODE](mf-mt-interlace-mode-attribute.md))</span></span>
-   <span data-ttu-id="86df0-121">Relación de aspecto de píxeles ([ \_ relación de aspecto de \_ píxeles \_ \_ MF MT](mf-mt-pixel-aspect-ratio-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="86df0-121">Pixel aspect ratio ([MF\_MT\_PIXEL\_ASPECT\_RATIO](mf-mt-pixel-aspect-ratio-attribute.md))</span></span>
-   <span data-ttu-id="86df0-122">Subtipo ([ \_ \_ subtipo MF MT](mf-mt-subtype-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="86df0-122">Subtype ([MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md))</span></span>

<span data-ttu-id="86df0-123">Este atributo es similar al del [ \_ lector de código fuente MF habilitar el atributo de \_ \_ \_ \_ procesamiento de vídeo](mf-source-reader-enable-video-processing.md) , pero ofrece las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="86df0-123">This attribute is similar to the [MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING](mf-source-reader-enable-video-processing.md) attribute, but offers the following advantages:</span></span>

-   <span data-ttu-id="86df0-124">Se admite un mayor número de conversiones de formato.</span><span class="sxs-lookup"><span data-stu-id="86df0-124">A greater range of format conversions is supported.</span></span>
-   <span data-ttu-id="86df0-125">Las aplicaciones pueden registrar sus propios convertidores.</span><span class="sxs-lookup"><span data-stu-id="86df0-125">Applications can register their own converters.</span></span>
-   <span data-ttu-id="86df0-126">Algunas conversiones se pueden realizar en el hardware mediante la GPU.</span><span class="sxs-lookup"><span data-stu-id="86df0-126">Some conversions can be performed in hardware using the GPU.</span></span>

## <a name="requirements"></a><span data-ttu-id="86df0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86df0-127">Requirements</span></span>



| <span data-ttu-id="86df0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="86df0-128">Requirement</span></span> | <span data-ttu-id="86df0-129">Value</span><span class="sxs-lookup"><span data-stu-id="86df0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86df0-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86df0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="86df0-131">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="86df0-131">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="86df0-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86df0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="86df0-133">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="86df0-133">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="86df0-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86df0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="86df0-135"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="86df0-135"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86df0-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="86df0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86df0-137">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="86df0-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="86df0-138">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="86df0-138">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="86df0-139">Atributos del lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="86df0-139">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




