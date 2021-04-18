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
# <a name="mf_mt_audio_bits_per_sample-attribute"></a>MF \_ MT \_ audio \_ bits \_ por \_ atributo de ejemplo

Número de bits por muestra de audio en un tipo de medio de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo corresponde al miembro **wBitsPerSample** de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

Si algunos bits contienen relleno, establezca el atributo [**MF \_ MT \_ audio \_ Valid \_ bits \_ por \_ muestra**](mf-mt-audio-valid-bits-per-sample-attribute.md) para especificar el número de bits de datos de audio válidos en cada ejemplo.

Si el audio contiene 8 bits por muestra, los ejemplos de audio son valores sin signo. (Cada ejemplo de audio tiene el intervalo comprendido entre 0 y 255). Si el audio contiene 16 bits por muestra o superior, los ejemplos de audio son valores con signo.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 
