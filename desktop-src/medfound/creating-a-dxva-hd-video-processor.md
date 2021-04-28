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
# <a name="creating-a-dxva-hd-video-processor"></a>Creación de un procesador de vídeo DXVA-HD

La alta definición de aceleración de vídeo de Microsoft DirectX (DXVA-HD) usa dos interfaces principales:

-   [**IDXVAHD \_ Dispositivo**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device). Representa el dispositivo DXVA-HD. Use esta interfaz para consultar las funcionalidades del dispositivo y crear el procesador de vídeo.
-   [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor). Representa un conjunto de funcionalidades de procesamiento de vídeo. Use esta interfaz para realizar el procesamiento de vídeo blit.

En el código siguiente, se suponen las siguientes variables globales:


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



Para crear un procesador de vídeo DXVA-HD:

1.  Rellene una [**estructura DXVAHD \_ CONTENT \_ DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) con una descripción del contenido del vídeo. El controlador usa esta información como sugerencia para optimizar las funcionalidades del procesador de vídeo. La estructura no contiene una descripción de formato completa.
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

    

2.  Llame [**a DXVAHD \_ CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) para crear el dispositivo DXVA-HD. Esta función devuelve un puntero a la [**interfaz de dispositivo IDXVAHD. \_**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  Llame [**a IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps). Este método rellena una estructura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) con las funcionalidades del dispositivo. Si necesita características específicas de procesamiento de vídeo, como la clave de luma o el filtrado de imágenes, compruebe su disponibilidad mediante esta estructura.
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  Compruebe si el dispositivo DXVA-HD admite los formatos de vídeo de entrada que necesita. En el tema [Comprobación de formatos DXVA-HD](checking-supported-dxva-hd-formats.md) admitidos se describe este paso con más detalle.
5.  Compruebe si el dispositivo DXVA-HD admite el formato de salida que necesita. En la sección [Comprobación de los formatos DXVA-HD](checking-supported-dxva-hd-formats.md) admitidos se describe este paso con más detalle.
6.  Asigne una matriz de [**estructuras \_ DE DXVAHD VPCAPS.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) El miembro **VideoProcessorCount** de la estructura [**\_ DXVAHD VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) obtiene el número de elementos de matriz que se deben asignar, obtenido en el paso 3.
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  Cada [**estructura DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) representa un procesador de vídeo distinto. Puede recorrer en bucle esta matriz para detectar las funcionalidades de cada procesador de vídeo. La estructura incluye información sobre las funcionalidades de desenlazado, tele telefónica y conversión de velocidad de fotogramas del procesador de vídeo.
8.  Seleccione un procesador de vídeo para crearlo. El **miembro VPGuid** de la [**estructura DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) contiene un GUID que identifica de forma única el procesador de vídeo. Pase este GUID al [**método IDXVAHD \_ Device::CreateVideoProcessor.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) El método devuelve un [**puntero iDXVAHD \_ VideoProcessor.**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  Opcionalmente, llame a [**IDXVAHD \_ Device::CreateVideoSurface para**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) crear una matriz de superficies de vídeo de entrada.

En el ejemplo de código siguiente se muestra la secuencia completa de pasos:


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



La función CreateVPDevice que se muestra en este ejemplo crea el procesador de vídeo (pasos 5 a 7):


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



