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
# <a name="overview-of-reading-and-writing-image-metadata"></a><span data-ttu-id="57694-103">Información general sobre la lectura y escritura de metadatos de imagen</span><span class="sxs-lookup"><span data-stu-id="57694-103">Overview of Reading and Writing Image Metadata</span></span>

<span data-ttu-id="57694-104">En este tema se proporciona información general sobre cómo se pueden usar las API de Windows Imaging Component (WIC) para leer y escribir metadatos que se incrustan en archivos de imagen.</span><span class="sxs-lookup"><span data-stu-id="57694-104">This topic provides an overview of how you can use the Windows Imaging Component (WIC) APIs to read and write metadata that is embedded in image files.</span></span>

<span data-ttu-id="57694-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="57694-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="57694-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="57694-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="57694-107">Introducción</span><span class="sxs-lookup"><span data-stu-id="57694-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="57694-108">Lectura de Metadadata con un lector de consultas</span><span class="sxs-lookup"><span data-stu-id="57694-108">Reading Metadadata Using a Query Reader</span></span>](#reading-metadadata-using-a-query-reader)
    -   [<span data-ttu-id="57694-109">Obtener un lector de consultas</span><span class="sxs-lookup"><span data-stu-id="57694-109">Obtaining a Query Reader</span></span>](#obtaining-a-query-reader)
    -   [<span data-ttu-id="57694-110">Leer metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-110">Reading Metadata</span></span>](#reading-metadata)
    -   [<span data-ttu-id="57694-111">Métodos de lectura de consulta adicionales</span><span class="sxs-lookup"><span data-stu-id="57694-111">Additional Query Reader Methods</span></span>](#additional-query-reader-methods)
-   [<span data-ttu-id="57694-112">Escribir metadatos mediante un escritor de consultas</span><span class="sxs-lookup"><span data-stu-id="57694-112">Writing Metadata Using a Query Writer</span></span>](#writing-metadata-using-a-query-writer)
    -   [<span data-ttu-id="57694-113">Obtener un escritor de consultas</span><span class="sxs-lookup"><span data-stu-id="57694-113">Obtaining a Query Writer</span></span>](#obtaining-a-query-writer)
    -   [<span data-ttu-id="57694-114">Agregar metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-114">Adding Metadata</span></span>](#adding-metadata)
    -   [<span data-ttu-id="57694-115">Quitar metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-115">Removing Metadata</span></span>](#removing-metadata)
    -   [<span data-ttu-id="57694-116">Copia de metadatos para la recodificación</span><span class="sxs-lookup"><span data-stu-id="57694-116">Copying Metadata for Re-encoding</span></span>](#copying-metadata-for-re-encoding)
-   [<span data-ttu-id="57694-117">Codificación rápida de metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-117">Fast Metadata Encoding</span></span>](#fast-metadata-encoding)
    -   [<span data-ttu-id="57694-118">Agregar relleno a bloques de metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-118">Adding Padding to Metadata Blocks</span></span>](#adding-padding-to-metadata-blocks)
    -   [<span data-ttu-id="57694-119">Obtención de un codificador de metadatos rápido</span><span class="sxs-lookup"><span data-stu-id="57694-119">Obtaining a Fast Metadata Encoder</span></span>](#obtaining-a-fast-metadata-encoder)
    -   [<span data-ttu-id="57694-120">Usar el codificador de metadatos rápidos</span><span class="sxs-lookup"><span data-stu-id="57694-120">Using the Fast Metadata Encoder</span></span>](#using-the-fast-metadata-encoder)
-   [<span data-ttu-id="57694-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57694-121">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="57694-122">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="57694-122">Prerequisites</span></span>

<span data-ttu-id="57694-123">Para entender este tema, debe estar familiarizado con el sistema de metadatos de WIC tal y como se describe en [información general sobre metadatos de WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="57694-123">To understand this topic, you should be familiar with the WIC metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="57694-124">También debe estar familiarizado con el lenguaje de consulta que se usa para leer y escribir metadatos, como se describe en [información general sobre el lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="57694-124">You should also be familiar with the query language used to read and write metadata, as described in [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="57694-125">Introducción</span><span class="sxs-lookup"><span data-stu-id="57694-125">Introduction</span></span>

<span data-ttu-id="57694-126">WIC proporciona a los desarrolladores de aplicaciones los componentes del modelo de objetos componentes (COM) para leer y escribir metadatos incrustados en archivos de imagen.</span><span class="sxs-lookup"><span data-stu-id="57694-126">WIC provides application developers with Component Object Model (COM) components to read and write metadata embedded in image files.</span></span> <span data-ttu-id="57694-127">Hay dos maneras de leer y escribir metadatos:</span><span class="sxs-lookup"><span data-stu-id="57694-127">There are two ways to read and write metadata:</span></span>

-   <span data-ttu-id="57694-128">Usar un lector/escritor de consultas y una expresión de consulta para consultar bloques de metadatos para bloques anidados o metadatos específicos dentro de un bloque.</span><span class="sxs-lookup"><span data-stu-id="57694-128">Using a query reader/writer and a query expression to query metadata blocks for nested blocks or specific metadata within a block.</span></span>
-   <span data-ttu-id="57694-129">Usar un controlador de metadatos (un lector de metadatos o un escritor de metadatos) para tener acceso a los bloques de metadatos anidados o a metadatos específicos dentro de los bloques de metadatos.</span><span class="sxs-lookup"><span data-stu-id="57694-129">Using a metadata handler (a metadata reader or a metadata writer) to access the nested metadata blocks or specific metadata within the metadata blocks.</span></span>

<span data-ttu-id="57694-130">Lo más sencillo es usar un lector/escritor de consultas y una expresión de consulta para tener acceso a los metadatos.</span><span class="sxs-lookup"><span data-stu-id="57694-130">The easiest of these is to use a query reader/writer and a query expression to access the metadata.</span></span> <span data-ttu-id="57694-131">Un lector de consultas ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) se usa para leer los metadatos mientras se utiliza un escritor de consultas ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) para escribir los metadatos.</span><span class="sxs-lookup"><span data-stu-id="57694-131">A query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) is used to read metadata while a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used to write metadata.</span></span> <span data-ttu-id="57694-132">Ambos usan una expresión de consulta para leer o escribir los metadatos deseados.</span><span class="sxs-lookup"><span data-stu-id="57694-132">Both of these use a query expression to read or write the desired metadata.</span></span> <span data-ttu-id="57694-133">En segundo plano, un lector de consultas (y escritor) usa un controlador de metadatos para tener acceso a los metadatos descritos por la expresión de consulta.</span><span class="sxs-lookup"><span data-stu-id="57694-133">Behind the scenes, a query reader (and writer) uses a metadata handler to access the metadata described by the query expression.</span></span>

<span data-ttu-id="57694-134">El método más avanzado es acceder directamente a los controladores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="57694-134">The more advanced method is to directly access the metadata handlers.</span></span> <span data-ttu-id="57694-135">Un controlador de metadatos se obtiene de los marcos individuales mediante un lector de bloques ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) o un escritor de bloques ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span><span class="sxs-lookup"><span data-stu-id="57694-135">A metadata handler is obtained from the individual frames using a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) or a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span></span> <span data-ttu-id="57694-136">Los dos tipos de controladores de metadatos disponibles son el lector de metadatos ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) y el escritor de metadatos ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span><span class="sxs-lookup"><span data-stu-id="57694-136">The two types of metadata handlers available are the metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) and the metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span></span>

<span data-ttu-id="57694-137">El siguiente diagrama del contenido de un archivo de imagen JPEG se usa en los ejemplos de este tema.</span><span class="sxs-lookup"><span data-stu-id="57694-137">The following diagram of the contents of a JPEG image file is used throughout the examples in this topic.</span></span> <span data-ttu-id="57694-138">La imagen representada por este diagrama se creó con Microsoft Paint; los metadatos de clasificación se agregaron mediante la característica de la Galería fotográfica de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="57694-138">The image represented by this diagram was created by using Microsoft Paint; the rating metadata was added by using the Photo Gallery feature of Windows Vista.</span></span>

![Ilustración de una imagen JPEG con metadatos de clasificación](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a><span data-ttu-id="57694-140">Lectura de Metadadata con un lector de consultas</span><span class="sxs-lookup"><span data-stu-id="57694-140">Reading Metadadata Using a Query Reader</span></span>

<span data-ttu-id="57694-141">La manera más sencilla de leer los metadatos es usar la interfaz del lector de consultas, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span><span class="sxs-lookup"><span data-stu-id="57694-141">The easiest way to read metadata is to use the query reader interface, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span> <span data-ttu-id="57694-142">El lector de consultas permite leer bloques de metadatos y elementos dentro de bloques de metadatos mediante una expresión de consulta.</span><span class="sxs-lookup"><span data-stu-id="57694-142">The query reader enables you to read metadata blocks and items within metadata blocks using a query expression.</span></span>

<span data-ttu-id="57694-143">Hay tres maneras de obtener un lector de consultas: a través de un descodificador de mapa de bits ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), a través de sus marcos individuales ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) o a través de un escritor de consultas ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="57694-143">There are three ways to obtain a query reader: through a bitmap decoder ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), through its individual frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)), or through a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span>

### <a name="obtaining-a-query-reader"></a><span data-ttu-id="57694-144">Obtener un lector de consultas</span><span class="sxs-lookup"><span data-stu-id="57694-144">Obtaining a Query Reader</span></span>

<span data-ttu-id="57694-145">En el ejemplo de código siguiente se muestra cómo obtener un descodificador de mapa de bits de la factoría de imágenes y recuperar un marco de mapa de bits individual.</span><span class="sxs-lookup"><span data-stu-id="57694-145">The following example code shows how to obtain a bitmap decoder from the imaging factory and retrieve an individual bitmap frame.</span></span> <span data-ttu-id="57694-146">Este código también realiza el trabajo de configuración necesario para obtener un lector de consultas de un marco descodificado.</span><span class="sxs-lookup"><span data-stu-id="57694-146">This code also performs setup work needed to obtain a query reader from a decoded frame.</span></span>


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



<span data-ttu-id="57694-147">El descodificador de mapa de bits para el archivo test.jpg se obtiene mediante el método **CreateDecoderFromFilename** de la factoría de imágenes.</span><span class="sxs-lookup"><span data-stu-id="57694-147">The bitmap decoder for the test.jpg file is obtained by using the **CreateDecoderFromFilename** method of the imaging factory.</span></span> <span data-ttu-id="57694-148">En este método, el cuarto parámetro se establece en el valor WICDecodeMetadataCacheOnDemand de la enumeración [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) .</span><span class="sxs-lookup"><span data-stu-id="57694-148">In this method, the fourth parameter is set to the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration.</span></span> <span data-ttu-id="57694-149">Esto indica al descodificador que almacene en caché los metadatos cuando se necesitan los metadatos; ya sea mediante la obtención de un lector de consultas o el lector de metadatos subyacente.</span><span class="sxs-lookup"><span data-stu-id="57694-149">This tells the decoder to cache the metadata when the metadata is needed; either by obtaining a query reader or the underlying metadata reader.</span></span> <span data-ttu-id="57694-150">El uso de esta opción permite conservar la secuencia en los metadatos necesarios para la codificación rápida de los metadatos y permite la descodificación sin pérdida de la imagen JPEG.</span><span class="sxs-lookup"><span data-stu-id="57694-150">Using this option enables you to retain the stream to the metadata required for fast metadata encoding and enables lossless decoding of the JPEG image.</span></span> <span data-ttu-id="57694-151">Como alternativa, puede usar el otro valor de **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, que almacena en memoria caché los metadatos de la imagen incrustada en cuanto se carga la imagen.</span><span class="sxs-lookup"><span data-stu-id="57694-151">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

<span data-ttu-id="57694-152">Para obtener el lector de consultas del marco, realice una llamada simple al método **GetMetadataQueryReader** del marco.</span><span class="sxs-lookup"><span data-stu-id="57694-152">To obtain the frame's query reader, make a simple call to the frame's **GetMetadataQueryReader** method.</span></span> <span data-ttu-id="57694-153">En el código siguiente se muestra esta llamada.</span><span class="sxs-lookup"><span data-stu-id="57694-153">The following code demonstrates this call.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="57694-154">Del mismo modo, también se puede obtener un lector de consultas en el nivel de descodificador.</span><span class="sxs-lookup"><span data-stu-id="57694-154">Similarly, a query reader can also be obtained at the decoder level.</span></span> <span data-ttu-id="57694-155">Una llamada simple al método **GetMetadataQueryReader** del descodificador obtiene el lector de consultas del descodificador.</span><span class="sxs-lookup"><span data-stu-id="57694-155">A simple call to the decoder's **GetMetadataQueryReader** method gets the decoder's query reader.</span></span> <span data-ttu-id="57694-156">Un lector de consultas del descodificador, a diferencia del lector de consultas de un fotograma, Lee los metadatos de una imagen que está fuera de los fotogramas individuales.</span><span class="sxs-lookup"><span data-stu-id="57694-156">An decoder's query reader, unlike a frame's query reader, reads metadata for an image that is outside of the individual frames.</span></span> <span data-ttu-id="57694-157">Sin embargo, este escenario no es común y los formatos de imagen nativa no admiten esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="57694-157">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="57694-158">Los CÓDECs de imagen nativa proporcionados por WIC leen y escriben metadatos en el nivel de marco incluso en los formatos de un solo fotograma, como JPEG.</span><span class="sxs-lookup"><span data-stu-id="57694-158">The native image CODECS provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

### <a name="reading-metadata"></a><span data-ttu-id="57694-159">Leer metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-159">Reading Metadata</span></span>

<span data-ttu-id="57694-160">Antes de continuar para leer los metadatos, examine el siguiente diagrama de un archivo JPEG que incluye los bloques de metadatos insertados y los datos reales que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="57694-160">Before you move on to actually reading metadata, look at the following diagram of a JPEG file that includes embedded metadata blocks and actual data to retrieve.</span></span> <span data-ttu-id="57694-161">Este diagrama proporciona llamadas a bloques de metadatos específicos y elementos dentro de la imagen que proporcionan la expresión de consulta de metadatos a cada bloque o elemento.</span><span class="sxs-lookup"><span data-stu-id="57694-161">This diagram provides callouts to specific metadata blocks and items within the image providing the metadata query expression to each block or item.</span></span>

![Ilustración de una imagen JPEG con llamadas de metadatos](graphics/jpegwithcallouts.png)

<span data-ttu-id="57694-163">Para consultar bloques de metadatos incrustados o elementos específicos por nombre, llame al método **GetMetadataByName** .</span><span class="sxs-lookup"><span data-stu-id="57694-163">To query for embedded metadata blocks or specific items by name, call the **GetMetadataByName** method.</span></span> <span data-ttu-id="57694-164">Este método toma una expresión de consulta y una [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en la que se devuelve el elemento de metadatos.</span><span class="sxs-lookup"><span data-stu-id="57694-164">This method takes a query expression and a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in which the metadata item is returned.</span></span> <span data-ttu-id="57694-165">En el código siguiente se consulta un bloque de metadatos anidado y se convierte el componente [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) proporcionado por el valor PROPVARIANT en un lector de consultas, si se encuentra.</span><span class="sxs-lookup"><span data-stu-id="57694-165">The following code queries for a nested metadata block and converts the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) component provided by the PROPVARIANT value to a query reader if found.</span></span>


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



<span data-ttu-id="57694-166">La expresión de consulta "/app1/IFD" está consultando el bloque IFD anidado en el bloque app1.</span><span class="sxs-lookup"><span data-stu-id="57694-166">The query expression "/app1/ifd" is querying for the IFD block nested in the App1 block.</span></span> <span data-ttu-id="57694-167">El archivo de imagen JPEG contiene el bloque de metadatos anidado IFD, por lo que el [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) se devuelve con un tipo de variable (VT) de `VT_UNKNOWN` y un puntero a una interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) (punkVal).</span><span class="sxs-lookup"><span data-stu-id="57694-167">The JPEG image file contains the IFD nested metadata block, so the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) is returned with a variable type (vt) of `VT_UNKNOWN` and a pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface (punkVal).</span></span> <span data-ttu-id="57694-168">A continuación, se consulta la interfaz IUnknown para un lector de consultas.</span><span class="sxs-lookup"><span data-stu-id="57694-168">You then query the IUnknown interface for a query reader.</span></span>

<span data-ttu-id="57694-169">En el código siguiente se muestra una nueva consulta basada en el nuevo lector de consultas en relación con el bloque IFD anidado.</span><span class="sxs-lookup"><span data-stu-id="57694-169">The following code demonstrates a new query based on the new query reader relative to the nested IFD block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



<span data-ttu-id="57694-170">La expresión de consulta "/{ushort = 18249}" consulta el bloque IFD para la clasificación MicrosoftPhoto incrustada en la etiqueta 18249.</span><span class="sxs-lookup"><span data-stu-id="57694-170">The query expression "/{ushort=18249}" queries the IFD block for the MicrosoftPhoto rating embedded under tag 18249.</span></span> <span data-ttu-id="57694-171">El valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) contendrá ahora un tipo de valor de `VT_UI2` y un valor de datos de 50.</span><span class="sxs-lookup"><span data-stu-id="57694-171">The [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will now contain a value type of `VT_UI2` and a data value of 50.</span></span>

<span data-ttu-id="57694-172">Sin embargo, no es necesario obtener un bloque anidado antes de consultar valores de datos específicos.</span><span class="sxs-lookup"><span data-stu-id="57694-172">However, it is not necessary to obtain a nested block before querying for specific data values.</span></span> <span data-ttu-id="57694-173">Por ejemplo, en lugar de consultar el IFD anidado y, a continuación, para la clasificación de MicrosoftPhoto, puede usar en su lugar el bloque de metadatos raíz y la consulta que se muestra en el código siguiente para obtener la misma información.</span><span class="sxs-lookup"><span data-stu-id="57694-173">For instance, instead of querying for the nested IFD and then for the MicrosoftPhoto rating, you can instead use the root metadata block and the query shown in the following code to obtain the same information.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



<span data-ttu-id="57694-174">Además de consultar elementos de metadatos específicos en un bloque de metadatos, también puede enumerar todos los elementos de metadatos en un bloque de metadatos (sin incluir elementos de metadatos en bloques de metadatos anidados).</span><span class="sxs-lookup"><span data-stu-id="57694-174">In addition to querying for specific metadata items in a metadata block, you can also enumerate all the metadata items in a metadata block (not including metadata items in nested metadata blocks).</span></span> <span data-ttu-id="57694-175">Para enumerar los elementos de metadatos en el bloque actual, se usa el método **GetEnumeration** del lector de consultas.</span><span class="sxs-lookup"><span data-stu-id="57694-175">To enumerate the metadata items in the current block, the query reader's **GetEnumeration** method is used.</span></span> <span data-ttu-id="57694-176">Este método obtiene una interfaz **IEnumString** rellenada con los elementos de metadatos del bloque actual.</span><span class="sxs-lookup"><span data-stu-id="57694-176">This method obtains an **IEnumString** interface populated with the metadata items in the current block.</span></span> <span data-ttu-id="57694-177">Por ejemplo, el código siguiente enumera la clasificación XMP y la clasificación MicrosoftPhoto para el bloque IFD anidado que se obtuvo anteriormente.</span><span class="sxs-lookup"><span data-stu-id="57694-177">For example, the following code enumerates the XMP rating and MicrosoftPhoto rating for the nested IFD block that was obtained earlier.</span></span>


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



<span data-ttu-id="57694-178">Para obtener más información sobre cómo identificar etiquetas adecuadas para los distintos formatos de imagen y formatos de metadatos, vea [consultas de metadatos de formato de imagen nativa](-wic-native-image-format-metadata-queries.md).</span><span class="sxs-lookup"><span data-stu-id="57694-178">For more information on identifying appropriate tags for various image formats and metadata formats, see [Native Image Format Metadata Queries](-wic-native-image-format-metadata-queries.md).</span></span>

### <a name="additional-query-reader-methods"></a><span data-ttu-id="57694-179">Métodos de lectura de consulta adicionales</span><span class="sxs-lookup"><span data-stu-id="57694-179">Additional Query Reader Methods</span></span>

<span data-ttu-id="57694-180">Además de leer los metadatos, también puede obtener información adicional sobre el lector de consultas y obtener los metadatos a través de otros medios.</span><span class="sxs-lookup"><span data-stu-id="57694-180">In addition to reading metadata, you can also obtain additional information about the query reader and obtain metadata through other means.</span></span> <span data-ttu-id="57694-181">El lector de consultas proporciona dos métodos que proporcionan información sobre el lector de consultas, **GetContainerFormat** y **GetLocation**.</span><span class="sxs-lookup"><span data-stu-id="57694-181">The query reader provides two methods that provide information about the query reader, **GetContainerFormat** and **GetLocation**.</span></span>

<span data-ttu-id="57694-182">Con el lector de consultas incrustado, puede usar **GetContainerFormat** para determinar el tipo de bloque de metadatos, y puede llamar a **GetLocation** para obtener la ruta de acceso relativa al bloque de metadatos raíz.</span><span class="sxs-lookup"><span data-stu-id="57694-182">With the embedded query reader, you can use **GetContainerFormat** to determine the type of metadata block, and you can call **GetLocation** to obtain the path relative to the root metadata block.</span></span> <span data-ttu-id="57694-183">El código siguiente consulta el lector de consultas incrustado para su ubicación.</span><span class="sxs-lookup"><span data-stu-id="57694-183">The following code queries the embedded query reader for its location.</span></span>


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



<span data-ttu-id="57694-184">La llamada a **GetContainerFormat** para el lector de consultas incrustadas devuelve el GUID del formato de metadatos de IFD.</span><span class="sxs-lookup"><span data-stu-id="57694-184">The call to **GetContainerFormat** for the embedded query reader returns the IFD metadata format GUID.</span></span> <span data-ttu-id="57694-185">La llamada a **GetLocation** devuelve un espacio de nombres de "/app1/IFD"; proporcionar la ruta de acceso relativa desde la que se ejecutarán las consultas posteriores al nuevo lector de consultas.</span><span class="sxs-lookup"><span data-stu-id="57694-185">The call to **GetLocation** returns a namespace of "/app1/ifd"; providing you with the relative path from which subsequent queries to the new query reader will be executed.</span></span> <span data-ttu-id="57694-186">Por supuesto, el código anterior no es muy útil, pero muestra cómo usar el método **GetLocation** para buscar bloques de metadatos anidados.</span><span class="sxs-lookup"><span data-stu-id="57694-186">Of course, the preceding code isn't very useful, but it does demonstrate how to use the **GetLocation** method for finding nested metadata blocks.</span></span>

## <a name="writing-metadata-using-a-query-writer"></a><span data-ttu-id="57694-187">Escribir metadatos mediante un escritor de consultas</span><span class="sxs-lookup"><span data-stu-id="57694-187">Writing Metadata Using a Query Writer</span></span>

> [!Note]  
> <span data-ttu-id="57694-188">Algunos de los ejemplos de código proporcionados en esta sección no se muestran en el contexto de los pasos reales necesarios para escribir metadatos.</span><span class="sxs-lookup"><span data-stu-id="57694-188">Some of the code examples provided in this section are not shown in the context of the actual steps required to write metadata.</span></span> <span data-ttu-id="57694-189">Para ver los ejemplos de código en el contexto de un ejemplo de trabajo, vea el tutorial sobre cómo volver a codificar una imagen con metadatos.</span><span class="sxs-lookup"><span data-stu-id="57694-189">To view the code examples in the context of a working sample, see the How-to: Re-encode an Image with Metadata tutorial.</span></span>

 

<span data-ttu-id="57694-190">El componente principal para escribir metadatos es el escritor de consultas ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="57694-190">The main component for writing metadata is the query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span> <span data-ttu-id="57694-191">El escritor de consultas permite establecer y quitar bloques de metadatos y elementos dentro de un bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="57694-191">The query writer enables you to set and remove metadata blocks and items within a metadata block.</span></span>

<span data-ttu-id="57694-192">Al igual que el lector de consultas, hay tres maneras de obtener un escritor de consultas: a través de un codificador de mapa de bits ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), a través de sus marcos individuales ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) o a través de un codificador de metadatos rápido ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).</span><span class="sxs-lookup"><span data-stu-id="57694-192">Like the query reader, there are three ways to obtain a query writer: through a bitmap encoder ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), through its individual frames ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)), or through a fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).</span></span>

