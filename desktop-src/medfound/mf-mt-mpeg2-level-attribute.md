---
description: Especifica el nivel MPEG-2 o H. 264 en un tipo de medio de vídeo.
ms.assetid: 8dd8e8c4-5a6f-4a87-a643-73af35c362a9
title: MF_MT_MPEG2_LEVEL atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111c4b30befb1d4b25a688d25f46f02bcef21541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277690"
---
# <a name="mf_mt_mpeg2_level-attribute"></a><span data-ttu-id="c819d-103">\_Atributo de nivel MF MT \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="c819d-103">MF\_MT\_MPEG2\_LEVEL attribute</span></span>

<span data-ttu-id="c819d-104">Especifica el nivel MPEG-2 o H. 264 en un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c819d-104">Specifies the MPEG-2 or H.264 level in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="c819d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c819d-105">Data type</span></span>

<span data-ttu-id="c819d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c819d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c819d-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c819d-107">Remarks</span></span>

<span data-ttu-id="c819d-108">Para vídeo MPEG-2, el valor de este atributo es un miembro de la enumeración [**AM \_ MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) .</span><span class="sxs-lookup"><span data-stu-id="c819d-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) enumeration.</span></span>

<span data-ttu-id="c819d-109">Para el vídeo H. 264, el valor es un miembro de la enumeración [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) .</span><span class="sxs-lookup"><span data-stu-id="c819d-109">For H.264 video, the value is a member of the [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) enumeration.</span></span>

<span data-ttu-id="c819d-110">Este atributo corresponde al miembro **dwLevel** de la estructura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="c819d-110">This attribute corresponds to the **dwLevel** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="c819d-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c819d-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c819d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c819d-112">Requirements</span></span>



| <span data-ttu-id="c819d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c819d-113">Requirement</span></span> | <span data-ttu-id="c819d-114">Value</span><span class="sxs-lookup"><span data-stu-id="c819d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c819d-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c819d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c819d-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="c819d-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c819d-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c819d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c819d-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c819d-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c819d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c819d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c819d-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c819d-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c819d-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c819d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c819d-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c819d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c819d-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c819d-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c819d-124">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c819d-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c819d-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c819d-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c819d-126">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="c819d-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
