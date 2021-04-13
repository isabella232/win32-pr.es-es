---
description: Número de bits válidos de datos de audio en cada ejemplo de audio.
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: MF_MT_AUDIO_VALID_BITS_PER_SAMPLE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4e5efb41bf3b79d4feded2872b601eea43723a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361583"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a><span data-ttu-id="58873-103">\_ \_ Bits válidos de audio MF MT \_ \_ \_ por \_ atributo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="58873-103">MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="58873-104">Número de bits válidos de datos de audio en cada ejemplo de audio.</span><span class="sxs-lookup"><span data-stu-id="58873-104">Number of valid bits of audio data in each audio sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="58873-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="58873-105">Data type</span></span>

<span data-ttu-id="58873-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="58873-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="58873-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58873-107">Remarks</span></span>

<span data-ttu-id="58873-108">El atributo **MF \_ MT \_ audio \_ válido \_ \_ por \_ muestra** se usa para los formatos de audio que contienen relleno después de cada ejemplo de audio.</span><span class="sxs-lookup"><span data-stu-id="58873-108">The **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is used for audio formats that contain padding after each audio sample.</span></span> <span data-ttu-id="58873-109">El tamaño total de cada ejemplo de audio, incluidos los bits de relleno, se proporciona en el atributo [**MF \_ MT \_ audio \_ bits \_ por \_ muestra**](mf-mt-audio-bits-per-sample-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="58873-109">The total size of each audio sample, including padding bits, is given in the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="58873-110">Si no se ha establecido el atributo **MF \_ MT \_ audio \_ válido \_ \_ por \_ muestra** , use el atributo [**MF \_ MT audio for \_ \_ \_ \_ Sample**](mf-mt-audio-bits-per-sample-attribute.md) para buscar el número de bits válidos por muestra.</span><span class="sxs-lookup"><span data-stu-id="58873-110">If the **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is not set, use the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute to find the number of valid bits per sample.</span></span>

<span data-ttu-id="58873-111">Si un formato de audio no contiene ningún bit de relleno, este atributo no se debe establecer o debe establecerse en el mismo valor que el atributo [**MF \_ MT \_ audio \_ bits \_ por \_ muestra**](mf-mt-audio-bits-per-sample-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="58873-111">If an audio format does not contain any padding bits, then this attribute should not be set, or should be set to the same value as the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="58873-112">Este atributo corresponde al miembro **wValidBitsPerSample** de la estructura [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .</span><span class="sxs-lookup"><span data-stu-id="58873-112">This attribute corresponds to the **wValidBitsPerSample** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="58873-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="58873-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="58873-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58873-114">Requirements</span></span>



| <span data-ttu-id="58873-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="58873-115">Requirement</span></span> | <span data-ttu-id="58873-116">Value</span><span class="sxs-lookup"><span data-stu-id="58873-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58873-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58873-117">Minimum supported client</span></span><br/> | <span data-ttu-id="58873-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="58873-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="58873-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58873-119">Minimum supported server</span></span><br/> | <span data-ttu-id="58873-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="58873-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="58873-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58873-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="58873-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="58873-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58873-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="58873-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58873-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="58873-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="58873-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="58873-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="58873-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="58873-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="58873-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="58873-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="58873-128">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="58873-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
