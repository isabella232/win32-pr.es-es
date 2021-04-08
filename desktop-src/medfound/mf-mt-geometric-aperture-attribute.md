---
description: Define la abertura geométrica para un tipo de medio de vídeo.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: MF_MT_GEOMETRIC_APERTURE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001500"
---
# <a name="mf_mt_geometric_aperture-attribute"></a>\_Atributo de \_ \_ apertura geométrica de MF MT

Define la abertura geométrica para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

El valor de este atributo es una estructura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

La relación de aspecto de la imagen se calcula con respecto a la abertura geométrica mediante la siguiente fórmula: relación de aspecto de la imagen = (ancho de abertura geométrica/alto de abertura geométrica) × relación de aspecto de píxeles.

Si no se establece este atributo, se supone que la abertura geométrica es todo el fotograma de vídeo. Solo debe establecer este atributo cuando el tipo de medio describe un estándar de vídeo con un área activa definida.

Por ejemplo, en la televisión NTSC, el fotograma de vídeo es 720 × 480 con un área activa de 704 × 480 y una relación de aspecto de 10:11 píxeles. La imagen resultante tiene una relación de aspecto de (704/480) × (10/11) = 4:3.

> [!Note]  
> El presentador predeterminado para el [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR) muestra la abertura geométrica del vídeo, si se especifica.

 

La constante GUID para este atributo se exporta desde mfuuid. lib.

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
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Relación de aspecto de la imagen](picture-aspect-ratio.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**\_ \_ apertura mínima de \_ pantalla MF MT \_**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_apertura de \_ \_ análisis panorámico MF MT \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




