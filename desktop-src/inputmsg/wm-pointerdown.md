---
title: WM_POINTERDOWN mensaje
description: Se publica cuando un puntero realiza un contacto sobre el área de cliente de una ventana.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- WM_POINTERDOWN mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9f94bf4474e208d0b1d29df7a5e2939d7826ca77
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689208"
---
# <a name="wm_pointerdown-message"></a><span data-ttu-id="de5ac-104">WM_POINTERDOWN mensaje</span><span class="sxs-lookup"><span data-stu-id="de5ac-104">WM_POINTERDOWN message</span></span>

<span data-ttu-id="de5ac-105">Se publica cuando un puntero realiza un contacto sobre el área de cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="de5ac-105">Posted when a pointer makes contact over the client area of a window.</span></span> <span data-ttu-id="de5ac-106">Este mensaje de entrada tiene como destino la ventana a través de la que el puntero realiza el contacto y el puntero se captura implícitamente en la ventana para que la ventana siga recibiendo la entrada del puntero hasta que se interrumpe el contacto.</span><span class="sxs-lookup"><span data-stu-id="de5ac-106">This input message targets the window over which the pointer makes contact, and the pointer is implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="de5ac-107">Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="de5ac-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="de5ac-108">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="de5ac-108">\[!Important\]</span></span>  
> <span data-ttu-id="de5ac-109">Las aplicaciones de escritorio deben tener en cuenta los valores de PPP.</span><span class="sxs-lookup"><span data-stu-id="de5ac-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="de5ac-110">Si la aplicación no tiene reconocimiento de PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas pueden parecer inexactas debido a la virtualización de PPP.</span><span class="sxs-lookup"><span data-stu-id="de5ac-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="de5ac-111">La virtualización de PPP proporciona compatibilidad con el escalado automático a aplicaciones que no tienen reconocimiento de PPP y que están activas de forma predeterminada (los usuarios pueden desactivarla).</span><span class="sxs-lookup"><span data-stu-id="de5ac-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="de5ac-112">Para obtener más información, consulte [Escritura de aplicaciones Win32 con valores altos de PPP.](/previous-versions//dd464660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="de5ac-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a><span data-ttu-id="de5ac-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de5ac-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de5ac-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de5ac-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de5ac-115">Contiene información sobre el puntero.</span><span class="sxs-lookup"><span data-stu-id="de5ac-115">Contains information about the pointer.</span></span> <span data-ttu-id="de5ac-116">Use las macros siguientes para recuperar información del parámetro wParam.</span><span class="sxs-lookup"><span data-stu-id="de5ac-116">Use the following macros to retrieve information from the wParam parameter.</span></span>

-   <span data-ttu-id="de5ac-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador del puntero.</span><span class="sxs-lookup"><span data-stu-id="de5ac-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): the pointer identifier.</span></span>
-   <span data-ttu-id="de5ac-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje representa la primera entrada generada por un nuevo puntero.</span><span class="sxs-lookup"><span data-stu-id="de5ac-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message represents the first input generated by a new pointer.</span></span>
-   <span data-ttu-id="de5ac-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si un puntero generó este mensaje durante su vigencia.</span><span class="sxs-lookup"><span data-stu-id="de5ac-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer during its lifetime.</span></span> <span data-ttu-id="de5ac-120">Esta marca no se establece en los mensajes que indican que el puntero tiene un intervalo de detección izquierdo.</span><span class="sxs-lookup"><span data-stu-id="de5ac-120">This flag is not set on messages that indicate that the pointer has left detection range</span></span>
-   <span data-ttu-id="de5ac-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje lo generó un puntero que está en contacto con la superficie de la ventana.</span><span class="sxs-lookup"><span data-stu-id="de5ac-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer that is in contact with the window surface.</span></span> <span data-ttu-id="de5ac-122">Esta marca no se establece en los mensajes que indican un puntero que mantiene el puntero.</span><span class="sxs-lookup"><span data-stu-id="de5ac-122">This flag is not set on messages that indicate a hovering pointer.</span></span>
-   <span data-ttu-id="de5ac-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica que este puntero se ha designado como principal.</span><span class="sxs-lookup"><span data-stu-id="de5ac-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indicates that this pointer has been designated as primary.</span></span>
-   <span data-ttu-id="de5ac-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una acción principal.</span><span class="sxs-lookup"><span data-stu-id="de5ac-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a primary action.</span></span>
    -   <span data-ttu-id="de5ac-125">Esto es análogo a un botón izquierdo del mouse hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="de5ac-125">This is analogous to a mouse left button down.</span></span>
    -   <span data-ttu-id="de5ac-126">Un puntero táctil tendrá este conjunto cuando esté en contacto con la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="de5ac-126">A touch pointer will have this set when it is in contact with the digitizer surface.</span></span>
    -   <span data-ttu-id="de5ac-127">Un puntero de lápiz tendrá este conjunto cuando esté en contacto con la superficie del digitalizador sin botones presionados.</span><span class="sxs-lookup"><span data-stu-id="de5ac-127">A pen pointer will have this set when it is in contact with the digitizer surface with no buttons pressed.</span></span>
