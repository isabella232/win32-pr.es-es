---
title: Representación mediante un contexto de dispositivo Direct2D
description: En este tema aprenderá a crear Direct2D \ 32;contexto de dispositivo en Windows 8.
ms.assetid: D4563FEA-767E-4B16-8F3C-3D548A64B206
keywords:
- Dispositivo Direct2D
- Contexto del dispositivo Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2858861956a40bf969309be474105052e4692cde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163410"
---
# <a name="how-to-render-by-using-a-direct2d-device-context"></a>Representación mediante un contexto de dispositivo Direct2D

En este tema aprenderá a crear el contexto [de dispositivo Direct2D](./direct2d-portal.md) [**en**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Windows 8. Esta información se aplica a usted si va a desarrollar aplicaciones Windows Store o una aplicación de escritorio mediante Direct2D. En este tema se describe el propósito de los objetos de contexto del dispositivo Direct2D, cómo crear ese objeto y una guía paso a paso sobre la representación y visualización de imágenes y primitivas de Direct2D. También aprenderá a cambiar los destinos de representación y agregar efectos a la aplicación.

-   [¿Qué es un dispositivo Direct2D?](#what-is-a-direct2d-device)
-   [¿Qué es un contexto de dispositivo Direct2D?](#what-is-a-direct2d-device-context)
-   [Representación con Direct2D en Windows 8](#rendering-with-direct2d-on-windows-8)
-   [¿Por qué usar un contexto de dispositivo para representarlo?](#why-use-a-device-context-to-render)
-   [Creación de un contexto de dispositivo Direct2D para la representación](#how-to-create-a-direct2d-device-context-for-rendering)
-   [Selección de un destino](#selecting-a-target)
-   [Representación y visualización](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a>¿Qué es un dispositivo Direct2D?

Necesita un dispositivo Direct2D y un dispositivo Direct3D para crear un contexto de dispositivo Direct2D. Un [**dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (expone un **puntero de interfaz ID2D1Device)** representa un adaptador de pantalla. Un dispositivo Direct3D (expone un puntero de interfaz [**ID3D11Device)**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) está asociado a un dispositivo Direct2D. Cada aplicación debe tener un **dispositivo Direct2D,** pero puede tener más de un **dispositivo**.

## <a name="what-is-a-direct2d-device-context"></a>¿Qué es un contexto de dispositivo Direct2D?

Un [contexto de dispositivo Direct2D](./direct2d-portal.md) [**(expone**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) un puntero de interfaz **ID2D1DeviceContext)** representa un conjunto de búferes de estado y comandos que se usan para representar en un destino. Puede llamar a métodos en el contexto del dispositivo para establecer el estado de canalización y generar comandos de representación mediante los recursos que pertenecen a un dispositivo.

## <a name="rendering-with-direct2d-on-windows-8"></a>Representación con Direct2D en Windows 8

En Windows 7 y versiones anteriores, se usa [**un ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) u otra interfaz de destino de representación para representar en una ventana o superficie. A partir de Windows 8, no se recomienda la representación mediante métodos que se basan en interfaces como **ID2D1HwndRenderTarget,** ya que no funcionarán con Windows Store. Puede usar un contexto [**de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para representar en un Hwnd si desea crear una aplicación de escritorio y seguir aprovechando las características adicionales del contexto **del** dispositivo. Sin embargo, **el contexto del dispositivo** es necesario para representar el contenido en Windows store con [Direct2D.](./direct2d-portal.md)

## <a name="why-use-a-device-context-to-render"></a>¿Por qué usar un contexto de dispositivo para representarlo?

-   Puede representar para aplicaciones Windows Store.
-   Puede cambiar el destino de representación en cualquier momento antes, durante y después de la representación. El contexto del dispositivo garantiza que las llamadas a los métodos de dibujo se ejecutan en orden y los aplica al cambiar el destino de representación.
-   Puede usar más de un tipo de ventana con un contexto de dispositivo. Puede usar [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) un contexto de dispositivo y una cadena de intercambio [**DXGI**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) para representar directamente en un [**objeto Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) o [**Windows::UI::XAML::SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).
-   Puede usar el contexto [del dispositivo Direct2D](./direct2d-portal.md) [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para crear efectos de [Direct2D](effects-overview.md) y representar la salida de un efecto de imagen o un gráfico de efectos en un destino de representación.
-   Puede tener varios [**contextos de dispositivo,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)lo que puede ser útil para mejorar el rendimiento en una aplicación en subproceso. Consulte [Aplicaciones Direct2D multiproceso](multi-threaded-direct2d-apps.md) para obtener más información.
-   El [**contexto del dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interopera estrechamente con Direct3D, lo que proporciona más acceso a las opciones de Direct3D.

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a>Creación de un contexto de dispositivo Direct2D para la representación

El código aquí muestra cómo crear un dispositivo Direct3D11, obtener el dispositivo DXGI asociado, crear un [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) dispositivo [**Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)y, por último, crear el contexto del dispositivo Direct2D para la representación.

Este es un diagrama de las llamadas a métodos y las interfaces que usa este código.

![diagrama de dispositivos direct2d y direct3d y contextos de dispositivo.](images/devicecontextdiagram.png)

> [!Note]  
> En este código se supone que ya tiene un objeto [**ID2D1Factory1.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) Para obtener más información, consulte la página de [**referencia de ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).

 


```C++
    // This flag adds support for surfaces with a different color channel ordering than the API default.
    // You need it for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    
    // This array defines the set of DirectX hardware feature levels this app  supports.
    // The ordering is important and you should  preserve it.
    // Don't forget to declare your app's minimum required feature level in its
    // description.  All apps are assumed to support 9.1 unless otherwise stated.
    D3D_FEATURE_LEVEL featureLevels[] = 
    {
        D3D_FEATURE_LEVEL_11_1,
        D3D_FEATURE_LEVEL_11_0,
        D3D_FEATURE_LEVEL_10_1,
        D3D_FEATURE_LEVEL_10_0,
        D3D_FEATURE_LEVEL_9_3,
        D3D_FEATURE_LEVEL_9_2,
        D3D_FEATURE_LEVEL_9_1
    };

    // Create the DX11 API device object, and get a corresponding context.
    ComPtr<ID3D11Device> device;
    ComPtr<ID3D11DeviceContext> context;

    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of possible feature levels
            D3D11_SDK_VERSION,          
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );

    ComPtr<IDXGIDevice> dxgiDevice;
    // Obtain the underlying DXGI device of the Direct3D11 device.
    DX::ThrowIfFailed(
        device.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // Get Direct2D device's corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



Veamos los pasos del ejemplo de código anterior.

1.  Obtenga un puntero de interfaz ID3D11Device que necesitará para crear el contexto del dispositivo.

    -   Declare las marcas de creación para configurar el [dispositivo Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para la compatibilidad con BGRA. [Direct2D requiere](./direct2d-portal.md) el orden de color BGRA.
    -   Declare una matriz de [**entradas D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) que representen el conjunto de niveles de características que admitirá la aplicación.
        > [!Note]  
        > [Direct3D busca](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) en la lista hasta que encuentra el nivel de característica admitido por el sistema host.

         

    -   Use la función [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) para crear un objeto [**ID3D11Device,**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) la función también devolverá un objeto [**ID3D11DeviceContext,**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) pero ese objeto no es necesario para este ejemplo.

2.  Consulte el [**dispositivo Direct3D 11 para**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) obtener su [**interfaz de dispositivo DXGI.**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)
3.  Cree un [**objeto ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) llamando al método [**ID2D1Factory::CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) y pasando el [**objeto IDXGIDevice.**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)
4.  Cree un [**puntero ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) mediante el [**método ID2D1Device::CreateDeviceContext.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext)

## <a name="selecting-a-target"></a>Selección de un destino

El código aquí muestra cómo obtener la textura 2 dimensional de [**Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) para el búfer de reserva de ventana y crear un destino de mapa de bits que se vincula a esta textura a la que se representa el contexto del dispositivo [**Direct2D.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)


```C++
        // Allocate a descriptor.
        DXGI_SWAP_CHAIN_DESC1 swapChainDesc = {0};
        swapChainDesc.Width = 0;                           // use automatic sizing
        swapChainDesc.Height = 0;
        swapChainDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM; // this is the most common swapchain format
        swapChainDesc.Stereo = false; 
        swapChainDesc.SampleDesc.Count = 1;                // don't use multi-sampling
        swapChainDesc.SampleDesc.Quality = 0;
        swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapChainDesc.BufferCount = 2;                     // use double buffering to enable flip
        swapChainDesc.Scaling = DXGI_SCALING_NONE;
        swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL; // all apps must use this SwapEffect
        swapChainDesc.Flags = 0;

        // Identify the physical adapter (GPU or card) this device is runs on.
        ComPtr<IDXGIAdapter> dxgiAdapter;
        DX::ThrowIfFailed(
            dxgiDevice->GetAdapter(&dxgiAdapter)
            );

        // Get the factory object that created the DXGI device.
        ComPtr<IDXGIFactory2> dxgiFactory;
        DX::ThrowIfFailed(
            dxgiAdapter->GetParent(IID_PPV_ARGS(&dxgiFactory))
            );

        // Get the final swap chain for this window from the DXGI factory.
        DX::ThrowIfFailed(
            dxgiFactory->CreateSwapChainForCoreWindow(
                device.Get(),
                reinterpret_cast<IUnknown*>(m_window),
                &swapChainDesc,
                nullptr,    // allow on all displays
                &m_swapChain
                )
            );

        // Ensure that DXGI doesn't queue more than one frame at a time.
        DX::ThrowIfFailed(
            dxgiDevice->SetMaximumFrameLatency(1)
            );

    // Get the backbuffer for this window which is be the final 3D render target.
    ComPtr<ID3D11Texture2D> backBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&backBuffer))
        );

    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it is directly rendered to the 
    // swap chain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_IGNORE),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // Now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



Vamos a recorrer los pasos del ejemplo de código anterior.

1.  Asigne una [**estructura DXGI \_ SWAP CHAIN \_ \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) y defina la configuración de la cadena [**de intercambio**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).

    Esta configuración muestra un ejemplo de cómo crear una cadena de intercambio que una Windows store puede usar.

2.  Obtenga el adaptador en el que se ejecutan el dispositivo [**Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) y [**el dispositivo DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) y obtenga el objeto [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) asociado a ellos. Debe usar este generador **DXGI para** asegurarse de que la cadena [**de intercambio**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) se crea en el mismo adaptador.

3.  Llame al [**método IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) para crear la cadena de intercambio. Use la [**Windows::UI::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) para la ventana principal de una Windows Store.

    Asegúrese de establecer la latencia máxima del fotograma en 1 para minimizar el consumo de energía.

    Si desea representar contenido de Direct2D en una aplicación Windows Store, consulte el [**método CreateSwapChainForComposition.**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)

4.  Obtenga el búfer de reserva de la [**cadena de intercambio.**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) El búfer de reserva expone una [**interfaz ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) asignada por la cadena **de intercambio**

5.  Declare un [**struct D2D1 \_ BITMAP \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) y establezca los valores de propiedad. Establezca el formato de píxel en BGRA porque este es el formato que usan el [**dispositivo Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) y [**el dispositivo DXGI.**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)

6.  Obtenga el búfer de reserva como [**IDXGISurface para**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) pasarlo a Direct2D. Direct2D no acepta un [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) directamente.

    Cree un [**objeto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) desde el búfer de reserva mediante el [**método ID2D1DeviceContext::CreateBitmapFromDxgiSurface.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1))

7.  Ahora el [**mapa de bits de Direct2D**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) está vinculado al búfer de reserva. Establezca el destino en el contexto [**del dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) en el mapa de **bits**.

## <a name="how-to-render-and-display"></a>Representación y visualización

Ahora que tiene un mapa de bits de destino, puede dibujar primitivas, imágenes, efectos de imagen y texto en él mediante el contexto del dispositivo [**Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext). El código aquí muestra cómo dibujar un rectángulo.


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);

m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



Vamos a recorrer los pasos del ejemplo de código anterior.

1.  Llame a [**CreateSolidColorBrush para**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) crear un pincel para pintar el rectángulo.
2.  Llame al [**método BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir los comandos de dibujo.
3.  Llame al [**método DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) el rectángulo que se va a dibujar y el pincel.
4.  Llame al [**método EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) una vez que haya terminado de emitir comandos de dibujo.
5.  Para mostrar el resultado, llame [**al método IDXGISwapChain::P resent.**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)

Ahora puede usar el contexto del [**dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para dibujar primitivas, imágenes, efectos de imagen y texto en la pantalla.

 

 