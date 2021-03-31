---
title: Cómo cargar un mapa de bits desde un archivo
description: Muestra cómo cargar un mapa de bits de Direct2D desde un archivo de imagen.
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: c9590e799e71e92056157b75573565cf79b9236b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792825"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a><span data-ttu-id="74058-103">Cómo cargar un mapa de bits desde un archivo</span><span class="sxs-lookup"><span data-stu-id="74058-103">How to Load a Bitmap from a File</span></span>

<span data-ttu-id="74058-104">Direct2D usa el componente de creación de imágenes de Windows (WIC) para cargar mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="74058-104">Direct2D uses the Windows Imaging Component (WIC) to load bitmaps.</span></span> <span data-ttu-id="74058-105">Para cargar un mapa de bits desde un archivo, use primero objetos de WIC para cargar la imagen y convertirla a un formato compatible con Direct2D y, a continuación, use el método [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para crear un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="74058-105">To load a bitmap from a file, first use WIC objects to load the image and to convert it to a Direct2D-compatible format, then use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

1.  <span data-ttu-id="74058-106">Cree un [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) mediante el método [**IWICImagingFactory:: CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .</span><span class="sxs-lookup"><span data-stu-id="74058-106">Create an [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) by using the [**IWICImagingFactory::CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

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

    

2.  <span data-ttu-id="74058-107">Recupere un fotograma de la imagen y almacene el marco en un objeto [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="74058-107">Retrieve a frame from the image and store the frame in an [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  <span data-ttu-id="74058-108">El mapa de bits se debe convertir a un formato que pueda usar Direct2D, de modo que convierta el formato de píxel de la imagen en 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="74058-108">The bitmap must be converted to a format that Direct2D can use, so convert the image's pixel format to 32bppPBGRA.</span></span> <span data-ttu-id="74058-109">(Para obtener una lista de formatos admitidos, vea [formatos de píxeles y modos alfa](supported-pixel-formats-and-alpha-modes.md)).</span><span class="sxs-lookup"><span data-stu-id="74058-109">(For a list of supported formats, see [Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).).</span></span> <span data-ttu-id="74058-110">Llame al método [**IWICImagingFactory:: CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) para crear un objeto [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) y, a continuación, llame al método [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) del objeto **IWICFormatConverter** para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="74058-110">Call the [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) object, then call the **IWICFormatConverter** object's [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>
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

    

4.  <span data-ttu-id="74058-111">Llame al método [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para crear un objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que pueda ser dibujado por un destino de representación y que se use con otros objetos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="74058-111">Call the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object that can be drawn by a render target and used with other Direct2D objects.</span></span>
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

    

<span data-ttu-id="74058-112">En este ejemplo se ha omitido código.</span><span class="sxs-lookup"><span data-stu-id="74058-112">Some code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74058-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74058-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74058-114">**ID2D1Bitmap**</span><span class="sxs-lookup"><span data-stu-id="74058-114">**ID2D1Bitmap**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[<span data-ttu-id="74058-115">**CreateBitmapFromWicBitmap**</span><span class="sxs-lookup"><span data-stu-id="74058-115">**CreateBitmapFromWicBitmap**</span></span>](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[<span data-ttu-id="74058-116">Cómo cargar un mapa de bits desde un recurso</span><span class="sxs-lookup"><span data-stu-id="74058-116">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 