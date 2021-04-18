---
description: .
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: Creación de un procesador de vídeo DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee524681cad43a8e140421e8e6eff30d44cabcc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714933"
---
# <a name="creating-a-dxva-hd-video-processor"></a><span data-ttu-id="4fb53-103">Creación de un procesador de vídeo DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="4fb53-103">Creating a DXVA-HD Video Processor</span></span>

<span data-ttu-id="4fb53-104">La alta definición de Microsoft DirectX video Acceleration (DXVA-HD) usa dos interfaces principales:</span><span class="sxs-lookup"><span data-stu-id="4fb53-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) uses two primary interfaces:</span></span>

-   <span data-ttu-id="4fb53-105">[**IDXVAHD \_ Dispositivo**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span><span class="sxs-lookup"><span data-stu-id="4fb53-105">[**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span></span> <span data-ttu-id="4fb53-106">Representa el dispositivo DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="4fb53-106">Represents the DXVA-HD device.</span></span> <span data-ttu-id="4fb53-107">Use esta interfaz para consultar las capacidades del dispositivo y crear el procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4fb53-107">Use this interface to query the device capabilities and create the video processor.</span></span>
-   <span data-ttu-id="4fb53-108">[**IDXVAHD \_ Videoprocesador**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span><span class="sxs-lookup"><span data-stu-id="4fb53-108">[**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span></span> <span data-ttu-id="4fb53-109">Representa un conjunto de capacidades de procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4fb53-109">Represents a set of video processing capabilities.</span></span> <span data-ttu-id="4fb53-110">Use esta interfaz para realizar el procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4fb53-110">Use this interface to perform the video processing blit.</span></span>

<span data-ttu-id="4fb53-111">En el código siguiente, se asumen las variables globales siguientes:</span><span class="sxs-lookup"><span data-stu-id="4fb53-111">In the code that follows, the following global variables are assumed:</span></span>


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



<span data-ttu-id="4fb53-112">Para crear un procesador de vídeo DXVA-HD:</span><span class="sxs-lookup"><span data-stu-id="4fb53-112">To create a DXVA-HD video processor:</span></span>

1.  <span data-ttu-id="4fb53-113">Rellene una [**estructura \_ \_ DESC de contenido DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) con una descripción del contenido del vídeo.</span><span class="sxs-lookup"><span data-stu-id="4fb53-113">Fill in a [**DXVAHD\_CONTENT\_DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) structure with a description of the video content.</span></span> <span data-ttu-id="4fb53-114">El controlador utiliza esta información como una sugerencia para optimizar las capacidades del procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4fb53-114">The driver uses this information as a hint to optimize the capabilities of the video processor.</span></span> <span data-ttu-id="4fb53-115">La estructura no contiene una descripción del formato completo.</span><span class="sxs-lookup"><span data-stu-id="4fb53-115">The structure does not contain a complete format description.</span></span>
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

    

2.  <span data-ttu-id="4fb53-116">Llame a [**DXVAHD \_ CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) para crear el dispositivo DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="4fb53-116">Call [**DXVAHD\_CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) to create the DXVA-HD device.</span></span> <span data-ttu-id="4fb53-117">Esta función devuelve un puntero a la interfaz de [**\_ dispositivo IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) .</span><span class="sxs-lookup"><span data-stu-id="4fb53-117">This function returns a pointer to the [**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) interface.</span></span>
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  <span data-ttu-id="4fb53-118">Llame [**al \_ dispositivo IDXVAHD:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span><span class="sxs-lookup"><span data-stu-id="4fb53-118">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span></span> <span data-ttu-id="4fb53-119">Este método rellena una estructura de [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) con las funcionalidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4fb53-119">This method fills in a [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure with the device capabilities.</span></span> <span data-ttu-id="4fb53-120">Si necesita características específicas de procesamiento de vídeo, como la generación de claves de luminancia o el filtrado de imágenes, compruebe su disponibilidad con esta estructura.</span><span class="sxs-lookup"><span data-stu-id="4fb53-120">If you require specific video processing features, such as luma keying or image filtering, check their availability by using this structure.</span></span>
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  <span data-ttu-id="4fb53-121">Compruebe si el dispositivo DXVA-HD admite los formatos de vídeo de entrada que necesite.</span><span class="sxs-lookup"><span data-stu-id="4fb53-121">Check whether the DXVA-HD device supports the input video formats that you require.</span></span> <span data-ttu-id="4fb53-122">En el tema [comprobación de formatos de DXVA-HD compatibles](checking-supported-dxva-hd-formats.md) se describe este paso con más detalle.</span><span class="sxs-lookup"><span data-stu-id="4fb53-122">The topic [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
5.  <span data-ttu-id="4fb53-123">Compruebe si el dispositivo DXVA-HD admite el formato de salida que necesite.</span><span class="sxs-lookup"><span data-stu-id="4fb53-123">Check whether the DXVA-HD device supports the output format that you require.</span></span> <span data-ttu-id="4fb53-124">En la sección [comprobación de formatos de DXVA-HD admitidos](checking-supported-dxva-hd-formats.md) se describe con más detalle este paso.</span><span class="sxs-lookup"><span data-stu-id="4fb53-124">The section [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
6.  <span data-ttu-id="4fb53-125">Asigne una matriz de estructuras [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) .</span><span class="sxs-lookup"><span data-stu-id="4fb53-125">Allocate an array of [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structures.</span></span> <span data-ttu-id="4fb53-126">El miembro **VideoProcessorCount** de la estructura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) obtenido en el paso 3 proporciona el número de elementos de matriz que se deben asignar.</span><span class="sxs-lookup"><span data-stu-id="4fb53-126">The number of array elements that must be allocated is given by the **VideoProcessorCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure, obtained in step 3.</span></span>
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  <span data-ttu-id="4fb53-127">Cada estructura [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) representa un procesador de vídeo distinto.</span><span class="sxs-lookup"><span data-stu-id="4fb53-127">Each [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure represents a distinct video processor.</span></span> <span data-ttu-id="4fb53-128">Puede recorrer esta matriz para detectar las capacidades de cada procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4fb53-128">You can loop through this array to discover the capabilities of each video processor.</span></span> <span data-ttu-id="4fb53-129">La estructura incluye información sobre las capacidades de desentrelazado, telecine y conversión de velocidad de fotograma del procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4fb53-129">The structure includes information about the deinterlacing, telecine, and frame-rate conversion capabilities of the video processor.</span></span>
8.  <span data-ttu-id="4fb53-130">Seleccione un procesador de vídeo para crearlo.</span><span class="sxs-lookup"><span data-stu-id="4fb53-130">Select a video processor to create.</span></span> <span data-ttu-id="4fb53-131">El miembro **VPGuid** de la [**estructura \_ VPCAPS de DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) contiene un GUID que identifica de forma única el procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4fb53-131">The **VPGuid** member of the [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure contains a GUID that uniquely identifies the video processor.</span></span> <span data-ttu-id="4fb53-132">Pase este GUID al método [**\_ Device:: CreateVideoProcessor de IDXVAHD**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) .</span><span class="sxs-lookup"><span data-stu-id="4fb53-132">Pass this GUID to the [**IDXVAHD\_Device::CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) method.</span></span> <span data-ttu-id="4fb53-133">El método devuelve un puntero de [**\_ videoprocesador IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) .</span><span class="sxs-lookup"><span data-stu-id="4fb53-133">The method returns an [**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) pointer.</span></span>
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  <span data-ttu-id="4fb53-134">Opcionalmente, llame a [**IDXVAHD \_ Device:: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) para crear una matriz de superficies de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="4fb53-134">Optionally, call [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) to create an array of input video surfaces.</span></span>

<span data-ttu-id="4fb53-135">En el ejemplo de código siguiente se muestra la secuencia completa de pasos:</span><span class="sxs-lookup"><span data-stu-id="4fb53-135">The following code example shows the complete sequence of steps:</span></span>


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



<span data-ttu-id="4fb53-136">La función CreateVPDevice que se muestra en este ejemplo crea el procesador de vídeo (pasos 5 – 7):</span><span class="sxs-lookup"><span data-stu-id="4fb53-136">The CreateVPDevice function show in this example creates the video processor (steps 5–7):</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4fb53-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4fb53-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fb53-138">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="4fb53-138">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



