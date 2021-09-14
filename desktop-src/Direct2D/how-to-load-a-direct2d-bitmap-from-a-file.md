---
title: Cómo cargar un mapa de bits desde un archivo
description: Muestra cómo cargar un mapa de bits de Direct2D desde un archivo de imagen.
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: c9590e799e71e92056157b75573565cf79b9236b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163146"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a>Cómo cargar un mapa de bits desde un archivo

Direct2D usa el componente Windows imaging (WIC) para cargar mapas de bits. Para cargar un mapa de bits desde un archivo, use primero objetos WIC para cargar la imagen y convertirla a un formato compatible con Direct2D y, a continuación, use el método [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para crear un [**elemento ID2D1Bitmap.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)

1.  Cree un [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) mediante el método [**IWICImagingFactory::CreateDecoderFromFileName.**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)

    ```C++
    HRESULT DemoApp::LoadBitmapFromFile(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR uri,
        UINT destinationWidth,
        UINT destinationHeight,
        ID2D1Bitmap **ppBitmap
        )
    {
        IWICBitmapDecoder *pDecoder = NULL;
        IWICBitmapFrameDecode *pSource = NULL;
        IWICStream *pStream = NULL;
        IWICFormatConverter *pConverter = NULL;
        IWICBitmapScaler *pScaler = NULL;

        HRESULT hr = pIWICFactory->CreateDecoderFromFilename(
            uri,
            NULL,
            GENERIC_READ,
            WICDecodeMetadataCacheOnLoad,
            &pDecoder
            );
            
    ```

    

2.  Recupere un marco de la imagen y almacénelo en un [**objeto IWICBitmapFrameDecode.**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode)

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  El mapa de bits debe convertirse a un formato que Direct2D pueda usar, por lo que debe convertir el formato de píxel de la imagen a 32bppPBGRA. (Para obtener una lista de los formatos admitidos, vea [Formatos de píxeles y modos alfa).](supported-pixel-formats-and-alpha-modes.md) Llame al [**método IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) para crear un objeto [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) y, a continuación, llame al método [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) del objeto **IWICFormatConverter** para realizar la conversión.
    ```C++
        if (SUCCEEDED(hr))
        {

            // Convert the image format to 32bppPBGRA
            // (DXGI_FORMAT_B8G8R8A8_UNORM + D2D1_ALPHA_MODE_PREMULTIPLIED).
            hr = pIWICFactory->CreateFormatConverter(&pConverter);

        }
     
     
        if (SUCCEEDED(hr))
        {
            hr = pConverter->Initialize(
                pSource,
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                NULL,
                0.f,
                WICBitmapPaletteTypeMedianCut
                );
    ```

    

4.  Llame al [**método CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para crear un objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que un destino de representación puede dibujar y usar con otros objetos direct2D.
    ```C++
        if (SUCCEEDED(hr))
        {
        
            // Create a Direct2D bitmap from the WIC bitmap.
            hr = pRenderTarget->CreateBitmapFromWicBitmap(
                pConverter,
                NULL,
                ppBitmap
                );
        }

        SafeRelease(&pDecoder);
        SafeRelease(&pSource);
        SafeRelease(&pStream);
        SafeRelease(&pConverter);
        SafeRelease(&pScaler);

        return hr;
    }
    ```

    

En este ejemplo se ha omitido algún código.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[Cómo cargar un mapa de bits desde un recurso](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 