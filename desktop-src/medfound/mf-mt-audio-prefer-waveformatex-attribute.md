---
description: Especifica la estructura de formato heredado preferida que se usará al convertir un tipo de medio de audio.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: MF_MT_AUDIO_PREFER_WAVEFORMATEX atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23e2aeb00e2967b3f031a2aafe3a01f3846d7db077ba344a59680508bd385fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035303"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a>MF \_ MT \_ AUDIO \_ \_ PREFERIR EL atributo DE FORMA DE ONDAATEX

Especifica la estructura de formato heredado preferida que se usará al convertir un tipo de medio de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Comentarios

Este atributo proporciona una sugerencia a la [**función MFCreateWaveFormatExFromMFMediaType.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) Si el atributo es **TRUE**, la función convierte el tipo de medio de audio en una estructura [**DE FORMA DEDATOSTEX**](/previous-versions/dd757713(v=vs.85)) siempre que sea posible, en lugar de convertirlo en una estructura [**DE LA FORMADETEXTENSIBLE.**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))

La [**función MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) establece este atributo. Puede invalidar el valor de este atributo, pero al establecer este atributo en **TRUE** no se garantiza que un tipo de medio de audio se pueda convertir al formulario [**DE FORMATEX.**](/previous-versions/dd757713(v=vs.85))

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
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

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 
