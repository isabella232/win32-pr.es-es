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
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a>Cómo volver a codificar una imagen JPEG con metadatos

En el ejemplo siguiente se muestra cómo volver a codificar una imagen y sus metadatos en un nuevo archivo con el mismo formato. Además, en este ejemplo se agregan metadatos para mostrar una expresión de un solo elemento utilizada por un escritor de consultas.

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Parte 1: descodificación de una imagen](#part-1-decode-an-image)
-   [Parte 2: creación e inicialización del codificador de imágenes](#part-2-create-and-initialize-the-image-encoder)
-   [Parte 3: copia de la información del marco descodificado](#part-3-copy-decoded-frame-information)
-   [Parte 4: copia de los metadatos](#part-4-copy-the-metadata)
-   [Parte 5: agregar metadatos adicionales](#part-5-add-additional-metadata)
-   [Parte 6: finalización de la imagen codificada](#part-6-finalize-the-encoded-image)
-   [Código de ejemplo de recodificación JPEG](#jpeg-re-encode-example-code)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

Para entender este tema, debe estar familiarizado con el sistema de metadatos de Windows Imaging Component (WIC) tal y como se describe en [información general sobre metadatos de WIC](-wic-about-metadata.md). También debe estar familiarizado con los componentes del códec WIC tal y como se describe en [información general sobre el componente de creación de imágenes de Windows](-wic-about-windows-imaging-codec.md).

## <a name="part-1-decode-an-image"></a>Parte 1: descodificación de una imagen

Antes de poder copiar datos de imagen o metadatos en un archivo de imagen nuevo, primero debe crear un descodificador para la imagen existente que desea volver a codificar. En el código siguiente se muestra cómo crear un descodificador de WIC para el archivo de imagen test.jpg.


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



La llamada a **CreateDecoderFromFilename** usó el valor WICDecodeMetadataCacheOnDemand de la enumeración [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) como el cuarto parámetro. Esto indica al descodificador que almacene en caché los metadatos cuando se necesitan los metadatos, ya sea obteniendo un lector de consultas o usando el lector de metadatos subyacente. El uso de esta opción permite conservar la secuencia en los metadatos, lo que es necesario para realizar la codificación rápida de los metadatos y permite la descodificación y codificación sin pérdida de las imágenes JPEG. Como alternativa, puede usar el otro valor de **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, que almacena en memoria caché los metadatos de la imagen incrustada en cuanto se carga la imagen.

## <a name="part-2-create-and-initialize-the-image-encoder"></a>Parte 2: creación e inicialización del codificador de imágenes

En el código siguiente se muestra la creación del codificador que se va a usar para codificar la imagen previamente descodificada.


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



Se crea un flujo de archivos WIC piFileStream y se inicializa para escribir en el archivo de imagen "test2.jpg". a continuación, se usa piFileStream para inicializar el codificador, que informa al codificador dónde escribir los bits de la imagen cuando se completa la codificación.

## <a name="part-3-copy-decoded-frame-information"></a>Parte 3: copia de la información del marco descodificado

En el código siguiente se copia cada fotograma de una imagen en un nuevo marco del codificador. Esta copia incluye el tamaño, la resolución y el formato de píxel; todos ellos son necesarios para crear un marco válido.

> [!Note]  
> Las imágenes JPEG solo tendrán un fotograma y el bucle siguiente no es técnicamente necesario, sino que se incluye para mostrar el uso de varios fotogramas para los formatos que lo admiten.

 


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



El siguiente código realiza una comprobación rápida para determinar si los formatos de imagen de origen y de destino son los mismos. Esto es necesario, ya que la parte 4 muestra una operación que solo se admite cuando los formatos de origen y destino son los mismos.


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



## <a name="part-4-copy-the-metadata"></a>Parte 4: copia de los metadatos

> [!Note]  
> El código de esta sección solo es válido cuando los formatos de imagen de origen y de destino son los mismos. No se pueden copiar todos los metadatos de una imagen en una sola operación al codificar en un formato de imagen diferente.

 

Para conservar los metadatos mientras se vuelve a codificar una imagen en el mismo formato de imagen, hay métodos disponibles para copiar todos los metadatos en una sola operación. Cada una de estas operaciones sigue un patrón similar; cada uno establece los metadatos del marco descodificado directamente en el nuevo marco que se está codificando. Tenga en cuenta que esto se hace para cada fotograma de imagen individual.

El método preferido para copiar metadatos consiste en inicializar el escritor de bloque del nuevo fotograma con el lector de bloques del fotograma descodificado. En el código siguiente se muestra este método.


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



En este ejemplo, simplemente se obtiene el lector de bloque y el escritor de bloque del marco de origen y de destino, respectivamente. A continuación, el escritor de bloque se inicializa desde el lector de bloques. Esto inicializa el escritor de bloque con los metadatos rellenados previamente del lector de bloques. Para obtener más información sobre métodos adicionales para copiar metadatos, consulte la sección Writing Metadata en [información general sobre la lectura y la escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md).

De nuevo, esta operación solo funciona cuando las imágenes de origen y de destino tienen el mismo formato. Esto se debe a que los distintos formatos de imagen almacenan los bloques de metadatos en ubicaciones diferentes. Por ejemplo, JPEG y Tagged Image File Format (TIFF) admiten bloques de metadatos de la plataforma de metadatos extensible (XMP). En las imágenes JPEG, el bloque XMP está en el bloque de metadatos raíz, tal como se muestra en [información general sobre metadatos de WIC](-wic-about-metadata.md). Sin embargo, en una imagen TIFF, el bloque XMP se inserta en el bloque IFD raíz.

## <a name="part-5-add-additional-metadata"></a>Parte 5: agregar metadatos adicionales

En el ejemplo siguiente se muestra cómo agregar metadatos a la imagen de destino. Para ello, se llama al método **SetMetadataByName** del escritor de consultas mediante una expresión de consulta y los datos almacenados en un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).


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



Para obtener más información sobre la expresión de consulta, vea la [Introducción al lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md).

## <a name="part-6-finalize-the-encoded-image"></a>Parte 6: finalización de la imagen codificada

Los pasos finales para copiar la imagen son escribir los datos de píxeles para el marco, confirmar el fotograma al codificador y confirmar el codificador. La confirmación del codificador escribe el flujo de imagen en el archivo.


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



El método **WriteSource** del marco se utiliza para escribir los datos de píxeles de la imagen. Tenga en cuenta que esto se realiza una vez que se han escrito los metadatos. Esto es necesario para asegurarse de que los metadatos tienen suficiente espacio dentro del archivo de imagen. Después de escribir los datos de píxeles, el marco se escribe en la secuencia mediante el método **commit** del marco. Una vez procesados todos los fotogramas, el codificador (y, por lo tanto, la imagen) finaliza con el método **commit** del codificador.

Una vez que confirme el marco, debe liberar los objetos COM creados en el bucle.

## <a name="jpeg-re-encode-example-code"></a>Código de ejemplo de recodificación JPEG

El siguiente es el código de las partes 1 a 6 en un bloque Convienient.


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

**Vista**
</dt> <dt>

[Información general sobre metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general del lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Información general sobre la extensibilidad de metadatos](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
