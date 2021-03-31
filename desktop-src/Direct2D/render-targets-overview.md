---
title: Información general de destinos de representación
description: Describe los diferentes tipos de destinos de representación de Direct2D y cómo usarlos.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, destinos de representación
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995382"
---
# <a name="render-targets-overview"></a><span data-ttu-id="42b49-104">Información general de destinos de representación</span><span class="sxs-lookup"><span data-stu-id="42b49-104">Render Targets Overview</span></span>

<span data-ttu-id="42b49-105">Un destino de representación es un recurso que hereda de la interfaz [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="42b49-105">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="42b49-106">Un destino de representación crea recursos para dibujar y realiza operaciones de dibujo reales.</span><span class="sxs-lookup"><span data-stu-id="42b49-106">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="42b49-107">En este tema se describen los diferentes tipos de destinos de representación de Direct2D y cómo usarlos.</span><span class="sxs-lookup"><span data-stu-id="42b49-107">This topic describes the different types of Direct2D render targets and how to use them.</span></span>

-   [<span data-ttu-id="42b49-108">Destinos de representación</span><span class="sxs-lookup"><span data-stu-id="42b49-108">Render Targets</span></span>](#render-targets-overview)
    -   [<span data-ttu-id="42b49-109">Características de destino de representación</span><span class="sxs-lookup"><span data-stu-id="42b49-109">Render Target Features</span></span>](#render-target-features)
    -   [<span data-ttu-id="42b49-110">Representar recursos de destino</span><span class="sxs-lookup"><span data-stu-id="42b49-110">Render Target Resources</span></span>](#render-target-resources)
    -   [<span data-ttu-id="42b49-111">Dibujar comandos</span><span class="sxs-lookup"><span data-stu-id="42b49-111">Drawing Commands</span></span>](#drawing-commands)
    -   [<span data-ttu-id="42b49-112">Tratamiento de errores</span><span class="sxs-lookup"><span data-stu-id="42b49-112">Error Handling</span></span>](#error-handling)
-   [<span data-ttu-id="42b49-113">Ejemplo: representación de contenido en una ventana</span><span class="sxs-lookup"><span data-stu-id="42b49-113">Example: Render Content to a Window</span></span>](#example-render-content-to-a-window)

## <a name="render-targets"></a><span data-ttu-id="42b49-114">Destinos de representación</span><span class="sxs-lookup"><span data-stu-id="42b49-114">Render Targets</span></span>

<span data-ttu-id="42b49-115">Un destino de representación es un recurso que hereda de la interfaz [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="42b49-115">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="42b49-116">Un destino de representación crea recursos para dibujar y realiza operaciones de dibujo reales.</span><span class="sxs-lookup"><span data-stu-id="42b49-116">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="42b49-117">Hay varios tipos de destinos de representación que se pueden usar para representar gráficos de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="42b49-117">There are several kinds of render targets that can be used to render graphics in the following ways:</span></span>

-   <span data-ttu-id="42b49-118">Los objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) representan el contenido en una ventana.</span><span class="sxs-lookup"><span data-stu-id="42b49-118">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) objects render content to a window.</span></span>
-   <span data-ttu-id="42b49-119">Los objetos [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) se representan en un contexto de dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="42b49-119">[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) objects render to a GDI device context.</span></span>
-   <span data-ttu-id="42b49-120">Los objetos de destino de representación de mapas de bits representan el contenido en un mapa de bits fuera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="42b49-120">Bitmap render target objects render content to an off-screen bitmap.</span></span>
-   <span data-ttu-id="42b49-121">Los objetos de destino de representación de DXGI se representan en una superficie de DXGI para su uso con Direct3D.</span><span class="sxs-lookup"><span data-stu-id="42b49-121">DXGI render target objects render to a DXGI surface for use with Direct3D.</span></span>

<span data-ttu-id="42b49-122">Dado que un destino de representación está asociado a un dispositivo de representación determinado, es un recurso dependiente del dispositivo y deja de funcionar si se quita el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42b49-122">Because a render target is associated with a particular rendering device, it is a device-dependent resource and ceases to function if the device is removed.</span></span>

### <a name="render-target-features"></a><span data-ttu-id="42b49-123">Características de destino de representación</span><span class="sxs-lookup"><span data-stu-id="42b49-123">Render Target Features</span></span>

<span data-ttu-id="42b49-124">Puede especificar si un destino de representación utiliza la aceleración de hardware y si la pantalla remota se representa en un equipo local o remoto.</span><span class="sxs-lookup"><span data-stu-id="42b49-124">You can specify whether a render target uses hardware acceleration and whether remote display is rendered by a local or a remote computer.</span></span> <span data-ttu-id="42b49-125">Los destinos de representación pueden configurarse para la representación con alias o con suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="42b49-125">Render targets can be set up for aliased or antialiased rendering.</span></span> <span data-ttu-id="42b49-126">En el caso de las escenas de representación con un gran número de primitivas, un desarrollador también puede representar gráficos 2D en modo de alias y usar el suavizado de contorno de muestreo múltiple para lograr una mayor escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="42b49-126">For rendering scenes with a large number of primitives, a developer can also render 2-D graphics in aliased mode and use D3D multisample antialiasing to achieve greater scalability.</span></span>

<span data-ttu-id="42b49-127">Los destinos de representación también pueden agrupar las operaciones de dibujo en capas representadas por la interfaz [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) .</span><span class="sxs-lookup"><span data-stu-id="42b49-127">Render targets can also group drawing operations into layers represented by the [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) interface.</span></span> <span data-ttu-id="42b49-128">Las capas son útiles para recopilar operaciones de dibujo que se van a componer juntas al representar un fotograma.</span><span class="sxs-lookup"><span data-stu-id="42b49-128">Layers are useful for collecting drawing operations to be composited together when rendering a frame.</span></span> <span data-ttu-id="42b49-129">En algunos escenarios, puede ser una alternativa útil a la representación en un destino de representación de mapas de bits y, a continuación, volver a usar el contenido del mapa de bits, ya que los costos de asignación para la disposición en capas son menores que para un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="42b49-129">For some scenarios, this can be a useful alternative to rendering to a bitmap render target, and then reusing the bitmap contents, as allocation costs for layering are lower than for an [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span></span>

<span data-ttu-id="42b49-130">Los destinos de representación pueden crear nuevos destinos de representación que son compatibles con ellos mismos, lo que resulta útil para la representación fuera de pantalla intermedia, a la vez que conserva las distintas propiedades de representación y destino que se establecieron en el original.</span><span class="sxs-lookup"><span data-stu-id="42b49-130">Render targets can create new render targets that are compatible with themselves, which is useful for intermediate off-screen rendering while retaining the various render-target properties that were set on the original.</span></span>

<span data-ttu-id="42b49-131">También es posible representar usando GDI en un destino de representación de Direct2D llamando a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en un destino de representación para [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que tiene los métodos [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) y [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) en él que se pueden usar para recuperar un contexto de dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="42b49-131">It is also possible to render using GDI on a Direct2D render target by calling [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a render target for [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which has [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) and [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) methods on it that can be used to retrieve a GDI device context.</span></span> <span data-ttu-id="42b49-132">La representación a través de GDI solo es posible si el destino de representación se creó con el conjunto de marcadores [**compatible con GDI de uso de destino de representación de D2D1 \_ \_ \_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) .</span><span class="sxs-lookup"><span data-stu-id="42b49-132">Rendering via GDI is possible only if the render target was created with the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag set.</span></span> <span data-ttu-id="42b49-133">Esto resulta útil para las aplicaciones que se representan principalmente con Direct2D pero tienen un modelo de extensibilidad u otro contenido heredado que requiere la capacidad de presentar con GDI.</span><span class="sxs-lookup"><span data-stu-id="42b49-133">This is useful for applications that are primarily rendering with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span> <span data-ttu-id="42b49-134">Para obtener más información, vea [información general sobre la interoperación de Direct2D y GDI](direct2d-and-gdi-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="42b49-134">For more information, see the [Direct2D and GDI Interoperation Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

### <a name="render-target-resources"></a><span data-ttu-id="42b49-135">Representar recursos de destino</span><span class="sxs-lookup"><span data-stu-id="42b49-135">Render Target Resources</span></span>

<span data-ttu-id="42b49-136">Al igual que un generador, un destino de representación puede crear recursos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="42b49-136">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="42b49-137">Los recursos creados por un destino de representación son recursos dependientes del dispositivo (al igual que el destino de representación).</span><span class="sxs-lookup"><span data-stu-id="42b49-137">Any resources created by a render target are device-dependent resources (just like the render target).</span></span> <span data-ttu-id="42b49-138">Un destino de representación puede crear los siguientes tipos de recursos:</span><span class="sxs-lookup"><span data-stu-id="42b49-138">A render target can create the following types of resources:</span></span>

-   <span data-ttu-id="42b49-139">Mapas de bits</span><span class="sxs-lookup"><span data-stu-id="42b49-139">Bitmaps</span></span>
-   <span data-ttu-id="42b49-140">Pinceles</span><span class="sxs-lookup"><span data-stu-id="42b49-140">Brushes</span></span>
-   <span data-ttu-id="42b49-141">Capas</span><span class="sxs-lookup"><span data-stu-id="42b49-141">Layers</span></span>
-   <span data-ttu-id="42b49-142">Mallas</span><span class="sxs-lookup"><span data-stu-id="42b49-142">Meshes</span></span>

### <a name="drawing-commands"></a><span data-ttu-id="42b49-143">Dibujar comandos</span><span class="sxs-lookup"><span data-stu-id="42b49-143">Drawing Commands</span></span>

<span data-ttu-id="42b49-144">Para representar el contenido, se usan los métodos de dibujo del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="42b49-144">To render content, you use the render target drawing methods.</span></span> <span data-ttu-id="42b49-145">Antes de empezar a dibujar, se llama al método [**ID2D1RenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) .</span><span class="sxs-lookup"><span data-stu-id="42b49-145">Before you begin drawing, you call the [**ID2D1RenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method.</span></span> <span data-ttu-id="42b49-146">Una vez finalizado el dibujo, se llama al método [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="42b49-146">After you finished drawing, you call the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="42b49-147">Entre estas llamadas, se usan métodos Draw y Fill para representar recursos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="42b49-147">Between these calls, you use Draw and Fill methods to render drawing resources.</span></span> <span data-ttu-id="42b49-148">La mayoría de los métodos Draw y Fill toman una forma (una primitiva o una geometría) y un pincel para rellenar o esquematizar la forma.</span><span class="sxs-lookup"><span data-stu-id="42b49-148">Most Draw and Fill methods take a shape (either a primitive or a geometry) and a brush for filling or outlining the shape.</span></span>

<span data-ttu-id="42b49-149">Los destinos de representación proporcionan métodos para recortar, aplicar máscaras de opacidad y transformar el espacio de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="42b49-149">Render targets provide methods for clipping, applying opacity masks, and transforming the coordinate space.</span></span>

<span data-ttu-id="42b49-150">Direct2D usa un sistema de coordenadas de la mano izquierda: los valores positivos del eje x pasan a los valores correctos y positivos del eje y continúan hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="42b49-150">Direct2D uses a left-handed coordinate system: positive x-axis values proceed to the right and positive y-axis values proceed downward.</span></span>

### <a name="error-handling"></a><span data-ttu-id="42b49-151">Tratamiento de errores</span><span class="sxs-lookup"><span data-stu-id="42b49-151">Error Handling</span></span>

<span data-ttu-id="42b49-152">Los comandos de dibujo de destino de representación no indican si la operación solicitada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="42b49-152">Render target drawing commands do not indicate whether the requested operation was successful.</span></span> <span data-ttu-id="42b49-153">Para averiguar si hay errores de dibujo, llame al método [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) del destino de representación o al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) para obtener un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="42b49-153">To find out whether there are drawing errors, call the render target [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) method or [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method to obtain an **HRESULT**.</span></span>

## <a name="example-render-content-to-a-window"></a><span data-ttu-id="42b49-154">Ejemplo: representación de contenido en una ventana</span><span class="sxs-lookup"><span data-stu-id="42b49-154">Example: Render Content to a Window</span></span>

<span data-ttu-id="42b49-155">En el ejemplo siguiente se usa el método [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) para crear un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span><span class="sxs-lookup"><span data-stu-id="42b49-155">The following example uses the [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) method to create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



<span data-ttu-id="42b49-156">En el ejemplo siguiente se usa [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) para dibujar texto en la ventana.</span><span class="sxs-lookup"><span data-stu-id="42b49-156">The next example uses the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) to draw text to the window.</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



<span data-ttu-id="42b49-157">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="42b49-157">Code has been omitted from this example.</span></span>

 

 