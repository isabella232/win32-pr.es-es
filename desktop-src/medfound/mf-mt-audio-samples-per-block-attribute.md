---
description: Número de muestras de audio contenidas en un bloque comprimido de datos de audio. Este atributo se puede usar en formatos de audio comprimidos que tienen un número fijo de muestras dentro de cada bloque.
ms.assetid: 6ae31548-4d78-4e38-9cfc-01b611a6022d
title: MF_MT_AUDIO_SAMPLES_PER_BLOCK atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa3de2a07811c591cc64289d185d6ff0c7dcab2cd116df7bb8140dc1298f541a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955875"
---
# <a name="mf_mt_audio_samples_per_block-attribute"></a>Atributo MF \_ MT AUDIO SAMPLES PER \_ \_ \_ \_ BLOCK

Número de muestras de audio contenidas en un bloque comprimido de datos de audio. Este atributo se puede usar en formatos de audio comprimidos que tienen un número fijo de muestras dentro de cada bloque.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo corresponde al miembro **wSamplesPerBlock** de la [**estructuraSAMPLEATEXTENSIBLE.**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))

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

 

 
