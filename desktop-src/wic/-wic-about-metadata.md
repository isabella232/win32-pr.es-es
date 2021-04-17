---
description: En este tema se presenta la compatibilidad con metadatos de imágenes que proporciona el componente de creación de imágenes de Windows (WIC).
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Información general sobre metadatos de WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f00e3a77eb74a3fb4a00db05ef9e00028f02ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570512"
---
# <a name="wic-metadata-overview"></a>Información general sobre metadatos de WIC

En este tema se presenta la compatibilidad con metadatos de imágenes que proporciona el componente de creación de imágenes de Windows (WIC). Proporciona una introducción a la lectura y la escritura de metadatos de imagen, el lenguaje de consulta de metadatos y la extensibilidad del controlador de metadatos.

Los metadatos de la imagen son datos incrustados dentro de un archivo de imagen que proporciona información adicional sobre la imagen, como el dispositivo que se usa para capturar la imagen o las dimensiones de la imagen. Aunque se encuentra dentro del propio archivo de imagen, estos metadatos no forman parte de los datos de representación. WIC proporciona interfaces que permiten leer y escribir estos metadatos para varios formatos de metadatos comunes, entre los que se incluyen la plataforma de metadatos extensible (XMP), el archivo de imagen intercambiable (EXIF) y los datos de texto PNG (texto).

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Introducción](#introduction)
-   [Leer metadatos de imagen](#reading-image-metadata)
-   [Escribir metadatos de imagen](#writing-image-metadata)
-   [Extensibilidad de metadatos](#metadata-extensibility)
-   [Formatos de metadatos admitidos](#supported-metadata-formats)
-   [Resumen de los componentes de metadatos](#metadata-component-summary)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

Para entender este tema, debe estar familiarizado con las interfaces del codificador y el descodificador de WIC y con sus componentes de modelo de objetos componentes (COM) relacionados, tal como se describe en [información general sobre el componente de creación de imágenes de Windows](-wic-about-windows-imaging-codec.md). También ayuda a tener una familiaridad general con algunos de los formatos de metadatos de imágenes que se usan hoy en día.

## <a name="introduction"></a>Introducción

Los metadatos proporcionan información extendida sobre una imagen. Esta información se puede usar de varias maneras. Una imagen puede contener metadatos como una descripción, clasificación, etiquetas de categoría e información de copyright. El acceso a los metadatos facilita la realización de tareas como la administración de recursos, la ubicación de los archivos o la determinación de la información de copyright. Por ejemplo, la Galería fotográfica de Windows de Windows Vista permite agregar descripciones y etiquetas de categoría a las imágenes. Esto permite una mejor detectabilidad de las imágenes y una manera cómoda de clasificar las imágenes. Con las API de WIC y los formatos de metadatos comunes, las aplicaciones pueden escribir o leer fácilmente este tipo de metadatos en imágenes o desde ellas.

En el diagrama siguiente se muestra el contenido de un archivo JPEG que incluye bloques de metadatos incrustados y elementos de metadatos.

![imagen JPEG con metadatos de clasificación](graphics/jpeg.png)

En esta imagen de ejemplo, los metadatos se insertan en el archivo de imagen dentro de un marco de imagen. El formato JPEG no admite varios fotogramas de imagen, por lo que los metadatos se adjuntan conceptualmente a este único fotograma. Los formatos que admiten varios marcos, como TIFF, pueden tener metadatos adjuntos a cada fotograma de imagen como se muestra en este diagrama. Aunque no es habitual hoy y no es compatible con los códecs de imagen nativa, algunos formatos de imagen también pueden admitir metadatos fuera de un marco de imagen. WIC es lo suficientemente flexible como para controlar metadatos y metadatos de nivel de marco fuera del marco individual de una imagen.

## <a name="reading-image-metadata"></a>Leer metadatos de imagen

Las API de WIC proporcionan componentes COM que facilitan a las aplicaciones la lectura y escritura de metadatos de imágenes.

La forma principal de leer los metadatos es usar un lector de consultas de metadatos ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) para tener acceso a los elementos de metadatos específicos. El códec implementa el componente lector de consultas de metadatos y se puede tener acceso a él en el nivel de descodificador o a través de fotogramas de imagen individuales, que es el método más común. En el código siguiente se muestra cómo obtener acceso a un lector de consultas para un marco individual mediante el método **GetMetadataQueryReader** del lector de consultas.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Un lector de consultas proporciona métodos para obtener información sobre metadatos específicos y un medio para especificar un elemento de metadatos que se va a recuperar. En el código siguiente se usa una expresión de consulta para solicitar un elemento de metadatos específico dentro del bloque de directorio de archivos de imagen anidada (IFD) de app1. Esto se hace mediante el método **GetMetadataByName** del lector de consultas. En el código siguiente se muestra cómo utilizar el lector de consultas para obtener el valor de clasificación MicrosoftPhoto.


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



La variable pwzRatingQuery del ejemplo anterior es la cadena de consulta para tener acceso al elemento de metadatos MicrosoftPhoto rating. Esta cadena se crea mediante el lenguaje de consulta de metadatos. Para crear esta cadena, es necesario conocer el formato de metadatos y el lenguaje de consulta de metadatos para recuperar los elementos de metadatos individuales. Para obtener más información sobre el lenguaje de consulta de metadatos, vea [información general sobre el lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md).

En segundo plano, un lector de consultas usa un lector de metadatos ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) para tener acceso a los metadatos descritos por la expresión de consulta. Además de usar un lector de consultas, también puede tener acceso a un lector de metadatos directamente para leer los metadatos. Puede obtener un lector de metadatos del descodificador o de los marcos individuales consultando una interfaz de lectura de bloques ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)).

## <a name="writing-image-metadata"></a>Escribir metadatos de imagen

El proceso de escritura de metadatos es similar a la forma en que se lee, salvo que se usa un escritor de consultas de metadatos ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)). El codificador de imágenes implementa la interfaz del escritor de consultas y, como en el lector de consultas, se tiene acceso a los metadatos tanto en el codificador como en los marcos individuales (dependiendo de la compatibilidad con el formato de imagen).

