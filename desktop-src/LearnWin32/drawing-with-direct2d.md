---
title: Dibujo con Direct2D
description: Después de crear los recursos de gráficos, está listo para dibujar.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f8f3cf82d3ce6f485a7c54700c32c9eb65d054
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487611"
---
# <a name="drawing-with-direct2d"></a><span data-ttu-id="48355-103">Dibujo con Direct2D</span><span class="sxs-lookup"><span data-stu-id="48355-103">Drawing with Direct2D</span></span>

<span data-ttu-id="48355-104">Después de crear los recursos de gráficos, está listo para dibujar.</span><span class="sxs-lookup"><span data-stu-id="48355-104">After you create your graphics resources, you are ready to draw.</span></span>

## <a name="drawing-an-ellipse"></a><span data-ttu-id="48355-105">Dibujar una elipse</span><span class="sxs-lookup"><span data-stu-id="48355-105">Drawing an Ellipse</span></span>

<span data-ttu-id="48355-106">El programa de [círculo](your-first-direct2d-program.md) realiza una lógica de dibujo muy sencilla:</span><span class="sxs-lookup"><span data-stu-id="48355-106">The [Circle](your-first-direct2d-program.md) program performs very simple drawing logic:</span></span>

1.  <span data-ttu-id="48355-107">Rellene el fondo con un color sólido.</span><span class="sxs-lookup"><span data-stu-id="48355-107">Fill the background with a solid color.</span></span>
2.  <span data-ttu-id="48355-108">Dibuja un círculo relleno.</span><span class="sxs-lookup"><span data-stu-id="48355-108">Draw a filled circle.</span></span>

![captura de pantalla del programa de círculo.](images/graphics08.png)

