---
description: Número de muestras de audio contenidas en un bloque comprimido de datos de audio. Este atributo se puede usar en formatos de audio comprimidos que tienen un número fijo de muestras en cada bloque.
ms.assetid: 6ae31548-4d78-4e38-9cfc-01b611a6022d
title: MF_MT_AUDIO_SAMPLES_PER_BLOCK atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c453fa4daeaa310b5e41add44b63b0fb45372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716503"
---
# <a name="mf_mt_audio_samples_per_block-attribute"></a><span data-ttu-id="57eb6-104">\_Ejemplos de audio MF MT \_ \_ \_ por atributo de \_ bloque</span><span class="sxs-lookup"><span data-stu-id="57eb6-104">MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK attribute</span></span>

<span data-ttu-id="57eb6-105">Número de muestras de audio contenidas en un bloque comprimido de datos de audio.</span><span class="sxs-lookup"><span data-stu-id="57eb6-105">Number of audio samples contained in one compressed block of audio data.</span></span> <span data-ttu-id="57eb6-106">Este atributo se puede usar en formatos de audio comprimidos que tienen un número fijo de muestras en cada bloque.</span><span class="sxs-lookup"><span data-stu-id="57eb6-106">This attribute can be used in compressed audio formats that have a fixed number of samples within each block.</span></span>

## <a name="data-type"></a><span data-ttu-id="57eb6-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="57eb6-107">Data type</span></span>

<span data-ttu-id="57eb6-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="57eb6-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="57eb6-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57eb6-109">Remarks</span></span>

<span data-ttu-id="57eb6-110">Este atributo corresponde al miembro **wSamplesPerBlock** de la estructura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="57eb6-110">This attribute corresponds to the **wSamplesPerBlock** member of the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="57eb6-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="57eb6-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="57eb6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57eb6-112">Requirements</span></span>



| <span data-ttu-id="57eb6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="57eb6-113">Requirement</span></span> | <span data-ttu-id="57eb6-114">Value</span><span class="sxs-lookup"><span data-stu-id="57eb6-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="57eb6-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57eb6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="57eb6-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="57eb6-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="57eb6-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57eb6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="57eb6-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="57eb6-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="57eb6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57eb6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="57eb6-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="57eb6-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57eb6-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="57eb6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57eb6-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="57eb6-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="57eb6-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="57eb6-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="57eb6-124">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="57eb6-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="57eb6-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="57eb6-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="57eb6-126">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="57eb6-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