En el código siguiente se muestra cómo obtener un escritor de consultas de un marco de codificador y cómo quitar el valor de clasificación que se leyó previamente.


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



Otra manera de escribir metadatos es a través de actualizaciones rápidas de metadatos. La codificación rápida de metadatos es una manera de escribir metadatos de imagen sin tener que volver a codificar un archivo de imagen. Para ello, se escribe una nueva información de metadatos en una región rellenada del formato de metadatos. El codificador rápido de metadatos ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) se obtiene del generador de componentes, basado en el descodificador de imágenes. A continuación, el codificador de metadatos rápido obtiene un escritor de consultas que se utiliza para escribir los metadatos. Por último, el codificador rápido confirma el cambio.

En el código siguiente se muestra cómo obtener un codificador de metadatos rápido y usarlo para escribir el valor de MicrosoftRating.


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



No todos los formatos de metadatos admiten metadatos rápidos. Para ver qué formatos compatibles de forma nativa admiten la codificación rápida de metadatos, consulte la tabla de la sección [formatos de metadatos admitidos](#supported-metadata-formats) más adelante en este documento.

En segundo plano, un escritor de consultas usa un escritor de metadatos ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) para escribir los metadatos descritos por la expresión de consulta. Además de usar un lector de consultas, también puede tener acceso a un escritor de metadatos directamente para escribir metadatos. Puede obtener un escritor de metadatos del descodificador o de los fotogramas individuales mediante la consulta de una interfaz de bloqueo de bloques ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).

## <a name="metadata-extensibility"></a>Extensibilidad de metadatos

Como se mencionó anteriormente, WIC proporciona varios controladores de metadatos para leer y escribir metadatos para formatos de metadatos comunes. Sin embargo, hay algunos formatos de metadatos que no se admiten de forma nativa. Por lo tanto, WIC proporciona API para crear controladores de metadatos adicionales que pueden extender la compatibilidad de metadatos a otros formatos.

Para admitir por completo otros formatos de metadatos, se deben desarrollar dos tipos de controladores: un lector de metadatos para leer metadatos y un escritor de metadatos para escribir metadatos. Aunque estos dos controladores se suelen implementar en pares para un formato específico, no es un requisito. Puede haber algunos casos en los que solo sea necesaria la capacidad de lectura o solo la capacidad de escritura.

Para obtener más información sobre la extensibilidad de metadatos mediante las API de WIC, vea la [Introducción a la extensibilidad de metadatos](-wic-codec-metadatahandlers.md).

## <a name="supported-metadata-formats"></a>Formatos de metadatos admitidos