### <a name="obtaining-a-query-writer"></a><span data-ttu-id="57694-193">Obtener un escritor de consultas</span><span class="sxs-lookup"><span data-stu-id="57694-193">Obtaining a Query Writer</span></span>

<span data-ttu-id="57694-194">El escritor de consultas más común es para un marco individual de un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="57694-194">The most common query writer is for an individual frame of a bitmap.</span></span> <span data-ttu-id="57694-195">Este escritor de consultas establece y quita los elementos y bloques de metadatos de un fotograma de imagen.</span><span class="sxs-lookup"><span data-stu-id="57694-195">This query writer sets and removes an image frame's metadata blocks and items.</span></span> <span data-ttu-id="57694-196">Para obtener el escritor de consultas de un fotograma de imagen, llame al método **GetMetadataQueryWriter** del marco.</span><span class="sxs-lookup"><span data-stu-id="57694-196">To obtain an image frame's query writer, call the frame's **GetMetadataQueryWriter** method.</span></span> <span data-ttu-id="57694-197">En el código siguiente se muestra la llamada al método simple para obtener el escritor de consultas de un marco.</span><span class="sxs-lookup"><span data-stu-id="57694-197">The following code demonstrates the simple method call to obtain a frame's query writer.</span></span>


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



<span data-ttu-id="57694-198">Del mismo modo, también se puede obtener un escritor de consultas para el nivel de codificador.</span><span class="sxs-lookup"><span data-stu-id="57694-198">Similarly, a query writer can also be obtained for the encoder level.</span></span> <span data-ttu-id="57694-199">Una llamada simple al método **GetMetadataQueryWriter** del codificador obtiene el escritor de consultas del codificador.</span><span class="sxs-lookup"><span data-stu-id="57694-199">A simple call to the encoder's **GetMetadataQueryWriter** method gets the encoder's query writer.</span></span> <span data-ttu-id="57694-200">El escritor de consultas de un codificador, a diferencia del escritor de consultas de un fotograma, escribe los metadatos de una imagen fuera del fotograma individual.</span><span class="sxs-lookup"><span data-stu-id="57694-200">An encoder's query writer, unlike a frame's query writer, writes metadata for an image outside of the individual frame.</span></span> <span data-ttu-id="57694-201">Sin embargo, este escenario no es común y los formatos de imagen nativa no admiten esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="57694-201">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="57694-202">Los códecs de imagen nativa proporcionados por WIC leen y escriben metadatos en el nivel de marco incluso en los formatos de un solo fotograma, como JPEG.</span><span class="sxs-lookup"><span data-stu-id="57694-202">The native image codecs provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

