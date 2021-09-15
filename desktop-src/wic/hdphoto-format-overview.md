---
description: En este tema se proporciona información sobre el códec hd photo nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: C73752AB-3D6E-4D92-9FDE-CB68B6A9743C
title: Información general sobre el formato HD Photo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c526667c6bf77d340e895bdb66dc073134c33d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466874"
---
# <a name="hd-photo-format-overview"></a>Información general sobre el formato HD Photo

En este tema se proporciona información sobre el códec hd photo nativo disponible a través de Windows Imaging Component (WIC).

> [!IMPORTANT]
>
> El formato HD Photo es una implementación estándar del formato JPEG XR. El formato JPEG XR se ha implementado completamente en Windows 8. Para más [información, consulte Información general sobre el códec JPEG XR.](jpeg-xr-codec.md)

 

En este tema se incluyen las siguientes secciones.

-   [Identidad de códec](#codec-identity)
-   [Encoding](#encoding)
    -   [Opciones del codificador](#encoder-options)
-   [Descodificación](#decoding)
    -   [Compatibilidad con IWICBitmapSourceTransform](#iwicbitmapsourcetransform-support)

## <a name="codec-identity"></a>Identidad de códec

En la tabla siguiente se proporciona información de identificación de códecs.



|   Componente            | Descripción                                                                     |
|------------------------|---------------------------------------------------------------------------------|
| Nombres formales         | HD Photo, Windows Media Photo                                                   |
| Extensiones de nombre de archivo | Wdp                                                                             |
| Tipo de MIME              | image/vnd.ms-photo                                                              |
| Firmas de archivo      | Primeros cuatro bytes: 0x4949bc00 (versión 0; versión anterior), 0x4949bc01 (versión 1.0) |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes nativos del códec HD Photo.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatWmp | 57a37caa-367a-4540-916bf183c5093a4b |
| Descodificador          | CLSID \_ WICWmpDecoder     | a26cec36-234c-4950-ae16e34aace71d0d |
| Codificador          | CLSID \_ WICWmpEncoder     | ac4ce3cb-e1c1-44cd-82155a1665509ec2 |



 

## <a name="encoding"></a>Encoding

La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, vea Información general [sobre codificación.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Opciones del codificador

Los códecs habilitados para WIC difieren en el nivel de opción de codificación. Las opciones del codificador reflejan las funcionalidades de un codificador de imagen y cada códec nativo admite un conjunto de estas opciones de codificador. Las opciones de codificador pueden ser opciones básicas compatibles con WIC disponibles para todos los códigos habilitados para WIC (aunque no necesariamente admitidos) o opciones específicas del códec diseñadas por el códec de formato de imagen. Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la [**interfaz IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información sobre el uso de la **interfaz IPropertyBag2 para** la codificación WIC, vea Información general [sobre la codificación.](-wic-creating-encoder.md)

El códec HD Photo usa ambas opciones básicas de WIC y proporciona varias opciones de codificación específicas de hd photo. En la tabla siguiente se enumeran las opciones de codificador compatibles con el códec hd photo nativo.

Opciones básicas del codificador WIC

| Nombre de la propiedad | VARTYPE | Intervalo de valores | Valor predeterminado |
|---------------|---------|-------------|---------------|
| [ImageQuality](#imagequality-option) | VT \_ R4 | 0 - 1.0 | 0.9 |
| [Lossless](#lossless-option) | VT \_ BOOL | **TRUE**, **FALSE** | **FALSE** |
| [BitmapTransform](#bitmaptransform-option) | VT \_ UI1 | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |   [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |

Opciones específicas del codificador de fotos en HD

| Nombre de la propiedad | VARTYPE | Intervalo de valores | Valor predeterminado |
|---------------|---------|-------------|---------------|
| [UseCodecOptions](#usecodecoptions-option) | VT \_ BOOL | **TRUE**, **FALSE** | **FALSE** |
| [Quality](#quality-option) | VT \_ UI1 | 1 - 255 | 10 |
| [Traslapo](#overlap-option) | VT \_ UI1 | 0 - 2 | 1 |
| [Submuestreo](#subsampling-option) | VT \_ UI1 | 0 - 3 | 3 si ImageQuality > 0.8; de lo contrario, 1; |
| [HorizontalTileSlices](#horizontaltileslices-verticaltileslices-options) | VT \_ UI2 | 0 - 4095 | (ancho de imagen – 1) >> 8 |
| [VerticalTileSlices](#horizontaltileslices-verticaltileslices-options) | VT \_ UI2 | 0 - 4095 | (alto de la imagen : 1) >> 8 |
| [FrequencyOrder](#frequencyorder-option) | VT \_ BOOL | **TRUE**, **FALSE** | **TRUE** |
| [InterleavedAlpha](#interleavedalpha-option) | VT \_ BOOL | **TRUE**, **FALSE** | **FALSE** |
| [AlphaQuality](#alphaquality-option) | VT \_ UI1 | 1 - 255 | 1 |
| [CompressedDomainTranscode](#compresseddomaintranscode-option) | VT \_ BOOL | **TRUE**, **FALSE** | **TRUE** |
| [ImageDataDiscard](#imagedatadiscard-option) | VT \_ UI1 | 0 - 3 | 0 |
| [AlphaDataDiscard](#alphadatadiscard-option) | VT \_ UI1 | 0 - 4 | no se usa. |
| [IgnoreOverlap](#ignoreoverlap-option) | VT \_ BOOL | **TRUE**, **FALSE** | **FALSE** |


Si hay una opción de codificador en la [**lista de opciones IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.

### <a name="imagequality-option"></a>Opción ImageQuality

Especifica la fidelidad de la imagen deseada. 0,0 indica la fidelidad más baja posible y 1,0 especifica la fidelidad más alta. Para el formato de imagen hd photo, un valor 1.0 da como resultado una compresión matemáticamente sin pérdida.

El valor predeterminado es 0,9.

### <a name="compressionquality-option"></a>CompressionQuality (opción)

Especifica la calidad de compresión deseada. 0.0 indica el esquema de compresión eficaz disponible. Normalmente, este esquema genera una codificación más rápida, pero una salida mayor. Un valor de 1.0 especifica el esquema de compresión más eficaz disponible, que normalmente genera una codificación más larga pero una salida más pequeña.

HD Photo no admite esta opción de codificador. Este valor se omite si está presente en la [**lista de parámetros IPropertyBag2.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))

### <a name="lossless-option"></a>Opción sin pérdida

Especifica si se debe usar el modo de compresión de pérdidas. En el caso del formato de imagen hd photo, este valor invalida el [valor de la opción ImageQuality.](#imagequality-option)

El valor predeterminado es **FALSE**.

### <a name="bitmaptransform-option"></a>Opción BitmapTransform

Especifica cómo se transforma la imagen durante la decodificación de la imagen. Debe establecer esta opción en uno de los valores de enumeración [**WICBitmapTransformOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

El valor predeterminado es [**WICBitmapTransformOptions::WICBitmapTransformRotate0.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

### <a name="usecodecoptions-option"></a>Opción UseCodecOptions

Si el valor es VARIANT \_ TRUE, las [opciones Calidad,](#quality-option) [Superposición](#overlap-option)y [Submuestreo](#subsampling-option) en lugar del valor de opción.

El valor predeterminado es **FALSE**.

### <a name="quality-option"></a>Opción de calidad

Especifica la calidad de compresión de la imagen. Un valor de 1 indica el modo sin pérdida de datos. Al aumentar los valores, se aumentan las relaciones de compresión y se reduce la calidad de la imagen.

El valor predeterminado es 10.

### <a name="overlap-option"></a>Overlap (Opción)

Especifica el nivel de procesamiento de superposición.

En la tabla siguiente se enumeran los niveles de procesamiento de superposición disponibles.



| Value | Descripción                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | No se habilita el procesamiento de superposición.                                                                                                                                                           |
| 1     | Se habilita un nivel de procesamiento de superposición, modificando los valores codificados en bloques 4x4 en función de los valores de los bloques vecinos.                                                                       |
| 2     | Se habilitan dos niveles de procesamiento de superposición. Además del procesamiento de primer nivel, los valores codificados de bloques de macro de 16 x 16 se modifican en función de los valores de los bloques de macro vecinos. |



 

El valor predeterminado es 1.

### <a name="subsampling-option"></a>Opción de submuestreo

Especifica compresión adicional en el espacio de la barra espaciadora. De esta manera, puede conservar los detalles de luminosidad a costa de los detalles de color . Esta opción solo se aplica a las imágenes RGB.

En la tabla siguiente se enumeran las opciones de submuestreo disponibles.



| Value | Descripción                                                                                                                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 3     | La codificación 4:4:4 conserva la resolución completa del conflicto.                                                                                                                                                                                                                                            |
| 2     | La codificación 4:2:2 reduce la resolución de los ruidos a 1/2 de resolución de luminosidad.                                                                                                                                                                                                                      |
| 1     | La codificación 4:2:0 reduce la resolución de los ruidos a 1/4 de resolución de luminosidad.                                                                                                                                                                                                                      |
| 0     | La codificación 4:0:0 descarta todo el contenido de la escala y solo conserva la luminosidad. Dado que el códec usa una definición ligeramente modificada de luminosidad para mejorar el rendimiento, se recomienda convertir una imagen RGB a monocromática antes de la codificación en lugar de usar este modo de submuestreo. |



 

El valor predeterminado es 3 si [ImageQuality](#imagequality-option) > 0,8; de lo contrario, 1.

### <a name="horizontaltileslices-verticaltileslices-options"></a>HorizontalTileSlices, Opciones de VerticalTileSlices

Especifique el mosaico horizontal y vertical de la imagen antes de realizar la codificación de compresión para obtener un rendimiento óptimo de descodificación de región. Al dividir la imagen en iconos rectangulares durante la codificación, puede descodificar regiones de la imagen sin procesar todo el flujo de datos comprimido. El valor predeterminado de 0 no especifica ninguna subdivisión, por lo que toda la imagen se trata como un solo icono. Un valor de 1 para cada parámetro crea una única división horizontal y una sola división vertical, dividiendo eficazmente la imagen en cuatro iconos de igual tamaño. El valor máximo de 4095 para cada parámetro divide la imagen en 4096 filas de mosaico con 4096 iconos por fila. En otras palabras, los valores de parámetro son iguales al número de mosaicos horizontales y verticales (respectivamente) menos 1. Un icono nunca puede tener menos de 16 píxeles de ancho o alto, por lo que el codificador HD Photo podría ajustar este parámetro para mantener el tamaño mínimo de mosaico necesario. Dado que hay una sobrecarga de almacenamiento y procesamiento asociada a cada icono, debe elegir estos valores cuidadosamente para satisfacer el escenario específico.

[HorizontalTileSlices:](/windows)el valor predeterminado es (Ancho de imagen – 1) >> 8.

[VerticalTileSlices:](/windows)el valor predeterminado es (Alto de la imagen – 1) >> 8.

### <a name="frequencyorder-option"></a>Opción FrequencyOrder

Especifica que la imagen debe codificarse en orden de frecuencia. Los datos de frecuencia más baja aparecen primero en el archivo y el contenido de la imagen se agrupa por su frecuencia en lugar de por su orientación espacial. La organización de un archivo por orden de frecuencia proporciona el mejor rendimiento para cualquier decodificación basada en frecuencia y, por tanto, se recomienda. Las implementaciones de dispositivos de codificadores HD Photo pueden organizar un archivo en orden espacial para reducir la superficie de memoria necesaria durante la codificación.

El valor predeterminado es **TRUE y** se recomienda que las aplicaciones y los dispositivos siempre usen el orden de frecuencia, a menos que tenga motivos específicos del rendimiento o de la aplicación para usar el orden espacial.

### <a name="interleavedalpha-option"></a>Opción InterleavedAlpha

Al establecer esta opción en **TRUE,** se indica al códec que codifica la información del canal alfa como un canal intercalado adicional, sin correlación con los canales de contenido de la imagen. Este modo es útil cuando necesita descodificar alfa simultáneamente con la imagen en un escenario de streaming.

Si se establece este parámetro en **FALSE,** se genera un canal alfa planar, codificado como una imagen independiente con su propio valor de calidad opcional. Mediante el uso de un canal alfa planar, puede descodificar los datos de imagen y el canal alfa de forma independiente. Los canales alfa intercalados solo se admiten para determinados formatos de píxel RGB. Puede asociar un canal alfa planar con cualquier formato de imagen que defina un canal alfa.

El valor predeterminado es **FALSE**.

### <a name="alphaquality-option"></a>Opción AlphaQuality

Especifica la calidad de compresión de la imagen de canal alfa planar. Un valor de 1 establece el modo sin pérdida. Al aumentar los valores, se aumentan las relaciones de compresión y se reduce la calidad de la imagen.

El valor predeterminado es 1.

### <a name="compresseddomaintranscode-option"></a>CompressedDomainTranscode (opción)

Con HD Photo puede realizar una serie de operaciones de transformación de archivos sin realmente descodir los datos comprimidos y volver a codificar en el archivo de destino. Las operaciones de dominio comprimido son muy eficaces y evitan cualquier pérdida de calidad adicional típica al descodificar y volver a codificar una imagen comprimida por pérdida.

Se admiten las siguientes operaciones de dominio comprimido:

-   Recortar una región de la imagen.
-   Realice una transformación de rotación o de volteo.
-   Descartar datos de frecuencia (lo que permite crear un archivo de imagen más pequeño).
-   Reorganizar la imagen entre el orden secuencial espacial y de frecuencia.

El codificador HD Photo realiza una operación de transcodificación de dominios comprimidos cuando codifica una imagen de foto de HD mediante un descodificador hd photo como origen de la imagen. En función de las opciones de codificación seleccionadas, el códec usa una operación de dominio comprimido si es posible. Si una aplicación decide impedir explícitamente las operaciones de transcodificación de dominios comprimidos, debe establecer la opción *UseCodecOptions* en **TRUE** y la opción *CompressedDomainTranscode* en **FALSE.**

Cuando el códec realiza una operación de dominio comprimido, solo se permiten ciertos parámetros de codificador y valores de propiedad.

-   Se omiten las opciones básicas del codificador [ImageQuality,](#imagequality-option) [CompressionQuality](/windows) [y Lossless.](#lossless-option)
-   Se omiten las opciones de codificador específicas de hd Photo [Quality](#quality-option), [Overlap,](#overlap-option) [InterleavedAlpha](#interleavedalpha-option) y [AlphaQuality.](#alphaquality-option)
-   Si está presente, [las opciones HorizontalTileSlices](/windows) y [VerticalTileSlices](/windows) deben establecerse en cero. El tamaño del icono de una imagen no se puede cambiar como parte de una transcodificación de dominio comprimido.
-   Puede cambiar la organización de la imagen entre la frecuencia y el orden espacial especificando el valor adecuado de las [opciones FrequencyOrdering.](/windows)
-   Se puede realizar una rotación cardinal o una operación de volteo horizontal o vertical en función del valor especificado en la opción del codificador [BitmapTransform.](#bitmaptransform-option)
-   La imagen se puede recortar especificando la región deseada mediante el parámetro [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) del método de codificador **WriteSource.**
-   Los datos de imagen o alfa se pueden descartar especificando los valores adecuados en las opciones [ImageDataDiscard](#imagedatadiscard-option) o [AlphaDataDiscard,](#alphadatadiscard-option) lo que reduce el tamaño de archivo codificado y reduce eficazmente la resolución de la nueva imagen.

El valor predeterminado es **TRUE y** se recomienda que las aplicaciones y los dispositivos siempre usen el orden de frecuencia, a menos que tenga motivos específicos de rendimiento o de aplicación para usar el orden espacial.

### <a name="imagedatadiscard-option"></a>Opción ImageDataDiscard

Este parámetro solo es válido si la [opción CompressedDomainTranscode](#compresseddomaintranscode-option) es **TRUE**; De lo contrario, se omite. [ImageDataDiscard](#imagedatadiscard-option) especifica la cantidad de datos de imagen que se descartarán durante una transcodificación de dominio comprimido. Si la imagen contiene un canal alfa intercalado, este descarte de datos se aplica también al canal alfa, con las excepciones como se describe más adelante en esta sección.

Se permiten los valores siguientes.



| Value | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | No se descartan datos de frecuencia de la imagen.                                                                                                                                                                                                                                                                                                                                                                                        |
| 1     | Los FlexBits se descartan, lo que reduce arbitrariamente la calidad de la imagen transcodificada sin cambiar la resolución efectiva de la imagen. La reducción exacta del tamaño de archivo o la reducción de calidad específica depende de numerosos factores y no se puede especificar ni predecir. Este valor devuelve un error si se especifica para un canal alfa intercalado.                                                    |
| 2     | La banda de datos de frecuencia HighPass se descarta (que también incluye los FlexBits), lo que reduce eficazmente la resolución de la imagen transcodificada en un factor de 4 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero pierde todos los detalles de cada bloque de píxeles de 4x4. Por lo tanto, debe muestrear la imagen transcodificada en consecuencia cada vez que la descodifique.                            |
| 3     | Las bandas de datos de frecuencia HighPass y LowPass se descartan (lo que también incluye los FlexBits), lo que reduce eficazmente la resolución de la imagen transcodificada en un factor de 16 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero pierde todos los detalles de cada macrobloque de 16 x 16 píxeles. Por lo tanto, debe muestrear la imagen transcodificada en consecuencia cada vez que la descodifique. |



 

El valor predeterminado es 0.

### <a name="alphadatadiscard-option"></a>Opción AlphaDataDiscard

Esta opción solo es válida si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode-option) es **TRUE** y la imagen contiene un canal alfa planar o intercalado; De lo contrario, se omite. Especifica la cantidad de datos de frecuencia alfa que se descartarán durante una transcodificación de dominio comprimido. Se permiten los siguientes valores para un canal alfa planar.



| Value | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | No se descartan datos de frecuencia de la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 1     | Los FlexBits se descartan, lo que hace una reducción arbitraria de la calidad del canal alfa planar para la imagen transcodificada sin cambiar la resolución efectiva. La reducción exacta del tamaño de archivo o la reducción de calidad específica depende de numerosos factores y no se puede especificar ni predecir.                                                                                                                                                                                                                                                |
| 2     | Se descarta la banda de datos de frecuencia HighPass (que también incluye los FlexBits), lo que reduce eficazmente la resolución del canal alfa planar de imagen transcodificada en un factor de 4 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles del canal alfa planar en cada bloque de 4 x 4 píxeles. Por lo tanto, la imagen transcodificada se debe muestrear en consecuencia cada vez que se descodifica. Normalmente, debe establecer este valor solo cuando establezca la propiedad ImageDataDiscard en el mismo valor. |
| 3     | Las bandas de datos de frecuencia HighPass y LowPass se descartan (lo que también incluye los FlexBits), lo que reduce eficazmente la resolución de la imagen transcodificada en un factor de 16 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles de cada macrobloque de 16 x 16 píxeles. Por lo tanto, la imagen transcodificada se debe muestrear en consecuencia cada vez que se descodifica. Normalmente, este valor solo se debe establecer cuando se establece la propiedad ImageDataDiscard en el mismo valor.               |
| 4     | El canal Alfa se descarta completamente. El formato de píxel de la imagen transcodificada se cambia para reflejar la eliminación del canal alfa.                                                                                                                                                                                                                                                                                                                                                                                                               |



 

En el caso de las imágenes que contienen canales alfa intercalados, a menos que esta propiedad esté establecida en 4, el canal alfa se procesa igual que los datos de imagen, según el valor de la propiedad ImageDataDiscard. Si esta propiedad se establece en 4, el canal alfa intercalado se descarta completamente y el formato de píxel de la imagen transcodificada cambia en consecuencia.

Ningún valor predeterminado.

### <a name="ignoreoverlap-option"></a>Opción IgnoreOverlap

Esta opción solo es válida si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode-option) es **TRUE** y se solicita una transcodificación de subr regiones de exactamente uno o varios iconos. La operación predeterminada para una transcodificación de región (o descodificación) es expandir la región solicitada para incluir los píxeles circundantes necesarios para la descodificación superpuesta de los bordes de la región. Cuando este parámetro se establece en **TRUE,** se omiten los píxeles circundantes y solo se extraen los iconos o mosaicos seleccionados. De nuevo, esto requiere que la región solicitada coincida exactamente con las coordenadas de uno o varios iconos. Si la imagen de origen no está en mosaico o si la región solicitada especifica iconos parciales, se omite este parámetro.

El valor predeterminado es **FALSE**.

## <a name="decoding"></a>Descodificación

La API de decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre lacodación de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md) Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

### <a name="iwicbitmapsourcetransform-support"></a>Compatibilidad con IWICBitmapSourceTransform

Además de las interfaces necesarias para ser un códec habilitado para WIC, el descodificador hd photo nativo también admite [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform). La **interfaz IWICBitmapSourceTransform** proporciona una opción avanzada para lacodización de un flujo de bits de imagen. En lugar de simplemente devolver una imagen completa mediante [**IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)la interfaz **IWICBitmapSourceTransform** habilita las siguientes opciones de descodificador.

-   Descodificar una subrcuera rectangular de la imagen.
-   Descodificación a una resolución inferior
-   Descodificación a un formato de píxel diferente
-   Realización de una transformación (rotación/volteo) durante lacodización

El códec hd photo nativo proporciona el siguiente nivel de compatibilidad con la [**interfaz IWICBitmapSourceTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)

### <a name="doessupporttransform"></a>DoesSupportTransform

La implementación nativa admite [**todas las transformaciones WICBitmapTransformOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

### <a name="getclosestsize"></a>GetClosestSize

Para las solicitudes que son inferiores a 1/2 la dimensión de la imagen de origen en ambas dimensiones, HD Photo devuelve el siguiente tamaño de imagen entero más grande que se puede dividir uniformemente por un factor de dos. Para todos los demás tamaños solicitados, HD Photo devuelve las dimensiones de imagen originales.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

HD Photo devuelve el formato de píxel de la imagen codificada.

### <a name="copypixels"></a>CopyPixels

HD Photo acepta cualquier región solicitada especificada por el parámetro [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) y devuelve esa parte de la imagen.

Los *parámetros uiWidth* *y uiHeight* deben especificar dimensiones devueltas por la [**función GetClosestSize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) Cualquier otro valor devuelve un error.

El *parámetro pguidDstFormat* debe especificar el formato de píxel devuelto por la [**función GetClosestPixelFormat.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) Cualquier otro valor devuelve un error.

HD Photo acepta cualquier valor permitido para el *parámetro dstTransform.* Tenga en cuenta que los valores permitidos por WIC para este parámetro son diferentes de los que usa HD Photo para la etiqueta de metadatos Transformation.

 

 