WIC proporciona compatibilidad con varios formatos de metadatos comunes. En la tabla siguiente se enumeran los formatos de metadatos admitidos, sus versiones, los formatos de imagen que admiten el formato de metadatos y si el formato de metadatos admite la codificación rápida de metadatos. Para obtener más información sobre la codificación rápida de metadatos, vea la sección [escribir metadatos de imagen](#writing-image-metadata) anteriormente en este documento.



| Formatos de metadatos admitidos | Versión de especificación de metadatos | Compatibilidad con formato de imagen | Admite codificación rápida de metadatos |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| App0                       | JFIF 1,02                      | JPEG                 | No                              |
| Aplicación 1                       | JFIF 1,02                      | JPEG, TIFF           | No                              |
| App13                      | Unknown                        | JPEG, TIFF           | No                              |
| IFD                        | TIFF 6,0                       | JPEG, TIFF           | Sí                             |
| IRB                        | Unknown                        | JPEG, TIFF           | No                              |
| Exif                       | EXIF 2,2                       | JPEG, TIFF           | Sí                             |
| XMP                        | XMP 1,0 (2005 de septiembre)            | JPEG, TIFF           | Sí                             |
| GPS                        | EXIF 2,2                       | JPEG, TIFF           | Sí                             |
| CREACIÓN                       | IPTC 4,0                       | JPEG, TIFF           | Sí                             |
| Negrita                       | PNG 1,2                        | PNG                  | No                              |



 

> [!Note]  
> IPTC solo admite FME si los bloques aumentan de tamaño, ya que IPTC no admite el relleno.

 

## <a name="metadata-component-summary"></a>Resumen de los componentes de metadatos

En la tabla siguiente se describen las interfaces de WIC que admiten metadatos y sus componentes correspondientes. Estos componentes proporcionan el acceso a los metadatos de una imagen. Para obtener más información acerca de estos componentes, consulte la [información general](-wic-about-windows-imaging-codec.md)sobre el componente de creación de imágenes de Windows. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Descodificador de mapa de bits (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</td>
<td><ul>
<li>Lee una secuencia de imágenes y genera un origen de mapas de bits utilizable. Asociado con un formato de contenedor como Tagged Image File Format (TIFF) o Joint Photographic Experts Group (JPEG).</li>
<li>Implementa una interfaz <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> para enumerar todos los bloques de metadatos del flujo de datos del descodificador que no están dentro de un marco.</li>
<li>Expone un lector de consultas para leer los metadatos asociados a la imagen que no está dentro de un marco.</li>
</ul></td>
</tr>
<tr class="even">
<td>Descodificación de fotogramas de mapa de bits (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</td>
<td><ul>
<li>Accede a fotogramas individuales desde el flujo de imágenes mantenido por el descodificador.</li>
<li>Implementa una interfaz <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> para enumerar todos los bloques de metadatos en el flujo de datos del marco.</li>
<li>Expone un lector de consultas para leer los metadatos asociados con el marco, mediante expresiones de consulta.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Codificador de mapa de bits (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</td>
<td><ul>
<li>Escribe un origen de mapa de bits en una secuencia de imágenes. Asociado con un formato de contenedor como TIFF o JPEG.</li>
<li>Implementa una interfaz <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> para crear una lista de bloques de metadatos que se van a escribir en el flujo de datos del codificador.</li>
<li>Expone un escritor de consultas para escribir los metadatos asociados a la imagen mediante expresiones de consulta.</li>
</ul></td>
</tr>
<tr class="even">
<td>Código de marco Bitma (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</td>
<td><ul>
<li>Crea un marco que se codificará en el flujo mantenido por el codificador.</li>
<li>Implementa una interfaz <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> para crear una lista de bloques de metadatos que se van a escribir en el flujo de datos del marco.</li>
<li>Expone un escritor de consultas para escribir los metadatos asociados con el marco, mediante expresiones de consulta.</li>
</ul></td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se describen los componentes de metadatos de WIC. Estos componentes permiten leer y escribir los metadatos en una imagen expuesta por los componentes enumerados en la tabla anterior. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lector de consultas de metadatos (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</td>
<td><ul>
<li>Toma una cadena de consulta y navega por la jerarquía de metadatos subyacentes para obtener los metadatos.</li>
</ul></td>
</tr>
<tr class="even">
<td>Escritor de consultas de metadatos (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</td>
<td><ul>
<li>Toma una cadena de consulta y navega por la jerarquía de metadatos subyacentes para obtener, establecer y quitar metadatos.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lector de bloques de metadatos (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</td>
<td><ul>
<li>Administra una colección de solo lectura de objetos <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> en la parte superior de la jerarquía de metadatos y habilita la enumeración de todos los bloques de metadatos.</li>
<li>Implementado por un descodificador de mapa de bits y un marco de mapa de bits descodificado.</li>
<li>Implementado por desarrolladores de componentes de terceros para códecs personalizados.</li>
</ul></td>
</tr>
<tr class="even">
<td>Escritor de bloques de metadatos (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</td>
<td><ul>
<li>Administra una colección de lectura y escritura de objetos <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> en la parte superior de la jerarquía de metadatos.</li>
<li>Implementado por un codificador de mapa de bits y un código de marco de mapa de bits.</li>
<li>Implementado por desarrolladores de componentes de terceros para códecs personalizados.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lector de metadatos (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</td>
<td><ul>
<li>Analiza una secuencia de metadatos y administra una colección de solo lectura de los elementos de metadatos. Asociado con un formato de metadatos como EXIF, IFD y XMP.</li>
<li>Actúa como diccionario y devuelve un valor cuando se proporciona un par de formato y identificador.</li>
<li>Implementado por desarrolladores de componentes de terceros para tipos de metadatos personalizados.</li>
</ul></td>
</tr>
<tr class="even">
<td>Escritor de metadatos (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</td>
<td><ul>
<li>Analiza y serializa una secuencia de metadatos y administra una colección de lectura/escritura de elementos de metadatos.</li>
<li>Implementado por desarrolladores de componentes de terceros para tipos de metadatos personalizados.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Codificador de metadatos rápido<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></td>
<td><ul>
<li>Expone la semántica para escribir en una jerarquía de metadatos que actualizará los metadatos en su lugar sin volver a codificar la imagen.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general del lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Información general sobre la extensibilidad de metadatos](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Cómo volver a codificar una imagen JPEG con metadatos](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



