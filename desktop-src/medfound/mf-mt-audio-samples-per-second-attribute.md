---
description: 'MF_MT_AUDIO_SAMPLES_PER_SECOND atributo : número de muestras de audio por segundo en un tipo de medio de audio.'
ms.assetid: f640016d-595e-4b20-8ce8-23a029c2b064
title: MF_MT_AUDIO_SAMPLES_PER_SECOND atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a91b44ba4c55bf2512eefddfe3bc7a18d2eddd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093103"
---
# <a name="mf_mt_audio_samples_per_second-attribute"></a><span data-ttu-id="7dce1-103">Atributo MF \_ MT AUDIO SAMPLES PER \_ \_ \_ \_ SECOND</span><span class="sxs-lookup"><span data-stu-id="7dce1-103">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND attribute</span></span>

<span data-ttu-id="7dce1-104">Número de muestras de audio por segundo en un tipo de medio de audio.</span><span class="sxs-lookup"><span data-stu-id="7dce1-104">Number of audio samples per second in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="7dce1-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7dce1-105">Data type</span></span>

<span data-ttu-id="7dce1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7dce1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7dce1-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7dce1-107">Remarks</span></span>

<span data-ttu-id="7dce1-108">Este atributo se corresponde con el **miembro nSamplesPerSec** de la [**estructura DESATEX.**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7dce1-108">This attribute corresponds to the **nSamplesPerSec** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="7dce1-109">La constante GUID para este atributo se exporta desde mfuuid.lib.</span><span class="sxs-lookup"><span data-stu-id="7dce1-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dce1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dce1-110">Requirements</span></span>



| <span data-ttu-id="7dce1-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dce1-111">Requirement</span></span> | <span data-ttu-id="7dce1-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7dce1-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7dce1-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7dce1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7dce1-114">Aplicaciones de escritorio de Windows Vista \[ \| para aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="7dce1-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7dce1-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7dce1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7dce1-116">Aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="7dce1-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7dce1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7dce1-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dce1-118"><dt>Mfapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="7dce1-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dce1-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7dce1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dce1-120">Lista alfabética de Media Foundation atributos</span><span class="sxs-lookup"><span data-stu-id="7dce1-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7dce1-121">**ATTRIBUTEAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7dce1-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7dce1-122">**ATTRIBUTEAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7dce1-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7dce1-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="7dce1-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="7dce1-124">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="7dce1-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="7dce1-125">**MUESTRAS \_ DE AUDIO FLOAT DE MF MT POR \_ \_ \_ \_ \_ SEGUNDO**</span><span class="sxs-lookup"><span data-stu-id="7dce1-125">**MF\_MT\_AUDIO\_FLOAT\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-float-samples-per-second-attribute.md)
</dt> </dl>

 

 
