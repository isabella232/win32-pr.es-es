---
title: Movimiento del mouse
description: Movimiento del mouse
ms.assetid: 54366E9B-470A-4155-8A5F-425BAC8AC1A5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14176310882651cdeb2939d0db55368ff133ea11
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "105689604"
---
# <a name="mouse-movement"></a><span data-ttu-id="f6bb5-103">Movimiento del mouse</span><span class="sxs-lookup"><span data-stu-id="f6bb5-103">Mouse Movement</span></span>

<span data-ttu-id="f6bb5-104">Cuando se mueve el mouse, Windows envía un mensaje de [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="f6bb5-104">When the mouse moves, Windows posts a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="f6bb5-105">De forma predeterminada, el **\_ MOUSEMOVE de WM** va a la ventana que contiene el cursor.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-105">By default, **WM\_MOUSEMOVE** goes to the window that contains the cursor.</span></span> <span data-ttu-id="f6bb5-106">Puede invalidar este comportamiento mediante la *captura* del mouse, que se describe en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-106">You can override this behavior by *capturing* the mouse, which is described in the next section.</span></span>

<span data-ttu-id="f6bb5-107">El mensaje de [**\_ MOUSEMOVE de WM**](/windows/desktop/inputdev/wm-mousemove) contiene los mismos parámetros que los mensajes de clics del mouse.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-107">The [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message contains the same parameters as the messages for mouse clicks.</span></span> <span data-ttu-id="f6bb5-108">Los 16 bits más bajos de *lParam* contienen la coordenada x y los 16 bits siguientes contienen la coordenada y.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-108">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="f6bb5-109">Use las macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) y [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para desempaquetar las coordenadas de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-109">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span> <span data-ttu-id="f6bb5-110">El parámetro *wParam* contiene **una operación OR bit a bit** de marcas, que indica el estado de los demás botones del mouse más las teclas Mayús y Ctrl.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-110">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span> <span data-ttu-id="f6bb5-111">En el código siguiente se obtienen las coordenadas del mouse desde *lParam*.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-111">The following code gets the mouse coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="f6bb5-112">Recuerde que estas coordenadas están en píxeles, no en píxeles independientes del dispositivo (DIP).</span><span class="sxs-lookup"><span data-stu-id="f6bb5-112">Remember that these coordinates are in pixels, not device-independent pixels (DIPs).</span></span> <span data-ttu-id="f6bb5-113">Más adelante en este tema, veremos el código que convierte entre las dos unidades.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-113">Later in this topic, we will look at code that converts between the two units.</span></span>

<span data-ttu-id="f6bb5-114">Una ventana también puede recibir un mensaje de Windows de [**WM \_**](/windows/desktop/inputdev/wm-mousemove) si la posición del cursor cambia en relación con la ventana.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-114">A window can also receive a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message if the position of the cursor changes relative to the window.</span></span> <span data-ttu-id="f6bb5-115">Por ejemplo, si el cursor se coloca sobre una ventana y el usuario oculta la ventana, la ventana recibe mensajes de **WM \_ MOUSEMOVE** incluso si el mouse no se mueve.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-115">For example, if the cursor is positioned over a window, and the user hides the window, the window receives **WM\_MOUSEMOVE** messages even if the mouse did not move.</span></span> <span data-ttu-id="f6bb5-116">Una consecuencia de este comportamiento es que las coordenadas del mouse podrían no cambiar entre mensajes de **WM \_ MOUSEMOVE** .</span><span class="sxs-lookup"><span data-stu-id="f6bb5-116">One consequence of this behavior is that the mouse coordinates might not change between **WM\_MOUSEMOVE** messages.</span></span>

## <a name="capturing-mouse-movement-outside-the-window"></a><span data-ttu-id="f6bb5-117">Capturar el movimiento del mouse fuera de la ventana</span><span class="sxs-lookup"><span data-stu-id="f6bb5-117">Capturing Mouse Movement Outside the Window</span></span>

<span data-ttu-id="f6bb5-118">De forma predeterminada, una ventana deja de recibir mensajes de [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) si el mouse se desplaza más allá del borde del área cliente.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-118">By default, a window stops receiving [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages if the mouse moves past the edge of the client area.</span></span> <span data-ttu-id="f6bb5-119">Pero para algunas operaciones, es posible que tenga que realizar un seguimiento de la posición del mouse más allá de este punto.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-119">But for some operations, you might need to track the mouse position beyond this point.</span></span> <span data-ttu-id="f6bb5-120">Por ejemplo, un programa de dibujo podría permitir al usuario arrastrar el rectángulo de selección más allá del borde de la ventana, tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-120">For example, a drawing program might enable the user to drag the selection rectangle beyond the edge of the window, as shown in the following diagram.</span></span>

![Ilustración de la captura del mouse.](images/input01.png)

<span data-ttu-id="f6bb5-122">Para recibir mensajes de movimiento del mouse más allá del borde de la ventana, llame a la función [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) .</span><span class="sxs-lookup"><span data-stu-id="f6bb5-122">To receive mouse-move messages past the edge of the window, call the [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) function.</span></span> <span data-ttu-id="f6bb5-123">Después de llamar a esta función, la ventana seguirá recibiendo mensajes de [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) mientras el usuario mantenga al menos un botón del mouse hacia abajo, incluso si el mouse se mueve fuera de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-123">After this function is called, the window will continue to receive [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages for as long as the user holds at least one mouse button down, even if the mouse moves outside the window.</span></span> <span data-ttu-id="f6bb5-124">La ventana de captura debe ser la ventana de primer plano y solo una ventana puede ser la ventana de captura a la vez.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-124">The capture window must be the foreground window, and only one window can be the capture window at a time.</span></span> <span data-ttu-id="f6bb5-125">Para liberar la captura del mouse, llame a la función [**releaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) .</span><span class="sxs-lookup"><span data-stu-id="f6bb5-125">To release mouse capture, call the [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) function.</span></span>

<span data-ttu-id="f6bb5-126">Normalmente usaría [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) y [**releaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-126">You would typically use [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) and [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) in the following way.</span></span>

1.  <span data-ttu-id="f6bb5-127">Cuando el usuario presione el botón primario del mouse, llame a [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) para iniciar la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-127">When the user presses the left mouse button, call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to start capturing the mouse.</span></span>
2.  <span data-ttu-id="f6bb5-128">Responder a los mensajes de movimiento del mouse.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-128">Respond to mouse-move messages.</span></span>
3.  <span data-ttu-id="f6bb5-129">Cuando el usuario suelte el botón primario del mouse, llame a [**releaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).</span><span class="sxs-lookup"><span data-stu-id="f6bb5-129">When the user releases the left mouse button, call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).</span></span>

## <a name="example-drawing-circles"></a><span data-ttu-id="f6bb5-130">Ejemplo: dibujo de círculos</span><span class="sxs-lookup"><span data-stu-id="f6bb5-130">Example: Drawing Circles</span></span>

<span data-ttu-id="f6bb5-131">Vamos a ampliar el programa de círculo del [módulo 3](module-3---windows-graphics.md) , permitiendo al usuario dibujar un círculo con el mouse.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-131">Let's extend the Circle program from [Module 3](module-3---windows-graphics.md) by enabling the user to draw a circle with the mouse.</span></span> <span data-ttu-id="f6bb5-132">Comience con el programa de [ejemplo de círculo de Direct2D](direct2d-circle-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="f6bb5-132">Start with the [Direct2D Circle Sample](direct2d-circle-sample.md) program.</span></span> <span data-ttu-id="f6bb5-133">Se modificará el código de este ejemplo para agregar un dibujo sencillo.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-133">We will modify the code in this sample to add simple drawing.</span></span> <span data-ttu-id="f6bb5-134">En primer lugar, agregue una nueva variable miembro a la `MainWindow` clase.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-134">First, add a new member variable to the `MainWindow` class.</span></span>


```C++
    D2D1_POINT_2F           ptMouse;
```



<span data-ttu-id="f6bb5-135">Esta variable almacena la posición del puntero del mouse mientras el usuario arrastra el mouse.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-135">This variable stores the mouse-down position while the user is dragging the mouse.</span></span> <span data-ttu-id="f6bb5-136">En el `MainWindow` constructor, inicialice las variables *Ellipse* y *ptMouse* .</span><span class="sxs-lookup"><span data-stu-id="f6bb5-136">In the `MainWindow` constructor, initialize the *ellipse* and *ptMouse* variables.</span></span>


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



<span data-ttu-id="f6bb5-137">Quite el cuerpo del `MainWindow::CalculateLayout` método; no es necesario para este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-137">Remove the body of the `MainWindow::CalculateLayout` method; it's not required for this example.</span></span>


```C++
    void    CalculateLayout() { }
```



<span data-ttu-id="f6bb5-138">A continuación, declare los controladores de mensajes para los mensajes con el botón primario, el botón primario y el movimiento del mouse.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-138">Next, declare message handlers for the left-button down, left-button up, and mouse-move messages.</span></span>


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



<span data-ttu-id="f6bb5-139">Las coordenadas del mouse se proporcionan en píxeles físicos, pero Direct2D espera píxeles independientes del dispositivo (DIP).</span><span class="sxs-lookup"><span data-stu-id="f6bb5-139">Mouse coordinates are given in physical pixels, but Direct2D expects device-independent pixels (DIPs).</span></span> <span data-ttu-id="f6bb5-140">Para controlar correctamente los valores altos de PPP, debe traducir las coordenadas de píxeles en DIP.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-140">To handle high-DPI settings correctly, you must translate the pixel coordinates into DIPs.</span></span> <span data-ttu-id="f6bb5-141">Para obtener más información acerca de los PPP, consulte [PPP y Device-Independent píxeles](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="f6bb5-141">For more discussion about DPI, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span> <span data-ttu-id="f6bb5-142">En el código siguiente se muestra una clase auxiliar que convierte píxeles en DIP.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-142">The following code shows a helper class that converts pixels into DIPs.</span></span>


```C++
class DPIScale
{
    static float scaleX;
    static float scaleY;

public:
    static void Initialize(ID2D1Factory *pFactory)
    {
        FLOAT dpiX, dpiY;
        pFactory->GetDesktopDpi(&dpiX, &dpiY);
        scaleX = dpiX/96.0f;
        scaleY = dpiY/96.0f;
    }

    template <typename T>
    static D2D1_POINT_2F PixelsToDips(T x, T y)
    {
        return D2D1::Point2F(static_cast<float>(x) / scaleX, static_cast<float>(y) / scaleY);
    }
};

float DPIScale::scaleX = 1.0f;
float DPIScale::scaleY = 1.0f;
```



<span data-ttu-id="f6bb5-143">Llame a `DPIScale::Initialize` en el controlador de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) , después de crear el objeto de generador de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-143">Call `DPIScale::Initialize` in your [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) handler, after you create the Direct2D factory object.</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        DPIScale::Initialize(pFactory);
        return 0;
