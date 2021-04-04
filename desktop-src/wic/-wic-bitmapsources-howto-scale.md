---
description: En este tema se muestra cómo escalar un elemento IWICBitmapSource mediante el componente IWICBitmapScaler.
ms.assetid: d2c65c9b-6f52-46f7-935d-0c582ca83867
title: Cómo escalar un origen de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737f72014929065bc63ec9c6021b05e38799d06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154175"
---
# <a name="how-to-scale-a-bitmap-source"></a><span data-ttu-id="ec2b1-103">Cómo escalar un origen de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="ec2b1-103">How to Scale a Bitmap Source</span></span>

<span data-ttu-id="ec2b1-104">En este tema se muestra cómo escalar un elemento [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mediante el componente [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="ec2b1-104">This topic demonstrates how to scale an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) component.</span></span>

<span data-ttu-id="ec2b1-105">Para escalar un origen de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="ec2b1-105">To scale a bitmap source</span></span>

1.  <span data-ttu-id="ec2b1-106">Cree un objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para crear objetos de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="ec2b1-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="ec2b1-107">Use el método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para crear un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="ec2b1-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapScaler *pIScaler = NULL;


    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="ec2b1-108">Obtiene el primer [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen.</span><span class="sxs-lookup"><span data-stu-id="ec2b1-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="ec2b1-109">El formato de archivo JPEG solo admite un único fotograma.</span><span class="sxs-lookup"><span data-stu-id="ec2b1-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="ec2b1-110">Dado que el archivo de este ejemplo es un archivo JPEG, se usa el primer fotograma ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="ec2b1-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="ec2b1-111">Para obtener información sobre los formatos de imagen que tienen varios fotogramas, consulte [recuperación de los marcos de una imagen](-wic-bitmapsources-howto-retrieveimageframes.md) para tener acceso a cada fotograma de la imagen.</span><span class="sxs-lookup"><span data-stu-id="ec2b1-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="ec2b1-112">Cree el [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) que se usará para el ajuste de escala de la imagen.</span><span class="sxs-lookup"><span data-stu-id="ec2b1-112">Create the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) to use for the image scaling.</span></span>

    ```C++
    // Create the scaler.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapScaler(&pIScaler);
    }
    ```

    

5.  <span data-ttu-id="ec2b1-113">Inicialice el objeto Scaler con los datos de imagen del marco de mapa de bits a la mitad del tamaño.</span><span class="sxs-lookup"><span data-stu-id="ec2b1-113">Initialize the scaler object with the image data of the bitmap frame at half the size.</span></span>

    ```C++
    // Initialize the scaler to half the size of the original source.
    if (SUCCEEDED(hr))
    {
       hr = pIScaler->Initialize(
          pIDecoderFrame,                    // Bitmap source to scale.
          uiWidth/2,                         // Scale width to half of original.
          uiHeight/2,                        // Scale height to half of original.
          WICBitmapInterpolationModeFant);   // Use Fant mode interpolation.
    }
    ```

    

6.  <span data-ttu-id="ec2b1-114">Dibuje o procese el origen de mapa de bits escalado.</span><span class="sxs-lookup"><span data-stu-id="ec2b1-114">Draw or process the scaled bitmap source.</span></span>

    <span data-ttu-id="ec2b1-115">En la ilustración siguiente se muestra el escalado de imágenes.</span><span class="sxs-lookup"><span data-stu-id="ec2b1-115">The following illustration demonstrates imaging scaling.</span></span> <span data-ttu-id="ec2b1-116">La imagen original de la izquierda es 200 x 130 píxeles.</span><span class="sxs-lookup"><span data-stu-id="ec2b1-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="ec2b1-117">La imagen de la derecha es la imagen original escalada hasta la mitad del tamaño.</span><span class="sxs-lookup"><span data-stu-id="ec2b1-117">The image on the right is the original image scaled to half the size.</span></span>

    ![Ilustración en la que se muestra el escalado de una imagen a un tamaño más pequeño](graphics/scaledregion.png)

## <a name="see-also"></a><span data-ttu-id="ec2b1-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ec2b1-119">See Also</span></span>

[<span data-ttu-id="ec2b1-120">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="ec2b1-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="ec2b1-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="ec2b1-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="ec2b1-122">Muestras</span><span class="sxs-lookup"><span data-stu-id="ec2b1-122">Samples</span></span>](-wic-samples.md)


 

 



