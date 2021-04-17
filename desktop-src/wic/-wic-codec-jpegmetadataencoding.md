---
description: En el ejemplo siguiente se muestra cómo volver a codificar una imagen y sus metadatos en un nuevo archivo con el mismo formato.
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: Cómo volver a codificar una imagen JPEG con metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c023defb760faeab2bc6ea92232fcc916ef15126
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105718595"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a><span data-ttu-id="c4ab4-103">Cómo volver a codificar una imagen JPEG con metadatos</span><span class="sxs-lookup"><span data-stu-id="c4ab4-103">How-to re-encode a JPEG image with metadata</span></span>

<span data-ttu-id="c4ab4-104">En el ejemplo siguiente se muestra cómo volver a codificar una imagen y sus metadatos en un nuevo archivo con el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-104">The following example demonstrates how to re-encode an image and its metadata to a new file of the same format.</span></span> <span data-ttu-id="c4ab4-105">Además, en este ejemplo se agregan metadatos para mostrar una expresión de un solo elemento utilizada por un escritor de consultas.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-105">In addition, this example adds metadata to demonstrate a single-item expression used by a query writer.</span></span>

<span data-ttu-id="c4ab4-106">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c4ab4-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c4ab4-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="c4ab4-108">Parte 1: descodificación de una imagen</span><span class="sxs-lookup"><span data-stu-id="c4ab4-108">Part 1: Decode an Image</span></span>](#part-1-decode-an-image)
-   [<span data-ttu-id="c4ab4-109">Parte 2: creación e inicialización del codificador de imágenes</span><span class="sxs-lookup"><span data-stu-id="c4ab4-109">Part 2: Create and Initialize the Image Encoder</span></span>](#part-2-create-and-initialize-the-image-encoder)
-   [<span data-ttu-id="c4ab4-110">Parte 3: copia de la información del marco descodificado</span><span class="sxs-lookup"><span data-stu-id="c4ab4-110">Part 3: Copy Decoded Frame Information</span></span>](#part-3-copy-decoded-frame-information)
-   [<span data-ttu-id="c4ab4-111">Parte 4: copia de los metadatos</span><span class="sxs-lookup"><span data-stu-id="c4ab4-111">Part 4: Copy the Metadata</span></span>](#part-4-copy-the-metadata)
-   [<span data-ttu-id="c4ab4-112">Parte 5: agregar metadatos adicionales</span><span class="sxs-lookup"><span data-stu-id="c4ab4-112">Part 5: Add Additional Metadata</span></span>](#part-5-add-additional-metadata)
-   [<span data-ttu-id="c4ab4-113">Parte 6: finalización de la imagen codificada</span><span class="sxs-lookup"><span data-stu-id="c4ab4-113">Part 6: Finalize the Encoded Image</span></span>](#part-6-finalize-the-encoded-image)
-   [<span data-ttu-id="c4ab4-114">Código de ejemplo de recodificación JPEG</span><span class="sxs-lookup"><span data-stu-id="c4ab4-114">JPEG Re-encode Example Code</span></span>](#jpeg-re-encode-example-code)
-   [<span data-ttu-id="c4ab4-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c4ab4-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="c4ab4-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c4ab4-116">Prerequisites</span></span>

<span data-ttu-id="c4ab4-117">Para entender este tema, debe estar familiarizado con el sistema de metadatos de Windows Imaging Component (WIC) tal y como se describe en [información general sobre metadatos de WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="c4ab4-117">To understand this topic, you should be familiar with the Windows Imaging Component (WIC) metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="c4ab4-118">También debe estar familiarizado con los componentes del códec WIC tal y como se describe en [información general sobre el componente de creación de imágenes de Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="c4ab4-118">You should also be familiar with the WIC codec components as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="part-1-decode-an-image"></a><span data-ttu-id="c4ab4-119">Parte 1: descodificación de una imagen</span><span class="sxs-lookup"><span data-stu-id="c4ab4-119">Part 1: Decode an Image</span></span>

<span data-ttu-id="c4ab4-120">Antes de poder copiar datos de imagen o metadatos en un archivo de imagen nuevo, primero debe crear un descodificador para la imagen existente que desea volver a codificar.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-120">Before you can copy image data or metadata to a new image file, you must first create a decoder for the existing image that you want to re-encode.</span></span> <span data-ttu-id="c4ab4-121">En el código siguiente se muestra cómo crear un descodificador de WIC para el archivo de imagen test.jpg.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-121">The following code demonstrates how to create a WIC decoder for the image file test.jpg.</span></span>


```C++
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }
```



<span data-ttu-id="c4ab4-122">La llamada a **CreateDecoderFromFilename** usó el valor WICDecodeMetadataCacheOnDemand de la enumeración [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) como el cuarto parámetro.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-122">The call to **CreateDecoderFromFilename** used the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration as the fourth parameter.</span></span> <span data-ttu-id="c4ab4-123">Esto indica al descodificador que almacene en caché los metadatos cuando se necesitan los metadatos, ya sea obteniendo un lector de consultas o usando el lector de metadatos subyacente.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-123">This tells the decoder to cache the metadata when the metadata is needed, either by obtaining a query reader or by using the underlying metadata reader.</span></span> <span data-ttu-id="c4ab4-124">El uso de esta opción permite conservar la secuencia en los metadatos, lo que es necesario para realizar la codificación rápida de los metadatos y permite la descodificación y codificación sin pérdida de las imágenes JPEG.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-124">Using this option enables you to retain the stream to the metadata, which is required for performing fast metadata encoding and enables lossless decoding and encoding of JPEG images.</span></span> <span data-ttu-id="c4ab4-125">Como alternativa, puede usar el otro valor de **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, que almacena en memoria caché los metadatos de la imagen incrustada en cuanto se carga la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-125">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

## <a name="part-2-create-and-initialize-the-image-encoder"></a><span data-ttu-id="c4ab4-126">Parte 2: creación e inicialización del codificador de imágenes</span><span class="sxs-lookup"><span data-stu-id="c4ab4-126">Part 2: Create and Initialize the Image Encoder</span></span>

<span data-ttu-id="c4ab4-127">En el código siguiente se muestra la creación del codificador que se va a usar para codificar la imagen previamente descodificada.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-127">The following code demonstrates the creation of the encoder you will use to encode the image you previously decoded.</span></span>


```C++
    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }
```



<span data-ttu-id="c4ab4-128">Se crea un flujo de archivos WIC piFileStream y se inicializa para escribir en el archivo de imagen "test2.jpg".</span><span class="sxs-lookup"><span data-stu-id="c4ab4-128">A WIC file stream piFileStream is created and initialized for writing to the image file "test2.jpg".</span></span> <span data-ttu-id="c4ab4-129">a continuación, se usa piFileStream para inicializar el codificador, que informa al codificador dónde escribir los bits de la imagen cuando se completa la codificación.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-129">piFileStream is then used to initialize the encoder, informing the encoder where to write the image bits when the encoding is complete.</span></span>

## <a name="part-3-copy-decoded-frame-information"></a><span data-ttu-id="c4ab4-130">Parte 3: copia de la información del marco descodificado</span><span class="sxs-lookup"><span data-stu-id="c4ab4-130">Part 3: Copy Decoded Frame Information</span></span>

<span data-ttu-id="c4ab4-131">En el código siguiente se copia cada fotograma de una imagen en un nuevo marco del codificador.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-131">The following code copies each frame of an image to a new frame of the encoder.</span></span> <span data-ttu-id="c4ab4-132">Esta copia incluye el tamaño, la resolución y el formato de píxel; todos ellos son necesarios para crear un marco válido.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-132">This copy includes size, resolution, and pixel format; all of which are necessary to create a valid frame.</span></span>

> [!Note]  
> <span data-ttu-id="c4ab4-133">Las imágenes JPEG solo tendrán un fotograma y el bucle siguiente no es técnicamente necesario, sino que se incluye para mostrar el uso de varios fotogramas para los formatos que lo admiten.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-133">JPEG images will only have one frame and the loop below is not technically necessary but is included to demonstrate multi-frame usage for formats that support it.</span></span>

 


```C++
    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }
```



<span data-ttu-id="c4ab4-134">El siguiente código realiza una comprobación rápida para determinar si los formatos de imagen de origen y de destino son los mismos.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-134">The following code performs a quick check to determine whether the source and destination image formats are the same.</span></span> <span data-ttu-id="c4ab4-135">Esto es necesario, ya que la parte 4 muestra una operación que solo se admite cuando los formatos de origen y destino son los mismos.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-135">This is needed as Part 4 shows an operation that is only supported when the source and destination format are the same.</span></span>


```C++
            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }
```



## <a name="part-4-copy-the-metadata"></a><span data-ttu-id="c4ab4-136">Parte 4: copia de los metadatos</span><span class="sxs-lookup"><span data-stu-id="c4ab4-136">Part 4: Copy the Metadata</span></span>

> [!Note]  
> <span data-ttu-id="c4ab4-137">El código de esta sección solo es válido cuando los formatos de imagen de origen y de destino son los mismos.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-137">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="c4ab4-138">No se pueden copiar todos los metadatos de una imagen en una sola operación al codificar en un formato de imagen diferente.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-138">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="c4ab4-139">Para conservar los metadatos mientras se vuelve a codificar una imagen en el mismo formato de imagen, hay métodos disponibles para copiar todos los metadatos en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-139">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="c4ab4-140">Cada una de estas operaciones sigue un patrón similar; cada uno establece los metadatos del marco descodificado directamente en el nuevo marco que se está codificando.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-140">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span> <span data-ttu-id="c4ab4-141">Tenga en cuenta que esto se hace para cada fotograma de imagen individual.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-141">Note that this is done for each individual image frame.</span></span>

<span data-ttu-id="c4ab4-142">El método preferido para copiar metadatos consiste en inicializar el escritor de bloque del nuevo fotograma con el lector de bloques del fotograma descodificado.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-142">The preferred method for copying metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="c4ab4-143">En el código siguiente se muestra este método.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-143">The following code demonstrates this method.</span></span>


```C++
            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }
```



<span data-ttu-id="c4ab4-144">En este ejemplo, simplemente se obtiene el lector de bloque y el escritor de bloque del marco de origen y de destino, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-144">In this example, you simply obtain the block reader and block writer from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="c4ab4-145">A continuación, el escritor de bloque se inicializa desde el lector de bloques.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-145">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="c4ab4-146">Esto inicializa el escritor de bloque con los metadatos rellenados previamente del lector de bloques.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-146">This initializes the block writer with the pre-populated metadata of the block reader.</span></span> <span data-ttu-id="c4ab4-147">Para obtener más información sobre métodos adicionales para copiar metadatos, consulte la sección Writing Metadata en [información general sobre la lectura y la escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="c4ab4-147">To learn additional methods for copying metadata, see the Writing Metadata section in the [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="c4ab4-148">De nuevo, esta operación solo funciona cuando las imágenes de origen y de destino tienen el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-148">Again, this operation works only when the source and destination images have the same format.</span></span> <span data-ttu-id="c4ab4-149">Esto se debe a que los distintos formatos de imagen almacenan los bloques de metadatos en ubicaciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-149">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="c4ab4-150">Por ejemplo, JPEG y Tagged Image File Format (TIFF) admiten bloques de metadatos de la plataforma de metadatos extensible (XMP).</span><span class="sxs-lookup"><span data-stu-id="c4ab4-150">For instance, both JPEG and Tagged Image File Format (TIFF) support Extensible Metadata Platform (XMP) metadata blocks.</span></span> <span data-ttu-id="c4ab4-151">En las imágenes JPEG, el bloque XMP está en el bloque de metadatos raíz, tal como se muestra en [información general sobre metadatos de WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="c4ab4-151">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="c4ab4-152">Sin embargo, en una imagen TIFF, el bloque XMP se inserta en el bloque IFD raíz.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-152">However, in a TIFF image, the XMP block is embedded in the root IFD block.</span></span>

## <a name="part-5-add-additional-metadata"></a><span data-ttu-id="c4ab4-153">Parte 5: agregar metadatos adicionales</span><span class="sxs-lookup"><span data-stu-id="c4ab4-153">Part 5: Add Additional Metadata</span></span>

<span data-ttu-id="c4ab4-154">En el ejemplo siguiente se muestra cómo agregar metadatos a la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-154">The following example demonstrates how to add metadata to the destination image.</span></span> <span data-ttu-id="c4ab4-155">Para ello, se llama al método **SetMetadataByName** del escritor de consultas mediante una expresión de consulta y los datos almacenados en un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="c4ab4-155">This is done by calling the query writer's **SetMetadataByName** method using a query expression and the data stored in a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span>


```C++
            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
```



<span data-ttu-id="c4ab4-156">Para obtener más información sobre la expresión de consulta, vea la [Introducción al lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="c4ab4-156">For more information on the query expression, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="part-6-finalize-the-encoded-image"></a><span data-ttu-id="c4ab4-157">Parte 6: finalización de la imagen codificada</span><span class="sxs-lookup"><span data-stu-id="c4ab4-157">Part 6: Finalize the Encoded Image</span></span>

<span data-ttu-id="c4ab4-158">Los pasos finales para copiar la imagen son escribir los datos de píxeles para el marco, confirmar el fotograma al codificador y confirmar el codificador.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-158">The final steps for copying the image are to write the pixel data for the frame, commit the frame to the encoder, and commit the encoder.</span></span> <span data-ttu-id="c4ab4-159">La confirmación del codificador escribe el flujo de imagen en el archivo.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-159">Committing the encoder writes the image stream to the file.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
```



<span data-ttu-id="c4ab4-160">El método **WriteSource** del marco se utiliza para escribir los datos de píxeles de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-160">The frame's **WriteSource** method is used to write the pixel data for the image.</span></span> <span data-ttu-id="c4ab4-161">Tenga en cuenta que esto se realiza una vez que se han escrito los metadatos.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-161">Note that this is done after the metadata has been written.</span></span> <span data-ttu-id="c4ab4-162">Esto es necesario para asegurarse de que los metadatos tienen suficiente espacio dentro del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-162">This is necessary to ensure that the metadata has enough space within the image file.</span></span> <span data-ttu-id="c4ab4-163">Después de escribir los datos de píxeles, el marco se escribe en la secuencia mediante el método **commit** del marco.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-163">After the pixel data is written, the frame is written to the stream using the frame's **Commit** method.</span></span> <span data-ttu-id="c4ab4-164">Una vez procesados todos los fotogramas, el codificador (y, por lo tanto, la imagen) finaliza con el método **commit** del codificador.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-164">After all frames have been processed, the encoder (and thus the image) is finalized using the encoder's **Commit** method.</span></span>

<span data-ttu-id="c4ab4-165">Una vez que confirme el marco, debe liberar los objetos COM creados en el bucle.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-165">Once you commit the frame, you must release the COM objects created in the loop.</span></span>

## <a name="jpeg-re-encode-example-code"></a><span data-ttu-id="c4ab4-166">Código de ejemplo de recodificación JPEG</span><span class="sxs-lookup"><span data-stu-id="c4ab4-166">JPEG Re-encode Example Code</span></span>

<span data-ttu-id="c4ab4-167">El siguiente es el código de las partes 1 a 6 en un bloque Convienient.</span><span class="sxs-lookup"><span data-stu-id="c4ab4-167">The following is the code from Parts 1 through 6 in one convienient block.</span></span>


```C++
#include <Windows.h>
#include <Wincodecsdk.h>

int main()
{
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }

    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }

    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }

            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }

            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }

            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="c4ab4-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c4ab4-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c4ab4-169">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c4ab4-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c4ab4-170">Información general sobre metadatos de WIC</span><span class="sxs-lookup"><span data-stu-id="c4ab4-170">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="c4ab4-171">Información general del lenguaje de consulta de metadatos</span><span class="sxs-lookup"><span data-stu-id="c4ab4-171">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="c4ab4-172">Información general sobre la lectura y escritura de metadatos de imagen</span><span class="sxs-lookup"><span data-stu-id="c4ab4-172">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="c4ab4-173">Información general sobre la extensibilidad de metadatos</span><span class="sxs-lookup"><span data-stu-id="c4ab4-173">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
