---
description: Código de hora de inicio de grupo de imágenes (GOP), para un tipo de medio de vídeo MPEG-1 o MPEG-2.
ms.assetid: 8313b83c-5a0a-4aaa-bdc8-58a987c329c7
title: MF_MT_MPEG_START_TIME_CODE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b19a041dbcd791359d704b407445779927d0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716500"
---
# <a name="mf_mt_mpeg_start_time_code-attribute"></a><span data-ttu-id="03a4c-103">\_Atributo de \_ \_ código de hora de inicio de MPEG MT \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="03a4c-103">MF\_MT\_MPEG\_START\_TIME\_CODE attribute</span></span>

<span data-ttu-id="03a4c-104">Código de hora de inicio de grupo de imágenes (GOP), para un tipo de medio de vídeo MPEG-1 o MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="03a4c-104">Group-of-pictures (GOP) start time code, for an MPEG-1 or MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="03a4c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="03a4c-105">Data type</span></span>

<span data-ttu-id="03a4c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="03a4c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="03a4c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03a4c-107">Remarks</span></span>

<span data-ttu-id="03a4c-108">Este atributo corresponde al miembro **dwStartTimeCode** de las estructuras [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) y [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="03a4c-108">This attribute corresponds to the **dwStartTimeCode** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) and [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structures.</span></span>

<span data-ttu-id="03a4c-109">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="03a4c-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="03a4c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03a4c-110">Requirements</span></span>



| <span data-ttu-id="03a4c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="03a4c-111">Requirement</span></span> | <span data-ttu-id="03a4c-112">Value</span><span class="sxs-lookup"><span data-stu-id="03a4c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03a4c-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03a4c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="03a4c-114">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="03a4c-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="03a4c-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03a4c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="03a4c-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="03a4c-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="03a4c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03a4c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="03a4c-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="03a4c-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03a4c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="03a4c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a4c-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03a4c-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="03a4c-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="03a4c-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="03a4c-122">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="03a4c-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="03a4c-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="03a4c-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="03a4c-124">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="03a4c-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="03a4c-125">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03a4c-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 
