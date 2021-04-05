---
description: En este tema se proporciona información general sobre cómo se pueden usar las API de Windows Imaging Component (WIC) para leer y escribir metadatos que se incrustan en archivos de imagen.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Información general sobre la lectura y escritura de metadatos de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 484d562b71184c20adf054f1de2a4203878da9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002157"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a>Información general sobre la lectura y escritura de metadatos de imagen

En este tema se proporciona información general sobre cómo se pueden usar las API de Windows Imaging Component (WIC) para leer y escribir metadatos que se incrustan en archivos de imagen.

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Introducción](#introduction)
-   [Lectura de Metadadata con un lector de consultas](#reading-metadadata-using-a-query-reader)
    -   [Obtener un lector de consultas](#obtaining-a-query-reader)
    -   [Leer metadatos](#reading-metadata)
    -   [Métodos de lectura de consulta adicionales](#additional-query-reader-methods)
-   [Escribir metadatos mediante un escritor de consultas](#writing-metadata-using-a-query-writer)
    -   [Obtener un escritor de consultas](#obtaining-a-query-writer)
    -   [Agregar metadatos](#adding-metadata)
    -   [Quitar metadatos](#removing-metadata)
    -   [Copia de metadatos para la recodificación](#copying-metadata-for-re-encoding)
-   [Codificación rápida de metadatos](#fast-metadata-encoding)
    -   [Agregar relleno a bloques de metadatos](#adding-padding-to-metadata-blocks)
    -   [Obtención de un codificador de metadatos rápido](#obtaining-a-fast-metadata-encoder)
    -   [Usar el codificador de metadatos rápidos](#using-the-fast-metadata-encoder)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

Para entender este tema, debe estar familiarizado con el sistema de metadatos de WIC tal y como se describe en [información general sobre metadatos de WIC](-wic-about-metadata.md). También debe estar familiarizado con el lenguaje de consulta que se usa para leer y escribir metadatos, como se describe en [información general sobre el lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md).

## <a name="introduction"></a>Introducción

WIC proporciona a los desarrolladores de aplicaciones los componentes del modelo de objetos componentes (COM) para leer y escribir metadatos incrustados en archivos de imagen. Hay dos maneras de leer y escribir metadatos:

-   Usar un lector/escritor de consultas y una expresión de consulta para consultar bloques de metadatos para bloques anidados o metadatos específicos dentro de un bloque.
-   Usar un controlador de metadatos (un lector de metadatos o un escritor de metadatos) para tener acceso a los bloques de metadatos anidados o a metadatos específicos dentro de los bloques de metadatos.

Lo más sencillo es usar un lector/escritor de consultas y una expresión de consulta para tener acceso a los metadatos. Un lector de consultas ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) se usa para leer los metadatos mientras se utiliza un escritor de consultas ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) para escribir los metadatos. Ambos usan una expresión de consulta para leer o escribir los metadatos deseados. En segundo plano, un lector de consultas (y escritor) usa un controlador de metadatos para tener acceso a los metadatos descritos por la expresión de consulta.

El método más avanzado es acceder directamente a los controladores de metadatos. Un controlador de metadatos se obtiene de los marcos individuales mediante un lector de bloques ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) o un escritor de bloques ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)). Los dos tipos de controladores de metadatos disponibles son el lector de metadatos ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) y el escritor de metadatos ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).

El siguiente diagrama del contenido de un archivo de imagen JPEG se usa en los ejemplos de este tema. La imagen representada por este diagrama se creó con Microsoft Paint; los metadatos de clasificación se agregaron mediante la característica de la Galería fotográfica de Windows Vista.

![Ilustración de una imagen JPEG con metadatos de clasificación](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a>Lectura de Metadadata con un lector de consultas

La manera más sencilla de leer los metadatos es usar la interfaz del lector de consultas, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader). El lector de consultas permite leer bloques de metadatos y elementos dentro de bloques de metadatos mediante una expresión de consulta.

Hay tres maneras de obtener un lector de consultas: a través de un descodificador de mapa de bits ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), a través de sus marcos individuales ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) o a través de un escritor de consultas ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).

### <a name="obtaining-a-query-reader"></a>Obtener un lector de consultas

En el ejemplo de código siguiente se muestra cómo obtener un descodificador de mapa de bits de la factoría de imágenes y recuperar un marco de mapa de bits individual. Este código también realiza el trabajo de configuración necesario para obtener un lector de consultas de un marco descodificado.


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



El descodificador de mapa de bits para el archivo test.jpg se obtiene mediante el método **CreateDecoderFromFilename** de la factoría de imágenes. En este método, el cuarto parámetro se establece en el valor WICDecodeMetadataCacheOnDemand de la enumeración [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) . Esto indica al descodificador que almacene en caché los metadatos cuando se necesitan los metadatos; ya sea mediante la obtención de un lector de consultas o el lector de metadatos subyacente. El uso de esta opción permite conservar la secuencia en los metadatos necesarios para la codificación rápida de los metadatos y permite la descodificación sin pérdida de la imagen JPEG. Como alternativa, puede usar el otro valor de **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, que almacena en memoria caché los metadatos de la imagen incrustada en cuanto se carga la imagen.

Para obtener el lector de consultas del marco, realice una llamada simple al método **GetMetadataQueryReader** del marco. En el código siguiente se muestra esta llamada.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Del mismo modo, también se puede obtener un lector de consultas en el nivel de descodificador. Una llamada simple al método **GetMetadataQueryReader** del descodificador obtiene el lector de consultas del descodificador. Un lector de consultas del descodificador, a diferencia del lector de consultas de un fotograma, Lee los metadatos de una imagen que está fuera de los fotogramas individuales. Sin embargo, este escenario no es común y los formatos de imagen nativa no admiten esta funcionalidad. Los CÓDECs de imagen nativa proporcionados por WIC leen y escriben metadatos en el nivel de marco incluso en los formatos de un solo fotograma, como JPEG.

### <a name="reading-metadata"></a>Leer metadatos

Antes de continuar para leer los metadatos, examine el siguiente diagrama de un archivo JPEG que incluye los bloques de metadatos insertados y los datos reales que se van a recuperar. Este diagrama proporciona llamadas a bloques de metadatos específicos y elementos dentro de la imagen que proporcionan la expresión de consulta de metadatos a cada bloque o elemento.

![Ilustración de una imagen JPEG con llamadas de metadatos](graphics/jpegwithcallouts.png)

Para consultar bloques de metadatos incrustados o elementos específicos por nombre, llame al método **GetMetadataByName** . Este método toma una expresión de consulta y una [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en la que se devuelve el elemento de metadatos. En el código siguiente se consulta un bloque de metadatos anidado y se convierte el componente [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) proporcionado por el valor PROPVARIANT en un lector de consultas, si se encuentra.


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



La expresión de consulta "/app1/IFD" está consultando el bloque IFD anidado en el bloque app1. El archivo de imagen JPEG contiene el bloque de metadatos anidado IFD, por lo que el [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) se devuelve con un tipo de variable (VT) de `VT_UNKNOWN` y un puntero a una interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) (punkVal). A continuación, se consulta la interfaz IUnknown para un lector de consultas.

En el código siguiente se muestra una nueva consulta basada en el nuevo lector de consultas en relación con el bloque IFD anidado.


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



La expresión de consulta "/{ushort = 18249}" consulta el bloque IFD para la clasificación MicrosoftPhoto incrustada en la etiqueta 18249. El valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) contendrá ahora un tipo de valor de `VT_UI2` y un valor de datos de 50.

Sin embargo, no es necesario obtener un bloque anidado antes de consultar valores de datos específicos. Por ejemplo, en lugar de consultar el IFD anidado y, a continuación, para la clasificación de MicrosoftPhoto, puede usar en su lugar el bloque de metadatos raíz y la consulta que se muestra en el código siguiente para obtener la misma información.


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



Además de consultar elementos de metadatos específicos en un bloque de metadatos, también puede enumerar todos los elementos de metadatos en un bloque de metadatos (sin incluir elementos de metadatos en bloques de metadatos anidados). Para enumerar los elementos de metadatos en el bloque actual, se usa el método **GetEnumeration** del lector de consultas. Este método obtiene una interfaz **IEnumString** rellenada con los elementos de metadatos del bloque actual. Por ejemplo, el código siguiente enumera la clasificación XMP y la clasificación MicrosoftPhoto para el bloque IFD anidado que se obtuvo anteriormente.


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



Para obtener más información sobre cómo identificar etiquetas adecuadas para los distintos formatos de imagen y formatos de metadatos, vea [consultas de metadatos de formato de imagen nativa](-wic-native-image-format-metadata-queries.md).

### <a name="additional-query-reader-methods"></a>Métodos de lectura de consulta adicionales

Además de leer los metadatos, también puede obtener información adicional sobre el lector de consultas y obtener los metadatos a través de otros medios. El lector de consultas proporciona dos métodos que proporcionan información sobre el lector de consultas, **GetContainerFormat** y **GetLocation**.

Con el lector de consultas incrustado, puede usar **GetContainerFormat** para determinar el tipo de bloque de metadatos, y puede llamar a **GetLocation** para obtener la ruta de acceso relativa al bloque de metadatos raíz. El código siguiente consulta el lector de consultas incrustado para su ubicación.


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



La llamada a **GetContainerFormat** para el lector de consultas incrustadas devuelve el GUID del formato de metadatos de IFD. La llamada a **GetLocation** devuelve un espacio de nombres de "/app1/IFD"; proporcionar la ruta de acceso relativa desde la que se ejecutarán las consultas posteriores al nuevo lector de consultas. Por supuesto, el código anterior no es muy útil, pero muestra cómo usar el método **GetLocation** para buscar bloques de metadatos anidados.

## <a name="writing-metadata-using-a-query-writer"></a>Escribir metadatos mediante un escritor de consultas

> [!Note]  
> Algunos de los ejemplos de código proporcionados en esta sección no se muestran en el contexto de los pasos reales necesarios para escribir metadatos. Para ver los ejemplos de código en el contexto de un ejemplo de trabajo, vea el tutorial sobre cómo volver a codificar una imagen con metadatos.

 

El componente principal para escribir metadatos es el escritor de consultas ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)). El escritor de consultas permite establecer y quitar bloques de metadatos y elementos dentro de un bloque de metadatos.

Al igual que el lector de consultas, hay tres maneras de obtener un escritor de consultas: a través de un codificador de mapa de bits ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), a través de sus marcos individuales ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) o a través de un codificador de metadatos rápido ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).

