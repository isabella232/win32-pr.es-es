---
title: Operaciones de mouse misceláneas
description: En las secciones anteriores se han explicado los clics del mouse y el movimiento del mouse. A continuación se indican algunas operaciones que se pueden realizar con el mouse.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfba63dce8116d79a557cbbbf8895f17d2a8f1b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358951"
---
# <a name="miscellaneous-mouse-operations"></a><span data-ttu-id="edf92-104">Operaciones de mouse misceláneas</span><span class="sxs-lookup"><span data-stu-id="edf92-104">Miscellaneous Mouse Operations</span></span>

<span data-ttu-id="edf92-105">En las secciones anteriores se han explicado los clics del mouse y el movimiento del mouse.</span><span class="sxs-lookup"><span data-stu-id="edf92-105">The previous sections have discussed mouse clicks and mouse movement.</span></span> <span data-ttu-id="edf92-106">A continuación se indican algunas operaciones que se pueden realizar con el mouse.</span><span class="sxs-lookup"><span data-stu-id="edf92-106">Here are some other operations that can be performed with the mouse.</span></span>

## <a name="dragging-ui-elements"></a><span data-ttu-id="edf92-107">Arrastrar elementos de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="edf92-107">Dragging UI Elements</span></span>

<span data-ttu-id="edf92-108">Si la interfaz de usuario admite arrastrar elementos de la interfaz de usuario, hay otra función a la que se debe llamar en el controlador de mensajes de mouse: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span><span class="sxs-lookup"><span data-stu-id="edf92-108">If your UI supports dragging of UI elements, there is one other function that you should call in your mouse-down message handler: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span></span> <span data-ttu-id="edf92-109">La función **DragDetect** devuelve **true** si el usuario inicia un gesto del mouse que debe interpretarse como un arrastre.</span><span class="sxs-lookup"><span data-stu-id="edf92-109">The **DragDetect** function returns **TRUE** if the user initiates a mouse gesture that should be interpreted as dragging.</span></span> <span data-ttu-id="edf92-110">En el código siguiente se muestra cómo usar esta función.</span><span class="sxs-lookup"><span data-stu-id="edf92-110">The following code shows how to use this function.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        {
            POINT pt = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam) };
            if (DragDetect(m_hwnd, pt))
            {
                // Start dragging.
            }
        }
        return 0;
