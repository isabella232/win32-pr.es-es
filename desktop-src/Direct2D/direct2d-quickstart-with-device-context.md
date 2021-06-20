---
title: Inicio rápido de Direct2D para Windows 8
description: Resume los pasos necesarios para dibujar con Direct2D para Windows 8 y proporciona código de ejemplo. Direct2D es una API de código nativo para crear gráficos 2D.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D, ejemplo de código de rectángulo de dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43442e57ed0949bdf39fc05ce1a69fded42b4b3d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406148"
---
# <a name="direct2d-quickstart-for-windows-8"></a><span data-ttu-id="c15f6-105">Inicio rápido de Direct2D para Windows 8</span><span class="sxs-lookup"><span data-stu-id="c15f6-105">Direct2D Quickstart for Windows 8</span></span>

<span data-ttu-id="c15f6-106">Direct2D es una API en modo inmediato de código nativo para crear gráficos 2D.</span><span class="sxs-lookup"><span data-stu-id="c15f6-106">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="c15f6-107">En este tema se muestra cómo usar Direct2D para dibujar en [**windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="c15f6-107">This topic illustrates how to use Direct2D to draw to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

<span data-ttu-id="c15f6-108">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="c15f6-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="c15f6-109">Dibujar un rectángulo simple</span><span class="sxs-lookup"><span data-stu-id="c15f6-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="c15f6-110">Paso 1: Incluir encabezado Direct2D</span><span class="sxs-lookup"><span data-stu-id="c15f6-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="c15f6-111">Paso 2: Crear un id2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="c15f6-111">Step 2: Create an ID2D1Factory1</span></span>](#step-2-create-an-id2d1factory1)
-   [<span data-ttu-id="c15f6-112">Paso 3: Crear un ID2D1Device y un ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="c15f6-112">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [<span data-ttu-id="c15f6-113">Paso 4: Crear un pincel</span><span class="sxs-lookup"><span data-stu-id="c15f6-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="c15f6-114">Paso 5: Dibujar el rectángulo</span><span class="sxs-lookup"><span data-stu-id="c15f6-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="c15f6-115">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="c15f6-115">Example code</span></span>](#example-code)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="c15f6-116">Dibujar un rectángulo simple</span><span class="sxs-lookup"><span data-stu-id="c15f6-116">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="c15f6-117">Para dibujar un rectángulo mediante [GDI,](/windows/desktop/gdi/windows-gdi)puede controlar el [**mensaje WM \_ PAINT,**](/windows/desktop/gdi/wm-paint) como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="c15f6-117">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



<span data-ttu-id="c15f6-118">El código para dibujar el mismo rectángulo con Direct2D es similar: crea recursos de dibujo, describe una forma para dibujar, dibuja la forma y, a continuación, libera los recursos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c15f6-118">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="c15f6-119">En las secciones siguientes se describe cada uno de estos pasos con detalle.</span><span class="sxs-lookup"><span data-stu-id="c15f6-119">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="c15f6-120">Paso 1: Incluir encabezado Direct2D</span><span class="sxs-lookup"><span data-stu-id="c15f6-120">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="c15f6-121">Además de los encabezados necesarios para la aplicación, incluya los encabezados d2d1.h y d2d1 \_ 1.h.</span><span class="sxs-lookup"><span data-stu-id="c15f6-121">In addition to the headers required for the application, include the d2d1.h and d2d1\_1.h headers.</span></span>

## <a name="step-2-create-an-id2d1factory1"></a><span data-ttu-id="c15f6-122">Paso 2: Crear un id2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="c15f6-122">Step 2: Create an ID2D1Factory1</span></span>

<span data-ttu-id="c15f6-123">Una de las primeras cosas que hace cualquier ejemplo de Direct2D es crear un [**id2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span><span class="sxs-lookup"><span data-stu-id="c15f6-123">One of the first things that any Direct2D example does is create an [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span></span>


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



<span data-ttu-id="c15f6-124">La [**interfaz ID2D1Factory1 es**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) el punto de partida para usar Direct2D; use un **id2D1Factory1 para** crear recursos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="c15f6-124">The [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface is the starting point for using Direct2D; use an **ID2D1Factory1** to create Direct2D resources.</span></span>

<span data-ttu-id="c15f6-125">Al crear un generador, puede especificar si es multiproceso o de subproceso único.</span><span class="sxs-lookup"><span data-stu-id="c15f6-125">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="c15f6-126">(Para obtener más información sobre factorías multiproceso, vea los comentarios en la página de referencia [**de ID2D1Factory).**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) En este ejemplo se crea un generador de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="c15f6-126">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="c15f6-127">En general, la aplicación debe crear el generador una vez y conservarlo durante la vida útil de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c15f6-127">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a><span data-ttu-id="c15f6-128">Paso 3: Crear un ID2D1Device y un ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="c15f6-128">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>

<span data-ttu-id="c15f6-129">Después de crear un generador, úselo para crear un dispositivo Direct2D y, a continuación, use el dispositivo para crear un contexto de dispositivo Direct2D.</span><span class="sxs-lookup"><span data-stu-id="c15f6-129">After you create a factory, use it to create a Direct2D device and then use the device to create a Direct2D device context.</span></span> <span data-ttu-id="c15f6-130">Para crear estos objetos de Direct2D, debe tener un dispositivo [**Direct3D 11,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) un dispositivo [**DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)y una [**cadena de intercambio DXGI**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span><span class="sxs-lookup"><span data-stu-id="c15f6-130">In order to create these Direct2D objects, you must have a [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , a [**DXGI device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice), and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="c15f6-131">Consulte [Devices and Device Contexts (Dispositivos y contextos de dispositivo)](devices-and-device-contexts.md) para obtener información sobre cómo crear los requisitos previos necesarios.</span><span class="sxs-lookup"><span data-stu-id="c15f6-131">See [Devices and Device Contexts](devices-and-device-contexts.md) for info on creating the necessary prerequisites.</span></span>


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



<span data-ttu-id="c15f6-132">Un contexto de dispositivo es un dispositivo que puede realizar operaciones de dibujo y crear recursos de dibujo dependientes del dispositivo, como pinceles.</span><span class="sxs-lookup"><span data-stu-id="c15f6-132">A device context is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="c15f6-133">También se usa el contexto del dispositivo para vincular [**id2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a una superficie DXGI para usarla como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="c15f6-133">You also use the device context to link a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) to a DXGI surface to use as a render target.</span></span> <span data-ttu-id="c15f6-134">El contexto del dispositivo se puede representar en diferentes tipos de destinos.</span><span class="sxs-lookup"><span data-stu-id="c15f6-134">The device context can render to different types of targets.</span></span>

<span data-ttu-id="c15f6-135">El código aquí declara las propiedades del mapa de bits que se vincula a una cadena de intercambio DXGI que se representa en [**una instancia de CoreWindow.**](/uwp/api/Windows.UI.Core.CoreWindow)</span><span class="sxs-lookup"><span data-stu-id="c15f6-135">The code here declares the properties for bitmap that links to a DXGI swap chain that renders to a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span> <span data-ttu-id="c15f6-136">El [**método ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) obtiene una superficie direct2D de la superficie DXGI.</span><span class="sxs-lookup"><span data-stu-id="c15f6-136">The [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method gets a Direct2D surface from the DXGI surface.</span></span> <span data-ttu-id="c15f6-137">Esto hace que todo lo que se represente en el [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) de destino se represente en la superficie de la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="c15f6-137">This makes it so anything rendered to the target [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is rendered to the surface of the swap chain.</span></span>

<span data-ttu-id="c15f6-138">Una vez que tenga la superficie de Direct2D, use el método [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) para establecerla como destino de representación activo.</span><span class="sxs-lookup"><span data-stu-id="c15f6-138">Once you have the Direct2D surface, use the [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) method to set it as the active render target.</span></span>


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
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

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a><span data-ttu-id="c15f6-139">Paso 4: Crear un pincel</span><span class="sxs-lookup"><span data-stu-id="c15f6-139">Step 4: Create a Brush</span></span>

<span data-ttu-id="c15f6-140">Al igual que un generador, un contexto de dispositivo puede crear recursos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c15f6-140">Like a factory, a device context can create drawing resources.</span></span> <span data-ttu-id="c15f6-141">En este ejemplo, el contexto del dispositivo crea un pincel.</span><span class="sxs-lookup"><span data-stu-id="c15f6-141">In this example, the device context creates a brush.</span></span>


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



<span data-ttu-id="c15f6-142">Un pincel es un objeto que pinta un área, como el trazo de una forma o el relleno de una geometría.</span><span class="sxs-lookup"><span data-stu-id="c15f6-142">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="c15f6-143">El pincel de este ejemplo pinta un área con un color sólido predefinido, negro.</span><span class="sxs-lookup"><span data-stu-id="c15f6-143">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="c15f6-144">Direct2D también proporciona otros tipos de pinceles: pinceles de [](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) degradado para pintar degradados lineales y radiales, un [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) pincel de mapa de bits para pintar con mapas de bits y patrones, y a partir de Windows 8, un pincel de imagen para pintar con una imagen representado.</span><span class="sxs-lookup"><span data-stu-id="c15f6-144">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, a [**bitmap brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) for painting with bitmaps and patterns, and starting in Windows 8, an [**image brush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) for painting with a rendered image.</span></span>

<span data-ttu-id="c15f6-145">Algunas API de dibujo proporcionan lápices para dibujar contornos y pinceles para rellenar formas.</span><span class="sxs-lookup"><span data-stu-id="c15f6-145">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="c15f6-146">Direct2D es diferente: no proporciona un objeto de lápiz, sino que usa un pincel para dibujar contornos y rellenar formas.</span><span class="sxs-lookup"><span data-stu-id="c15f6-146">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="c15f6-147">Al dibujar contornos, use la interfaz [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) o a partir de Windows 8 la interfaz [**ID2D1StrokeStyle1,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) con un pincel para controlar las operaciones de trazado de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c15f6-147">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface, or starting in Windows 8 the [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) interface, with a brush to control path stroking operations.</span></span>

<span data-ttu-id="c15f6-148">Solo se puede usar un pincel con el destino de representación que lo creó y con otros destinos de representación en el mismo dominio de recursos.</span><span class="sxs-lookup"><span data-stu-id="c15f6-148">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="c15f6-149">En general, debe crear pinceles una vez y conservarlos durante la vida del destino de representación que los creó.</span><span class="sxs-lookup"><span data-stu-id="c15f6-149">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="c15f6-150">[**ID2D1SolidColorBrush es**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) la única excepción; Dado que es relativamente económico crearlo, puede crear un **objeto ID2D1SolidColorBrush** cada vez que dibuje un marco, sin que se note ningún impacto en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c15f6-150">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="c15f6-151">También puede usar un único **ID2D1SolidColorBrush** y cambiar su color u opacidad cada vez que lo use.</span><span class="sxs-lookup"><span data-stu-id="c15f6-151">You can also use a single **ID2D1SolidColorBrush** and just change its color or opacity every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="c15f6-152">Paso 5: Dibujar el rectángulo</span><span class="sxs-lookup"><span data-stu-id="c15f6-152">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="c15f6-153">A continuación, use el contexto del dispositivo para dibujar el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="c15f6-153">Next, use the device context to draw the rectangle.</span></span>


```C++
 
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



<span data-ttu-id="c15f6-154">El [**método DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) toma dos parámetros: el rectángulo que se va a dibujar y el pincel que se va a usar para pintar el contorno del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="c15f6-154">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="c15f6-155">Opcionalmente, también puede especificar el ancho del trazo, el patrón de guiones, la combinación de línea y las opciones de extremo.</span><span class="sxs-lookup"><span data-stu-id="c15f6-155">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="c15f6-156">Debe llamar al [**método BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir los comandos de dibujo y debe llamar al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) una vez que haya terminado de emitir comandos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c15f6-156">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="c15f6-157">El **método EndDraw** devuelve **un valor HRESULT** que indica si los comandos de dibujo se han realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c15f6-157">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span> <span data-ttu-id="c15f6-158">Si no se realiza correctamente, la función auxiliar ThrowIfFailed producirá una excepción.</span><span class="sxs-lookup"><span data-stu-id="c15f6-158">If it is not successful, the ThrowIfFailed helper function will throw an exception.</span></span>

<span data-ttu-id="c15f6-159">El [**método IDXGISwapChain::P resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) intercambia la superficie del búfer con la superficie en pantalla para mostrar el resultado.</span><span class="sxs-lookup"><span data-stu-id="c15f6-159">The [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method swaps the buffer surface with the on screen surface to display the result.</span></span>

## <a name="example-code"></a><span data-ttu-id="c15f6-160">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="c15f6-160">Example code</span></span>

<span data-ttu-id="c15f6-161">El código de este tema muestra los elementos básicos de una aplicación de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="c15f6-161">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="c15f6-162">Por brevedad, el tema omite el marco de trabajo de la aplicación y el código de control de errores que es característica de una aplicación bien escrita.</span><span class="sxs-lookup"><span data-stu-id="c15f6-162">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span>

 

 