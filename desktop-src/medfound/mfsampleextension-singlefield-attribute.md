---
description: Especifica si un ejemplo de vídeo contiene un solo campo o dos campos intercalados. Este atributo se aplica a los ejemplos de medios.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: MFSampleExtension_SingleField atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d7c43a9777982485ba350d259a59a518e26c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543926"
---
# <a name="mfsampleextension_singlefield-attribute"></a><span data-ttu-id="887fe-104">\_Atributo SingleField de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="887fe-104">MFSampleExtension\_SingleField attribute</span></span>

<span data-ttu-id="887fe-105">Especifica si un ejemplo de vídeo contiene un solo campo o dos campos intercalados.</span><span class="sxs-lookup"><span data-stu-id="887fe-105">Specifies whether a video sample contains a single field or two interleaved fields.</span></span> <span data-ttu-id="887fe-106">Este atributo se aplica a los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="887fe-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="887fe-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="887fe-107">Data type</span></span>

<span data-ttu-id="887fe-108">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="887fe-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="887fe-109">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="887fe-109">Get/set</span></span>

<span data-ttu-id="887fe-110">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="887fe-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="887fe-111">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="887fe-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="887fe-112">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="887fe-112">Applies to</span></span>

[<span data-ttu-id="887fe-113">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="887fe-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="887fe-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="887fe-114">Remarks</span></span>

<span data-ttu-id="887fe-115">Si el valor es **true**, el ejemplo contiene un campo.</span><span class="sxs-lookup"><span data-stu-id="887fe-115">If the value is **TRUE**, the sample contains one field.</span></span> <span data-ttu-id="887fe-116">Si el valor es **false** o el atributo no está establecido, el ejemplo contiene un marco completo.</span><span class="sxs-lookup"><span data-stu-id="887fe-116">If the value is **FALSE** or the attribute is not set, the sample contains a complete frame.</span></span> <span data-ttu-id="887fe-117">(Dos campos, si están entrelazados, o un marco progresivo).</span><span class="sxs-lookup"><span data-stu-id="887fe-117">(Two fields if interlaced, or a progressive frame.)</span></span>

<span data-ttu-id="887fe-118">Si el tipo de medio es fotogramas progresivos o campos intercalados, este atributo debe ser **falso** o dejar sin establecer.</span><span class="sxs-lookup"><span data-stu-id="887fe-118">If the media type is progressive frames or interleaved fields, this attribute must be **FALSE** or left unset.</span></span>

<span data-ttu-id="887fe-119">Si el tipo de medio es un campo único, este atributo debe ser **true**.</span><span class="sxs-lookup"><span data-stu-id="887fe-119">If the media type is single field, this attribute must be **TRUE**.</span></span> <span data-ttu-id="887fe-120">Establezca el atributo [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) en el ejemplo para indicar si es el campo superior o el campo inferior.</span><span class="sxs-lookup"><span data-stu-id="887fe-120">Set the [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute on the sample to indicate whether it is the upper field or the lower field.</span></span>

<span data-ttu-id="887fe-121">Actualmente, el representador de vídeo mejorado (EVR) no admite contenido que cambie entre fotogramas entrelazados y campos individuales.</span><span class="sxs-lookup"><span data-stu-id="887fe-121">Currently the enhanced video renderer (EVR) does not support content that switches between interlaced frames and single fields.</span></span>

<span data-ttu-id="887fe-122">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="887fe-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="887fe-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="887fe-123">Requirements</span></span>



| <span data-ttu-id="887fe-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="887fe-124">Requirement</span></span> | <span data-ttu-id="887fe-125">Value</span><span class="sxs-lookup"><span data-stu-id="887fe-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="887fe-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="887fe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="887fe-127">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="887fe-127">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="887fe-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="887fe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="887fe-129">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="887fe-129">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="887fe-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="887fe-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="887fe-131"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="887fe-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="887fe-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="887fe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887fe-133">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="887fe-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="887fe-134">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="887fe-134">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="887fe-135">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="887fe-135">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="887fe-136">Entrelazado de vídeo</span><span class="sxs-lookup"><span data-stu-id="887fe-136">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




