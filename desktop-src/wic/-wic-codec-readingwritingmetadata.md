---
description: En este tema se proporciona información general sobre cómo puede usar las API de Windows Imaging Component (WIC) para leer y escribir metadatos insertados en archivos de imagen.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Información general sobre la lectura y escritura de metadatos de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 484d562b71184c20adf054f1de2a4203878da9b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359621"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a>Información general sobre la lectura y escritura de metadatos de imagen

En este tema se proporciona información general sobre cómo puede usar las API de Windows Imaging Component (WIC) para leer y escribir metadatos insertados en archivos de imagen.

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Introducción](#introduction)
-   [Lectura de metadatos mediante un lector de consultas](#reading-metadadata-using-a-query-reader)
    -   [Obtener un lector de consultas](#obtaining-a-query-reader)
    -   [Leer metadatos](#reading-metadata)
    -   [Métodos de lector de consultas adicionales](#additional-query-reader-methods)
-   [Escribir metadatos mediante un escritor de consultas](#writing-metadata-using-a-query-writer)
    -   [Obtener un escritor de consultas](#obtaining-a-query-writer)
    -   [Agregar metadatos](#adding-metadata)
    -   [Quitar metadatos](#removing-metadata)
    -   [Copiar metadatos para volver a codificar](#copying-metadata-for-re-encoding)
-   [Codificación rápida de metadatos](#fast-metadata-encoding)
    -   [Agregar relleno a bloques de metadatos](#adding-padding-to-metadata-blocks)
    -   [Obtener un codificador de metadatos rápido](#obtaining-a-fast-metadata-encoder)
    -   [Uso del codificador de metadatos rápido](#using-the-fast-metadata-encoder)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

Para comprender este tema, debe estar familiarizado con el sistema de metadatos de WIC, como se describe en Información general sobre los [metadatos de WIC.](-wic-about-metadata.md) También debe estar familiarizado con el lenguaje de consulta que se usa para leer y escribir metadatos, como se describe en Información general del lenguaje [de consulta de metadatos](-wic-codec-metadataquerylanguage.md).

## <a name="introduction"></a>Introducción

WIC proporciona a los desarrolladores de aplicaciones componentes del Modelo de objetos componentes (COM) para leer y escribir metadatos insertados en archivos de imagen. Hay dos maneras de leer y escribir metadatos:

-   Usar un lector o escritor de consultas y una expresión de consulta para consultar bloques de metadatos para bloques anidados o metadatos específicos dentro de un bloque.
-   Usar un controlador de metadatos (un lector de metadatos o un escritor de metadatos) para acceder a los bloques de metadatos anidados o metadatos específicos dentro de los bloques de metadatos.

La más fácil de ellas es usar un lector o escritor de consultas y una expresión de consulta para acceder a los metadatos. Un lector de consultas [**(IWICMetadataQueryReader)**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)se usa para leer metadatos mientras que un escritor de consultas [**(IWICMetadataQueryWriter)**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)se usa para escribir metadatos. Ambos usan una expresión de consulta para leer o escribir los metadatos deseados. En segundo plano, un lector de consultas (y escritor) usa un controlador de metadatos para acceder a los metadatos descritos por la expresión de consulta.

El método más avanzado consiste en acceder directamente a los controladores de metadatos. Se obtiene un controlador de metadatos de los fotogramas individuales mediante un lector de bloques [**(IWICMetadataBlockReader)**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)o un escritor de bloques ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)). Los dos tipos de controladores de metadatos disponibles son el lector de metadatos ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) y el escritor de metadatos ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).

En los ejemplos de este tema se usa el siguiente diagrama del contenido de un archivo de imagen JPEG. La imagen representada por este diagrama se creó mediante Microsoft Paint; los metadatos de clasificación se agregaron mediante la característica Galería de fotos de Windows Vista.

![ilustración de imagen jpeg con metadatos de clasificación](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a>Lectura de metadatos mediante un lector de consultas

La manera más fácil de leer metadatos es usar la interfaz del lector de consultas, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader). El lector de consultas permite leer bloques de metadatos y elementos dentro de bloques de metadatos mediante una expresión de consulta.

Hay tres maneras de obtener un lector de consultas: a través de un descodificador de mapa de bits [**(IWICBitmapDecoder),**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)a través de sus marcos individuales [**(IWICBitmapFrameDecode)**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)o a través de un escritor de consultas ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).

### <a name="obtaining-a-query-reader"></a>Obtener un lector de consultas

El código de ejemplo siguiente muestra cómo obtener un descodificador de mapa de bits del generador de imágenes y recuperar un marco de mapa de bits individual. Este código también realiza el trabajo de configuración necesario para obtener un lector de consultas a partir de un marco descodificado.


```
IWICImagingFactory *pFactory = NULL;
IWICBitmapDecoder *pDecoder = NULL;
IWICBitmapFrameDecode *pFrameDecode = NULL;
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pEmbedReader = NULL;
PROPVARIANT value;

// Initialize COM
CoInitialize(NULL);

// Initialize PROPVARIANT
PropVariantInit(&value);

//Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_IWICImagingFactory,
    (LPVOID*)&pFactory);

// Create the decoder
if (SUCCEEDED(hr))
{
    hr = pFactory->CreateDecoderFromFilename(
        L"test.jpg",
        NULL,
        GENERIC_READ,
        WICDecodeMetadataCacheOnDemand,
        &pDecoder);
}

// Get a single frame from the image
if (SUCCEEDED(hr))
{
    hr = pDecoder->GetFrame(
         0,  //JPEG has only one frame.
         &pFrameDecode); 
}
```



El descodificador de mapa de bits test.jpg archivo se obtiene mediante el método **CreateDecoderFromFilename** del generador de imágenes. En este método, el cuarto parámetro se establece en el valor WICDecodeMetadataCacheOnDemand de la [**enumeración WICDecodeOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) Esto indica al descodificador que almacena en caché los metadatos cuando se necesitan los metadatos. mediante la obtención de un lector de consultas o el lector de metadatos subyacente. El uso de esta opción le permite conservar la secuencia de los metadatos necesarios para la codificación rápida de metadatos y permite la codificación sin pérdida de la imagen JPEG. Como alternativa, podría usar el otro valor **de WICDecodeOptions,** WICDecodeMetadataCacheOnLoad, que almacena en caché los metadatos de la imagen incrustada en cuanto se carga la imagen.

Para obtener el lector de consultas del marco, realice una llamada sencilla al método **GetMetadataQueryReader del** marco. El código siguiente muestra esta llamada.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



De forma similar, también se puede obtener un lector de consultas en el nivel de descodificador. Una llamada simple al método **GetMetadataQueryReader** del descodificador obtiene el lector de consultas del descodificador. El lector de consultas de un descodificador, a diferencia del lector de consultas de un marco, lee los metadatos de una imagen que está fuera de los fotogramas individuales. Sin embargo, este escenario no es común y los formatos de imagen nativa no admiten esta funcionalidad. Los CÓDECS de imagen nativa proporcionados por WIC leen y escriben metadatos en el nivel de fotograma incluso para formatos de fotograma único, como JPEG.

### <a name="reading-metadata"></a>Leer metadatos

Antes de pasar a leer realmente los metadatos, vea el siguiente diagrama de un archivo JPEG que incluye bloques de metadatos incrustados y datos reales para recuperar. En este diagrama se proporcionan llamadas a bloques de metadatos y elementos específicos dentro de la imagen que proporcionan la expresión de consulta de metadatos a cada bloque o elemento.

![ilustración de la imagen jpeg con llamadas de metadatos](graphics/jpegwithcallouts.png)

Para consultar bloques de metadatos incrustados o elementos específicos por nombre, llame al **método GetMetadataByName.** Este método toma una expresión de consulta y [propVARIANT en](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) la que se devuelve el elemento de metadatos. El código siguiente consulta un bloque de metadatos anidado y convierte el componente [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) proporcionado por el valor PROPVARIANT en un lector de consultas si se encuentra.


```
if (SUCCEEDED(hr))
{
    // Get the nested IFD reader
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pEmbedReader);
    }
    PropVariantClear(&value); // Clear value for new query
}
```



La expresión de consulta "/app1/ifd" está consultando el bloque IFD anidado en el bloque App1. El archivo de imagen JPEG contiene el bloque de metadatos anidados IFD, por lo que [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) se devuelve con un tipo de variable (vt) de y un puntero a una `VT_UNKNOWN` [interfaz IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) (val). A continuación, consulte la interfaz IUnknown para un lector de consultas.

El código siguiente muestra una nueva consulta basada en el nuevo lector de consultas con respecto al bloque IFD anidado.


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



La expresión de consulta "/{ushort=18249}" consulta el bloque IFD para la clasificación MicrosoftPhoto incrustada en la etiqueta 18249. El [valor PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) ahora contendrá un tipo de valor de `VT_UI2` y un valor de datos de 50.

Sin embargo, no es necesario obtener un bloque anidado antes de consultar valores de datos específicos. Por ejemplo, en lugar de consultar el IFD anidado y, a continuación, para la clasificación MicrosoftPhoto, puede usar en su lugar el bloque de metadatos raíz y la consulta que se muestra en el código siguiente para obtener la misma información.


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



Además de consultar elementos de metadatos específicos en un bloque de metadatos, también puede enumerar todos los elementos de metadatos de un bloque de metadatos (sin incluir elementos de metadatos en bloques de metadatos anidados). Para enumerar los elementos de metadatos del bloque actual, se usa el **método GetEnumeration del** lector de consultas. Este método obtiene una interfaz **IEnumString** rellenada con los elementos de metadatos del bloque actual. Por ejemplo, el código siguiente enumera la clasificación XMP y la clasificación MicrosoftPhoto para el bloque IFD anidado que se obtuvo anteriormente.


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



Para obtener más información sobre cómo identificar etiquetas adecuadas para varios formatos de imagen y formatos de metadatos, vea [Consultas de metadatos de](-wic-native-image-format-metadata-queries.md)formato de imagen nativa.

### <a name="additional-query-reader-methods"></a>Métodos de lector de consultas adicionales

Además de leer metadatos, también puede obtener información adicional sobre el lector de consultas y obtener metadatos a través de otros medios. El lector de consultas proporciona dos métodos que proporcionan información sobre el lector de consultas, **GetContainerFormat** y **GetLocation**.

Con el lector de consultas incrustado, puede usar **GetContainerFormat** para determinar el tipo de bloque de metadatos y puede llamar a **GetLocation** para obtener la ruta de acceso relativa al bloque de metadatos raíz. El código siguiente consulta su ubicación al lector de consultas incrustado.


```
// Determine the metadata block format

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetContainerFormat(&containerGUID);
}

// Determine the query reader's location
if (SUCCEEDED(hr))
{
    UINT length;
    WCHAR readerNamespace[100];
    hr = pEmbedReader->GetLocation(100, readerNamespace, &length);
}
```



La llamada a **GetContainerFormat para** el lector de consultas incrustadas devuelve el GUID de formato de metadatos IFD. La llamada a **GetLocation** devuelve un espacio de nombres de "/app1/ifd"; proporciona la ruta de acceso relativa desde la que se ejecutarán las consultas posteriores al nuevo lector de consultas. Por supuesto, el código anterior no es muy útil, pero muestra cómo usar el **método GetLocation** para buscar bloques de metadatos anidados.

## <a name="writing-metadata-using-a-query-writer"></a>Escribir metadatos mediante un escritor de consultas

> [!Note]  
> Algunos de los ejemplos de código proporcionados en esta sección no se muestran en el contexto de los pasos reales necesarios para escribir metadatos. Para ver los ejemplos de código en el contexto de un ejemplo de trabajo, consulte el tutorial Cómo: Volver a codificar una imagen con metadatos.

 

El componente principal para escribir metadatos es el escritor de consultas ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)). El escritor de consultas permite establecer y quitar bloques de metadatos y elementos dentro de un bloque de metadatos.

Al igual que el lector de consultas, hay tres maneras de obtener un escritor de consultas: a través de un codificador de mapa de bits [**(IWICBitmapEncoder),**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)a través de sus fotogramas individuales [**(IWICBitmapFrameEncode)**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)o a través de un codificador de metadatos rápido [**(IWICFastMetadataEncoder).**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)

### <a name="obtaining-a-query-writer"></a>Obtener un escritor de consultas

El escritor de consultas más común es para un fotograma individual de un mapa de bits. Este escritor de consultas establece y quita los bloques y elementos de metadatos de un marco de imagen. Para obtener el escritor de consultas de un marco de imagen, llame al **método GetMetadataQueryWriter del** marco. En el código siguiente se muestra la llamada al método simple para obtener el escritor de consultas de un marco.


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



De forma similar, también se puede obtener un escritor de consultas para el nivel de codificador. Una llamada simple al método **GetMetadataQueryWriter** del codificador obtiene el escritor de consultas del codificador. El escritor de consultas de un codificador, a diferencia del escritor de consultas de un fotograma, escribe metadatos para una imagen fuera del marco individual. Sin embargo, este escenario no es común y los formatos de imagen nativa no admiten esta funcionalidad. Los códecs de imagen nativos proporcionados por WIC leen y escriben metadatos en el nivel de fotograma incluso para formatos de fotograma único, como JPEG.

También puede obtener un escritor de consultas directamente desde el generador de imágenes ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)). Hay dos métodos de generador de imágenes que devuelven un escritor de consultas: **CreateQueryWriter** y **CreateQueryWriterFromReader.**

**CreateQueryWriter crea** un escritor de consultas para el proveedor y el formato de metadatos especificados. Este escritor de consultas permite escribir metadatos para un formato de metadatos específico y agregarlos a la imagen. En el código siguiente se muestra una **llamada CreateQueryWriter** para crear un escritor de consultas XMP.


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



En este ejemplo, el nombre descriptivo `GUID_MetadataFormatXMP` se usa como parámetro *guidMetadataFormat.* Representa el GUID del formato de metadatos XMP y el proveedor representa el controlador creado por Microsoft. Como alternativa, **se puede** pasar NULL como parámetro *pguidVendor* con los mismos resultados si no existe ningún otro controlador XMP. Si se instala un controlador XMP personalizado junto con el controlador XMP nativo, si se pasa **NULL** para el proveedor, se devolverá el escritor de consultas con el GUID más bajo.

**CreateQueryWriterFromReader** es similar al método **CreateQueryWriter,** salvo que rellenará previamente el nuevo escritor de consultas con los datos proporcionados por el lector de consultas. Esto es útil para volver a codificar una imagen mientras se mantienen los metadatos existentes o para quitar metadatos no deseados. El código siguiente muestra una **llamada a CreateQueryWriterFromReader.**


```
hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

// Copy metadata using query readers
if(SUCCEEDED(hr) && pFrameQReader)
{
    IWICMetadataQueryWriter *pNewWriter = NULL;

    GUID vendor = GUID_VendorMicrosoft;
    hr = pFactory->CreateQueryWriterFromReader(
        pFrameQReader,
        &vendor,
        &pNewWriter);
```



### <a name="adding-metadata"></a>Agregar metadatos

Después de obtener un escritor de consultas, puede usarlo para agregar bloques de metadatos y elementos. Para escribir metadatos, use el método **SetMetadataByName** del escritor de consultas. **SetMetadataByName toma** dos parámetros: una expresión de consulta (*wzName*) y un puntero a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*). La expresión de consulta define el bloque o elemento que se debe establecer, mientras que PROPVARIANT proporciona el valor de datos real que se debe establecer.

En el ejemplo siguiente se muestra cómo agregar un título mediante el escritor de consultas XMP obtenido previamente mediante el **método CreateQueryWriter.**


```
// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
   
    hr = pXMPWriter->SetMetadataByName(L"/dc:title", &value);

    PropVariantClear(&value);
}
```



En este ejemplo, el tipo de valor (vt) se establece en , lo que indica que se usará una cadena `VT_LPWSTR` como valor de datos. Dado *que* el tipo del valor es una cadena, *pwszVal* se usa para establecer el título que se va a usar. A continuación, se llama a **SetMetadataByName** mediante la expresión de consulta "/dc:title" y el [recién establecido PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). La expresión de consulta usada indica que se debe establecer la propiedad title en el esquema de la cámara digital (dc). Tenga en cuenta que la expresión no es "/xmp/dc:title"; Esto se debe a que el escritor de consultas ya es específico de XMP y no contiene un bloque XMP incrustado, lo que sugeriría "/xmp/dc:title".

Hasta este momento no ha agregado metadatos a un marco de imagen. Simplemente ha rellenado un escritor de consultas con datos. Para agregar a un marco un bloque de metadatos representado por el escritor de consultas, llame de nuevo a **SetMetadataByName** mediante el escritor de consultas como valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Esto copia eficazmente los metadatos del escritor de consultas en el marco de la imagen. En el código siguiente se muestra cómo agregar los metadatos del escritor de consultas XMP obtenidos previamente al bloque de metadatos raíz de un marco.


```
// Get the frame's query writer and write the XMP query writer to it
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);

    // Copy the metadata in the XMP query writer to the frame
    if (SUCCEEDED(hr))
    {
        PROPVARIANT value;

        PropVariantInit(&value);
        value.vt = VT_UNKNOWN;
        value.punkVal = pXMPWriter;
        value.punkVal->AddRef();

        hr = pFrameQWriter->SetMetadataByName(L"/", &value);

        PropVariantClear(&value);
    }
}
```



En este ejemplo, se usa un tipo de valor (vt) de `VT_UNKOWN` , que indica un tipo de valor de interfaz COM. A continuación, se usa el escritor de consultas XMP (piXMPWriter) como valor de [PROPVARIANT,](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)agregando una referencia a él mediante el método AddRef. Por último, el escritor de consultas XMP se establece llamando al método **SetMetadataByName** del marco y pasando la expresión de consulta "/", que indica el bloque raíz y el propVARIANT recién establecido.

> [!Note]  
> Si el marco ya contiene el bloque de metadatos que está intentando agregar, se agregarán los metadatos que agregue y se sobrescribirán los metadatos existentes.

 

### <a name="removing-metadata"></a>Quitar metadatos

Un escritor de consultas también permite quitar metadatos mediante una llamada al **método RemoveMetadataByName.** **RemoveMetadataByName toma** una expresión de consulta y quita el bloque o elemento de metadatos si existe. En el código siguiente se muestra cómo quitar el título que se agregó anteriormente.


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



En el código siguiente se muestra cómo quitar todo el bloque de metadatos XMP.


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a>Copiar metadatos para volver a codificar

> [!Note]  
> El código de esta sección solo es válido cuando los formatos de imagen de origen y destino son los mismos. No se pueden copiar todos los metadatos de una imagen en una sola operación al codificar en un formato de imagen diferente.

 

Para conservar los metadatos al volver a codificar una imagen en el mismo formato de imagen, hay métodos disponibles para copiar todos los metadatos en una sola operación. Cada una de estas operaciones sigue un patrón similar; cada establece los metadatos del marco descodificado directamente en el nuevo marco que se va a codificar.

El método preferido para copiar metadatos es inicializar el escritor de bloques del nuevo marco con el lector de bloques del marco descodificado. En el código siguiente se muestra este método.


```
if (SUCCEEDED(hr) && formatsEqual)
{
    // Copy metadata using metadata block reader/writer
    if (SUCCEEDED(hr))
    {
        pFrameDecode->QueryInterface(
            IID_IWICMetadataBlockReader,
            (void**)&pBlockReader);
    }
    if (SUCCEEDED(hr))
    {
        pFrameEncode->QueryInterface(
            IID_IWICMetadataBlockWriter,
            (void**)&pBlockWriter);
    }
    if (SUCCEEDED(hr))
    {
        pBlockWriter->InitializeFromBlockReader(pBlockReader);
    }
}
```



En este ejemplo, el lector de bloques y el escritor de bloques se obtienen del marco de origen y del marco de destino, respectivamente. A continuación, el escritor de bloques se inicializa desde el lector de bloques. Esto inicializa el lector de bloques con los metadatos rellenados previamente del lector de bloques.

Otro método para copiar metadatos es escribir el bloque de metadatos al que hace referencia el lector de consultas mediante el escritor de consultas del codificador. En el código siguiente se muestra este método.


```
if (SUCCEEDED(hr) && formatsEqual)
{
    hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

    // Copy metadata using query readers
    if(SUCCEEDED(hr))
    {
        hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
        if (SUCCEEDED(hr))
        {
            PropVariantClear(&value);
            value.vt=VT_UNKNOWN;
            value.punkVal=pFrameQReader;
            value.punkVal->AddRef();
            hr = pFrameQWriter->SetMetadataByName(L"/", &value);
            PropVariantClear(&value);
        }
    }
}
```



En este caso, se obtiene un lector de consultas del marco descodificado y, a continuación, se usa como valor de propiedad de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) con un tipo de valor establecido en VT \_ UNKNOWN. Se obtiene el escritor de consultas para el codificador y se usa la expresión de consulta "/" para establecer los metadatos en la ruta de navegación raíz. También puede usar este método al establecer bloques de metadatos anidados ajustando la expresión de consulta a la ubicación deseada.

De forma similar, puede crear un escritor de consultas basado en el lector de consultas del marco descodificado mediante el método **CreateQueryWriterFromReader** de la factoría de imágenes. El escritor de consultas creado en esta operación se volverá a poblar con los metadatos del lector de consultas y, a continuación, se podrá establecer en el marco. En el código siguiente se muestra **la operación de copia CreateQueryWriterFromReader.**


```
IWICMetadataQueryWriter *pNewWriter = NULL;

GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriterFromReader(
    pFrameQReader,
    &vendor,
    &pNewWriter);

if (SUCCEEDED(hr))
{
    // Get the frame's query writer
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

// Set the query writer to the frame.
if (SUCCEEDED(hr))
{
    PROPVARIANT value;

    PropVariantInit(&value);
    value.vt = VT_UNKNOWN;
    value.punkVal = pNewWriter;
    value.punkVal->AddRef();
    hr = pFrameQWriter->SetMetadataByName(L"/",&value);
}
```



Este método usa un escritor de consultas independiente que se basa en los datos del lector de consultas. A continuación, este nuevo escritor de consultas se establece en el marco.

De nuevo, estas operaciones para copiar metadatos solo funcionan cuando las imágenes de origen y destino tienen el mismo formato. Esto se debe a que diferentes formatos de imagen almacenan los bloques de metadatos en ubicaciones diferentes. Por ejemplo, JPEG y TIFF admiten bloques de metadatos XMP. En imágenes JPEG, el bloque XMP se encuentra en el bloque de metadatos raíz, como se muestra en información general sobre metadatos [de WIC.](-wic-about-metadata.md) Sin embargo, en una imagen TIFF, el bloque XMP se anida en un bloque IFD raíz. En el diagrama siguiente se muestran las diferencias entre una imagen JPEG y una imagen TIFF con los mismos metadatos de clasificación.

![Comparación jpeg y tiff.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a>Codificación rápida de metadatos

No siempre es necesario volver a codificar una imagen para escribir nuevos metadatos en ella. Los metadatos también se pueden escribir mediante un codificador de metadatos rápido. Un codificador de metadatos rápido puede escribir una cantidad limitada de metadatos en una imagen sin volver a codificar la imagen. Esto se logra escribiendo los nuevos metadatos dentro del relleno vacío proporcionado por algunos formatos de metadatos. Los formatos de metadatos nativos que admiten el relleno de metadatos son Exif, IFD, GPS y XMP.

### <a name="adding-padding-to-metadata-blocks"></a>Agregar relleno a bloques de metadatos

Para poder realizar una codificación rápida de metadatos, debe haber espacio dentro del bloque de metadatos para escribir más metadatos. Si no hay suficiente espacio dentro del relleno existente para escribir los nuevos metadatos, se producirá un error en la codificación rápida de metadatos. Para agregar relleno de metadatos a una imagen, se debe volver a codificar la imagen. Puede agregar relleno de la misma manera que agregaría cualquier otro elemento de metadatos, mediante una expresión de consulta, si el bloque de metadatos que va a rellenar lo admite. En el ejemplo siguiente se muestra cómo agregar relleno a un bloque IFD incrustado en un bloque App1.


```
if (SUCCEEDED(hr))
{
    // Add metadata padding
    PROPVARIANT padding;

    PropVariantInit(&padding);
    padding.vt = VT_UI4;
    padding.uiVal = 4096; // 4KB

    hr = pFrameQWriter->SetMetadataByName(L"/app1/ifd/PaddingSchema:padding", &padding);

    PropVariantClear(&padding);
}
```



Para agregar relleno, cree un PROPVARIANT de tipo VT UI4 y un valor correspondiente al número de bytes de relleno que se \_ agregarán. Un valor típico es 4096 bytes. Las consultas de metadatos de JPEG, TIFF y JPEG-XR se encuentran en esta tabla.



| Formato de metadatos | Consulta de metadatos JPEG                  | Consulta de metadatos TIFF, JPEG-XR    |
|-----------------|--------------------------------------|---------------------------------|
| IFD             | /app1/ifd/PaddingSchema:Padding      | /ifd/PaddingSchema:Padding      |
| EXIF            | /app1/ifd/exif/PaddingSchema:Padding | /ifd/exif/PaddingSchema:Padding |
| XMP             | /xmp/PaddingSchema:Padding           | /ifd/xmp/PaddingSchema:Padding  |
| GPS             | /app1/ifd/gps/PaddingSchema:Padding  | /ifd/gps/PaddingSchema:Padding  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a>Obtención de un codificador de metadatos rápido

Cuando tiene una imagen con relleno de metadatos, se puede obtener un codificador de metadatos rápido mediante los métodos de generador de imágenes **CreateFastMetadataEncoderFromDecoder** y **CreateFastMetadataEncoderFromFrameDecode**.

Como su nombre indica, **CreateFastMetadataEncoderFromDecoder** crea un codificador de metadatos rápido para metadatos de nivel de descodificador. Los formatos de imagen nativos proporcionados por WIC no admiten metadatos de nivel de descodificador, pero este método se proporciona en caso de que este formato de imagen se desarrollara en el futuro.

El escenario más común es obtener un codificador de metadatos rápido de un marco de imagen mediante **CreateFastMetadataEncoderFromFrameDecode**. El código siguiente obtiene el codificador de metadatos rápido de un marco descodificado y cambia el valor de clasificación en el bloque App1.


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode, 
        &pFME);
}
```



### <a name="using-the-fast-metadata-encoder"></a>Uso del codificador de metadatos rápido

Desde el codificador de metadatos rápido, puede obtener un escritor de consultas. Esto le permite escribir metadatos mediante una expresión de consulta como se ha mostrado anteriormente. Una vez establecidos los metadatos en el escritor de consultas, confirme el codificador de metadatos rápido para finalizar la actualización de metadatos. En el código siguiente se muestra cómo establecer y confirmar los cambios de metadatos


```
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



Si **se** produce un error de confirmación por cualquier motivo, deberá volver a codificar la imagen para asegurarse de que los nuevos metadatos se agregan a la imagen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Introducción a los metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general sobre el lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Información general sobre extensibilidad de metadatos](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Cómo: Volver a codificar una imagen JPEG con metadatos](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
