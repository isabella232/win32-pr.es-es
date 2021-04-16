---
description: Para un tipo de medio de vídeo, especifica cómo se almacenan los fotogramas de vídeo 3D en la memoria.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: MF_MT_VIDEO_3D_FORMAT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678286"
---
# <a name="mf_mt_video_3d_format-attribute"></a><span data-ttu-id="b5232-103">\_Atributo de \_ formato de vídeo \_ 3D MF MT \_</span><span class="sxs-lookup"><span data-stu-id="b5232-103">MF\_MT\_VIDEO\_3D\_FORMAT attribute</span></span>

<span data-ttu-id="b5232-104">Para un tipo de medio de vídeo, especifica cómo se almacenan los fotogramas de vídeo 3D en la memoria.</span><span class="sxs-lookup"><span data-stu-id="b5232-104">For a video media type, specifies how 3D video frames are stored in memory.</span></span>

## <a name="data-type"></a><span data-ttu-id="b5232-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b5232-105">Data type</span></span>

<span data-ttu-id="b5232-106">**MFVideo3DFormat** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="b5232-106">**MFVideo3DFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b5232-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5232-107">Remarks</span></span>

<span data-ttu-id="b5232-108">El valor de este atributo es un miembro de la enumeración [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) .</span><span class="sxs-lookup"><span data-stu-id="b5232-108">The value of this attribute is a member of the [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) enumeration.</span></span> <span data-ttu-id="b5232-109">El atributo solo se aplica si el atributo [MF \_ MT \_ video \_ 3D](mf-mt-video-3d.md) es **true**.</span><span class="sxs-lookup"><span data-stu-id="b5232-109">The attribute applies only if the [MF\_MT\_VIDEO\_3D](mf-mt-video-3d.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="b5232-110">Este atributo es necesario para los formatos de vídeo 3D sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="b5232-110">This attribute is required for uncompressed 3D video formats.</span></span> <span data-ttu-id="b5232-111">Es opcional para vídeo 3D comprimido.</span><span class="sxs-lookup"><span data-stu-id="b5232-111">It is optional for compressed 3D video.</span></span> <span data-ttu-id="b5232-112">Un origen multimedia que proporciona fotogramas codificados podría establecer el atributo, en función de la información del contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="b5232-112">A media source that delivers encoded frames might be able to set the attribute, based on information in the file container.</span></span> <span data-ttu-id="b5232-113">En caso contrario, el descodificador debe establecer el atributo en el tipo de medio de salida del descodificador.</span><span class="sxs-lookup"><span data-stu-id="b5232-113">Otherwise, the attribute should be set by the decoder in the decoder's output media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5232-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5232-114">Requirements</span></span>



| <span data-ttu-id="b5232-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5232-115">Requirement</span></span> | <span data-ttu-id="b5232-116">Value</span><span class="sxs-lookup"><span data-stu-id="b5232-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5232-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5232-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b5232-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="b5232-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b5232-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5232-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b5232-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="b5232-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b5232-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5232-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5232-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5232-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5232-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5232-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5232-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b5232-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




