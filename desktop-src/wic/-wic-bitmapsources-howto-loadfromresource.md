---
description: En este tema se muestra cómo cargar un IWICBitmapFrameDecode desde un recurso de aplicación.
ms.assetid: 2260ad3a-44d4-4fe2-aa8c-608ffc11fbfb
title: Cómo cargar un mapa de bits desde un recurso (componente de Windows Imaging)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb33ad57b3b9dac1cb5d98719c681adb38c11de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910426"
---
# <a name="how-to-load-a-bitmap-from-a-resource-windows-imaging-component"></a><span data-ttu-id="5b0ba-103">Cómo cargar un mapa de bits desde un recurso (componente de Windows Imaging)</span><span class="sxs-lookup"><span data-stu-id="5b0ba-103">How to Load a Bitmap from a Resource (Windows Imaging Component)</span></span>

<span data-ttu-id="5b0ba-104">En este tema se muestra cómo cargar un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) desde un recurso de aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b0ba-104">This topic demonstrates how to load an [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) from an application resource.</span></span>

1.  <span data-ttu-id="5b0ba-105">En el archivo de definición de recursos de la aplicación (. RC), defina el recurso.</span><span class="sxs-lookup"><span data-stu-id="5b0ba-105">In the application resource definition (.rc) file , define the resource.</span></span> <span data-ttu-id="5b0ba-106">En el ejemplo siguiente se define un `Image` recurso denominado `IDR_SAMPLE_IMAGE` .</span><span class="sxs-lookup"><span data-stu-id="5b0ba-106">The following example defines an `Image` resource named `IDR_SAMPLE_IMAGE`.</span></span>

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    <span data-ttu-id="5b0ba-107">El recurso se agregará a los recursos de la aplicación cuando se compile la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b0ba-107">The resource will be added to the application's resources when the application is built.</span></span>

2.  <span data-ttu-id="5b0ba-108">Cargue el recurso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b0ba-108">Load the resource from the application.</span></span>

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

    

3.  <span data-ttu-id="5b0ba-109">Bloquee el recurso y obtenga el tamaño.</span><span class="sxs-lookup"><span data-stu-id="5b0ba-109">Lock the resource and get the size.</span></span>

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

    

4.  <span data-ttu-id="5b0ba-110">Use el método [**CreateStream (**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) para crear un objeto [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) e inicializarlo con el puntero de memoria de imagen.</span><span class="sxs-lookup"><span data-stu-id="5b0ba-110">Use the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object and initialize it by using the image memory pointer.</span></span>

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

    

5.  <span data-ttu-id="5b0ba-111">Cree una [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) desde el nuevo objeto de secuencia mediante el método [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="5b0ba-111">Create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from the new stream object by using the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

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

    

6.  <span data-ttu-id="5b0ba-112">Recupere un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen descodificada.</span><span class="sxs-lookup"><span data-stu-id="5b0ba-112">Retrieve an [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) from the decoded image.</span></span>

    ```C++
    // Retrieve the initial frame.
    if (SUCCEEDED(hr)){
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="5b0ba-113">Este código solo recupera el primer `0` fotograma () de la imagen.</span><span class="sxs-lookup"><span data-stu-id="5b0ba-113">This code only retrieves the first (`0`) frame of the image.</span></span> <span data-ttu-id="5b0ba-114">En el caso de las imágenes con varios marcos, use [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) para determinar el número de fotogramas de la imagen.</span><span class="sxs-lookup"><span data-stu-id="5b0ba-114">For multi-framed images, use [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) to determine the number of frames in the image.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b0ba-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5b0ba-115">See Also</span></span>

[<span data-ttu-id="5b0ba-116">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="5b0ba-116">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="5b0ba-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="5b0ba-117">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="5b0ba-118">Muestras</span><span class="sxs-lookup"><span data-stu-id="5b0ba-118">Samples</span></span>](-wic-samples.md)


 

 



