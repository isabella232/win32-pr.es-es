---
title: Cómo representar mediante un contexto de dispositivo de Direct2D
description: En este tema, aprenderá a crear el contexto de dispositivo de Direct2D \ 32; en Windows 8.
ms.assetid: D4563FEA-767E-4B16-8F3C-3D548A64B206
keywords:
- Dispositivo Direct2D
- Contexto de dispositivo de Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2858861956a40bf969309be474105052e4692cde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104567674"
---
# <a name="how-to-render-by-using-a-direct2d-device-context"></a><span data-ttu-id="1275f-105">Cómo representar mediante un contexto de dispositivo de Direct2D</span><span class="sxs-lookup"><span data-stu-id="1275f-105">How to render by using a Direct2D device context</span></span>

<span data-ttu-id="1275f-106">En este tema, aprenderá a crear el [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) de [Direct2D](./direct2d-portal.md) en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1275f-106">In this topic you will learn about creating [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) in Windows 8.</span></span> <span data-ttu-id="1275f-107">Esta información se aplica si va a desarrollar aplicaciones de la tienda Windows o una aplicación de escritorio mediante Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1275f-107">This information applies to you if you are developing Windows Store apps or a desktop app by using Direct2D.</span></span> <span data-ttu-id="1275f-108">En este tema se describe el propósito de los objetos de contexto de dispositivo de Direct2D, cómo crear ese objeto y una guía paso a paso sobre la representación y visualización de imágenes y primitivas de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1275f-108">This topic describes the purpose of Direct2D device context objects, how to create that object , and a step by step guide about rendering and displaying Direct2D primitives and images.</span></span> <span data-ttu-id="1275f-109">También obtendrá información sobre cómo cambiar los destinos de representación y agregar efectos a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1275f-109">You will also learn about switching render targets and adding effects to your app.</span></span>

