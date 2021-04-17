---
description: Describe cómo se muestrea el croma para un tipo de medio de vídeo YCbCr.
ms.assetid: 0c930348-8669-42cc-9d74-df9ef475bdc8
title: MF_MT_VIDEO_CHROMA_SITING atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa634cf9a9ca7f5c292eb0cf06c6a1a14c788d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716348"
---
# <a name="mf_mt_video_chroma_siting-attribute"></a><span data-ttu-id="a54fd-103">Atributo de colocación de vídeo de \_ \_ polijuego MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="a54fd-103">MF\_MT\_VIDEO\_CHROMA\_SITING attribute</span></span>

<span data-ttu-id="a54fd-104">Describe cómo se muestrea el croma para un tipo de medio de vídeo Y'Cb'Cr.</span><span class="sxs-lookup"><span data-stu-id="a54fd-104">Describes how chroma was sampled for a Y'Cb'Cr' video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a54fd-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a54fd-105">Data type</span></span>

<span data-ttu-id="a54fd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a54fd-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a54fd-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a54fd-107">Remarks</span></span>

<span data-ttu-id="a54fd-108">El valor de este atributo es **una operación OR bit a bit** de las marcas de la enumeración [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) .</span><span class="sxs-lookup"><span data-stu-id="a54fd-108">The value of this attribute is a bitwise **OR** of flags from the [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) enumeration.</span></span>

<span data-ttu-id="a54fd-109">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a54fd-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a54fd-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a54fd-110">Requirements</span></span>



| <span data-ttu-id="a54fd-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a54fd-111">Requirement</span></span> | <span data-ttu-id="a54fd-112">Value</span><span class="sxs-lookup"><span data-stu-id="a54fd-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a54fd-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a54fd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a54fd-114">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="a54fd-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a54fd-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a54fd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a54fd-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="a54fd-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a54fd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a54fd-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a54fd-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a54fd-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a54fd-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="a54fd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a54fd-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a54fd-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a54fd-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a54fd-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a54fd-122">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a54fd-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a54fd-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a54fd-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a54fd-124">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="a54fd-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="a54fd-125">Información de color ampliada</span><span class="sxs-lookup"><span data-stu-id="a54fd-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




