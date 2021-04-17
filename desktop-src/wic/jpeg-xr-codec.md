---
description: El códec nativo JPEG XR está disponible a través de Windows Imaging Component (WIC). El formato JPEG XR, que el códec admite, está diseñado para la fotografía digital del consumidor y del profesional.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Información general sobre el códec JPEG XR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706877"
---
# <a name="jpeg-xr-codec-overview"></a>Información general sobre el códec JPEG XR

El códec nativo JPEG XR está disponible a través de Windows Imaging Component (WIC). El formato JPEG XR, que el códec admite, está diseñado para la fotografía digital del consumidor y del profesional.

El formato JPEG XR puede lograr hasta dos veces la eficiencia de compresión del formato JPEG original, con artefactos de compresión menos perceptibles. Las características de JPEG XR incluyen:

-   Compatibilidad con imágenes monocromáticas, RGB, CMYK y n-Channel
-   formatos enteros de 8, 16 y 32 bits
-   Alta gama dinámica, formatos anchos, con valores de color de punto fijo o punto flotante
-   Descodificación progresiva
-   Codificación con pérdida o sin pérdida mediante el mismo algoritmo de compresión
-   Compatibilidad con la descodificación de regiones de interés en imágenes de gran tamaño

El formato JPEG XR se define en los siguientes documentos de estándares:

-   ITU-T T. 832: *tecnología de la información: JPEG XR Image Coding System – Image codificación Specification*
-   ISO/IEC 29199-2:2010: *tecnología de la información: sistema de codificación de imágenes JPEG XR, parte 2: especificación de codificación de imágenes*

El estándar JPEG XR se basa en gran medida en el formato de [fotografía HD](hdphoto-format-overview.md) , pero hay algunas diferencias entre los dos formatos. En Windows 8, el códec HD Photo se ha actualizado para que sea compatible con JPEG XR. El codificador ahora siempre genera un flujo de bits compatible con JPEG XR. El descodificador puede descodificar imágenes JPEG XR y HD.

Se han realizado mejoras sustanciales en el rendimiento, en relación con el códec HD Photo, en el códec JPEG XR. Por ejemplo, se ha mejorado la descodificación de imágenes de subresolución, como la generación de miniaturas, así como la descodificación de imágenes de baja resolución. Se recomienda usar el formato JPEG XR en lugar del formato HD Photo.

## <a name="codec-information"></a>Información del códec



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| Extensión de nombre de archivo | "jxr" y "WDP"                                                         |
| GUID de contenedor      | **GUID \_ ContainerFormatWmp**                                            |
| GUID del descodificador        | **CLSID \_ WICWmpDecoder**                                                |
| GUID del codificador        | **CLSID \_ WICWmpEncoder**                                                |
| Compatibilidad con perfiles     | El codificador y el descodificador admiten hasta el perfil principal y hasta el nivel 128. |



 

## <a name="codec-features"></a>Características del códec

### <a name="high-dynamic-range"></a>Alto rango dinámico

JPEG XR admite imágenes de rangos más dinámicas, mediante el uso de colores de punto flotante o de punto fijo. En estos formatos de color, el intervalo numérico de un píxel es mayor que el intervalo visible, de modo que puede ajustar los colores por encima o por debajo del rango visible durante las fases de procesamiento intermedios.

-   Punto fijo: en una representación de punto fijo, 0 representa el negro y 1,0 representa la saturación máxima. El códec JPEG XR admite formatos de punto fijo de 16 y 32 bits. Para 16 bits, 1,0 = 0x2000h, que proporciona 13 bits para el intervalo visible \[ 0... 1 \] . El intervalo total es de – 4,0 a + 3,999 y se asigna linealmente. Para 32 bits, 1,0 = 0x01000000h, el intervalo visible es de 24 bits y el intervalo total es – 128 a + 127,999.
-   Punto flotante: en una representación de punto flotante, 0 representa el negro y 1,0 representa la saturación máxima. El códec JPEG XR es compatible con los formatos de punto flotante de 16 y 32 bits.

### <a name="tiles"></a>Iconos

Un marco se puede particionar en subregiones rectangulares denominadas *mosaicos*. Un icono es un área de una imagen que contiene matrices rectangulares de macrobloques. Los mosaicos permiten descodificar las regiones de la imagen sin procesar toda la imagen.

