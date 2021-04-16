---
title: Inicio rápido de Direct2D para Windows 8
description: Resume los pasos necesarios para dibujar con Direct2D y proporciona código de ejemplo.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Ejemplo de código de rectángulo de Direct2D, dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28e5cfbbf4e63e129a43bec783a64203e20e30a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656371"
---
# <a name="direct2d-quickstart-for-windows-8"></a><span data-ttu-id="76cd5-104">Inicio rápido de Direct2D para Windows 8</span><span class="sxs-lookup"><span data-stu-id="76cd5-104">Direct2D Quickstart for Windows 8</span></span>

<span data-ttu-id="76cd5-105">Direct2D es una API de modo inmediato y de código nativo para crear gráficos 2D.</span><span class="sxs-lookup"><span data-stu-id="76cd5-105">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="76cd5-106">En este tema se muestra cómo usar Direct2D para dibujar en [**Windows:: UI:: Core:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="76cd5-106">This topic illustrates how to use Direct2D to draw to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

<span data-ttu-id="76cd5-107">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="76cd5-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="76cd5-108">Dibujar un rectángulo simple</span><span class="sxs-lookup"><span data-stu-id="76cd5-108">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="76cd5-109">Paso 1: incluir el encabezado de Direct2D</span><span class="sxs-lookup"><span data-stu-id="76cd5-109">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="76cd5-110">Paso 2: creación de un ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="76cd5-110">Step 2: Create an ID2D1Factory1</span></span>](#step-2-create-an-id2d1factory1)
-   [<span data-ttu-id="76cd5-111">Paso 3: creación de un ID2D1Device y un ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="76cd5-111">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [<span data-ttu-id="76cd5-112">Paso 4: crear un pincel</span><span class="sxs-lookup"><span data-stu-id="76cd5-112">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="76cd5-113">Paso 5: dibujo del rectángulo</span><span class="sxs-lookup"><span data-stu-id="76cd5-113">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="76cd5-114">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="76cd5-114">Example code</span></span>](#example-code)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="76cd5-115">Dibujar un rectángulo simple</span><span class="sxs-lookup"><span data-stu-id="76cd5-115">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="76cd5-116">Para dibujar un rectángulo mediante [GDI](/windows/desktop/gdi/windows-gdi), podría controlar el mensaje [**de \_ dibujo de WM**](/windows/desktop/gdi/wm-paint) , tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="76cd5-116">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


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



<span data-ttu-id="76cd5-117">El código para dibujar el mismo rectángulo con Direct2D es similar: crea recursos de dibujo, describe una forma para dibujar, dibuja la forma y, a continuación, libera los recursos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="76cd5-117">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="76cd5-118">En las secciones siguientes se describe detalladamente cada uno de estos pasos.</span><span class="sxs-lookup"><span data-stu-id="76cd5-118">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="76cd5-119">Paso 1: incluir el encabezado de Direct2D</span><span class="sxs-lookup"><span data-stu-id="76cd5-119">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="76cd5-120">Además de los encabezados necesarios para la aplicación, incluya los encabezados d2d1. h y d2d1 \_ 1. h.</span><span class="sxs-lookup"><span data-stu-id="76cd5-120">In addition to the headers required for the application, include the d2d1.h and d2d1\_1.h headers.</span></span>

## <a name="step-2-create-an-id2d1factory1"></a><span data-ttu-id="76cd5-121">Paso 2: creación de un ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="76cd5-121">Step 2: Create an ID2D1Factory1</span></span>

<span data-ttu-id="76cd5-122">Una de las primeras cosas que hace cualquier ejemplo de Direct2D es crear un [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span><span class="sxs-lookup"><span data-stu-id="76cd5-122">One of the first things that any Direct2D example does is create an [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span></span>


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



<span data-ttu-id="76cd5-123">La interfaz [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) es el punto de partida para usar Direct2D; Use un **ID2D1Factory1** para crear recursos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="76cd5-123">The [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface is the starting point for using Direct2D; use an **ID2D1Factory1** to create Direct2D resources.</span></span>

<span data-ttu-id="76cd5-124">Al crear una factoría, puede especificar si es multiproceso o de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="76cd5-124">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="76cd5-125">(Para obtener más información sobre los generadores multiproceso, consulte la sección Comentarios en la [**Página de referencia de ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)). En este ejemplo se crea un generador de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="76cd5-125">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="76cd5-126">En general, la aplicación debe crear el generador una vez y conservarlo durante la vida de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="76cd5-126">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a><span data-ttu-id="76cd5-127">Paso 3: creación de un ID2D1Device y un ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="76cd5-127">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>

<span data-ttu-id="76cd5-128">Después de crear un generador, úselo para crear un dispositivo de Direct2D y, a continuación, use el dispositivo para crear un contexto de dispositivo de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="76cd5-128">After you create a factory, use it to create a Direct2D device and then use the device to create a Direct2D device context.</span></span> <span data-ttu-id="76cd5-129">Para crear estos objetos de Direct2D, debe tener un [**dispositivo Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , un [**dispositivo dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)y una [**cadena de intercambio de dxgi**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span><span class="sxs-lookup"><span data-stu-id="76cd5-129">In order to create these Direct2D objects, you must have a [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , a [**DXGI device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice), and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="76cd5-130">Consulte [dispositivos y contextos de dispositivos](devices-and-device-contexts.md) para obtener información sobre cómo crear los requisitos previos necesarios.</span><span class="sxs-lookup"><span data-stu-id="76cd5-130">See [Devices and Device Contexts](devices-and-device-contexts.md) for info on creating the necessary prerequisites.</span></span>


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



<span data-ttu-id="76cd5-131">Un contexto de dispositivo es un dispositivo que puede realizar operaciones de dibujo y crear recursos de dibujo dependientes del dispositivo, como los pinceles.</span><span class="sxs-lookup"><span data-stu-id="76cd5-131">A device context is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="76cd5-132">También se usa el contexto de dispositivo para vincular un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a una superficie de DXGI que se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="76cd5-132">You also use the device context to link a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) to a DXGI surface to use as a render target.</span></span> <span data-ttu-id="76cd5-133">El contexto del dispositivo se puede representar en diferentes tipos de destinos.</span><span class="sxs-lookup"><span data-stu-id="76cd5-133">The device context can render to different types of targets.</span></span>

<span data-ttu-id="76cd5-134">El código que se muestra aquí declara las propiedades para el mapa de bits que se vincula a una cadena de intercambio de DXGI que se representa en [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="76cd5-134">The code here declares the properties for bitmap that links to a DXGI swap chain that renders to a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span> <span data-ttu-id="76cd5-135">El método [**ID2D1DeviceContext:: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) obtiene una superficie de Direct2D de la superficie de DXGI.</span><span class="sxs-lookup"><span data-stu-id="76cd5-135">The [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method gets a Direct2D surface from the DXGI surface.</span></span> <span data-ttu-id="76cd5-136">Esto hace que todo lo que se represente en el [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) de destino se represente en la superficie de la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="76cd5-136">This makes it so anything rendered to the target [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is rendered to the surface of the swap chain.</span></span>

<span data-ttu-id="76cd5-137">Una vez que tenga la superficie de Direct2D, use el método [**ID2D1DeviceContext:: SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) para establecerla como destino de representación activo.</span><span class="sxs-lookup"><span data-stu-id="76cd5-137">Once you have the Direct2D surface, use the [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) method to set it as the active render target.</span></span>


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



## <a name="step-4-create-a-brush"></a><span data-ttu-id="76cd5-138">Paso 4: crear un pincel</span><span class="sxs-lookup"><span data-stu-id="76cd5-138">Step 4: Create a Brush</span></span>

<span data-ttu-id="76cd5-139">Al igual que un generador, un contexto de dispositivo puede crear recursos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="76cd5-139">Like a factory, a device context can create drawing resources.</span></span> <span data-ttu-id="76cd5-140">En este ejemplo, el contexto de dispositivo crea un pincel.</span><span class="sxs-lookup"><span data-stu-id="76cd5-140">In this example, the device context creates a brush.</span></span>


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



<span data-ttu-id="76cd5-141">Un pincel es un objeto que pinta un área, como el trazo de una forma o el relleno de una geometría.</span><span class="sxs-lookup"><span data-stu-id="76cd5-141">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="76cd5-142">El pincel de este ejemplo pinta un área con un color sólido predefinido, negro.</span><span class="sxs-lookup"><span data-stu-id="76cd5-142">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="76cd5-143">Direct2D también proporciona otros tipos de pinceles: pinceles de degradado para pintar degradados lineales y radiales, un [**pincel de mapa de bits**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para pintar con mapas de bits y patrones, y a partir de Windows 8, un pincel de [**imagen**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) para pintar con una imagen representada.</span><span class="sxs-lookup"><span data-stu-id="76cd5-143">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, a [**bitmap brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) for painting with bitmaps and patterns, and starting in Windows 8, an [**image brush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) for painting with a rendered image.</span></span>

<span data-ttu-id="76cd5-144">Algunas API de dibujo proporcionan lápices para dibujar contornos y pinceles para rellenar formas.</span><span class="sxs-lookup"><span data-stu-id="76cd5-144">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="76cd5-145">Direct2D es diferente: no proporciona un objeto Pen, sino que usa un pincel para dibujar contornos y formas de relleno.</span><span class="sxs-lookup"><span data-stu-id="76cd5-145">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="76cd5-146">Al dibujar contornos, utilice la interfaz [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) o a partir de la interfaz [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) de Windows 8 con un pincel para controlar las operaciones de trazado de trazado.</span><span class="sxs-lookup"><span data-stu-id="76cd5-146">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface, or starting in Windows 8 the [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) interface, with a brush to control path stroking operations.</span></span>

<span data-ttu-id="76cd5-147">Un pincel solo se puede usar con el destino de representación que lo creó y con otros destinos de representación en el mismo dominio de recursos.</span><span class="sxs-lookup"><span data-stu-id="76cd5-147">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="76cd5-148">En general, debe crear pinceles una vez y conservarlos durante la vida del destino de representación que los creó.</span><span class="sxs-lookup"><span data-stu-id="76cd5-148">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="76cd5-149">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) es la única excepción; Dado que es relativamente económico crearlo, puede crear un **ID2D1SolidColorBrush** cada vez que dibuje un fotograma, sin que se produzca ningún impacto apreciable en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="76cd5-149">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="76cd5-150">También puede usar una sola **ID2D1SolidColorBrush** y simplemente cambiar su color o opacidad cada vez que la use.</span><span class="sxs-lookup"><span data-stu-id="76cd5-150">You can also use a single **ID2D1SolidColorBrush** and just change its color or opacity every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="76cd5-151">Paso 5: dibujo del rectángulo</span><span class="sxs-lookup"><span data-stu-id="76cd5-151">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="76cd5-152">A continuación, use el contexto de dispositivo para dibujar el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="76cd5-152">Next, use the device context to draw the rectangle.</span></span>


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



<span data-ttu-id="76cd5-153">El método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) toma dos parámetros: el rectángulo que se va a dibujar y el pincel que se va a usar para pintar el contorno del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="76cd5-153">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="76cd5-154">Opcionalmente, también puede especificar las opciones ancho del trazo, patrón de guión, combinación de líneas y límite final.</span><span class="sxs-lookup"><span data-stu-id="76cd5-154">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="76cd5-155">Debe llamar al método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir cualquier comando de dibujo y debe llamar al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) una vez que haya terminado de emitir comandos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="76cd5-155">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="76cd5-156">El método **EndDraw** devuelve un **valor HRESULT** que indica si los comandos de dibujo se realizaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="76cd5-156">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span> <span data-ttu-id="76cd5-157">Si no se realiza correctamente, la función auxiliar ThrowIfFailed producirá una excepción.</span><span class="sxs-lookup"><span data-stu-id="76cd5-157">If it is not successful, the ThrowIfFailed helper function will throw an exception.</span></span>

<span data-ttu-id="76cd5-158">El método [**IDXGISwapChain::P reenviado**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) intercambia la superficie del búfer con la superficie de la pantalla para mostrar el resultado.</span><span class="sxs-lookup"><span data-stu-id="76cd5-158">The [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method swaps the buffer surface with the on screen surface to display the result.</span></span>

## <a name="example-code"></a><span data-ttu-id="76cd5-159">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="76cd5-159">Example code</span></span>

<span data-ttu-id="76cd5-160">En el código de este tema se muestran los elementos básicos de una aplicación de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="76cd5-160">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="76cd5-161">Por motivos de brevedad, el tema omite el marco de trabajo de la aplicación y el código de control de errores que es característico de una aplicación bien escrita.</span><span class="sxs-lookup"><span data-stu-id="76cd5-161">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span>

 

 