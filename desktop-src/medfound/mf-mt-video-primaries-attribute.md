---
description: Especifica los valores de color principal para un tipo de medio de vídeo.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: MF_MT_VIDEO_PRIMARIES atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580352"
---
# <a name="mf_mt_video_primaries-attribute"></a>Atributo MF \_ MT \_ VIDEO \_ PRIMARIES

Especifica los valores de color principal para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El valor de este atributo es un miembro de la [**enumeración MFVideoPrimaries.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries)

La [**enumeración MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) identifica las primarias de color asociadas a determinados estándares de vídeo comunes. Si el tipo de medio usa elementos de color principal que no se identifican en la enumeración **MFVideoPrimaries,** establezca el atributo [**MF MT CUSTOM VIDEO \_ \_ \_ \_ PRIMARIES**](mf-mt-custom-video-primaries-attribute.md) en lugar de este atributo.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



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
</dt> <dt>

[Información de color extendida](extended-color-information.md)
</dt> </dl>

 

 