<span data-ttu-id="57694-203">También puede obtener un escritor de consultas directamente desde el generador de imágenes ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)).</span><span class="sxs-lookup"><span data-stu-id="57694-203">You can also obtain a query writer directly from the imaging factory ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)).</span></span> <span data-ttu-id="57694-204">Hay dos métodos de generador de imágenes que devuelven un escritor de consultas: **CreateQueryWriter** y **CreateQueryWriterFromReader**.</span><span class="sxs-lookup"><span data-stu-id="57694-204">There are two imaging factory methods that return a query writer: **CreateQueryWriter** and **CreateQueryWriterFromReader**.</span></span>

<span data-ttu-id="57694-205">**CreateQueryWriter** crea un escritor de consultas para el formato de metadatos y el proveedor especificados.</span><span class="sxs-lookup"><span data-stu-id="57694-205">**CreateQueryWriter** creates a query writer for the specified metadata format and vendor.</span></span> <span data-ttu-id="57694-206">Este escritor de consultas permite escribir metadatos para un formato de metadatos específico y agregarlos a la imagen.</span><span class="sxs-lookup"><span data-stu-id="57694-206">This query writer enables you to write metadata for a specific metadata format and add it to the image.</span></span> <span data-ttu-id="57694-207">En el código siguiente se muestra una llamada a **CreateQueryWriter** para crear un escritor de consultas XMP.</span><span class="sxs-lookup"><span data-stu-id="57694-207">The following code demonstrates a **CreateQueryWriter** call to create an XMP query writer.</span></span>


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



