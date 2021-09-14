---
description: Número de bits por muestra de audio en un tipo de medio de audio.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: MF_MT_AUDIO_BITS_PER_SAMPLE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896e77c937269b63208cb4bff73482a8df8596aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263319"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a>Atributo \_ MF MT AUDIO BITS PER \_ \_ \_ \_ SAMPLE

Número de bits por muestra de audio en un tipo de medio de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo corresponde al miembro **wBitsPerSample** de la [**estructuraSAMPLEATEX.**](/previous-versions/dd757713(v=vs.85))

Si algunos bits contienen relleno, establezca el atributo [**MF MT AUDIO VALID BITS PER \_ \_ \_ \_ \_ \_ SAMPLE**](mf-mt-audio-valid-bits-per-sample-attribute.md) para especificar el número de bits de datos de audio válidos en cada muestra.

Si el audio contiene 8 bits por muestra, las muestras de audio son valores sin signo. (Cada ejemplo de audio tiene el intervalo de 0 a 255). Si el audio contiene 16 bits por muestra o superior, las muestras de audio son valores firmados.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



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

 

 
