---
description: En un tipo de medio de audio, especifica la asignación de canales de audio a las posiciones del hablante.
ms.assetid: fa5f6baa-0a21-4162-8870-38e71763aba0
title: MF_MT_AUDIO_CHANNEL_MASK atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5293f5387a2c293b97ee32db54fcfb3f3ff304d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082344"
---
# <a name="mf_mt_audio_channel_mask-attribute"></a><span data-ttu-id="be25e-103">\_Atributo de \_ máscara de canal de audio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="be25e-103">MF\_MT\_AUDIO\_CHANNEL\_MASK attribute</span></span>

<span data-ttu-id="be25e-104">En un tipo de medio de audio, especifica la asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="be25e-104">In an audio media type, specifies the assignment of audio channels to speaker positions.</span></span>

## <a name="data-type"></a><span data-ttu-id="be25e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="be25e-105">Data type</span></span>

<span data-ttu-id="be25e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="be25e-106">**UINT32**</span></span>

<span data-ttu-id="be25e-107">El valor de este atributo es **una operación OR bit a bit** de las marcas siguientes, que se definen en el archivo de encabezado mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="be25e-107">The value of this attribute is a bitwise **OR** of the following flags, which are defined in the header file mmreg.h.</span></span>

<dl> <dt>

<span data-ttu-id="be25e-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**Altavoz \_ de FRONT \_ left** (0x1)</span><span class="sxs-lookup"><span data-stu-id="be25e-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**SPEAKER\_FRONT\_LEFT** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**Altavoz \_ de \_Derecha delantera** (0X2)</span><span class="sxs-lookup"><span data-stu-id="be25e-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**SPEAKER\_FRONT\_RIGHT** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**Altavoz \_ de \_Centro frontal** (0x4)</span><span class="sxs-lookup"><span data-stu-id="be25e-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**SPEAKER\_FRONT\_CENTER** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**Altavoz \_ de \_Frecuencia baja** (0x8)</span><span class="sxs-lookup"><span data-stu-id="be25e-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**SPEAKER\_LOW\_FREQUENCY** (0x8)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**Altavoz \_ de ATRÁS \_** a la izquierda (0x10)</span><span class="sxs-lookup"><span data-stu-id="be25e-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**SPEAKER\_BACK\_LEFT** (0x10)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**Altavoz \_ de ATRÁS \_** a la derecha (0x20)</span><span class="sxs-lookup"><span data-stu-id="be25e-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**SPEAKER\_BACK\_RIGHT** (0x20)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**Altavoz \_ de \_Izquierda delantera \_ del \_ Centro** (0x40)</span><span class="sxs-lookup"><span data-stu-id="be25e-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**SPEAKER\_FRONT\_LEFT\_OF\_CENTER** (0x40)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**Altavoz \_ de FRONT \_ right \_ of \_ Center** (0x80)</span><span class="sxs-lookup"><span data-stu-id="be25e-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**SPEAKER\_FRONT\_RIGHT\_OF\_CENTER** (0x80)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**Altavoz \_ de \_Centro trasero** (0x100)</span><span class="sxs-lookup"><span data-stu-id="be25e-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**SPEAKER\_BACK\_CENTER** (0x100)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**Altavoz \_ de LADO \_ izquierdo** (0x200)</span><span class="sxs-lookup"><span data-stu-id="be25e-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**SPEAKER\_SIDE\_LEFT** (0x200)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**Altavoz \_ de LADO \_ derecho** (0x400)</span><span class="sxs-lookup"><span data-stu-id="be25e-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**SPEAKER\_SIDE\_RIGHT** (0x400)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**Altavoz \_ de TOP \_ Center** (0x800)</span><span class="sxs-lookup"><span data-stu-id="be25e-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**SPEAKER\_TOP\_CENTER** (0x800)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**Altavoz \_ de Parte \_ superior \_ izquierda** (0x1000)</span><span class="sxs-lookup"><span data-stu-id="be25e-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**SPEAKER\_TOP\_FRONT\_LEFT** (0x1000)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**Altavoz \_ de \_ \_ Centro frontal superior** (0x2000)</span><span class="sxs-lookup"><span data-stu-id="be25e-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**SPEAKER\_TOP\_FRONT\_CENTER** (0x2000)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**Altavoz \_ de Parte \_ superior \_ derecha** (0x4000)</span><span class="sxs-lookup"><span data-stu-id="be25e-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**SPEAKER\_TOP\_FRONT\_RIGHT** (0x4000)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**Altavoz \_ de Parte \_ superior \_ izquierda** (0x8000)</span><span class="sxs-lookup"><span data-stu-id="be25e-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**SPEAKER\_TOP\_BACK\_LEFT** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**Altavoz \_ de \_ \_ Centro trasero superior** (0x10000)</span><span class="sxs-lookup"><span data-stu-id="be25e-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**SPEAKER\_TOP\_BACK\_CENTER** (0x10000)</span></span>
</dt> <dt>

<span data-ttu-id="be25e-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**Altavoz \_ de Parte \_ superior \_ derecha** (0x20000)</span><span class="sxs-lookup"><span data-stu-id="be25e-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**SPEAKER\_TOP\_BACK\_RIGHT** (0x20000)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="be25e-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be25e-126">Remarks</span></span>

<span data-ttu-id="be25e-127">Este atributo corresponde al miembro **dwChannelMask** de la estructura [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .</span><span class="sxs-lookup"><span data-stu-id="be25e-127">This attribute corresponds to the **dwChannelMask** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="be25e-128">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="be25e-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="be25e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be25e-129">Requirements</span></span>



| <span data-ttu-id="be25e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="be25e-130">Requirement</span></span> | <span data-ttu-id="be25e-131">Value</span><span class="sxs-lookup"><span data-stu-id="be25e-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be25e-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be25e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="be25e-133">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="be25e-133">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="be25e-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be25e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="be25e-135">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="be25e-135">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="be25e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be25e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="be25e-137"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="be25e-137"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be25e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="be25e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be25e-139">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be25e-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="be25e-140">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="be25e-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="be25e-141">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="be25e-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="be25e-142">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="be25e-142">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="be25e-143">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="be25e-143">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
