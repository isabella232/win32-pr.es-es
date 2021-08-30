---
description: Nivel de volumen máximo de destino de un Windows de audio multimedia.
ms.assetid: 73f4e763-dcb7-48cd-ab80-37635d973da0
title: MF_MT_AUDIO_WMADRC_PEAKTARGET atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 806f81c0095481ab5e0694614a54e8374d8bd73445b825493253898ff6f6f0f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955855"
---
# <a name="mf_mt_audio_wmadrc_peaktarget-attribute"></a>Atributo MF \_ MT \_ AUDIO \_ WMADRC \_ PEAKTARGET

Nivel de volumen máximo de destino de un Windows de audio multimedia.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los tipos de medios de audio Windows códecs de audio multimedia. Especifica el nivel de volumen máximo de destino del contenido. El descodificador puede usar este valor para realizar el control de intervalo dinámico.

El [**método IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) agrega este atributo al tipo de medio si el encabezado ASF contiene el [**atributo WM/WMADRCPeakTarget.**](../wmformat/wm-wmadrcpeaktarget.md) Este atributo se documenta en la documentación del SDK Windows Media Format.

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

 

 
