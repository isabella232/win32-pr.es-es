---
title: Responder a clics del mouse
description: Responder a clics del mouse
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c37903264ca638aeca1c0b28fb2ea7fa792660
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149263"
---
# <a name="responding-to-mouse-clicks"></a><span data-ttu-id="104a5-103">Responder a clics del mouse</span><span class="sxs-lookup"><span data-stu-id="104a5-103">Responding to Mouse Clicks</span></span>

<span data-ttu-id="104a5-104">Si el usuario hace clic en un botón del mouse mientras el cursor está sobre el área cliente de una ventana, la ventana recibe uno de los mensajes siguientes.</span><span class="sxs-lookup"><span data-stu-id="104a5-104">If the user clicks a mouse button while the cursor is over the client area of a window, the window receives one of the following messages.</span></span>



| <span data-ttu-id="104a5-105">Mensaje</span><span class="sxs-lookup"><span data-stu-id="104a5-105">Message</span></span>                                        | <span data-ttu-id="104a5-106">Significado</span><span class="sxs-lookup"><span data-stu-id="104a5-106">Meaning</span></span>                   |
|------------------------------------------------|---------------------------|
| [<span data-ttu-id="104a5-107">**LBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="104a5-107">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown) | <span data-ttu-id="104a5-108">Botón primario abajo</span><span class="sxs-lookup"><span data-stu-id="104a5-108">Left button down</span></span>          |
| [<span data-ttu-id="104a5-109">**LBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="104a5-109">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)     | <span data-ttu-id="104a5-110">Botón primario arriba</span><span class="sxs-lookup"><span data-stu-id="104a5-110">Left button up</span></span>            |
| [<span data-ttu-id="104a5-111">**MBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="104a5-111">**WM\_MBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-mbuttondown) | <span data-ttu-id="104a5-112">Botón central abajo</span><span class="sxs-lookup"><span data-stu-id="104a5-112">Middle button down</span></span>        |
| [<span data-ttu-id="104a5-113">**MBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="104a5-113">**WM\_MBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-mbuttonup)     | <span data-ttu-id="104a5-114">Botón central arriba</span><span class="sxs-lookup"><span data-stu-id="104a5-114">Middle button up</span></span>          |
| [<span data-ttu-id="104a5-115">**RBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="104a5-115">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown) | <span data-ttu-id="104a5-116">Botón derecho abajo</span><span class="sxs-lookup"><span data-stu-id="104a5-116">Right button down</span></span>         |
| [<span data-ttu-id="104a5-117">**RBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="104a5-117">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)     | <span data-ttu-id="104a5-118">Botón derecho arriba</span><span class="sxs-lookup"><span data-stu-id="104a5-118">Right button up</span></span>           |
| [<span data-ttu-id="104a5-119">**XBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="104a5-119">**WM\_XBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-xbuttondown) | <span data-ttu-id="104a5-120">XBUTTON1 o XBUTTON2 abajo</span><span class="sxs-lookup"><span data-stu-id="104a5-120">XBUTTON1 or XBUTTON2 down</span></span> |
| [<span data-ttu-id="104a5-121">**XBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="104a5-121">**WM\_XBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-xbuttonup)     | <span data-ttu-id="104a5-122">XBUTTON1 o XBUTTON2 up</span><span class="sxs-lookup"><span data-stu-id="104a5-122">XBUTTON1 or XBUTTON2 up</span></span>   |



 

<span data-ttu-id="104a5-123">Recuerde que el área cliente es la parte de la ventana que excluye el marco.</span><span class="sxs-lookup"><span data-stu-id="104a5-123">Recall that the client area is the portion of the window that excludes the frame.</span></span> <span data-ttu-id="104a5-124">Para obtener más información acerca de las áreas de cliente, consulte [¿Qué es una ventana?](what-is-a-window-.md)</span><span class="sxs-lookup"><span data-stu-id="104a5-124">For more information about client areas, see [What Is a Window?](what-is-a-window-.md)</span></span>

### <a name="mouse-coordinates"></a><span data-ttu-id="104a5-125">Coordenadas del mouse</span><span class="sxs-lookup"><span data-stu-id="104a5-125">Mouse Coordinates</span></span>