-   <span data-ttu-id="de5ac-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una acción secundaria.</span><span class="sxs-lookup"><span data-stu-id="de5ac-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a secondary action.</span></span>
    -   <span data-ttu-id="de5ac-129">Esto es análogo a un botón derecho del mouse hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="de5ac-129">This is analogous to a mouse right button down.</span></span>
    -   <span data-ttu-id="de5ac-130">Un puntero de lápiz tendrá este conjunto cuando esté en contacto con la superficie del digitalizador con el botón de lápiz presionado.</span><span class="sxs-lookup"><span data-stu-id="de5ac-130">A pen pointer will have this set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>
-   <span data-ttu-id="de5ac-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): una marca que indica si hay una o varias acciones terciarias basadas en el tipo de puntero; Las aplicaciones que desean responder a acciones terciarias deben recuperar información específica del tipo de puntero para determinar qué botones terciarios se presionan.</span><span class="sxs-lookup"><span data-stu-id="de5ac-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there are one or more tertiary actions based on the pointer type; applications that wish to respond to tertiary actions must retrieve information specific to the pointer type to determine which tertiary buttons are pressed.</span></span> <span data-ttu-id="de5ac-132">Por ejemplo, una aplicación puede determinar los estados de los botones de un lápiz llamando a [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) y examinando las marcas que especifican los estados de los botones.</span><span class="sxs-lookup"><span data-stu-id="de5ac-132">For example, an application can determine the buttons states of a pen by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>
-   <span data-ttu-id="de5ac-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si el puntero especificado realizó la cuarta acción.</span><span class="sxs-lookup"><span data-stu-id="de5ac-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether the specified pointer took fourth action.</span></span> <span data-ttu-id="de5ac-134">Las aplicaciones que deseen responder a cuartas acciones deben recuperar información específica del tipo de puntero para determinar si se presiona el primer botón extendido del mouse (XButton1).</span><span class="sxs-lookup"><span data-stu-id="de5ac-134">Applications that wish to respond to fourth actions must retrieve information specific to the pointer type to determine if the first extended mouse (XButton1) button is pressed.</span></span>
-   <span data-ttu-id="de5ac-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): [**marca**](pointer-flags-contants.md) que indica si el puntero especificado realizó la quinta acción.</span><span class="sxs-lookup"><span data-stu-id="de5ac-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a [**flag**](pointer-flags-contants.md) that indicates whether the specified pointer took fifth action.</span></span> <span data-ttu-id="de5ac-136">Las aplicaciones que deseen responder a la quinta acción deben recuperar información específica del tipo de puntero para determinar si se presiona el segundo botón extendido del mouse (XButton2).</span><span class="sxs-lookup"><span data-stu-id="de5ac-136">Applications that wish to respond to fifth actions must retrieve information specific to the pointer type to determine if the second extended mouse (XButton2) button is pressed.</span></span>

    <span data-ttu-id="de5ac-137">Consulte [**Marcas de puntero para**](pointer-flags-contants.md) obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="de5ac-137">See [**Pointer Flags**](pointer-flags-contants.md) for more details.</span></span>

    > [!Note]  
    > <span data-ttu-id="de5ac-138">Un puntero que mantiene el puntero no tiene establecida ninguna de las marcas de botón.</span><span class="sxs-lookup"><span data-stu-id="de5ac-138">A hovering pointer has none of the button flags set.</span></span> <span data-ttu-id="de5ac-139">Esto es análogo a un movimiento del mouse sin botones del mouse hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="de5ac-139">This is analogous to a mouse move with no mouse buttons down.</span></span> <span data-ttu-id="de5ac-140">Una aplicación puede determinar los estados de botones de un lápiz que mantiene el puntero, por ejemplo, llamando a [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) y examinando las marcas que especifican los estados de los botones.</span><span class="sxs-lookup"><span data-stu-id="de5ac-140">An application can determine the buttons states of a hovering pen, for example, by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>

     

