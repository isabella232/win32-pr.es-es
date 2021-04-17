---
description: En este tema se proporciona información sobre el códec JPEG nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Información general sobre el formato JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953d1d6a02e47b41d1b7cf872f3381cd640151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687547"
---
# <a name="jpeg-format-overview"></a>Información general sobre el formato JPEG

En este tema se proporciona información sobre el códec JPEG nativo disponible a través de Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidad del códec

En la tabla siguiente se proporciona información de identificación del códec.



|                        |                                         |
|------------------------|-----------------------------------------|
| Nombres formales         | Formato JPEG (Joint Photographic Experts Group) |
| Extensiones de nombre de archivo | JPE, JPEG, jpg                          |
| Tipo de MIME              | image/JPEG, Image/JPE, Image/jpg        |
| Compatibilidad con las especificaciones  | Especificación JFIF 1,02                 |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes nativos del códec JPEG.



| Componente        | Nombre descriptivo             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatJpeg | 19e4a5aa-5662-4fc5-a0c01758028e1057 |
| Descodificador          | CLSID \_ WICJpegDecoder     | 9456a480-e88b-43ea-9e730b2d9b71b1ca |
| Codificador          | CLSID \_ WICJpegEncoder     | 1a34f5c1-4a5a-46dc-b6441f4567e7a676 |



 

## <a name="encoding"></a>Encoding

La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para los códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

### <a name="encoder-options"></a>Opciones del codificador

Los códecs habilitados para WIC difieren en el nivel de opción de codificación. Las opciones del codificador reflejan las capacidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador. Las opciones del codificador pueden ser opciones básicas de WIC compatibles disponibles para todos los códigos habilitados para WIC (aunque no se admiten necesariamente) o las opciones específicas del códec diseñadas con el códec formato de imagen. Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información sobre el uso de la interfaz **IPropertyBag2** para la codificación de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

El códec JPEG usa las opciones básicas de WIC. En la tabla siguiente se enumeran las opciones del codificador WIC admitidas por el códec JPEG nativo.



| Nombre de la propiedad                                        | VARTYPE           | Intervalo de valores                                                                       | Valor predeterminado                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ImageQuality](#imagequality-option)                 | VT \_ R4            | 0-1,0                                                                           | 0.9                                                                            |
| [BitmapTransform](#bitmaptransform-option)           | VT \_ UI1           | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [Luminancia](#luminance-option)                       | Matriz de VT \_ UI4/VT \_ | 64 entradas (DCT)                                                                  | Tabla de luminancia predeterminada.                                                       |
| [Chrominance](#chrominance-option)                   | Matriz de VT \_ UI4/VT \_ | 64 entradas (DCT)                                                                  | Tabla de crominancia predeterminada.                                                     |
| [JpegYCrCbSubsampling](#jpegycrcbsubsampling-option) | VT \_ UI1           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [SuppressApp0](/windows)                       | VT \_ bool          | **True** / **False**                                                                | **FALSE**                                                                      |



 

Si una opción de codificador está presente en la lista de opciones [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.

### <a name="imagequality-option"></a>Opción ImageQuality

Especifica la fidelidad de imagen deseada. 0,0 indica la fidelidad más baja posible y 1,0 especifica la fidelidad más alta.

El valor predeterminado es 0,9.

### <a name="bitmaptransform-option"></a>Opción BitmapTransform

Especifica cómo se transformará la imagen durante la descodificación de imágenes. Esta opción debe establecerse en uno de los valores de enumeración [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

El valor predeterminado es [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).

### <a name="luminance-option"></a>Opción de luminancia

Especifica la tabla de nivel de brillo de escala de grises que se va a usar para la codificación.

### <a name="chrominance-option"></a>Opción de crominancia

Especifica la tabla de crominancia que se va a utilizar para la codificación.

### <a name="jpegycrcbsubsampling-option"></a>Opción JpegYCrCbSubsampling

Especifica la proporción de submuestreo que se va a usar para la codificación YCrCb.

El valor predeterminado es [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).

### <a name="suppressapp0-option"></a>Opción SuppressApp0

Especifica si se va a suprimir la escritura de metadatos de App0 mientras se codifican los datos de la imagen.

El valor predeterminado es **FALSE**.

## <a name="decoding"></a>Descodificación

La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md). Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

El códec JPEG nativo también admite [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) en la descodificación de fotogramas agregar opciones de avanzada para descodificar una secuencia de imágenes. Para obtener más información acerca de estas opciones avanzadas, consulte la [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

 

 