<span data-ttu-id="57694-208">En este ejemplo, se usa el nombre descriptivo `GUID_MetadataFormatXMP` como parámetro *guidMetadataFormat* .</span><span class="sxs-lookup"><span data-stu-id="57694-208">In this example, the friendly name `GUID_MetadataFormatXMP` is used as the *guidMetadataFormat* parameter.</span></span> <span data-ttu-id="57694-209">Representa el GUID del formato de metadatos XMP y el proveedor representa el controlador creado por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="57694-209">It represents the XMP metadata format GUID, and vendor represents the Microsoft created handler.</span></span> <span data-ttu-id="57694-210">Como alternativa, se puede pasar **null** como parámetro *pguidVendor* con los mismos resultados si no existe ningún otro controlador XMP.</span><span class="sxs-lookup"><span data-stu-id="57694-210">Alternatively, **NULL** can be passed as the *pguidVendor* parameter with the same results if no other XMP handler exists.</span></span> <span data-ttu-id="57694-211">Si se instala un controlador XMP personalizado junto con el controlador XMP nativo, pasar **null** para el proveedor dará lugar al escritor de consultas con el GUID más bajo que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="57694-211">If a custom XMP handler is installed alongside the native XMP handler, passing **NULL** for the vendor will result in the query writer with the lowest GUID being returned.</span></span>