```



<span data-ttu-id="edf92-111">Esta es la idea: cuando un programa admite arrastrar y colocar, no desea que todos los clics del mouse se interpreten como un arrastre.</span><span class="sxs-lookup"><span data-stu-id="edf92-111">Here's the idea: When a program supports drag and drop, you don't want every mouse click to be interpreted as a drag.</span></span> <span data-ttu-id="edf92-112">De lo contrario, es posible que el usuario arrastre accidentalmente algo cuando simplemente destinaría hacer clic en él (por ejemplo, para seleccionarlo).</span><span class="sxs-lookup"><span data-stu-id="edf92-112">Otherwise, the user might accidentally drag something when he or she simply meant to click on it (for example, to select it).</span></span> <span data-ttu-id="edf92-113">Pero si un mouse es especialmente sensible, puede ser difícil mantener el mouse perfectamente al hacer clic.</span><span class="sxs-lookup"><span data-stu-id="edf92-113">But if a mouse is particularly sensitive, it can be hard to keep the mouse perfectly still while clicking.</span></span> <span data-ttu-id="edf92-114">Por lo tanto, Windows define un umbral de arrastre de unos pocos píxeles.</span><span class="sxs-lookup"><span data-stu-id="edf92-114">Therefore, Windows defines a drag threshold of a few pixels.</span></span> <span data-ttu-id="edf92-115">Cuando el usuario presiona el botón del mouse, no se considera un arrastre a menos que el mouse cruce este umbral.</span><span class="sxs-lookup"><span data-stu-id="edf92-115">When the user presses the mouse button, it is not considered a drag unless the mouse crosses this threshold.</span></span> <span data-ttu-id="edf92-116">La función [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) comprueba si se alcanza este umbral.</span><span class="sxs-lookup"><span data-stu-id="edf92-116">The [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function tests whether this threshold is reached.</span></span> <span data-ttu-id="edf92-117">Si la función devuelve **true**, puede interpretar el clic del mouse como un arrastre.</span><span class="sxs-lookup"><span data-stu-id="edf92-117">If the function returns **TRUE**, you can interpret the mouse click as a drag.</span></span> <span data-ttu-id="edf92-118">En caso contrario, no.</span><span class="sxs-lookup"><span data-stu-id="edf92-118">Otherwise, do not.</span></span>

> [!Note]  
> <span data-ttu-id="edf92-119">Si [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) devuelve **false**, Windows suprime el mensaje de [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) cuando el usuario suelta el botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="edf92-119">If [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) returns **FALSE**, Windows suppresses the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message when the user releases the mouse button.</span></span> <span data-ttu-id="edf92-120">Por lo tanto, no llame a **DragDetect** a menos que el programa esté actualmente en un modo que admita arrastrar.</span><span class="sxs-lookup"><span data-stu-id="edf92-120">Therefore, do not call **DragDetect** unless your program is currently in a mode that supports dragging.</span></span> <span data-ttu-id="edf92-121">(Por ejemplo, si ya se ha seleccionado un elemento de la interfaz de usuario arrastrable). Al final de este módulo, veremos un ejemplo de código más largo en el que se usa la función **DragDetect** .</span><span class="sxs-lookup"><span data-stu-id="edf92-121">(For example, if a draggable UI element is already selected.) At the end of this module, we will see a longer code example that uses the **DragDetect** function.</span></span>

 

## <a name="confining-the-cursor"></a><span data-ttu-id="edf92-122">Restringir el cursor</span><span class="sxs-lookup"><span data-stu-id="edf92-122">Confining the Cursor</span></span>

<span data-ttu-id="edf92-123">En ocasiones, es posible que desee restringir el cursor al área cliente o a una parte del área cliente.</span><span class="sxs-lookup"><span data-stu-id="edf92-123">Sometimes you might want to restrict the cursor to the client area or a portion of the client area.</span></span> <span data-ttu-id="edf92-124">La función [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) restringe el movimiento del cursor a un rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="edf92-124">The [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) function restricts the movement of the cursor to a specified rectangle.</span></span> <span data-ttu-id="edf92-125">Este rectángulo se proporciona en coordenadas de pantalla, en lugar de coordenadas de cliente, por lo que el punto (0,0) significa la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="edf92-125">This rectangle is given in screen coordinates, rather than client coordinates, so the point (0, 0) means the upper left corner of the screen.</span></span> <span data-ttu-id="edf92-126">Para convertir las coordenadas de cliente en coordenadas de pantalla, llame a la función [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).</span><span class="sxs-lookup"><span data-stu-id="edf92-126">To translate client coordinates into screen coordinates, call the function [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).</span></span>

<span data-ttu-id="edf92-127">El siguiente código refina el cursor en el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="edf92-127">The following code confines the cursor to the client area of the window.</span></span>


```C++
    // Get the window client area.
    RECT rc;
    GetClientRect(m_hwnd, &rc);

    // Convert the client area to screen coordinates.
    POINT pt = { rc.left, rc.top };
    POINT pt2 = { rc.right, rc.bottom };
    ClientToScreen(m_hwnd, &pt);
    ClientToScreen(m_hwnd, &pt2);
    SetRect(&rc, pt.x, pt.y, pt2.x, pt2.y);

    // Confine the cursor.
    ClipCursor(&rc);
