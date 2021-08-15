---
description: Número de bits válidos de datos de audio en cada muestra de audio.
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: MF_MT_AUDIO_VALID_BITS_PER_SAMPLE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f84fa3938e4d74473da70bd28e5ccbb1bab71441c694b670cdb8b54bead31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973584"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a>Atributo \_ MF MT AUDIO VALID BITS PER \_ \_ \_ \_ \_ SAMPLE

Número de bits válidos de datos de audio en cada muestra de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El **atributo MF MT AUDIO VALID BITS PER \_ \_ \_ \_ \_ \_ SAMPLE** se usa para los formatos de audio que contienen relleno después de cada muestra de audio. El tamaño total de cada muestra de audio, incluidos los bits de relleno, se proporciona en el atributo [**MF MT AUDIO BITS PER \_ \_ \_ \_ \_ SAMPLE.**](mf-mt-audio-bits-per-sample-attribute.md)

Si el **atributo MF MT AUDIO VALID BITS PER \_ \_ \_ \_ \_ \_ SAMPLE** no está establecido, use el atributo [**MF MT AUDIO BITS PER \_ \_ \_ \_ \_ SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) para buscar el número de bits válidos por muestra.

Si un formato de audio no contiene bits de relleno, este atributo no debe establecerse o debe establecerse en el mismo valor que el atributo [**MF MT AUDIO BITS PER \_ \_ \_ \_ \_ SAMPLE.**](mf-mt-audio-bits-per-sample-attribute.md)

Este atributo corresponde al miembro **wValidBitsPerSample** de la [**estructuraSAMPLEATEXTENSIBLE.**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 
