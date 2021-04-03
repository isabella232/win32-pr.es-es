---
description: GUID de subtipo para un tipo de medio.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: MF_MT_SUBTYPE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082727"
---
# <a name="mf_mt_subtype-attribute"></a><span data-ttu-id="67f1d-103">\_Atributo de \_ subtipo MF MT</span><span class="sxs-lookup"><span data-stu-id="67f1d-103">MF\_MT\_SUBTYPE attribute</span></span>

<span data-ttu-id="67f1d-104">GUID de subtipo para un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="67f1d-104">Subtype GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="67f1d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="67f1d-105">Data type</span></span>

<span data-ttu-id="67f1d-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="67f1d-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="67f1d-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67f1d-107">Remarks</span></span>

<span data-ttu-id="67f1d-108">El GUID del subtipo define un tipo de formato multimedia específico dentro de un tipo principal.</span><span class="sxs-lookup"><span data-stu-id="67f1d-108">The subtype GUID defines a specific media format type within a major type.</span></span> <span data-ttu-id="67f1d-109">Por ejemplo, en el vídeo, los subtipos son RGB-24, RGB-32, UYVY, AYUV, etc.</span><span class="sxs-lookup"><span data-stu-id="67f1d-109">For example, within video, the subtypes include RGB-24, RGB-32, UYVY, AYUV, and so forth.</span></span> <span data-ttu-id="67f1d-110">En el audio, los subtipos incluyen audio PCM, Windows Media Audio 9, etc.</span><span class="sxs-lookup"><span data-stu-id="67f1d-110">Within audio, the subtypes include PCM audio, Windows Media Audio 9, and so forth.</span></span>

<span data-ttu-id="67f1d-111">Para obtener los valores posibles, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="67f1d-111">For possible values, see the following topics:</span></span>

-   [<span data-ttu-id="67f1d-112">GUID de subtipo de audio</span><span class="sxs-lookup"><span data-stu-id="67f1d-112">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
-   [<span data-ttu-id="67f1d-113">GUID de subtipo de vídeo</span><span class="sxs-lookup"><span data-stu-id="67f1d-113">Video Subtype GUIDs</span></span>](video-subtype-guids.md)

<span data-ttu-id="67f1d-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="67f1d-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="67f1d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67f1d-115">Requirements</span></span>



| <span data-ttu-id="67f1d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="67f1d-116">Requirement</span></span> | <span data-ttu-id="67f1d-117">Value</span><span class="sxs-lookup"><span data-stu-id="67f1d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67f1d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67f1d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="67f1d-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="67f1d-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="67f1d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67f1d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="67f1d-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="67f1d-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="67f1d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67f1d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="67f1d-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="67f1d-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67f1d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="67f1d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67f1d-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67f1d-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="67f1d-126">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="67f1d-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="67f1d-127">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="67f1d-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="67f1d-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="67f1d-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="67f1d-129">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="67f1d-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




