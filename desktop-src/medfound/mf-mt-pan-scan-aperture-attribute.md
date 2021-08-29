---
description: Define el diafragma de panorámica/examen, que es la región de vídeo 4&215;3 que se debe mostrar en \# modo de panorámica o examen.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: MF_MT_PAN_SCAN_APERTURE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d9b8d4ed5e8fe8887c229d83ffc276bf4d90b968834161ab60cc5d102095bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940615"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a>Atributo MF \_ MT \_ PAN SCAN \_ \_ APERTURE

Define el diafragma de panorámica/examen, que es la región de vídeo de 4×3 que se debe mostrar en modo de panorámica o examen.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Comentarios

El valor del atributo es [**una estructura MFVideoArea.**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea)

Este atributo se usa para recortar vídeo de pantalla ancha a una relación de aspecto 4:3. La apertura de panorámica/examen solo se usa en el modo de panorámica y examen, que se habilita estableciendo el atributo [**MF MT PAN SCAN \_ \_ \_ \_ ENABLED**](mf-mt-pan-scan-enabled-attribute.md) en **TRUE.**

Si el modo de panorámica/examen no está habilitado, use el diafragma de presentación, especificado por el atributo [**MF MT MINIMUM DISPLAY \_ \_ \_ \_ APERTURE.**](mf-mt-minimum-display-aperture-attribute.md)

Si no se establece este atributo, se supone que el diafragma de panorámica o digitalización es todo el fotograma de vídeo.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Relación de aspecto de la imagen](picture-aspect-ratio.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**APERTURA \_ GEOMÉTRICA DE MF MT \_ \_**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**APERTURA \_ DE PANTALLA MÍNIMA \_ DE \_ \_ MF MT**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ PAN \_ SCAN \_ ENABLED**](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




