---
description: Especifica si el motor multimedia va a reproducir contenido protegido.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS atributo (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33feb8d3e1d7c216cfd0392a1fcf9df0100f924
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361869"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a><span data-ttu-id="f113a-103">MF \_ \_ atributo de \_ marcas de protección de contenido de motor multimedia \_ \_</span><span class="sxs-lookup"><span data-stu-id="f113a-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_FLAGS attribute</span></span>

<span data-ttu-id="f113a-104">Especifica si el motor multimedia va a reproducir contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="f113a-104">Specifies whether the Media Engine will play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="f113a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f113a-105">Data type</span></span>

<span data-ttu-id="f113a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f113a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f113a-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f113a-107">Remarks</span></span>

<span data-ttu-id="f113a-108">El valor de este atributo es **una operación OR bit a bit** de marcas de la enumeración de [**marcas de \_ \_ \_ protección \_ de motor multimedia MF**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) .</span><span class="sxs-lookup"><span data-stu-id="f113a-108">The value of this attribute is a bitwise **OR** of flags from the [**MF\_MEDIA\_ENGINE\_PROTECTION\_FLAGS**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) enumeration.</span></span> <span data-ttu-id="f113a-109">Para habilitar la reproducción de contenido protegido, establezca la marca **MF \_ media \_ Engine \_ habilitar \_ \_ contenido protegido** .</span><span class="sxs-lookup"><span data-stu-id="f113a-109">To enable playback of protected content, set the **MF\_MEDIA\_ENGINE\_ENABLE\_PROTECTED\_CONTENT** flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="f113a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f113a-110">Requirements</span></span>



| <span data-ttu-id="f113a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f113a-111">Requirement</span></span> | <span data-ttu-id="f113a-112">Value</span><span class="sxs-lookup"><span data-stu-id="f113a-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f113a-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f113a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f113a-114">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="f113a-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="f113a-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f113a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f113a-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="f113a-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="f113a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f113a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f113a-118"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="f113a-118"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f113a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f113a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f113a-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f113a-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f113a-121">Atributos del motor multimedia</span><span class="sxs-lookup"><span data-stu-id="f113a-121">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="f113a-122">**IMFMediaEngineClassFactory:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="f113a-122">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




