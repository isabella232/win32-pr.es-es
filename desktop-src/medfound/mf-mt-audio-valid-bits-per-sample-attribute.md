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
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a>\_ \_ Bits válidos de audio MF MT \_ \_ \_ por \_ atributo de ejemplo

Número de bits válidos de datos de audio en cada ejemplo de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El atributo **MF \_ MT \_ audio \_ válido \_ \_ por \_ muestra** se usa para los formatos de audio que contienen relleno después de cada ejemplo de audio. El tamaño total de cada ejemplo de audio, incluidos los bits de relleno, se proporciona en el atributo [**MF \_ MT \_ audio \_ bits \_ por \_ muestra**](mf-mt-audio-bits-per-sample-attribute.md) .

Si no se ha establecido el atributo **MF \_ MT \_ audio \_ válido \_ \_ por \_ muestra** , use el atributo [**MF \_ MT audio for \_ \_ \_ \_ Sample**](mf-mt-audio-bits-per-sample-attribute.md) para buscar el número de bits válidos por muestra.

Si un formato de audio no contiene ningún bit de relleno, este atributo no se debe establecer o debe establecerse en el mismo valor que el atributo [**MF \_ MT \_ audio \_ bits \_ por \_ muestra**](mf-mt-audio-bits-per-sample-attribute.md) .

Este atributo corresponde al miembro **wValidBitsPerSample** de la estructura [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .

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

 

 
