---
description: Contiene la miniatura de la fotografía de un IMFSample.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: MFSampleExtension_PhotoThumbnail atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155961"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a>MFSampleExtension \_ Fotominiaturas, atributo

Contiene la miniatura de la fotografía de un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).

## <a name="data-type"></a>Tipo de datos

**IUnknown** almacenado como **IMFMediaBuffer**

La miniatura se configura mediante **KSPROPERTYSETID \_ ExtendedCameraControl**.

## <a name="remarks"></a>Observaciones

Este atributo se establece en el [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) proporcionado por MFT0 y es la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) asociado a la miniatura de la fotografía.

El formato de la miniatura de la fotografía puede ser JPEG (imagen de tipo principal), NV12 o ARGB32.

[MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) es necesario para que las miniaturas describan el tipo de medio.

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

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