### <a name="obtaining-a-query-writer"></a>Obtener un escritor de consultas

El escritor de consultas más común es para un marco individual de un mapa de bits. Este escritor de consultas establece y quita los elementos y bloques de metadatos de un fotograma de imagen. Para obtener el escritor de consultas de un fotograma de imagen, llame al método **GetMetadataQueryWriter** del marco. En el código siguiente se muestra la llamada al método simple para obtener el escritor de consultas de un marco.


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



Del mismo modo, también se puede obtener un escritor de consultas para el nivel de codificador. Una llamada simple al método **GetMetadataQueryWriter** del codificador obtiene el escritor de consultas del codificador. El escritor de consultas de un codificador, a diferencia del escritor de consultas de un fotograma, escribe los metadatos de una imagen fuera del fotograma individual. Sin embargo, este escenario no es común y los formatos de imagen nativa no admiten esta funcionalidad. Los códecs de imagen nativa proporcionados por WIC leen y escriben metadatos en el nivel de marco incluso en los formatos de un solo fotograma, como JPEG.

También puede obtener un escritor de consultas directamente desde el generador de imágenes ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)). Hay dos métodos de generador de imágenes que devuelven un escritor de consultas: **CreateQueryWriter** y **CreateQueryWriterFromReader**.

**CreateQueryWriter** crea un escritor de consultas para el formato de metadatos y el proveedor especificados. Este escritor de consultas permite escribir metadatos para un formato de metadatos específico y agregarlos a la imagen. En el código siguiente se muestra una llamada a **CreateQueryWriter** para crear un escritor de consultas XMP.


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



