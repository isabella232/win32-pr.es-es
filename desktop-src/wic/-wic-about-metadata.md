---
description: En este tema se presenta la compatibilidad con los metadatos de creación de imágenes que proporciona Windows Imaging Component (WIC).
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Introducción a los metadatos de WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f5031759dd73861a97aace623b35f229b75952
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472031"
---
# <a name="wic-metadata-overview"></a>Introducción a los metadatos de WIC

En este tema se presenta la compatibilidad con los metadatos de creación de imágenes que proporciona Windows Imaging Component (WIC). Proporciona una introducción a la lectura y escritura de metadatos de imagen, el lenguaje de consulta de metadatos y la extensibilidad del controlador de metadatos.

Los metadatos de imagen son datos insertados dentro de un archivo de imagen que proporcionan información adicional sobre la imagen, como el dispositivo que se usa para capturar la imagen o las dimensiones de la imagen. Aunque se encuentra dentro del propio archivo de imagen, estos metadatos no forman parte de los datos de representación. WIC proporciona interfaces que permiten leer y escribir estos metadatos para varios formatos de metadatos comunes, como Extensible Metadata Platform (XMP), Exchangeable Image File (EXIF) y Png Textual Data (tEXt).

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Introducción](#introduction)
-   [Leer metadatos de imagen](#reading-image-metadata)
-   [Escribir metadatos de imagen](#writing-image-metadata)
-   [Extensibilidad de metadatos](#metadata-extensibility)
-   [Formatos de metadatos admitidos](#supported-metadata-formats)
-   [Resumen del componente de metadatos](#metadata-component-summary)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Prerrequisitos

Para comprender este tema, debe estar familiarizado con las interfaces de descodificador y codificador WIC y sus componentes de Component Object Model (COM) relacionados, como se describe en la información general sobre componentes de creación de imágenes de [Windows.](-wic-about-windows-imaging-codec.md) También ayuda a familiarizarse con algunos de los formatos de metadatos de creación de imágenes que se usan actualmente.

## <a name="introduction"></a>Introducción

Los metadatos proporcionan información ampliada sobre una imagen. Esta información se puede usar de varias maneras. Una imagen puede contener metadatos como una descripción, clasificación, etiquetas de categoría e información de copyright. El acceso a los metadatos facilita la realización de tareas como la administración de recursos, la ubicación de los archivos o la determinación de la información de copyright. Por ejemplo, el Windows Galería de fotos en Windows Vista le permite agregar descripciones y etiquetas de categoría a las imágenes. Esto permite una mejor detectabilidad de las imágenes y una manera cómoda de clasificar las imágenes. Con las API de WIC y los formatos de metadatos comunes, las aplicaciones pueden escribir o leer fácilmente este tipo de metadatos hacia o desde imágenes.

En el diagrama siguiente se muestra el contenido de un archivo JPEG que incluye bloques de metadatos incrustados y elementos de metadatos.

![imagen jpeg con metadatos de clasificación](graphics/jpeg.png)

En esta imagen de ejemplo, los metadatos se incrustan en el archivo de imagen dentro de un marco de imagen. El formato JPEG no admite varios fotogramas de imagen, por lo que los metadatos se adjuntan conceptualmente a este único fotograma. Los formatos que admiten varios fotogramas, como TIFF, pueden tener metadatos asociados a cada fotograma de imagen, como se muestra en este diagrama. Aunque actualmente no son comunes y no son compatibles con los códecs de imagen nativos, algunos formatos de imagen también pueden admitir metadatos fuera de un marco de imagen. WIC es lo suficientemente flexible como para controlar metadatos de nivel de fotograma y metadatos fuera del marco individual de una imagen.

## <a name="reading-image-metadata"></a>Leer metadatos de imagen

Las API de WIC proporcionan componentes COM que hacen que sea fácil para las aplicaciones leer y escribir metadatos de imagen.

La manera principal de leer los metadatos es usar un lector de consultas de metadatos [**(IWICMetadataQueryReader)**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)para acceder a elementos de metadatos específicos. El códec implementa el componente de lector de consultas de metadatos y se puede acceder a ellos en el nivel de descodificador o a través de fotogramas de imagen individuales, que es el método más común. El código siguiente muestra cómo acceder a un lector de consultas para un marco individual mediante el método **GetMetadataQueryReader del** lector de consultas.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Un lector de consultas proporciona métodos para obtener información sobre metadatos específicos y un medio para especificar un elemento de metadatos para recuperar. El código siguiente usa una expresión de consulta para solicitar un elemento de metadatos específico dentro del bloque de directorio de archivos de imagen anidado (IFD) app1. Esto se hace mediante el método **GetMetadataByName** del lector de consultas. En el código siguiente se muestra cómo usar el lector de consultas para obtener el valor de clasificación MicrosoftPhoto.


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



La variable pwzRatingQuery del ejemplo anterior es la cadena de consulta para acceder al elemento de metadatos clasificación MicrosoftPhoto. Esta cadena se crea mediante el lenguaje de consulta de metadatos. Para crear esta cadena, es necesario conocer el formato de metadatos y el lenguaje de consulta de metadatos para recuperar elementos de metadatos individuales. Para obtener más información sobre el lenguaje de consulta de metadatos, vea Información general del lenguaje [de consulta de metadatos](-wic-codec-metadataquerylanguage.md).

En segundo plano, un lector de consultas usa un lector de metadatos [**(IWICMetadataReader)**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)para acceder a los metadatos descritos por la expresión de consulta. Además de usar un lector de consultas, también puede acceder a un lector de metadatos directamente para leer los metadatos. Puede obtener un lector de metadatos del descodificador o fotogramas individuales consultando una interfaz de lector de bloques [**(IWICMetadataBlockReader).**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)

## <a name="writing-image-metadata"></a>Escribir metadatos de imagen

El proceso de escritura de metadatos es similar a la forma en que se leen, salvo que se usa un escritor de consultas de metadatos [**(IWICMetadataQueryWriter).**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) El codificador de imágenes implementa la interfaz del escritor de consultas y, al igual que en el lector de consultas, se accede a los metadatos tanto en el codificador como en fotogramas individuales (en función de la compatibilidad con el formato de imagen).

El código siguiente muestra cómo obtener un escritor de consultas de un marco de codificador y quitar el valor de clasificación que se leyó anteriormente.


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



Otra manera de escribir metadatos es a través de actualizaciones rápidas de metadatos. La codificación rápida de metadatos es una manera de escribir metadatos de imagen sin tener que volver a codificar un archivo de imagen. Para ello, escriba nueva información de metadatos en una región de acolchada con el formato de metadatos. El codificador de metadatos rápido [**(IWICFastMetadataEncoder)**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)se obtiene del generador de componentes, en función del descodificador de imágenes. A continuación, el codificador de metadatos rápido obtiene un escritor de consultas que se usa para escribir los metadatos. Por último, el codificador rápido confirma el cambio.

El código siguiente muestra cómo obtener un codificador de metadatos rápido y usarlo para escribir el valor MicrosoftRating.


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



No todos los formatos de metadatos admiten metadatos rápidos. Para ver qué formatos admitidos de forma nativa admiten la codificación rápida de metadatos, consulte la tabla de la sección [Formatos](#supported-metadata-formats) de metadatos admitidos más adelante en este documento.

En segundo plano, un escritor de consultas usa un escritor de metadatos [**(IWICMetadataWriter)**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)para escribir los metadatos descritos por la expresión de consulta. Además de usar un lector de consultas, también puede acceder a un escritor de metadatos directamente para escribir metadatos. Puede obtener un escritor de metadatos desde el descodificador o fotogramas individuales mediante la consulta de una interfaz de escritor de bloques [**(IWICMetadataBlockWriter).**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)

## <a name="metadata-extensibility"></a>Extensibilidad de metadatos

Como se mencionó anteriormente, WIC proporciona varios controladores de metadatos para leer y escribir metadatos para formatos de metadatos comunes. Sin embargo, hay algunos formatos de metadatos que no se admiten de forma nativa. Por lo tanto, WIC proporciona API para crear controladores de metadatos adicionales que pueden ampliar la compatibilidad con metadatos a otros formatos.

Para admitir completamente otros formatos de metadatos, se deben desarrollar dos tipos de controladores: un lector de metadatos para leer metadatos y un escritor de metadatos para escribir metadatos. Aunque estos dos controladores normalmente se implementan en pares para un formato específico, no es un requisito. Puede haber algunos casos en los que solo se necesita la capacidad de lectura o solo la capacidad de escritura.

Para obtener más información sobre la extensibilidad de metadatos mediante las API de WIC, vea Información general sobre [la extensibilidad de metadatos.](-wic-codec-metadatahandlers.md)

## <a name="supported-metadata-formats"></a>Formatos de metadatos admitidos

WIC proporciona compatibilidad con varios formatos de metadatos comunes. En la tabla siguiente se enumeran los formatos de metadatos admitidos, sus versiones, los formatos de imagen que admiten el formato de metadatos y si el formato de metadatos admite la codificación rápida de metadatos. Para obtener más información sobre la codificación rápida de metadatos, consulte la sección Escribir metadatos [de](#writing-image-metadata) imagen anteriormente en este documento.



| Formatos de metadatos admitidos | Versión de especificación de metadatos | Compatibilidad con el formato de imagen | Admite la codificación rápida de metadatos |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| App0                       | JFIF 1.02                      | JPEG                 | No                              |
| Aplicación 1                       | JFIF 1.02                      | JPEG, TIFF           | No                              |
| App13                      | Unknown                        | JPEG, TIFF           | No                              |
| IFD                        | TIFF 6.0                       | JPEG, TIFF           | Sí                             |
| IRB                        | Unknown                        | JPEG, TIFF           | No                              |
| Exif                       | Ejemplo 2.2                       | JPEG, TIFF           | Sí                             |
| XMP                        | XMP 1.0 (septiembre de 2005)            | JPEG, TIFF           | Sí                             |
| GPS                        | Ejemplo 2.2                       | JPEG, TIFF           | Sí                             |
| IPTC                       | IPTC 4.0                       | JPEG, TIFF           | Sí                             |
| Texto                       | PNG 1.2                        | PNG                  | No                              |



 

> [!Note]  
> IPTC solo admite FME si los bloques aumentan de tamaño, ya que IPTC no admite el relleno.

 

## <a name="metadata-component-summary"></a>Resumen del componente de metadatos

En la tabla siguiente se describen las interfaces WIC que admiten metadatos y sus componentes correspondientes. Estos componentes proporcionan el acceso a los metadatos de una imagen. Para obtener más información sobre estos componentes, vea la información general Windows [componentes de creación de imágenes](-wic-about-windows-imaging-codec.md). 


| Componente | Descripción | 
|-----------|-------------|
| Descodificador de mapa de bits (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>) | <ul><li>Lee un flujo de imagen y genera un origen de mapa de bits utilizable. Asociado a un formato de contenedor, como Tagged Image File Format (TIFF) o Joint Jpeg.</li><li>Implementa una interfaz <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> para enumerar todos los bloques de metadatos del flujo de datos del descodificador que no están dentro de un marco.</li><li>Expone un lector de consultas para leer los metadatos asociados a la imagen que no está dentro de un marco.</li></ul> | 
| Descodificación de fotogramas de mapa de bits (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>) | <ul><li>Accede a fotogramas individuales desde la secuencia de imágenes que mantiene el descodificador.</li><li>Implementa una interfaz <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> para enumerar todos los bloques de metadatos del flujo de datos del marco.</li><li>Expone un lector de consultas para leer los metadatos asociados al marco, mediante expresiones de consulta.</li></ul> | 
| Bitmap Encoder (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>) | <ul><li>Escribe un origen de mapa de bits en un flujo de imagen. Asociado a un formato de contenedor como TIFF o JPEG.</li><li>Implementa una interfaz <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> para crear una lista de bloques de metadatos para escribir en el flujo de datos del codificador.</li><li>Expone un escritor de consultas para escribir los metadatos asociados a la imagen, mediante expresiones de consulta.</li></ul> | 
| Codificación de marco de Bitma (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>) | <ul><li>Crea un marco que se codificará en la secuencia que mantiene el codificador.</li><li>Implementa una interfaz <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> para crear una lista de bloques de metadatos para escribir en el flujo de datos del marco.</li><li>Expone un escritor de consultas para escribir los metadatos asociados al marco, mediante expresiones de consulta.</li></ul> | 




 

En la tabla siguiente se describen los componentes de metadatos de WIC. Estos componentes permiten leer y escribir los metadatos en una imagen expuesta por los componentes enumerados en la tabla anterior. 


| Componente | Descripción | 
|-----------|-------------|
| Lector de consultas de metadatos (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>) | <ul><li>Toma una cadena de consulta y navega por la jerarquía de metadatos subyacente para obtener los metadatos.</li></ul> | 
| Escritor de consultas de metadatos (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>) | <ul><li>Toma una cadena de consulta y navega por la jerarquía de metadatos subyacente para obtener, establecer y quitar metadatos.</li></ul> | 
| Lector de bloques de metadatos (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>) | <ul><li>Administra una colección de solo lectura de objetos <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> en la parte superior de la jerarquía de metadatos y habilita la enumeración de todos los bloques de metadatos.</li><li>Implementado por un descodificador de mapa de bits y un marco de mapa de bits descodificado.</li><li>Implementado por desarrolladores de componentes de terceros para códecs personalizados.</li></ul> | 
| Escritor de bloques de metadatos (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>) | <ul><li>Administra una colección de lectura y escritura de <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>objetos IWICMetadataWriter</strong></a> en la parte superior de la jerarquía de metadatos.</li><li>Implementado por un codificador de mapa de bits y una codificación de marco de mapa de bits.</li><li>Implementado por desarrolladores de componentes de terceros para códecs personalizados.</li></ul> | 
| Lector de metadatos (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>) | <ul><li>Analiza un flujo de metadatos y administra una colección de solo lectura de los elementos de metadatos. Asociado a un formato de metadatos como EXIF, IFD y XMP.</li><li>Actúa como diccionario y devuelve un valor cuando se le da un formato y un par de identificadores.</li><li>Implementado por desarrolladores de componentes de terceros para tipos de metadatos personalizados.</li></ul> | 
| Metadata Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>) | <ul><li>Analiza y serializa una secuencia de metadatos y administra una colección de lectura y escritura de elementos de metadatos.</li><li>Implementado por desarrolladores de componentes de terceros para tipos de metadatos personalizados.</li></ul> | 
| Codificador de metadatos<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>rápido IWICFastMetadataEncoder</strong></a> | <ul><li>Expone la semántica para escribir en una jerarquía de metadatos que actualizará los metadatos en su lugar sin volver a codificar la imagen.</li></ul> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre el lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Información general sobre extensibilidad de metadatos](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Cómo: Volver a codificar una imagen JPEG con metadatos](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



