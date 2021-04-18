---
description: En este tema se muestra el proceso para dibujar un IWICBitmapSource mediante Direct2D.
ms.assetid: 11d38c9a-775d-41f7-a193-37b702b29a96
title: Cómo dibujar un BitmapSource mediante Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6dfdddb7cd6f7ab7341eb3c13a9fe40b797f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720532"
---
# <a name="how-to-draw-a-bitmapsource-using-direct2d"></a><span data-ttu-id="68f3e-103">Cómo dibujar un BitmapSource mediante Direct2D</span><span class="sxs-lookup"><span data-stu-id="68f3e-103">How to Draw a BitmapSource Using Direct2D</span></span>

<span data-ttu-id="68f3e-104">En este tema se muestra el proceso para dibujar un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mediante Direct2D.</span><span class="sxs-lookup"><span data-stu-id="68f3e-104">This topic demonstrates the process for drawing an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) by using Direct2D.</span></span>

<span data-ttu-id="68f3e-105">Para dibujar una fuente de mapa de bits mediante Direct2D</span><span class="sxs-lookup"><span data-stu-id="68f3e-105">To draw a bitmap source by using Direct2D</span></span>

1.  <span data-ttu-id="68f3e-106">Descodifique una imagen de origen y obtenga un origen de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="68f3e-106">Decode a source image and obtain a bitmap source.</span></span> <span data-ttu-id="68f3e-107">En este ejemplo, se usa [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) para descodificar la imagen y se recupera el primer fotograma de la imagen.</span><span class="sxs-lookup"><span data-stu-id="68f3e-107">In this example, an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) is used to decode the image and the first image frame is retrieved.</span></span>

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

    

    <span data-ttu-id="68f3e-108">Para obtener más [información sobre](-wic-bitmapsources.md)los tipos de orígenes de mapas de bits que se van a dibujar, vea la introducción a los orígenes</span><span class="sxs-lookup"><span data-stu-id="68f3e-108">For additional types of bitmap sources to draw, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

2.  <span data-ttu-id="68f3e-109">Convierta el origen del mapa de bits a un formato de píxel de 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="68f3e-109">Convert the bitmap source to an 32bppPBGRA pixel format.</span></span>

    <span data-ttu-id="68f3e-110">Antes de que Direct2D pueda usar una imagen, se debe convertir al formato de píxel 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="68f3e-110">Before Direct2D can use an image, it must be converted to the 32bppPBGRA pixel format.</span></span> <span data-ttu-id="68f3e-111">Para convertir el formato de imagen, use el método [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) para crear un objeto [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="68f3e-111">To convert the image format, use the [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span> <span data-ttu-id="68f3e-112">Una vez creado, use el método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="68f3e-112">Once created, use the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>

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

    

3.  <span data-ttu-id="68f3e-113">Cree un objeto [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) para la representación en un identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="68f3e-113">Create an [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) object for rendering to a window handle.</span></span>

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

    

    <span data-ttu-id="68f3e-114">Para obtener más información sobre los destinos de representación, consulte [información general de destinos de representación](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="68f3e-114">For more information render targets, see the Direct2D [Render Targets Overview](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span>

4.  <span data-ttu-id="68f3e-115">Cree un objeto [ID2D1Bitmap](../direct2d/render-targets-overview.md) mediante el método [ID2D1RenderTarget:: CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) .</span><span class="sxs-lookup"><span data-stu-id="68f3e-115">Create an [ID2D1Bitmap](../direct2d/render-targets-overview.md) object using the [ID2D1RenderTarget::CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) method.</span></span>

    ```C++
        // D2DBitmap may have been released due to device loss. 
        // If so, re-create it from the source bitmap
        if (m_pConvertedSourceBitmap && !m_pD2DBitmap)
        {
            m_pRT->CreateBitmapFromWicBitmap(m_pConvertedSourceBitmap, NULL, &m_pD2DBitmap);
        }
    ```

    

5.  <span data-ttu-id="68f3e-116">Dibuje el [ID2D1Bitmap](../direct2d/render-targets-overview.md) mediante D2D [ID2D1RenderTarget::D rawbitmap](../direct2d/id2d1rendertarget-drawbitmap.md) método.</span><span class="sxs-lookup"><span data-stu-id="68f3e-116">Draw the [ID2D1Bitmap](../direct2d/render-targets-overview.md) using D2D [ID2D1RenderTarget::DrawBitmap](../direct2d/id2d1rendertarget-drawbitmap.md) method.</span></span>

    ```C++
        // Draws an image and scales it to the current window size
        if (m_pD2DBitmap)
        {
            m_pRT->DrawBitmap(m_pD2DBitmap, rectangle);
        }
    ```

    

<span data-ttu-id="68f3e-117">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="68f3e-117">Code has been omitted from this example.</span></span> <span data-ttu-id="68f3e-118">Para obtener el código completo, vea el [visor de imágenes de WIC con el ejemplo de Direct2D](-wic-sample-d2d-viewer.md).</span><span class="sxs-lookup"><span data-stu-id="68f3e-118">For the complete code, see the [WIC Image Viewer Using Direct2D Sample](-wic-sample-d2d-viewer.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="68f3e-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="68f3e-119">See Also</span></span>

[<span data-ttu-id="68f3e-120">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="68f3e-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="68f3e-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="68f3e-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="68f3e-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="68f3e-122">Samples</span></span>](-wic-samples.md)


[<span data-ttu-id="68f3e-123">Direct2D</span><span class="sxs-lookup"><span data-stu-id="68f3e-123">Direct2D</span></span>](../direct2d/direct2d-portal.md)


 

 
