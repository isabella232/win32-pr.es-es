---
description: Haga referencia al nivel de volumen medio de Windows archivo de audio multimedia.
ms.assetid: ea7d4ed1-2a96-4372-9936-abdd6473b57e
title: MF_MT_AUDIO_WMADRC_AVGREF atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a822046d368025bcfd068f7c1afd32f75d22b5d1ceab69d3e4b517595baa9b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035293"
---
# <a name="mf_mt_audio_wmadrc_avgref-attribute"></a>Atributo \_ \_ AVGREF MF MT AUDIO \_ WMADRC \_

Haga referencia al nivel de volumen medio de Windows archivo de audio multimedia.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los tipos de medios de audio Windows códecs de audio multimedia. Especifica el nivel de volumen medio original del contenido. El descodificador puede usar este valor para realizar el control de intervalo dinámico.

El [**método IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) agrega este atributo al tipo de medio si el encabezado ASF contiene el atributo [**WM/WMADRCAverageReference.**](../wmformat/wm-wmadrcaveragereference.md) Este atributo se documenta en la documentación del SDK Windows Media Format.

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

 

 
