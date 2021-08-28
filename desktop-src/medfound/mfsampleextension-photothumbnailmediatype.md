---
description: Contiene EL VALOR DE TIPO DEFIMAMEDIA, que describe el tipo de formato de imagen contenido en el atributo MFSampleExtension \_ PhotoThumbnail.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: MFSampleExtension_PhotoThumbnailMediaType atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77496340d598c7caf1064df0d3fc7e1ae7f112309bf6fbba6a66f3d5516e3828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713605"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>Atributo MFSampleExtension \_ PhotoThumbnailMediaType

Contiene [**EL VALOR DE TIPO**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) DEFIMAMEDIA, que describe el tipo de formato de imagen contenido en el atributo [MFSampleExtension \_ PhotoThumbnail.](mfsampleextension-photothumbnail.md)

## <a name="data-type"></a>Tipo de datos

**IUnknown almacenado** como **IMFMediaType**

## <a name="remarks"></a>Comentarios

Si el atributo [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md) está presente en la muestra de fotos, se requiere MFSampleExtension \_ PhotoThumbnailMediaType y debe contener, como mínimo, [MF MT MAJOR \_ \_ \_ TYPE,](mf-mt-major-type-attribute.md) [MF MT \_ \_ SUBTYPE](mf-mt-subtype-attribute.md) y [MF MT FRAME \_ \_ \_ SIZE](mf-mt-frame-size-attribute.md) que describen la miniatura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