<span data-ttu-id="57694-212">**CreateQueryWriterFromReader** es similar al método **CreateQueryWriter** , salvo que rellena previamente el nuevo escritor de consultas con los datos proporcionados por el lector de consultas.</span><span class="sxs-lookup"><span data-stu-id="57694-212">**CreateQueryWriterFromReader** is similar to the **CreateQueryWriter** method except that it prepopulates the new query writer with the data provided by the query reader.</span></span> <span data-ttu-id="57694-213">Esto resulta útil para volver a codificar una imagen mientras se conservan los metadatos existentes o para quitar los metadatos no deseados.</span><span class="sxs-lookup"><span data-stu-id="57694-213">This is useful for re-encoding an image while maintaining the existing metadata, or for removing unwanted metadata.</span></span> <span data-ttu-id="57694-214">En el código siguiente se muestra una llamada a **CreateQueryWriterFromReader** .</span><span class="sxs-lookup"><span data-stu-id="57694-214">The following code demonstrates a **CreateQueryWriterFromReader** call.</span></span>


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



### <a name="adding-metadata"></a><span data-ttu-id="57694-215">Agregar metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-215">Adding Metadata</span></span>

<span data-ttu-id="57694-216">Después de obtener un escritor de consultas, puede usarlo para agregar bloques de metadatos y elementos.</span><span class="sxs-lookup"><span data-stu-id="57694-216">After you obtain a query writer, you can use it to add metadata blocks and items.</span></span> <span data-ttu-id="57694-217">Para escribir metadatos, se usa el método **SetMetadataByName** del escritor de consultas.</span><span class="sxs-lookup"><span data-stu-id="57694-217">To write metadata, you use the query writer's **SetMetadataByName** method.</span></span> <span data-ttu-id="57694-218">**SetMetadataByName** toma dos parámetros: una expresión de consulta (*wzName*) y un puntero a un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*).</span><span class="sxs-lookup"><span data-stu-id="57694-218">**SetMetadataByName** takes two parameters: a query expression (*wzName*) and a pointer to a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*).</span></span> <span data-ttu-id="57694-219">La expresión de consulta define el bloque o el elemento que se va a establecer mientras PROPVARIANT proporciona el valor de datos real que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="57694-219">The query expression defines the block or item to set while the PROPVARIANT provides the actual data value to set.</span></span>

<span data-ttu-id="57694-220">En el ejemplo siguiente se muestra cómo agregar un título mediante el escritor de consultas XMP obtenido previamente con el método **CreateQueryWriter** .</span><span class="sxs-lookup"><span data-stu-id="57694-220">The following example demonstrates how to add a title by using the XMP query writer previously obtained by using the **CreateQueryWriter** method.</span></span>


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



<span data-ttu-id="57694-221">En este ejemplo, el tipo de valor (VT) se establece en `VT_LPWSTR` , lo que indica que se usará una cadena como valor de datos.</span><span class="sxs-lookup"><span data-stu-id="57694-221">In this example, value's type (vt) is set to `VT_LPWSTR`, indicating that a string will be used as the data value.</span></span> <span data-ttu-id="57694-222">Dado que el tipo del *valor* es una cadena, *pwszVal* se usa para establecer el título que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="57694-222">Because *value*'s type is a string, *pwszVal* is used to set the title to use.</span></span> <span data-ttu-id="57694-223">A continuación, se llama a **SetMetadataByName** con la expresión de consulta "/DC: title" y la [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)recién establecida.</span><span class="sxs-lookup"><span data-stu-id="57694-223">**SetMetadataByName** is then called using the query expression "/dc:title" and the newly set [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="57694-224">La expresión de consulta utilizada indica que se debe establecer la propiedad title en el esquema de cámara digital (DC).</span><span class="sxs-lookup"><span data-stu-id="57694-224">The query expression used indicates that the title property in the digital camera (dc) schema should be set.</span></span> <span data-ttu-id="57694-225">Tenga en cuenta que la expresión no es "/XMP/DC: title"; Esto se debe a que el escritor de consultas ya es específico de XMP y no contiene un bloque XMP incrustado, que sugeriría "/XMP/DC: title".</span><span class="sxs-lookup"><span data-stu-id="57694-225">Note that the expression is not "/xmp/dc:title"; this is because the query writer is already specific to XMP and does not contain an embedded XMP block, which "/xmp/dc:title" would suggest.</span></span>

<span data-ttu-id="57694-226">Hasta este momento no se han agregado metadatos a un fotograma de imagen.</span><span class="sxs-lookup"><span data-stu-id="57694-226">Up to this point you haven't actually added any metadata to an image frame.</span></span> <span data-ttu-id="57694-227">Simplemente ha rellenado un escritor de consultas con datos.</span><span class="sxs-lookup"><span data-stu-id="57694-227">You've simply populated a query writer with data.</span></span> <span data-ttu-id="57694-228">Para agregar a un marco un bloque de metadatos representado por el escritor de consultas, vuelva a llamar a **SetMetadataByName** con el escritor de consultas como el valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="57694-228">To add to a frame a metadata block represented by the query writer, you again call **SetMetadataByName** using the query writer as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="57694-229">Esto copia eficazmente los metadatos del escritor de consultas en el marco de la imagen.</span><span class="sxs-lookup"><span data-stu-id="57694-229">This effectively copies the metadata in the query writer to the image frame.</span></span> <span data-ttu-id="57694-230">En el código siguiente se muestra cómo agregar los metadatos del escritor de consultas XMP obtenidos previamente al bloque de metadatos raíz de un marco.</span><span class="sxs-lookup"><span data-stu-id="57694-230">The following code demonstrates how to add the metadata in the XMP query writer previously obtained to a frame's root metadata block.</span></span>


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



<span data-ttu-id="57694-231">En este ejemplo, se usa un tipo de valor (VT) de `VT_UNKOWN` ; que indica un tipo de valor de interfaz com.</span><span class="sxs-lookup"><span data-stu-id="57694-231">In this example, a value type (vt) of `VT_UNKOWN` is used; indicating a COM interface value type.</span></span> <span data-ttu-id="57694-232">A continuación, el escritor de consultas XMP (piXMPWriter) se usa como el valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), agregando una referencia a él mediante el método AddRef.</span><span class="sxs-lookup"><span data-stu-id="57694-232">The XMP query writer (piXMPWriter) is then used as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), adding a reference to it by using the AddRef method.</span></span> <span data-ttu-id="57694-233">Por último, el escritor de consultas XMP se establece mediante una llamada al método **SetMetadataByName** del marco y pasando la expresión de consulta "/", que indica el bloque raíz y el PROPVARIANT recién establecido.</span><span class="sxs-lookup"><span data-stu-id="57694-233">Finally, the XMP query writer is set by calling the frame's **SetMetadataByName** method and passing the query expression "/", indicating the root block, and the newly set PROPVARIANT.</span></span>

