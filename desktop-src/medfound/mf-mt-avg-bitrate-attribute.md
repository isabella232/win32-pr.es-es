---
description: Velocidad de datos aproximada de la secuencia de vídeo, en bits por segundo, para un tipo de medio de vídeo.
ms.assetid: cf9374a7-3688-4a6c-8339-d68c267c9bed
title: MF_MT_AVG_BITRATE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4497c58abf8587e72dea47d4f8ac222a1b0692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424016"
---
# <a name="mf_mt_avg_bitrate-attribute"></a><span data-ttu-id="6f56e-103">\_Atributo de \_ velocidad de bits promedio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="6f56e-103">MF\_MT\_AVG\_BITRATE attribute</span></span>

<span data-ttu-id="6f56e-104">Velocidad de datos aproximada de la secuencia de vídeo, en bits por segundo, para un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6f56e-104">Approximate data rate of the video stream, in bits per second, for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="6f56e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6f56e-105">Data type</span></span>

<span data-ttu-id="6f56e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6f56e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6f56e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f56e-107">Remarks</span></span>

<span data-ttu-id="6f56e-108">Este atributo corresponde al miembro **dwBitRate** de las estructuras [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) y [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="6f56e-108">This attribute corresponds to the **dwBitRate** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structures.</span></span>

<span data-ttu-id="6f56e-109">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6f56e-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f56e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f56e-110">Requirements</span></span>



| <span data-ttu-id="6f56e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f56e-111">Requirement</span></span> | <span data-ttu-id="6f56e-112">Value</span><span class="sxs-lookup"><span data-stu-id="6f56e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6f56e-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f56e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6f56e-114">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="6f56e-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6f56e-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f56e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6f56e-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="6f56e-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6f56e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f56e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f56e-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f56e-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f56e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f56e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f56e-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6f56e-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6f56e-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6f56e-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6f56e-122">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6f56e-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="6f56e-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6f56e-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6f56e-124">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="6f56e-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
