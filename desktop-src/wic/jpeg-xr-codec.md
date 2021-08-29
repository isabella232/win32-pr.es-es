---
description: El códec JPEG XR nativo está disponible a través de Windows Imaging Component (WIC). El formato JPEG XR, compatible con el códec, está diseñado para la digitalización profesional y de consumidor.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Introducción al códec JPEG XR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb63bcc6764f01222bf9040d0dd727eb61a39f5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480751"
---
# <a name="jpeg-xr-codec-overview"></a>Introducción al códec JPEG XR

El códec JPEG XR nativo está disponible a través de Windows Imaging Component (WIC). El formato JPEG XR, compatible con el códec, está diseñado para la digitalización profesional y de consumidor.

El formato JPEG XR puede lograr hasta el doble de eficacia de compresión del formato JPEG original, con artefactos de compresión menos perceptibles. Las características de JPEG XR incluyen:

-   Compatibilidad con imágenes monocromáticas, RGB, MUTACIÓN y n canales
-   Formatos enteros de 8, 16 y 32 bits
-   Rango dinámico alto, formatos de gama ancha, con valores de color de punto fijo o punto flotante
-   Decoding progresiva
-   Codificación sin pérdida o pérdida de datos con el mismo algoritmo de compresión
-   Compatibilidad con la decodificación de regiones de interés en imágenes grandes

El formato JPEG XR se define en los siguientes documentos de estándar:

-   ITU-T T.832: Tecnología de la información– Sistema de codificación de imágenes *JPEG XR – Especificación de codificación de imágenes*
-   ISO/IEC 29199-2:2010: Tecnología de la información: sistema de codificación de imágenes *JPEG XR( Parte 2:* Especificación de codificación de imágenes

El estándar JPEG XR se basa en gran medida en el formato [HD Photo,](hdphoto-format-overview.md) pero hay algunas diferencias entre los dos formatos. En Windows 8, el códec HD Photo se ha actualizado para admitir JPEG XR. El codificador ahora siempre genera una secuencia de bits compatible con JPEG XR. El descodificador puede descodificar imágenes JPEG XR y HD Photo.

Se han realizado mejoras sustanciales de rendimiento en relación con el códec HD Photo en el códec JPEG XR. Por ejemplo, se ha mejorado la decodificación de imágenes de sub resolución, como la generación de miniaturas, así como lacoding de imágenes de baja resolución. Se recomienda usar el formato JPEG XR en lugar del formato HD Photo.

## <a name="codec-information"></a>Información del códec



|      Componente      |    Descripción                                                          |
|---------------------|-------------------------------------------------------------------------|
| Extensión de nombre de archivo | "jxr" y "wdp"                                                         |
| GUID de contenedor      | **GUID \_ ContainerFormatWmp**                                            |
| GUID del descodificador        | **CLSID \_ WICWmpDecoder**                                                |
| GUID del codificador        | **CLSID \_ WICWmpEncoder**                                                |
| Compatibilidad con perfiles     | El codificador y el descodificador admiten hasta el perfil principal y hasta el nivel 128. |



 

## <a name="codec-features"></a>Características del códec

### <a name="high-dynamic-range"></a>Alto rango dinámico

JPEG XR admite imágenes de rangos altamente dinámicos, mediante colores de punto flotante o de punto fijo. En estos formatos de color, el intervalo numérico de un píxel es mayor que el intervalo visible, por lo que puede ajustar los colores por encima o por debajo del intervalo visible durante las fases de procesamiento intermedias.

-   Punto fijo: en una representación de punto fijo, 0 representa el negro y 1,0 representa la saturación máxima. El códec JPEG XR admite formatos de punto fijo de 16 y 32 bits. Para 16 bits, 1,0 = 0x2000h, que proporciona 13 bits para el intervalo visible \[ 0...1 \] . El intervalo total es de -4,0 a +3,999 y se asigna linealmente. Para 32 bits, 1,0 = 0x01000000 h, el intervalo visible es de 24 bits y el intervalo total es de -128 a +127,999.
-   Punto flotante: en una representación de punto flotante, 0 representa el negro y 1,0 representa la saturación máxima. El códec JPEG XR admite formatos de punto flotante de 16 y 32 bits.

### <a name="tiles"></a>Iconos

Un marco se puede dividir en subregiones rectangulares *denominadas iconos*. Un icono es un área de una imagen que contiene matrices rectangulares de bloques de macros. Los iconos permiten descodificar las regiones de la imagen sin procesar toda la imagen.

Durante la codificación, seleccione el número de iconos estableciendo las propiedades **HorizontalTileSlices** y **VerticalTileSlices.** El tamaño mínimo del icono es de 16 × 16 píxeles. El codificador ajusta el número de iconos para mantener esta restricción. Hay una sobrecarga de almacenamiento y procesamiento asociada a cada icono, por lo que debe tener en cuenta el número de iconos necesarios para escenarios concretos.

### <a name="image-stream-output"></a>Salida del flujo de imagen

El estándar JPEG-XR define dos partes de un archivo JPEG-XR:

-   Secuencia de bits de imagen, definida en el cuerpo del estándar.
-   Contenedor de imágenes. El archivo contiene metadatos Exif y XMP, y se define en el anexo A del estándar.

Es posible, y lo permite el estándar, insertar el flujo de imagen dentro de otro tipo de contenedor de archivos. El codificador admite un modo de solo transmisión, que genera la secuencia de bits de imagen sin procesar sin contenedor de imágenes. Una aplicación puede almacenar el flujo de bits en algún otro formato de contenedor.

Para habilitar el modo de solo secuencia, establezca la **propiedad StreamOnly.**

### <a name="image-quality-settings"></a>Calidad de la imagen Configuración

Varias propiedades de códec controlan la calidad de la imagen de salida del codificador.

-   [ImageQuality es](#imagequality) una propiedad común entre códecs WIC. Especifica la calidad de la imagen como un valor de punto flotante único entre 0,0 y 1,0,
-   Las [propiedades Calidad,](#image-quality-settings) [Superposición](#overlap) [y Submuestreo](#subsampling) dan más control sobre la configuración de calidad.

Para usar las [propiedades Quality](#image-quality-settings), [Overlap](#overlap)y [Subsampling,](#subsampling) establezca la propiedad [UseCodecOptions](#usecodecoptions) en **VARIANT \_ TRUE.**

Si [UseCodecOptions](#usecodecoptions) es **VARIANT \_ FALSE** **(VARIANT \_ FALSE** es el valor predeterminado), el codificador usa la [propiedad ImageQuality.](#imagequality) El codificador asigna el valor de ImageQuality a [Quality](#image-quality-settings), [Overlap](#overlap)y [Subsampling](#subsampling) a través de una tabla de búsqueda.

El codificador no admite la **propiedad CompressionQuality.**

### <a name="compressed-domain-transcode"></a>Transcodificación de dominio comprimido

El códec JPEG XR puede realizar determinadas transformaciones de imagen sin realmente descodir los datos comprimidos y volver a codificar los datos. Las operaciones de dominio comprimido son muy eficaces y evitan cualquier pérdida de calidad adicional típica al descodificar y volver a codificar una imagen comprimida por pérdida.

Se admiten las siguientes operaciones de dominio comprimido:

-   Recortar una región de la imagen.
-   Girar o voltear la imagen.
-   Descarte los datos de frecuencia para crear un archivo de imagen más pequeño.
-   Reorganizar la imagen entre el orden espacial y el de frecuencia.

El codificador JPEG XR usa la transcodificación de dominios comprimidos, si es posible, cuando la imagen de origen es una imagen JPEG XR. Cuando el codificador realiza una operación de dominio comprimido, omite las siguientes propiedades de códec: [AlphaQuality,](#alphaquality) [ImageQuality,](#imagequality) [InterleavedAlpha,](#interleavedalpha) [Lossless](#lossless)[Overlap](#overlap)y [Quality](#image-quality-settings). Si las [propiedades HorizontalTileSlices](/windows) y [VerticalTileSlices están presentes,](/windows) debe establecerlas en cero. No se puede cambiar el tamaño del icono de una imagen como parte de una transcodificación de dominio comprimido.

En la lista siguiente se describe cómo realizar las transformaciones de imagen.

-   Para recortar la imagen, establezca la región deseada en el [**parámetro WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) del **método WriteSource.**
-   Para girar o voltear la imagen, establezca la [propiedad BitmapTransform.](#bitmaptransform)
-   Para descartar los datos de frecuencia de la imagen, establezca [la propiedad ImageDataDiscard.](#imagedatadiscard) Para descartar los datos de frecuencia en el canal alfa, establezca [la propiedad AlphaDataDiscard.](#alphadatadiscard) Si se descartan los datos de frecuencia, se reduce el tamaño del archivo codificado y se puede reducir la resolución.
-   Para cambiar la organización de la imagen entre la frecuencia y el orden espacial, establezca la [propiedad FrequencyOrdering.](/windows)

Para deshabilitar la transcodificación de dominio comprimido y forzar al codificador a volver a codificar la imagen, establezca [UseCodecOptions](#usecodecoptions) en **VARIANT \_ TRUE** y [establezca CompressedDomainTranscode](#compresseddomaintranscode) en **VARIANT \_ FALSE.**

## <a name="encoder-options"></a>Opciones del codificador

Para establecer las propiedades de codificación, use [**la interfaz IPropertyBag2.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) Para obtener más información, vea Información [general sobre codificación.](-wic-creating-encoder.md)

En la lista siguiente se especifican las opciones del codificador.

-   [AlphaDataDiscard](#alphadatadiscard)
-   [AlphaQuality](#alphaquality)
-   [BitmapTransform](#bitmaptransform)
-   [CompressedDomainTranscode](#compresseddomaintranscode)
-   [FrequencyOrder](#frequencyorder)
-   [HorizontalTileSlices](#horizontaltileslices)
-   [IgnoreOverlap](#ignoreoverlap)
-   [ImageDataDiscard](#imagedatadiscard)
-   [ImageQuality](#imagequality)
-   [InterleavedAlpha](#interleavedalpha)
-   [Lossless](#lossless)
-   [Traslapo](#overlap)
-   [ProgressiveMode](#progressivemode)
-   [Quality](#image-quality-settings)
-   [StreamOnly](#streamonly)
-   [Submuestreo](#subsampling)
-   [UseCodecOptions](#usecodecoptions)
-   [VerticalTileSlices](#verticaltileslices)

### <a name="alphadatadiscard"></a>AlphaDataDiscard

Establece la cantidad de datos de frecuencia alfa que se descartarán durante una transcodificación de dominio comprimido.



| Tipo de datos | VARTYPE     | Intervalo | Valor predeterminado |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0–4   | Ninguno    |



 

Esta propiedad solo se aplica si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode) está establecida en **VARIANT \_ TRUE** y la imagen contiene un canal alfa planar o un canal alfa intercalado; de lo contrario, se omite.

Para las imágenes que contienen un canal alfa planar, los valores siguientes son válidos.



| Valor | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | No se descartan datos de frecuencia de la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1     | Los flexbits se descartan. Esto reduce arbitrariamente la calidad del canal alfa planar para la imagen transcodificada. , sin un cambio en la resolución efectiva. La reducción exacta del tamaño y la calidad del archivo depende de numerosos factores y no se puede especificar exactamente.                                                                                                                                                                                           |
| 2     | Se descarta la banda de datos de frecuencia de paso alto, incluidos los flexbits. Esto reduce eficazmente la resolución del canal alfa planar en un factor de 4 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles de cada bloque 4x4 de píxeles de canal alfa. Normalmente, debe establecer este valor solo cuando la [propiedad ImageDataDiscard](#imagedatadiscard) tenga el mismo valor.                            |
| 3     | Se descartan las bandas de datos de frecuencia de paso alto y baja, incluidos los flexbits. Esto reduce ffectively la resolución del canal alfa planar en un factor de 16 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles de cada macrobloque de 16 x 16 píxeles de canal alfa. Normalmente, debe establecer este valor solo cuando la [propiedad ImageDataDiscard](#imagedatadiscard) tenga el mismo valor. |
| 4     | Se descarta totalmente el canal alfa. El formato de píxel de la imagen transcodificada se cambia para reflejar la eliminación del canal alfa.                                                                                                                                                                                                                                                                                                                                |



 

Para las imágenes que contienen un canal alfa intercalado, el siguiente valor es válido.



| Valor | Descripción                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 4     | Se descarta totalmente el canal alfa. El formato de píxel de la imagen transcodificada se cambia para reflejar la eliminación del canal alfa. |



 

Para alfa intercalado, a menos que esta propiedad se establezca en 4, el canal alfa se procesa igual que los datos de imagen, según el valor de la [propiedad ImageDataDiscard.](#imagedatadiscard)

### <a name="alphaquality"></a>AlphaQuality

Establece la calidad de compresión de la imagen de canal alfa planar.



| Tipo de datos | VARTYPE     | Intervalo | Valor predeterminado |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 1–255 | 1       |



 

Esta propiedad se aplica cuando la imagen tiene un canal alfa y la [propiedad InterleavedAlpha](#interleavedalpha) es **VARIANT \_ FALSE.** El valor 1 indica el modo sin pérdida de datos. Al aumentar los valores, se aumentan las relaciones de compresión y se reduce la calidad de la imagen.

### <a name="bitmaptransform"></a>BitmapTransform

Especifica si la imagen se gira o se volteo al descodificarse.



| Tipo de datos | VARTYPE     | Intervalo                                                                     | Valor predeterminado                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| **UCHAR** | **VT \_ UI1** | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | **WICBitmapTransformRotate0** |



 

### <a name="compresseddomaintranscode"></a>CompressedDomainTranscode

Habilita o deshabilita la transcodificación de dominios comprimidos.



| Tipo de datos         | VARTYPE      | Valor predeterminado           |
|-------------------|--------------|-------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ TRUE** |



 

Para deshabilitar las operaciones de dominio comprimido, establezca esta propiedad en **VARIANT \_ FALSE.**

### <a name="frequencyorder"></a>FrequencyOrder

Habilita la codificación en orden de frecuencia. Las implementaciones de dispositivos de codificadores JPEG XR pueden organizar un archivo en orden espacial para reducir la memoria necesaria durante la codificación.



| Tipo de datos         | VARTYPE      | Valor predeterminado           |
|-------------------|--------------|-------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ TRUE** |



 

-   **VARIANT \_ TRUE:** orden de frecuencia. Los datos de frecuencia más baja aparecen primero en el archivo y el contenido de la imagen se agrupa por su frecuencia en lugar de por su orientación espacial. La organización de un archivo por orden de frecuencia proporciona el mejor rendimiento para cualquier decodificación basada en frecuencia.
-   **VARIANT \_ FALSE:** orden espacial. El orden espacial reduce la memoria necesaria durante la codificación

Se recomienda el orden de frecuencia a menos que tenga motivos específicos del rendimiento o de la aplicación para usar el orden espacial.

### <a name="horizontaltileslices"></a>HorizontalTileSlices

Establece el número de iconos horizontales.



| Tipo de datos  | VARTYPE     | Intervalo  | Valor predeterminado                      |
|------------|-------------|--------|------------------------------|
| **USHORT** | **VT \_ UI2** | 0–4095 | (ancho de imagen – 1) >> 8 |



 

El valor es el número de subdivisiones horizontales; es decir, el número de mosaicos horizontales : 1.

### <a name="ignoreoverlap"></a>IgnoreOverlap

Especifica cómo el codificador controla los límites de mosaico durante una transcodificación de dominio comprimido.



| Tipo de datos         | VARTYPE      | Valor predeterminado            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 

Esta propiedad solo se aplica si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode) está establecida en **VARIANT \_ TRUE** y se realiza una transcodificación de subr regiones de exactamente uno o varios iconos.

La operación predeterminada para una transcodificación de región es expandir la región solicitada para incluir los píxeles circundantes necesarios para la descodificación superpuesta de los bordes de la región. Si esta propiedad se establece en **VARIANT \_ TRUE,** el códec omite los píxeles circundantes y solo se extraen los iconos o mosaicos seleccionados. Si la imagen de origen no está en mosaico o si la región solicitada incluye iconos parciales, se omite este parámetro.

### <a name="imagedatadiscard"></a>ImageDataDiscard

Establece la cantidad de datos de frecuencia de imagen que se descartarán durante una transcodificación de dominio comprimido.



| Tipo de datos | VARTYPE     | Intervalo | Valor predeterminado |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0–3   | 0       |



 

Esta propiedad solo se aplica si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode) está establecida en **VARIANT \_ TRUE;** de lo contrario, se omite.



| Valor | Descripción                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | No se descartan datos de frecuencia de la imagen.                                                                                                                                                                                                                                                                                                                                                                             |
| 1     | Los flexbits se descartan. Esto reduce arbitrariamente la calidad de la imagen transcodificada sin cambiar la resolución efectiva de la imagen. La reducción exacta del tamaño y la calidad del archivo depende de numerosos factores y no se puede especificar exactamente. Este valor devuelve un error especificado para un canal alfa intercalado.                                                                                |
| 2     | Se descarta la banda de datos de frecuencia de paso alto, incluidos los flexbits. Esto reduce la resolución de la imagen transcodificada en un factor de 4 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles de cada bloque de 4 x 4 píxeles. Por lo tanto, la imagen transcodificada se debe degradar en consecuencia cada vez que se descodifica.                             |
| 3     | Se descartan las bandas de datos de frecuencia de paso alto y baja, incluidos los flexbits. Esto reduce la resolución de la imagen transcodificada en un factor de 16 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles de cada macrobloque de 16 x 16 píxeles. Por lo tanto, la imagen transcodificada se debe degradar en consecuencia cada vez que se descodifica. |



 

Si la imagen contiene un canal alfa intercalado, el valor de [ImageDataDiscard](#imagedatadiscard) se aplica al canal alfa a menos que la propiedad [AlphaDataDiscard](#alphadatadiscard) esté establecida en 4, en cuyo caso se descarta el canal alfa.

Para alfa planar, los datos de frecuencia que se descartan se controlan mediante la [propiedad AlphaDataDiscard.](#alphadatadiscard)

### <a name="imagequality"></a>ImageQuality

Establece la calidad de la imagen.



| Tipo de datos | VARTYPE    | Intervalo | Valor predeterminado |
|-----------|------------|-------|---------|
| **FLOAT** | **VT \_ R4** | 0–1.0 | 0.9     |



 

El nivel 1.0 proporciona compresión matemáticamente sin pérdida.

El nivel 0.0 es la configuración de calidad más baja.

### <a name="interleavedalpha"></a>InterleavedAlpha

Especifica si se codifica alfa intercalado o alfa planar.



| Tipo de datos         | VARTYPE      | Valor predeterminado            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 

-   **VARIANT \_ TRUE:** alfa intercalado. La información del canal alfa se codifica como un canal intercalado adicional, sin correlación con los canales de contenido de la imagen. Este modo es útil para la decodificación alfa simultáneamente con la imagen cuando la imagen se transmite por secuencias.
-   VARIANT \_ FALSE: alfa planar. Un canal alfa planar se codifica como una imagen independiente. Los datos de imagen y el canal alfa se descodifican de forma independiente. Opcionalmente, puede establecer el nivel de calidad del canal alfa estableciendo la [propiedad AlphaQuality.](#alphaquality)

El alfa intercalado solo se admite para determinados formatos de píxel RGB. Se admite alfa planar para cualquier formato de imagen que defina un canal alfa.

### <a name="lossless"></a>Lossless

Habilita la compresión de pérdidas.



| Tipo de datos         | VARTYPE      | Valor predeterminado        |
|-------------------|--------------|----------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | VARIANT \_ FALSE |



 

Si el valor es **VARIANT \_ TRUE,** el codificador usa la compresión sin pérdida. Cuando se establece **en VARIANT \_ TRUE,** esta propiedad invalida la [propiedad ImageQuality.](#imagequality)

### <a name="overlap"></a>Superposición

Establece el nivel de filtrado superpuesto. Con el filtrado superpuesto, los coeficientes de transformación se aplican a través de los límites de bloque y macrobloqueo. Esto puede reducir los artefactos de bloqueo.



| Tipo de datos | VARTYPE     | Intervalo | Valor predeterminado |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0–4   | 1       |



 



| Valor | Descripción                                   |
|-------|-----------------------------------------------|
| 0     | Sin superposición.                                   |
| 1     | Un nivel de superposición, tiling suave. (Valor predeterminado). |
| 2     | Dos niveles de superposición, tiling suave.           |
| 3     | Un nivel de superposición, de tilings duros             |
| 4     | Dos niveles de superposición, de tilings duros.           |



 

Definiciones:

-   Un nivel de superposición: los valores codificados de los bloques 4x4 se modifican en función de los bloques vecinos.
-   Dos niveles de superposición: se aplica el primer nivel de superposición. Además, los valores codificados de los macrobloques de 16 x 16 se modifican en función de los bloques de macro vecinos.
-   Mosaicos flexibles: el filtrado de superposición se aplica a través de los límites de los mosaicos.
-   Mosaicos duros: el filtrado de superposición no se aplica a través de los límites de los mosaicos. Los iconos duros pueden introducir algunos artefactos visuales a lo largo de los límites de los iconos.

Si establece esta propiedad, establezca también [UseCodecOptions](#usecodecoptions) en **VARIANT \_ TRUE.**

### <a name="progressivemode"></a>ProgressiveMode

Habilita o deshabilita la codificación progresiva.



| Tipo de datos         | VARTYPE      | Valor predeterminado            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 



| Valor              | Descripción                |
|--------------------|----------------------------|
| **VARIANT \_ TRUE**  | Modo secuencial (valor predeterminado). |
| **VARIANT \_ FALSE** | Modo progresiva.          |



 

### <a name="quality"></a>Calidad

Establece la calidad de compresión.



| Tipo de datos | VARTYPE     | Intervalo | Valor predeterminado |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 1–255 | 1       |



 

El valor 1 indica el modo sin pérdida de datos. Al aumentar los valores, se aumentan las relaciones de compresión y se reduce la calidad de la imagen.

Si establece esta propiedad, establezca también [UseCodecOptions](#usecodecoptions) en **VARIANT \_ TRUE.**

### <a name="streamonly"></a>StreamOnly

Habilita o deshabilita el modo de solo secuencia.



| Tipo de datos         | VARTYPE      | Valor predeterminado            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 



| Valor              | Descripción                                                            |
|--------------------|------------------------------------------------------------------------|
| **VARIANT \_ TRUE**  | El codificador genera la secuencia de imagen sin procesar sin metadatos.             |
| **VARIANT \_ FALSE** | El codificador genera el formato de contenedor (flujo de imagen más metadatos). |



 

### <a name="subsampling"></a>Submuestreo

Establece el submuestreo de zona. Esta propiedad solo se aplica a las imágenes RGB.



| Tipo de datos | VARTYPE     | Intervalo | Valor predeterminado                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| **UCHAR** | **VT \_ UI1** | 0–3   | 3 si [ImageQuality](#imagequality) > 0.8; de lo contrario, 1 |



 




| Valor | Descripción | 
|-------|-------------|
| 3 | Codificación 4:4:4. Conserva la resolución completa de los conflictos. | 
| 2 | Codificación 4:2:2. La resolución de la luminosidad es de 1/2 de resolución de luminosidad. | 
| 1 | Codificación 4:2:0. La resolución de resoluciones es 1/4 de resolución de luminosidad. | 
| 0 | Codificación 4:0:0. Descarta todos los valores de los colores y solo conserva la luminosidad.<blockquote>[!Note]<br />No se recomienda este modo, ya que el códec usa una definición ligeramente modificada de luminosidad para mejorar el rendimiento. En su lugar, es mejor convertir la imagen en monocromática antes de codificar.</blockquote><br /> | 




 

4:2:2 y 4:2:0 conservan los detalles de luminosidad a costa de los detalles de color.

Si establece esta propiedad, establezca también [UseCodecOptions](#usecodecoptions) en **VARIANT \_ TRUE.**

### <a name="usecodecoptions"></a>UseCodecOptions

Especifica si se deben usar las propiedades [Quality](#image-quality-settings), [Overlap](#overlap)y [Subsampling](#subsampling) en lugar de la [propiedad ImageQuality](#imagequality) genérica.



| Tipo de datos         | VARTYPE      | Valor predeterminado            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 

### <a name="verticaltileslices"></a>VerticalTileSlices

Establece el número de iconos horizontales.



| Tipo de datos  | VARTYPE     | Intervalo  | Valor predeterminado                       |
|------------|-------------|--------|-------------------------------|
| **USHORT** | **VT \_ UI2** | 0–4095 | (altura de la imagen : 1) >> 8 |



 

El valor es el número de subdivisiones verticales; es decir, el número de mosaicos verticales : 1.

## <a name="supported-color-formats"></a>Formatos de color admitidos

Para obtener más información sobre estos formatos, vea [Formatos de píxeles nativos.](-wic-codec-native-pixel-formats.md)

-   **Formatos RGB enteros**
    -   GUID \_ WICPixelFormat24bppRGB
    -   GUID \_ WICPixelFormat24bppBGR
    -   GUID \_ WICPixelFormat32bppBGR
    -   GUID \_ WICPixelFormat48bppRGB
    -   GUID \_ WICPixelFormat32bppBGRA
    -   GUID \_ WICPixelFormat64bppRGBA
    -   GUID \_ WICPixelFormat32bppPBGRA
    -   GUID \_ WICPixelFormat64bppPRGBA
-   **Formatos RGB de punto fijo**
    -   GUID \_ WICPixelFormat48bppRGBFixedPoint
    -   GUID \_ WICPixelFormat64bppRGBFixedPoint
    -   GUID \_ WICPixelFormat96bppRGBFixedPoint
    -   GUID \_ WICPixelFormat128bppRGBFixedPoint
    -   GUID \_ WICPixelFormat128bppRGBAFixedPoint
-   **Formatos RGB de punto flotante**
    -   GUID \_ WICPixelFormat48bppRGBHalf
    -   GUID \_ WICPixelFormat64bppRGBHalf
    -   GUID \_ WICPixelFormat128bppRGBFloat
    -   GUID \_ WICPixelFormat64bppRGBAFixedPoint
    -   GUID \_ WICPixelFormat64bppRGBAHalf
    -   GUID \_ WICPixelFormat128bppRGBAFloat
    -   GUID \_ WICPixelFormat128bppPRGBAFloat
-   **Formatos de escala de grises**
    -   GUID \_ WICPixelFormat8bppGray
    -   GUID \_ WICPixelFormat16bppGray
    -   GUID \_ WICPixelFormat16bppGrayFixedPoint
    -   GUID \_ WICPixelFormat16bppGrayHalf
    -   GUID \_ WICPixelFormat32bppGrayFixedPoint
    -   GUID \_ WICPixelFormat32bppGrayFloat
-   **Formatos empaquetados**
    -   GUID \_ WICPixelFormat16bppBGR555
    -   GUID \_ WICPixelFormat16bppBGR565
    -   GUID \_ WICPixelFormat32bppBGR101010
    -   GUID \_ WICPixelFormat32bppRGBE
-   **Formatos FORMAT**
    -   GUID \_ WICPixelFormat40bppCIALAlpha
    -   GUID \_ WICPixelFormat64bppPIX
    -   GUID \_ WICPixelFormat80bppCIALAlpha
-   **Formatos de N canales**
    -   GUID \_ WICPixelFormat32bpp4Channels
    -   GUID \_ WICPixelFormat40bpp5Channels
    -   GUID \_ WICPixelFormat48bpp6Channels
    -   GUID \_ WICPixelFormat56bpp7Channels
    -   GUID \_ WICPixelFormat64bpp8Channels
    -   GUID \_ WICPixelFormat32bpp3ChannelsAlpha
    -   GUID \_ WICPixelFormat40bpp4ChannelsAlpha
    -   GUID \_ WICPixelFormat48bpp5ChannelsAlpha
    -   GUID \_ WICPixelFormat56bpp6ChannelsAlpha
    -   GUID \_ WICPixelFormat64bpp7ChannelsAlpha
    -   GUID \_ WICPixelFormat72bpp8ChannelsAlpha
    -   GUID \_ WICPixelFormat48bpp3Channels
    -   GUID \_ WICPixelFormat64bpp4Channels
    -   GUID \_ WICPixelFormat80bpp5Channels
    -   GUID \_ WICPixelFormat96bpp6Channels
    -   GUID \_ WICPixelFormat128bpp8Channels
    -   GUID \_ WICPixelFormat64bpp3ChannelsAlpha
    -   GUID \_ WICPixelFormat80bpp4ChannelsAlpha
    -   GUID \_ WICPixelFormat96bpp5ChannelsAlpha
    -   GUID \_ WICPixelFormat112bpp6ChannelsAlpha
    -   GUID \_ WICPixelFormat128bpp7ChannelsAlpha
    -   GUID \_ WICPixelFormat144bpp8ChannelsAlpha

 

 
