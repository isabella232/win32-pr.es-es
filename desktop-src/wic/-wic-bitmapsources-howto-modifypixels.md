---
description: En este tema se muestra cómo modificar los píxeles de un origen de mapa de bits mediante los componentes IWICBitmap y IWICBitmapLock.
ms.assetid: a08af015-bc42-4a31-af03-106714b08d08
title: Cómo modificar los píxeles de un origen de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be623d540fcd313476ea5c7ec5e724231d33aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706498"
---
# <a name="how-to-modify-the-pixels-of-a-bitmap-source"></a><span data-ttu-id="3fb1d-103">Cómo modificar los píxeles de un origen de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="3fb1d-103">How to Modify the Pixels of a Bitmap Source</span></span>

<span data-ttu-id="3fb1d-104">En este tema se muestra cómo modificar los píxeles de un origen de mapa de bits mediante los componentes [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) y [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="3fb1d-104">This topic demonstrates how to modify the pixels of a bitmap source using the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) and [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) components.</span></span>

<span data-ttu-id="3fb1d-105">Para modificar los píxeles de un origen de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="3fb1d-105">To modify the pixels of a bitmap source</span></span>

1.  <span data-ttu-id="3fb1d-106">Cree un objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para crear objetos de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="3fb1d-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="3fb1d-107">Use el método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para crear un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="3fb1d-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="3fb1d-108">Obtiene el primer [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3fb1d-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="3fb1d-109">El formato de archivo JPEG solo admite un único fotograma.</span><span class="sxs-lookup"><span data-stu-id="3fb1d-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="3fb1d-110">Dado que el archivo de este ejemplo es un archivo JPEG, se usa el primer fotograma ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="3fb1d-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="3fb1d-111">Para obtener información sobre los formatos de imagen que tienen varios fotogramas, consulte [recuperación de los marcos de una imagen](-wic-bitmapsources-howto-retrieveimageframes.md) para tener acceso a cada fotograma de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3fb1d-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="3fb1d-112">Cree un [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) a partir del fotograma de imagen obtenido previamente.</span><span class="sxs-lookup"><span data-stu-id="3fb1d-112">Create an [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) from the previously obtained image frame.</span></span>

    ```C++
    IWICBitmap *pIBitmap = NULL;
    IWICBitmapLock *pILock = NULL;

    UINT uiWidth = 10;
    UINT uiHeight = 10;

    WICRect rcLock = { 0, 0, uiWidth, uiHeight };

    // Create the bitmap from the image frame.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFromSource(
          pIDecoderFrame,          // Create a bitmap from the image frame
          WICBitmapCacheOnDemand,  // Cache metadata when needed
          &pIBitmap);              // Pointer to the bitmap
    }
    ```

    

5.  <span data-ttu-id="3fb1d-113">Obtiene un [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) para un rectángulo especificado de [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap).</span><span class="sxs-lookup"><span data-stu-id="3fb1d-113">Obtain an [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) for a specified rectangle of the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap).</span></span>

    ```C++
    if (SUCCEEDED(hr))
    {
       // Obtain a bitmap lock for exclusive write.
       // The lock is for a 10x10 rectangle starting at the top left of the
       // bitmap.
       hr = pIBitmap->Lock(&rcLock, WICBitmapLockWrite, &pILock);
    ```

    

6.  <span data-ttu-id="3fb1d-114">Procesa los datos de píxeles que ahora están bloqueados por el objeto [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="3fb1d-114">Process the pixel data that is now locked by the [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

    ```C++
       if (SUCCEEDED(hr))
       {
          UINT cbBufferSize = 0;
          BYTE *pv = NULL;

          // Retrieve a pointer to the pixel data.
          if (SUCCEEDED(hr))
          {
             hr = pILock->GetDataPointer(&cbBufferSize, &pv);
          }
          
          // Pixel manipulation using the image data pointer pv.
          // ...

          // Release the bitmap lock.
          SafeRelease(&pILock);
       }
    }
    ```

    

    <span data-ttu-id="3fb1d-115">Para desbloquear [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), llame a [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en todos los objetos [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) asociados al **IWICBitmap**.</span><span class="sxs-lookup"><span data-stu-id="3fb1d-115">To unlock the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), call [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) objects associated with the **IWICBitmap**.</span></span>

7.  <span data-ttu-id="3fb1d-116">Limpie los objetos creados.</span><span class="sxs-lookup"><span data-stu-id="3fb1d-116">Clean up created objects.</span></span>

    ```C++
    SafeRelease(&pIBitmap);
    SafeRelease(&pIDecoder);
    SafeRelease(&pIDecoderFrame);
    ```

    

## <a name="see-also"></a><span data-ttu-id="3fb1d-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3fb1d-117">See Also</span></span>

[<span data-ttu-id="3fb1d-118">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="3fb1d-118">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="3fb1d-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="3fb1d-119">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="3fb1d-120">Muestras</span><span class="sxs-lookup"><span data-stu-id="3fb1d-120">Samples</span></span>](-wic-samples.md)


 

 
