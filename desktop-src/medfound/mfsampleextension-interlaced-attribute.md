---
description: Indica si un fotograma de vídeo está entrelazado o progresivo.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: MFSampleExtension_Interlaced atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720446"
---
# <a name="mfsampleextension_interlaced-attribute"></a><span data-ttu-id="721f3-103">\_Atributo entrelazado MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="721f3-103">MFSampleExtension\_Interlaced attribute</span></span>

<span data-ttu-id="721f3-104">Indica si un fotograma de vídeo está entrelazado o progresivo.</span><span class="sxs-lookup"><span data-stu-id="721f3-104">Indicates whether a video frame is interlaced or progressive.</span></span> <span data-ttu-id="721f3-105">Si es **true**, el marco está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="721f3-105">If **TRUE**, the frame is interlaced.</span></span> <span data-ttu-id="721f3-106">Si es **false**, el marco es progresivo.</span><span class="sxs-lookup"><span data-stu-id="721f3-106">If **FALSE**, the frame is progressive.</span></span> <span data-ttu-id="721f3-107">Si no se establece, el tipo de medio describe el entrelazado.</span><span class="sxs-lookup"><span data-stu-id="721f3-107">If not set, the media type describes the interlacing.</span></span> <span data-ttu-id="721f3-108">Este atributo se aplica a los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="721f3-108">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="721f3-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="721f3-109">Data type</span></span>

<span data-ttu-id="721f3-110">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="721f3-110">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="721f3-111">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="721f3-111">Get/set</span></span>

<span data-ttu-id="721f3-112">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="721f3-112">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="721f3-113">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="721f3-113">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="721f3-114">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="721f3-114">Applies to</span></span>

[<span data-ttu-id="721f3-115">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="721f3-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="721f3-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="721f3-116">Remarks</span></span>

<span data-ttu-id="721f3-117">En el caso de contenido de vídeo que contenga fotogramas progresivos e entrelazados mixtos, establezca el tipo de medio en entrelazado y use este atributo en cada fotograma para indicar si el marco es progresivo o entrelazado.</span><span class="sxs-lookup"><span data-stu-id="721f3-117">For video content that contains mixed progressive and interlaced frames, set the media type to interlaced and use this attribute on each frame to indicate whether the frame is progressive or interlaced.</span></span>

<span data-ttu-id="721f3-118">Para el contenido de vídeo que está totalmente entrelazado, establezca el tipo de medio en entrelazado y Omita este atributo, o establézcalo en **true** en cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="721f3-118">For video content that is entirely interlaced, set the media type to interlaced and omit this attribute, or set it to **TRUE** on every sample.</span></span>

<span data-ttu-id="721f3-119">Para el contenido de vídeo que es totalmente progresivo, establezca el tipo de medio en progresivo y Omita este atributo, o establézcalo en **false** en cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="721f3-119">For video content that is entirely progressive, set the media type to progressive and omit this attribute, or set it to **FALSE** on every sample.</span></span>

<span data-ttu-id="721f3-120">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="721f3-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="721f3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="721f3-121">Requirements</span></span>



| <span data-ttu-id="721f3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="721f3-122">Requirement</span></span> | <span data-ttu-id="721f3-123">Value</span><span class="sxs-lookup"><span data-stu-id="721f3-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="721f3-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="721f3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="721f3-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="721f3-125">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="721f3-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="721f3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="721f3-127">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="721f3-127">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="721f3-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="721f3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="721f3-129"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="721f3-129"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="721f3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="721f3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="721f3-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="721f3-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="721f3-132">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="721f3-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="721f3-133">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="721f3-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="721f3-134">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="721f3-134">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="721f3-135">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="721f3-135">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="721f3-136">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="721f3-136">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="721f3-137">Entrelazado de vídeo</span><span class="sxs-lookup"><span data-stu-id="721f3-137">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




