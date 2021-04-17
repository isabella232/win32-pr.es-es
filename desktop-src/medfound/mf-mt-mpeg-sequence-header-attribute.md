---
description: Contiene el encabezado de secuencia MPEG-1 o MPEG-2 para un tipo de medio de vídeo.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: MF_MT_MPEG_SEQUENCE_HEADER atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697396"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a>\_Atributo de \_ \_ encabezado de secuencia MF MT MPEG \_

Contiene el encabezado de secuencia MPEG-1 o MPEG-2 para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

Este atributo corresponde al miembro **dwSequenceHeader** de la estructura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) , o al miembro **bSequenceHeader** de la estructura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .

En el caso de H264 y H265 video, el BLOB contiene [unidades nal](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) concatenadas en el formato del Anexo B, junto con sus códigos de inicio. En concreto, para el vídeo de H264, son SP & unidades de PPS. En el caso de H265, son VPS, SPS & PPS.

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

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 
