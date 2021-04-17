---
description: En este tema se describe cómo crear un descodificador de mapa de bits mediante el uso de un nombre de archivo de imagen.
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: Cómo crear un descodificador mediante un nombre de archivo de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113ea82b741f2a8dab6c92d6391d65eb7d7e99c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697656"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a><span data-ttu-id="1ad52-103">Cómo crear un descodificador mediante un nombre de archivo de imagen</span><span class="sxs-lookup"><span data-stu-id="1ad52-103">How to Create a Decoder Using an Image Filename</span></span>

<span data-ttu-id="1ad52-104">En este tema se describe cómo crear un descodificador de mapa de bits mediante el uso de un nombre de archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="1ad52-104">This topic describes how to create a bitmap decoder by using an image filename.</span></span>

<span data-ttu-id="1ad52-105">Para crear un descodificador de mapa de bits mediante un nombre de archivo de imagen</span><span class="sxs-lookup"><span data-stu-id="1ad52-105">To create a bitmap decoder by using an image filename</span></span>

1.  <span data-ttu-id="1ad52-106">Cree un objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para crear objetos de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="1ad52-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="1ad52-107">Use el método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para crear un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="1ad52-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="1ad52-108">Obtiene el primer [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen.</span><span class="sxs-lookup"><span data-stu-id="1ad52-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="1ad52-109">El formato de archivo JPEG solo admite un único fotograma.</span><span class="sxs-lookup"><span data-stu-id="1ad52-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="1ad52-110">Dado que el archivo de este ejemplo es un archivo JPEG, se usa el primer fotograma ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="1ad52-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="1ad52-111">Para obtener información sobre los formatos de imagen que tienen varios fotogramas, consulte [recuperación de los marcos de una imagen](-wic-bitmapsources-howto-retrieveimageframes.md) para tener acceso a cada fotograma de la imagen.</span><span class="sxs-lookup"><span data-stu-id="1ad52-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="1ad52-112">Procesa el marco de imagen.</span><span class="sxs-lookup"><span data-stu-id="1ad52-112">Process the image frame.</span></span> <span data-ttu-id="1ad52-113">Para obtener más información sobre los objetos de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , vea la [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="1ad52-113">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1ad52-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1ad52-114">See Also</span></span>

[<span data-ttu-id="1ad52-115">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="1ad52-115">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="1ad52-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="1ad52-116">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="1ad52-117">Muestras</span><span class="sxs-lookup"><span data-stu-id="1ad52-117">Samples</span></span>](-wic-samples.md)


 

 



