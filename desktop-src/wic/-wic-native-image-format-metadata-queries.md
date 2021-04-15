---
description: En este tema se proporciona información general sobre las consultas del lenguaje de consulta de metadatos para leer y escribir metadatos compatibles con imágenes GIF, PNG, TIFF y JPEG.
ms.assetid: a6ab1708-dd82-4960-b908-f1daef7374ef
title: Consultas de metadatos de formato de imagen nativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be5e9c0f853e4c5e48fb5eb41f2d2ab27b4f4d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648571"
---
# <a name="native-image-format-metadata-queries"></a>Consultas de metadatos de formato de imagen nativo

En este tema se proporciona información general sobre las consultas del [lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md) para leer y escribir metadatos compatibles con imágenes GIF, PNG, TIFF y JPEG. Incluye metadatos específicos de cada formato de imagen, así como metadatos que se admiten en varios formatos.

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Expresión de directiva de metadatos de fotos](#photo-metadata-policy-expression)
-   [Metadatos específicos de formato de archivo](#file-format-specific-metadata)
    -   [Metadatos GIF](#gif-metadata)
    -   [Metadatos PNG](#png-metadata)
    -   [Metadatos TIFF](#tiff-metadata)
    -   [Metadatos JPEG](#jpeg-metadata)
-   [Metadatos independientes del formato de archivo](#file-format-independent-metadata)
    -   [Metadatos de IFD](#ifd-metadata)
    -   [Metadatos EXIF](#exif-metadata)
    -   [Metadatos de GPS](#gps-metadata)
    -   [Metadatos XMP](#xmp-metadata)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

Para entender este tema, debe estar familiarizado con el sistema de metadatos de Windows Imaging Component (WIC) tal y como se describe en [información general sobre metadatos de WIC](-wic-about-metadata.md). También debe estar familiarizado con el lenguaje de consulta que se usa para leer y escribir metadatos, como se describe en [información general sobre el lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md).

## <a name="photo-metadata-policy-expression"></a>Expresión de directiva de metadatos de fotos

Además de admitir el lenguaje de consulta de metadatos, [WIC](-wic-api.md) también acepta nombres de propiedad canónicos del [sistema de propiedades de Windows](../properties/windows-properties-system.md). WIC admite un subconjunto del espacio de nombres de propiedades de Windows que es relevante para los formatos de imagen, como se describe en [directivas de metadatos de fotos](photo-metadata-policies.md). Una propiedad de Windows que se usa como una consulta de metadatos de WIC se conoce como expresión de directiva de metadatos de fotos.

Por ejemplo, la expresión de la Directiva de metadatos de fotos para la marca de orientación EXIF es:

-   [System. Photo. Orientation](-wic-photoprop-system-photo-orientation.md)

En general, se recomiendan las expresiones de Directiva sobre las consultas de metadatos nativas para los elementos de metadatos de imagen comunes que están incluidos en el espacio de nombres de la propiedad de Windows. El lenguaje de consulta de metadatos es más adecuado para los casos en los que se necesita acceso de bajo nivel a elementos de metadatos de imagen específicos, o para elementos de metadatos personalizados o avanzados que no son compatibles con el sistema de propiedades de Windows. Para obtener más información, vea [expresiones de directivas de metadatos de fotos](-wic-codec-metadataquerylanguage.md).

## <a name="file-format-specific-metadata"></a>Metadatos específicos de formato de archivo

Las secciones siguientes contienen tablas que enumeran las consultas de metadatos disponibles para cada tipo de archivo de imagen. Cada tabla tiene las columnas siguientes:

-   **Ruta** de acceso: la ruta de la consulta que se usa para recuperar el elemento de metadatos.
-   **Name** : el nombre del elemento de metadatos.
-   **Type** : el tipo de elemento de metadatos recuperado de la ruta de acceso de la consulta. Los metadatos recuperados por [WIC](-wic-api.md) se devuelven en forma de PROPVARIANT, que notifica el tipo de datos mediante la enumeración VARTYPE. on.

La API de metadatos de WIC usa las rutas de consulta para tener acceso a los metadatos incrustados de una imagen. En el ejemplo de código siguiente se muestra cómo usar un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) para consultar el bloque de metadatos IFD de JPEG.


```
// Not shown: image decoding 
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pIFDReader = NULL;

// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

if (SUCCEEDED(hr))
{
    // Get the nested IFD reader.
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pIFDReader);
    }
    PropVariantClear(&value); // Clear value for new query.
}
```



### <a name="gif-metadata"></a>Metadatos GIF

El formato de imagen de formato de intercambio de gráficos (GIF) admite metadatos globales y de nivel de marco. En las dos secciones siguientes se proporcionan las rutas de acceso de consulta de metadatos disponibles para los metadatos globales y de nivel de marco de GIF.

> [!Note]  
> Para obtener una lista completa de metadatos GIF junto con información más detallada, consulte el [estándar GIF](https://www.w3.org/Graphics/GIF/spec-gif89a.txt) en el sitio web de W3C.

 

### <a name="global-metadata"></a>Metadatos globales

En la tabla siguiente se proporcionan las rutas de consulta de metadatos disponibles que se pueden utilizar para tener acceso a los metadatos GIF globales.



| Ruta                                               | Nombre                       | Tipo                                |
|----------------------------------------------------|----------------------------|-------------------------------------|
| /commentext o/ \[ \* \] commentext donde \* = 0 a N | Extensión de comentarios          | VT \_ desconocido: lector/escritor de consultas |
| /commentext/TextEntry                              |                            | VT \_ LPSTR                           |
| /logscrdesc                                        | Descripción de la pantalla lógica | VT \_ desconocido: lector/escritor de consultas |
| /logscrdesc/Signature                              |                            | \_Vector VT UI1 \| VT \_               |
| /logscrdesc/Width                                  |                            | VT \_ UI2                             |
| /logscrdesc/Height                                 |                            | VT \_ UI2                             |
| /logscrdesc/GlobalColorTableFlag                   |                            | VT \_ bool                            |
| /logscrdesc/ColorResolution                        |                            | VT \_ UI1                             |
| /logscrdesc/SortFlag                               |                            | VT \_ bool                            |
| /logscrdesc/GlobalColorTableSize                   |                            | VT \_ UI1                             |
| /logscrdesc/BackgroundColorIndex                   |                            | VT \_ UI1                             |
| /logscrdesc/PixelAspectRatio                       |                            | VT \_ UI1                             |
| /appext o/ \[ \* \] appext donde \* = 0 a N         | Extensión de aplicación      | VT \_ desconocido: lector/escritor de consultas |
| /appext/Application                                |                            | \_Vector VT UI1 \| VT \_               |
| /appext/Data                                       |                            | \_Vector VT UI1 \| VT \_               |



 

### <a name="frame-metadata"></a>Metadatos de marco

En la tabla siguiente se proporcionan las rutas de consulta de metadatos disponibles que se pueden usar para tener acceso a los metadatos GIF de nivel de marco.



| Ruta                            | Nombre                      | Tipo                              |
|---------------------------------|---------------------------|-----------------------------------|
| /grctlext                       | Extensión de control gráfico | VT \_ desconocido-lector de consultas/escritor |
| /grctlext/Disposal              |                           | VT \_ UI1                           |
| /grctlext/UserInputFlag         |                           | VT \_ bool                          |
| /grctlext/TransparencyFlag      |                           | VT \_ bool                          |
| /grctlext/Delay                 |                           | VT \_ UI2                           |
| /grctlext/TransparentColorIndex |                           | VT \_ UI1                           |
| /imgdesc                        | Descriptor de imagen          | VT \_ desconocido-lector de consultas/escritor |
| /imgdesc/Left                   |                           | VT \_ UI2                           |
| /imgdesc/Top                    |                           | VT \_ UI2                           |
| /imgdesc/Width                  |                           | VT \_ UI2                           |
| /imgdesc/Height                 |                           | VT \_ UI2                           |
| /imgdesc/LocalColorTableFlag    |                           | VT \_ bool                          |
| /imgdesc/InterlaceFlag          |                           | VT \_ bool                          |
| /imgdesc/SortFlag               |                           | VT \_ bool                          |
| /imgdesc/LocalColorTableSize    |                           | VT \_ UI1                           |



 

### <a name="png-metadata"></a>Metadatos PNG

El formato de imagen PNG (Portable Network Graphics) admite metadatos de nivel de marco.

> [!Note]  
> Para obtener una lista completa de los metadatos PNG junto con información más detallada, vea el [estándar PNG](https://www.w3.org/TR/PNG/) en el sitio web de W3C.

 

### <a name="frame-metadata"></a>Metadatos de marco

En la tabla siguiente se proporcionan las rutas de consulta de metadatos disponibles que se pueden usar para tener acceso a los metadatos de PNG de nivel de marco.



| Ruta                                                   | Nombre             | Tipo                                      |
|--------------------------------------------------------|------------------|-------------------------------------------|
| /text o/ \[ \* \] Text donde \* = 0 a N                 | Fragmento de texto       | \_Lector/escritor de consultas de texto desconocido VT    |
| /tEXt/{str = \* } Where \* = palabra clave de identificación del texto |                  | VT \_ LPSTR                                 |
| /gAMA                                                  | Fragmento gama       | VT \_ desconocido-gama de lectura/escritura de consultas    |
| /gAMA/ImageGamma                                       |                  | VT \_ UI4                                   |
| /iTXt o/ \[ \* \] iTXt donde \* = 0 a N                 | Fragmento IText      | VT \_ desconocido-iTXt de lectura/escritura de consultas    |
| /iTXt/Keyword                                          |                  | VT \_ LPSTR                                 |
| /iTXt/CompressionFlag                                  |                  | VT \_ UI1                                   |
| /iTXt/LanguageTag                                      |                  | LPSTR                                     |
| /iTXt/TranslatedKeyword                                |                  | LPWSTR                                    |
| /iTXt/TextEntry                                        |                  | LPWSTR                                    |
| /cHRM                                                  | Fragmento de HRM        | VT \_ desconocido-cHRM de lectura/escritura de consultas    |
| /cHRM/WhitePointX                                      |                  | VT \_ UI4                                   |
| /cHRM/WhitePointY                                      |                  | VT \_ UI4                                   |
| /cHRM/RedX                                             |                  | VT \_ UI4                                   |
| /cHRM/RedY                                             |                  | VT \_ UI4                                   |
| /cHRM/GreenX                                           |                  | VT \_ UI4                                   |
| /cHRM/GreenY                                           |                  | VT \_ UI4                                   |
| /cHRM/BlueX                                            |                  | VT \_ UI4                                   |
| /cHRM/BlueY                                            |                  | VT \_ UI4                                   |
| /sRGB                                                  | sRGB Chuck       | \_Lector/escritor de consulta de VT desconocido-sRGB    |
| /sRGB/RenderingIntent                                  |                  | VT \_ UI1                                   |
| /tIME                                                  | Fragmento de tiempo       | \_Lector/escritor de consultas en tiempo desconocido de VT    |
| /tIME/Year                                             |                  | VT \_ UI2                                   |
| /tIME/Month                                            |                  | VT \_ UI1                                   |
| /tIME/Day                                              |                  | VT \_ UI1                                   |
| /tIME/Hour                                             |                  | VT \_ UI1                                   |
| /tIME/Minute                                           |                  | VT \_ UI1                                   |
| /tIME/Second                                           |                  | VT \_ UI1                                   |
| /bKGD                                                  | Fragmento de fondo | VT \_ desconocido-bKGB de lectura/escritura de consultas    |
| /bKGD/BackgroundColor                                  |                  | VT \_ UI1, VT \_ UI2 o VT \_ UI2 \| VT \_ |
| /hIST                                                  | Fragmento de hIST       | VT \_ desconocido-lector/escritor de consultas de hist    |
| /hIST/Frequencies                                      |                  | VT \_ Vector \| VT \_ UI2                     |
| /iCCP                                                  | Fragmento iCCP       | VT \_ desconocido-ICCP de lectura/escritura de consultas    |
| /iCCP/ProfileName                                      |                  | VT \_ LPSTR                                 |
| /iCCP/ProfileData                                      |                  | VT \_ Vector \| VT \_ UI1                     |



 

### <a name="tiff-metadata"></a>Metadatos TIFF

El formato de imagen de Tagged Image File Format (TIFF) admite metadatos de nivel de marco.

> [!Note]  
> Para obtener una lista completa de los metadatos TIFF junto con información más detallada, vea [el estándar TIFF](https://www.adobe.io/content/dam/udp/en/open/standards/tiff/TIFF6.pdf).

 

### <a name="frame-metadata"></a>Metadatos de marco

En la tabla siguiente se proporcionan las rutas de consulta de metadatos disponibles que se pueden usar para tener acceso a los metadatos TIFF de nivel de marco.



| Ruta                                          | Nombre            | Tipo                                |
|-----------------------------------------------|-----------------|-------------------------------------|
| /ifd                                          | 0 IFD           | VT \_ desconocido: lector/escritor de consultas |
| /IFD/{ushort = \* } donde \* = 0 a 65535        | Entrada de IFD por identificador | Variable                            |
| /IFD/Thumb o/IFD/{ushort = 330}               | IFD en miniatura   | VT \_ desconocido: lector/escritor de consultas |
| /IFD/XMP o/IFD/{ushort = 700}                 | XMP             | VT \_ desconocido: lector/escritor de consultas |
| /IFD/Exif o/IFD/{ushort = 34665}              | EXIF            | VT \_ desconocido: lector/escritor de consultas |
| /IFD/GPS o/IFD/{ushort = 34853}               | GPS             | VT \_ desconocido: lector/escritor de consultas |
| /IFD/Exif/Interop o/IFD/Exif/{ushort = 40965} | Interop         | VT \_ desconocido: lector/escritor de consultas |
| /IFD/IPTC o/IFD/{ushort = 33723}              | CREACIÓN            | VT \_ desconocido: lector/escritor de consultas |
| /IFD/IPTC/{Str = \* } donde \* = palabra clave IPTC    | Entrada de IPTC      | Variable                            |
| /ifd/irb/8bimiptc/iptc                        | CREACIÓN            | VT \_ desconocido: lector/escritor de consultas |
| /IFD/IRB/8bimiptc/IPTC/{Str = \* }               | Entrada de IPTC      | Variable                            |



 

### <a name="jpeg-metadata"></a>Metadatos JPEG

El formato de imagen JPEG admite metadatos de nivel de marco.

> [!Note]  
> Para obtener una lista completa de metadatos JPEG junto con información más detallada, consulte el [estándar Exif JPEG](http://www.cipa.jp/std/documents/e/DC-008-2010_E.pdf).

 

### <a name="frame-metadata"></a>Metadatos de marco

En la tabla siguiente se proporcionan las rutas de consulta de metadatos disponibles que se pueden usar para tener acceso a los metadatos JPEG de nivel de marco.



| Ruta                                                               | Nombre                 | Tipo                                          |
|--------------------------------------------------------------------|----------------------|-----------------------------------------------|
| /app0                                                              | App0                 | VT \_ desconocido-App0 de lectura/escritura de consultas        |
| /app0/{ushort = 0}                                                   | Versión              | VT \_ UI2                                       |
| /app0/{ushort = 1}                                                   | Unidades                | VT \_ UI1                                       |
| /app0/{ushort = 2}                                                   | DpiX                 | VT \_ UI2                                       |
| /app0/{ushort = 3}                                                   | DpiY                 | VT \_ UI2                                       |
| /app0/{ushort = 4}                                                   | Xthumbnail           | VT \_ UI1                                       |
| /app0/{ushort = 5}                                                   | Ythumbnail           | VT \_ UI1                                       |
| /app0/{ushort = 6}                                                   | ThumbnailData        | BLOB de VT \_                                      |
| /app1                                                              | Aplicación 1                 | VT \_ desconocido: lector/escritor de consultas de app1        |
| /app1/IFD o/app1/{ushort = 0}                                     | 0 IFD                | VT \_ desconocido-lector/escritor de consultas IFD         |
| /app1/IFD/Exif o/app1/IFD/{ushort = 34665}                         | IFD DE EXIF             | VT \_ desconocido: lector/escritor de consultas EXIF        |
| /app1/Thumb o/app1/{ushort = 1}                                   | IFD en miniatura        | VT \_ desconocido-SubIFD de lectura/escritura de consultas      |
| /app13                                                             | App13                | VT \_ desconocido-App13 de lectura/escritura de consultas       |
| /app13/IRB o/app13/{ushort = 0}                                    | IRB                  | VT \_ desconocido-IRB de lectura/escritura de consultas         |
| /app13/IRB/{ulonglong = \* } donde \* = identificador de IRB (vea la especificación IRB) | Entrada IRB            | VT \_ desconocido-lector/escritor de consultas desconocido     |
| /app13/IRB/{ulonglong = \* }/{}                                       | Contenido de la entrada IRB   | BLOB de VT \_                                      |
| /app13/IRB/8bimiptc o/app13/IRB/{ulonglong = 61857348781060}       | 8BIMIPTC             | VT \_ desconocido-8BIMIPTC de lectura/escritura de consultas    |
| /app13/irb/8bimiptc/iptc                                           | CREACIÓN                 | VT \_ /escritor de consultas desconocido-IPTC desconocido        |
| /app13/IRB/8bimiptc/IPTC/{Str = \* }                                  | Entrada de IPTC           | Variable                                      |
| /app13/irb/8bimResInfo o/app13/IRB/{ulonglong = 61857348781037}    | Información de resolución de 8BIM | VT \_ desconocido-lector de consultas/escritor             |
| /app13/irb/8bimResInfo/PString                                     |                      | VT \_ LPSTR                                     |
| /app13/irb/8bimResInfo/HResolution                                 |                      | VT \_ UI4                                       |
| /app13/irb/8bimResInfo/VResolution                                 |                      | VT \_ UI4                                       |
| /app13/irb/8bimResInfo/WidthUnit                                   |                      | VT \_ UI2                                       |
| /app13/irb/8bimResInfo/HeightUnit                                  |                      | VT \_ UI2                                       |
| /app13/irb/8bimResInfo/HResolutionUnit                             |                      | VT \_ UI2                                       |
| /app13/irb/8bimResInfo/VResolutionUnit                             |                      | VT \_ UI2                                       |
| /com                                                               | Comentario JPEG         | \_Lector/escritor de consultas de comentario desconocido VT     |
| /com/TextEntry                                                     |                      | LPSTR                                         |
| /luminance                                                         | Luminance            | VT \_ desconocido-lector/escritor de consultas de luminancia   |
| /luminance/TableEntry                                              |                      | \_Vector VT UI1 \| VT \_                         |
| /chrominance                                                       | Chrominance          | VT \_ desconocido-lector/escritor de consultas de crominancia |
| /chrominance/TableEntry                                            |                      | \_Vector VT UI1 \| VT \_                         |
| /xmp                                                               | XMP                  | VT \_ desconocido-lector/escritor de consultas XMP         |



 

## <a name="file-format-independent-metadata"></a>Metadatos independientes del formato de archivo

Las secciones siguientes contienen información sobre los formatos de metadatos que se admiten en varios formatos de imagen. Cada tabla tiene las columnas siguientes:

-   **Ruta de acceso relativa** : la ruta de la consulta que se usa para recuperar el elemento de metadatos, en relación con el bloque de metadatos.
-   **Name** : el nombre del elemento de metadatos.
-   **Type** : el tipo de elemento de metadatos recuperado de la ruta de acceso de la consulta. Los metadatos recuperados por [WIC](-wic-api.md) se devuelven en forma de PROPVARIANT, que notifica el tipo de datos mediante la enumeración VARTYPE.

> [!Note]  
> Las tablas aquí solo proporcionan la ruta de acceso relativa para tener acceso a un elemento de metadatos en el formato de metadatos determinado. Para obtener la consulta de metadatos completa, anexe esta ruta de acceso relativa a la consulta de bloque de metadatos para el formato de metadatos determinado.

 

Por ejemplo, para tener acceso a la marca de [orientación](-wic-photoprop-system-photo-orientation.md) en un archivo JPEG, utilice la siguiente expresión:

-   /app1/IFD/{ushort = 274}

En un archivo TIFF, use la siguiente expresión:

-   /IFD/{ushort = 274}

En este ejemplo, tenga en cuenta que los distintos formatos de imagen pueden almacenar un bloque de metadatos determinado de forma diferente, por lo que la consulta de metadatos completa para tener acceso a un elemento de metadatos determinado puede tener un formato de imagen específico. Vea la tabla de cada formato para encontrar la consulta de metadatos adecuada para tener acceso a un bloque de metadatos determinado.

### <a name="ifd-metadata"></a>Metadatos de IFD

Un IFD, o un directorio de archivos de imagen, es una estructura de datos definida en el estándar TIFF que puede contener metadatos de imagen. Identifica cada elemento de metadatos mediante una etiqueta de tipo ushort. JPEG, TIFF y JPEG-XR admiten metadatos de IFD. Los formatos de terceros, como algunos formatos RAW de cámara, también pueden admitir metadatos de IFD.

En la tabla siguiente se proporcionan las rutas de acceso de consulta de metadatos relativas para acceder a algunos elementos de metadatos IFD usados comúnmente. La estructura de datos de IFD permite la extensibilidad de terceros y esta tabla no es una lista exhaustiva. Consulte el estándar TIFF para obtener más información.

> [!Note]  
> Aunque JPEG y otros formatos admiten la estructura de datos de IFD, no pueden usar todos los elementos de metadatos que define. Para obtener más información, consulte el estándar de cada formato.

 

> [!Note]  
> Algunos elementos de metadatos de la tabla requieren una interpretación o información adicional para usarse correctamente, consulte el estándar TIFF. Por ejemplo, el elemento de metadatos [PhotometricInterpretation](-wic-photoprop-system-photo-photometricinterpretation.md) devuelve un PROPVARIANT de tipo VT \_ UI2. Sin embargo, según el estándar TIFF, se interpreta como una enumeración. Consulte el estándar TIFF para obtener más información.

 



| Ruta relativa   | Nombre                      | Tipo                                           |
|-----------------|---------------------------|------------------------------------------------|
| /{ushort = 256}   | ImageWidth                | VT \_ UI2 o VT \_ UI4                             |
| /{ushort = 257}   | ImageLength               | VT \_ UI2 o VT \_ UI4                             |
| /{ushort = 258}   | BitsPerSample             | VT \_ UI2                                        |
| /{ushort = 259}   | Compresión               | VT \_ UI2                                        |
| /{ushort = 262}   | PhotometricInterpretation | VT \_ UI2                                        |
| /{ushort = 274}   | Orientación               | VT \_ UI2                                        |
| /{ushort = 277}   | SamplesPerPixel           | VT \_ UI2                                        |
| /{ushort = 284}   | PlanarConfiguration       | VT \_ UI2                                        |
| /{ushort = 530}   | YCbCrSubSampling          | VT \_ Vector \| VT \_ UI2                          |
| /{ushort = 531}   | YCbCrPositioning          | VT \_ UI2                                        |
| /{ushort = 282}   | XResolution               | VT \_ UI8                                        |
| /{ushort = 283}   | YResolution               | VT \_ UI8                                        |
| /{ushort = 296}   | ResolutionUnit            | VT \_ UI2                                        |
| /{ushort = 306}   | DateTime                  | VT \_ LPSTR                                      |
| /{ushort = 270}   | ImageDescription          | VT \_ LPSTR                                      |
| /{ushort = 271}   | Make                      | VT \_ LPSTR                                      |
| /{ushort = 272}   | Modelo                     | VT \_ LPSTR                                      |
| /{ushort = 305}   | Software                  | VT \_ LPSTR                                      |
| /{ushort = 315}   | Artistas                    | VT \_ LPSTR                                      |
| /{ushort = 33432} | Copyright                 | VT \_ LPSTR                                      |
| /{ushort = 338}   | Ejemplos de              | VT \_ UI2                                        |
| /{ushort = 254}   | NewSubfileType            | VT \_ UI4                                        |
| /{ushort = 278}   | RowsPerStrip              | VT \_ UI2 o VT \_ UI4                             |
| /{ushort = 279}   | StripByteCounts           | VT \_ Vector \| VT \_ UI2 o VT \_ Vector \| VT \_ UI4 |
| /{ushort = 273}   | StripOffsets              | VT \_ Vector \| VT \_ UI2 o VT \_ Vector \| VT \_ UI4 |



 

### <a name="exif-metadata"></a>Metadatos EXIF

Los metadatos EXIF se definen como parte de la especificación EXIF JPEG. Los metadatos EXIF se basan en la estructura de datos de IFD tal y como se define en el estándar TIFF y proporcionan atributos adicionales, como información sobre los dispositivos y atributos fotográficos usados para crear la imagen. Identifica cada elemento de metadatos mediante una etiqueta de tipo ushort. JPEG, TIFF y JPEG-XR admiten metadatos EXIF. Los formatos de terceros, como algunos formatos RAW de cámara, también pueden admitir metadatos EXIF.

En la tabla siguiente se proporcionan las rutas de acceso de consulta de metadatos relativas para acceder a algunos elementos de metadatos EXIF usados habitualmente. La estructura de datos EXIF permite la extensibilidad de terceros y esta tabla no es una lista exhaustiva. Consulte el estándar EXIF para obtener más información.

> [!Note]  
> Muchos elementos de metadatos EXIF se definen en el estándar EXIF como tipo "RATIONAL" o "SRATIONAL". Una "racional" consta de un numerador y un denominador, que son enteros de 32 bits sin signo. El numerador se encuentra en los bits 32 altos y el denominador en los 32 bits inferiores. En [WIC](-wic-api.md), se devuelven como PROPVARIANT con un tipo de VT \_ UI8 o VT \_ i8, respectivamente; el valor real se almacena como ULARGE \_ entero o grande \_ , respectivamente. Para tener acceso al numerador y al denominador, lea los miembros HighPart y LowPart del \_ valor entero ULARGE o entero grande \_ .

 

> [!Note]  
> Algunos elementos de metadatos de la tabla siguiente requieren una interpretación o información adicional para utilizarlos correctamente. Por ejemplo, el elemento de metadatos [ColorSpace](-wic-photoprop-system-image-colorspace.md) devuelve un PROPVARIANT de tipo VT \_ UI2. Sin embargo, según el estándar EXIF, se interpreta como una enumeración. Vea el estándar EXIF para obtener más información.

 



| Ruta relativa   | Nombre                      | Tipo                  |
|-----------------|---------------------------|-----------------------|
| /{ushort = 36864} | ExifVersion               | BLOB de VT \_              |
| /{ushort = 40960} | FlashpixVersion           | BLOB de VT \_              |
| /{ushort = 40961} | ColorSpace                | VT \_ UI2               |
| /{ushort = 40962} | PixelXDimension           | VT \_ UI2 o VT \_ UI4    |
| /{ushort = 40963} | PixelYDimension           | VT \_ UI2 o VT \_ UI4    |
| /{ushort = 37500} | MakerNote                 | BLOB de VT \_              |
| /{ushort = 37510} | UserComment               | VT \_ LPWStr            |
| /{ushort = 36867} | DateTimeOriginal          | VT \_ LPSTR             |
| /{ushort = 36868} | DateTimeDigitized         | VT \_ LPSTR             |
| /{ushort = 42016} | ImageUniqueID             | VT \_ LPSTR             |
| /{ushort = 42032} | CameraOwnerName           | VT \_ LPSTR             |
| /{ushort = 42033} | BodySerialNumber          | VT \_ LPSTR             |
| /{ushort = 42034} | LensSpecification         | VT \_ Vector \| VT \_ UI8 |
| /{ushort = 42035} | LensMake                  | VT \_ LPSTR             |
| /{ushort = 42036} | LensModel                 | VT \_ LPSTR             |
| /{ushort = 42037} | LensSerialNumber          | VT \_ LPSTR             |
| /{ushort = 33434} | ExposureTime              | VT \_ UI8               |
| /{ushort = 33437} | FNumber                   | VT \_ UI8               |
| /{ushort = 34850} | ExposureProgram           | VT \_ UI2               |
| /{ushort = 34852} | SpectralSensitivity       | VT \_ LPSTR             |
| /{ushort = 34855} | PhotographicSensitivity   | VT \_ Vector \| VT \_ UI2 |
| /{ushort = 34856} | OECF                      | BLOB de VT \_              |
| /{ushort = 34864} | SensitivityType           | VT \_ UI2               |
| /{ushort = 34865} | StandardOutputSensitivity | VT \_ UI4               |
| /{ushort = 34866} | RecommendedExposureIndex  | VT \_ UI4               |
| /{ushort = 34867} | Isospeed                  | VT \_ UI4               |
| /{ushort = 34868} | ISOSpeedLatitudeyyy       | VT \_ UI4               |
| /{ushort = 34869} | ISOSpeedLatitudezzz       | VT \_ UI4               |
| /{ushort = 37377} | ShutterSpeedValue         | VT \_ i8                |
| /{ushort = 37378} | ApertureValue             | VT \_ UI8               |
| /{ushort = 37379} | BrightnessValue           | VT \_ i8                |
| /{ushort = 37380} | ExposureBiasValue         | VT \_ i8                |
| /{ushort = 37381} | MaxApertureValue          | VT \_ UI8               |
| /{ushort = 37382} | SubjectDistance           | VT \_ UI8               |
| /{ushort = 37383} | MeteringMode              | VT \_ UI2               |
| /{ushort = 37384} | LightSource               | VT \_ UI2               |
| /{ushort = 37385} | Intermitente                     | VT \_ UI2               |
| /{ushort = 37386} | FocalLength               | VT \_ UI8               |
| /{ushort = 37396} | SubjectArea               | VT \_ Vector \| VT \_ UI2 |
| /{ushort = 41483} | FlashEnergy               | VT \_ UI8               |
| /{ushort = 41484} | SpatialFrequencyResponse  | BLOB de VT \_              |
| /{ushort = 41486} | FocalPlaneXResolution     | VT \_ UI8               |
| /{ushort = 41487} | FocalPlaneYResolution     | VT \_ UI8               |
| /{ushort = 41488} | FocalPlaneResolutionUnit  | VT \_ UI2               |
| /{ushort = 41492} | SubjectLocation           | VT \_ Vector \| VT \_ UI2 |
| /{ushort = 41493} | ExposureIndex             | VT \_ UI8               |
| /{ushort = 41495} | SensingMethod             | VT \_ UI2               |
| /{ushort = 41728} | FileSource                | BLOB de VT \_              |
| /{ushort = 41729} | SceneType                 | BLOB de VT \_              |
| /{ushort = 41730} | CFAPattern                | BLOB de VT \_              |
| /{ushort = 41985} | CustomRendered            | VT \_ UI2               |
| /{ushort = 41986} | ExposureMode              | VT \_ UI2               |
| /{ushort = 41987} | WhiteBalance              | VT \_ UI2               |
| /{ushort = 41988} | DigitalZoomRatio          | VT \_ UI8               |
| /{ushort = 41989} | FocalLengthIn35mmFilm     | VT \_ UI2               |
| /{ushort = 41990} | SceneCaptureType          | VT \_ UI2               |
| /{ushort = 41991} | GainControl               | VT \_ UI8               |
| /{ushort = 41992} | Compare                  | VT \_ UI2               |
| /{ushort = 41993} | Saturación                | VT \_ UI2               |
| /{ushort = 41994} | Nitidez                 | VT \_ UI2               |
| /{ushort = 41995} | DeviceSettingDescription  | BLOB de VT \_              |
| /{ushort = 41996} | SubjectDistanceRange      | VT \_ UI2               |



 

### <a name="gps-metadata"></a>Metadatos de GPS

Los metadatos de GPS contienen información de geolocalización y se define como parte de la especificación de JPEG EXIF. Identifica cada elemento de metadatos mediante una etiqueta de tipo ushort. JPEG, TIFF y JPEG-XR admiten metadatos de GPS; los formatos de terceros, como algunos formatos RAW de cámara, también pueden admitir metadatos de GPS.

En la tabla siguiente se proporcionan las rutas de acceso de consulta de metadatos relativas para acceder a algunos elementos de metadatos GPS usados habitualmente. Esta tabla no es una lista exhaustiva; Consulte el estándar EXIF para obtener más información.

> [!Note]  
> Muchos elementos de metadatos de GPS se definen en el estándar EXIF como tipo "RATIONAL". Una "racional" consta de un numerador y un denominador, que son enteros de 32 bits sin signo. El numerador se encuentra en los bits 32 altos y el denominador en los 32 bits inferiores. En [WIC](-wic-api.md), estos se devuelven como PROPVARIANT con un tipo de VT \_ UI8. El valor real se almacena como un \_ entero ULARGE. Para tener acceso al numerador y al denominador, lea los miembros HighPart y LowPart del \_ valor entero ULARGE.

 

> [!Note]  
> Algunos elementos de metadatos de la tabla requieren una interpretación o información adicional para usarlos correctamente. Por ejemplo, el elemento de metadatos GPSLatitudeRef devuelve un PROPVARIANT de tipo VT \_ LPSTR. Según el estándar EXIF, esta cadena es "N" o "S", que representa la latitud norte o sur. Vea el estándar EXIF para obtener más información.

 



| Ruta relativa | Nombre            | Tipo                                          |
|---------------|-----------------|-----------------------------------------------|
| {ushort = 0}    | GPSVersionID    | VT \_ Vector \| VT \_ UI1                         |
| {ushort = 1}    | GPSLatitudeRef  | VT \_ LPSTR                                     |
| {ushort = 2}    | GPSLatitude     | VT \_ Vector \| VT \_ UI8                         |
| {ushort = 3}    | GPSLongitudeRef | VT \_ LPSTR                                     |
| {ushort = 4}    | GPSLongitude    | {ushort = 4} GPSLongitude VT \_ Vector \| VT \_ UI8 |
| {ushort = 5}    | GPSAltitudeRef  | VT \_ UI1                                       |
| {ushort = 6}    | GPSAltitude     | VT \_ UI8                                       |
| {ushort = 7}    | GPSTimeStamp    | VT \_ Vector \| VT \_ UI8                         |
| {ushort = 8}    | GPSSatellites   | VT \_ LPSTR                                     |
| {ushort = 9}    | GPSStatus       | VT \_ LPSTR                                     |
| {ushort = 10}   | GPSMeasureMode  | VT \_ LPSTR                                     |
| {ushort = 11}   | GPSDOP          | VT \_ UI8                                       |
| {ushort = 12}   | GPSSpeedRef     | VT \_ LPSTR                                     |
| {ushort = 13}   | GPSSpeed        | VT \_ UI8                                       |
| {ushort = 14}   | GPSTrackRef     | VT \_ LPSTR                                     |
| {ushort = 15}   | GPSTrack        | VT \_ UI8                                       |



 

### <a name="xmp-metadata"></a>Metadatos XMP

XMP es un estándar de metadatos extensible basado en XML. Los elementos de metadatos pueden ser jerárquicos y contener estructuras de datos complejas. JPEG, TIFF y JPEG-XR admiten metadatos XMP. Los formatos de terceros, como algunos formatos RAW de cámara, también pueden admitir metadatos XMP.

El estándar XMP se puede obtener de: <https://www.adobe.com/devnet/xmp.html> .

XMP y permite a las entidades de terceros publicar sus propios esquemas, o espacios de nombres, que les permiten definir nuevos elementos de metadatos sin tener que modificar el estándar XMP. Un esquema XMP se identifica de forma única mediante una dirección URL, pero [WIC](-wic-api.md) proporciona un conjunto de identificadores descriptivos para los esquemas conocidos.

Los elementos de metadatos XMP se identifican mediante un nombre de cadena, así como un identificador de esquema. Como práctica recomendada, cada consulta de metadatos XMP debe especificar el esquema y el nombre. Si falta el identificador de esquema, JPEG intentará hacer coincidir el nombre de los metadatos en todos los espacios de nombres presentes en el paquete de metadatos XMP.

Por ejemplo, para obtener la propiedad rating tal como la define el esquema XMP en una imagen JPEG, utilice la siguiente consulta:

-   /XMP/{wstr =https://ns.adobe.com/xap/1.0/}:Rating

La primera parte, "/XMP", recupera el lector/escritor de metadatos XMP para la imagen. " https://ns.adobe.com/xap/1.0/ " es la dirección URL del esquema XMP, tal como se define en el estándar XMP. La dirección URL se incluye en una expresión de datos para permitir el uso de caracteres como una barra diagonal (/). Finalmente, "rating" es el nombre de elemento de metadatos real tal y como lo define el esquema XMP y se separa del identificador de esquema mediante dos puntos (:).

En este ejemplo, WIC proporciona un identificador descriptivo para el esquema XMP que se puede usar en lugar de la dirección URL completa. Por lo tanto, la consulta anterior se puede volver a escribir de la siguiente manera:

-   /XMP/XMP: clasificación

[WIC](-wic-api.md) proporciona prefijos de esquema descriptivos para los siguientes esquemas de uso frecuente:



| Prefijo de esquema  | URL de esquema                                        | Vínculo a estándar                                         |
|----------------|---------------------------------------------------|----------------------------------------------------------|
| RDF            | https://www.w3.org/1999/02/22-rdf-syntax-ns\#      | <https://www.w3.org/TR/REC-rdf-syntax/>                   |
| dc             | https://purl.org/dc/elements/1.1/                  | <https://www.adobe.com/devnet/xmp.html>                   |
| XMP            | https://ns.adobe.com/xap/1.0/                      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpidq         | https://ns.adobe.com/xmp/Identifier/qual/1.0/      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpRights      | https://ns.adobe.com/xap/1.0/rights/               | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpMM          | https://ns.adobe.com/xap/1.0/mm/                   | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpBJ          | https://ns.adobe.com/xap/1.0/bj/                   | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpTPg         | https://ns.adobe.com/xap/1.0/t/pg/                 | <https://www.adobe.com/devnet/xmp.html>                   |
| pdf            | https://ns.adobe.com/pdf/1.3/                      | <https://www.adobe.com/devnet/xmp.html>                   |
| Photoshop      | https://ns.adobe.com/photoshop/1.0/                | <https://www.adobe.com/devnet/xmp.html>                   |
| tiff           | https://ns.adobe.com/tiff/1.0/                     | <https://www.adobe.com/devnet/xmp.html>                   |
| EXIF           | https://ns.adobe.com/exif/1.0/                     | <https://www.adobe.com/devnet/xmp.html>                   |
| stDim          | https://ns.adobe.com/xap/1.0/sType/Dimensions\#    | <https://www.adobe.com/devnet/xmp.html>                   |
| xapGImg        | https://ns.adobe.com/xap/1.0/g/img/                | <https://www.adobe.com/devnet/xmp.html>                   |
| stEvt          | https://ns.adobe.com/xap/1.0/sType/ResourceEvent\# | <https://www.adobe.com/devnet/xmp.html>                   |
| stRef          | https://ns.adobe.com/xap/1.0/sType/ResourceRef\#   | <https://www.adobe.com/devnet/xmp.html>                   |
| stVer          | https://ns.adobe.com/xap/1.0/sType/Version\#       | <https://www.adobe.com/devnet/xmp.html>                   |
| stJob          | https://ns.adobe.com/xap/1.0/sType/Job\#           | <https://www.adobe.com/devnet/xmp.html>                   |
| AUX            | https://ns.adobe.com/exif/1.0/aux/                 | <https://www.adobe.com/devnet/xmp.html>                   |
| CRS            | https://ns.adobe.com/camera-raw-settings/1.0/      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpDM          | https://ns.adobe.com/xmp/1.0/DynamicMedia/         | <https://www.adobe.com/devnet/xmp.html>                   |
| Iptc4xmpCore   | https://iptc.org/std/Iptc4xmpCore/1.0/xmlns/       | <https://www.iptc.org/cms/site/index.html?channel=CH0099> |
| MicrosoftPhoto | https://ns.microsoft.com/photo/1.0/                | [Información general sobre el etiquetado de personas](-wic-people-tagging.md)       |
| MP             | https://ns.microsoft.com/photo/1.2/                | [Información general sobre el etiquetado de personas](-wic-people-tagging.md)       |
| MPRI           | https://ns.microsoft.com/photo/1.2/t/RegionInfo\#  | [Información general sobre el etiquetado de personas](-wic-people-tagging.md)       |
| MPReg          | https://ns.microsoft.com/photo/1.2/t/Region\#      | [Información general sobre el etiquetado de personas](-wic-people-tagging.md)       |



 

Si no hay un prefijo de esquema descriptivo para un esquema determinado, por ejemplo, si una imagen contiene metadatos XMP mediante un esquema personalizado de terceros, la consulta de metadatos debe usar la dirección URL completa del esquema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general del lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Información general sobre la extensibilidad de metadatos](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Cómo volver a codificar una imagen JPEG con metadatos](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