</dd> <dt>

<span data-ttu-id="de5ac-141">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de5ac-141">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de5ac-142">Contiene la ubicación de punto del puntero.</span><span class="sxs-lookup"><span data-stu-id="de5ac-142">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="de5ac-143">Dado que el puntero puede ponerse en contacto con el dispositivo a través de un área no trivial, esta ubicación de punto puede ser una simplificación de un área de puntero más compleja.</span><span class="sxs-lookup"><span data-stu-id="de5ac-143">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="de5ac-144">Siempre que sea posible, una aplicación debe usar la información completa del área de puntero en lugar de la ubicación del punto.</span><span class="sxs-lookup"><span data-stu-id="de5ac-144">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="de5ac-145">Use las macros siguientes para recuperar las coordenadas de pantalla física del punto.</span><span class="sxs-lookup"><span data-stu-id="de5ac-145">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="de5ac-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): la coordenada x (punto horizontal).</span><span class="sxs-lookup"><span data-stu-id="de5ac-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="de5ac-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordenada y (punto vertical).</span><span class="sxs-lookup"><span data-stu-id="de5ac-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de5ac-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de5ac-148">Return value</span></span>

<span data-ttu-id="de5ac-149">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="de5ac-149">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="de5ac-150">Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="de5ac-150">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="de5ac-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de5ac-151">Remarks</span></span>

> <span data-ttu-id="de5ac-152">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="de5ac-152">\[!Important\]</span></span>  
> <span data-ttu-id="de5ac-153">Cuando una ventana pierde la captura de [](wm-pointercapturechanged.md) un puntero y recibe la notificación WM_POINTERCAPTURECHANGED, normalmente no recibirá ninguna notificación adicional.</span><span class="sxs-lookup"><span data-stu-id="de5ac-153">When a window loses capture of a pointer and it receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it typically will not receive any further notifications.</span></span> <span data-ttu-id="de5ac-154">Por esta razón, es importante que no realice ninguna suposición basada en notificaciones de WM_POINTERDOWN WM_POINTERUP o WM_POINTERENTER / [](wm-pointerup.md) [](wm-pointerenter.md) / [**WM_POINTERLEAVE**](wm-pointerleave.md) emparejadas uniformemente.</span><span class="sxs-lookup"><span data-stu-id="de5ac-154">For this reason, it is important that you not make any assumptions based on evenly paired **WM_POINTERDOWN**/[**WM_POINTERUP**](wm-pointerup.md) or [**WM_POINTERENTER**](wm-pointerenter.md)/[**WM_POINTERLEAVE**](wm-pointerleave.md) notifications.</span></span>

 

<span data-ttu-id="de5ac-155">Cada puntero tiene un identificador de puntero único durante su duración.</span><span class="sxs-lookup"><span data-stu-id="de5ac-155">Each pointer has a unique pointer identifier during its lifetime.</span></span> <span data-ttu-id="de5ac-156">La duración de un puntero comienza cuando se detecta por primera vez.</span><span class="sxs-lookup"><span data-stu-id="de5ac-156">The lifetime of a pointer begins when it is first detected.</span></span>