> [!Note]  
> <span data-ttu-id="57694-234">Si el marco ya contiene el bloque de metadatos que está intentando agregar, se agregarán los metadatos que va a agregar y se sobrescribirán los metadatos existentes.</span><span class="sxs-lookup"><span data-stu-id="57694-234">If the frame already contains the metadata block you are trying to add, the metadata you are adding will be added and existing metadata overwritten.</span></span>

 

### <a name="removing-metadata"></a><span data-ttu-id="57694-235">Quitar metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-235">Removing Metadata</span></span>

<span data-ttu-id="57694-236">Un escritor de consultas también permite quitar los metadatos llamando al método **RemoveMetadataByName** .</span><span class="sxs-lookup"><span data-stu-id="57694-236">A query writer also enables you to remove metadata by calling the **RemoveMetadataByName** method.</span></span> <span data-ttu-id="57694-237">**RemoveMetadataByName** toma una expresión de consulta y quita el bloque de metadatos o el elemento si existe.</span><span class="sxs-lookup"><span data-stu-id="57694-237">**RemoveMetadataByName** takes a query expression and removes the metadata block or item if it exists.</span></span> <span data-ttu-id="57694-238">En el código siguiente se muestra cómo quitar el título que se agregó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="57694-238">The following code demonstrates how to remove the title that was previously added.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



<span data-ttu-id="57694-239">En el código siguiente se muestra cómo quitar el bloque de metadatos XMP completo.</span><span class="sxs-lookup"><span data-stu-id="57694-239">The following code demonstrates how to remove the entire XMP metadata block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a><span data-ttu-id="57694-240">Copia de metadatos para la recodificación</span><span class="sxs-lookup"><span data-stu-id="57694-240">Copying Metadata for Re-encoding</span></span>

> [!Note]  
> <span data-ttu-id="57694-241">El código de esta sección solo es válido cuando los formatos de imagen de origen y de destino son los mismos.</span><span class="sxs-lookup"><span data-stu-id="57694-241">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="57694-242">No se pueden copiar todos los metadatos de una imagen en una sola operación al codificar en un formato de imagen diferente.</span><span class="sxs-lookup"><span data-stu-id="57694-242">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="57694-243">Para conservar los metadatos mientras se vuelve a codificar una imagen en el mismo formato de imagen, hay métodos disponibles para copiar todos los metadatos en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="57694-243">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="57694-244">Cada una de estas operaciones sigue un patrón similar; cada uno establece los metadatos del marco descodificado directamente en el nuevo marco que se está codificando.</span><span class="sxs-lookup"><span data-stu-id="57694-244">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span>

<span data-ttu-id="57694-245">El método preferido para copiar los metadatos consiste en inicializar el escritor de bloque del nuevo fotograma con el lector de bloques del fotograma descodificado.</span><span class="sxs-lookup"><span data-stu-id="57694-245">The preferred method to copy metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="57694-246">En el código siguiente se muestra este método.</span><span class="sxs-lookup"><span data-stu-id="57694-246">The following code demonstrates this method.</span></span>


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



<span data-ttu-id="57694-247">En este ejemplo, el lector de bloques y el escritor de bloque se obtienen del marco de origen y el de destino, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="57694-247">In this example, the block reader and the block writer are obtained from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="57694-248">A continuación, el escritor de bloque se inicializa desde el lector de bloques.</span><span class="sxs-lookup"><span data-stu-id="57694-248">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="57694-249">Esto inicializa el lector de bloques con los metadatos rellenados previamente del lector de bloques.</span><span class="sxs-lookup"><span data-stu-id="57694-249">This initializes the block reader with the pre-populated metadata of the block reader.</span></span>

<span data-ttu-id="57694-250">Otro método para copiar los metadatos es escribir el bloque de metadatos al que hace referencia el lector de consultas mediante el escritor de consultas del codificador.</span><span class="sxs-lookup"><span data-stu-id="57694-250">Another method to copy metadata is to write the metadata block referenced by the query reader using the encoder's query writer.</span></span> <span data-ttu-id="57694-251">En el código siguiente se muestra este método.</span><span class="sxs-lookup"><span data-stu-id="57694-251">The following code demonstrates this method.</span></span>


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



<span data-ttu-id="57694-252">En este caso, se obtiene un lector de consultas del marco descodificado y, a continuación, se usa como valor de propiedad de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) con un tipo de valor establecido en VT \_ Unknown.</span><span class="sxs-lookup"><span data-stu-id="57694-252">Here, a query reader is obtained from the decoded frame and then used as the property value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) with a value type set to VT\_UNKNOWN.</span></span> <span data-ttu-id="57694-253">Se obtiene el escritor de consultas para el codificador y se usa la expresión de consulta "/" para establecer los metadatos en la ruta de navegación raíz.</span><span class="sxs-lookup"><span data-stu-id="57694-253">The query writer for the encoder is obtained and the query expression "/" is used to set the metadata at the root navigation path.</span></span> <span data-ttu-id="57694-254">También puede utilizar este método al establecer los bloques de metadatos anidados, ajustando la expresión de consulta a la ubicación deseada.</span><span class="sxs-lookup"><span data-stu-id="57694-254">You can also use this method when setting nested metadata blocks, by adjusting the query expression to the desired location.</span></span>