En este ejemplo, se usa el nombre descriptivo `GUID_MetadataFormatXMP` como parámetro *guidMetadataFormat* . Representa el GUID del formato de metadatos XMP y el proveedor representa el controlador creado por Microsoft. Como alternativa, se puede pasar **null** como parámetro *pguidVendor* con los mismos resultados si no existe ningún otro controlador XMP. Si se instala un controlador XMP personalizado junto con el controlador XMP nativo, pasar **null** para el proveedor dará lugar al escritor de consultas con el GUID más bajo que se devuelve.

**CreateQueryWriterFromReader** es similar al método **CreateQueryWriter** , salvo que rellena previamente el nuevo escritor de consultas con los datos proporcionados por el lector de consultas. Esto resulta útil para volver a codificar una imagen mientras se conservan los metadatos existentes o para quitar los metadatos no deseados. En el código siguiente se muestra una llamada a **CreateQueryWriterFromReader** .


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

Después de obtener un escritor de consultas, puede usarlo para agregar bloques de metadatos y elementos. Para escribir metadatos, se usa el método **SetMetadataByName** del escritor de consultas. **SetMetadataByName** toma dos parámetros: una expresión de consulta (*wzName*) y un puntero a un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*). La expresión de consulta define el bloque o el elemento que se va a establecer mientras PROPVARIANT proporciona el valor de datos real que se va a establecer.

En el ejemplo siguiente se muestra cómo agregar un título mediante el escritor de consultas XMP obtenido previamente con el método **CreateQueryWriter** .


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