<span data-ttu-id="de5ac-157">Se [**WM_POINTERENTER**](wm-pointerenter.md) mensaje de confirmación si se detecta un puntero que mantiene el puntero.</span><span class="sxs-lookup"><span data-stu-id="de5ac-157">A [**WM_POINTERENTER**](wm-pointerenter.md) message is generated if a hovering pointer is detected.</span></span> <span data-ttu-id="de5ac-158">Si **se detecta un** puntero que no mantiene el **puntero, WM_POINTERDOWN** un mensaje de WM_POINTERENTER seguido de un mensaje de confirmación.</span><span class="sxs-lookup"><span data-stu-id="de5ac-158">A **WM_POINTERDOWN** message followed by a **WM_POINTERENTER** message is generated if a non-hovering pointer is detected.</span></span>

<span data-ttu-id="de5ac-159">Durante su vigencia, un puntero puede generar una serie de mensajes [**WM_POINTERUPDATE**](wm-pointerupdate.md) mientras mantiene el puntero o está en contacto.</span><span class="sxs-lookup"><span data-stu-id="de5ac-159">During its lifetime, a pointer may generate a series of [**WM_POINTERUPDATE**](wm-pointerupdate.md) messages while it is hovering or in contact.</span></span>

<span data-ttu-id="de5ac-160">La duración de un puntero finaliza cuando ya no se detecta.</span><span class="sxs-lookup"><span data-stu-id="de5ac-160">The lifetime of a pointer ends when it is no longer detected.</span></span> <span data-ttu-id="de5ac-161">Esto genera un mensaje [**WM_POINTERLEAVE**](wm-pointerleave.md) mensaje.</span><span class="sxs-lookup"><span data-stu-id="de5ac-161">This generates a [**WM_POINTERLEAVE**](wm-pointerleave.md) message.</span></span>

<span data-ttu-id="de5ac-162">Cuando se anula un puntero, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) se establece.</span><span class="sxs-lookup"><span data-stu-id="de5ac-162">When a pointer is aborted, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) is set.</span></span>

<span data-ttu-id="de5ac-163">También [**WM_POINTERLEAVE**](wm-pointerleave.md) mensaje de error cuando un puntero no capturado se mueve fuera de los límites de una ventana.</span><span class="sxs-lookup"><span data-stu-id="de5ac-163">A [**WM_POINTERLEAVE**](wm-pointerleave.md) message may also be generated when a non-captured pointer moves outside the bounds of a window.</span></span>

