---
description: En este tema se proporciona información sobre el códec de fotografías de HD nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: C73752AB-3D6E-4D92-9FDE-CB68B6A9743C
title: Información general sobre el formato HD Photo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9275abd4b74c7eb4be7673d85bb4eab5f45a163d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706317"
---
# <a name="hd-photo-format-overview"></a>Información general sobre el formato HD Photo

En este tema se proporciona información sobre el códec de fotografías de HD nativo disponible a través de Windows Imaging Component (WIC).

> [!IMPORTANT]
>
> El formato HD Photo es una implementación previa estándar del formato JPEG XR. El formato JPEG XR se ha implementado completamente en Windows 8. Para obtener más información, consulte la [Introducción al códec JPEG XR](jpeg-xr-codec.md) .

 

En este tema se incluyen las siguientes secciones.

-   [Identidad del códec](#codec-identity)
-   [Encoding](#encoding)
    -   [Opciones del codificador](#encoder-options)
-   [Descodificación](#decoding)
    -   [Compatibilidad con IWICBitmapSourceTransform](#iwicbitmapsourcetransform-support)

## <a name="codec-identity"></a>Identidad del códec

En la tabla siguiente se proporciona información de identificación del códec.



|                        |                                                                                 |
|------------------------|---------------------------------------------------------------------------------|
| Nombres formales         | HD Photo, Windows Media Photo                                                   |
| Extensiones de nombre de archivo | WDP                                                                             |
| Tipo de MIME              | Image/vnd. ms-Photo                                                              |
| Firma de archivo (s)      | Primeros cuatro bytes: 0x4949bc00 (versión 0; versión preliminar), 0x4949bc01 (versión 1,0) |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes nativos del códec HD de HD.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatWmp | 57a37caa-367a-4540-916bf183c5093a4b |
| Descodificador          | CLSID \_ WICWmpDecoder     | a26cec36-234c-4950-ae16e34aace71d0d |
| Codificador          | CLSID \_ WICWmpEncoder     | ac4ce3cb-e1c1-44cd-82155a1665509ec2 |



 

## <a name="encoding"></a>Encoding

La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para los códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

### <a name="encoder-options"></a>Opciones del codificador

Los códecs habilitados para WIC difieren en el nivel de opción de codificación. Las opciones del codificador reflejan las capacidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador. Las opciones del codificador pueden ser opciones básicas de WIC compatibles disponibles para todos los códigos habilitados para WIC (aunque no se admiten necesariamente) o las opciones específicas del códec diseñadas con el códec formato de imagen. Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información sobre el uso de la interfaz **IPropertyBag2** para la codificación de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

El códec HD Photo usa ambas opciones básicas de WIC y proporciona varias opciones de codificación específicas de la foto HD. En la tabla siguiente se enumeran las opciones del codificador que admite el códec fotográfico de HD nativo.

Opciones básicas del codificador WIC

| Nombre de la propiedad | VARTYPE | Intervalo de valores | Valor predeterminado |
|---------------|---------|-------------|---------------|
| [ImageQuality](#imagequality-option) | VT \_ R4 | 0-1,0 | 0.9 |
| [Lossless](#lossless-option) | VT \_ bool | **true**, **false** | **FALSE** |
| [BitmapTransform](#bitmaptransform-option) | VT \_ UI1 | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |   [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |

Opciones de codificador específicas de la foto HD

| Nombre de la propiedad | VARTYPE | Intervalo de valores | Valor predeterminado |
|---------------|---------|-------------|---------------|
| [UseCodecOptions](#usecodecoptions-option) | VT \_ bool | **true**, **false** | **FALSE** |
| [Quality](#quality-option) | VT \_ UI1 | 1 - 255 | 10 |
| [Superpone](#overlap-option) | VT \_ UI1 | 0 - 2 | 1 |
| [Un submuestreo](#subsampling-option) | VT \_ UI1 | 0 - 3 | 3 si ImageQuality > 0,8; de lo contrario, 1; |
| [HorizontalTileSlices](#horizontaltileslices-verticaltileslices-options) | VT \_ UI2 | 0 - 4095 | (ancho de imagen – 1)  >> 8 |
| [VerticalTileSlices](#horizontaltileslices-verticaltileslices-options) | VT \_ UI2 | 0 - 4095 | (alto de imagen – 1)  >> 8 |
| [FrequencyOrder](#frequencyorder-option) | VT \_ bool | **true**, **false** | **TRUE** |
| [InterleavedAlpha](#interleavedalpha-option) | VT \_ bool | **true**, **false** | **FALSE** |
| [AlphaQuality](#alphaquality-option) | VT \_ UI1 | 1 - 255 | 1 |
| [CompressedDomainTranscode](#compresseddomaintranscode-option) | VT \_ bool | **true**, **false** | **TRUE** |
| [ImageDataDiscard](#imagedatadiscard-option) | VT \_ UI1 | 0 - 3 | 0 |
| [AlphaDataDiscard](#alphadatadiscard-option) | VT \_ UI1 | 0 - 4 | no se usa. |
| [IgnoreOverlap](#ignoreoverlap-option) | VT \_ bool | **true**, **false** | **FALSE** |


Si una opción de codificador está presente en la lista de opciones [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.

### <a name="imagequality-option"></a>Opción ImageQuality

Especifica la fidelidad de imagen deseada. 0,0 indica la fidelidad más baja posible y 1,0 especifica la fidelidad más alta. En el formato de imagen de fotográfica HD, un valor 1,0 produce una compresión matemática sin pérdida.

El valor predeterminado es 0,9.

### <a name="compressionquality-option"></a>Opción CompressionQuality

Especifica la calidad de compresión deseada. 0,0 indica que el esquema de compresión eficaz está disponible. Normalmente, este esquema genera una codificación más rápida pero una salida más grande. Un valor de 1,0 especifica el esquema de compresión más eficaz disponible, que normalmente genera una codificación más larga, pero una salida más pequeña.

HD Photo no es compatible con esta opción de codificador. Este valor se omite si está presente en la lista de parámetros [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .

### <a name="lossless-option"></a>Opción sin pérdida

Especifica si se va a utilizar el modo de compresión de pérdida. En el formato de imagen de fotográfica HD, este valor invalida el valor de la opción [ImageQuality](#imagequality-option) .

El valor predeterminado es **FALSE**.

### <a name="bitmaptransform-option"></a>Opción BitmapTransform

Especifica cómo se transforma la imagen durante la descodificación de imágenes. Esta opción debe establecerse en uno de los valores de enumeración [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

El valor predeterminado es [**WICBitmapTransformOptions:: WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).

### <a name="usecodecoptions-option"></a>Opción UseCodecOptions

Si el valor es VARIANT \_ true, las opciones de [calidad](#quality-option), [superposición](#overlap-option)y [submuestreo](#subsampling-option) en lugar del valor de la opción.

El valor predeterminado es **FALSE**.

### <a name="quality-option"></a>Opción de calidad

Especifica la calidad de compresión de la imagen. Un valor de 1 indica el modo sin pérdida. Aumentar los valores produce mayores proporciones de compresión y una calidad de imagen inferior.

El valor predeterminado es 10.

### <a name="overlap-option"></a>Opción de superposición

Especifica el nivel de procesamiento de superposición.

En la tabla siguiente se enumeran los niveles de procesamiento de superposición disponibles.



| Value | Descripción                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | No se habilita el procesamiento de superposición.                                                                                                                                                           |
| 1     | Un nivel de procesamiento de superposición está habilitado, modificando los valores codificados en bloque 4x4 en función de los valores de los bloques vecinos.                                                                       |
| 2     | Se habilitan dos niveles de procesamiento de superposición. Además del procesamiento del primer nivel, los valores codificados de los bloques de macros 16x16 se modifican en función de los valores de los bloques de macros vecinos. |



 

El valor predeterminado es 1.

### <a name="subsampling-option"></a>Opción de submuestreo

Especifica la compresión adicional en el espacio de croma. De esta manera, puede conservar el detalle de luminancia a costa de los detalles de color. Esta opción solo se aplica a las imágenes RGB.

En la tabla siguiente se enumeran las opciones de submuestreo disponibles.



| Value | Descripción                                                                                                                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 3     | la codificación 4:4:4 conserva la resolución de croma completa.                                                                                                                                                                                                                                            |
| 2     | 4:2:2 la codificación reduce la resolución de croma a 1/2 de resolución de luminancia.                                                                                                                                                                                                                      |
| 1     | 4:2:0 la codificación reduce la resolución de croma a 1/4 de resolución de luminancia.                                                                                                                                                                                                                      |
| 0     | 4:0:0 la codificación descarta todo el contenido de croma y conserva únicamente la luminancia. Dado que el códec usa una definición ligeramente modificada de luminancia para mejorar el rendimiento, se recomienda convertir una imagen RGB en monocromo antes de la codificación en lugar de utilizar este modo de submuestreo de croma. |



 

El valor predeterminado es 3 Si [ImageQuality](#imagequality-option) > 0,8; de lo contrario, 1.

### <a name="horizontaltileslices-verticaltileslices-options"></a>HorizontalTileSlices, opciones de VerticalTileSlices

Especifique el mosaico horizontal y vertical de la imagen antes de realizar la codificación de compresión para el rendimiento óptimo de la descodificación de regiones. Al dividir la imagen en mosaicos rectangulares durante la codificación puede descodificar las regiones de la imagen sin procesar todo el flujo de datos comprimidos. El valor predeterminado 0 no especifica ninguna subdivisión, por lo que toda la imagen se trata como un único mosaico. Un valor de 1 para cada parámetro crea una única división horizontal y una única vertical, con lo que la imagen se divide de forma eficaz en cuatro mosaicos de igual tamaño. El valor máximo de 4095 para cada parámetro divide la imagen en las filas del mosaico 4096 con 4096 mosaicos por fila. En otras palabras, los valores de parámetro son iguales al número de mosaicos horizontales y verticales (respectivamente) menos 1. Un icono nunca puede tener menos de 16 píxeles de ancho o alto, de modo que el codificador de imágenes HD podría ajustar este parámetro para mantener el tamaño mínimo de mosaico necesario. Dado que hay una sobrecarga de almacenamiento y procesamiento asociada a cada mosaico, debe elegir estos valores con cuidado para cumplir el escenario específico.

[HorizontalTileSlices](/windows): el valor predeterminado es (ancho de imagen – 1)  >> 8.

[VerticalTileSlices](/windows): el valor predeterminado es (alto de imagen – 1)  >> 8.

### <a name="frequencyorder-option"></a>Opción FrequencyOrder

Especifica que la imagen debe estar codificada en orden de frecuencia. Los datos de la frecuencia más baja aparecen en primer lugar en el archivo y el contenido de la imagen se agrupa por su frecuencia en lugar de su orientación espacial. La organización de un archivo por orden de frecuencia proporciona el mejor rendimiento para cualquier descodificación basada en frecuencias y, por lo tanto, se recomienda. Las implementaciones de dispositivos de los codificadores fotográficas HD pueden organizar un archivo en orden espacial para reducir la superficie de memoria necesaria durante la codificación.

El valor predeterminado es **true** y se recomienda que las aplicaciones y los dispositivos siempre usen el orden de frecuencia a menos que tenga razones de rendimiento o específicas de la aplicación para usar el orden espacial.

### <a name="interleavedalpha-option"></a>Opción InterleavedAlpha

Al establecer esta opción en **true** , se indica al códec que codifique la información del canal alfa como un canal intercalado adicional, sin correlación con los canales de contenido de la imagen. Este modo es útil cuando se necesita descodificar alfa simultáneamente con la imagen en un escenario de streaming.

Si se establece este parámetro en **false** , se produce un canal alfa plano, codificado como una imagen independiente con su propio valor de calidad opcional. Mediante el uso de un canal alfa plano, puede descodificar los datos de la imagen y el canal alfa de manera independiente. Los canales alfa intercalados solo se admiten para determinados formatos de píxeles RGB. Puede asociar un canal alfa plano a cualquier formato de imagen que defina un canal alfa.

El valor predeterminado es **FALSE**.

### <a name="alphaquality-option"></a>Opción AlphaQuality

Especifica la calidad de compresión para la imagen del canal alfa plana. Un valor de 1 establece el modo sin pérdida. Aumentar los valores produce mayores proporciones de compresión y una calidad de imagen inferior.

El valor predeterminado es 1.

### <a name="compresseddomaintranscode-option"></a>Opción CompressedDomainTranscode

Mediante el uso de la foto HD, puede realizar una serie de operaciones de transformación de archivos sin descodificar realmente los datos comprimidos y volver a codificarlos en el archivo de destino. Las operaciones de dominio comprimido son muy eficaces y evitan cualquier pérdida de calidad adicional que sea habitual al descodificar y volver a codificar una imagen comprimida con pérdida.

Se admiten las siguientes operaciones de dominio comprimido:

-   Recortar una región de la imagen.
-   Realice una transformación de rotación/volteo.
-   Descartar los datos de frecuencia (lo que permite crear un archivo de imagen más pequeño).
-   Reorganice la imagen entre el orden secuencial espacial y la frecuencia.

El codificador de imágenes HD realiza una operación de transcodificación de dominios comprimidos al codificar una imagen fotográfica HD mediante un descodificador de fotografías HD como origen de la imagen. En función de las opciones de codificación que haya seleccionado, el códec usará una operación de dominio comprimido si es posible. Si una aplicación decide impedir explícitamente cualquier operación de transcodificación de dominio comprimido, debe establecer la opción *UseCodecOptions* en **true** y la opción *CompressedDomainTranscode* en **false**.

Cuando el códec realiza una operación de dominio comprimido, solo se permiten determinados parámetros de codificador y valores de propiedad.

-   Se omiten las opciones básicas del codificador [ImageQuality](#imagequality-option), [CompressionQuality](/windows) y [Lossless](#lossless-option) .
-   Se omiten la [calidad](#quality-option), la [superposición](#overlap-option), [InterleavedAlpha](#interleavedalpha-option) y [AlphaQuality](#alphaquality-option) de las opciones de codificador específicas de la foto HD.
-   Si está presente, las opciones [HorizontalTileSlices](/windows) y [VerticalTileSlices](/windows) deben establecerse en cero. No se puede cambiar el tamaño de mosaico de una imagen como parte de un transcodificación de dominios comprimidos.
-   Puede cambiar la organización de la imagen entre la frecuencia y la ordenación espacial especificando el valor adecuado de las opciones de [FrequencyOrdering](/windows) .
-   Se puede realizar una operación de giro cardinal o de volteo horizontal/vertical según el valor especificado en la opción de codificador [BitmapTransform](#bitmaptransform-option) .
-   La imagen se puede recortar especificando la región deseada mediante el parámetro [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) del método **WriteSource** Encoder.
-   Los datos alfa y de imagen se pueden descartar especificando los valores adecuados en las opciones [ImageDataDiscard](#imagedatadiscard-option) y/o [AlphaDataDiscard](#alphadatadiscard-option) , reduciendo el tamaño de archivo codificado y reduciendo eficazmente la resolución de la nueva imagen.

El valor predeterminado es **true** y se recomienda que las aplicaciones y los dispositivos siempre usen el orden de frecuencia a menos que tenga razones específicas de rendimiento o aplicación para usar el orden espacial.

### <a name="imagedatadiscard-option"></a>Opción ImageDataDiscard

Este parámetro solo es válido si la opción [CompressedDomainTranscode](#compresseddomaintranscode-option) es **true**; en caso contrario, se omite. [ImageDataDiscard](#imagedatadiscard-option) especifica la cantidad de datos de imagen que se van a descartar durante la transcodificación de un dominio comprimido. Si la imagen contiene un canal alfa intercalado, este descartado de datos se aplica también al canal alfa, con las excepciones que se describen más adelante en esta sección.

Se permiten los siguientes valores.



| Value | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | No se descartan datos de frecuencia de la imagen.                                                                                                                                                                                                                                                                                                                                                                                        |
| 1     | Los FlexBits se descartan, lo que realiza una reducción arbitraria de la calidad de la imagen transcodificada sin cambiar la resolución efectiva de la imagen. La reducción exacta del tamaño de archivo o la reducción de la calidad específica depende de numerosos factores y no se puede especificar ni predecir. Esto valuereturns un error si se especifica para un canal alfa intercalado.                                                    |
| 2     | La banda de datos paso alto Frequency se descarta (lo que también incluye FlexBits), lo que reduce de manera eficaz la resolución de la imagen transcodificada en un factor de 4 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero pierden todos los detalles en cada bloque 4x4 de píxeles. Por lo tanto, debe hacer un muestreo de la imagen transcodificada en consecuencia siempre que la descodifique.                            |
| 3     | Se descartan las bandas de datos de frecuencia paso alto y paso bajo (que también incluyen FlexBits), lo que reduce de manera eficaz la resolución de la imagen transcodificada en un factor de 16 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero pierden todos los detalles en cada adaptativo macrobloque de 16x16 de píxeles. Por lo tanto, debe hacer un muestreo de la imagen transcodificada en consecuencia siempre que la descodifique. |



 

El valor predeterminado es 0.

### <a name="alphadatadiscard-option"></a>Opción AlphaDataDiscard

Esta opción solo es válida si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode-option) es **true** y la imagen contiene un canal alfa plano o intercalado. en caso contrario, se omite. Especifica la cantidad de datos de frecuencia alfa que se descartan durante la transcodificación de un dominio comprimido. Se permiten los siguientes valores para un canal alfa plano.



| Value | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | No se descartan datos de frecuencia de la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 1     | Los FlexBits se descartan, lo que realiza una reducción arbitraria de la calidad del canal alfa plano de la imagen transcodificada sin cambiar la resolución efectiva. La reducción exacta del tamaño de archivo o la reducción de la calidad específica depende de numerosos factores y no se puede especificar ni predecir.                                                                                                                                                                                                                                                |
| 2     | La banda de datos paso alto Frequency se descarta (lo que también incluye FlexBits), lo que reduce la resolución del canal alfa plano de la imagen transcodificada en un factor de 4 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles del canal alfa plano en cada bloque 4x4 de píxeles. Por lo tanto, la imagen transcodificada no se debe mostrar en sentido descendente, siempre que se descodifique. Normalmente, solo debe establecer este valor cuando establezca la propiedad ImageDataDiscard en el mismo valor. |
| 3     | Se descartan las bandas de datos de frecuencia paso alto y paso bajo (que también incluyen FlexBits), lo que reduce de manera eficaz la resolución de la imagen transcodificada en un factor de 16 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles en cada adaptativo macrobloque de 16x16 de píxeles. Por lo tanto, la imagen transcodificada no se debe mostrar en sentido descendente, siempre que se descodifique. Normalmente, solo debe establecer este valor cuando establezca la propiedad ImageDataDiscard en el mismo valor.               |
| 4     | El canal alfa se descarta por completo. El formato de píxel de la imagen transcodificada se cambia para reflejar la eliminación del canal alfa.                                                                                                                                                                                                                                                                                                                                                                                                               |



 

En el caso de las imágenes que contienen canales alfa intercalados, a menos que esta propiedad esté establecida en 4, el canal alfa se procesa de la misma forma que los datos de la imagen, según el valor de la propiedad ImageDataDiscard. Si esta propiedad se establece en 4, el canal alfa intercalado se descarta por completo y el formato de píxel de la imagen transcodificada se cambia en consecuencia.

Ningún valor predeterminado.

### <a name="ignoreoverlap-option"></a>Opción IgnoreOverlap

Esta opción solo es válida si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode-option) es **true** y se solicita una subregión de subcodificación de exactamente uno o más mosaicos. La operación predeterminada para una región de transcodificación (o descodificación) es expandir la región solicitada para incluir los píxeles circundantes necesarios para la descodificación de superposiciones de los bordes de la región. Cuando este parámetro se establece en **true**, los píxeles circundantes se omiten y solo se extraen el mosaico o los mosaicos seleccionados. De nuevo, esto requiere que la región solicitada coincida exactamente con las coordenadas de uno o más mosaicos. Si la imagen de origen no está en mosaico o si la región solicitada especifica algún mosaico parcial, se omite este parámetro.

El valor predeterminado es **FALSE**.

## <a name="decoding"></a>Descodificación

La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md). Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

### <a name="iwicbitmapsourcetransform-support"></a>Compatibilidad con IWICBitmapSourceTransform

Además de las interfaces necesarias para ser un códec habilitado para WIC, el descodificador de fotografías de HD nativo también es compatible con [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform). La interfaz **IWICBitmapSourceTransform** proporciona una opción avanzada para descodificar una secuencia de bits de imagen. En lugar de devolver simplemente una imagen completa mediante [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), la interfaz **IWICBitmapSourceTransform** habilita las siguientes opciones del descodificador.

-   Descodificar una subregión rectangular de la imagen.
-   Descodificación a una resolución más baja
-   Descodificar en un formato de píxel diferente
-   Realización de una transformación (giro/volteo) durante la descodificación

El códec de foto HD nativo proporciona el siguiente nivel de compatibilidad para la interfaz [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) .

### <a name="doessupporttransform"></a>DoesSupportTransform

La implementación nativa es compatible con todas las transformaciones de [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

### <a name="getclosestsize"></a>GetClosestSize

En el caso de las solicitudes que son inferiores a 1/2 la dimensión de la imagen de origen en ambas dimensiones, la foto de HD devuelve el tamaño de imagen del siguiente número entero más grande que se puede dividir uniformemente por un factor de dos. En el resto de los tamaños solicitados, HD Photo devuelve las dimensiones de la imagen original.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

HD Photo devuelve el formato de píxel de la imagen codificada.

### <a name="copypixels"></a>CopyPixels

HD Photo acepta cualquier región solicitada que especifique el parámetro [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) y devuelve esa parte de la imagen.

Los parámetros *uiWidth* y *uiHeight* deben especificar las dimensiones devueltas por la función [**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) . Cualquier otro valor devolverá un error.

El parámetro *pguidDstFormat* debe especificar el formato de píxel devuelto por la función [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) . Cualquier otro valor devuelve un error.

HD Photo acepta cualquier valor permitido para el parámetro *dstTransform* . Tenga en cuenta que los valores permitidos por WIC para este parámetro son distintos de los valores usados por la foto HD para la etiqueta de metadatos de transformación.

 

 