En este ejemplo, el tipo de valor (VT) se establece en `VT_LPWSTR` , lo que indica que se usará una cadena como valor de datos. Dado que el tipo del *valor* es una cadena, *pwszVal* se usa para establecer el título que se va a usar. A continuación, se llama a **SetMetadataByName** con la expresión de consulta "/DC: title" y la [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)recién establecida. La expresión de consulta utilizada indica que se debe establecer la propiedad title en el esquema de cámara digital (DC). Tenga en cuenta que la expresión no es "/XMP/DC: title"; Esto se debe a que el escritor de consultas ya es específico de XMP y no contiene un bloque XMP incrustado, que sugeriría "/XMP/DC: title".

Hasta este momento no se han agregado metadatos a un fotograma de imagen. Simplemente ha rellenado un escritor de consultas con datos. Para agregar a un marco un bloque de metadatos representado por el escritor de consultas, vuelva a llamar a **SetMetadataByName** con el escritor de consultas como el valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Esto copia eficazmente los metadatos del escritor de consultas en el marco de la imagen. En el código siguiente se muestra cómo agregar los metadatos del escritor de consultas XMP obtenidos previamente al bloque de metadatos raíz de un marco.


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



En este ejemplo, se usa un tipo de valor (VT) de `VT_UNKOWN` ; que indica un tipo de valor de interfaz com. A continuación, el escritor de consultas XMP (piXMPWriter) se usa como el valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), agregando una referencia a él mediante el método AddRef. Por último, el escritor de consultas XMP se establece mediante una llamada al método **SetMetadataByName** del marco y pasando la expresión de consulta "/", que indica el bloque raíz y el PROPVARIANT recién establecido.

> [!Note]  
> Si el marco ya contiene el bloque de metadatos que está intentando agregar, se agregarán los metadatos que va a agregar y se sobrescribirán los metadatos existentes.

 

### <a name="removing-metadata"></a>Quitar metadatos

Un escritor de consultas también permite quitar los metadatos llamando al método **RemoveMetadataByName** . **RemoveMetadataByName** toma una expresión de consulta y quita el bloque de metadatos o el elemento si existe. En el código siguiente se muestra cómo quitar el título que se agregó anteriormente.


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



En el código siguiente se muestra cómo quitar el bloque de metadatos XMP completo.


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a>Copia de metadatos para la recodificación

> [!Note]  
> El código de esta sección solo es válido cuando los formatos de imagen de origen y de destino son los mismos. No se pueden copiar todos los metadatos de una imagen en una sola operación al codificar en un formato de imagen diferente.

 

Para conservar los metadatos mientras se vuelve a codificar una imagen en el mismo formato de imagen, hay métodos disponibles para copiar todos los metadatos en una sola operación. Cada una de estas operaciones sigue un patrón similar; cada uno establece los metadatos del marco descodificado directamente en el nuevo marco que se está codificando.

El método preferido para copiar los metadatos consiste en inicializar el escritor de bloque del nuevo fotograma con el lector de bloques del fotograma descodificado. En el código siguiente se muestra este método.


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



En este ejemplo, el lector de bloques y el escritor de bloque se obtienen del marco de origen y el de destino, respectivamente. A continuación, el escritor de bloque se inicializa desde el lector de bloques. Esto inicializa el lector de bloques con los metadatos rellenados previamente del lector de bloques.

Otro método para copiar los metadatos es escribir el bloque de metadatos al que hace referencia el lector de consultas mediante el escritor de consultas del codificador. En el código siguiente se muestra este método.


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



En este caso, se obtiene un lector de consultas del marco descodificado y, a continuación, se usa como valor de propiedad de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) con un tipo de valor establecido en VT \_ Unknown. Se obtiene el escritor de consultas para el codificador y se usa la expresión de consulta "/" para establecer los metadatos en la ruta de navegación raíz. También puede utilizar este método al establecer los bloques de metadatos anidados, ajustando la expresión de consulta a la ubicación deseada.

Del mismo modo, puede crear un escritor de consultas basado en el lector de consultas del marco descodificado mediante el método **CreateQueryWriterFromReader** de la factoría de imágenes. El escritor de consultas creado en esta operación se rellenará con los metadatos del lector de consultas y, a continuación, se podrá establecer en el marco. En el código siguiente se muestra la operación de copia **CreateQueryWriterFromReader** .


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



Este método usa un escritor de consultas independiente que se basa en los datos del lector de consultas. Este nuevo escritor de consultas se establece en el marco.