```



<span data-ttu-id="edf92-128">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) toma una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) , pero [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) toma una estructura [**Point**](/previous-versions//dd162805(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="edf92-128">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) takes a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure, but [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) takes a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="edf92-129">Un rectángulo se define por sus puntos superior izquierdo e inferior derecho.</span><span class="sxs-lookup"><span data-stu-id="edf92-129">A rectangle is defined by its top-left and bottom-right points.</span></span> <span data-ttu-id="edf92-130">Puede limitar el cursor a cualquier área rectangular, incluidas las áreas fuera de la ventana, pero restringir el cursor al área cliente es una forma habitual de usar la función.</span><span class="sxs-lookup"><span data-stu-id="edf92-130">You can confine the cursor to any rectangular area, including areas outside the window, but confining the cursor to the client area is a typical way to use the function.</span></span> <span data-ttu-id="edf92-131">Restringir el cursor a una región totalmente fuera de la ventana sería inusual y los usuarios probablemente lo percibirían como un error.</span><span class="sxs-lookup"><span data-stu-id="edf92-131">Confining the cursor to a region entirely outside your window would be unusual, and users would probably perceive it as a bug.</span></span>

<span data-ttu-id="edf92-132">Para quitar la restricción, llame a [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) con el valor **null**.</span><span class="sxs-lookup"><span data-stu-id="edf92-132">To remove the restriction, call [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) with the value **NULL**.</span></span>


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a><span data-ttu-id="edf92-133">Eventos de seguimiento del mouse: mantener el mouse y salir</span><span class="sxs-lookup"><span data-stu-id="edf92-133">Mouse Tracking Events: Hover and Leave</span></span>

<span data-ttu-id="edf92-134">Otros dos mensajes del mouse están deshabilitados de forma predeterminada, pero pueden ser útiles para algunas aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="edf92-134">Two other mouse messages are disabled by default, but may be useful for some applications:</span></span>

-   <span data-ttu-id="edf92-135">[**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): el cursor se ha desplazado sobre el área de cliente durante un período de tiempo fijo.</span><span class="sxs-lookup"><span data-stu-id="edf92-135">[**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): The cursor has hovered over the client area for a fixed period of time.</span></span>
-   <span data-ttu-id="edf92-136">[**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): el cursor ha dejado el área cliente.</span><span class="sxs-lookup"><span data-stu-id="edf92-136">[**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): The cursor has left the client area.</span></span>

<span data-ttu-id="edf92-137">Para habilitar estos mensajes, llame a la función [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) .</span><span class="sxs-lookup"><span data-stu-id="edf92-137">To enable these messages, call the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function.</span></span>


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



<span data-ttu-id="edf92-138">La estructura [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) contiene los parámetros de la función.</span><span class="sxs-lookup"><span data-stu-id="edf92-138">The [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) structure contains the parameters for the function.</span></span> <span data-ttu-id="edf92-139">El miembro **dwFlags** de la estructura contiene marcas de bits que especifican los mensajes de seguimiento que le interesan.</span><span class="sxs-lookup"><span data-stu-id="edf92-139">The **dwFlags** member of the structure contains bit flags that specify which tracking messages you are interested in.</span></span> <span data-ttu-id="edf92-140">Puede optar por obtener [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) y [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), como se muestra aquí, o solo uno de los dos.</span><span class="sxs-lookup"><span data-stu-id="edf92-140">You can choose to get both [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) and [**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), as shown here, or just one of the two.</span></span> <span data-ttu-id="edf92-141">El miembro **dwHoverTime** especifica cuánto tiempo debe desplazarse el mouse antes de que el sistema genere un mensaje de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="edf92-141">The **dwHoverTime** member specifies how long the mouse needs to hover before the system generates a hover message.</span></span> <span data-ttu-id="edf92-142">Este valor se expresa en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="edf92-142">This value is given in milliseconds.</span></span> <span data-ttu-id="edf92-143">El **\_ valor predeterminado de mantener el puntero** constante significa usar el valor predeterminado del sistema.</span><span class="sxs-lookup"><span data-stu-id="edf92-143">The constant **HOVER\_DEFAULT** means to use the system default.</span></span>

<span data-ttu-id="edf92-144">Después de obtener uno de los mensajes solicitados, se restablece la función [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) .</span><span class="sxs-lookup"><span data-stu-id="edf92-144">After you get one of the messages that you requested, the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function resets.</span></span> <span data-ttu-id="edf92-145">Debe llamarlo de nuevo para obtener otro mensaje de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="edf92-145">You must call it again to get another tracking message.</span></span> <span data-ttu-id="edf92-146">Sin embargo, debe esperar hasta el siguiente mensaje de movimiento del mouse antes de volver a llamar a **TrackMouseEvent** .</span><span class="sxs-lookup"><span data-stu-id="edf92-146">However, you should wait until the next mouse-move message before calling **TrackMouseEvent** again.</span></span> <span data-ttu-id="edf92-147">De lo contrario, es posible que la ventana esté desbordada por mensajes de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="edf92-147">Otherwise, your window might be flooded with tracking messages.</span></span> <span data-ttu-id="edf92-148">Por ejemplo, si se mantiene el mouse, el sistema continuará generando un flujo de mensajes [**\_ MOUSEHOVER de WM**](/windows/desktop/inputdev/wm-mousehover) mientras el mouse sea estacionario.</span><span class="sxs-lookup"><span data-stu-id="edf92-148">For example, if the mouse is hovering, the system would continue to generate a stream of [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) messages while the mouse is stationary.</span></span> <span data-ttu-id="edf92-149">En realidad, no desea otro mensaje de **\_ MOUSEHOVER de WM** hasta que el mouse se desplace a otro lugar y mantenga el puntero de nuevo.</span><span class="sxs-lookup"><span data-stu-id="edf92-149">You don't actually want another **WM\_MOUSEHOVER** message until the mouse moves to another spot and hovers again.</span></span>

<span data-ttu-id="edf92-150">Esta es una pequeña clase auxiliar que puede usar para administrar los eventos de seguimiento del mouse.</span><span class="sxs-lookup"><span data-stu-id="edf92-150">Here is a small helper class that you can use to manage mouse-tracking events.</span></span>


```C++
class MouseTrackEvents
{
    bool m_bMouseTracking;

public:
    MouseTrackEvents() : m_bMouseTracking(false)
    {
    }
    
