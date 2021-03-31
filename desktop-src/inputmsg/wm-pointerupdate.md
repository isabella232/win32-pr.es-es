---
title: Mensaje WM_POINTERUPDATE
description: Se publica para proporcionar una actualización en un puntero que se puso en contacto con el área de cliente de una ventana o en un puntero no capturado al mantener el mouse sobre el área cliente de una ventana.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac222
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERUPDATE
topic_type:
- apiref
api_name:
- WM_POINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 215874f4dc1b3438ae3d69b22758ced09a050f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151163"
---
# <a name="wm_pointerupdate-message"></a><span data-ttu-id="d9db4-104">Mensaje WM_POINTERUPDATE</span><span class="sxs-lookup"><span data-stu-id="d9db4-104">WM_POINTERUPDATE message</span></span>

<span data-ttu-id="d9db4-105">Se publica para proporcionar una actualización en un puntero que se puso en contacto con el área de cliente de una ventana o en un puntero no capturado al mantener el mouse sobre el área cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="d9db4-105">Posted to provide an update on a pointer that made contact over the client area of a window or on a hovering uncaptured pointer over the client area of a window.</span></span> <span data-ttu-id="d9db4-106">Mientras se mantiene el puntero, el mensaje se dirige a la ventana en la que se encuentra el puntero.</span><span class="sxs-lookup"><span data-stu-id="d9db4-106">While the pointer is hovering, the message targets whichever window the pointer happens to be over.</span></span> <span data-ttu-id="d9db4-107">Mientras el puntero se encuentra en contacto con la superficie, el puntero se captura implícitamente en la ventana en la que el puntero se pone en contacto y la ventana continúa recibiendo entradas para el puntero hasta que interrumpe el contacto.</span><span class="sxs-lookup"><span data-stu-id="d9db4-107">While the pointer is in contact with the surface, the pointer is implicitly captured to the window over which the pointer made contact and that window continues to receive input for the pointer until it breaks contact.</span></span>

