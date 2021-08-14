---
description: Especifica los valores de color principal para un tipo de medio de vídeo.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: MF_MT_VIDEO_PRIMARIES atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44b4e1c99dc9a4f288ebab36d413f7eed7c74881e7c10d3c7e9a8a4fe3f0bcf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876715"
---
# <a name="mf_mt_video_primaries-attribute"></a>Atributo \_ MF MT VIDEO \_ \_ PRIMARIES

Especifica los valores de color principal para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es un miembro de la [**enumeración MFVideoPrimaries.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries)

La [**enumeración MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) identifica las primarias de color asociadas a determinados estándares de vídeo comunes. Si el tipo de medio usa elementos de color principal que no se identifican en la enumeración **MFVideoPrimaries,** establezca el atributo [**MF MT CUSTOM VIDEO \_ \_ \_ \_ PRIMARIES**](mf-mt-custom-video-primaries-attribute.md) en lugar de este atributo.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 




