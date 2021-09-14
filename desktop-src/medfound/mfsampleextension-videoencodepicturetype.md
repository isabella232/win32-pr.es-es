---
description: Especifica el tipo de imagen que genera un codificador de vídeo.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: MFSampleExtension_VideoEncodePictureType atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe0df0e4f3163e7c8c0581c5c7c2a854555eec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363762"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a>Atributo MFSampleExtension \_ VideoEncodePictureType

Especifica el tipo de imagen que genera un codificador de vídeo.

## <a name="data-type"></a>Tipo de datos

**eAVEncH264PictureType \_ B** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**SAMPLESample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Observaciones

El codificador de vídeo [**H.264**](h-264-video-encoder.md) establece este atributo en los ejemplos de salida que genera. El valor del atributo es miembro de la [**enumeración eAVEncH264PictureType.**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Codificador de vídeo H.264**](h-264-video-encoder.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> </dl>

 

 