    void OnMouseMove(HWND hwnd)
    {
        if (!m_bMouseTracking)
        {
            // Enable mouse tracking.
            TRACKMOUSEEVENT tme;
            tme.cbSize = sizeof(tme);
            tme.hwndTrack = hwnd;
            tme.dwFlags = TME_HOVER | TME_LEAVE;
            tme.dwHoverTime = HOVER_DEFAULT;
            TrackMouseEvent(&tme);
            m_bMouseTracking = true;
        }
    }
    void Reset(HWND hwnd)
    {
        m_bMouseTracking = false;
    }
};
```



<span data-ttu-id="edf92-151">En el ejemplo siguiente se muestra cómo utilizar esta clase en el procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="edf92-151">The next example shows how to use this class in your window procedure.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_MOUSEMOVE:
        mouseTrack.OnMouseMove(m_hwnd);  // Start tracking.

        // TODO: Handle the mouse-move message.

        return 0;

    case WM_MOUSELEAVE:

        // TODO: Handle the mouse-leave message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    case WM_MOUSEHOVER:

        // TODO: Handle the mouse-hover message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="edf92-152">Los eventos de seguimiento del mouse requieren un procesamiento adicional por parte del sistema, por lo que debe dejarlos deshabilitados si no los necesita.</span><span class="sxs-lookup"><span data-stu-id="edf92-152">Mouse tracking events require additional processing by the system, so leave them disabled if you do not need them.</span></span>

<span data-ttu-id="edf92-153">Por integridad, esta es una función que consulta el sistema para el tiempo de espera predeterminado de mantener el mouse.</span><span class="sxs-lookup"><span data-stu-id="edf92-153">For completeness, here is a function that queries the system for the default hover timeout.</span></span>


```C++
UINT GetMouseHoverTime()
{
    UINT msec; 
    if (SystemParametersInfo(SPI_GETMOUSEHOVERTIME, 0, &msec, 0))
    {   
        return msec;
    }
    else
    {
        return 0;
    }
}
```



## <a name="mouse-wheel"></a><span data-ttu-id="edf92-154">Rueda del mouse</span><span class="sxs-lookup"><span data-stu-id="edf92-154">Mouse Wheel</span></span>

<span data-ttu-id="edf92-155">La función siguiente comprueba si hay una rueda del mouse.</span><span class="sxs-lookup"><span data-stu-id="edf92-155">The following function checks if a mouse wheel is present.</span></span>


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



<span data-ttu-id="edf92-156">Si el usuario gira la rueda del mouse, la ventana que tiene el foco recibe un mensaje de [**WM \_ MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) .</span><span class="sxs-lookup"><span data-stu-id="edf92-156">If the user rotates the mouse wheel, the window with focus receives a [**WM\_MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) message.</span></span> <span data-ttu-id="edf92-157">El parámetro *wParam* de este mensaje contiene un valor entero denominado *Delta* que mide hasta qué punto se ha girado la rueda.</span><span class="sxs-lookup"><span data-stu-id="edf92-157">The *wParam* parameter of this message contains an integer value called the *delta* that measures how far the wheel was rotated.</span></span> <span data-ttu-id="edf92-158">La diferencia usa unidades arbitrarias, donde se definen 120 unidades como la rotación necesaria para realizar una "acción".</span><span class="sxs-lookup"><span data-stu-id="edf92-158">The delta uses arbitrary units, where 120 units is defined as the rotation needed to perform one "action."</span></span> <span data-ttu-id="edf92-159">Por supuesto, la definición de una acción depende del programa.</span><span class="sxs-lookup"><span data-stu-id="edf92-159">Of course, the definition of an action depends on your program.</span></span> <span data-ttu-id="edf92-160">Por ejemplo, si se usa la rueda del mouse para desplazar el texto, cada 120 unidades de giro se desplazarían una línea de texto.</span><span class="sxs-lookup"><span data-stu-id="edf92-160">For example, if the mouse wheel is used to scroll text, each 120 units of rotation would scroll one line of text.</span></span>

<span data-ttu-id="edf92-161">El signo de la diferencia indica la dirección de la rotación:</span><span class="sxs-lookup"><span data-stu-id="edf92-161">The sign of the delta indicates the direction of rotation:</span></span>

-   <span data-ttu-id="edf92-162">Positivo: girar hacia delante, fuera del usuario.</span><span class="sxs-lookup"><span data-stu-id="edf92-162">Positive: Rotate forward, away from the user.</span></span>
-   <span data-ttu-id="edf92-163">Negativo: gira hacia atrás, hacia el usuario.</span><span class="sxs-lookup"><span data-stu-id="edf92-163">Negative: Rotate backward, toward the user.</span></span>

<span data-ttu-id="edf92-164">El valor del delta se coloca en *wParam* junto con algunas marcas adicionales.</span><span class="sxs-lookup"><span data-stu-id="edf92-164">The value of the delta is placed in *wParam* along with some additional flags.</span></span> <span data-ttu-id="edf92-165">Use la macro [**Get \_ wheel \_ Delta \_ wParam**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) para obtener el valor de la diferencia.</span><span class="sxs-lookup"><span data-stu-id="edf92-165">Use the [**GET\_WHEEL\_DELTA\_WPARAM**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) macro to get the value of the delta.</span></span>


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="edf92-166">Si la rueda del mouse tiene una resolución alta, el valor absoluto de la diferencia puede ser menor que 120.</span><span class="sxs-lookup"><span data-stu-id="edf92-166">If the mouse wheel has a high resolution, the absolute value of the delta might be less than 120.</span></span> <span data-ttu-id="edf92-167">En ese caso, si tiene sentido que la acción se produzca en incrementos más pequeños, puede hacerlo.</span><span class="sxs-lookup"><span data-stu-id="edf92-167">In that case, if it makes sense for the action to occur in smaller increments, you can do so.</span></span> <span data-ttu-id="edf92-168">Por ejemplo, el texto podría desplazarse por incrementos de menos de una línea.</span><span class="sxs-lookup"><span data-stu-id="edf92-168">For example, text could scroll by increments of less than one line.</span></span> <span data-ttu-id="edf92-169">De lo contrario, acumule la diferencia total hasta que la rueda gire lo suficiente para realizar la acción.</span><span class="sxs-lookup"><span data-stu-id="edf92-169">Otherwise, accumulate the total delta until the wheel rotates enough to perform the action.</span></span> <span data-ttu-id="edf92-170">Almacene el Delta sin usar en una variable y, cuando se acumulen 120 unidades (positivo o negativo), realice la acción.</span><span class="sxs-lookup"><span data-stu-id="edf92-170">Store the unused delta in a variable, and when 120 units accumulate (either positive or negative), perform the action.</span></span>

## <a name="next"></a><span data-ttu-id="edf92-171">Siguientes</span><span class="sxs-lookup"><span data-stu-id="edf92-171">Next</span></span>

[<span data-ttu-id="edf92-172">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="edf92-172">Keyboard Input</span></span>](keyboard-input.md)

 

 