<span data-ttu-id="de5ac-164">Para obtener la posición horizontal y vertical de un puntero, use lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="de5ac-164">To obtain the horizontal and vertical position of a pointer, use the following:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="de5ac-165">Para convertir el parámetro lParam en una [**estructura POINTS,**](/previous-versions//dd162808(v=vs.85)) use la macro [**MAKEPOINTS.**](/windows/win32/api/wingdi/nf-wingdi-makepoints)</span><span class="sxs-lookup"><span data-stu-id="de5ac-165">To convert the lParam parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure, use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro.</span></span>

<span data-ttu-id="de5ac-166">Para recuperar más información asociada al mensaje, use la [**función GetPointerInfo.**](/previous-versions/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="de5ac-166">To retrieve further information associated with the message, use the [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span>

<span data-ttu-id="de5ac-167">Para determinar los estados de tecla modificadora de teclado asociados a este mensaje, use la [**función GetKeyState.**](/windows/win32/api/winuser/nf-winuser-getkeystate)</span><span class="sxs-lookup"><span data-stu-id="de5ac-167">To determine the keyboard modifier key states associated with this message, use the [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) function.</span></span> <span data-ttu-id="de5ac-168">Por ejemplo, para detectar que se presionó la tecla ALT, compruebe si GetKeyState(VK_MENU) &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="de5ac-168">For example, to detect that the ALT key was pressed, check whether GetKeyState(VK_MENU) &lt; 0.</span></span>

<span data-ttu-id="de5ac-169">Tenga en cuenta que si la aplicación no procesa este mensaje, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) puede generar uno o varios mensajes [**WM_GESTURE**](../wintouch/wm-gesture.md) si la secuencia de entrada de este y, posiblemente, otros punteros se reconocen como un gesto.</span><span class="sxs-lookup"><span data-stu-id="de5ac-169">Note that if the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages if the sequence of input from this and, possibly, other pointers is recognized as a gesture.</span></span> <span data-ttu-id="de5ac-170">Si no se reconoce un gesto, **DefWindowProc puede** generar la entrada del mouse.</span><span class="sxs-lookup"><span data-stu-id="de5ac-170">If a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="de5ac-171">Si una aplicación consume selectivamente alguna entrada de puntero y pasa el resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), el comportamiento resultante es indefinido.</span><span class="sxs-lookup"><span data-stu-id="de5ac-171">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

<span data-ttu-id="de5ac-172">Cuando una ventana pierde la captura de un puntero y recibe la notificación [**WM_POINTERCAPTURECHANGED,**](wm-pointercapturechanged.md) normalmente no recibirá ninguna notificación adicional.</span><span class="sxs-lookup"><span data-stu-id="de5ac-172">When a window loses capture of a pointer and receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it will typically not receive any further notifications.</span></span> <span data-ttu-id="de5ac-173">Por lo tanto, es importante que una ventana no realice ninguna suposición de su estado de puntero, independientemente de si recibe notificaciones DOWN/UP o ENTER/LEAVE emparejadas uniformemente.</span><span class="sxs-lookup"><span data-stu-id="de5ac-173">Therefore, it is important that a window does not make any assumptions of its pointer status, regardless of whether it receives evenly paired DOWN / UP or ENTER / LEAVE notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="de5ac-174">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="de5ac-174">Examples</span></span>

<span data-ttu-id="de5ac-175">En el ejemplo de código siguiente se muestra cómo usar [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)y [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)para recuperar la información pertinente asociada al mensaje **de WM_POINTERDOWN.**</span><span class="sxs-lookup"><span data-stu-id="de5ac-175">The following code example shows how to use [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), and [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)to retrieve the relevant information associated with the **WM_POINTERDOWN** message.</span></span>


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse right button down
}
```



<span data-ttu-id="de5ac-176">En el ejemplo de código siguiente se muestra cómo [**usar GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para recuperar el identificador de puntero del **WM_POINTERDOWN** mensaje.</span><span class="sxs-lookup"><span data-stu-id="de5ac-176">The following code example shows how to use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to retrieve the pointer id from the **WM_POINTERDOWN** message.</span></span>


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



<span data-ttu-id="de5ac-177">En el ejemplo de código siguiente se muestra cómo controlar diferentes tipos de puntero, como dispositivos táctiles, de lápiz o de puntos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="de5ac-177">The following code example shows how to handle different pointer type such as touch, pen, or default pointing devices.</span></span>


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

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
        fHandled = HandleGenericPointerMessage(&pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a><span data-ttu-id="de5ac-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de5ac-178">Requirements</span></span>



| <span data-ttu-id="de5ac-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="de5ac-179">Requirement</span></span> | <span data-ttu-id="de5ac-180">Valor</span><span class="sxs-lookup"><span data-stu-id="de5ac-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de5ac-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de5ac-181">Minimum supported client</span></span><br/> | <span data-ttu-id="de5ac-182">\[Windows 8 solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="de5ac-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="de5ac-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de5ac-183">Minimum supported server</span></span><br/> | <span data-ttu-id="de5ac-184">\[Windows Server 2012 solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="de5ac-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="de5ac-185">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de5ac-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="de5ac-186"><dt>Winuser.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="de5ac-186"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de5ac-187">Consulte también</span><span class="sxs-lookup"><span data-stu-id="de5ac-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5ac-188">Mensajes</span><span class="sxs-lookup"><span data-stu-id="de5ac-188">Messages</span></span>](messages.md)
</dt> <dt>

<span data-ttu-id="de5ac-189">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="de5ac-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="de5ac-190">**Marcas de puntero**</span><span class="sxs-lookup"><span data-stu-id="de5ac-190">**Pointer Flags**</span></span>](pointer-flags-contants.md)
</dt> <dt>

[<span data-ttu-id="de5ac-191">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="de5ac-191">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="de5ac-192">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="de5ac-192">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="de5ac-193">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="de5ac-193">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="de5ac-194">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="de5ac-194">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="de5ac-195">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="de5ac-195">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="de5ac-196">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="de5ac-196">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="de5ac-197">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="de5ac-197">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="de5ac-198">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="de5ac-198">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="de5ac-199">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="de5ac-199">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="de5ac-200">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="de5ac-200">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>
