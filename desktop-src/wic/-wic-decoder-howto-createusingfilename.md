---
description: En este tema se describe cómo crear un descodificador de mapa de bits mediante un nombre de archivo de imagen.
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: Cómo crear un descodificador mediante un nombre de archivo de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867581e06692188913e4bb1af4956956c462c46bc189a4983f3c5d24bc38c986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811995"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a>Cómo crear un descodificador mediante un nombre de archivo de imagen

En este tema se describe cómo crear un descodificador de mapa de bits mediante un nombre de archivo de imagen.

Para crear un descodificador de mapa de bits mediante un nombre de archivo de imagen

1.  Cree un [**objeto IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para crear objetos Windows Imaging Component (WIC).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Use el [**método CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para crear un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de un archivo de imagen.

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

    

3.  Obtiene el [**primer IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    El formato de archivo JPEG solo admite un único marco. Dado que el archivo de este ejemplo es un archivo JPEG, se usa el primer fotograma ( `0` ). Para ver los formatos de imagen que tienen varios fotogramas, consulte Cómo recuperar los fotogramas [de una imagen](-wic-bitmapsources-howto-retrieveimageframes.md) para acceder a cada fotograma de la imagen.

4.  Procese el marco de imagen. Para obtener información adicional sobre [**los objetos IWICBitmapSource,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) vea Información general sobre orígenes [de mapa de bits.](-wic-bitmapsources.md)

## <a name="see-also"></a>Consulte también

[Guía de programación](-wic-programming-guide.md)


[Referencia](-wic-codec-reference.md)


[Muestras](-wic-samples.md)


 

 



