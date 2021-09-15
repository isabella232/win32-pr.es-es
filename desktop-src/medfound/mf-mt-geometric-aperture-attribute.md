---
description: Define la apertura geométrica para un tipo de medio de vídeo.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: MF_MT_GEOMETRIC_APERTURE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474153"
---
# <a name="mf_mt_geometric_aperture-attribute"></a>Atributo MF \_ MT \_ GEOMETRIC \_ APERTURE

Define la apertura geométrica para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

El valor de este atributo es una [**estructura MFVideoArea.**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea)

La relación de aspecto de la imagen se calcula en relación con la apertura geométrica, mediante la fórmula siguiente: Relación de aspecto de imagen = (ancho de apertura geométrica/alto de apertura geométrica) × relación de aspecto de píxeles.

Si no se establece este atributo, se supone que la apertura geométrica es todo el fotograma de vídeo. Debe establecer este atributo solo cuando el tipo de medio describa un estándar de vídeo con un área activa definida.

Por ejemplo, en la televisión XEL, el fotograma de vídeo es 720 × 480 con un área activa de 704 × 480 y una relación de aspecto de 10:11 píxeles. La imagen resultante tiene una relación de aspecto de (704/480) × (10/11) = 4:3.

> [!Note]  
> El presentador predeterminado para [el representador](enhanced-video-renderer.md) de vídeo mejorado (EVR) muestra la apertura geométrica del vídeo, si se especifica.

 

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="examples"></a>Ejemplos


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
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

[**APERTURA \_ DE PANTALLA MÍNIMA \_ DE \_ \_ MF MT**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




