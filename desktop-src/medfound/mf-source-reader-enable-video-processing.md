---
description: Habilita el procesamiento de vídeo por el lector de origen.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497357"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a><span data-ttu-id="3d1a7-103">\_Lector de código fuente MF \_ \_ Habilitar atributo de \_ procesamiento de vídeo \_</span><span class="sxs-lookup"><span data-stu-id="3d1a7-103">MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="3d1a7-104">Habilita el procesamiento de vídeo por el [lector de origen](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="3d1a7-104">Enables video processing by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="3d1a7-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3d1a7-105">Data type</span></span>

<span data-ttu-id="3d1a7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3d1a7-106">**UINT32**</span></span>



| <span data-ttu-id="3d1a7-107">Value</span><span class="sxs-lookup"><span data-stu-id="3d1a7-107">Value</span></span>                                                                                                                                                                | <span data-ttu-id="3d1a7-108">Significado</span><span class="sxs-lookup"><span data-stu-id="3d1a7-108">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <span data-ttu-id="3d1a7-109"><dt>**Distinto**</dt></span><span class="sxs-lookup"><span data-stu-id="3d1a7-109"><dt>**Nonzero**</dt></span></span> </dl> | <span data-ttu-id="3d1a7-110">Habilitar el procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3d1a7-110">Enable video processing.</span></span><br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <span data-ttu-id="3d1a7-111"><dt>**Nulo**</dt></span><span class="sxs-lookup"><span data-stu-id="3d1a7-111"><dt>**Zero**</dt></span></span> </dl>             | <span data-ttu-id="3d1a7-112">Deshabilitar el procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3d1a7-112">Disable video processing.</span></span> <span data-ttu-id="3d1a7-113">(Es el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="3d1a7-113">(Default)</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="3d1a7-114">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="3d1a7-114">Get/set</span></span>

<span data-ttu-id="3d1a7-115">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="3d1a7-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3d1a7-116">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="3d1a7-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d1a7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d1a7-117">Remarks</span></span>

<span data-ttu-id="3d1a7-118">Si este atributo es **true** (distinto de cero), el lector de origen puede realizar el siguiente procesamiento de vídeo limitado en fotogramas de vídeo sin comprimir:</span><span class="sxs-lookup"><span data-stu-id="3d1a7-118">If this attribute is **TRUE** (nonzero), the source reader can perform the following limited video processing on uncompressed video frames:</span></span>

-   <span data-ttu-id="3d1a7-119">Conversión de YUV a RGB-32.</span><span class="sxs-lookup"><span data-stu-id="3d1a7-119">Conversion from YUV to RGB-32.</span></span>
-   <span data-ttu-id="3d1a7-120">Desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="3d1a7-120">Deinterlacing.</span></span>

<span data-ttu-id="3d1a7-121">Estas operaciones se realizan en el software y no están optimizadas para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="3d1a7-121">These operations are performed in software, and are not optimized for playback.</span></span> <span data-ttu-id="3d1a7-122">Esta característica está destinada a las aplicaciones que procesan un pequeño número de fotogramas, por ejemplo, para crear una miniatura de vídeo, o aplicaciones que no descodifican fotogramas en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="3d1a7-122">This feature is intended for applications that process a small number of frames—for example, to create a video thumbnail—or applications that do not decode frames in real time.</span></span> <span data-ttu-id="3d1a7-123">La operación de desentrelazado interpola los datos de un solo campo, por lo que es una pérdida.</span><span class="sxs-lookup"><span data-stu-id="3d1a7-123">The deinterlace operation interpolates data from a single field, so it is lossy.</span></span>

<span data-ttu-id="3d1a7-124">Evite esta opción si usa Direct3D para mostrar los fotogramas de vídeo, ya que la GPU suele proporcionar mejores capacidades de procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3d1a7-124">Avoid this setting if you are using Direct3D to display the video frames, because the GPU generally provides better video processing capabilities.</span></span>

<span data-ttu-id="3d1a7-125">Si este atributo es **true**, los siguientes atributos deben ser **false**:</span><span class="sxs-lookup"><span data-stu-id="3d1a7-125">If this attribute is **TRUE**, the following attributes must be **FALSE**:</span></span>

-   [<span data-ttu-id="3d1a7-126">\_Administrador de \_ D3D de lector de origen MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="3d1a7-126">MF\_SOURCE\_READER\_D3D\_MANAGER</span></span>](mf-source-reader-d3d-manager.md)
-   [<span data-ttu-id="3d1a7-127">MF \_ ReadWrite \_ deshabilitar \_ convertidores</span><span class="sxs-lookup"><span data-stu-id="3d1a7-127">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)

## <a name="requirements"></a><span data-ttu-id="3d1a7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d1a7-128">Requirements</span></span>



| <span data-ttu-id="3d1a7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d1a7-129">Requirement</span></span> | <span data-ttu-id="3d1a7-130">Value</span><span class="sxs-lookup"><span data-stu-id="3d1a7-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1a7-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d1a7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3d1a7-132">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="3d1a7-132">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="3d1a7-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d1a7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3d1a7-134">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="3d1a7-134">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3d1a7-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d1a7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d1a7-136"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d1a7-136"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d1a7-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d1a7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d1a7-138">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d1a7-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3d1a7-139">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="3d1a7-139">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="3d1a7-140">Atributos del lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="3d1a7-140">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




