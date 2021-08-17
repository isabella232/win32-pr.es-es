---
description: En el ejemplo siguiente se muestra cómo volver a codificar una imagen y sus metadatos en un nuevo archivo con el mismo formato.
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: Cómo volver a codificar una imagen JPEG con metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13851af04c6af742dbc68acc31fd674c3602ebeb16bec6903a3570f8cb1e0400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088167"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a>Cómo volver a codificar una imagen JPEG con metadatos

En el ejemplo siguiente se muestra cómo volver a codificar una imagen y sus metadatos en un nuevo archivo con el mismo formato. Además, en este ejemplo se agregan metadatos para mostrar una expresión de un solo elemento usada por un escritor de consultas.

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Parte 1: Descodificación de una imagen](#part-1-decode-an-image)
-   [Parte 2: Crear e inicializar el codificador de imágenes](#part-2-create-and-initialize-the-image-encoder)
-   [Parte 3: Copiar información de marco descodificado](#part-3-copy-decoded-frame-information)
-   [Parte 4: Copiar los metadatos](#part-4-copy-the-metadata)
-   [Parte 5: Agregar metadatos adicionales](#part-5-add-additional-metadata)
-   [Parte 6: Finalizar la imagen codificada](#part-6-finalize-the-encoded-image)
-   [Código de ejemplo de volver a codificar JPEG](#jpeg-re-encode-example-code)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

Para comprender este tema, debe estar familiarizado con el sistema de metadatos de Windows Imaging Component (WIC), tal como se describe en información general sobre los metadatos [de WIC.](-wic-about-metadata.md) También debe estar familiarizado con los componentes del códec WIC, tal como se describe en la introducción al componente Windows creación de [imágenes.](-wic-about-windows-imaging-codec.md)

## <a name="part-1-decode-an-image"></a>Parte 1: Descodificación de una imagen

Para poder copiar datos de imagen o metadatos en un nuevo archivo de imagen, primero debe crear un descodificador para la imagen existente que desea volver a codificar. El código siguiente muestra cómo crear un descodificador WIC para el archivo de imagen test.jpg.


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



La llamada a **CreateDecoderFromFilename** usó el valor WICDecodeMetadataCacheOnDemand de la enumeración [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) como cuarto parámetro. Esto indica al descodificador que almacena en caché los metadatos cuando se necesitan, ya sea mediante la obtención de un lector de consultas o mediante el lector de metadatos subyacente. El uso de esta opción le permite conservar la secuencia en los metadatos, que es necesaria para realizar la codificación rápida de metadatos y permite la codificación y la codificación sin pérdida de imágenes JPEG. Como alternativa, podría usar el otro valor **de WICDecodeOptions,** WICDecodeMetadataCacheOnLoad, que almacena en caché los metadatos de la imagen incrustada en cuanto se carga la imagen.

## <a name="part-2-create-and-initialize-the-image-encoder"></a>Parte 2: Crear e inicializar el codificador de imágenes

El código siguiente muestra la creación del codificador que usará para codificar la imagen que descodificó anteriormente.


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



Se crea e inicializa una secuencia de archivos WIC piFileStream para escribir en el archivo de imagen "test2.jpg". Después, piFileStream se usa para inicializar el codificador, informando al codificador de dónde escribir los bits de imagen una vez completada la codificación.

## <a name="part-3-copy-decoded-frame-information"></a>Parte 3: Copiar información de marco descodificado

El código siguiente copia cada fotograma de una imagen en un nuevo fotograma del codificador. Esta copia incluye el tamaño, la resolución y el formato de píxel; todos los cuales son necesarios para crear un marco válido.

> [!Note]  
> Las imágenes JPEG solo tendrán un fotograma y el bucle siguiente no es técnicamente necesario, pero se incluye para mostrar el uso de varios fotogramas para los formatos que lo admiten.

 


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



El código siguiente realiza una comprobación rápida para determinar si los formatos de imagen de origen y destino son los mismos. Esto es necesario, ya que la parte 4 muestra una operación que solo se admite cuando el formato de origen y destino es el mismo.


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



## <a name="part-4-copy-the-metadata"></a>Parte 4: Copiar los metadatos

> [!Note]  
> El código de esta sección solo es válido cuando los formatos de imagen de origen y destino son los mismos. No se pueden copiar todos los metadatos de una imagen en una sola operación al codificar en un formato de imagen diferente.

 

Para conservar los metadatos al volver a codificar una imagen en el mismo formato de imagen, hay métodos disponibles para copiar todos los metadatos en una sola operación. Cada una de estas operaciones sigue un patrón similar; cada establece los metadatos del marco descodificado directamente en el nuevo marco que se va a codificar. Tenga en cuenta que esto se hace para cada fotograma de imagen individual.

El método preferido para copiar metadatos es inicializar el escritor de bloques del marco nuevo con el lector de bloques del marco descodificado. El código siguiente muestra este método.


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



En este ejemplo, simplemente obtiene el lector de bloques y el escritor de bloques del marco de origen y del marco de destino, respectivamente. A continuación, el escritor de bloques se inicializa desde el lector de bloques. Esto inicializa el escritor de bloques con los metadatos rellenados previamente del lector de bloques. Para obtener más información sobre métodos adicionales para copiar metadatos, vea la sección Escribir metadatos en Información general sobre la lectura y escritura de [metadatos de imagen.](-wic-codec-readingwritingmetadata.md)

De nuevo, esta operación solo funciona cuando las imágenes de origen y destino tienen el mismo formato. Esto se debe a que diferentes formatos de imagen almacenan los bloques de metadatos en ubicaciones diferentes. Por ejemplo, jpeg y Tagged Image File Format (TIFF) admiten bloques de metadatos de Extensible Metadata Platform (XMP). En las imágenes JPEG, el bloque XMP se encuentra en el bloque de metadatos raíz, como se muestra en información general sobre los [metadatos de WIC.](-wic-about-metadata.md) Sin embargo, en una imagen TIFF, el bloque XMP se incrusta en el bloque IFD raíz.

## <a name="part-5-add-additional-metadata"></a>Parte 5: Agregar metadatos adicionales

En el ejemplo siguiente se muestra cómo agregar metadatos a la imagen de destino. Para ello, llame al método **SetMetadataByName** del escritor de consultas mediante una expresión de consulta y los datos almacenados [en propVARIANT.](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)


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



Para obtener más información sobre la expresión de consulta, vea Información general del lenguaje [de consulta de metadatos](-wic-codec-metadataquerylanguage.md).

## <a name="part-6-finalize-the-encoded-image"></a>Parte 6: Finalizar la imagen codificada

Los pasos finales para copiar la imagen son escribir los datos de píxeles del fotograma, confirmar el fotograma en el codificador y confirmar el codificador. Al confirmar el codificador, se escribe la secuencia de imagen en el archivo.


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



El método **WriteSource del** marco se usa para escribir los datos de píxeles de la imagen. Tenga en cuenta que esto se realiza una vez escritos los metadatos. Esto es necesario para asegurarse de que los metadatos tienen suficiente espacio dentro del archivo de imagen. Una vez escritos los datos de píxeles, el marco se escribe en la secuencia mediante el **método Commit del** fotograma. Una vez procesados todos los fotogramas, el codificador (y, por tanto, la imagen) se completa con el método **Commit del** codificador.

Una vez que confirme el marco, debe liberar los objetos COM creados en el bucle .

## <a name="jpeg-re-encode-example-code"></a>Código de ejemplo de volver a codificar JPEG

A continuación se muestra el código de las partes 1 a 6 en un bloque convienient.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Introducción a los metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general sobre el lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Información general sobre extensibilidad de metadatos](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
