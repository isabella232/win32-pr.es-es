---
description: En este tema se muestra el proceso para dibujar un IWICBitmapSource mediante Direct2D.
ms.assetid: 11d38c9a-775d-41f7-a193-37b702b29a96
title: Dibujar un objeto BitmapSource mediante Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6636bb1d0b0294e7d496ffd8839c645ad046bb256001b2abd1744714eb4c48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668705"
---
# <a name="how-to-draw-a-bitmapsource-using-direct2d"></a>Dibujar un objeto BitmapSource mediante Direct2D

En este tema se muestra el proceso para dibujar [**un IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mediante Direct2D.

Para dibujar un origen de mapa de bits mediante Direct2D

1.  Descodificar una imagen de origen y obtener un origen de mapa de bits. En este ejemplo, se [**usa un IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) para descodificar la imagen y se recupera el primer marco de imagen.

    ```C++
       // Create a decoder
       IWICBitmapDecoder *pDecoder = NULL;

       hr = m_pIWICFactory->CreateDecoderFromFilename(
           szFileName,                      // Image to be decoded
           NULL,                            // Do not prefer a particular vendor
           GENERIC_READ,                    // Desired read access to the file
           WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
           &pDecoder                        // Pointer to the decoder
           );

       // Retrieve the first frame of the image from the decoder
       IWICBitmapFrameDecode *pFrame = NULL;

       if (SUCCEEDED(hr))
       {
           hr = pDecoder->GetFrame(0, &pFrame);
       }
    ```

    

    Para obtener tipos adicionales de orígenes de mapa de bits que se dibujarán, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

2.  Convierta el origen del mapa de bits en un formato de píxeles de 32bppPBGRA.

    Para que Direct2D pueda usar una imagen, debe convertirse al formato de píxeles 32bppPBGRA. Para convertir el formato de imagen, use [**el método CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) para crear un [**objeto IWICFormatConverter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) Una vez creado, use el [**método Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) para realizar la conversión.

    ```C++
       // Format convert the frame to 32bppPBGRA
       if (SUCCEEDED(hr))
       {
           SafeRelease(&m_pConvertedSourceBitmap);
           hr = m_pIWICFactory->CreateFormatConverter(&m_pConvertedSourceBitmap);
       }

       if (SUCCEEDED(hr))
       {
           hr = m_pConvertedSourceBitmap->Initialize(
               pFrame,                          // Input bitmap to convert
               GUID_WICPixelFormat32bppPBGRA,   // Destination pixel format
               WICBitmapDitherTypeNone,         // Specified dither pattern
               NULL,                            // Specify a particular palette 
               0.f,                             // Alpha threshold
               WICBitmapPaletteTypeCustom       // Palette translation type
               );
       }
    ```

    

3.  Cree un [objeto ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) para representarlo en un identificador de ventana.

    ```C++
       // Create a D2D render target properties
       D2D1_RENDER_TARGET_PROPERTIES renderTargetProperties = D2D1::RenderTargetProperties();

       // Set the DPI to be the default system DPI to allow direct mapping
       // between image pixels and desktop pixels in different system DPI settings
       renderTargetProperties.dpiX = DEFAULT_DPI;
       renderTargetProperties.dpiY = DEFAULT_DPI;

       // Create a D2D render target
       D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

       hr = m_pD2DFactory->CreateHwndRenderTarget(
           renderTargetProperties,
           D2D1::HwndRenderTargetProperties(hWnd, size),
           &m_pRT
           );
    ```

    

    Para obtener más información sobre los destinos de representación, vea Introducción a los destinos [de representación de](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)Direct2D.

4.  Cree un [objeto ID2D1Bitmap](../direct2d/render-targets-overview.md) mediante el [método ID2D1RenderTarget::CreateBitmapFromWicBitmap.](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md)

    ```C++
        // D2DBitmap may have been released due to device loss. 
        // If so, re-create it from the source bitmap
        if (m_pConvertedSourceBitmap && !m_pD2DBitmap)
        {
            m_pRT->CreateBitmapFromWicBitmap(m_pConvertedSourceBitmap, NULL, &m_pD2DBitmap);
        }
    ```

    

5.  Dibuje [id2D1Bitmap](../direct2d/render-targets-overview.md) mediante el método D2D [ID2D1RenderTarget::D rawBitmap.](../direct2d/id2d1rendertarget-drawbitmap.md)

    ```C++
        // Draws an image and scales it to the current window size
        if (m_pD2DBitmap)
        {
            m_pRT->DrawBitmap(m_pD2DBitmap, rectangle);
        }
    ```

    

El código se ha omitido en este ejemplo. Para obtener el código completo, consulte el visor [de imágenes wic mediante el ejemplo de Direct2D](-wic-sample-d2d-viewer.md).

## <a name="see-also"></a>Consulte también

[Guía de programación](-wic-programming-guide.md)


[Referencia](-wic-codec-reference.md)


[Ejemplos](-wic-samples.md)


[Direct2D](../direct2d/direct2d-portal.md)


 

 
