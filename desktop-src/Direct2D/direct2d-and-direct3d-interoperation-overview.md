---
title: Introducción a la interoperabilidad de Direct2D y Direct3D
description: .
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- Direct2D, interoperación de Direct3D
- Direct2D, interoperabilidad
- interoperabilidad, Direct2D
- interoperabilidad, Direct3D
- Direct3D, interoperabilidad
- Direct3D, interoperación de Direct2D
- Direct2D, DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6854481ec2a8d869467aa912252e3649e17f2501
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2020
ms.locfileid: "104149709"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a>Introducción a la interoperabilidad de Direct2D y Direct3D

Los gráficos con aceleración de hardware en 2D y 3D se convierten cada vez en una parte de las aplicaciones que no son de juegos y la mayoría de las aplicaciones de juegos usan gráficos 2D en forma de menús y pantallas de Heads-Up (HUDs). Hay un gran número de valores que se pueden agregar al permitir que la representación 2D tradicional se mezcle con la representación de Direct3D de una manera eficaz.

En este tema se describe cómo integrar gráficos 2D y 3D mediante Direct2D y [Direct3D](../graphics-and-multimedia.md).

Contiene las siguientes secciones:

-   [Requisitos previos](#prerequisites)
-   [Versiones admitidas de Direct3D](#supported-direct3d-versions)
-   [Interoperabilidad a través de DXGI](#interoperability-through-dxgi)
-   [Escribir en una superficie de Direct3D con un destino de representación de la superficie de DXGI](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [Crear una superficie de DXGI](#creating-a-dxgi-surface)
-   [Escritura de contenido de Direct2D en un búfer de cadena de intercambio](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [Ejemplo: dibujar un fondo en 2D](#example-draw-a-2-d-background)
-   [Usar contenido de Direct2D como textura](#using-direct2d-content-as-a-texture)
    -   [Ejemplo: uso de contenido de Direct2D como textura](#example-use-direct2d-content-as-a-texture)
-   [Cambiar el tamaño de un destino de representación de la superficie de DXGI](#resizing-a-dxgi-surface-render-target)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

En esta información general se supone que está familiarizado con las operaciones básicas de dibujo de Direct2D. Para ver un tutorial, consulte la guía de [Inicio rápido de Direct2D](direct2d-quickstart.md). También se supone que puede programar con [Direct3D 10,1](/windows/desktop/direct3d10/d3d10-graphics).

## <a name="supported-direct3d-versions"></a>Versiones admitidas de Direct3D

Con DirectX 11,0, Direct2D solo admite la interoperabilidad con dispositivos Direct3D 10,1. Con DirectX 11,1 o posterior, Direct2D también admite la interoperabilidad con Direct3D 11.

## <a name="interoperability-through-dxgi"></a>Interoperabilidad a través de DXGI

A partir de Direct3D 10, el tiempo de ejecución de Direct3D usa [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) para la administración de recursos. La capa de tiempo de ejecución de DXGI proporciona el uso compartido entre procesos de superficies de memoria de vídeo y sirve como base para otras plataformas en tiempo de ejecución basadas en memoria de vídeo. Direct2D usa DXGI para interoperar con Direct3D.

Hay dos formas principales de usar Direct2D y Direct3D conjuntamente:

-   Puede escribir contenido de Direct2D en una superficie de Direct3D mediante la obtención de un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) y su uso con [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para crear un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). Después, puede usar el destino de representación para agregar una interfaz bidimensional o un fondo a gráficos tridimensionales, o bien usar un dibujo de Direct2D como textura para un objeto de tres dimensiones.
-   Mediante el uso de [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para crear un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) desde un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), puede escribir una escena de Direct3D en un mapa de bits y representarlo con Direct2D.

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a>Escribir en una superficie de Direct3D con un destino de representación de la superficie de DXGI

Para escribir en una superficie de Direct3D, obtenga un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) y páselo al método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para crear un destino de representación de la superficie de DXGI. Después, puede usar el destino de representación de la superficie de DXGI para dibujar contenido 2D en la superficie de DXGI.

Un destino de representación de la superficie de DXGI es un tipo de [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). Al igual que otros destinos de representación de Direct2D, puede usarlo para crear recursos y emitir comandos de dibujo.

El destino de representación de la superficie de DXGI y la superficie de DXGI deben usar el mismo formato de DXGI. Si especifica el formato de [**DXGI formato \_ \_ desconocido**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) al crear el destino de representación, usará automáticamente el formato de la superficie.

El destino de representación de la superficie de DXGI no realiza la sincronización de la superficie de DXGI.

### <a name="creating-a-dxgi-surface"></a>Crear una superficie de DXGI

Con Direct3D 10, hay varias maneras de obtener una superficie de DXGI. Puede crear un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) para un dispositivo y, a continuación, usar el método [**getBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de la cadena de intercambio para obtener una superficie de DXGI. O bien, puede usar un dispositivo para crear una textura y, a continuación, usar esa textura como una superficie de DXGI.

Independientemente de cómo cree la superficie de DXGI, la superficie debe usar uno de los formatos de DXGI que admiten los objetivos de representación de la superficie de DXGI. Para obtener una lista, vea [formatos de píxel admitidos y modos alfa](supported-pixel-formats-and-alpha-modes.md).

Además, el [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) asociado a la superficie de dxgi debe admitir formatos de BGRA DXGI para que la superficie funcione con Direct2D. Para garantizar esta compatibilidad, use la marca de [**\_ soporte D3D10 Create \_ Device \_ BGRA \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) al llamar al método [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para crear el dispositivo.

En el código siguiente se define un método que crea un [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1). Selecciona el mejor nivel de características disponible y recurre a [Windows Advanced rasterization Platform (warp)](./installing-the-direct2d-debug-layer.md) cuando no está disponible la representación de hardware.


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



En el ejemplo de código siguiente `CreateD3DDevice` se usa el método que se muestra en el ejemplo anterior para crear un dispositivo Direct3D que pueda crear superficies de DXGI para su uso con Direct2D.


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

La manera más sencilla de agregar contenido de Direct2D a una escena de Direct3D es usar el método [**getBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) para obtener una superficie de DXGI y luego usar la superficie con el método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para crear un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) con el que dibujar el contenido 2D.

Este enfoque no representa el contenido en tres dimensiones. no tendrá perspectiva ni profundidad. Sin embargo, resulta útil para varias tareas comunes:

-   Crear un fondo 2D para una escena 3D.
-   Creación de una interfaz 2D delante de una escena 3D.
-   Usar el muestreo múltiple de Direct3D al representar contenido de Direct2D.

En la sección siguiente se muestra cómo crear un fondo 2D para una escena 3D.

### <a name="example-draw-a-2-d-background"></a>Ejemplo: dibujar un fondo en 2D

En los pasos siguientes se describe cómo crear un destino de representación de la superficie de DXGI y cómo usarlo para dibujar un fondo degradado.

1.  Use el método [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) para crear una cadena de intercambio para una [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (la variable *\_ pDevice de m* ). La cadena de intercambio usa el formato [**dxgi \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) dxgi Format, uno de los formatos de dxgi admitidos por Direct2D.

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

    

2.  Use el método [**getBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de la cadena de intercambio para obtener una superficie de DXGI.

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  Use la superficie de DXGI para crear un destino de representación de DXGI.
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



    

4.  Use el destino de representación para dibujar un fondo degradado.

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

Otra forma de usar el contenido de Direct2D con Direct3D es usar Direct2D para generar una textura 2D y después aplicar esa textura a un modelo 3D. Para ello, cree un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtenga una superficie de dxgi a partir de la textura y, a continuación, use la superficie para crear un destino de representación de la superficie de dxgi. La superficie **ID3D10Texture2D** debe usar la marca de enlace de destino de [**representación de \_ enlace \_ \_ D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) y usar un formato de dxgi compatible con los destinos de representación de la superficie de DXGI. Para obtener una lista de formatos de DXGI compatibles, vea [formatos de píxeles compatibles y modos alfa](supported-pixel-formats-and-alpha-modes.md).

### <a name="example-use-direct2d-content-as-a-texture"></a>Ejemplo: uso de contenido de Direct2D como textura

En los siguientes ejemplos se muestra cómo crear un destino de representación de la superficie de DXGI que se representa en una textura 2D (representada por un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).

1.  En primer lugar, use un dispositivo Direct3D para crear una textura 2D. La textura usa las marcas de enlace del recurso de destino de representación de enlace de D3D10 y del **\_ \_ sombreador \_ de enlace de D3D10** y usa el formato de [**dxgi \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) dxgi, uno de los formatos de dxgi admitidos por Direct2D. [**\_ \_ \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag)

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

    

2.  Use la textura para obtener una superficie de DXGI.

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  Use la superficie con el método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para obtener un destino de representación de Direct2D.

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



    

Ahora que ha obtenido un destino de representación de Direct2D y lo ha asociado con una textura de Direct3D, puede usar el destino de representación para dibujar el contenido de Direct2D en esa textura, y puede aplicar esa textura a los primitivos de Direct3D.

El código se omite en este ejemplo.

## <a name="resizing-a-dxgi-surface-render-target"></a>Cambiar el tamaño de un destino de representación de la superficie de DXGI

Los destinos de representación de la superficie de DXGI no admiten el método [**ID2D1RenderTarget:: Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) . Para cambiar el tamaño de un destino de representación de la superficie de DXGI, la aplicación debe liberarla y volver a crearla.

Esta operación puede crear problemas de rendimiento. El destino de representación podría ser el último recurso de Direct2D activo que mantiene una referencia al [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) asociado a la superficie de DXGI del destino de representación. Si la aplicación libera el destino de representación y se destruye la referencia **ID3D10Device1** , se debe volver a crear una nueva.

Puede evitar esta operación potencialmente costosa manteniendo al menos un recurso de Direct2D creado por el destino de presentación mientras vuelve a crear ese destino de representación. A continuación se muestran algunos recursos de Direct2D que funcionan para este enfoque:

-   [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (que un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)puede mantener indirectamente)
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

Para dar cabida a este enfoque, el método de cambiar tamaño debe probar para ver si el dispositivo Direct3D está disponible. Si está disponible, libere y vuelva a crear los destinos de representación de la superficie de DXGI, pero Mantenga todos los recursos que crearon previamente y vuelva a usarlos. Esto funciona porque, como se describe en la [información general](resources-and-resource-domains.md)de los recursos, los recursos creados por dos destinos de representación son compatibles cuando ambos destinos de representación están asociados al mismo dispositivo de Direct3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos de píxel admitidos y modos alfa](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))
</dt> <dt>

[Gráficos de Windows DirectX](../graphics-and-multimedia.md)
</dt> </dl>

 

 