Durante la codificación, seleccione el número de mosaicos mediante el establecimiento de las propiedades **HorizontalTileSlices** y **VerticalTileSlices** . El tamaño mínimo del mosaico es de 16 × 16 píxeles. El codificador ajusta el número de mosaicos para mantener esta restricción. Hay una sobrecarga de almacenamiento y procesamiento asociada a cada mosaico, por lo que debe tener en cuenta el número de mosaicos necesarios para determinados escenarios.

### <a name="image-stream-output"></a>Salida de flujo de imagen

El estándar JPEG-XR define dos partes de un archivo JPEG-XR:

-   Flujo de bits de imagen, definido en el cuerpo del estándar.
-   Contenedor de la imagen. El archivo contiene metadatos Exif y XMP, y se define en el anexo A del estándar.

Es posible, y permitido por el estándar, incrustar el flujo de imágenes dentro de otro tipo de contenedor de archivos. El codificador admite un modo de solo transmisión, que genera la secuencia de bits de imagen sin procesar sin contenedor de imágenes. Una aplicación puede almacenar el flujo de bits en otro formato de contenedor.

Para habilitar el modo de solo transmisión, establezca la propiedad **StreamOnly** .

### <a name="image-quality-settings"></a>Configuración de calidad de imagen

Varias propiedades de códec controlan la calidad de la imagen de salida del codificador.

