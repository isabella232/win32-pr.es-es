---
description: Especifica el perfil MPEG-2 o H. 264 en un tipo de medio de vídeo.
ms.assetid: 8c6a68cb-d976-4099-8934-064f0e8f6374
title: MF_MT_MPEG2_PROFILE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee5c64ea9f5bdf73a78d6ae29124c7cd5b37df43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911189"
---
# <a name="mf_mt_mpeg2_profile-attribute"></a><span data-ttu-id="8f375-103">\_Atributo de perfil MF MT \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="8f375-103">MF\_MT\_MPEG2\_PROFILE attribute</span></span>

<span data-ttu-id="8f375-104">Especifica el perfil MPEG-2 o H. 264 en un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8f375-104">Specifies the MPEG-2 or H.264 profile in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="8f375-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8f375-105">Data type</span></span>

<span data-ttu-id="8f375-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8f375-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8f375-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f375-107">Remarks</span></span>

<span data-ttu-id="8f375-108">Para vídeo MPEG-2, el valor de este atributo es un miembro de la enumeración [**AM \_ MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) .</span><span class="sxs-lookup"><span data-stu-id="8f375-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) enumeration.</span></span>

<span data-ttu-id="8f375-109">Para el vídeo H. 264, el valor es un miembro de la enumeración [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="8f375-109">For H.264 video, the value is a member of the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span>

<span data-ttu-id="8f375-110">Este atributo corresponde al miembro **dwProfile** de la estructura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="8f375-110">This attribute corresponds to the **dwProfile** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="8f375-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8f375-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f375-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f375-112">Requirements</span></span>



| <span data-ttu-id="8f375-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f375-113">Requirement</span></span> | <span data-ttu-id="8f375-114">Value</span><span class="sxs-lookup"><span data-stu-id="8f375-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f375-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f375-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8f375-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="8f375-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="8f375-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f375-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8f375-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="8f375-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="8f375-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f375-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f375-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f375-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f375-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f375-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f375-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8f375-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8f375-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8f375-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8f375-124">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8f375-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8f375-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="8f375-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="8f375-126">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="8f375-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