De nuevo, estas operaciones para copiar metadatos solo funcionan cuando las imágenes de origen y de destino tienen el mismo formato. Esto se debe a que los distintos formatos de imagen almacenan los bloques de metadatos en ubicaciones diferentes. Por ejemplo, JPEG y TIFF admiten bloques de metadatos XMP. En las imágenes JPEG, el bloque XMP está en el bloque de metadatos raíz, tal como se muestra en [información general sobre metadatos de WIC](-wic-about-metadata.md). Sin embargo, en una imagen TIFF, el bloque XMP está anidado en un bloque IFD raíz. En el diagrama siguiente se muestran las diferencias entre una imagen JPEG y una imagen TIFF con los mismos metadatos de clasificación.

![comparación de JPEG y TIFF.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a>Codificación rápida de metadatos

No siempre es necesario volver a codificar una imagen para escribir nuevos metadatos en ella. Los metadatos también se pueden escribir con un codificador de metadatos rápido. Un codificador rápido de metadatos puede escribir una cantidad limitada de metadatos en una imagen sin volver a codificar la imagen. Esto se logra escribiendo los nuevos metadatos en el relleno vacío proporcionado por algunos formatos de metadatos. Los formatos de metadatos nativos que admiten el relleno de metadatos son EXIF, IFD, GPS y XMP.

### <a name="adding-padding-to-metadata-blocks"></a>Agregar relleno a bloques de metadatos

Antes de poder realizar la codificación rápida de metadatos, debe haber espacio en el bloque de metadatos para escribir más metadatos. Si no hay suficiente espacio en el relleno existente para escribir los nuevos metadatos, se producirá un error en la codificación rápida de los metadatos. Para agregar relleno de metadatos a una imagen, se debe volver a codificar la imagen. Puede Agregar el relleno de la misma manera que agregaría cualquier otro elemento de metadatos, mediante una expresión de consulta, si el bloque de metadatos que está rellenando lo admite. En el ejemplo siguiente se muestra cómo agregar relleno a un bloque IFD incrustado en un bloque app1.


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



Para agregar relleno, cree un PROPVARIANT de tipo VT \_ UI4 y un valor que se corresponda con el número de bytes de relleno que se van a agregar. Un valor típico es 4096 bytes. Las consultas de metadatos para JPEG, TIFF y JPEG-XR se encuentran en esta tabla.



| Formato de metadatos | Consulta de metadatos JPEG                  | TIFF, consulta de metadatos JPEG-XR    |
|-----------------|--------------------------------------|---------------------------------|
| IFD             | /app1/ifd/PaddingSchema: relleno      | /ifd/PaddingSchema: relleno      |
| EXIF            | /app1/ifd/exif/PaddingSchema: relleno | /ifd/exif/PaddingSchema: relleno |
| XMP             | /xmp/PaddingSchema: relleno           | /ifd/xmp/PaddingSchema: relleno  |
| GPS             | /app1/ifd/gps/PaddingSchema: relleno  | /ifd/gps/PaddingSchema: relleno  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a>Obtención de un codificador de metadatos rápido

Si tiene una imagen con relleno de metadatos, se puede obtener un codificador rápido de metadatos mediante los métodos de generador de imágenes **CreateFastMetadataEncoderFromDecoder** y **CreateFastMetadataEncoderFromFrameDecode**.

Como su nombre implica, **CreateFastMetadataEncoderFromDecoder** crea un codificador de metadatos rápido para los metadatos de nivel de descodificador. Los formatos de imagen nativa que proporciona WIC no admiten metadatos de nivel de descodificador, pero este método se proporciona en caso de que se desarrolle un formato de imagen en el futuro.

El escenario más común consiste en obtener un codificador rápido de metadatos de un fotograma de imagen mediante **CreateFastMetadataEncoderFromFrameDecode**. El código siguiente obtiene el codificador de metadatos rápido de un fotograma descodificado y cambia el valor de clasificación en el bloque app1.


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



### <a name="using-the-fast-metadata-encoder"></a>Usar el codificador de metadatos rápidos

Desde el codificador de metadatos rápido, puede obtener un escritor de consultas. Esto le permite escribir metadatos utilizando una expresión de consulta como se ha mostrado anteriormente. Una vez que se han establecido los metadatos en el escritor de consultas, confirme el codificador de metadatos rápido para finalizar la actualización de los metadatos. El código siguiente muestra cómo establecer y confirmar los cambios de metadatos


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



Si se produce un error en la **confirmación** por cualquier motivo, tendrá que volver a codificar la imagen para asegurarse de que los nuevos metadatos se agregan a la imagen.

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

 

 
