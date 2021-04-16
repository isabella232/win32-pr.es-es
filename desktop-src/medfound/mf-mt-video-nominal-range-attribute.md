---
description: Especifica el intervalo nominal de la información de color en un tipo de medio de vídeo.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: MF_MT_VIDEO_NOMINAL_RANGE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4539b06281655e079d9ff6ca4000e0ed75462b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678437"
---
# <a name="mf_mt_video_nominal_range-attribute"></a>\_Atributo de \_ \_ intervalo nominal de vídeo MF MT \_

Especifica el intervalo nominal de la información de color en un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El valor de este atributo es un miembro de la enumeración [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

**Codificadores H. 264/AVC:**

En el tipo de medio de salida, el \_ \_ intervalo nominal de vídeo MF MT \_ \_ se puede establecer con **MFNominalRange \_ 0 \_ 255** y **MFNominalRange \_ 16 \_ 235**.

El codificador H. 264/AVC debe tratar **MFNominalRange \_ Unknown** como **MFNominalRange \_ 16 \_ 235**.

El codificador H. 264/AVC debe rechazar un tipo de medio de salida cuando el \_ \_ intervalo nominal de vídeo de MF MT \_ \_ está establecido en **MFNominalRange \_ 48 \_ 208**, **MFNominalRange \_ 64 \_ 127** o en cualquier otro valor no definido en [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).

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

 

 




