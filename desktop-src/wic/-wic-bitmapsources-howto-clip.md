---
description: En este tema se muestra cómo obtener una parte rectangular de un elemento IWICBitmapSource mediante un componente IWICBitmapClipper.
ms.assetid: c9834827-8e1d-436d-be82-c1a2a2f7ca5c
title: Cómo recortar un origen de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43919e03d5d866d37ad4af203e741d2b10e60889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565650"
---
# <a name="how-to-clip-a-bitmap-source"></a>Cómo recortar un origen de mapa de bits

En este tema se muestra cómo obtener una parte rectangular de un elemento [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mediante un componente [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .

Para recortar un origen de mapa de bits

1.  Cree un objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para crear objetos de Windows Imaging Component (WIC).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Use el método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para crear un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de un archivo de imagen.

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

    

3.  Obtiene el primer [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    El formato de archivo JPEG solo admite un único fotograma. Dado que el archivo de este ejemplo es un archivo JPEG, se usa el primer fotograma ( `0` ). Para obtener información sobre los formatos de imagen que tienen varios fotogramas, consulte [recuperación de los marcos de una imagen](-wic-bitmapsources-howto-retrieveimageframes.md) para tener acceso a cada fotograma de la imagen.

4.  Cree el [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) que se va a usar para el recorte de la imagen.

    ```C++
    IWICBitmapClipper *pIClipper = NULL;

    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapClipper(&pIClipper);
    }
    ```

    

5.  Inicializa el objeto Clipper con los datos de la imagen dentro del rectángulo especificado del marco de mapa de bits.

    ```C++
    // Create the clipping rectangle.
    WICRect rcClip = { 0, 0, uiWidth/2, uiHeight/2 };

    // Initialize the clipper with the given rectangle of the frame's image data.
    if (SUCCEEDED(hr))
    {
       hr = pIClipper->Initialize(pIDecoderFrame, &rcClip);
    }
    ```

    

6.  Dibuje o procese la imagen recortada.

    En la ilustración siguiente se muestra el recorte de imágenes. La imagen original de la izquierda es 200 x 130 píxeles. La imagen de la derecha es la imagen original recortada en un rectángulo definido como `{20,20,100,100}` .

    ![Ilustración del recorte de imágenes](graphics/cliparegion_axisalignedclip.png)

## <a name="see-also"></a>Consulte también

[Guía de programación](-wic-programming-guide.md)


[Referencia](-wic-codec-reference.md)


[Muestras](-wic-samples.md)


 

 



