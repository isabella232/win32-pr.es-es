---
description: Especifica si un tipo de medio de vídeo requiere la aplicación de protección contra copia.
ms.assetid: fb12ba38-a4f4-44fe-bf31-e731c56bb145
title: MF_MT_DRM_FLAGS atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ef771cb72050b2273d822ce799092ce51e64c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716501"
---
# <a name="mf_mt_drm_flags-attribute"></a><span data-ttu-id="c9d67-103">\_Atributo de \_ marcadores de DRM MF MT \_</span><span class="sxs-lookup"><span data-stu-id="c9d67-103">MF\_MT\_DRM\_FLAGS attribute</span></span>

<span data-ttu-id="c9d67-104">Especifica si un tipo de medio de vídeo requiere la aplicación de protección contra copia.</span><span class="sxs-lookup"><span data-stu-id="c9d67-104">Specifies whether a video media type requires the enforcement of copy protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="c9d67-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c9d67-105">Data type</span></span>

<span data-ttu-id="c9d67-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c9d67-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c9d67-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9d67-107">Remarks</span></span>

<span data-ttu-id="c9d67-108">El valor de este atributo es un miembro de la enumeración [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) .</span><span class="sxs-lookup"><span data-stu-id="c9d67-108">The value of this attribute is a member of the [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) enumeration.</span></span>

<span data-ttu-id="c9d67-109">Este atributo proporciona una sugerencia a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c9d67-109">This attribute provides a hint to the application.</span></span> <span data-ttu-id="c9d67-110">No se utiliza para aplicar la protección contra copia o para especificar el mecanismo de protección contra copia.</span><span class="sxs-lookup"><span data-stu-id="c9d67-110">It is not used to enforce copy protection or to specify the copy protection mechanism.</span></span>

<span data-ttu-id="c9d67-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c9d67-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9d67-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9d67-112">Requirements</span></span>



| <span data-ttu-id="c9d67-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9d67-113">Requirement</span></span> | <span data-ttu-id="c9d67-114">Value</span><span class="sxs-lookup"><span data-stu-id="c9d67-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d67-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9d67-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c9d67-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="c9d67-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c9d67-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9d67-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c9d67-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c9d67-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c9d67-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9d67-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9d67-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9d67-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d67-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9d67-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d67-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9d67-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c9d67-123">MF \_ SD \_ protegido</span><span class="sxs-lookup"><span data-stu-id="c9d67-123">MF\_SD\_PROTECTED</span></span>](mf-sd-protected-attribute.md)
</dt> <dt>

[<span data-ttu-id="c9d67-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c9d67-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c9d67-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c9d67-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c9d67-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c9d67-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c9d67-127">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="c9d67-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




