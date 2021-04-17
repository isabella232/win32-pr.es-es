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
# <a name="how-to-clip-a-bitmap-source"></a><span data-ttu-id="78a73-103">Cómo recortar un origen de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="78a73-103">How to Clip a Bitmap Source</span></span>

<span data-ttu-id="78a73-104">En este tema se muestra cómo obtener una parte rectangular de un elemento [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mediante un componente [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="78a73-104">This topic demonstrates how to obtain a rectangular portion of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using an [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) component.</span></span>

<span data-ttu-id="78a73-105">Para recortar un origen de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="78a73-105">To clip a bitmap source</span></span>

1.  <span data-ttu-id="78a73-106">Cree un objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para crear objetos de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="78a73-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="78a73-107">Use el método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para crear un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="78a73-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="78a73-108">Obtiene el primer [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen.</span><span class="sxs-lookup"><span data-stu-id="78a73-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="78a73-109">El formato de archivo JPEG solo admite un único fotograma.</span><span class="sxs-lookup"><span data-stu-id="78a73-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="78a73-110">Dado que el archivo de este ejemplo es un archivo JPEG, se usa el primer fotograma ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="78a73-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="78a73-111">Para obtener información sobre los formatos de imagen que tienen varios fotogramas, consulte [recuperación de los marcos de una imagen](-wic-bitmapsources-howto-retrieveimageframes.md) para tener acceso a cada fotograma de la imagen.</span><span class="sxs-lookup"><span data-stu-id="78a73-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="78a73-112">Cree el [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) que se va a usar para el recorte de la imagen.</span><span class="sxs-lookup"><span data-stu-id="78a73-112">Create the [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) to use for the image clipping.</span></span>

    ```C++
    IWICBitmapClipper *pIClipper = NULL;

    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapClipper(&pIClipper);
    }
    ```

    

5.  <span data-ttu-id="78a73-113">Inicializa el objeto Clipper con los datos de la imagen dentro del rectángulo especificado del marco de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="78a73-113">Initialize the clipper object with the image data within the given rectangle of the bitmap frame.</span></span>

    ```C++
    // Create the clipping rectangle.
    WICRect rcClip = { 0, 0, uiWidth/2, uiHeight/2 };

    // Initialize the clipper with the given rectangle of the frame's image data.
    if (SUCCEEDED(hr))
    {
       hr = pIClipper->Initialize(pIDecoderFrame, &rcClip);
    }
    ```

    

6.  <span data-ttu-id="78a73-114">Dibuje o procese la imagen recortada.</span><span class="sxs-lookup"><span data-stu-id="78a73-114">Draw or process the clipped image.</span></span>

    <span data-ttu-id="78a73-115">En la ilustración siguiente se muestra el recorte de imágenes.</span><span class="sxs-lookup"><span data-stu-id="78a73-115">The following illustration demonstrates imaging clipping.</span></span> <span data-ttu-id="78a73-116">La imagen original de la izquierda es 200 x 130 píxeles.</span><span class="sxs-lookup"><span data-stu-id="78a73-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="78a73-117">La imagen de la derecha es la imagen original recortada en un rectángulo definido como `{20,20,100,100}` .</span><span class="sxs-lookup"><span data-stu-id="78a73-117">The image on the right is the original image clipped to a rectangle defined as `{20,20,100,100}`.</span></span>

    ![Ilustración del recorte de imágenes](graphics/cliparegion_axisalignedclip.png)

## <a name="see-also"></a><span data-ttu-id="78a73-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="78a73-119">See Also</span></span>

[<span data-ttu-id="78a73-120">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="78a73-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="78a73-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="78a73-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="78a73-122">Muestras</span><span class="sxs-lookup"><span data-stu-id="78a73-122">Samples</span></span>](-wic-samples.md)


 

 



