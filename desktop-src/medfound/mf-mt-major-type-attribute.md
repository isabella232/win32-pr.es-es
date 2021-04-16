---
description: GUID de tipo principal para un tipo de medio.
ms.assetid: b88b5fcf-8025-4638-930d-9fc5cf0ec8a3
title: MF_MT_MAJOR_TYPE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c4cc02df4f89e261605c91b71ac1c80ba38b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705709"
---
# <a name="mf_mt_major_type-attribute"></a><span data-ttu-id="ffd58-103">\_Atributo de \_ tipo principal MF MT \_</span><span class="sxs-lookup"><span data-stu-id="ffd58-103">MF\_MT\_MAJOR\_TYPE attribute</span></span>

<span data-ttu-id="ffd58-104">GUID de tipo principal para un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="ffd58-104">Major type GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="ffd58-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ffd58-105">Data type</span></span>

<span data-ttu-id="ffd58-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="ffd58-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd58-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffd58-107">Remarks</span></span>

<span data-ttu-id="ffd58-108">El tipo principal define la categoría general de los datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="ffd58-108">The major type defines the overall category of the media data.</span></span> <span data-ttu-id="ffd58-109">Los tipos principales incluyen vídeo, audio, script, etc.</span><span class="sxs-lookup"><span data-stu-id="ffd58-109">Major types include video, audio, script, and so forth.</span></span> <span data-ttu-id="ffd58-110">Para obtener una lista de los valores posibles, consulte [tipos de medios principales](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="ffd58-110">For a list of possible values, see [Major Media Types](media-type-guids.md).</span></span>

<span data-ttu-id="ffd58-111">Una manera alternativa de recuperar este atributo es llamar a [**IMFMediaType:: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="ffd58-111">An alternate way to retrieve this attribute is to call [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span></span>

<span data-ttu-id="ffd58-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ffd58-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd58-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffd58-113">Requirements</span></span>



| <span data-ttu-id="ffd58-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffd58-114">Requirement</span></span> | <span data-ttu-id="ffd58-115">Value</span><span class="sxs-lookup"><span data-stu-id="ffd58-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd58-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffd58-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd58-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="ffd58-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ffd58-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffd58-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd58-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ffd58-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ffd58-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffd58-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffd58-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffd58-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffd58-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffd58-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffd58-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ffd58-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ffd58-124">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="ffd58-124">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="ffd58-125">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="ffd58-125">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="ffd58-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ffd58-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ffd58-127">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="ffd58-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