-   [<span data-ttu-id="1275f-110">¿Qué es un dispositivo Direct2D?</span><span class="sxs-lookup"><span data-stu-id="1275f-110">What is a Direct2D device?</span></span>](#what-is-a-direct2d-device)
-   [<span data-ttu-id="1275f-111">¿Qué es un contexto de dispositivo de Direct2D?</span><span class="sxs-lookup"><span data-stu-id="1275f-111">What is a Direct2D device context?</span></span>](#what-is-a-direct2d-device-context)
-   [<span data-ttu-id="1275f-112">Representar con Direct2D en Windows 8</span><span class="sxs-lookup"><span data-stu-id="1275f-112">Rendering with Direct2D on Windows 8</span></span>](#rendering-with-direct2d-on-windows-8)
-   [<span data-ttu-id="1275f-113">¿Por qué usar un contexto de dispositivo para la representación?</span><span class="sxs-lookup"><span data-stu-id="1275f-113">Why use a device context to render?</span></span>](#why-use-a-device-context-to-render)
-   [<span data-ttu-id="1275f-114">Cómo crear un contexto de dispositivo de Direct2D para la representación</span><span class="sxs-lookup"><span data-stu-id="1275f-114">How to create a Direct2D device context for rendering</span></span>](#how-to-create-a-direct2d-device-context-for-rendering)
-   [<span data-ttu-id="1275f-115">Seleccionar un destino</span><span class="sxs-lookup"><span data-stu-id="1275f-115">Selecting a target</span></span>](#selecting-a-target)
-   [<span data-ttu-id="1275f-116">Cómo representar y mostrar</span><span class="sxs-lookup"><span data-stu-id="1275f-116">How to render and display</span></span>](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a><span data-ttu-id="1275f-117">¿Qué es un dispositivo Direct2D?</span><span class="sxs-lookup"><span data-stu-id="1275f-117">What is a Direct2D device?</span></span>

<span data-ttu-id="1275f-118">Necesita un dispositivo de Direct2D y un dispositivo de Direct3D para crear un contexto de dispositivo de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1275f-118">You need a Direct2D device and a Direct3D device to create a Direct2D device context.</span></span> <span data-ttu-id="1275f-119">Un [**dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (expone un puntero de interfaz **ID2D1Device** ) representa un adaptador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="1275f-119">A [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (exposes an **ID2D1Device** interface pointer) represents a display adapter.</span></span> <span data-ttu-id="1275f-120">Un dispositivo Direct3D (expone un puntero de interfaz [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) ) está asociado a un dispositivo Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1275f-120">A Direct3D device (exposes an [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) interface pointer) is associated with a Direct2D device.</span></span> <span data-ttu-id="1275f-121">Cada aplicación debe tener un **dispositivo Direct2D**, pero puede tener más de un **dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="1275f-121">Each app must have one **Direct2D device**, but can have more than one **device**.</span></span>

## <a name="what-is-a-direct2d-device-context"></a><span data-ttu-id="1275f-122">¿Qué es un contexto de dispositivo de Direct2D?</span><span class="sxs-lookup"><span data-stu-id="1275f-122">What is a Direct2D device context?</span></span>

<span data-ttu-id="1275f-123">Un [](./direct2d-portal.md) [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) de Direct2D (expone un puntero de interfaz **ID2D1DeviceContext** ) representa un conjunto de búferes de estado y de comandos que se usa para representar en un destino.</span><span class="sxs-lookup"><span data-stu-id="1275f-123">A [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) (exposes an **ID2D1DeviceContext** interface pointer) represents a set of state and command buffers that you use to render to a target.</span></span> <span data-ttu-id="1275f-124">Puede llamar a métodos en el contexto de dispositivo para establecer el estado de la canalización y generar comandos de representación mediante el uso de los recursos que pertenecen a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1275f-124">You can call methods on the device context to set pipeline state and generate rendering commands by using the resources owned by a device.</span></span>

## <a name="rendering-with-direct2d-on-windows-8"></a><span data-ttu-id="1275f-125">Representar con Direct2D en Windows 8</span><span class="sxs-lookup"><span data-stu-id="1275f-125">Rendering with Direct2D on Windows 8</span></span>

<span data-ttu-id="1275f-126">En Windows 7 y versiones anteriores, se usa una [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) u otra interfaz de destino de representación para representar en una ventana o una superficie.</span><span class="sxs-lookup"><span data-stu-id="1275f-126">On Windows 7 and earlier, you use a [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) or another render target interface to render to a window or surface.</span></span> <span data-ttu-id="1275f-127">A partir de Windows 8, no se recomienda la representación mediante métodos que se basan en interfaces como **ID2D1HwndRenderTarget** , ya que no funcionarán con las aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="1275f-127">Starting with Windows 8, we do not recommend rendering by using methods that rely on interfaces like **ID2D1HwndRenderTarget** because they won't work with Windows Store apps.</span></span> <span data-ttu-id="1275f-128">Puede usar un [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para representarlo en un HWND si quiere crear una aplicación de escritorio y seguir aprovechando las características adicionales **del contexto del dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="1275f-128">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to render to an Hwnd if you want to make a desktop app and still take advantage of the **device context's** additional features.</span></span> <span data-ttu-id="1275f-129">Sin embargo, el **contexto del dispositivo** es necesario para representar el contenido en las aplicaciones de la tienda Windows con [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="1275f-129">However, the **device context** is required to render content in a Windows Store apps with [Direct2D](./direct2d-portal.md).</span></span>

## <a name="why-use-a-device-context-to-render"></a><span data-ttu-id="1275f-130">¿Por qué usar un contexto de dispositivo para la representación?</span><span class="sxs-lookup"><span data-stu-id="1275f-130">Why use a device context to render?</span></span>

-   <span data-ttu-id="1275f-131">Puede representar aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="1275f-131">You can render for Windows Store apps.</span></span>
-   <span data-ttu-id="1275f-132">Puede cambiar el destino de representación en cualquier momento antes, durante y después de la representación.</span><span class="sxs-lookup"><span data-stu-id="1275f-132">You can change the render target at any time before, during, and after rendering.</span></span> <span data-ttu-id="1275f-133">El contexto de dispositivo garantiza que las llamadas a métodos de dibujo se ejecutan en orden y se aplican al cambiar el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="1275f-133">The device context ensures that the calls to drawing methods are executed in order and applies them when you switch the render target.</span></span>
-   <span data-ttu-id="1275f-134">Puede usar más de un tipo de ventana con un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1275f-134">You can use more than one type of window with a device context.</span></span> <span data-ttu-id="1275f-135">Puede usar un [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) y una [**cadena de intercambio de DXGI**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) para representar directamente en [**Windows:: UI:: Core:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) o en [**Windows:: UI:: XAML:: SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).</span><span class="sxs-lookup"><span data-stu-id="1275f-135">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) to render directly to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) or a [**Windows::UI::XAML::SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).</span></span>
-   <span data-ttu-id="1275f-136">Puede usar el [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) de [direct2d](./direct2d-portal.md) para crear [efectos de direct2d](effects-overview.md) y representar la salida de un gráfico de efecto o efecto de imagen en un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="1275f-136">You can use the [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to create [Direct2D effects](effects-overview.md) and to render the output of an image effect or effect graph to a render target.</span></span>
-   <span data-ttu-id="1275f-137">Puede tener varios [**contextos de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), lo que puede ser útil para mejorar el rendimiento en una aplicación de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1275f-137">You can have multiple [**device contexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), which can be helpful for improving performance in a threaded app.</span></span> <span data-ttu-id="1275f-138">Para obtener más información, vea [aplicaciones de Direct2D multiproceso](multi-threaded-direct2d-apps.md) .</span><span class="sxs-lookup"><span data-stu-id="1275f-138">See [Multithreaded Direct2D apps](multi-threaded-direct2d-apps.md) for more information.</span></span>
-   <span data-ttu-id="1275f-139">El [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interopera estrechamente con Direct3D, lo que le proporciona más acceso a las opciones de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1275f-139">The [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interoperates closely with Direct3D, giving you more access to Direct3D options.</span></span>

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a><span data-ttu-id="1275f-140">Cómo crear un contexto de dispositivo de Direct2D para la representación</span><span class="sxs-lookup"><span data-stu-id="1275f-140">How to create a Direct2D device context for rendering</span></span>

<span data-ttu-id="1275f-141">En este código se muestra cómo crear un dispositivo Direct3D 11, obtener el dispositivo DXGI asociado, crear un [**dispositivo direct2d**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)y, por último, crear el [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) de direct2d para la representación.</span><span class="sxs-lookup"><span data-stu-id="1275f-141">The code here shows you how to create a Direct3D11 device, get the associated DXGI device, create a [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device), and then finally create the Direct2D [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) for rendering.</span></span>

<span data-ttu-id="1275f-142">Este es un diagrama de las llamadas a métodos y las interfaces que este código usa.</span><span class="sxs-lookup"><span data-stu-id="1275f-142">Here is a diagram of the method calls and the interfaces this code uses.</span></span>

![diagrama de dispositivos y contextos de dispositivos de direct2d y Direct3D.](images/devicecontextdiagram.png)

> [!Note]  
> <span data-ttu-id="1275f-144">En este código se supone que ya tiene un objeto [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) . para obtener más información, consulte la [**Página de referencia de ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="1275f-144">This code assumes you already have an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) object, for more information see the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>

 


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



<span data-ttu-id="1275f-145">Vamos a recorrer los pasos descritos en el ejemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="1275f-145">Let's walk through the steps in the preceding code sample.</span></span>

1.  <span data-ttu-id="1275f-146">Obtener un puntero de la interfaz ID3D11Device lo necesitará para crear el contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1275f-146">Get an ID3D11Device interface pointer you will need this to create the device context.</span></span>

    -   <span data-ttu-id="1275f-147">Declare las marcas de creación para configurar el dispositivo [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para la compatibilidad con BGRA.</span><span class="sxs-lookup"><span data-stu-id="1275f-147">Declare the creation flags to set up the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) device for BGRA support.</span></span> <span data-ttu-id="1275f-148">[Direct2D](./direct2d-portal.md) requiere el orden de color BGRA.</span><span class="sxs-lookup"><span data-stu-id="1275f-148">[Direct2D](./direct2d-portal.md) requires BGRA color order.</span></span>
    -   <span data-ttu-id="1275f-149">Declare una matriz de entradas de [**\_ \_ nivel de característica D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) que represente el conjunto de niveles de características que admitirá la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1275f-149">Declare an array of [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) entries representing the set of feature levels that your app will support.</span></span>
        > [!Note]  
        > <span data-ttu-id="1275f-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) busca en la lista hasta que encuentre el nivel de características admitido por el sistema host.</span><span class="sxs-lookup"><span data-stu-id="1275f-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) searches your list until it finds the feature level supported by the host system.</span></span>

         

    -   <span data-ttu-id="1275f-151">Usar la función [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) para crear un objeto [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) , la función también devolverá un objeto [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) , pero ese objeto no es necesario en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1275f-151">Use the [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) function to create an [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) object, the function will also return an [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) object, but that object is not needed for this example.</span></span>

2.  <span data-ttu-id="1275f-152">Consulte el [**dispositivo Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) para su interfaz de [**dispositivo DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="1275f-152">Query the [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) for its [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) interface.</span></span>
3.  <span data-ttu-id="1275f-153">Cree un objeto [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) llamando al método [**ID2D1Factory:: CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) y pasando el objeto [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="1275f-153">Create an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) object by calling the [**ID2D1Factory::CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) method and passing in the [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) object.</span></span>
4.  <span data-ttu-id="1275f-154">Cree un puntero [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) mediante el método [**ID2D1Device:: CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) .</span><span class="sxs-lookup"><span data-stu-id="1275f-154">Create an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pointer using the [**ID2D1Device::CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) method.</span></span>

## <a name="selecting-a-target"></a><span data-ttu-id="1275f-155">Seleccionar un destino</span><span class="sxs-lookup"><span data-stu-id="1275f-155">Selecting a target</span></span>

<span data-ttu-id="1275f-156">En el código siguiente se muestra cómo obtener la [**textura de Direct3D bidimensional**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) para el búfer de reserva de la ventana y cómo crear un destino de mapa de bits que se vincula a esta textura en la que se representa el [**contexto de dispositivo de Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="1275f-156">The code here shows you how to get the [**2 dimensional Direct3D texture**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) for the window back buffer and create a bitmap target that links to this texture to which the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) renders.</span></span>


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



<span data-ttu-id="1275f-157">Vamos a recorrer los pasos del ejemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="1275f-157">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="1275f-158">Asigne una [**estructura \_ \_ \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) de la cadena de intercambio de DXGI y defina la configuración de la [**cadena de intercambio**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="1275f-158">Allocate a [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and define the settings for the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

    <span data-ttu-id="1275f-159">Esta configuración muestra un ejemplo de cómo crear una cadena de intercambio que puede usar una aplicación de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="1275f-159">These settings show an example of how to create a swap chain that a Windows Store app can use.</span></span>

2.  <span data-ttu-id="1275f-160">Obtiene el adaptador en el que se ejecutan el [**dispositivo Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) y el [**dispositivo DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) y obtiene el objeto [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) asociado a ellos.</span><span class="sxs-lookup"><span data-stu-id="1275f-160">Get the adapter that the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) are running on and get the [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) object associated with them.</span></span> <span data-ttu-id="1275f-161">Debe usar esta **fábrica de DXGI** para asegurarse de que la [**cadena de intercambio**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) se crea en el mismo adaptador.</span><span class="sxs-lookup"><span data-stu-id="1275f-161">You must use this **DXGI factory** to ensure the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) is created on the same adapter.</span></span>

3.  <span data-ttu-id="1275f-162">Llame al método [**IDXGIFactory2:: CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) para crear la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="1275f-162">Call the [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) method to create the swap chain.</span></span> <span data-ttu-id="1275f-163">Use la clase [**Windows:: UI:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) para la ventana principal de una aplicación de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="1275f-163">Use the [**Windows::UI::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) class for the main window of a Windows Store app.</span></span>

    <span data-ttu-id="1275f-164">Asegúrese de establecer la latencia máxima de fotogramas en 1 para minimizar el consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="1275f-164">Make sure to set the maximum frame latency to 1 to minimize power consumption.</span></span>

    <span data-ttu-id="1275f-165">Si quiere representar contenido de Direct2D en una aplicación de la tienda Windows, consulte el método [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .</span><span class="sxs-lookup"><span data-stu-id="1275f-165">If you want to render Direct2D content in a Windows Store app, see the [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method.</span></span>

4.  <span data-ttu-id="1275f-166">Obtiene el búfer de reserva de la [**cadena de intercambio**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="1275f-166">Get the back buffer from the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span> <span data-ttu-id="1275f-167">El búfer de reserva expone una interfaz [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) asignada por la **cadena de intercambio**</span><span class="sxs-lookup"><span data-stu-id="1275f-167">The back buffer exposes an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) interface allocated by the **swap chain**</span></span>

5.  <span data-ttu-id="1275f-168">Declare un [**D2D1 \_ Bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct y establezca los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="1275f-168">Declare a [**D2D1\_BITMAP\_PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct and set the property values.</span></span> <span data-ttu-id="1275f-169">Establezca el formato de píxel en BGRA porque es el formato que usa el [**dispositivo Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) y el [**dispositivo DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="1275f-169">Set the pixel format to BGRA because this is the format the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) use.</span></span>

6.  <span data-ttu-id="1275f-170">Obtiene el búfer de reserva como [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) para pasar a Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1275f-170">Get the back buffer as an [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) to pass to Direct2D.</span></span> <span data-ttu-id="1275f-171">Direct2D no acepta un [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) directamente.</span><span class="sxs-lookup"><span data-stu-id="1275f-171">Direct2D doesn't accept an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) directly.</span></span>

    <span data-ttu-id="1275f-172">Cree un objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a partir del búfer de reserva mediante el método [**ID2D1DeviceContext:: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) .</span><span class="sxs-lookup"><span data-stu-id="1275f-172">Create a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object from the back buffer using the [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method.</span></span>

7.  <span data-ttu-id="1275f-173">Ahora el [**mapa de bits de Direct2D**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) está vinculado al búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="1275f-173">Now the [**Direct2D bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is linked to the back buffer.</span></span> <span data-ttu-id="1275f-174">Establezca el destino en el [**contexto de dispositivo de Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) en el **mapa de bits**.</span><span class="sxs-lookup"><span data-stu-id="1275f-174">Set the target on the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to the **bitmap**.</span></span>

## <a name="how-to-render-and-display"></a><span data-ttu-id="1275f-175">Cómo representar y mostrar</span><span class="sxs-lookup"><span data-stu-id="1275f-175">How to render and display</span></span>

<span data-ttu-id="1275f-176">Ahora que tiene un mapa de bits de destino, puede dibujar primitivos, imágenes, efectos de imagen y texto en él mediante el [**contexto de dispositivo de Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span><span class="sxs-lookup"><span data-stu-id="1275f-176">Now that you have a target bitmap, you can draw primitives, images, image effects, and text to it using the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span></span> <span data-ttu-id="1275f-177">En el código siguiente se muestra cómo dibujar un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="1275f-177">The code here shows you how to draw a rectangle.</span></span>


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



<span data-ttu-id="1275f-178">Vamos a recorrer los pasos del ejemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="1275f-178">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="1275f-179">Llame a [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) para crear un pincel para pintar el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="1275f-179">Call the [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) to create a brush to paint the rectangle.</span></span>
2.  <span data-ttu-id="1275f-180">Llame al método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir cualquier comando de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1275f-180">Call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands.</span></span>
3.  <span data-ttu-id="1275f-181">Llame al método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) del rectángulo que se va a dibujar y al pincel.</span><span class="sxs-lookup"><span data-stu-id="1275f-181">Call the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method the rectangle to be drawn and the brush.</span></span>
4.  <span data-ttu-id="1275f-182">Llame al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) una vez que haya terminado de emitir comandos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1275f-182">Call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span>
5.  <span data-ttu-id="1275f-183">Muestre el resultado mediante una llamada al método [**IDXGISwapChain::P reenviar**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) .</span><span class="sxs-lookup"><span data-stu-id="1275f-183">Display the result by calling the [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method.</span></span>

<span data-ttu-id="1275f-184">Ahora puede usar el [**contexto de dispositivo de Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para dibujar primitivos, imágenes, efectos de imagen y texto en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1275f-184">Now you can use the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) draw primitives, images, image effects, and text to the screen.</span></span>

 

 