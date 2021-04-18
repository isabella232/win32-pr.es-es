---
description: Especifica los elementos primarios de color para un tipo de medio de vídeo.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: MF_MT_VIDEO_PRIMARIES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716958"
---
# <a name="mf_mt_video_primaries-attribute"></a><span data-ttu-id="ac753-103">\_ \_ Atributo primarios de vídeo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="ac753-103">MF\_MT\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="ac753-104">Especifica los elementos primarios de color para un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ac753-104">Specifies the color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="ac753-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ac753-105">Data type</span></span>

<span data-ttu-id="ac753-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ac753-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ac753-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac753-107">Remarks</span></span>

<span data-ttu-id="ac753-108">El valor de este atributo es un miembro de la enumeración [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) .</span><span class="sxs-lookup"><span data-stu-id="ac753-108">The value of this attribute is a member of the [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration.</span></span>

<span data-ttu-id="ac753-109">La enumeración [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) identifica los primarios de color asociados a determinados estándares de vídeo comunes.</span><span class="sxs-lookup"><span data-stu-id="ac753-109">The [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration identifies color primaries associated with certain common video standards.</span></span> <span data-ttu-id="ac753-110">Si el tipo de medio usa elementos primarios de color que no se identifican en la enumeración **MFVideoPrimaries** , establezca el atributo de [**\_ \_ \_ \_ primarios de vídeo personalizado MF MT**](mf-mt-custom-video-primaries-attribute.md) en lugar de este atributo.</span><span class="sxs-lookup"><span data-stu-id="ac753-110">If the media type uses color primaries that are not identified in the **MFVideoPrimaries** enumeration, set the [**MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES**](mf-mt-custom-video-primaries-attribute.md) attribute instead of this attribute.</span></span>

<span data-ttu-id="ac753-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ac753-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac753-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac753-112">Requirements</span></span>



| <span data-ttu-id="ac753-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac753-113">Requirement</span></span> | <span data-ttu-id="ac753-114">Value</span><span class="sxs-lookup"><span data-stu-id="ac753-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac753-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac753-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ac753-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="ac753-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ac753-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac753-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ac753-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ac753-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ac753-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac753-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac753-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac753-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac753-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac753-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac753-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac753-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ac753-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ac753-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ac753-124">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ac753-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ac753-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ac753-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ac753-126">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="ac753-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="ac753-127">Información de color ampliada</span><span class="sxs-lookup"><span data-stu-id="ac753-127">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




