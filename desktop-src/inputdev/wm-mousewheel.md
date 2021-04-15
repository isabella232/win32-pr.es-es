---
title: Mensaje de WM_MOUSEWHEEL (Winuser. h)
description: Se envía a la ventana de foco cuando se gira la rueda del mouse.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- Entrada de mouse y teclado de mensaje de WM_MOUSEWHEEL
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b918989b41b43c3f54d8ec3133223716e839e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695899"
---
# <a name="wm_mousewheel-message"></a><span data-ttu-id="14853-104">Mensaje de WM \_ MOUSEWHEEL</span><span class="sxs-lookup"><span data-stu-id="14853-104">WM\_MOUSEWHEEL message</span></span>

<span data-ttu-id="14853-105">Se envía a la ventana de foco cuando se gira la rueda del mouse.</span><span class="sxs-lookup"><span data-stu-id="14853-105">Sent to the focus window when the mouse wheel is rotated.</span></span> <span data-ttu-id="14853-106">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga el mensaje al elemento primario de la ventana.</span><span class="sxs-lookup"><span data-stu-id="14853-106">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function propagates the message to the window's parent.</span></span> <span data-ttu-id="14853-107">No debe haber un reenvío interno del mensaje, ya que **DefWindowProc** lo propaga hacia arriba en la cadena primaria hasta que encuentra una ventana que la procesa.</span><span class="sxs-lookup"><span data-stu-id="14853-107">There should be no internal forwarding of the message, since **DefWindowProc** propagates it up the parent chain until it finds a window that processes it.</span></span>

<span data-ttu-id="14853-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="14853-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a><span data-ttu-id="14853-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14853-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14853-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14853-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14853-111">La palabra de orden superior indica la distancia a la que gira la rueda, expresada en múltiplos o divisiones de la **\_ diferencia** de la rueda, que es 120.</span><span class="sxs-lookup"><span data-stu-id="14853-111">The high-order word indicates the distance the wheel is rotated, expressed in multiples or divisions of **WHEEL\_DELTA**, which is 120.</span></span> <span data-ttu-id="14853-112">Un valor positivo indica que la rueda se giró hacia delante, alejándose del usuario; un valor negativo indica que la rueda se giró hacia atrás, hacia el usuario.</span><span class="sxs-lookup"><span data-stu-id="14853-112">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span>

<span data-ttu-id="14853-113">La palabra de orden inferior indica si varias claves virtuales están inactivas.</span><span class="sxs-lookup"><span data-stu-id="14853-113">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="14853-114">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="14853-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="14853-115">Value</span><span class="sxs-lookup"><span data-stu-id="14853-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="14853-116">Significado</span><span class="sxs-lookup"><span data-stu-id="14853-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="14853-117"><dt>**MK \_**</dt> <dt>0X0008</dt> de control</span><span class="sxs-lookup"><span data-stu-id="14853-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="14853-118">La tecla CTRL está presionada.</span><span class="sxs-lookup"><span data-stu-id="14853-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="14853-119"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="14853-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="14853-120">El botón primario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="14853-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="14853-121"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="14853-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="14853-122">El botón central del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="14853-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="14853-123"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="14853-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="14853-124">El botón secundario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="14853-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="14853-125"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="14853-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="14853-126">La tecla Mayús está presionada.</span><span class="sxs-lookup"><span data-stu-id="14853-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="14853-127"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="14853-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="14853-128">El primer botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="14853-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="14853-129"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="14853-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="14853-130">El segundo botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="14853-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="14853-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14853-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14853-132">La palabra de orden inferior especifica la coordenada x del puntero, relativa a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="14853-132">The low-order word specifies the x-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="14853-133">La palabra de orden superior especifica la coordenada y del puntero, con respecto a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="14853-133">The high-order word specifies the y-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14853-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14853-134">Return value</span></span>

<span data-ttu-id="14853-135">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="14853-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="14853-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14853-136">Remarks</span></span>

<span data-ttu-id="14853-137">Use el código siguiente para obtener la información del parámetro *wParam* :</span><span class="sxs-lookup"><span data-stu-id="14853-137">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="14853-138">Use el código siguiente para obtener la posición horizontal y vertical:</span><span class="sxs-lookup"><span data-stu-id="14853-138">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="14853-139">Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores).</span><span class="sxs-lookup"><span data-stu-id="14853-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="14853-140">Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="14853-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="14853-141">También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.</span><span class="sxs-lookup"><span data-stu-id="14853-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14853-142">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="14853-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="14853-143">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="14853-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="14853-144">La rotación de la rueda será un múltiplo de la **\_ diferencia** de la rueda, que se establece en 120.</span><span class="sxs-lookup"><span data-stu-id="14853-144">The wheel rotation will be a multiple of **WHEEL\_DELTA**, which is set at 120.</span></span> <span data-ttu-id="14853-145">Este es el umbral de acción que se va a realizar y una acción de este tipo (por ejemplo, desplazarse un incremento) debe producirse para cada diferencia.</span><span class="sxs-lookup"><span data-stu-id="14853-145">This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.</span></span>