-   [ImageQuality](#imagequality) es una propiedad común a través de los códecs WIC. Especifica la calidad de la imagen como un valor de punto flotante único entre 0,0 y 1,0.
-   Las propiedades [calidad](#image-quality-settings), [superposición](#overlap)y [submuestreo](#subsampling) proporcionan más control sobre la configuración de calidad.

Para usar las propiedades [calidad](#image-quality-settings), [superposición](#overlap)y [submuestreo](#subsampling) , establezca la propiedad [UseCodecOptions](#usecodecoptions) en **Variant \_ true**.

Si [UseCodecOptions](#usecodecoptions) es **Variant \_ false** (**Variant \_ false** es el valor predeterminado), el codificador utiliza la propiedad [ImageQuality](#imagequality) . El codificador asigna el valor de ImageQuality a la [calidad](#image-quality-settings), la [superposición](#overlap)y el [submuestreo](#subsampling) a través de una tabla de búsqueda.

El codificador no admite la propiedad **CompressionQuality** .

### <a name="compressed-domain-transcode"></a>Transcodificación de dominios comprimidos

El códec JPEG XR puede realizar ciertas transformaciones de imágenes sin descodificar realmente los datos comprimidos y volver a codificarlos. Las operaciones de dominio comprimido son muy eficaces y evitan cualquier pérdida de calidad adicional que sea habitual al descodificar y volver a codificar una imagen comprimida con pérdida.

Se admiten las siguientes operaciones de dominio comprimido:

-   Recortar una región de la imagen.
-   Girar o voltear la imagen.
-   Descarte los datos de frecuencia para crear un archivo de imagen más pequeño.
-   Reorganice la imagen entre el orden espacial y el orden de las frecuencias.

El codificador de JPEG XR usa la transcodificación de dominios comprimidos, si es posible, cuando la imagen de origen es una imagen de JPEG XR. Cuando el codificador realiza una operación de dominio comprimido, omite las siguientes propiedades de códec: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha),[superposición](#overlap)sin [pérdida](#lossless)y [calidad](#image-quality-settings). Si las propiedades [HorizontalTileSlices](/windows) y [VerticalTileSlices](/windows) están presentes, debe establecerlas en cero. No se puede cambiar el tamaño de mosaico de una imagen como parte de un transcodificación de dominios comprimidos.

En la lista siguiente se describe cómo realizar las transformaciones de imagen.

-   Para recortar la imagen, establezca la región deseada en el parámetro [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) del método **WriteSource** .
-   Para girar o voltear la imagen, establezca la propiedad [BitmapTransform](#bitmaptransform) .
-   Para descartar los datos de frecuencia de la imagen, establezca la propiedad [ImageDataDiscard](#imagedatadiscard) . Para descartar los datos de frecuencia en el canal alfa, establezca la propiedad [AlphaDataDiscard](#alphadatadiscard) . Descartar los datos de frecuencia reduce el tamaño del archivo codificado y puede reducir la resolución.
-   Para cambiar la organización de la imagen entre la frecuencia y la ordenación espacial, establezca la propiedad [FrequencyOrdering](/windows) .

Para deshabilitar el transcodificación de dominios comprimidos y forzar que el codificador vuelva a codificar la imagen, establezca [UseCodecOptions](#usecodecoptions) en **Variant \_ true** y establezca [CompressedDomainTranscode](#compresseddomaintranscode) en **Variant \_ false**.

## <a name="encoder-options"></a>Opciones del codificador

Para establecer las propiedades de codificación, use la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información, vea [información general sobre la codificación](-wic-creating-encoder.md).

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
-   [Superpone](#overlap)
-   [ProgressiveMode](#progressivemode)
-   [Quality](#image-quality-settings)
-   [StreamOnly](#streamonly)
-   [Un submuestreo](#subsampling)
-   [UseCodecOptions](#usecodecoptions)
-   [VerticalTileSlices](#verticaltileslices)

### <a name="alphadatadiscard"></a>AlphaDataDiscard

Establece la cantidad de datos de frecuencia alfa que se va a descartar durante la transcodificación de un dominio comprimido.



| Tipo de datos | VARTYPE     | Intervalo | Valor predeterminado |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | de 0 a 4   | None    |



 

Esta propiedad solo se aplica si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode) está establecida en **Variant \_ true** y la imagen contiene un canal alfa plano o un canal alfa intercalado; de lo contrario, se omite.

En el caso de las imágenes que contienen un canal alfa plano, los valores siguientes son válidos.



| Value | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | No se descartan datos de frecuencia de la imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1     | Se descartan los flexbits. Esto reduce arbitrariamente la calidad del canal alfa plano para la imagen transcodificada. , sin un cambio en la resolución efectiva. La reducción exacta del tamaño y la calidad de los archivos depende de numerosos factores y no se puede especificar exactamente.                                                                                                                                                                                           |
| 2     | La banda de datos de frecuencia de paso alto se descarta, incluido el flexbits. Esto reduce eficazmente la resolución del canal alfa plano en un factor de 4 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles en cada bloque 4x4 de píxeles de canal alfa. Normalmente, solo debe establecer este valor cuando la propiedad [ImageDataDiscard](#imagedatadiscard) tiene el mismo valor.                            |
| 3     | Se descartan las bandas de datos de frecuencia alta y de baja pasada, incluido el flexbits. Este ffectively reduce la resolución del canal alfa plano en un factor de 16 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles en cada adaptativo macrobloque de 16x16 de píxeles de canal alfa. Normalmente, solo debe establecer este valor cuando la propiedad [ImageDataDiscard](#imagedatadiscard) tiene el mismo valor. |
| 4     | Se descarta totalmente el canal alfa. El formato de píxel de la imagen transcodificada se cambia para reflejar la eliminación del canal alfa.                                                                                                                                                                                                                                                                                                                                |



 

En el caso de las imágenes que contienen un canal alfa intercalado, el valor siguiente es válido.



| Value | Descripción                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 4     | Se descarta totalmente el canal alfa. El formato de píxel de la imagen transcodificada se cambia para reflejar la eliminación del canal alfa. |



 

En el caso de alfa intercalado, a menos que esta propiedad esté establecida en 4, el canal alfa se procesa igual que los datos de la imagen, de acuerdo con el valor de la propiedad [ImageDataDiscard](#imagedatadiscard) .

### <a name="alphaquality"></a>AlphaQuality

Establece la calidad de compresión para la imagen del canal alfa plana.



| Tipo de datos | VARTYPE     | Intervalo | Valor predeterminado |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | de 1 a 255 | 1       |



 

Esta propiedad se aplica cuando la imagen tiene un canal alfa y la propiedad [InterleavedAlpha](#interleavedalpha) es una **variante \_ falsa**. El valor 1 indica el modo sin pérdida. Aumentar los valores produce mayores proporciones de compresión y una calidad de imagen inferior.

### <a name="bitmaptransform"></a>BitmapTransform

Especifica si la imagen se gira o voltea al descodificar.



| Tipo de datos | VARTYPE     | Intervalo                                                                     | Valor predeterminado                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| **UCHAR** | **VT \_ UI1** | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | **WICBitmapTransformRotate0** |



 

### <a name="compresseddomaintranscode"></a>CompressedDomainTranscode

Habilita o deshabilita la transcodificación de dominios comprimidos.



| Tipo de datos         | VARTYPE      | Valor predeterminado           |
|-------------------|--------------|-------------------|
| **VARIANTE \_ bool** | **VT \_ bool** | **VARIANTE \_ true** |



 

Para deshabilitar las operaciones de dominio comprimido, establezca esta propiedad en **Variant \_ false**.

### <a name="frequencyorder"></a>FrequencyOrder

Habilita la codificación en orden de frecuencia. Las implementaciones de dispositivos de los codificadores JPEG XR pueden organizar un archivo en orden espacial para reducir la memoria necesaria durante la codificación.



| Tipo de datos         | VARTYPE      | Valor predeterminado           |
|-------------------|--------------|-------------------|
| **VARIANTE \_ bool** | **VT \_ bool** | **VARIANTE \_ true** |



 

-   **Variante \_ TRUE**: orden de la frecuencia. Los datos de la frecuencia más baja aparecen en primer lugar en el archivo y el contenido de la imagen se agrupa por su frecuencia en lugar de su orientación espacial. La organización de un archivo por orden de frecuencia proporciona el mejor rendimiento para cualquier descodificación basada en frecuencias.
-   **Variante \_ FALSE**: orden espacial. El orden espacial reduce la memoria necesaria durante la codificación

Se recomienda el orden de las frecuencias a menos que tenga razones de rendimiento o específicas de la aplicación para usar el orden espacial.

### <a name="horizontaltileslices"></a>HorizontalTileSlices

Establece el número de mosaicos horizontales.



| Tipo de datos  | VARTYPE     | Intervalo  | Valor predeterminado                      |
|------------|-------------|--------|------------------------------|
| **USHORT** | **VT \_ UI2** | 0 – 4095 | (ancho de imagen – 1)  >> 8 |



 

El valor es el número de subdivisiones horizontales; es decir, el número de mosaicos horizontales: 1.

### <a name="ignoreoverlap"></a>IgnoreOverlap

Especifica cómo el codificador controla los límites del mosaico durante la transcodificación de un dominio comprimido.



| Tipo de datos         | VARTYPE      | Valor predeterminado            |
|-------------------|--------------|--------------------|
| **VARIANTE \_ bool** | **VT \_ bool** | **VARIANTE \_ false** |



 

Esta propiedad solo se aplica si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode) se establece en **Variant \_ true** y se realiza una subcodificación de una subregión de exactamente uno o más mosaicos.

La operación predeterminada para una región Transcode es expandir la región solicitada para incluir los píxeles circundantes necesarios para la descodificación de superposiciones de los bordes de la región. Si esta propiedad se establece en **Variant \_ true**, el códec omite los píxeles circundantes y solo se extraen el mosaico o los mosaicos seleccionados. Si la imagen de origen no está en mosaico o si la región solicitada incluye mosaicos parciales, se omite este parámetro.

### <a name="imagedatadiscard"></a>ImageDataDiscard

Establece la cantidad de datos de frecuencia de la imagen que se van a descartar durante una transcodificación de dominio comprimido.



| Tipo de datos | VARTYPE     | Intervalo | Valor predeterminado |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0 – 3   | 0       |



 

Esta propiedad solo se aplica si la propiedad [CompressedDomainTranscode](#compresseddomaintranscode) está establecida en **Variant \_ true**; en caso contrario, se omite.



| Value | Descripción                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | No se descartan datos de frecuencia de la imagen.                                                                                                                                                                                                                                                                                                                                                                             |
| 1     | Se descartan los flexbits. Esto reduce arbitrariamente la calidad de la imagen transcodificada sin cambiar la resolución efectiva de la imagen. La reducción exacta del tamaño y la calidad de los archivos depende de numerosos factores y no se puede especificar exactamente. Este valor devuelve un error especificado para un canal alfa intercalado.                                                                                |
| 2     | La banda de datos de frecuencia de paso alto se descarta, incluido el flexbits. Esto reduce la resolución de la imagen transcodificada en un factor de 4 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles en cada bloque 4x4 de píxeles. Por lo tanto, la imagen transcodificada debe downsampledse en consecuencia cada vez que se descodifica.                             |
| 3     | Se descartan las bandas de datos de frecuencia alta y de baja pasada, incluido el flexbits. Esto reduce la resolución de la imagen transcodificada en un factor de 16 en ambas dimensiones. Las dimensiones reales de la imagen transcodificada siguen siendo las mismas, pero la imagen pierde todos los detalles en cada adaptativo macrobloque de 16x16 de píxeles. Por lo tanto, la imagen transcodificada debe downsampledse en consecuencia cada vez que se descodifica. |



 

Si la imagen contiene un canal alfa intercalado, el valor de [ImageDataDiscard](#imagedatadiscard) se aplica al canal alfa a menos que la propiedad [AlphaDataDiscard](#alphadatadiscard) esté establecida en 4, en cuyo caso se descarta el canal alfa.

En el caso del alfa plano, los datos de frecuencia que se descartan se controlan mediante la propiedad [AlphaDataDiscard](#alphadatadiscard) .

### <a name="imagequality"></a>ImageQuality

Establece la calidad de la imagen.



| Tipo de datos | VARTYPE    | Intervalo | Valor predeterminado |
|-----------|------------|-------|---------|
| **FLOAT** | **VT \_ R4** | 0 – 1,0 | 0.9     |



 

El nivel 1,0 proporciona una compresión matemática sin pérdida de los mismos.

El nivel 0,0 es el valor de la calidad más baja.

### <a name="interleavedalpha"></a>InterleavedAlpha

Especifica si se va a codificar un alfa plano o alfa intercalado.



| Tipo de datos         | VARTYPE      | Valor predeterminado            |
|-------------------|--------------|--------------------|
| **VARIANTE \_ bool** | **VT \_ bool** | **VARIANTE \_ false** |



 

-   **Variante \_ TRUE**: alfa intercalado. La información del canal alfa se codifica como un canal intercalado adicional, sin correlación con los canales de contenido de la imagen. Este modo es útil para descodificar alfa simultáneamente con la imagen cuando la imagen se transmite por secuencias.
-   VARIANT \_ false: alfa plana. Un canal alfa plano se codifica como una imagen independiente. Los datos de la imagen y el canal alfa se descodifican de forma independiente. Opcionalmente, puede establecer el nivel de calidad del canal alfa estableciendo la propiedad [AlphaQuality](#alphaquality) .

El alfa intercalado solo se admite para determinados formatos de píxeles RGB. El alfa plano es compatible con cualquier formato de imagen que defina un canal alfa.

### <a name="lossless"></a>Lossless

Habilita la compresión de pérdidas.



| Tipo de datos         | VARTYPE      | Valor predeterminado        |
|-------------------|--------------|----------------|
| **VARIANTE \_ bool** | **VT \_ bool** | VARIANTE \_ false |



 

Si el valor es **Variant \_ true**, el codificador utiliza la compresión sin pérdida de datos. Cuando se establece en **Variant \_ true**, esta propiedad invalida la propiedad [ImageQuality](#imagequality) .

### <a name="overlap"></a>Superposición

Establece el nivel de filtrado de superposición. Con el filtrado de superposición, los coeficientes de transformación se aplican en los límites de bloque y adaptativo macrobloque. Esto puede reducir los artefactos de bloqueo.



| Tipo de datos | VARTYPE     | Intervalo | Valor predeterminado |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | de 0 a 4   | 1       |



 



| Value | Descripción                                   |
|-------|-----------------------------------------------|
| 0     | No superponerse.                                   |
| 1     | Un nivel de superposición, mosaico flexible. (Valor predeterminado). |
| 2     | Dos niveles de superposición, mosaico flexible.           |
| 3     | Un nivel de superposición, mosaico fuerte             |
| 4     | Dos niveles de superposición, mosaico fuerte.           |



 

Definiciones:

-   Un nivel de superposición: los valores codificados de los bloques 4x4 se modifican en función de los bloques vecinos.
-   Dos niveles de superposición: se aplica el primer nivel de superposición. Además, los valores codificados de 16x16 macrobloques se modifican en función de la macrobloques vecina.
-   Mosaico flexible: el filtrado de superposición se aplica a través de los límites del mosaico.
-   Mosaico fuerte: el filtrado de superposición no se aplica a través de los límites del mosaico. Los mosaicos fuertes pueden introducir algunos artefactos visuales a lo largo de los límites del mosaico.

Si establece esta propiedad, establezca también [UseCodecOptions](#usecodecoptions) en **Variant \_ true**.

### <a name="progressivemode"></a>ProgressiveMode

Habilita o deshabilita la codificación progresiva.



| Tipo de datos         | VARTYPE      | Valor predeterminado            |
|-------------------|--------------|--------------------|
| **VARIANTE \_ bool** | **VT \_ bool** | **VARIANTE \_ false** |



 



| Value              | Descripción                |
|--------------------|----------------------------|
| **VARIANTE \_ true**  | Modo secuencial (valor predeterminado). |
| **VARIANTE \_ false** | Modo progresivo.          |



 

### <a name="quality"></a>Calidad

Establece la calidad de compresión.



| Tipo de datos | VARTYPE     | Intervalo | Valor predeterminado |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | de 1 a 255 | 1       |



 

El valor 1 indica el modo sin pérdida. Aumentar los valores produce mayores proporciones de compresión y una calidad de imagen inferior.

Si establece esta propiedad, establezca también [UseCodecOptions](#usecodecoptions) en **Variant \_ true**.

### <a name="streamonly"></a>StreamOnly

Habilita o deshabilita el modo de solo transmisión por secuencias.



| Tipo de datos         | VARTYPE      | Valor predeterminado            |
|-------------------|--------------|--------------------|
| **VARIANTE \_ bool** | **VT \_ bool** | **VARIANTE \_ false** |



 



| Value              | Descripción                                                            |
|--------------------|------------------------------------------------------------------------|
| **VARIANTE \_ true**  | El codificador genera el flujo de imágenes sin formato sin metadatos.             |
| **VARIANTE \_ false** | El codificador genera el formato de contenedor (flujo de imagen más metadatos). |



 

### <a name="subsampling"></a>Un submuestreo

Establece el submuestreo de croma. Esta propiedad solo se aplica a las imágenes RGB.



| Tipo de datos | VARTYPE     | Intervalo | Valor predeterminado                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| **UCHAR** | **VT \_ UI1** | 0 – 3   | 3 Si [ImageQuality](#imagequality) > 0,8; de lo contrario 1 |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3</td>
<td>codificación 4:4:4. Conserva la resolución de croma completa.</td>
</tr>
<tr class="even">
<td>2</td>
<td>codificación 4:2:2. La resolución de croma es 1/2 de la resolución de luminancia.</td>
</tr>
<tr class="odd">
<td>1</td>
<td>codificación 4:2:0. La resolución de croma es 1/4 de la resolución de luminancia.</td>
</tr>
<tr class="even">
<td>0</td>
<td>Codificación 4:0:0. Descarta todos los valores de croma y conserva solo la luminancia.
<blockquote>
[!Note]<br />
No se recomienda este modo, ya que el códec utiliza una definición ligeramente modificada de luminancia para mejorar el rendimiento. En su lugar, es mejor convertir la imagen en monocromo antes de la codificación.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

4:2:2 y 4:2:0 conservar el detalle de luminancia a costa de los detalles de color.

Si establece esta propiedad, establezca también [UseCodecOptions](#usecodecoptions) en **Variant \_ true**.

### <a name="usecodecoptions"></a>UseCodecOptions

Especifica si se deben usar las propiedades de [calidad](#image-quality-settings), [superposición](#overlap)y [submuestreo](#subsampling) en lugar de la propiedad [ImageQuality](#imagequality) genérica.



| Tipo de datos         | VARTYPE      | Valor predeterminado            |
|-------------------|--------------|--------------------|
| **VARIANTE \_ bool** | **VT \_ bool** | **VARIANTE \_ false** |



 

### <a name="verticaltileslices"></a>VerticalTileSlices

Establece el número de mosaicos horizontales.



| Tipo de datos  | VARTYPE     | Intervalo  | Valor predeterminado                       |
|------------|-------------|--------|-------------------------------|
| **USHORT** | **VT \_ UI2** | 0 – 4095 | (alto de imagen – 1)  >> 8 |



 

El valor es el número de subdivisiones verticales; es decir, el número de mosaicos verticales-1.

## <a name="supported-color-formats"></a>Formatos de color admitidos

Para obtener más información sobre estos formatos, vea [formatos de píxeles nativos](-wic-codec-native-pixel-formats.md).

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
-   **Formatos CMYK**
    -   GUID \_ WICPixelFormat40bppCMYKAlpha
    -   GUID \_ WICPixelFormat64bppCMYK
    -   GUID \_ WICPixelFormat80bppCMYKAlpha
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

 

 
