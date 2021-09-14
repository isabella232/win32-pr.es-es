---
title: Introducción a la interoperabilidad de Direct2D y Direct3D
description: Introducción a la interoperabilidad de Direct2D y Direct3D
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- Interoperación de Direct2D,Direct3D
- Direct2D, interoperabilidad
- interoperabilidad, Direct2D
- interoperabilidad, Direct3D
- Direct3D, interoperabilidad
- Interoperación de Direct3D,Direct2D
- Direct2D,DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cf7cfa41c3decc964492258dad9c6a3a497f504b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163413"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a>Introducción a la interoperabilidad de Direct2D y Direct3D

Los gráficos 2D y 3D acelerados por hardware se están convirtiendo cada vez más en una parte de las aplicaciones que no son de juegos y la mayoría de las aplicaciones de juegos usan gráficos 2D en forma de menús y Heads-Up pantallas (HUD). Hay una gran cantidad de valor que se puede agregar al permitir que la representación 2D tradicional se mezcle con la representación de Direct3D de una manera eficaz.

En este tema se describe cómo integrar gráficos 2D y 3D mediante Direct2D [y Direct3D.](../graphics-and-multimedia.md)

Contiene las siguientes secciones:

-   [Requisitos previos](#prerequisites)
-   [Versiones admitidas de Direct3D](#supported-direct3d-versions)
-   [Interoperabilidad a través de DXGI](#interoperability-through-dxgi)
-   [Escritura en una superficie de Direct3D con un destino de representación de superficie DXGI](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [Creación de una superficie DXGI](#creating-a-dxgi-surface)
-   [Escritura de contenido de Direct2D en un búfer de cadena de intercambio](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [Ejemplo: Dibujar un fondo 2D](#example-draw-a-2-d-background)
-   [Usar contenido de Direct2D como textura](#using-direct2d-content-as-a-texture)
    -   [Ejemplo: Uso de contenido de Direct2D como textura](#example-use-direct2d-content-as-a-texture)
-   [Redimensionar un destino de representación de superficie DXGI](#resizing-a-dxgi-surface-render-target)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

En esta introducción se supone que está familiarizado con las operaciones básicas de dibujo de Direct2D. Para ver un tutorial, consulte la [guía de inicio rápido de Direct2D.](direct2d-quickstart.md) También se supone que puede programar mediante [Direct3D 10.1](/windows/desktop/direct3d10/d3d10-graphics).

## <a name="supported-direct3d-versions"></a>Versiones admitidas de Direct3D

Con DirectX 11.0, Direct2D solo admite la interoperabilidad con dispositivos Direct3D 10.1. Con DirectX 11.1 o posterior, Direct2D también admite la interoperabilidad con Direct3D 11.

## <a name="interoperability-through-dxgi"></a>Interoperabilidad a través de DXGI

A partir de Direct3D 10, el entorno de ejecución de Direct3D usa [DXGI para](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) la administración de recursos. La capa de tiempo de ejecución de DXGI proporciona un uso compartido entre procesos de superficies de memoria de vídeo y sirve como base para otras plataformas de tiempo de ejecución basadas en memoria de vídeo. Direct2D usa DXGI para interoperar con Direct3D.

Hay dos maneras principales de usar Direct2D y Direct3D juntos:

-   Puede escribir contenido de Direct2D en una superficie de Direct3D obteniendo un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) y usándose con [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para crear un [**id2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) A continuación, puede usar el destino de representación para agregar una interfaz bidimensional o un fondo a gráficos tridimensionales, o bien usar un dibujo de Direct2D como textura para un objeto tridimensional.
-   Mediante el uso de [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para crear un [**elemento ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a partir de [**un IDXGISurface,**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)puede escribir una escena de Direct3D en un mapa de bits y representarla con Direct2D.

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a>Escritura en una superficie de Direct3D con un destino de representación de superficie DXGI

Para escribir en una superficie de Direct3D, se obtiene un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) y se pasa al [**método CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para crear un destino de representación de superficie DXGI. A continuación, puede usar el destino de representación de superficie DXGI para dibujar contenido 2D en la superficie DXGI.

Un destino de representación de superficie DXGI es un tipo [**de ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Al igual que otros destinos de representación de Direct2D, puede usarlo para crear recursos y emitir comandos de dibujo.

El destino de representación de la superficie DXGI y la superficie DXGI deben usar el mismo formato DXGI. Si especifica el formato [**DXGI \_ FORMAT \_ UNICIALMENTEN**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) al crear el destino de representación, usará automáticamente el formato de la superficie.

El destino de representación de la superficie DXGI no realiza la sincronización de la superficie DXGI.

### <a name="creating-a-dxgi-surface"></a>Creación de una superficie DXGI

Con Direct3D 10, hay varias maneras de obtener una superficie DXGI. Puede crear un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) para un dispositivo y, a continuación, usar el método [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de la cadena de intercambio para obtener una superficie DXGI. O bien, puede usar un dispositivo para crear una textura y, a continuación, usar esa textura como una superficie DXGI.

Independientemente de cómo cree la superficie DXGI, la superficie debe usar uno de los formatos DXGI admitidos por los destinos de representación de la superficie DXGI. Para obtener una lista, vea [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).

Además, el [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) asociado a la superficie DXGI debe admitir formatos BGRA DXGI para que la superficie funcione con Direct2D. Para garantizar esta compatibilidad, use la marca [**D3D10 \_ CREATE \_ DEVICE \_ BGRA \_ SUPPORT**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) al llamar al método [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para crear el dispositivo.

El código siguiente define un método que crea un [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1). Selecciona el mejor nivel de característica disponible y vuelve a Windows [Advanced Rasterization Platform (WARP)](./installing-the-direct2d-debug-layer.md) cuando la representación de hardware no está disponible.


```C++
HRESULT DXGISampleApp::CreateD3DDevice(
    IDXGIAdapter *pAdapter,
    D3D10_DRIVER_TYPE driverType,
    UINT flags,
    ID3D10Device1 **ppDevice
    )
{
    HRESULT hr = S_OK;

    static const D3D10_FEATURE_LEVEL1 levelAttempts[] =
    {
        D3D10_FEATURE_LEVEL_10_0,
        D3D10_FEATURE_LEVEL_9_3,
        D3D10_FEATURE_LEVEL_9_2,
        D3D10_FEATURE_LEVEL_9_1,
    };

    for (UINT level = 0; level < ARRAYSIZE(levelAttempts); level++)
    {
        ID3D10Device1 *pDevice = NULL;
        hr = D3D10CreateDevice1(
            pAdapter,
            driverType,
            NULL,
            flags,
            levelAttempts[level],
            D3D10_1_SDK_VERSION,
            &pDevice
            );

        if (SUCCEEDED(hr))
        {
            // transfer reference
            *ppDevice = pDevice;
            pDevice = NULL;
            break;
        }

    }

    return hr;
}
```



En el ejemplo de código siguiente se usa el método que se muestra en el ejemplo anterior para crear un dispositivo Direct3D que puede crear superficies DXGI para su uso `CreateD3DDevice` con Direct2D.


```C++
// Create device
hr = CreateD3DDevice(
    NULL,
    D3D10_DRIVER_TYPE_HARDWARE,
    nDeviceFlags,
    &pDevice
    );

if (FAILED(hr))
{
    hr = CreateD3DDevice(
        NULL,
        D3D10_DRIVER_TYPE_WARP,
        nDeviceFlags,
        &pDevice
        );
}
```



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a>Escritura de contenido de Direct2D en un búfer de cadena de intercambio

La manera más sencilla de agregar contenido de Direct2D a una escena de Direct3D es usar el método [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) para obtener una superficie DXGI y, a continuación, usar la superficie con el método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para crear un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) con el que dibujar el contenido 2D.

Este enfoque no representa el contenido en tres dimensiones; no tendrá perspectiva ni profundidad. Sin embargo, es útil para varias tareas comunes:

-   Crear un fondo 2D para una escena 3D.
-   Crear una interfaz 2D delante de una escena 3D.
-   Uso de multimuestreo de Direct3D al representar contenido de Direct2D.

En la sección siguiente se muestra cómo crear un fondo 2D para una escena 3D.

### <a name="example-draw-a-2-d-background"></a>Ejemplo: Dibujar un fondo 2D

En los pasos siguientes se describe cómo crear un destino de representación de superficie DXGI y usarlo para dibujar un fondo de degradado.

1.  Use el [**método CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) para crear una cadena de intercambio para [**un ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (la variable *m \_ pDevice).* La cadena de intercambio usa el formato [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, uno de los formatos DXGI compatibles con Direct2D.

```C++
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&m_pDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&pDXGIDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDXGIDevice->GetAdapter(&pAdapter);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAdapter->GetParent(IID_PPV_ARGS(&pDXGIFactory));
    }
    if (SUCCEEDED(hr))
    {
        DXGI_SWAP_CHAIN_DESC swapDesc;
        ::ZeroMemory(&swapDesc, sizeof(swapDesc));

        swapDesc.BufferDesc.Width = nWidth;
        swapDesc.BufferDesc.Height = nHeight;
        swapDesc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
        swapDesc.BufferDesc.RefreshRate.Numerator = 60;
        swapDesc.BufferDesc.RefreshRate.Denominator = 1;
        swapDesc.SampleDesc.Count = 1;
        swapDesc.SampleDesc.Quality = 0;
        swapDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapDesc.BufferCount = 1;
        swapDesc.OutputWindow = m_hwnd;
        swapDesc.Windowed = TRUE;

        hr = pDXGIFactory->CreateSwapChain(m_pDevice, &swapDesc, &m_pSwapChain);
    }
```

    

2.  Use el método [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de la cadena de intercambio para obtener una superficie DXGI.

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  Use la superficie DXGI para crear un destino de representación DXGI.
```C++
    // Create the DXGI Surface Render Target.
    FLOAT dpiX;
    FLOAT dpiY;
    m_pD2DFactory->GetDesktopDpi(&dpiX, &dpiY);

    D2D1_RENDER_TARGET_PROPERTIES props =
        D2D1::RenderTargetProperties(
            D2D1_RENDER_TARGET_TYPE_DEFAULT,
            D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
            dpiX,
            dpiY
            );

    // Create a Direct2D render target which can draw into the surface in the swap chain

    
hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pBackBuffer,
        &props,
        &m_pBackBufferRT
        );
    
```



    

4.  Use el destino de representación para dibujar un fondo de degradado.

```C++
    // Swap chain will tell us how big the back buffer is
    DXGI_SWAP_CHAIN_DESC swapDesc;
    hr = m_pSwapChain->GetDesc(&swapDesc);

    if (SUCCEEDED(hr))
    {

    
// Draw a gradient background.
    if (m_pBackBufferRT)
    {
        D2D1_SIZE_F targetSize = m_pBackBufferRT->GetSize();

        m_pBackBufferRT->BeginDraw();

        m_pBackBufferGradientBrush->SetTransform(
            D2D1::Matrix3x2F::Scale(targetSize)
            );

        D2D1_RECT_F rect = D2D1::RectF(
            0.0f,
            0.0f,
            targetSize.width,
            targetSize.height
            );

        m_pBackBufferRT->FillRectangle(&rect, m_pBackBufferGradientBrush);

        hr = m_pBackBufferRT->EndDraw();
    }
```



    

El código se omite en este ejemplo.

## <a name="using-direct2d-content-as-a-texture"></a>Usar contenido de Direct2D como textura

Otra manera de usar contenido de Direct2D con Direct3D es usar Direct2D para generar una textura 2D y, a continuación, aplicar esa textura a un modelo 3D. Para ello, cree un [**ID3D10Texture2D,**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)obtenga una superficie DXGI a partir de la textura y, a continuación, use la superficie para crear un destino de representación de superficie DXGI. La **superficie ID3D10Texture2D** debe usar la marca de enlace [**D3D10 \_ BIND RENDER \_ \_ TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) y usar un formato DXGI compatible con los destinos de representación de la superficie DXGI. Para obtener una lista de los formatos DXGI admitidos, vea [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).

### <a name="example-use-direct2d-content-as-a-texture"></a>Ejemplo: Uso de contenido de Direct2D como textura

En los ejemplos siguientes se muestra cómo crear un destino de representación de superficie DXGI que se representa en una textura 2D (representada por un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).

1.  En primer lugar, use un dispositivo Direct3D para crear una textura 2D. La textura usa las marcas de enlace [**D3D10 \_ BIND \_ RENDER \_ TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) y **D3D10 \_ BIND SHADER \_ \_ RESOURCE,** y usa el formato [**DXGI FORMAT \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, uno de los formatos DXGI admitidos por Direct2D.

```C++
    // Allocate a offscreen D3D surface for D2D to render our 2D content into
    D3D10_TEXTURE2D_DESC texDesc;
    texDesc.ArraySize = 1;
    texDesc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
    texDesc.CPUAccessFlags = 0;
    texDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
    texDesc.Height = 512;
    texDesc.Width = 512;
    texDesc.MipLevels = 1;
    texDesc.MiscFlags = 0;
    texDesc.SampleDesc.Count = 1;
    texDesc.SampleDesc.Quality = 0;
    texDesc.Usage = D3D10_USAGE_DEFAULT;

    hr = m_pDevice->CreateTexture2D(&texDesc, NULL, &m_pOffscreenTexture);
```

    

2.  Use la textura para obtener una superficie DXGI.

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  Use la superficie con el [**método CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para obtener un destino de representación de Direct2D.

```C++
    if (SUCCEEDED(hr))
    {
        // Create a D2D render target which can draw into our offscreen D3D
        // surface. Given that we use a constant size for the texture, we
        // fix the DPI at 96.
        D2D1_RENDER_TARGET_PROPERTIES props =
            D2D1::RenderTargetProperties(
                D2D1_RENDER_TARGET_TYPE_DEFAULT,
                D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
                96,
                96
                );

    
    hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
            pDxgiSurface,
            &props,
            &m_pRenderTarget
            );
    }
```



    

Ahora que ha obtenido un destino de representación de Direct2D y lo ha asociado a una textura de Direct3D, puede usar el destino de representación para dibujar contenido de Direct2D en esa textura y aplicar esa textura a las primitivas de Direct3D.

El código se omite en este ejemplo.

## <a name="resizing-a-dxgi-surface-render-target"></a>Redimensionar un destino de representación de superficie DXGI

Los destinos de representación de superficie DXGI no admiten [**el método ID2D1RenderTarget::Resize.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) Para cambiar el tamaño de un destino de representación de superficie DXGI, la aplicación debe liberarlo y volver a crearlo.

Esta operación puede crear posibles problemas de rendimiento. El destino de representación podría ser el último recurso activo de Direct2D que mantiene una referencia al [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) asociado a la superficie DXGI del destino de representación. Si la aplicación libera el destino de representación y se destruye la referencia **ID3D10Device1,** se debe volver a crear uno nuevo.

Puede evitar esta operación potencialmente costosa manteniendo al menos un recurso de Direct2D creado por el destino de representación mientras vuelve a crear ese destino de representación. Estos son algunos recursos de Direct2D que funcionan para este enfoque:

-   [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (que puede ser mantenido indirectamente por un [**objeto ID2D1BitmapBrush)**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

Para adaptarse a este enfoque, el método de cambio de tamaño debe probar para ver si el dispositivo Direct3D está disponible. Si está disponible, libere y vuelva a crear los destinos de representación de la superficie DXGI, pero mantenga todos los recursos que creó anteriormente y vuelva a usarlos. Esto funciona porque, como se describe en Información general de [recursos,](resources-and-resource-domains.md)los recursos creados por dos destinos de representación son compatibles cuando ambos destinos de representación están asociados al mismo dispositivo Direct3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos de píxel admitidos y modos alfa](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))
</dt> <dt>

[Windows Gráficos de DirectX](../graphics-and-multimedia.md)
</dt> </dl>

 

 
