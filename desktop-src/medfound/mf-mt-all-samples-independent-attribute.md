---
description: Especifica para un tipo de medio si cada ejemplo es independiente de los demás ejemplos de la secuencia.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: MF_MT_ALL_SAMPLES_INDEPENDENT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82173e99a30e033b3d90f6cfec0dc2aa8b3af97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648257"
---
# <a name="mf_mt_all_samples_independent-attribute"></a><span data-ttu-id="4ded9-103">\_ \_ Atributo independiente MF MT All \_ Samples \_</span><span class="sxs-lookup"><span data-stu-id="4ded9-103">MF\_MT\_ALL\_SAMPLES\_INDEPENDENT attribute</span></span>

<span data-ttu-id="4ded9-104">Especifica para un tipo de medio si cada ejemplo es independiente de los demás ejemplos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="4ded9-104">Specifies for a media type whether each sample is independent of the other samples in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="4ded9-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4ded9-105">Data type</span></span>

<span data-ttu-id="4ded9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4ded9-106">**UINT32**</span></span>

<span data-ttu-id="4ded9-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="4ded9-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ded9-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ded9-108">Remarks</span></span>

<span data-ttu-id="4ded9-109">Si este atributo es **false**, algunos ejemplos no se pueden usar sin hacer referencia a otros ejemplos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="4ded9-109">If this attribute is **FALSE**, some samples cannot be used without referring to other samples in the stream.</span></span> <span data-ttu-id="4ded9-110">Por ejemplo, si un formato de vídeo contiene fotogramas Delta, este atributo debe ser **false**.</span><span class="sxs-lookup"><span data-stu-id="4ded9-110">For example, if a video format contains delta frames, this attribute should be **FALSE**.</span></span>

<span data-ttu-id="4ded9-111">Este atributo corresponde al campo **bTemporalCompression** de la estructura de [**\_ \_ tipo de medio**](/windows/win32/api/strmif/ns-strmif-am_media_type) de DirectShow AM.</span><span class="sxs-lookup"><span data-stu-id="4ded9-111">This attribute corresponds to the **bTemporalCompression** field in the DirectShow [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="4ded9-112">Establezca este atributo en **true** para todos los tipos de medios sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="4ded9-112">Set this attribute to **TRUE** for all uncompressed media types.</span></span>

<span data-ttu-id="4ded9-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4ded9-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ded9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ded9-114">Requirements</span></span>



| <span data-ttu-id="4ded9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ded9-115">Requirement</span></span> | <span data-ttu-id="4ded9-116">Value</span><span class="sxs-lookup"><span data-stu-id="4ded9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4ded9-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ded9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4ded9-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="4ded9-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="4ded9-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ded9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4ded9-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="4ded9-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4ded9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ded9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ded9-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ded9-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ded9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ded9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ded9-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ded9-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4ded9-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4ded9-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4ded9-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4ded9-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4ded9-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4ded9-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="4ded9-128">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="4ded9-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