<span data-ttu-id="48355-110">Dado que el destino de representación es una ventana (en lugar de un mapa de bits u otra superficie fuera de la pantalla), el dibujo se realiza en respuesta a los mensajes de [**\_ pintura de WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="48355-110">Because the render target is a window (as opposed to a bitmap or other offscreen surface), drawing is done in response to [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) messages.</span></span> <span data-ttu-id="48355-111">En el código siguiente se muestra el procedimiento de ventana para el programa de círculo.</span><span class="sxs-lookup"><span data-stu-id="48355-111">The following code shows the window procedure for the Circle program.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_PAINT:
            OnPaint();
            return 0;

         // Other messages not shown...
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```

<span data-ttu-id="48355-112">Este es el código que dibuja el círculo.</span><span class="sxs-lookup"><span data-stu-id="48355-112">Here is the code that draws the circle.</span></span>

```C++
void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="48355-113">La interfaz [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) se usa para todas las operaciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="48355-113">The [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface is used for all drawing operations.</span></span> <span data-ttu-id="48355-114">El método del programa `OnPaint` hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="48355-114">The program's `OnPaint` method does the following:</span></span>

1.  <span data-ttu-id="48355-115">El método [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) señala el inicio del dibujo.</span><span class="sxs-lookup"><span data-stu-id="48355-115">The [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method signals the start of drawing.</span></span>
2.  <span data-ttu-id="48355-116">El método [**ID2D1RenderTarget:: Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) llena todo el destino de representación con un color sólido.</span><span class="sxs-lookup"><span data-stu-id="48355-116">The [**ID2D1RenderTarget::Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) method fills the entire render target with a solid color.</span></span> <span data-ttu-id="48355-117">El color se proporciona como una [**estructura \_ \_ F de color D2D1**](/windows/desktop/Direct2D/d2d1-color-f) .</span><span class="sxs-lookup"><span data-stu-id="48355-117">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) structure.</span></span> <span data-ttu-id="48355-118">Puede usar la clase [**D2D1:: ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) para inicializar la estructura.</span><span class="sxs-lookup"><span data-stu-id="48355-118">You can use the [**D2D1::ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) class to initialize the structure.</span></span> <span data-ttu-id="48355-119">Para obtener más información, vea [usar el color en Direct2D](using-color-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="48355-119">For more information, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>
3.  <span data-ttu-id="48355-120">El método [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) dibuja una elipse rellena, utilizando el pincel especificado para el relleno.</span><span class="sxs-lookup"><span data-stu-id="48355-120">The [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws a filled ellipse, using the specified brush for the fill.</span></span> <span data-ttu-id="48355-121">Una elipse se especifica mediante un punto central y los radios x e y.</span><span class="sxs-lookup"><span data-stu-id="48355-121">An ellipse is specified by a center point and the x- and y-radii.</span></span> <span data-ttu-id="48355-122">Si los radios x e y son iguales, el resultado es un círculo.</span><span class="sxs-lookup"><span data-stu-id="48355-122">If the x- and y-radii are the same, the result is a circle.</span></span>
4.  <span data-ttu-id="48355-123">El método [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) indica la finalización del dibujo para este marco.</span><span class="sxs-lookup"><span data-stu-id="48355-123">The [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method signals the completion of drawing for this frame.</span></span> <span data-ttu-id="48355-124">Todas las operaciones de dibujo se deben colocar entre las llamadas a [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) y **EndDraw**.</span><span class="sxs-lookup"><span data-stu-id="48355-124">All drawing operations must be placed between calls to [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw**.</span></span>

<span data-ttu-id="48355-125">Todos los métodos [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)y [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) tienen un tipo de valor devuelto **void** .</span><span class="sxs-lookup"><span data-stu-id="48355-125">The [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear), and [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) methods all have a **void** return type.</span></span> <span data-ttu-id="48355-126">Si se produce un error durante la ejecución de cualquiera de estos métodos, el error se señaliza a través del valor devuelto del método [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="48355-126">If an error occurs during the execution of any of these methods, the error is signaled through the return value of the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="48355-127">El `CreateGraphicsResources` método se muestra en el tema [crear recursos de Direct2D](render-targets--devices--and-resources.md).</span><span class="sxs-lookup"><span data-stu-id="48355-127">The `CreateGraphicsResources` method is shown in the topic [Creating Direct2D Resources](render-targets--devices--and-resources.md).</span></span> <span data-ttu-id="48355-128">Este método crea el destino de representación y el pincel de color sólido.</span><span class="sxs-lookup"><span data-stu-id="48355-128">This method creates the render target and the solid-color brush.</span></span>

<span data-ttu-id="48355-129">El dispositivo puede almacenar en búfer los comandos de dibujo y aplazar su ejecución hasta que se llame a [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="48355-129">The device might buffer the drawing commands and defer executing them until [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) is called.</span></span> <span data-ttu-id="48355-130">Puede forzar que el dispositivo ejecute cualquier comando de dibujo pendiente mediante una llamada a [**ID2D1RenderTarget:: Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span><span class="sxs-lookup"><span data-stu-id="48355-130">You can force the device to execute any pending drawing commands by calling [**ID2D1RenderTarget::Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span> <span data-ttu-id="48355-131">Sin embargo, el vaciado puede reducir el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="48355-131">Flushing can reduce performance, however.</span></span>

## <a name="handling-device-loss"></a><span data-ttu-id="48355-132">Controlar la pérdida del dispositivo</span><span class="sxs-lookup"><span data-stu-id="48355-132">Handling Device Loss</span></span>

<span data-ttu-id="48355-133">Mientras se ejecuta el programa, es posible que el dispositivo gráfico que está usando no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="48355-133">While your program is running, the graphics device that you are using might become unavailable.</span></span> <span data-ttu-id="48355-134">Por ejemplo, se puede perder el dispositivo si cambia la resolución de pantalla, o si el usuario quita el adaptador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="48355-134">For example, the device can be lost if the display resolution changes, or if the user removes the display adapter.</span></span> <span data-ttu-id="48355-135">Si se pierde el dispositivo, el destino de representación también deja de ser válido, junto con los recursos dependientes del dispositivo asociados al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48355-135">If the device is lost, the render target also becomes invalid, along with any device-dependent resources that were associated with the device.</span></span> <span data-ttu-id="48355-136">Direct2D señala un dispositivo perdido al devolver el código de error D2DERR volver a **crear el \_ \_ destino** desde el método [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="48355-136">Direct2D signals a lost device by returning the error code **D2DERR\_RECREATE\_TARGET** from the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="48355-137">Si recibe este código de error, debe volver a crear el destino de representación y todos los recursos dependientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48355-137">If you receive this error code, you must re-create the render target and all device-dependent resources.</span></span>

<span data-ttu-id="48355-138">Para descartar un recurso, simplemente libere la interfaz para ese recurso.</span><span class="sxs-lookup"><span data-stu-id="48355-138">To discard a resource, simply release the interface for that resource.</span></span>


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



<span data-ttu-id="48355-139">La creación de un recurso puede ser una operación costosa, por lo que no se deben volver a crear los recursos de cada mensaje de [**\_ pintura de WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="48355-139">Creating a resource can be an expensive operation, so do not recreate your resources for every [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="48355-140">Cree un recurso una vez y almacene en caché el puntero de recursos hasta que el recurso deje de ser válido debido a la pérdida del dispositivo o hasta que ya no necesite ese recurso.</span><span class="sxs-lookup"><span data-stu-id="48355-140">Create a resource once, and cache the resource pointer until the resource becomes invalid due to device loss, or until you no longer need that resource.</span></span>

## <a name="the-direct2d-render-loop"></a><span data-ttu-id="48355-141">El bucle de representación de Direct2D</span><span class="sxs-lookup"><span data-stu-id="48355-141">The Direct2D Render Loop</span></span>

<span data-ttu-id="48355-142">Independientemente de lo que dibuje, el programa debe realizar un bucle similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="48355-142">Regardless of what you draw, your program should perform a loop similar to following.</span></span>

1.  <span data-ttu-id="48355-143">Cree recursos independientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48355-143">Create device-independent resources.</span></span>
2.  <span data-ttu-id="48355-144">Representar la escena.</span><span class="sxs-lookup"><span data-stu-id="48355-144">Render the scene.</span></span>
    1.  <span data-ttu-id="48355-145">Compruebe si existe un destino de representación válido.</span><span class="sxs-lookup"><span data-stu-id="48355-145">Check if a valid render target exists.</span></span> <span data-ttu-id="48355-146">Si no es así, cree el destino de representación y los recursos dependientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48355-146">If not, create the render target and the device-dependent resources.</span></span>
    2.  <span data-ttu-id="48355-147">Llame a [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span><span class="sxs-lookup"><span data-stu-id="48355-147">Call [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span></span>
    3.  <span data-ttu-id="48355-148">Emitir comandos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="48355-148">Issue drawing commands.</span></span>
    4.  <span data-ttu-id="48355-149">Llame a [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="48355-149">Call [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>
    5.  <span data-ttu-id="48355-150">Si [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) devuelve **D2DERR \_ Recreate \_**, descarte el destino de representación y los recursos dependientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48355-150">If [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) returns **D2DERR\_RECREATE\_TARGET**, discard the render target and device-dependent resources.</span></span>
3.  <span data-ttu-id="48355-151">Repita el paso 2 cada vez que necesite actualizar o volver a dibujar la escena.</span><span class="sxs-lookup"><span data-stu-id="48355-151">Repeat step 2 whenever you need to update or redraw the scene.</span></span>

<span data-ttu-id="48355-152">Si el destino de representación es una ventana, el paso 2 se produce siempre que la ventana recibe un mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="48355-152">If the render target is a window, step 2 occurs whenever the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="48355-153">El bucle que se muestra aquí controla la pérdida del dispositivo al descartar los recursos dependientes del dispositivo y volver a crearlos al principio del siguiente bucle (paso 2a).</span><span class="sxs-lookup"><span data-stu-id="48355-153">The loop shown here handles device loss by discarding the device-dependent resources and re-creating them at the start of the next loop (step 2a).</span></span>

## <a name="next"></a><span data-ttu-id="48355-154">Siguientes</span><span class="sxs-lookup"><span data-stu-id="48355-154">Next</span></span>

[<span data-ttu-id="48355-155">PPP y Device-Independent píxeles</span><span class="sxs-lookup"><span data-stu-id="48355-155">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)

 

 