```



<span data-ttu-id="f6bb5-144">Para obtener las coordenadas del mouse en DIP desde los mensajes del mouse, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f6bb5-144">To get the mouse coordinates in DIPs from the mouse messages, do the following:</span></span>

1.  <span data-ttu-id="f6bb5-145">Use las macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) y [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para obtener las coordenadas de píxeles.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-145">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to get the pixel coordinates.</span></span> <span data-ttu-id="f6bb5-146">Estas macros se definen en WindowsX. h, por lo que no olvide incluir ese encabezado en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-146">These macros are defined in WindowsX.h, so remember to include that header in your project.</span></span>
2.  <span data-ttu-id="f6bb5-147">Llame a `DPIScale::PixelsToDipsX` y `DPIScale::PixelsToDipsY` para convertir los píxeles en DIP.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-147">Call `DPIScale::PixelsToDipsX` and `DPIScale::PixelsToDipsY` to convert pixels to DIPs.</span></span>

<span data-ttu-id="f6bb5-148">Ahora, agregue los controladores de mensajes al procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-148">Now add the message handlers to your window procedure.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        OnLButtonDown(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;

    case WM_LBUTTONUP: 
        OnLButtonUp();
        return 0;

    case WM_MOUSEMOVE: 
        OnMouseMove(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;
```