> <span data-ttu-id="d9db4-108">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="d9db4-108">\[!Important\]</span></span>  
> <span data-ttu-id="d9db4-109">Las aplicaciones de escritorio deben tener en cuenta los ppp.</span><span class="sxs-lookup"><span data-stu-id="d9db4-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="d9db4-110">Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP.</span><span class="sxs-lookup"><span data-stu-id="d9db4-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="d9db4-111">La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla).</span><span class="sxs-lookup"><span data-stu-id="d9db4-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="d9db4-112">Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9db4-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERUPDATE              0x0245
```



## <a name="parameters"></a><span data-ttu-id="d9db4-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9db4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9db4-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9db4-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9db4-115">Contiene información sobre el puntero.</span><span class="sxs-lookup"><span data-stu-id="d9db4-115">Contains information about the pointer.</span></span> <span data-ttu-id="d9db4-116">Use las siguientes macros para recuperar información del parámetro wParam.</span><span class="sxs-lookup"><span data-stu-id="d9db4-116">Use the following macros to retrieve information from the wParam parameter.</span></span>

-   <span data-ttu-id="d9db4-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): el identificador de puntero.</span><span class="sxs-lookup"><span data-stu-id="d9db4-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): the pointer identifier.</span></span>
-   <span data-ttu-id="d9db4-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje representa la primera entrada generada por un nuevo puntero.</span><span class="sxs-lookup"><span data-stu-id="d9db4-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message represents the first input generated by a new pointer.</span></span>
-   <span data-ttu-id="d9db4-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje fue generado por un puntero durante su duración.</span><span class="sxs-lookup"><span data-stu-id="d9db4-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer during its lifetime.</span></span> <span data-ttu-id="d9db4-120">Esta marca no se establece en mensajes que indican que el puntero tiene el intervalo de detección izquierdo</span><span class="sxs-lookup"><span data-stu-id="d9db4-120">This flag is not set on messages that indicate that the pointer has left detection range</span></span>
-   <span data-ttu-id="d9db4-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje fue generado por un puntero que está en contacto con la superficie de la ventana.</span><span class="sxs-lookup"><span data-stu-id="d9db4-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer that is in contact with the window surface.</span></span> <span data-ttu-id="d9db4-122">Esta marca no se establece en los mensajes que indican un puntero de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d9db4-122">This flag is not set on messages that indicate a hovering pointer.</span></span>
-   <span data-ttu-id="d9db4-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica que este puntero se ha designado como principal.</span><span class="sxs-lookup"><span data-stu-id="d9db4-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indicates that this pointer has been designated as primary.</span></span>
-   <span data-ttu-id="d9db4-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una acción principal.</span><span class="sxs-lookup"><span data-stu-id="d9db4-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a primary action.</span></span>
    -   <span data-ttu-id="d9db4-125">Es análogo a un botón primario del mouse hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="d9db4-125">This is analogous to a mouse left button down.</span></span>
    -   <span data-ttu-id="d9db4-126">Un puntero táctil tendrá este conjunto cuando esté en contacto con la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="d9db4-126">A touch pointer will have this set when it is in contact with the digitizer surface.</span></span>
    -   <span data-ttu-id="d9db4-127">Un puntero de pluma tendrá este conjunto cuando esté en contacto con la superficie del digitalizador sin presionar ningún botón.</span><span class="sxs-lookup"><span data-stu-id="d9db4-127">A pen pointer will have this set when it is in contact with the digitizer surface with no buttons pressed.</span></span>
-   <span data-ttu-id="d9db4-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una acción secundaria.</span><span class="sxs-lookup"><span data-stu-id="d9db4-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a secondary action.</span></span>
    -   <span data-ttu-id="d9db4-129">Es análogo a un botón secundario del mouse hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="d9db4-129">This is analogous to a mouse right button down.</span></span>
    -   <span data-ttu-id="d9db4-130">Un puntero de pluma tendrá este conjunto cuando esté en contacto con la superficie del digitalizador con el botón de barril del lápiz presionado.</span><span class="sxs-lookup"><span data-stu-id="d9db4-130">A pen pointer will have this set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>
-   <span data-ttu-id="d9db4-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una o varias acciones terciarias basadas en el tipo de puntero; las aplicaciones que desean responder a las acciones terciarias deben recuperar información específica del tipo de puntero para determinar qué botones terciarios se presionan.</span><span class="sxs-lookup"><span data-stu-id="d9db4-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there are one or more tertiary actions based on the pointer type; applications that wish to respond to tertiary actions must retrieve information specific to the pointer type to determine which tertiary buttons are pressed.</span></span> <span data-ttu-id="d9db4-132">Por ejemplo, una aplicación puede determinar los Estados de los botones de un lápiz mediante una llamada a [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) y el examen de las marcas que especifican los Estados de los botones.</span><span class="sxs-lookup"><span data-stu-id="d9db4-132">For example, an application can determine the buttons states of a pen by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>
-   <span data-ttu-id="d9db4-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si el puntero especificado tardó la cuarta acción.</span><span class="sxs-lookup"><span data-stu-id="d9db4-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether the specified pointer took fourth action.</span></span> <span data-ttu-id="d9db4-134">Las aplicaciones que deseen responder a las cuarta acciones deben recuperar información específica del tipo de puntero para determinar si se presiona el botón del primer Mouse extendido (XButton1).</span><span class="sxs-lookup"><span data-stu-id="d9db4-134">Applications that wish to respond to fourth actions must retrieve information specific to the pointer type to determine if the first extended mouse (XButton1) button is pressed.</span></span>
-   <span data-ttu-id="d9db4-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): [**marca**](pointer-flags-contants.md) que indica si el puntero especificado tardó la quinta acción.</span><span class="sxs-lookup"><span data-stu-id="d9db4-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a [**flag**](pointer-flags-contants.md) that indicates whether the specified pointer took fifth action.</span></span> <span data-ttu-id="d9db4-136">Las aplicaciones que deseen responder a las Quinta acciones deben recuperar información específica del tipo de puntero para determinar si se presiona el botón secundario del mouse (XButton2).</span><span class="sxs-lookup"><span data-stu-id="d9db4-136">Applications that wish to respond to fifth actions must retrieve information specific to the pointer type to determine if the second extended mouse (XButton2) button is pressed.</span></span>

    <span data-ttu-id="d9db4-137">Consulte [**marcadores de puntero**](pointer-flags-contants.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="d9db4-137">See [**Pointer Flags**](pointer-flags-contants.md) for more details.</span></span>

    > [!Note]  
    > <span data-ttu-id="d9db4-138">Un puntero que mantiene el mouse no tiene ninguna de las marcas de botón establecidas.</span><span class="sxs-lookup"><span data-stu-id="d9db4-138">A hovering pointer has none of the button flags set.</span></span> <span data-ttu-id="d9db4-139">Esto es análogo a un movimiento del mouse sin presionar los botones del mouse.</span><span class="sxs-lookup"><span data-stu-id="d9db4-139">This is analogous to a mouse move with no mouse buttons down.</span></span> <span data-ttu-id="d9db4-140">Una aplicación puede determinar los Estados de los botones de un lápiz que mantiene el mouse, por ejemplo, llamando a [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) y examinando las marcas que especifican los Estados de los botones.</span><span class="sxs-lookup"><span data-stu-id="d9db4-140">An application can determine the buttons states of a hovering pen, for example, by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>

     

</dd> <dt>

<span data-ttu-id="d9db4-141">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9db4-141">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9db4-142">Contiene la ubicación del punto del puntero.</span><span class="sxs-lookup"><span data-stu-id="d9db4-142">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="d9db4-143">Dado que el puntero puede establecer contacto con el dispositivo a través de un área no trivial, esta ubicación de punto puede ser una simplificación de un área de puntero más compleja.</span><span class="sxs-lookup"><span data-stu-id="d9db4-143">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="d9db4-144">Siempre que sea posible, una aplicación debe usar la información de área de puntero completa en lugar de la ubicación del punto.</span><span class="sxs-lookup"><span data-stu-id="d9db4-144">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="d9db4-145">Utilice las siguientes macros para recuperar las coordenadas físicas de la pantalla del punto.</span><span class="sxs-lookup"><span data-stu-id="d9db4-145">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="d9db4-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): la coordenada X (punto horizontal).</span><span class="sxs-lookup"><span data-stu-id="d9db4-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="d9db4-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): la coordenada Y (punto vertical).</span><span class="sxs-lookup"><span data-stu-id="d9db4-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9db4-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9db4-148">Return value</span></span>

<span data-ttu-id="d9db4-149">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="d9db4-149">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="d9db4-150">Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="d9db4-150">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="d9db4-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9db4-151">Remarks</span></span>

<span data-ttu-id="d9db4-152">Cada puntero tiene un identificador de puntero único durante su duración.</span><span class="sxs-lookup"><span data-stu-id="d9db4-152">Each pointer has a unique pointer identifier during its lifetime.</span></span> <span data-ttu-id="d9db4-153">La duración de un puntero comienza cuando se detecta por primera vez.</span><span class="sxs-lookup"><span data-stu-id="d9db4-153">The lifetime of a pointer begins when it is first detected.</span></span>

<span data-ttu-id="d9db4-154">Si se detecta un puntero de desplazamiento, se genera un mensaje de [**WM_POINTERENTER**](wm-pointerenter.md) .</span><span class="sxs-lookup"><span data-stu-id="d9db4-154">A [**WM_POINTERENTER**](wm-pointerenter.md) message is generated if a hovering pointer is detected.</span></span> <span data-ttu-id="d9db4-155">Se genera un mensaje de [**WM_POINTERDOWN**](wm-pointerdown.md) seguido de un mensaje de **WM_POINTERENTER** si se detecta un puntero que no tiene el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d9db4-155">A [**WM_POINTERDOWN**](wm-pointerdown.md) message followed by a **WM_POINTERENTER** message is generated if a non-hovering pointer is detected.</span></span>

<span data-ttu-id="d9db4-156">Durante su duración, un puntero puede generar una serie de mensajes de **WM_POINTERUPDATE** mientras se mantiene el mouse o el contacto.</span><span class="sxs-lookup"><span data-stu-id="d9db4-156">During its lifetime, a pointer may generate a series of **WM_POINTERUPDATE** messages while it is hovering or in contact.</span></span>

<span data-ttu-id="d9db4-157">La duración de un puntero finaliza cuando ya no se detecta.</span><span class="sxs-lookup"><span data-stu-id="d9db4-157">The lifetime of a pointer ends when it is no longer detected.</span></span> <span data-ttu-id="d9db4-158">Esto genera un mensaje de [**WM_POINTERLEAVE**](wm-pointerleave.md) .</span><span class="sxs-lookup"><span data-stu-id="d9db4-158">This generates a [**WM_POINTERLEAVE**](wm-pointerleave.md) message.</span></span>

<span data-ttu-id="d9db4-159">Cuando se anula un puntero, se establece [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) .</span><span class="sxs-lookup"><span data-stu-id="d9db4-159">When a pointer is aborted, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) is set.</span></span>

<span data-ttu-id="d9db4-160">También se puede generar un mensaje [**WM_POINTERLEAVE**](wm-pointerleave.md) cuando un puntero no capturado se mueve fuera de los límites de una ventana.</span><span class="sxs-lookup"><span data-stu-id="d9db4-160">A [**WM_POINTERLEAVE**](wm-pointerleave.md) message may also be generated when a non-captured pointer moves outside the bounds of a window.</span></span>

<span data-ttu-id="d9db4-161">Para obtener la posición horizontal y vertical de un puntero, use lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d9db4-161">To obtain the horizontal and vertical position of a pointer, use the following:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="d9db4-162">La macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) también se puede usar para convertir el parámetro lParam en una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d9db4-162">The [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro can also be used to convert the lParam parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="d9db4-163">La función [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) se puede usar para determinar los Estados de tecla modificador de teclado asociados a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="d9db4-163">The [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) function can be used to determine the keyboard modifier key states associated with this message.</span></span> <span data-ttu-id="d9db4-164">Por ejemplo, para detectar que se presionó la tecla ALT, compruebe si **GetKeyState** (VK_MENU) &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d9db4-164">For example, to detect that the ALT key was pressed, check whether **GetKeyState** (VK_MENU) &lt; 0.</span></span>

<span data-ttu-id="d9db4-165">Si la aplicación no procesa este mensaje, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) puede generar uno o varios mensajes [**WM_GESTURE**](../wintouch/wm-gesture.md) si la secuencia de entrada de este y, posiblemente, otros punteros se reconocen como un gesto.</span><span class="sxs-lookup"><span data-stu-id="d9db4-165">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages if the sequence of input from this and, possibly, other pointers is recognized as a gesture.</span></span> <span data-ttu-id="d9db4-166">Si no se reconoce un gesto, **DefWindowProc** puede generar la entrada del mouse.</span><span class="sxs-lookup"><span data-stu-id="d9db4-166">If a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="d9db4-167">Si una aplicación usa selectivamente alguna entrada de puntero y pasa el resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), el comportamiento resultante es indefinido.</span><span class="sxs-lookup"><span data-stu-id="d9db4-167">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

<span data-ttu-id="d9db4-168">Utilice la función [**GetPointerInfo**](/previous-versions/windows/desktop/api) para recuperar más información relacionada con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="d9db4-168">Use the [**GetPointerInfo**](/previous-versions/windows/desktop/api) function to retrieve further information related to this message.</span></span>

<span data-ttu-id="d9db4-169">Si la aplicación no procesa estos mensajes tan rápido como se generan, se pueden fusionar algunos movimientos.</span><span class="sxs-lookup"><span data-stu-id="d9db4-169">If the application does not process these messages as fast as they are generated, some moves may be coalesced.</span></span> <span data-ttu-id="d9db4-170">El historial de entradas que se fusionaron en este mensaje se puede recuperar mediante la función [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="d9db4-170">The history of inputs that were coalesced into this message can be retrieved using the [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) function.</span></span>

## <a name="examples"></a><span data-ttu-id="d9db4-171">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d9db4-171">Examples</span></span>

<span data-ttu-id="d9db4-172">En el ejemplo de código siguiente se muestra cómo usar [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)y [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api) para recuperar información relevante de los parámetros wParam e lParam del mensaje **WM_POINTERUPDATE** .</span><span class="sxs-lookup"><span data-stu-id="d9db4-172">The following code example shows how to use [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), and [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api) to retrieve relevant information from the wParam and lParam parameters of the **WM_POINTERUPDATE** message.</span></span>


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer move while down, similar to mouse move with left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer move while down, similar to mouse move with right button down
}
```