<span data-ttu-id="104a5-126">En todos estos mensajes, el parámetro *lParam* contiene las coordenadas x e y del puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="104a5-126">In all of these messages, the *lParam* parameter contains the x- and y-coordinates of the mouse pointer.</span></span> <span data-ttu-id="104a5-127">Los 16 bits más bajos de *lParam* contienen la coordenada x y los 16 bits siguientes contienen la coordenada y.</span><span class="sxs-lookup"><span data-stu-id="104a5-127">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="104a5-128">Use las macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) y [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para desempaquetar las coordenadas de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="104a5-128">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="104a5-129">Estas macros se definen en el archivo de encabezado WindowsX. h.</span><span class="sxs-lookup"><span data-stu-id="104a5-129">These macros are defined in the header file WindowsX.h.</span></span>

<span data-ttu-id="104a5-130">En Windows de 64 bits, *lParam* es un valor de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="104a5-130">On 64-bit Windows, *lParam* is 64-bit value.</span></span> <span data-ttu-id="104a5-131">No se usan los 32 superiores de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="104a5-131">The upper 32 bits of *lParam* are not used.</span></span> <span data-ttu-id="104a5-132">La documentación de MSDN menciona la "palabra de orden inferior" y la "palabra de orden superior" de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="104a5-132">The MSDN documentation mentions the "low-order word" and "high-order word" of *lParam*.</span></span> <span data-ttu-id="104a5-133">En el caso de 64 bits, esto significa que las palabras de orden inferior y superior de los 32 bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="104a5-133">In the 64-bit case, this means the low- and high-order words of the lower 32 bits.</span></span> <span data-ttu-id="104a5-134">Las macros extraen los valores correctos, por lo que, si los usa, estará seguro.</span><span class="sxs-lookup"><span data-stu-id="104a5-134">The macros extract the right values, so if you use them, you will be safe.</span></span>

<span data-ttu-id="104a5-135">Las coordenadas del mouse se proporcionan en píxeles, no en píxeles independientes del dispositivo (DIP) y se miden en relación con el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="104a5-135">Mouse coordinates are given in pixels, not device-independent pixels (DIPs), and are measured relative to the client area of the window.</span></span> <span data-ttu-id="104a5-136">Las coordenadas son valores con signo.</span><span class="sxs-lookup"><span data-stu-id="104a5-136">Coordinates are signed values.</span></span> <span data-ttu-id="104a5-137">Las posiciones situadas encima y a la izquierda del área cliente tienen coordenadas negativas, lo que es importante si realiza el seguimiento de la posición del mouse fuera de la ventana.</span><span class="sxs-lookup"><span data-stu-id="104a5-137">Positions above and to the left of the client area have negative coordinates, which is important if you track the mouse position outside the window.</span></span> <span data-ttu-id="104a5-138">Veremos cómo hacerlo en un tema posterior, [capturando el movimiento del mouse fuera de la ventana](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="104a5-138">We will see how to do that in a later topic, [Capturing Mouse Movement Outside the Window](mouse-movement.md).</span></span>

### <a name="additional-flags"></a><span data-ttu-id="104a5-139">Marcas adicionales</span><span class="sxs-lookup"><span data-stu-id="104a5-139">Additional Flags</span></span>

<span data-ttu-id="104a5-140">El parámetro *wParam* contiene **una operación OR bit a bit** de marcas, que indica el estado de los demás botones del mouse más las teclas Mayús y Ctrl.</span><span class="sxs-lookup"><span data-stu-id="104a5-140">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span>



| <span data-ttu-id="104a5-141">Marca</span><span class="sxs-lookup"><span data-stu-id="104a5-141">Flag</span></span>             | <span data-ttu-id="104a5-142">Significado</span><span class="sxs-lookup"><span data-stu-id="104a5-142">Meaning</span></span>                          |
|------------------|----------------------------------|
| <span data-ttu-id="104a5-143">**MK ( \_ control)**</span><span class="sxs-lookup"><span data-stu-id="104a5-143">**MK\_CONTROL**</span></span>  | <span data-ttu-id="104a5-144">La tecla CTRL está presionada.</span><span class="sxs-lookup"><span data-stu-id="104a5-144">The CTRL key is down.</span></span>            |
| <span data-ttu-id="104a5-145">**MK \_ LBUTTON**</span><span class="sxs-lookup"><span data-stu-id="104a5-145">**MK\_LBUTTON**</span></span>  | <span data-ttu-id="104a5-146">El botón primario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="104a5-146">The left mouse button is down.</span></span>   |
| <span data-ttu-id="104a5-147">**MK \_ MBUTTON**</span><span class="sxs-lookup"><span data-stu-id="104a5-147">**MK\_MBUTTON**</span></span>  | <span data-ttu-id="104a5-148">El botón central del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="104a5-148">The middle mouse button is down.</span></span> |
| <span data-ttu-id="104a5-149">**MK \_ RBUTTON**</span><span class="sxs-lookup"><span data-stu-id="104a5-149">**MK\_RBUTTON**</span></span>  | <span data-ttu-id="104a5-150">El botón secundario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="104a5-150">The right mouse button is down.</span></span>  |
| <span data-ttu-id="104a5-151">**\_MAYÚS MK**</span><span class="sxs-lookup"><span data-stu-id="104a5-151">**MK\_SHIFT**</span></span>    | <span data-ttu-id="104a5-152">La tecla Mayús está presionada.</span><span class="sxs-lookup"><span data-stu-id="104a5-152">The SHIFT key is down.</span></span>           |
| <span data-ttu-id="104a5-153">**MK \_ XBUTTON1**</span><span class="sxs-lookup"><span data-stu-id="104a5-153">**MK\_XBUTTON1**</span></span> | <span data-ttu-id="104a5-154">El botón XBUTTON1 está inactivo.</span><span class="sxs-lookup"><span data-stu-id="104a5-154">The XBUTTON1 button is down.</span></span>     |
| <span data-ttu-id="104a5-155">**MK \_ XBUTTON2**</span><span class="sxs-lookup"><span data-stu-id="104a5-155">**MK\_XBUTTON2**</span></span> | <span data-ttu-id="104a5-156">El botón XBUTTON2 está inactivo.</span><span class="sxs-lookup"><span data-stu-id="104a5-156">The XBUTTON2 button is down.</span></span>     |



 

<span data-ttu-id="104a5-157">La ausencia de una marca significa que no se presionó el botón o la tecla correspondiente.</span><span class="sxs-lookup"><span data-stu-id="104a5-157">The absence of a flag means the corresponding button or key was not pressed.</span></span> <span data-ttu-id="104a5-158">Por ejemplo, para comprobar si la tecla CTRL está presionada:</span><span class="sxs-lookup"><span data-stu-id="104a5-158">For example, to test whether the CTRL key is down:</span></span>


```C++
if (wParam & MK_CONTROL) { ...
```



<span data-ttu-id="104a5-159">Si necesita buscar el estado de otras teclas además de CTRL y Mayús, use la función [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) , que se describe en [entrada de teclado](keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="104a5-159">If you need to find the state of other keys besides CTRL and SHIFT, use the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function, which is described in [Keyboard Input](keyboard-input.md).</span></span>

<span data-ttu-id="104a5-160">Los mensajes de la ventana de [**WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) y [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) se aplican tanto a XBUTTON1 como a XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="104a5-160">The [**WM\_XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) and [**WM\_XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) window messages apply to both XBUTTON1 and XBUTTON2.</span></span> <span data-ttu-id="104a5-161">El parámetro *wParam* indica en qué botón se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="104a5-161">The *wParam* parameter indicates which button was clicked.</span></span>


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a><span data-ttu-id="104a5-162">Doble clics</span><span class="sxs-lookup"><span data-stu-id="104a5-162">Double Clicks</span></span>

<span data-ttu-id="104a5-163">De forma predeterminada, una ventana no recibe notificaciones de doble clic.</span><span class="sxs-lookup"><span data-stu-id="104a5-163">A window does not receive double-click notifications by default.</span></span> <span data-ttu-id="104a5-164">Para recibir doble clic, establezca la marca **CS \_ DBLCLKS** en la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) al registrar la clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="104a5-164">To receive double clicks, set the **CS\_DBLCLKS** flag in the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure when you register the window class.</span></span>


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



<span data-ttu-id="104a5-165">Si establece la marca **CS \_ DBLCLKS** como se muestra, la ventana recibirá notificaciones de doble clic.</span><span class="sxs-lookup"><span data-stu-id="104a5-165">If you set the **CS\_DBLCLKS** flag as shown, the window will receive double-click notifications.</span></span> <span data-ttu-id="104a5-166">Un clic doble se indica mediante un mensaje de ventana con "DBLCLK" en el nombre.</span><span class="sxs-lookup"><span data-stu-id="104a5-166">A double click is indicated by a window message with "DBLCLK" in the name.</span></span> <span data-ttu-id="104a5-167">Por ejemplo, al hacer doble clic en el botón primario del mouse, se genera la siguiente secuencia de mensajes:</span><span class="sxs-lookup"><span data-stu-id="104a5-167">For example, a double click on the left mouse button produces the following sequence of messages:</span></span>

<dl>

[<span data-ttu-id="104a5-168">**LBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="104a5-168">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)  
[<span data-ttu-id="104a5-169">**LBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="104a5-169">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
[<span data-ttu-id="104a5-170">**LBUTTONDBLCLK de WM \_**</span><span class="sxs-lookup"><span data-stu-id="104a5-170">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)  
[<span data-ttu-id="104a5-171">**LBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="104a5-171">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

<span data-ttu-id="104a5-172">En efecto, el segundo mensaje de [**\_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown) que se generaría normalmente se convierte en un mensaje de [**\_ LBUTTONDBLCLK de WM**](/windows/desktop/inputdev/wm-lbuttondblclk) .</span><span class="sxs-lookup"><span data-stu-id="104a5-172">In effect, the second [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message that would normally be generated becomes a [**WM\_LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) message.</span></span> <span data-ttu-id="104a5-173">Los mensajes equivalentes se definen para los botones derecho, medio y botón XBUTTON.</span><span class="sxs-lookup"><span data-stu-id="104a5-173">Equivalent messages are defined for right, middle, and XBUTTON buttons.</span></span>

<span data-ttu-id="104a5-174">Hasta que obtenga el mensaje de doble clic, no hay ninguna manera de indicar que el primer clic del mouse es el inicio de un doble clic.</span><span class="sxs-lookup"><span data-stu-id="104a5-174">Until you get the double-click message, there is no way to tell that the first mouse click is the start of a double click.</span></span> <span data-ttu-id="104a5-175">Por lo tanto, una acción de doble clic debe continuar una acción que comience con el primer clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="104a5-175">Therefore, a double-click action should continue an action that begins with the first mouse click.</span></span> <span data-ttu-id="104a5-176">Por ejemplo, en el shell de Windows, un solo clic selecciona una carpeta, mientras que un doble clic abre la carpeta.</span><span class="sxs-lookup"><span data-stu-id="104a5-176">For example, in the Windows Shell, a single click selects a folder, while a double click opens the folder.</span></span>

## <a name="non-client-mouse-messages"></a><span data-ttu-id="104a5-177">Mensajes de mouse que no son de cliente</span><span class="sxs-lookup"><span data-stu-id="104a5-177">Non-client Mouse Messages</span></span>

<span data-ttu-id="104a5-178">Se define un conjunto independiente de mensajes para los eventos del mouse que se producen dentro del área no cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="104a5-178">A separate set of messages are defined for mouse events that occur within the non-client area of the window.</span></span> <span data-ttu-id="104a5-179">Estos mensajes tienen las letras "NC" en el nombre.</span><span class="sxs-lookup"><span data-stu-id="104a5-179">These messages have the letters "NC" in the name.</span></span> <span data-ttu-id="104a5-180">Por ejemplo, [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) es el equivalente no cliente de [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span><span class="sxs-lookup"><span data-stu-id="104a5-180">For example, [**WM\_NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) is the non-client equivalent of [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span></span> <span data-ttu-id="104a5-181">Una aplicación típica no interceptará estos mensajes, porque la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) controla estos mensajes correctamente.</span><span class="sxs-lookup"><span data-stu-id="104a5-181">A typical application will not intercept these messages, because the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function handles these messages correctly.</span></span> <span data-ttu-id="104a5-182">Sin embargo, pueden ser útiles para ciertas funciones avanzadas.</span><span class="sxs-lookup"><span data-stu-id="104a5-182">However, they can be useful for certain advanced functions.</span></span> <span data-ttu-id="104a5-183">Por ejemplo, podría utilizar estos mensajes para implementar el comportamiento personalizado en la barra de título.</span><span class="sxs-lookup"><span data-stu-id="104a5-183">For example, you could use these messages to implement custom behavior in the title bar.</span></span> <span data-ttu-id="104a5-184">Si administra estos mensajes, normalmente debe pasarlos a **DefWindowProc** después.</span><span class="sxs-lookup"><span data-stu-id="104a5-184">If you do handle these messages, you should generally pass them to **DefWindowProc** afterward.</span></span> <span data-ttu-id="104a5-185">De lo contrario, la aplicación interrumpirá la funcionalidad estándar, como arrastrar o minimizar la ventana.</span><span class="sxs-lookup"><span data-stu-id="104a5-185">Otherwise, your application will break standard functionality such as dragging or minimizing the window.</span></span>

## <a name="next"></a><span data-ttu-id="104a5-186">Siguientes</span><span class="sxs-lookup"><span data-stu-id="104a5-186">Next</span></span>

[<span data-ttu-id="104a5-187">Movimiento del mouse</span><span class="sxs-lookup"><span data-stu-id="104a5-187">Mouse Movement</span></span>](mouse-movement.md)

 

 