<span data-ttu-id="f6bb5-149">Por último, implemente los propios controladores de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-149">Finally, implement the message handlers themselves.</span></span>

### <a name="left-button-down"></a><span data-ttu-id="f6bb5-150">Botón primario abajo</span><span class="sxs-lookup"><span data-stu-id="f6bb5-150">Left Button Down</span></span>

<span data-ttu-id="f6bb5-151">En el caso del mensaje situado a la izquierda, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f6bb5-151">For the left-button down message, do the following:</span></span>

1.  <span data-ttu-id="f6bb5-152">Llame a [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) para empezar a capturar el mouse.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-152">Call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to begin capturing the mouse.</span></span>
2.  <span data-ttu-id="f6bb5-153">Almacene la posición del clic del mouse en la variable *ptMouse* .</span><span class="sxs-lookup"><span data-stu-id="f6bb5-153">Store the position of the mouse click in the *ptMouse* variable.</span></span> <span data-ttu-id="f6bb5-154">Esta posición define la esquina superior izquierda del cuadro de límite de la elipse.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-154">This position defines the upper left corner of the bounding box for the ellipse.</span></span>
3.  <span data-ttu-id="f6bb5-155">Restablecer la estructura de la elipse.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-155">Reset the ellipse structure.</span></span>
4.  <span data-ttu-id="f6bb5-156">Llame a [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="f6bb5-156">Call [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="f6bb5-157">Esta función obliga a que se vuelva a dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-157">This function forces the window to be repainted.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a><span data-ttu-id="f6bb5-158">Movimiento del mouse</span><span class="sxs-lookup"><span data-stu-id="f6bb5-158">Mouse Move</span></span>

<span data-ttu-id="f6bb5-159">Para el mensaje de movimiento del mouse, compruebe si el botón primario del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-159">For the mouse-move message, check whether the left mouse button is down.</span></span> <span data-ttu-id="f6bb5-160">Si es así, vuelva a calcular la elipse y vuelva a dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-160">If it is, recalculate the ellipse and repaint the window.</span></span> <span data-ttu-id="f6bb5-161">En Direct2D, una elipse se define mediante el punto central y los radios x e y.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-161">In Direct2D, an ellipse is defined by the center point and x- and y-radii.</span></span> <span data-ttu-id="f6bb5-162">Queremos dibujar una elipse que se ajuste al rectángulo de selección definido por el punto de desplazamiento del mouse (*ptMouse*) y la posición actual del cursor (*x*, *y*), por lo que se necesita un poco de aritmética para buscar el ancho, el alto y la posición de la elipse.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-162">We want to draw an ellipse that fits the bounding box defined by the mouse-down point (*ptMouse*) and the current cursor position (*x*, *y*), so a bit of arithmetic is needed to find the width, height, and position of the ellipse.</span></span>

<span data-ttu-id="f6bb5-163">En el código siguiente se vuelve a calcular la elipse y, a continuación, se llama a [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) para volver a dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-163">The following code recalculates the ellipse and then calls [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) to repaint the window.</span></span>

![Diagrama que muestra una elipse con RADIUS x e y.](images/input02.png)


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    if (flags & MK_LBUTTON) 
    { 
        const D2D1_POINT_2F dips = DPIScale::PixelsToDips(pixelX, pixelY);

        const float width = (dips.x - ptMouse.x) / 2;
        const float height = (dips.y - ptMouse.y) / 2;
        const float x1 = ptMouse.x + width;
        const float y1 = ptMouse.y + height;

        ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);

        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



### <a name="left-button-up"></a><span data-ttu-id="f6bb5-165">Botón primario arriba</span><span class="sxs-lookup"><span data-stu-id="f6bb5-165">Left Button Up</span></span>

<span data-ttu-id="f6bb5-166">En el caso del mensaje de botón izquierdo, simplemente llame a [**releaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) para liberar la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="f6bb5-166">For the left-button-up message, simply call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) to release the mouse capture.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a><span data-ttu-id="f6bb5-167">Siguientes</span><span class="sxs-lookup"><span data-stu-id="f6bb5-167">Next</span></span>

[<span data-ttu-id="f6bb5-168">Otras operaciones del mouse</span><span class="sxs-lookup"><span data-stu-id="f6bb5-168">Other Mouse Operations</span></span>](other-mouse-operations.md)

 

 