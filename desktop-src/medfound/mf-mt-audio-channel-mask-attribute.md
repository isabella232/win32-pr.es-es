---
description: En un tipo de medio de audio, especifica la asignación de canales de audio a las posiciones del hablante.
ms.assetid: fa5f6baa-0a21-4162-8870-38e71763aba0
title: MF_MT_AUDIO_CHANNEL_MASK atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 544f287ad9cc8addc60245143e079f0ccdd3c1fead043198be93eed59babc98c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955935"
---
# <a name="mf_mt_audio_channel_mask-attribute"></a>Atributo MF \_ MT \_ AUDIO CHANNEL \_ \_ MASK

En un tipo de medio de audio, especifica la asignación de canales de audio a las posiciones del hablante.

## <a name="data-type"></a>Tipo de datos

**UINT32**

El valor de este atributo es un **OR** bit a bit de las marcas siguientes, que se definen en el archivo de encabezado mmreg.h.

<dl> <dt>

<span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**ALTAVOZ \_ FRONT \_ LEFT** (0x1)
</dt> <dt>

<span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**ALTAVOZ \_ FRONT \_ RIGHT** (0x2)
</dt> <dt>

<span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**ALTAVOZ \_ FRONT \_ CENTER** (0x4)
</dt> <dt>

<span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**ALTAVOZ \_ BAJA \_ FRECUENCIA** (0x8)
</dt> <dt>

<span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**ALTAVOZ \_ ATRÁS \_ A LA** IZQUIERDA (0x10)
</dt> <dt>

<span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**ALTAVOZ \_ BACK \_ RIGHT** (0x20)
</dt> <dt>

<span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**ALTAVOZ \_ PARTE \_ DELANTERA IZQUIERDA DEL \_ \_ CENTRO** (0x40)
</dt> <dt>

<span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**ALTAVOZ \_ PARTE \_ DERECHA \_ DEL \_ CENTRO** (0x80)
</dt> <dt>

<span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**ALTAVOZ \_ BACK \_ CENTER** (0x100)
</dt> <dt>

<span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**ALTAVOZ \_ LATERAL \_ IZQUIERDO** (0x200)
</dt> <dt>

<span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**ALTAVOZ \_ LATERAL \_ DERECHO** (0x400)
</dt> <dt>

<span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**ALTAVOZ \_ CENTRO \_ SUPERIOR** (0x800)
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**ALTAVOZ \_ PARTE \_ SUPERIOR \_ IZQUIERDA** (0x1000)
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**ALTAVOZ \_ TOP \_ FRONT \_ CENTER** (0x2000)
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**ALTAVOZ \_ PARTE \_ SUPERIOR \_ DERECHA** (0x4000)
</dt> <dt>

<span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**ALTAVOZ \_ PARTE \_ SUPERIOR \_ IZQUIERDA** (0x8000)
</dt> <dt>

<span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**ALTAVOZ \_ CENTRO \_ SUPERIOR \_ ATRÁS** (0x10000)
</dt> <dt>

<span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**ALTAVOZ \_ PARTE \_ SUPERIOR \_ DERECHA** (0x20000)
</dt> </dl>

## <a name="remarks"></a>Comentarios

Este atributo se corresponde con el **miembro dwChannelMask** de la [**estructura DESATEXTENSIBLE.**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 