<span data-ttu-id="14853-146">El delta se estableció en 120 para que Microsoft u otros proveedores puedan crear ruedas de resolución más precisa (una rueda de rotación gratuita sin muescas) para enviar más mensajes por rotación, pero con un valor menor en cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="14853-146">The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message.</span></span> <span data-ttu-id="14853-147">Para usar esta característica, puede Agregar los valores Delta entrantes hasta que se alcance la **\_ diferencia** de la rueda (por lo que para una rotación Delta obtiene la misma respuesta) o desplazarse por las líneas parciales en respuesta a los mensajes con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="14853-147">To use this feature, you can either add the incoming delta values until **WHEEL\_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to the more frequent messages.</span></span> <span data-ttu-id="14853-148">También puede elegir la granularidad de desplazamiento y acumular las diferencias hasta que se alcance.</span><span class="sxs-lookup"><span data-stu-id="14853-148">You can also choose your scroll granularity and accumulate deltas until it is reached.</span></span>

<span data-ttu-id="14853-149">Tenga en cuenta que no hay *fwKeys* para **MSH \_ MOUSEWHEEL**.</span><span class="sxs-lookup"><span data-stu-id="14853-149">Note, there is no *fwKeys* for **MSH\_MOUSEWHEEL**.</span></span> <span data-ttu-id="14853-150">De lo contrario, los parámetros son exactamente iguales que para **WM \_ MOUSEWHEEL**.</span><span class="sxs-lookup"><span data-stu-id="14853-150">Otherwise, the parameters are exactly the same as for **WM\_MOUSEWHEEL**.</span></span>

<span data-ttu-id="14853-151">Depende de la aplicación reenviar **MSH \_ MOUSEWHEEL** a cualquier objeto o control incrustado.</span><span class="sxs-lookup"><span data-stu-id="14853-151">It is up to the application to forward **MSH\_MOUSEWHEEL** to any embedded objects or controls.</span></span> <span data-ttu-id="14853-152">La aplicación es necesaria para enviar el mensaje a una aplicación OLE integrada activa.</span><span class="sxs-lookup"><span data-stu-id="14853-152">The application is required to send the message to an active embedded OLE application.</span></span> <span data-ttu-id="14853-153">Es opcional que la aplicación la envíe a un control habilitado para rueda con el foco.</span><span class="sxs-lookup"><span data-stu-id="14853-153">It is optional that the application sends it to a wheel-enabled control with focus.</span></span> <span data-ttu-id="14853-154">Si la aplicación envía el mensaje a un control, puede comprobar el valor devuelto para ver si se procesó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="14853-154">If the application does send the message to a control, it can check the return value to see if the message was processed.</span></span> <span data-ttu-id="14853-155">Los controles son necesarios para devolver el valor **true** si procesan el mensaje.</span><span class="sxs-lookup"><span data-stu-id="14853-155">Controls are required to return a value of **TRUE** if they process the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="14853-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14853-156">Requirements</span></span>



| <span data-ttu-id="14853-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="14853-157">Requirement</span></span> | <span data-ttu-id="14853-158">Value</span><span class="sxs-lookup"><span data-stu-id="14853-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14853-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14853-159">Minimum supported client</span></span><br/> | <span data-ttu-id="14853-160">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="14853-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="14853-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14853-161">Minimum supported server</span></span><br/> | <span data-ttu-id="14853-162">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14853-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="14853-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14853-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="14853-164"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14853-164"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14853-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="14853-165">See also</span></span>

<dl> <dt>

<span data-ttu-id="14853-166">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="14853-166">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="14853-167">**OBTENER \_ KEYSTATE \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="14853-167">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="14853-168">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="14853-168">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="14853-169">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="14853-169">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="14853-170">**GET \_ wheel \_ Delta \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="14853-170">**GET\_WHEEL\_DELTA\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

<span data-ttu-id="14853-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="14853-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="14853-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="14853-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="14853-173">**evento del mouse \_**</span><span class="sxs-lookup"><span data-stu-id="14853-173">**mouse\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

<span data-ttu-id="14853-174">**Vista**</span><span class="sxs-lookup"><span data-stu-id="14853-174">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="14853-175">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="14853-175">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="14853-176">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="14853-176">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="14853-177">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="14853-177">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[<span data-ttu-id="14853-178">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="14853-178">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="14853-179">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="14853-179">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="14853-180">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="14853-180">**SystemParametersInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

