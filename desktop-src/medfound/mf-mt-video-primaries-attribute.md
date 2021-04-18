---
description: Especifica los elementos primarios de color para un tipo de medio de vídeo.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: MF_MT_VIDEO_PRIMARIES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716958"
---
# <a name="mf_mt_video_primaries-attribute"></a>\_ \_ Atributo primarios de vídeo MF MT \_

Especifica los elementos primarios de color para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El valor de este atributo es un miembro de la enumeración [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) .

La enumeración [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) identifica los primarios de color asociados a determinados estándares de vídeo comunes. Si el tipo de medio usa elementos primarios de color que no se identifican en la enumeración **MFVideoPrimaries** , establezca el atributo de [**\_ \_ \_ \_ primarios de vídeo personalizado MF MT**](mf-mt-custom-video-primaries-attribute.md) en lugar de este atributo.

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
</dt> <dt>

[Información de color ampliada](extended-color-information.md)
</dt> </dl>

 

 




