---
description: En este tema se describe cómo crear un descodificador de mapa de bits mediante una secuencia.
ms.assetid: 982d2110-ff2f-43e0-a931-cb2b8146ad0a
title: Cómo crear un descodificador mediante una secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a76badec0e2587f9136cfa6bc3ff041b76592
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247593"
---
# <a name="how-to-create-a-decoder-using-a-stream"></a>Cómo crear un descodificador mediante una secuencia

En este tema se describe cómo crear un descodificador de mapa de bits mediante una secuencia.

Para crear un descodificador de mapa de bits mediante una secuencia

1.  Cargue un archivo de imagen en una secuencia. En este ejemplo, se crea una secuencia para un recurso de aplicación.

    En el archivo de definición de recursos de aplicación (.rc), defina el recurso. En el ejemplo siguiente se define `Image` un recurso denominado `IDR_SAMPLE_IMAGE` .

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    El recurso se agregará a los recursos de la aplicación cuando se haya creado la aplicación.

2.  Cargue el recurso desde la aplicación.

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

    

4.  Cree una [**IWICImagingFactory para**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) crear objetos Windows Imaging Component (WIC).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  Use el [**método CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) para crear un [**objeto IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) e inicializarlo mediante el puntero de memoria de imagen.

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

    

6.  Cree un [**IWICBitmapDecoder a partir**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) del nuevo objeto de secuencia mediante el [**método CreateDecoderFromStream.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

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

    

7.  Obtenga el [**primer IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    El formato de archivo JPEG solo admite un único fotograma. Dado que el archivo de este ejemplo es un archivo JPEG, se usa el primer fotograma ( `0` ). Para ver los formatos de imagen que tienen varios fotogramas, [consulte Recuperación](-wic-bitmapsources-howto-retrieveimageframes.md) de los fotogramas de una imagen para acceder a cada fotograma de la imagen.

8.  Procese el marco de imagen. Para obtener información adicional sobre [**los objetos IWICBitmapSource,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) vea Información general sobre orígenes [de mapa de bits.](-wic-bitmapsources.md)

## <a name="see-also"></a>Consulte también

[Guía de programación](-wic-programming-guide.md)


[Referencia](-wic-codec-reference.md)


[Muestras](-wic-samples.md)


 

 



