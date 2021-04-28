---
description: Creación de un procesador de vídeo DXVA-HD
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: Creación de un procesador de vídeo DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89c5a361335f83296eec538a5a6a710b9e19604
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102603"
---
# <a name="creating-a-dxva-hd-video-processor"></a><span data-ttu-id="48e0d-103">Creación de un procesador de vídeo DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="48e0d-103">Creating a DXVA-HD Video Processor</span></span>

<span data-ttu-id="48e0d-104">La alta definición de aceleración de vídeo de Microsoft DirectX (DXVA-HD) usa dos interfaces principales:</span><span class="sxs-lookup"><span data-stu-id="48e0d-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) uses two primary interfaces:</span></span>

-   <span data-ttu-id="48e0d-105">[**IDXVAHD \_ Dispositivo**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span><span class="sxs-lookup"><span data-stu-id="48e0d-105">[**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span></span> <span data-ttu-id="48e0d-106">Representa el dispositivo DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="48e0d-106">Represents the DXVA-HD device.</span></span> <span data-ttu-id="48e0d-107">Use esta interfaz para consultar las funcionalidades del dispositivo y crear el procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="48e0d-107">Use this interface to query the device capabilities and create the video processor.</span></span>
-   <span data-ttu-id="48e0d-108">[**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span><span class="sxs-lookup"><span data-stu-id="48e0d-108">[**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span></span> <span data-ttu-id="48e0d-109">Representa un conjunto de funcionalidades de procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="48e0d-109">Represents a set of video processing capabilities.</span></span> <span data-ttu-id="48e0d-110">Use esta interfaz para realizar el procesamiento de vídeo blit.</span><span class="sxs-lookup"><span data-stu-id="48e0d-110">Use this interface to perform the video processing blit.</span></span>

<span data-ttu-id="48e0d-111">En el código siguiente, se suponen las siguientes variables globales:</span><span class="sxs-lookup"><span data-stu-id="48e0d-111">In the code that follows, the following global variables are assumed:</span></span>


```C++
IDirect3D9Ex            *g_pD3D = NULL;     
IDirect3DDevice9Ex      *g_pD3DDevice = NULL;   // Direct3D device.
IDXVAHD_Device          *g_pDXVAHD = NULL;      // DXVA-HD device.
IDXVAHD_VideoProcessor  *g_pDXVAVP = NULL;      // DXVA-HD video processor.
IDirect3DSurface9       *g_pSurface = NULL;     // Video surface.
        
const D3DFORMAT     RENDER_TARGET_FORMAT = D3DFMT_X8R8G8B8;
const D3DFORMAT     VIDEO_FORMAT         = D3DFMT_X8R8G8B8; 
const UINT          VIDEO_FPS            = 60;
const UINT          VIDEO_WIDTH          = 640;
const UINT          VIDEO_HEIGHT         = 480;
```



<span data-ttu-id="48e0d-112">Para crear un procesador de vídeo DXVA-HD:</span><span class="sxs-lookup"><span data-stu-id="48e0d-112">To create a DXVA-HD video processor:</span></span>

1.  <span data-ttu-id="48e0d-113">Rellene una [**estructura DXVAHD \_ CONTENT \_ DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) con una descripción del contenido del vídeo.</span><span class="sxs-lookup"><span data-stu-id="48e0d-113">Fill in a [**DXVAHD\_CONTENT\_DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) structure with a description of the video content.</span></span> <span data-ttu-id="48e0d-114">El controlador usa esta información como sugerencia para optimizar las funcionalidades del procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="48e0d-114">The driver uses this information as a hint to optimize the capabilities of the video processor.</span></span> <span data-ttu-id="48e0d-115">La estructura no contiene una descripción de formato completa.</span><span class="sxs-lookup"><span data-stu-id="48e0d-115">The structure does not contain a complete format description.</span></span>
    ```C++
        DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

        DXVAHD_CONTENT_DESC desc;

        desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
        desc.InputFrameRate = fps;
        desc.InputWidth = VIDEO_WIDTH;
        desc.InputHeight = VIDEO_HEIGHT;
        desc.OutputFrameRate = fps;
        desc.OutputWidth = VIDEO_WIDTH;
        desc.OutputHeight = VIDEO_HEIGHT;
    ```

    

2.  <span data-ttu-id="48e0d-116">Llame [**a DXVAHD \_ CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) para crear el dispositivo DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="48e0d-116">Call [**DXVAHD\_CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) to create the DXVA-HD device.</span></span> <span data-ttu-id="48e0d-117">Esta función devuelve un puntero a la [**interfaz de dispositivo IDXVAHD. \_**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)</span><span class="sxs-lookup"><span data-stu-id="48e0d-117">This function returns a pointer to the [**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) interface.</span></span>
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  <span data-ttu-id="48e0d-118">Llame [**a IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span><span class="sxs-lookup"><span data-stu-id="48e0d-118">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span></span> <span data-ttu-id="48e0d-119">Este método rellena una estructura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) con las funcionalidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48e0d-119">This method fills in a [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure with the device capabilities.</span></span> <span data-ttu-id="48e0d-120">Si necesita características específicas de procesamiento de vídeo, como la clave de luma o el filtrado de imágenes, compruebe su disponibilidad mediante esta estructura.</span><span class="sxs-lookup"><span data-stu-id="48e0d-120">If you require specific video processing features, such as luma keying or image filtering, check their availability by using this structure.</span></span>
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  <span data-ttu-id="48e0d-121">Compruebe si el dispositivo DXVA-HD admite los formatos de vídeo de entrada que necesita.</span><span class="sxs-lookup"><span data-stu-id="48e0d-121">Check whether the DXVA-HD device supports the input video formats that you require.</span></span> <span data-ttu-id="48e0d-122">En el tema [Comprobación de formatos DXVA-HD](checking-supported-dxva-hd-formats.md) admitidos se describe este paso con más detalle.</span><span class="sxs-lookup"><span data-stu-id="48e0d-122">The topic [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
5.  <span data-ttu-id="48e0d-123">Compruebe si el dispositivo DXVA-HD admite el formato de salida que necesita.</span><span class="sxs-lookup"><span data-stu-id="48e0d-123">Check whether the DXVA-HD device supports the output format that you require.</span></span> <span data-ttu-id="48e0d-124">En la sección [Comprobación de los formatos DXVA-HD](checking-supported-dxva-hd-formats.md) admitidos se describe este paso con más detalle.</span><span class="sxs-lookup"><span data-stu-id="48e0d-124">The section [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
6.  <span data-ttu-id="48e0d-125">Asigne una matriz de [**estructuras \_ DE DXVAHD VPCAPS.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps)</span><span class="sxs-lookup"><span data-stu-id="48e0d-125">Allocate an array of [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structures.</span></span> <span data-ttu-id="48e0d-126">El miembro **VideoProcessorCount** de la estructura [**\_ DXVAHD VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) obtiene el número de elementos de matriz que se deben asignar, obtenido en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="48e0d-126">The number of array elements that must be allocated is given by the **VideoProcessorCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure, obtained in step 3.</span></span>
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  <span data-ttu-id="48e0d-127">Cada [**estructura DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) representa un procesador de vídeo distinto.</span><span class="sxs-lookup"><span data-stu-id="48e0d-127">Each [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure represents a distinct video processor.</span></span> <span data-ttu-id="48e0d-128">Puede recorrer en bucle esta matriz para detectar las funcionalidades de cada procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="48e0d-128">You can loop through this array to discover the capabilities of each video processor.</span></span> <span data-ttu-id="48e0d-129">La estructura incluye información sobre las funcionalidades de desenlazado, tele telefónica y conversión de velocidad de fotogramas del procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="48e0d-129">The structure includes information about the deinterlacing, telecine, and frame-rate conversion capabilities of the video processor.</span></span>
8.  <span data-ttu-id="48e0d-130">Seleccione un procesador de vídeo para crearlo.</span><span class="sxs-lookup"><span data-stu-id="48e0d-130">Select a video processor to create.</span></span> <span data-ttu-id="48e0d-131">El **miembro VPGuid** de la [**estructura DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) contiene un GUID que identifica de forma única el procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="48e0d-131">The **VPGuid** member of the [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure contains a GUID that uniquely identifies the video processor.</span></span> <span data-ttu-id="48e0d-132">Pase este GUID al [**método IDXVAHD \_ Device::CreateVideoProcessor.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor)</span><span class="sxs-lookup"><span data-stu-id="48e0d-132">Pass this GUID to the [**IDXVAHD\_Device::CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) method.</span></span> <span data-ttu-id="48e0d-133">El método devuelve un [**puntero iDXVAHD \_ VideoProcessor.**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)</span><span class="sxs-lookup"><span data-stu-id="48e0d-133">The method returns an [**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) pointer.</span></span>
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  <span data-ttu-id="48e0d-134">Opcionalmente, llame a [**IDXVAHD \_ Device::CreateVideoSurface para**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) crear una matriz de superficies de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="48e0d-134">Optionally, call [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) to create an array of input video surfaces.</span></span>

<span data-ttu-id="48e0d-135">En el ejemplo de código siguiente se muestra la secuencia completa de pasos:</span><span class="sxs-lookup"><span data-stu-id="48e0d-135">The following code example shows the complete sequence of steps:</span></span>


```C++
// Initializes the DXVA-HD video processor.

// NOTE: The following example makes some simplifying assumptions:
//
// 1. There is a single input stream.
// 2. The input frame rate matches the output frame rate.
// 3. No advanced DXVA-HD features are needed, such as luma keying or IVTC.
// 4. The application uses a single input video surface.

HRESULT InitializeDXVAHD()
{
    if (g_pD3DDevice == NULL)
    {
        return E_FAIL;
    }

    HRESULT hr = S_OK;

    IDXVAHD_Device          *pDXVAHD = NULL;
    IDXVAHD_VideoProcessor  *pDXVAVP = NULL;
    IDirect3DSurface9       *pSurf = NULL;

    DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

    DXVAHD_CONTENT_DESC desc;

    desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
    desc.InputFrameRate = fps;
    desc.InputWidth = VIDEO_WIDTH;
    desc.InputHeight = VIDEO_HEIGHT;
    desc.OutputFrameRate = fps;
    desc.OutputWidth = VIDEO_WIDTH;
    desc.OutputHeight = VIDEO_HEIGHT;

#ifdef USE_SOFTWARE_PLUGIN    
    HMODULE hSWPlugin = LoadLibrary(L"C:\\dxvahdsw.dll");

    PDXVAHDSW_Plugin pSWPlugin = (PDXVAHDSW_Plugin)GetProcAddress(hSWPlugin, "DXVAHDSW_Plugin");

    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc,DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        pSWPlugin, &pDXVAHD);
#else
    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        NULL, &pDXVAHD);
#endif
    if (FAILED(hr))
    {
        goto done;
    }

    DXVAHD_VPDEVCAPS caps;

    hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    if (FAILED(hr))
    {
        goto done;
    }

    // Check whether the device supports the input and output formats.

    hr = CheckInputFormatSupport(pDXVAHD, caps, VIDEO_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CheckOutputFormatSupport(pDXVAHD, caps, RENDER_TARGET_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the VP device.
    hr = CreateVPDevice(pDXVAHD, caps, &pDXVAVP);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );

    if (FAILED(hr))
    {
        goto done;
    }


    g_pDXVAHD = pDXVAHD;
    g_pDXVAHD->AddRef();

    g_pDXVAVP = pDXVAVP;
    g_pDXVAVP->AddRef();

    g_pSurface = pSurf;
    g_pSurface->AddRef();

done:
    SafeRelease(&pDXVAHD);
    SafeRelease(&pDXVAVP);
    SafeRelease(&pSurf);
    return hr;
}
```



<span data-ttu-id="48e0d-136">La función CreateVPDevice que se muestra en este ejemplo crea el procesador de vídeo (pasos 5 a 7):</span><span class="sxs-lookup"><span data-stu-id="48e0d-136">The CreateVPDevice function show in this example creates the video processor (steps 5–7):</span></span>


```C++
// Creates a DXVA-HD video processor.

HRESULT CreateVPDevice(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    IDXVAHD_VideoProcessor  **ppDXVAVP
    )
{
    // Create the array of video processor caps. 
    
    DXVAHD_VPCAPS *pVPCaps = 
        new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

    if (pVPCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
        caps.VideoProcessorCount, pVPCaps);

    // At this point, an application could loop through the array and examine
    // the capabilities. For purposes of this example, however, we simply
    // create the first video processor in the list.

    if (SUCCEEDED(hr))
    {
        // The VPGuid member contains the GUID that identifies the video 
        // processor.

        hr = pDXVAHD->CreateVideoProcessor(&pVPCaps[0].VPGuid, ppDXVAVP);
    }

    delete [] pVPCaps;
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="48e0d-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="48e0d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48e0d-138">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="48e0d-138">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



