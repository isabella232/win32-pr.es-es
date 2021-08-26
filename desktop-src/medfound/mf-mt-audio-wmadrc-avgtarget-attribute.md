---
description: Nivel de volumen promedio de destino de un Windows de audio multimedia.
ms.assetid: f81158c8-b341-4b39-8fa4-b510c93b89fc
title: MF_MT_AUDIO_WMADRC_AVGTARGET atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a05ef07966313d9b06bec57ec09af068f385bbc869cba7fab33e42e786dc63b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940635"
---
# <a name="mf_mt_audio_wmadrc_avgtarget-attribute"></a>Atributo \_ \_ AVGTARGET de AUDIO MF MT \_ WMADRC \_

Nivel de volumen promedio de destino de un Windows de audio multimedia.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los tipos de medios de audio Windows códecs de audio multimedia. Especifica el nivel de volumen promedio de destino del contenido. El descodificador puede usar este valor para realizar el control de intervalo dinámico.

El [**método IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) agrega este atributo al tipo de medio si el encabezado ASF contiene el atributo [**WM/WMADRCAverageTarget.**](../wmformat/wm-wmadrcaveragetarget.md) Este atributo se documenta en la documentación del SDK Windows Media Format.

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

 

 
