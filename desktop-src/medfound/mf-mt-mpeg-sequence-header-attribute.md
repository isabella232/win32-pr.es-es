---
description: Contiene el encabezado de secuencia MPEG-1 o MPEG-2 para un tipo de medio de vídeo.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: MF_MT_MPEG_SEQUENCE_HEADER atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697396"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a><span data-ttu-id="ffea3-103">\_Atributo de \_ \_ encabezado de secuencia MF MT MPEG \_</span><span class="sxs-lookup"><span data-stu-id="ffea3-103">MF\_MT\_MPEG\_SEQUENCE\_HEADER attribute</span></span>

<span data-ttu-id="ffea3-104">Contiene el encabezado de secuencia MPEG-1 o MPEG-2 para un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ffea3-104">Contains the MPEG-1 or MPEG-2 sequence header for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="ffea3-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ffea3-105">Data type</span></span>

<span data-ttu-id="ffea3-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="ffea3-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="ffea3-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffea3-107">Remarks</span></span>

<span data-ttu-id="ffea3-108">Este atributo corresponde al miembro **dwSequenceHeader** de la estructura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) , o al miembro **bSequenceHeader** de la estructura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="ffea3-108">This attribute corresponds to the **dwSequenceHeader** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure, or the **bSequenceHeader** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) structure.</span></span>

<span data-ttu-id="ffea3-109">En el caso de H264 y H265 video, el BLOB contiene [unidades nal](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) concatenadas en el formato del Anexo B, junto con sus códigos de inicio.</span><span class="sxs-lookup"><span data-stu-id="ffea3-109">For h264 and h265 video, the blob contains concatenated [NAL units](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) in Annex B format, along with their start codes.</span></span> <span data-ttu-id="ffea3-110">En concreto, para el vídeo de H264, son SP & unidades de PPS.</span><span class="sxs-lookup"><span data-stu-id="ffea3-110">Specifically, for h264 video they are SPS & PPS NAL units.</span></span> <span data-ttu-id="ffea3-111">En el caso de H265, son VPS, SPS & PPS.</span><span class="sxs-lookup"><span data-stu-id="ffea3-111">For h265 they are VPS, SPS & PPS.</span></span>

<span data-ttu-id="ffea3-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ffea3-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffea3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffea3-113">Requirements</span></span>



| <span data-ttu-id="ffea3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffea3-114">Requirement</span></span> | <span data-ttu-id="ffea3-115">Value</span><span class="sxs-lookup"><span data-stu-id="ffea3-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ffea3-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffea3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ffea3-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="ffea3-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ffea3-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffea3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ffea3-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ffea3-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ffea3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffea3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffea3-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffea3-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffea3-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffea3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffea3-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ffea3-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ffea3-124">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="ffea3-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="ffea3-125">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="ffea3-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="ffea3-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ffea3-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ffea3-127">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="ffea3-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
