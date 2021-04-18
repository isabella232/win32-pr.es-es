---
description: Número de bits por muestra de audio en un tipo de medio de audio.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: MF_MT_AUDIO_BITS_PER_SAMPLE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896e77c937269b63208cb4bff73482a8df8596aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696754"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a><span data-ttu-id="09eb1-103">MF \_ MT \_ audio \_ bits \_ por \_ atributo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="09eb1-103">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="09eb1-104">Número de bits por muestra de audio en un tipo de medio de audio.</span><span class="sxs-lookup"><span data-stu-id="09eb1-104">Number of bits per audio sample in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="09eb1-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="09eb1-105">Data type</span></span>

<span data-ttu-id="09eb1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="09eb1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="09eb1-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09eb1-107">Remarks</span></span>

<span data-ttu-id="09eb1-108">Este atributo corresponde al miembro **wBitsPerSample** de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="09eb1-108">This attribute corresponds to the **wBitsPerSample** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="09eb1-109">Si algunos bits contienen relleno, establezca el atributo [**MF \_ MT \_ audio \_ Valid \_ bits \_ por \_ muestra**](mf-mt-audio-valid-bits-per-sample-attribute.md) para especificar el número de bits de datos de audio válidos en cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="09eb1-109">If some bits contain padding, set the [**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**](mf-mt-audio-valid-bits-per-sample-attribute.md) attribute to specify the number of bits of valid audio data in each sample.</span></span>

<span data-ttu-id="09eb1-110">Si el audio contiene 8 bits por muestra, los ejemplos de audio son valores sin signo.</span><span class="sxs-lookup"><span data-stu-id="09eb1-110">If the audio contains 8 bits per sample, the audio samples are unsigned values.</span></span> <span data-ttu-id="09eb1-111">(Cada ejemplo de audio tiene el intervalo comprendido entre 0 y 255). Si el audio contiene 16 bits por muestra o superior, los ejemplos de audio son valores con signo.</span><span class="sxs-lookup"><span data-stu-id="09eb1-111">(Each audio sample has the range 0–255.) If the audio contains 16 bits per sample or higher, the audio samples are signed values.</span></span>

<span data-ttu-id="09eb1-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="09eb1-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="09eb1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09eb1-113">Requirements</span></span>



| <span data-ttu-id="09eb1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="09eb1-114">Requirement</span></span> | <span data-ttu-id="09eb1-115">Value</span><span class="sxs-lookup"><span data-stu-id="09eb1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09eb1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09eb1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="09eb1-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="09eb1-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="09eb1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09eb1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="09eb1-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="09eb1-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="09eb1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09eb1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="09eb1-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="09eb1-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09eb1-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="09eb1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09eb1-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="09eb1-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="09eb1-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="09eb1-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="09eb1-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="09eb1-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="09eb1-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="09eb1-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="09eb1-127">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="09eb1-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
