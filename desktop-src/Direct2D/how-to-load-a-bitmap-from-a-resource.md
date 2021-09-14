---
title: Cómo cargar un mapa de bits desde un recurso (Direct2D)
description: Muestra cómo cargar un mapa de bits de Direct2D almacenado como un recurso de aplicación.
ms.assetid: 7285e6ea-ebc7-4693-8a77-99bff0b5d0d1
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: fe96ba4e0674392333173df7daeb5a354a379343
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163154"
---
# <a name="how-to-load-a-bitmap-from-a-resource-direct2d"></a>Cómo cargar un mapa de bits desde un recurso (Direct2D)

Como se describe [en Carga de](how-to-load-a-direct2d-bitmap-from-a-file.md)un mapa de bits desde un archivo , Direct2D usa el componente Windows Imaging Component (WIC) para cargar mapas de bits. Para cargar un mapa de bits desde un recurso, use objetos WIC para cargar la imagen y convertirla a un formato compatible con Direct2D. a continuación, use [**el método CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para crear un [**id2D1Bitmap.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)

1.  En el archivo [de definición de recursos de](/windows/desktop/menurc/about-resource-files)la aplicación, defina el recurso. En el ejemplo siguiente se define un recurso denominado "SampleImage".

    ```C++
    // THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
    // ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
    // THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
    // PARTICULAR PURPOSE.
    //
    // Copyright (c) Microsoft Corporation. All rights reserved
    #include "windows.h"

    SampleImage Image "sampleImage.jpg"
    ```

Este recurso se agregará al archivo de recursos de la aplicación cuando se haya creado la aplicación.

2.  Cargue la imagen desde el archivo de recursos de la aplicación.

    ```C++
    HRESULT DemoApp::LoadResourceBitmap(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR resourceName,
        PCWSTR resourceType,
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

        HRSRC imageResHandle = NULL;
        HGLOBAL imageResDataHandle = NULL;
        void *pImageFile = NULL;
        DWORD imageFileSize = 0;

        // Locate the resource.
        imageResHandle = FindResourceW(HINST_THISCOMPONENT, resourceName, resourceType);
        HRESULT hr = imageResHandle ? S_OK : E_FAIL;
        if (SUCCEEDED(hr))
        {
            // Load the resource.
            imageResDataHandle = LoadResource(HINST_THISCOMPONENT, imageResHandle);

            hr = imageResDataHandle ? S_OK : E_FAIL;
        }
    ```

    

3.  Bloquee el recurso y calcule el tamaño de la imagen.
    ```C++
        if (SUCCEEDED(hr))
        {
            // Lock it to get a system memory pointer.
            pImageFile = LockResource(imageResDataHandle);

            hr = pImageFile ? S_OK : E_FAIL;
        }
        if (SUCCEEDED(hr))
        {
            // Calculate the size.
            imageFileSize = SizeofResource(HINST_THISCOMPONENT, imageResHandle);

            hr = imageFileSize ? S_OK : E_FAIL;
            
        }
    ```

    

4.  Use el [**método IWICImagingFactory::CreateStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) para crear un [**objeto IWICStream.**](/windows/win32/api/wincodec/nn-wincodec-iwicstream)
    ```C++
        if (SUCCEEDED(hr))
        {
              // Create a WIC stream to map onto the memory.
            hr = pIWICFactory->CreateStream(&pStream);
        }
        if (SUCCEEDED(hr))
        {
            // Initialize the stream with the memory pointer and size.
            hr = pStream->InitializeFromMemory(
                reinterpret_cast<BYTE*>(pImageFile),
                imageFileSize
                );
        }
    ```

    

5.  Use el [**método IWICImagingFactory::CreateDecoderFromStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) para crear un [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create a decoder for the stream.
            hr = pIWICFactory->CreateDecoderFromStream(
                pStream,
                NULL,
                WICDecodeMetadataCacheOnLoad,
                &pDecoder
                );
        }
    ```

    

6.  Recupere un marco de la imagen y almacénelo en un [**objeto IWICBitmapFrameDecode.**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode)

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

7.  Para que Direct2D pueda usar la imagen, debe convertirse al formato de píxeles 32bppPBGRA. Para convertir el formato de imagen, use el método [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) para crear un objeto [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) y, a continuación, use el método [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) del objeto **IWICFormatConverter** para realizar la conversión.
 
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

    

8.  Por último, use el [**método CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para crear un objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que un destino de representación pueda dibujar y usar con otros objetos de Direct2D.
    ```C++
        if (SUCCEEDED(hr))
        {
            //create a Direct2D bitmap from the WIC bitmap.
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

[Cómo cargar un mapa de bits desde un archivo](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

 
