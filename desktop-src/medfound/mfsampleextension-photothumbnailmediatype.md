---
description: Contiene el IMFMediaType que describe el tipo de formato de imagen contenido en el \_ atributo de Fotominiatura MFSampleExtension.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: MFSampleExtension_PhotoThumbnailMediaType atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721343"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>\_Atributo PhotoThumbnailMediaType de MFSampleExtension

Contiene el [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que describe el tipo de formato de imagen contenido en el atributo de [ \_ fotominiatura MFSampleExtension](mfsampleextension-photothumbnail.md) .

## <a name="data-type"></a>Tipo de datos

**IUnknown** almacenado como **IMFMediaType**

## <a name="remarks"></a>Observaciones

Si el atributo de [ \_ fotominiatura MFSampleExtension](mfsampleextension-photothumbnail.md) está presente en el ejemplo Photo, \_ se requiere MFSampleExtension PhotoThumbnailMediaType y debe contener, como mínimo, el [ \_ tipo de módulo MF MT \_ major \_ ](mf-mt-major-type-attribute.md), el [ \_ \_ subtipo MF MT](mf-mt-subtype-attribute.md) y [ \_ \_ \_ el tamaño de marco MF MT](mf-mt-frame-size-attribute.md) que describen la miniatura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Fotominiatura MFSampleExtension \_](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




