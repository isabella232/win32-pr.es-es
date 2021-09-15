---
description: Contiene EL VALOR DE LA PROPIEDADMEDIATYPE, que describe el tipo de formato de imagen contenido en el atributo MFSampleExtension \_ PhotoThumbnail.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: MFSampleExtension_PhotoThumbnailMediaType atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580285"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>Atributo MFSampleExtension \_ PhotoThumbnailMediaType

Contiene [**EL VALOR DE LA PROPIEDADMEDIATYPE,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que describe el tipo de formato de imagen contenido en el [atributo MFSampleExtension \_ PhotoThumbnail.](mfsampleextension-photothumbnail.md)

## <a name="data-type"></a>Tipo de datos

**IUnknown almacenado** como **IMFMediaType**

## <a name="remarks"></a>Observaciones

Si el atributo [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md) está presente en la muestra de foto, se requiere MFSampleExtension \_ PhotoThumbnailMediaType y debe contener, como mínimo, [MF MT MAJOR \_ \_ \_ TYPE](mf-mt-major-type-attribute.md), [MF MT \_ \_ SUBTYPE](mf-mt-subtype-attribute.md) y [MF MT FRAME \_ \_ \_ SIZE](mf-mt-frame-size-attribute.md) que describen la miniatura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