<span data-ttu-id="d9db4-173">En el ejemplo de código siguiente se muestra cómo usar [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para recuperar el identificador de puntero del parámetro wParam del mensaje de **WM_POINTERUPDATE** .</span><span class="sxs-lookup"><span data-stu-id="d9db4-173">The following code example shows how to use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to retrieve the pointer id from the wParam parameter of the **WM_POINTERUPDATE** message.</span></span>


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &amp;pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



<span data-ttu-id="d9db4-174">En el ejemplo de código siguiente se muestra cómo administrar distintos tipos de puntero.</span><span class="sxs-lookup"><span data-stu-id="d9db4-174">The following code example shows how to handle different pointer types.</span></span>


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_INPUT_TYPE pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerInfo(&pointerInfo);
    }
    break;
}
```



## <a name="requirements"></a><span data-ttu-id="d9db4-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9db4-175">Requirements</span></span>



| <span data-ttu-id="d9db4-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9db4-176">Requirement</span></span> | <span data-ttu-id="d9db4-177">Value</span><span class="sxs-lookup"><span data-stu-id="d9db4-177">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9db4-178">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9db4-178">Minimum supported client</span></span><br/> | <span data-ttu-id="d9db4-179">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9db4-179">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="d9db4-180">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9db4-180">Minimum supported server</span></span><br/> | <span data-ttu-id="d9db4-181">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9db4-181">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d9db4-182">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9db4-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9db4-183"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9db4-183"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9db4-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9db4-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9db4-185">Mensajes</span><span class="sxs-lookup"><span data-stu-id="d9db4-185">Messages</span></span>](messages.md)
</dt> <dt>

<span data-ttu-id="d9db4-186">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d9db4-186">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d9db4-187">**Marcas de puntero**</span><span class="sxs-lookup"><span data-stu-id="d9db4-187">**Pointer Flags**</span></span>](pointer-flags-contants.md)
</dt> <dt>

[<span data-ttu-id="d9db4-188">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9db4-188">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="d9db4-189">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9db4-189">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="d9db4-190">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9db4-190">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="d9db4-191">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9db4-191">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="d9db4-192">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9db4-192">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="d9db4-193">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9db4-193">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="d9db4-194">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9db4-194">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="d9db4-195">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9db4-195">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="d9db4-196">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9db4-196">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="d9db4-197">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9db4-197">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