<span data-ttu-id="57694-255">Del mismo modo, puede crear un escritor de consultas basado en el lector de consultas del marco descodificado mediante el método **CreateQueryWriterFromReader** de la factoría de imágenes.</span><span class="sxs-lookup"><span data-stu-id="57694-255">Similarly, you can create a query writer based on the decoded frame's query reader by using the imaging factory's **CreateQueryWriterFromReader** method.</span></span> <span data-ttu-id="57694-256">El escritor de consultas creado en esta operación se rellenará con los metadatos del lector de consultas y, a continuación, se podrá establecer en el marco.</span><span class="sxs-lookup"><span data-stu-id="57694-256">The query writer created in this operation will be prepopulated with the metadata from the query reader and can then be set in the frame.</span></span> <span data-ttu-id="57694-257">En el código siguiente se muestra la operación de copia **CreateQueryWriterFromReader** .</span><span class="sxs-lookup"><span data-stu-id="57694-257">The following code demonstrates the **CreateQueryWriterFromReader** copy operation.</span></span>


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



<span data-ttu-id="57694-258">Este método usa un escritor de consultas independiente que se basa en los datos del lector de consultas.</span><span class="sxs-lookup"><span data-stu-id="57694-258">This method uses a separate query writer is created that is based on the data of the query reader.</span></span> <span data-ttu-id="57694-259">Este nuevo escritor de consultas se establece en el marco.</span><span class="sxs-lookup"><span data-stu-id="57694-259">This new query writer then set in the frame.</span></span>

