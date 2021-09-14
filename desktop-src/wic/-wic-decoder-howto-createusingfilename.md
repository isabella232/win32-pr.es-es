---
description: En este tema se describe cómo crear un descodificador de mapa de bits mediante un nombre de archivo de imagen.
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: Cómo crear un descodificador mediante un nombre de archivo de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113ea82b741f2a8dab6c92d6391d65eb7d7e99c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247598"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a>Cómo crear un descodificador mediante un nombre de archivo de imagen

En este tema se describe cómo crear un descodificador de mapa de bits mediante un nombre de archivo de imagen.

Para crear un descodificador de mapa de bits mediante un nombre de archivo de imagen

1.  Cree un [**objeto IWICImagingFactory para**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) crear Windows componentes de creación de imágenes (WIC).

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

4.  Procese el marco de imagen. Para obtener información adicional sobre [**los objetos IWICBitmapSource,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) vea Información general sobre orígenes [de mapa de bits.](-wic-bitmapsources.md)

## <a name="see-also"></a>Consulte también

[Guía de programación](-wic-programming-guide.md)


[Referencia](-wic-codec-reference.md)


[Muestras](-wic-samples.md)


 

 



