---
description: Especifica el intervalo nominal de la información de color en un tipo de medio de vídeo.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: MF_MT_VIDEO_NOMINAL_RANGE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b294ea3c63f845b51c9636f78ee78f04135e17929ae6e64d92ab85720f3c7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876725"
---
# <a name="mf_mt_video_nominal_range-attribute"></a>Atributo MF \_ MT \_ VIDEO NOMINAL \_ \_ RANGE

Especifica el intervalo nominal de la información de color en un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es un miembro de la [**enumeración MFNorangeRange.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange)

La constante GUID para este atributo se exporta desde mfuuid.lib.

**Codificadores H.264/AVC:**

En el tipo de medio de salida, MF MT VIDEO NOMINAL RANGE se puede establecer \_ \_ con \_ \_ **MFNorangeRange \_ 0 \_ 255** y **MFNorangeRange \_ 16 \_ 235**.

El codificador H.264/AVC debe tratar **MFNorangeRange \_ Desconocido** como **MFNorangeRange \_ 16 \_ 235**.

El codificador H.264/AVC rechazará un tipo de medio de salida cuando MF MT VIDEO NOMINAL RANGE esté establecido en \_ \_ \_ \_ **MFNorangeRange \_ 48 \_ 208,** **MFNorangeRange \_ 64 \_ 127** o cualquier otro valor no definido en [**MFNorangeRange.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange)

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
</dt> <dt>

[Información de color extendida](extended-color-information.md)
</dt> </dl>

 

 




