---
title: Cómo cargar un mapa de bits desde un recurso (Direct2D)
description: Muestra cómo cargar un mapa de bits de Direct2D almacenado como un recurso de aplicación.
ms.assetid: 7285e6ea-ebc7-4693-8a77-99bff0b5d0d1
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: fe96ba4e0674392333173df7daeb5a354a379343
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676529"
---
# <a name="how-to-load-a-bitmap-from-a-resource-direct2d"></a><span data-ttu-id="454d0-103">Cómo cargar un mapa de bits desde un recurso (Direct2D)</span><span class="sxs-lookup"><span data-stu-id="454d0-103">How to Load a Bitmap from a Resource (Direct2D)</span></span>

<span data-ttu-id="454d0-104">Como se describe en [Cómo cargar un mapa de bits desde un archivo](how-to-load-a-direct2d-bitmap-from-a-file.md), Direct2D usa el componente de creación de imágenes de Windows (WIC) para cargar los mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="454d0-104">As described in [How to Load a Bitmap from a File](how-to-load-a-direct2d-bitmap-from-a-file.md), Direct2D uses the Windows Imaging Component (WIC) to load bitmaps.</span></span> <span data-ttu-id="454d0-105">Para cargar un mapa de bits desde un recurso, utilice objetos WIC para cargar la imagen y convertirla a un formato compatible con Direct2D; a continuación, use el método [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para crear un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="454d0-105">To load a bitmap from a resource, use WIC objects to load the image and to convert it to a Direct2D-compatible format; then, use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

1.  <span data-ttu-id="454d0-106">En el [archivo de definición de recursos](/windows/desktop/menurc/about-resource-files)de la aplicación, defina el recurso.</span><span class="sxs-lookup"><span data-stu-id="454d0-106">In the [application resource definition file](/windows/desktop/menurc/about-resource-files), define the resource.</span></span> <span data-ttu-id="454d0-107">En el ejemplo siguiente se define un recurso denominado "SampleImage".</span><span class="sxs-lookup"><span data-stu-id="454d0-107">The following example defines a resource named "SampleImage".</span></span>

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

<span data-ttu-id="454d0-108">Este recurso se agregará al archivo de recursos de la aplicación cuando se compile la aplicación.</span><span class="sxs-lookup"><span data-stu-id="454d0-108">This resource will be added to the application's resource file when the application is built.</span></span>

2.  <span data-ttu-id="454d0-109">Cargue la imagen desde el archivo de recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="454d0-109">Load the image from the application resource file.</span></span>

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

    

3.  <span data-ttu-id="454d0-110">Bloquear el recurso y calcular el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="454d0-110">Lock the resource and calculate the image's size.</span></span>
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

    

4.  <span data-ttu-id="454d0-111">Use el método [**IWICImagingFactory:: CreateStream (**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) para crear un objeto [**IWICStream**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="454d0-111">Use the [**IWICImagingFactory::CreateStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) object.</span></span>
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

    

5.  <span data-ttu-id="454d0-112">Use el método [**IWICImagingFactory:: CreateDecoderFromStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) para crear un [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="454d0-112">Use the [**IWICImagingFactory::CreateDecoderFromStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method to create an [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

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

    

6.  <span data-ttu-id="454d0-113">Recupere un fotograma de la imagen y almacénelo en un objeto [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="454d0-113">Retrieve a frame from the image and store it in an [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

7.  <span data-ttu-id="454d0-114">Antes de que Direct2D pueda usar la imagen, se debe convertir al formato de píxel 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="454d0-114">Before Direct2D can use the image, it must be converted to the 32bppPBGRA pixel format.</span></span> <span data-ttu-id="454d0-115">Para convertir el formato de imagen, use el método [**IWICImagingFactory:: CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) para crear un objeto [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) y, a continuación, use el método [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) del objeto **IWICFormatConverter** para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="454d0-115">To convert the image format, use the [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) object, then use the **IWICFormatConverter** object's [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>
 
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

    

8.  <span data-ttu-id="454d0-116">Por último, use el método [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para crear un objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que pueda ser dibujado por un destino de representación y que se use con otros objetos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="454d0-116">Finally, use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object that can be drawn by a render target and used with other Direct2D objects.</span></span>
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

    

<span data-ttu-id="454d0-117">En este ejemplo se ha omitido código.</span><span class="sxs-lookup"><span data-stu-id="454d0-117">Some code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="454d0-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="454d0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="454d0-119">Cómo cargar un mapa de bits desde un archivo</span><span class="sxs-lookup"><span data-stu-id="454d0-119">How to Load a Bitmap from a File</span></span>](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

 
