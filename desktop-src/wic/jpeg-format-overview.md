---
description: En este tema se proporciona información sobre el códec JPEG nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Introducción al formato JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2acc7fcd71fc962d3321112d342f675b878188
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251769"
---
# <a name="jpeg-format-overview"></a>Introducción al formato JPEG

En este tema se proporciona información sobre el códec JPEG nativo disponible a través de Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidad de códec

En la tabla siguiente se proporciona información de identificación de códecs.



|   Componente            | Descripción                             |
|------------------------|-----------------------------------------|
| Nombres formales         | Formato JPEG (Joint Photographic Experts Group) |
| Extensiones de nombre de archivo | jpe, jpeg, jpg                          |
| Tipo de MIME              | image/jpeg, image/jpe, image/jpg        |
| Compatibilidad con especificaciones  | Especificación JFIF 1.02                 |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec JPEG nativos.



| Componente        | Nombre descriptivo             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatFormatFormateg | 19e4a5aa-5662-4fc5-a0c01758028e1057 |
| Descodificador          | CLSID \_ WICShuegDecoder     | 9456a480-e88b-43ea-9e730b2d9b71b1ca |
| Codificador          | CLSID \_ WICShuegEncoder     | 1a34f5c1-4a5a-46dc-b6441f4567e7a676 |



 

## <a name="encoding"></a>Encoding

La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, vea Información general [sobre codificación.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Opciones del codificador

Los códecs habilitados para WIC difieren en el nivel de opción de codificación. Las opciones del codificador reflejan las funcionalidades de un codificador de imagen y cada códec nativo admite un conjunto de estas opciones de codificador. Las opciones de codificador pueden ser opciones básicas compatibles con WIC disponibles para todos los códigos habilitados para WIC (aunque no necesariamente admitidos) o opciones específicas del códec diseñadas por el códec de formato de imagen. Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la [**interfaz IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información sobre el uso de la **interfaz IPropertyBag2 para** la codificación WIC , vea Información general [sobre la codificación.](-wic-creating-encoder.md)

El códec JPEG usa opciones básicas de WIC. En la tabla siguiente se enumeran las opciones del codificador WIC compatibles con el códec JPEG nativo.



| Nombre de la propiedad                                        | VARTYPE           | Intervalo de valores                                                                       | Valor predeterminado                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ImageQuality](#imagequality-option)                 | VT \_ R4            | 0 - 1.0                                                                           | 0.9                                                                            |
| [BitmapTransform](#bitmaptransform-option)           | VT \_ UI1           | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [Luminancia](#luminance-option)                       | VT \_ UI4/VT \_ ARRAY | 64 entradas (DCT)                                                                  | Tabla de luminosidad predeterminada.                                                       |
| [Chrominance](#chrominance-option)                   | VT \_ UI4/VT \_ ARRAY | 64 entradas (DCT)                                                                  | Tabla de chrominance predeterminada.                                                     |
| [JpegYCrCbSubsampling](#jpegycrcbsubsampling-option) | VT \_ UI1           | [**WICOptionegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [**WICCbegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [SuppressApp0](/windows)                       | VT \_ BOOL          | **TRUE** / **FALSE**                                                                | **FALSE**                                                                      |



 

Si hay una opción de codificador en la lista [**de opciones IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.

### <a name="imagequality-option"></a>Opción ImageQuality

Especifica la fidelidad de la imagen deseada. 0,0 indica la fidelidad más baja posible y 1,0 especifica la fidelidad más alta.

El valor predeterminado es 0,9.

### <a name="bitmaptransform-option"></a>Opción BitmapTransform

Especifica cómo se va a transformar la imagen durante la decodificación de la imagen. Esta opción debe establecerse en uno de los valores de enumeración [**WICBitmapTransformOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

El valor predeterminado es [**WICBitmapTransformRotate0.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

### <a name="luminance-option"></a>Opción de luminosidad

Especifica la tabla de nivel de brillo de escala de grises que se usará para la codificación.

### <a name="chrominance-option"></a>Opción chrominance

Especifica la tabla chrominance que se usará para la codificación.

### <a name="jpegycrcbsubsampling-option"></a>JpegYCrCbSubsampling (opción)

Especifica la proporción de submuestreo que se usará para la codificación YCrCb.

El valor predeterminado [**es WICOmisiónegYCrCbSubsampling420.**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption)

### <a name="suppressapp0-option"></a>Opción SuppressApp0

Especifica si se debe suprimir la escritura de metadatos de App0 al codificar los datos de la imagen.

El valor predeterminado es **FALSE**.

## <a name="decoding"></a>Descodificación

La API de decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre lacoding de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md) Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

El códec JPEG nativo también admite [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) en la codificación de fotogramas agregando opciones avanzadas para la decodización de un flujo de imagen. Para obtener más información sobre estas opciones avanzadas, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

 

 
