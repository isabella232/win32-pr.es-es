---
description: Indica si se ha aplicado la estabilización de vídeo a un fotograma de vídeo.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: MFSampleExtension_VideoDSPMode atributo (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309d4b5b68455e78ba63074b9d8ec5e4cbde4fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720488"
---
# <a name="mfsampleextension_videodspmode-attribute"></a><span data-ttu-id="e3554-103">\_Atributo VideoDSPMode de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="e3554-103">MFSampleExtension\_VideoDSPMode attribute</span></span>

<span data-ttu-id="e3554-104">Indica si se ha aplicado la estabilización de vídeo a un fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e3554-104">Indicates whether video stabilization was applied to a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="e3554-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e3554-105">Data type</span></span>

<span data-ttu-id="e3554-106">**MFVideoDSPMode** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e3554-106">**MFVideoDSPMode** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e3554-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="e3554-107">Get/set</span></span>

<span data-ttu-id="e3554-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e3554-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e3554-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e3554-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e3554-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="e3554-110">Applies to</span></span>

[<span data-ttu-id="e3554-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="e3554-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="e3554-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3554-112">Remarks</span></span>

<span data-ttu-id="e3554-113">El [**video stabilization MFT**](video-stabilization-mft.md) establece este atributo en los ejemplos de salida que genera.</span><span class="sxs-lookup"><span data-stu-id="e3554-113">The [**Video Stabilization MFT**](video-stabilization-mft.md) sets this attribute on the output samples that it produces.</span></span> <span data-ttu-id="e3554-114">El valor del atributo es un valor de enumeración [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) .</span><span class="sxs-lookup"><span data-stu-id="e3554-114">The value of the attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="e3554-115">Si el valor es **MFVideoDSPMode \_ estabilización**, significa que la MFT aplicó la estabilización de la imagen al marco.</span><span class="sxs-lookup"><span data-stu-id="e3554-115">If the value is **MFVideoDSPMode\_Stabilization**, it means that the MFT applied image stabilization to the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3554-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3554-116">Requirements</span></span>



| <span data-ttu-id="e3554-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3554-117">Requirement</span></span> | <span data-ttu-id="e3554-118">Value</span><span class="sxs-lookup"><span data-stu-id="e3554-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3554-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3554-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e3554-120">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3554-120">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e3554-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3554-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e3554-122">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3554-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3554-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3554-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3554-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3554-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3554-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3554-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3554-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3554-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e3554-127">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3554-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="e3554-128">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="e3554-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="e3554-129">**Video Stabilization MFT**</span><span class="sxs-lookup"><span data-stu-id="e3554-129">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




