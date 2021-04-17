---
description: En este tema se describe cómo crear un descodificador de mapa de bits mediante un flujo.
ms.assetid: 982d2110-ff2f-43e0-a931-cb2b8146ad0a
title: Cómo crear un descodificador mediante un flujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a76badec0e2587f9136cfa6bc3ff041b76592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697810"
---
# <a name="how-to-create-a-decoder-using-a-stream"></a>Cómo crear un descodificador mediante un flujo

En este tema se describe cómo crear un descodificador de mapa de bits mediante un flujo.

Para crear un descodificador de mapa de bits mediante un flujo

1.  Cargar un archivo de imagen en una secuencia. En este ejemplo, se crea un flujo para un recurso de aplicación.

    En el archivo de definición de recursos de la aplicación (. RC), defina el recurso. En el ejemplo siguiente se define un `Image` recurso denominado `IDR_SAMPLE_IMAGE` .

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    El recurso se agregará a los recursos de la aplicación cuando se compile la aplicación.

2.  Cargue el recurso de la aplicación.

    ```C++
    HRESULT hr = S_OK;

    // WIC interface pointers.
    IWICStream *pIWICStream = NULL;
    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame = NULL;

    // Resource management.
    HRSRC imageResHandle = NULL;
    HGLOBAL imageResDataHandle = NULL;
    void *pImageFile = NULL;
    DWORD imageFileSize = 0;

    // Locate the resource in the application's executable.
    imageResHandle = FindResource(
       NULL,             // This component.
       L"SampleImage",   // Resource name.
       L"Image");        // Resource type.

    hr = (imageResHandle ? S_OK : E_FAIL);

    // Load the resource to the HGLOBAL.
    if (SUCCEEDED(hr)){
       imageResDataHandle = LoadResource(NULL, imageResHandle);
       hr = (imageResDataHandle ? S_OK : E_FAIL);
    }
    
    ```

    

3.  Bloquee el recurso y obtenga el tamaño.

    ```C++
    // Lock the resource to retrieve memory pointer.
    if (SUCCEEDED(hr)){
       pImageFile = LockResource(imageResDataHandle);
       hr = (pImageFile ? S_OK : E_FAIL);
    }

    // Calculate the size.
    if (SUCCEEDED(hr)){
       imageFileSize = SizeofResource(NULL, imageResHandle);
       hr = (imageFileSize ? S_OK : E_FAIL);
    }
    
    ```

    

4.  Cree un [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para crear objetos de Windows Imaging Component (WIC).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  Use el método [**CreateStream (**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) para crear un objeto [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) e inicializarlo con el puntero de memoria de imagen.

    ```C++
    // Create a WIC stream to map onto the memory.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateStream(&pIWICStream);
    }

    // Initialize the stream with the memory pointer and size.
    if (SUCCEEDED(hr)){
       hr = pIWICStream->InitializeFromMemory(
             reinterpret_cast<BYTE*>(pImageFile),
             imageFileSize);
    }
    ```

    

6.  Cree una [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) desde el nuevo objeto de secuencia mediante el método [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .

    ```C++
    // Create a decoder for the stream.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateDecoderFromStream(
          pIWICStream,                   // The stream to use to create the decoder
          NULL,                          // Do not prefer a particular vendor
          WICDecodeMetadataCacheOnLoad,  // Cache metadata when needed
          &pIDecoder);                   // Pointer to the decoder
    }
    ```

    

7.  Obtiene el primer [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    El formato de archivo JPEG solo admite un único fotograma. Dado que el archivo de este ejemplo es un archivo JPEG, se usa el primer fotograma ( `0` ). Para obtener información sobre los formatos de imagen que tienen varios fotogramas, consulte [recuperación de los marcos de una imagen](-wic-bitmapsources-howto-retrieveimageframes.md) para tener acceso a cada fotograma de la imagen.

8.  Procesa el marco de imagen. Para obtener más información sobre los objetos de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , vea la [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

## <a name="see-also"></a>Consulte también

[Guía de programación](-wic-programming-guide.md)


[Referencia](-wic-codec-reference.md)


[Muestras](-wic-samples.md)


 

 



