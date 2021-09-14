---
description: Contiene el encabezado de secuencia MPEG-1 o MPEG-2 para un tipo de medio de vídeo.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: MF_MT_MPEG_SEQUENCE_HEADER atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257855"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a>Atributo MF \_ MT \_ MPEG SEQUENCE \_ \_ HEADER

Contiene el encabezado de secuencia MPEG-1 o MPEG-2 para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

Este atributo corresponde al miembro **dwSequenceHeader** de la estructura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) o al **miembro bSequenceHeader** de la [**estructura MPEG1VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)

En el vídeo h264 y h265, el blob contiene [unidades NAL](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) concatenadas en formato anexo B, junto con sus códigos de inicio. En concreto, para el vídeo h264 son SPS & NAL de PPS. Para h265 son VPS, SPS & PPS.

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

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 
