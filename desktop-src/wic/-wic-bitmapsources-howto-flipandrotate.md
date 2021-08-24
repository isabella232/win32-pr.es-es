---
description: En este tema se muestra cómo rotar un IWICBitmapSource mediante un componente IWICBitmapFlipRotator.
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: Cómo voltear y girar un origen de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a61a1546f5a0191d2e20cc3079af3e4d772e6d2c3c07a5dd1e1e4aa331dc3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331555"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a>Cómo voltear y girar un origen de mapa de bits

En este tema se muestra cómo rotar [**un IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mediante un [**componente IWICBitmapFlipRotator.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)

Para voltear y girar un origen de mapa de bits

1.  Cree un [**objeto IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para crear Windows componentes de creación de imágenes (WIC).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Use el [**método CreateDecoderFromFilename para**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) crear un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de un archivo de imagen.

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapFlipRotator *pIFlipRotator = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  Obtenga el [**primer IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    El formato de archivo JPEG solo admite un único fotograma. Dado que el archivo de este ejemplo es un archivo JPEG, se usa el primer fotograma ( `0` ). Para ver los formatos de imagen que tienen varios fotogramas, [consulte Recuperación](-wic-bitmapsources-howto-retrieveimageframes.md) de los fotogramas de una imagen para acceder a cada fotograma de la imagen.

4.  Cree el [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) que se usará para voltear la imagen.

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  Inicialice el objeto flip/rotator con los datos de imagen del marco de mapa de bits volteado horizontalmente (a lo largo del eje y vertical).

    ```C++
    // Initialize the flip/rotator to flip the original source horizontally.
    if (SUCCEEDED(hr))
    {
       hr = pIFlipRotator->Initialize(
          pIDecoderFrame,                     // Bitmap source to flip.
          WICBitmapTransformFlipHorizontal);  // Flip the pixels along the 
                                              //  vertical y-axis.
    }
    ```

    

    Consulte [**WICBitmapTransformOptions para**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) obtener más rotaciones y opciones de volteo.

6.  Dibuje o procese el origen del mapa de bits volteado.

    > [!Note]  
    > La interfaz [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) hereda de la interfaz [**IWICBitmapSource,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) por lo que puede usar el objeto flip/rotator inicializado en cualquier lugar que acepte un **IWICBitmapSource**.

     

    En la ilustración siguiente se muestra cómo voltear una imagen horizontalmente (a lo largo del eje X vertical).

    ![ilustración que muestra un volteo horizontal (a lo largo del eje X verital) de una imagen](graphics/fliphorizontal.png)

## <a name="see-also"></a>Consulte también

[Guía de programación](-wic-programming-guide.md)


[Referencia](-wic-codec-reference.md)


[Muestras](-wic-samples.md)


 

 



