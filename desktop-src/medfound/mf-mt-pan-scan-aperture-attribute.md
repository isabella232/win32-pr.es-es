---
description: Define la apertura de panorámica/digitalización, que es la región 4&215;3 del vídeo que debe mostrarse en modo \# de panorámica/examen.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: MF_MT_PAN_SCAN_APERTURE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363975"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a>Atributo MF \_ MT \_ PAN SCAN \_ \_ APERTURE

Define la apertura de panorámica/examen, que es la región de 4×3 del vídeo que debe mostrarse en modo de panorámica/examen.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

El valor del atributo es [**una estructura MFVideoArea.**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea)

Este atributo se usa para recortar vídeo de pantalla ancha a una relación de aspecto de 4:3. La apertura de panorámica/examen solo se usa en el modo de panorámica y examen, que se habilita estableciendo el atributo [**MF MT PAN SCAN \_ \_ \_ \_ ENABLED**](mf-mt-pan-scan-enabled-attribute.md) en **TRUE.**

Si el modo de panorámica/examen no está habilitado, use la apertura de pantalla, especificada por el atributo [**MF MT MINIMUM DISPLAY \_ \_ \_ \_ APERTURE.**](mf-mt-minimum-display-aperture-attribute.md)

Si no se establece este atributo, se supone que la apertura de panorámica o digitalización es todo el fotograma de vídeo.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
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

 

 




