---
description: En este tema se muestra cómo girar un elemento IWICBitmapSource mediante un componente IWICBitmapFlipRotator.
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: Cómo voltear y girar un origen de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f6a805144025f185a4f4793fc4fafb27d7695a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154177"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a><span data-ttu-id="4b319-103">Cómo voltear y girar un origen de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="4b319-103">How to Flip and Rotate a Bitmap Source</span></span>

<span data-ttu-id="4b319-104">En este tema se muestra cómo girar un elemento [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mediante un componente [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="4b319-104">This topic demonstrates how to rotate an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) by using an [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) component.</span></span>

<span data-ttu-id="4b319-105">Para voltear y girar un origen de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="4b319-105">To flip and rotate a bitmap source</span></span>

1.  <span data-ttu-id="4b319-106">Cree un objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para crear objetos de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="4b319-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="4b319-107">Use el método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para crear un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="4b319-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapFlipRotator *pIFlipRotator = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="4b319-108">Obtiene el primer [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen.</span><span class="sxs-lookup"><span data-stu-id="4b319-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="4b319-109">El formato de archivo JPEG solo admite un único fotograma.</span><span class="sxs-lookup"><span data-stu-id="4b319-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="4b319-110">Dado que el archivo de este ejemplo es un archivo JPEG, se usa el primer fotograma ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="4b319-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="4b319-111">Para obtener información sobre los formatos de imagen que tienen varios fotogramas, consulte [recuperación de los marcos de una imagen](-wic-bitmapsources-howto-retrieveimageframes.md) para tener acceso a cada fotograma de la imagen.</span><span class="sxs-lookup"><span data-stu-id="4b319-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="4b319-112">Cree el [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) que se usará para voltear la imagen.</span><span class="sxs-lookup"><span data-stu-id="4b319-112">Create the [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) to use for flipping the image.</span></span>

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  <span data-ttu-id="4b319-113">Inicialice el objeto Flip/Rotator con los datos de imagen del marco de mapa de bits volteados horizontalmente (a lo largo del eje y vertical).</span><span class="sxs-lookup"><span data-stu-id="4b319-113">Initialize the flip/rotator object with the image data of the bitmap frame flipped horizontally (along the vertical y-axis).</span></span>

    ```C++
    // Initialize the flip/rotator to flip the original source horizontally.
    if (SUCCEEDED(hr))
    {
       hr = pIFlipRotator->Initialize(
          pIDecoderFrame,                     // Bitmap source to flip.
          WICBitmapTransformFlipHorizontal);  // Flip the pixels along the 
                                              //  vertical y-axis.
    }
    ```

    

    <span data-ttu-id="4b319-114">Vea [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) para obtener más rotaciones y opciones de volteo.</span><span class="sxs-lookup"><span data-stu-id="4b319-114">See [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) for additional rotations and flipping options.</span></span>

6.  <span data-ttu-id="4b319-115">Dibuje o procese el origen del mapa de bits volteado.</span><span class="sxs-lookup"><span data-stu-id="4b319-115">Draw or process the flipped bitmap source.</span></span>

    > [!Note]  
    > <span data-ttu-id="4b319-116">La interfaz [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) se hereda de la interfaz [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , por lo que puede usar el objeto Flip/Rotator inicializado en cualquier lugar que acepte un objeto **IWICBitmapSource**.</span><span class="sxs-lookup"><span data-stu-id="4b319-116">The [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) interface inherits from the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, so you can use the initialized flip/rotator object anywhere that accepts a **IWICBitmapSource**.</span></span>

     

    <span data-ttu-id="4b319-117">En la ilustración siguiente se muestra cómo Voltear horizontalmente una imagen (a lo largo del eje x vertical).</span><span class="sxs-lookup"><span data-stu-id="4b319-117">The following illustration demonstrates flipping an imaging horizontally (along the vertical x-axis).</span></span>

    ![Ilustración en la que se muestra un volteo horizontal (a lo largo del eje x Verity) de una imagen](graphics/fliphorizontal.png)

## <a name="see-also"></a><span data-ttu-id="4b319-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4b319-119">See Also</span></span>

[<span data-ttu-id="4b319-120">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="4b319-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="4b319-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="4b319-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="4b319-122">Muestras</span><span class="sxs-lookup"><span data-stu-id="4b319-122">Samples</span></span>](-wic-samples.md)


 

 



