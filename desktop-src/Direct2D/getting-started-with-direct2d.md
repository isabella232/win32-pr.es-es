---
title: Inicio rápido de Direct2D
description: Resume los pasos necesarios para dibujar con Direct2D y proporciona código de ejemplo.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Ejemplo de código de rectángulo de Direct2D, dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa59d7da057a7a9922e270d83937307762b06a40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149300"
---
# <a name="direct2d-quickstart"></a><span data-ttu-id="1f627-104">Inicio rápido de Direct2D</span><span class="sxs-lookup"><span data-stu-id="1f627-104">Direct2D QuickStart</span></span>

<span data-ttu-id="1f627-105">Direct2D es una API de modo inmediato y de código nativo para crear gráficos 2D.</span><span class="sxs-lookup"><span data-stu-id="1f627-105">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="1f627-106">En este tema se muestra cómo usar Direct2D en una aplicación Win32 típica para dibujar en un **hWnd**.</span><span class="sxs-lookup"><span data-stu-id="1f627-106">This topic illustrates how to use Direct2D within a typical Win32 application to draw to an **HWND**.</span></span>

> [!Note]  
> <span data-ttu-id="1f627-107">Si quiere crear una aplicación de la tienda Windows que use Direct2D, vea el tema [de inicio rápido de direct2d para Windows 8](direct2d-quickstart-with-device-context.md) .</span><span class="sxs-lookup"><span data-stu-id="1f627-107">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="1f627-108">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="1f627-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="1f627-109">Dibujar un rectángulo simple</span><span class="sxs-lookup"><span data-stu-id="1f627-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="1f627-110">Paso 1: incluir el encabezado de Direct2D</span><span class="sxs-lookup"><span data-stu-id="1f627-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="1f627-111">Paso 2: creación de un ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="1f627-111">Step 2: Create an ID2D1Factory</span></span>](#step-2-create-an-id2d1factory)
-   [<span data-ttu-id="1f627-112">Paso 3: creación de un ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="1f627-112">Step 3: Create an ID2D1HwndRenderTarget</span></span>](#step-3-create-an-id2d1hwndrendertarget)
-   [<span data-ttu-id="1f627-113">Paso 4: crear un pincel</span><span class="sxs-lookup"><span data-stu-id="1f627-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="1f627-114">Paso 5: dibujo del rectángulo</span><span class="sxs-lookup"><span data-stu-id="1f627-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="1f627-115">Paso 6: liberar recursos</span><span class="sxs-lookup"><span data-stu-id="1f627-115">Step 6: Release Resources</span></span>](#step-6-release-resources)
-   [<span data-ttu-id="1f627-116">Creación de una aplicación de Direct2D sencilla</span><span class="sxs-lookup"><span data-stu-id="1f627-116">Create a Simple Direct2D Application</span></span>](#create-a-simple-direct2d-application)
-   [<span data-ttu-id="1f627-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f627-117">Related topics</span></span>](#related-topics)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="1f627-118">Dibujar un rectángulo simple</span><span class="sxs-lookup"><span data-stu-id="1f627-118">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="1f627-119">Para dibujar un rectángulo mediante [GDI](/windows/desktop/gdi/windows-gdi), podría controlar el mensaje [**de \_ dibujo de WM**](/windows/desktop/gdi/wm-paint) , tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="1f627-119">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


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



<span data-ttu-id="1f627-120">El código para dibujar el mismo rectángulo con Direct2D es similar: crea recursos de dibujo, describe una forma para dibujar, dibuja la forma y, a continuación, libera los recursos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1f627-120">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="1f627-121">En las secciones siguientes se describe detalladamente cada uno de estos pasos.</span><span class="sxs-lookup"><span data-stu-id="1f627-121">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="1f627-122">Paso 1: incluir el encabezado de Direct2D</span><span class="sxs-lookup"><span data-stu-id="1f627-122">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="1f627-123">Además de los encabezados necesarios para una aplicación Win32, incluya el encabezado d2d1. h.</span><span class="sxs-lookup"><span data-stu-id="1f627-123">In addition to the headers required for a Win32 application, include the d2d1.h header.</span></span>

## <a name="step-2-create-an-id2d1factory"></a><span data-ttu-id="1f627-124">Paso 2: creación de un ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="1f627-124">Step 2: Create an ID2D1Factory</span></span>

<span data-ttu-id="1f627-125">Una de las primeras cosas que hace cualquier ejemplo de Direct2D es crear un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="1f627-125">One of the first things that any Direct2D example does is create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



<span data-ttu-id="1f627-126">La interfaz [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) es el punto de partida para usar Direct2D; Use un **ID2D1Factory** para crear recursos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1f627-126">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface is the starting point for using Direct2D; use an **ID2D1Factory** to create Direct2D resources.</span></span>

<span data-ttu-id="1f627-127">Al crear una factoría, puede especificar si es multiproceso o de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="1f627-127">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="1f627-128">(Para obtener más información sobre los generadores multiproceso, consulte la sección Comentarios en la [**Página de referencia de ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)). En este ejemplo se crea un generador de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="1f627-128">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="1f627-129">En general, la aplicación debe crear el generador una vez y conservarlo durante la vida de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1f627-129">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1hwndrendertarget"></a><span data-ttu-id="1f627-130">Paso 3: creación de un ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="1f627-130">Step 3: Create an ID2D1HwndRenderTarget</span></span>

<span data-ttu-id="1f627-131">Después de crear un generador, úselo para crear un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="1f627-131">After you create a factory, use it to create a render target.</span></span>


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



<span data-ttu-id="1f627-132">Un destino de representación es un dispositivo que puede realizar operaciones de dibujo y crear recursos de dibujo dependientes del dispositivo, como pinceles.</span><span class="sxs-lookup"><span data-stu-id="1f627-132">A render target is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="1f627-133">Los distintos tipos de destinos de representación se representan en distintos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1f627-133">Different types of render targets render to different devices.</span></span> <span data-ttu-id="1f627-134">En el ejemplo anterior se usa un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), que se representa en una parte de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1f627-134">The preceding example uses an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), which renders to a portion of the screen.</span></span>

<span data-ttu-id="1f627-135">Cuando es posible, un destino de representación usa la GPU para acelerar las operaciones de representación y crear recursos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1f627-135">When possible, a render target uses the GPU to accelerate rendering operations and create drawing resources.</span></span> <span data-ttu-id="1f627-136">De lo contrario, el destino de representación utiliza la CPU para procesar las instrucciones de representación y crear recursos.</span><span class="sxs-lookup"><span data-stu-id="1f627-136">Otherwise, the render target uses the CPU to process rendering instructions and create resources.</span></span> <span data-ttu-id="1f627-137">(Puede modificar este comportamiento mediante las marcas de [**\_ tipo de \_ destino \_ de representación de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) al crear el destino de representación).</span><span class="sxs-lookup"><span data-stu-id="1f627-137">(You can modify this behavior by using the [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) flags when you create the render target.)</span></span>

<span data-ttu-id="1f627-138">El método [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) toma tres parámetros.</span><span class="sxs-lookup"><span data-stu-id="1f627-138">The [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method takes three parameters.</span></span> <span data-ttu-id="1f627-139">El primer parámetro, un struct de propiedades de destino de representación de D2D1, especifica las opciones de pantalla remotas, si se debe forzar el destino de representación para que se represente en el software o hardware, y en el PPP. [**\_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)</span><span class="sxs-lookup"><span data-stu-id="1f627-139">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) struct, specifies remote display options, whether to force the render target to render to software or hardware, and the DPI.</span></span> <span data-ttu-id="1f627-140">El código de este ejemplo usa la función auxiliar [**D2D1:: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) para aceptar las propiedades de destino de representación predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="1f627-140">The code in this example uses the [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) helper function to accept default render target properties.</span></span>

<span data-ttu-id="1f627-141">El segundo parámetro, un struct de [**propiedades de destino de representación de D2D1 \_ hWnd \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) , especifica el **hWnd** en el que se representa el contenido, el tamaño inicial del destino de representación (en píxeles) y sus [**Opciones de presentación**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span><span class="sxs-lookup"><span data-stu-id="1f627-141">The second parameter, a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) struct, specifies the **HWND** to which content is rendered, the initial size of the render target (in pixels), and its [**presentation options**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span></span> <span data-ttu-id="1f627-142">En este ejemplo se usa la función auxiliar [**D2D1:: HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) para especificar un HWND y el tamaño inicial.</span><span class="sxs-lookup"><span data-stu-id="1f627-142">This example uses the [**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) helper function to specify an HWND and initial size.</span></span> <span data-ttu-id="1f627-143">Usa las opciones de presentación predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="1f627-143">It uses default presentation options.</span></span>

<span data-ttu-id="1f627-144">El tercer parámetro es la dirección del puntero que recibe la referencia de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="1f627-144">The third parameter is the address of the pointer that receives the render target reference.</span></span>

<span data-ttu-id="1f627-145">Cuando se crea un destino de representación y la aceleración de hardware está disponible, se asignan recursos en la GPU del equipo.</span><span class="sxs-lookup"><span data-stu-id="1f627-145">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="1f627-146">Al crear un destino de representación una vez y conservarlo lo máximo posible, se obtienen ventajas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1f627-146">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="1f627-147">La aplicación debe crear los destinos de representación una vez y conservarlos durante la vida de la aplicación o hasta que se reciba el error de [**\_ \_ destino de recreación de D2DERR**](direct2d-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1f627-147">Your application should create render targets once and hold on to them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="1f627-148">Cuando reciba este error, deberá volver a crear el destino de representación (y los recursos que haya creado).</span><span class="sxs-lookup"><span data-stu-id="1f627-148">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="step-4-create-a-brush"></a><span data-ttu-id="1f627-149">Paso 4: crear un pincel</span><span class="sxs-lookup"><span data-stu-id="1f627-149">Step 4: Create a Brush</span></span>

<span data-ttu-id="1f627-150">Al igual que un generador, un destino de representación puede crear recursos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1f627-150">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="1f627-151">En este ejemplo, el destino de representación crea un pincel.</span><span class="sxs-lookup"><span data-stu-id="1f627-151">In this example, the render target creates a brush.</span></span>


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



<span data-ttu-id="1f627-152">Un pincel es un objeto que pinta un área, como el trazo de una forma o el relleno de una geometría.</span><span class="sxs-lookup"><span data-stu-id="1f627-152">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="1f627-153">El pincel de este ejemplo pinta un área con un color sólido predefinido, negro.</span><span class="sxs-lookup"><span data-stu-id="1f627-153">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="1f627-154">Direct2D también proporciona otros tipos de pinceles: pinceles de degradado para pintar degradados lineales y radiales, y un pincel de mapa de bits para dibujar con mapas de bits y patrones.</span><span class="sxs-lookup"><span data-stu-id="1f627-154">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, and a bitmap brush for painting with bitmaps and patterns.</span></span>

<span data-ttu-id="1f627-155">Algunas API de dibujo proporcionan lápices para dibujar contornos y pinceles para rellenar formas.</span><span class="sxs-lookup"><span data-stu-id="1f627-155">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="1f627-156">Direct2D es diferente: no proporciona un objeto Pen, sino que usa un pincel para dibujar contornos y formas de relleno.</span><span class="sxs-lookup"><span data-stu-id="1f627-156">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="1f627-157">Al dibujar contornos, utilice la interfaz [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) con un pincel para controlar las operaciones de trazado de trazados.</span><span class="sxs-lookup"><span data-stu-id="1f627-157">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface with a brush to control path stroking operations.</span></span>

<span data-ttu-id="1f627-158">Un pincel solo se puede usar con el destino de representación que lo creó y con otros destinos de representación en el mismo dominio de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f627-158">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="1f627-159">En general, debe crear pinceles una vez y conservarlos durante la vida del destino de representación que los creó.</span><span class="sxs-lookup"><span data-stu-id="1f627-159">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="1f627-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) es la única excepción; Dado que es relativamente económico crearlo, puede crear un **ID2D1SolidColorBrush** cada vez que dibuje un fotograma, sin que se produzca ningún impacto apreciable en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1f627-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="1f627-161">También puede usar un solo **ID2D1SolidColorBrush** y cambiar su color cada vez que lo use.</span><span class="sxs-lookup"><span data-stu-id="1f627-161">You can also use a single **ID2D1SolidColorBrush** and just change its color every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="1f627-162">Paso 5: dibujo del rectángulo</span><span class="sxs-lookup"><span data-stu-id="1f627-162">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="1f627-163">A continuación, use el destino de representación para dibujar el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="1f627-163">Next, use the render target to draw the rectangle.</span></span>


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



<span data-ttu-id="1f627-164">El método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) toma dos parámetros: el rectángulo que se va a dibujar y el pincel que se va a usar para pintar el contorno del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="1f627-164">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="1f627-165">Opcionalmente, también puede especificar las opciones ancho del trazo, patrón de guión, combinación de líneas y límite final.</span><span class="sxs-lookup"><span data-stu-id="1f627-165">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="1f627-166">Debe llamar al método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir cualquier comando de dibujo y debe llamar al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) una vez que haya terminado de emitir comandos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1f627-166">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="1f627-167">El método **EndDraw** devuelve un **valor HRESULT** que indica si los comandos de dibujo se realizaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="1f627-167">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span>

## <a name="step-6-release-resources"></a><span data-ttu-id="1f627-168">Paso 6: liberar recursos</span><span class="sxs-lookup"><span data-stu-id="1f627-168">Step 6: Release Resources</span></span>

<span data-ttu-id="1f627-169">Cuando no haya más fotogramas para dibujar, o cuando reciba el error de [**\_ \_ destino de recreación de D2DERR**](direct2d-error-codes.md) , libere el destino de representación y los dispositivos que creó.</span><span class="sxs-lookup"><span data-stu-id="1f627-169">When there are no more frames to draw, or when you receive the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error, release the render target and any devices it created.</span></span>


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



<span data-ttu-id="1f627-170">Cuando la aplicación haya terminado de usar recursos de Direct2D (como cuando esté a punto de salir), libere el generador de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1f627-170">When your application has finished using Direct2D resources (such as when it is about to exit), release the Direct2D factory.</span></span>


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a><span data-ttu-id="1f627-171">Creación de una aplicación de Direct2D sencilla</span><span class="sxs-lookup"><span data-stu-id="1f627-171">Create a Simple Direct2D Application</span></span>

<span data-ttu-id="1f627-172">En el código de este tema se muestran los elementos básicos de una aplicación de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1f627-172">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="1f627-173">Por motivos de brevedad, el tema omite el marco de trabajo de la aplicación y el código de control de errores que es característico de una aplicación bien escrita.</span><span class="sxs-lookup"><span data-stu-id="1f627-173">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span> <span data-ttu-id="1f627-174">Para ver un tutorial más detallado en el que se muestra el código completo para crear una aplicación de Direct2D simple y se muestran las prácticas de diseño más adecuadas, consulte [creación de una aplicación de Direct2d simple](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="1f627-174">For a more detailed walk-through that shows the complete code for creating a simple Direct2D application and demonstrates best design practices, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f627-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f627-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f627-176">Crear una aplicación de Direct2D simple</span><span class="sxs-lookup"><span data-stu-id="1f627-176">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

 

 