<span data-ttu-id="57694-260">De nuevo, estas operaciones para copiar metadatos solo funcionan cuando las imágenes de origen y de destino tienen el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="57694-260">Again, these operations to copy metadata only work when the source and destination images have the same format.</span></span> <span data-ttu-id="57694-261">Esto se debe a que los distintos formatos de imagen almacenan los bloques de metadatos en ubicaciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="57694-261">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="57694-262">Por ejemplo, JPEG y TIFF admiten bloques de metadatos XMP.</span><span class="sxs-lookup"><span data-stu-id="57694-262">For instance, both JPEG and TIFF support XMP metadata blocks.</span></span> <span data-ttu-id="57694-263">En las imágenes JPEG, el bloque XMP está en el bloque de metadatos raíz, tal como se muestra en [información general sobre metadatos de WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="57694-263">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="57694-264">Sin embargo, en una imagen TIFF, el bloque XMP está anidado en un bloque IFD raíz.</span><span class="sxs-lookup"><span data-stu-id="57694-264">However, in a TIFF image, the XMP block is nested in a root IFD block.</span></span> <span data-ttu-id="57694-265">En el diagrama siguiente se muestran las diferencias entre una imagen JPEG y una imagen TIFF con los mismos metadatos de clasificación.</span><span class="sxs-lookup"><span data-stu-id="57694-265">The following diagram illustrates the differences between a JPEG image and a TIFF image with the same rating metadata.</span></span>

![comparación de JPEG y TIFF.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a><span data-ttu-id="57694-267">Codificación rápida de metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-267">Fast Metadata Encoding</span></span>

<span data-ttu-id="57694-268">No siempre es necesario volver a codificar una imagen para escribir nuevos metadatos en ella.</span><span class="sxs-lookup"><span data-stu-id="57694-268">It is not always necessary to re-encode an image to write new metadata to it.</span></span> <span data-ttu-id="57694-269">Los metadatos también se pueden escribir con un codificador de metadatos rápido.</span><span class="sxs-lookup"><span data-stu-id="57694-269">Metadata can also be written by using a fast metadata encoder.</span></span> <span data-ttu-id="57694-270">Un codificador rápido de metadatos puede escribir una cantidad limitada de metadatos en una imagen sin volver a codificar la imagen.</span><span class="sxs-lookup"><span data-stu-id="57694-270">A fast metadata encoder can write a limited amount of metadata to an image without re-encoding the image.</span></span> <span data-ttu-id="57694-271">Esto se logra escribiendo los nuevos metadatos en el relleno vacío proporcionado por algunos formatos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="57694-271">This is accomplished by writing the new metadata within the empty padding provided by some metadata formats.</span></span> <span data-ttu-id="57694-272">Los formatos de metadatos nativos que admiten el relleno de metadatos son EXIF, IFD, GPS y XMP.</span><span class="sxs-lookup"><span data-stu-id="57694-272">The native metadata formats that support metadata padding are Exif, IFD, GPS and XMP.</span></span>

### <a name="adding-padding-to-metadata-blocks"></a><span data-ttu-id="57694-273">Agregar relleno a bloques de metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-273">Adding Padding to Metadata Blocks</span></span>

<span data-ttu-id="57694-274">Antes de poder realizar la codificación rápida de metadatos, debe haber espacio en el bloque de metadatos para escribir más metadatos.</span><span class="sxs-lookup"><span data-stu-id="57694-274">Before you can perform fast metadata encoding, there must be room within the metadata block to write more metadata.</span></span> <span data-ttu-id="57694-275">Si no hay suficiente espacio en el relleno existente para escribir los nuevos metadatos, se producirá un error en la codificación rápida de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="57694-275">If there is not enough room within the existing padding to write the new metadata, the fast metadata encoding will fail.</span></span> <span data-ttu-id="57694-276">Para agregar relleno de metadatos a una imagen, se debe volver a codificar la imagen.</span><span class="sxs-lookup"><span data-stu-id="57694-276">To add metadata padding to an image, the image must be re-encoded.</span></span> <span data-ttu-id="57694-277">Puede Agregar el relleno de la misma manera que agregaría cualquier otro elemento de metadatos, mediante una expresión de consulta, si el bloque de metadatos que está rellenando lo admite.</span><span class="sxs-lookup"><span data-stu-id="57694-277">You can add padding the same way you would add any other metadata item, by using a query expression, if the metadata block you are padding supports it.</span></span> <span data-ttu-id="57694-278">En el ejemplo siguiente se muestra cómo agregar relleno a un bloque IFD incrustado en un bloque app1.</span><span class="sxs-lookup"><span data-stu-id="57694-278">The following example demonstrates how to add padding to an IFD block embedded in an App1 block.</span></span>


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



<span data-ttu-id="57694-279">Para agregar relleno, cree un PROPVARIANT de tipo VT \_ UI4 y un valor que se corresponda con el número de bytes de relleno que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="57694-279">To add padding, create a PROPVARIANT of type VT\_UI4 and a value corresponding to the number of bytes of padding to add.</span></span> <span data-ttu-id="57694-280">Un valor típico es 4096 bytes.</span><span class="sxs-lookup"><span data-stu-id="57694-280">A typical value is 4096 bytes.</span></span> <span data-ttu-id="57694-281">Las consultas de metadatos para JPEG, TIFF y JPEG-XR se encuentran en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="57694-281">The metadata queries for JPEG, TIFF, and JPEG-XR are in this table.</span></span>



| <span data-ttu-id="57694-282">Formato de metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-282">Metadata format</span></span> | <span data-ttu-id="57694-283">Consulta de metadatos JPEG</span><span class="sxs-lookup"><span data-stu-id="57694-283">JPEG metadata query</span></span>                  | <span data-ttu-id="57694-284">TIFF, consulta de metadatos JPEG-XR</span><span class="sxs-lookup"><span data-stu-id="57694-284">TIFF, JPEG-XR metadata query</span></span>    |
|-----------------|--------------------------------------|---------------------------------|
| <span data-ttu-id="57694-285">IFD</span><span class="sxs-lookup"><span data-stu-id="57694-285">IFD</span></span>             | <span data-ttu-id="57694-286">/app1/ifd/PaddingSchema: relleno</span><span class="sxs-lookup"><span data-stu-id="57694-286">/app1/ifd/PaddingSchema:Padding</span></span>      | <span data-ttu-id="57694-287">/ifd/PaddingSchema: relleno</span><span class="sxs-lookup"><span data-stu-id="57694-287">/ifd/PaddingSchema:Padding</span></span>      |
| <span data-ttu-id="57694-288">EXIF</span><span class="sxs-lookup"><span data-stu-id="57694-288">EXIF</span></span>            | <span data-ttu-id="57694-289">/app1/ifd/exif/PaddingSchema: relleno</span><span class="sxs-lookup"><span data-stu-id="57694-289">/app1/ifd/exif/PaddingSchema:Padding</span></span> | <span data-ttu-id="57694-290">/ifd/exif/PaddingSchema: relleno</span><span class="sxs-lookup"><span data-stu-id="57694-290">/ifd/exif/PaddingSchema:Padding</span></span> |
| <span data-ttu-id="57694-291">XMP</span><span class="sxs-lookup"><span data-stu-id="57694-291">XMP</span></span>             | <span data-ttu-id="57694-292">/xmp/PaddingSchema: relleno</span><span class="sxs-lookup"><span data-stu-id="57694-292">/xmp/PaddingSchema:Padding</span></span>           | <span data-ttu-id="57694-293">/ifd/xmp/PaddingSchema: relleno</span><span class="sxs-lookup"><span data-stu-id="57694-293">/ifd/xmp/PaddingSchema:Padding</span></span>  |
| <span data-ttu-id="57694-294">GPS</span><span class="sxs-lookup"><span data-stu-id="57694-294">GPS</span></span>             | <span data-ttu-id="57694-295">/app1/ifd/gps/PaddingSchema: relleno</span><span class="sxs-lookup"><span data-stu-id="57694-295">/app1/ifd/gps/PaddingSchema:Padding</span></span>  | <span data-ttu-id="57694-296">/ifd/gps/PaddingSchema: relleno</span><span class="sxs-lookup"><span data-stu-id="57694-296">/ifd/gps/PaddingSchema:Padding</span></span>  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a><span data-ttu-id="57694-297">Obtención de un codificador de metadatos rápido</span><span class="sxs-lookup"><span data-stu-id="57694-297">Obtaining a Fast Metadata Encoder</span></span>

<span data-ttu-id="57694-298">Si tiene una imagen con relleno de metadatos, se puede obtener un codificador rápido de metadatos mediante los métodos de generador de imágenes **CreateFastMetadataEncoderFromDecoder** y **CreateFastMetadataEncoderFromFrameDecode**.</span><span class="sxs-lookup"><span data-stu-id="57694-298">When you have an image with metadata padding, a fast metadata encoder can be obtained by using the imaging factory methods **CreateFastMetadataEncoderFromDecoder** and **CreateFastMetadataEncoderFromFrameDecode**.</span></span>

<span data-ttu-id="57694-299">Como su nombre implica, **CreateFastMetadataEncoderFromDecoder** crea un codificador de metadatos rápido para los metadatos de nivel de descodificador.</span><span class="sxs-lookup"><span data-stu-id="57694-299">As the name implies, **CreateFastMetadataEncoderFromDecoder** creates a fast metadata encoder for decoder-level metadata.</span></span> <span data-ttu-id="57694-300">Los formatos de imagen nativa que proporciona WIC no admiten metadatos de nivel de descodificador, pero este método se proporciona en caso de que se desarrolle un formato de imagen en el futuro.</span><span class="sxs-lookup"><span data-stu-id="57694-300">The native image formats provided by WIC do not support decoder-level metadata but this method is provided in case such an image format is developed in the future.</span></span>

<span data-ttu-id="57694-301">El escenario más común consiste en obtener un codificador rápido de metadatos de un fotograma de imagen mediante **CreateFastMetadataEncoderFromFrameDecode**.</span><span class="sxs-lookup"><span data-stu-id="57694-301">The more common scenario is to obtain a fast metadata encoder from an image frame by using **CreateFastMetadataEncoderFromFrameDecode**.</span></span> <span data-ttu-id="57694-302">El código siguiente obtiene el codificador de metadatos rápido de un fotograma descodificado y cambia el valor de clasificación en el bloque app1.</span><span class="sxs-lookup"><span data-stu-id="57694-302">The following code obtains a decoded frame's fast metadata encoder and changes the rating value in the App1 block.</span></span>


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



### <a name="using-the-fast-metadata-encoder"></a><span data-ttu-id="57694-303">Usar el codificador de metadatos rápidos</span><span class="sxs-lookup"><span data-stu-id="57694-303">Using the Fast Metadata Encoder</span></span>

<span data-ttu-id="57694-304">Desde el codificador de metadatos rápido, puede obtener un escritor de consultas.</span><span class="sxs-lookup"><span data-stu-id="57694-304">From the fast metadata encoder, you can obtain a query writer.</span></span> <span data-ttu-id="57694-305">Esto le permite escribir metadatos utilizando una expresión de consulta como se ha mostrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="57694-305">This enables you to write metadata by using a query expression as previously demonstrated.</span></span> <span data-ttu-id="57694-306">Una vez que se han establecido los metadatos en el escritor de consultas, confirme el codificador de metadatos rápido para finalizar la actualización de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="57694-306">After metadata has been set in the query writer, commit the fast metadata encoder to finalize the metadata update.</span></span> <span data-ttu-id="57694-307">El código siguiente muestra cómo establecer y confirmar los cambios de metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-307">The following code demonstrates setting and committing the metadata changes</span></span>


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



<span data-ttu-id="57694-308">Si se produce un error en la **confirmación** por cualquier motivo, tendrá que volver a codificar la imagen para asegurarse de que los nuevos metadatos se agregan a la imagen.</span><span class="sxs-lookup"><span data-stu-id="57694-308">If **Commit** fails for any reason, you will need to re-encode the image to ensure the new metadata is added to the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57694-309">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57694-309">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="57694-310">**Vista**</span><span class="sxs-lookup"><span data-stu-id="57694-310">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="57694-311">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="57694-311">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="57694-312">Información general sobre metadatos de WIC</span><span class="sxs-lookup"><span data-stu-id="57694-312">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="57694-313">Información general del lenguaje de consulta de metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-313">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="57694-314">Información general sobre la extensibilidad de metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-314">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="57694-315">Cómo volver a codificar una imagen JPEG con metadatos</span><span class="sxs-lookup"><span data-stu-id="57694-315">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
