---
description: En este tema se describe cómo crear un descodificador de mapa de bits mediante un flujo.
ms.assetid: 982d2110-ff2f-43e0-a931-cb2b8146ad0a
title: Cómo crear un descodificador mediante un flujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a76badec0e2587f9136cfa6bc3ff041b76592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697810"
---
# <a name="how-to-create-a-decoder-using-a-stream"></a><span data-ttu-id="eb96c-103">Cómo crear un descodificador mediante un flujo</span><span class="sxs-lookup"><span data-stu-id="eb96c-103">How to Create a Decoder Using a Stream</span></span>

<span data-ttu-id="eb96c-104">En este tema se describe cómo crear un descodificador de mapa de bits mediante un flujo.</span><span class="sxs-lookup"><span data-stu-id="eb96c-104">This topic describes how to create a bitmap decoder by using a stream.</span></span>

<span data-ttu-id="eb96c-105">Para crear un descodificador de mapa de bits mediante un flujo</span><span class="sxs-lookup"><span data-stu-id="eb96c-105">To create a bitmap decoder by using a stream</span></span>

1.  <span data-ttu-id="eb96c-106">Cargar un archivo de imagen en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="eb96c-106">Load an image file into a stream.</span></span> <span data-ttu-id="eb96c-107">En este ejemplo, se crea un flujo para un recurso de aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb96c-107">In this example, a stream is created for an application resource.</span></span>

    <span data-ttu-id="eb96c-108">En el archivo de definición de recursos de la aplicación (. RC), defina el recurso.</span><span class="sxs-lookup"><span data-stu-id="eb96c-108">In the application resource definition (.rc) file, define the resource.</span></span> <span data-ttu-id="eb96c-109">En el ejemplo siguiente se define un `Image` recurso denominado `IDR_SAMPLE_IMAGE` .</span><span class="sxs-lookup"><span data-stu-id="eb96c-109">The following example defines an `Image` resource named `IDR_SAMPLE_IMAGE`.</span></span>

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    <span data-ttu-id="eb96c-110">El recurso se agregará a los recursos de la aplicación cuando se compile la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb96c-110">The resource will be added to the application's resources when the application is built.</span></span>

2.  <span data-ttu-id="eb96c-111">Cargue el recurso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb96c-111">Load the resource from the application.</span></span>

    ```C++
    HRESULT hr = S_OK;

    // WIC interface pointers.
    IWICStream *pIWICStream = NULL;
    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame = NULL;

    // Resource management.
    HRSRC imageResHandle = NULL;
    HGLOBAL imageResDataHandle = NULL;
    void *pImageFile = NULL;
    DWORD imageFileSize = 0;

    // Locate the resource in the application's executable.
    imageResHandle = FindResource(
       NULL,             // This component.
       L"SampleImage",   // Resource name.
       L"Image");        // Resource type.

    hr = (imageResHandle ? S_OK : E_FAIL);

    // Load the resource to the HGLOBAL.
    if (SUCCEEDED(hr)){
       imageResDataHandle = LoadResource(NULL, imageResHandle);
       hr = (imageResDataHandle ? S_OK : E_FAIL);
    }
    
    ```

    

3.  <span data-ttu-id="eb96c-112">Bloquee el recurso y obtenga el tamaño.</span><span class="sxs-lookup"><span data-stu-id="eb96c-112">Lock the resource and get the size.</span></span>

    ```C++
    // Lock the resource to retrieve memory pointer.
    if (SUCCEEDED(hr)){
       pImageFile = LockResource(imageResDataHandle);
       hr = (pImageFile ? S_OK : E_FAIL);
    }

    // Calculate the size.
    if (SUCCEEDED(hr)){
       imageFileSize = SizeofResource(NULL, imageResHandle);
       hr = (imageFileSize ? S_OK : E_FAIL);
    }
    
    ```

    

4.  <span data-ttu-id="eb96c-113">Cree un [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para crear objetos de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="eb96c-113">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  <span data-ttu-id="eb96c-114">Use el método [**CreateStream (**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) para crear un objeto [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) e inicializarlo con el puntero de memoria de imagen.</span><span class="sxs-lookup"><span data-stu-id="eb96c-114">Use the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object and initialize it by using the image memory pointer.</span></span>

    ```C++
    // Create a WIC stream to map onto the memory.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateStream(&pIWICStream);
    }

    // Initialize the stream with the memory pointer and size.
    if (SUCCEEDED(hr)){
       hr = pIWICStream->InitializeFromMemory(
             reinterpret_cast<BYTE*>(pImageFile),
             imageFileSize);
    }
    ```

    

6.  <span data-ttu-id="eb96c-115">Cree una [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) desde el nuevo objeto de secuencia mediante el método [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="eb96c-115">Create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from the new stream object using the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

    ```C++
    // Create a decoder for the stream.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateDecoderFromStream(
          pIWICStream,                   // The stream to use to create the decoder
          NULL,                          // Do not prefer a particular vendor
          WICDecodeMetadataCacheOnLoad,  // Cache metadata when needed
          &pIDecoder);                   // Pointer to the decoder
    }
    ```

    

7.  <span data-ttu-id="eb96c-116">Obtiene el primer [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen.</span><span class="sxs-lookup"><span data-stu-id="eb96c-116">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="eb96c-117">El formato de archivo JPEG solo admite un único fotograma.</span><span class="sxs-lookup"><span data-stu-id="eb96c-117">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="eb96c-118">Dado que el archivo de este ejemplo es un archivo JPEG, se usa el primer fotograma ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="eb96c-118">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="eb96c-119">Para obtener información sobre los formatos de imagen que tienen varios fotogramas, consulte [recuperación de los marcos de una imagen](-wic-bitmapsources-howto-retrieveimageframes.md) para tener acceso a cada fotograma de la imagen.</span><span class="sxs-lookup"><span data-stu-id="eb96c-119">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

8.  <span data-ttu-id="eb96c-120">Procesa el marco de imagen.</span><span class="sxs-lookup"><span data-stu-id="eb96c-120">Process the image frame.</span></span> <span data-ttu-id="eb96c-121">Para obtener más información sobre los objetos de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , vea la [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="eb96c-121">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="eb96c-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="eb96c-122">See Also</span></span>

[<span data-ttu-id="eb96c-123">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="eb96c-123">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="eb96c-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="eb96c-124">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="eb96c-125">Muestras</span><span class="sxs-lookup"><span data-stu-id="eb96c-125">Samples</span></span>](-wic-samples.md)


 

 



