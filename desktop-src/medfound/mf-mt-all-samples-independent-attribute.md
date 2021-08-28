---
description: Especifica para un tipo de medio si cada muestra es independiente de las otras muestras de la secuencia.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: MF_MT_ALL_SAMPLES_INDEPENDENT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ada34232ccbc7eb30fc9a5bcb64e96542b0375140de426fae951f5e0317c9e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060755"
---
# <a name="mf_mt_all_samples_independent-attribute"></a>Atributo MF \_ MT \_ ALL SAMPLES \_ \_ INDEPENDENT

Especifica para un tipo de medio si cada muestra es independiente de las otras muestras de la secuencia.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Comentarios

Si este atributo es **FALSE,** algunos ejemplos no se pueden usar sin hacer referencia a otros ejemplos de la secuencia. Por ejemplo, si un formato de vídeo contiene marcos delta, este atributo debe ser **FALSE.**

Este atributo corresponde al campo **bComposiciónCompression** de la estructura DirectShow [**AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

Establezca este atributo en **TRUE para** todos los tipos de medios sin comprimir.

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

 

 
