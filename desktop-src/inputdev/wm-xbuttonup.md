---
title: Mensaje de WM_XBUTTONUP (Winuser. h)
description: Se envía cuando el usuario suelta el primer o el segundo botón X mientras el cursor está en el área de cliente de una ventana.
ms.assetid: ad726859-368a-4603-bffa-4e639bc69a6a
keywords:
- Entrada de mouse y teclado de mensaje de WM_XBUTTONUP
topic_type:
- apiref
api_name:
- WM_XBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 08/23/2019
ms.openlocfilehash: 521faefb2e2a76e94a0517c28a5fa812ef34ef5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996764"
---
# <a name="wm_xbuttonup-message"></a><span data-ttu-id="9cdc0-104">Mensaje de XBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="9cdc0-104">WM\_XBUTTONUP message</span></span>

<span data-ttu-id="9cdc0-105">Se envía cuando el usuario suelta el primer o el segundo botón X mientras el cursor está en el área de cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-105">Posted when the user releases the first or second X button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="9cdc0-106">Si no se captura el mouse, el mensaje se envía a la ventana debajo del cursor.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="9cdc0-107">De lo contrario, el mensaje se envía a la ventana que ha capturado el mouse.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="9cdc0-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9cdc0-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_XBUTTONUP                    0x020C
```



## <a name="parameters"></a><span data-ttu-id="9cdc0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9cdc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cdc0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9cdc0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cdc0-111">La palabra de orden inferior indica si varias claves virtuales están inactivas.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-111">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="9cdc0-112">Puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-112">It can be one or more of the following values.</span></span>



| <span data-ttu-id="9cdc0-113">Value</span><span class="sxs-lookup"><span data-stu-id="9cdc0-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="9cdc0-114">Significado</span><span class="sxs-lookup"><span data-stu-id="9cdc0-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="9cdc0-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de control</span><span class="sxs-lookup"><span data-stu-id="9cdc0-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="9cdc0-116">La tecla CTRL está presionada.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="9cdc0-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="9cdc0-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="9cdc0-118">El botón primario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="9cdc0-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="9cdc0-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="9cdc0-120">El botón central del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="9cdc0-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="9cdc0-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="9cdc0-122">El botón secundario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="9cdc0-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="9cdc0-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="9cdc0-124">La tecla Mayús está presionada.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="9cdc0-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="9cdc0-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="9cdc0-126">El primer botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="9cdc0-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="9cdc0-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="9cdc0-128">El segundo botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-128">The second X button is down.</span></span><br/>     |



 

<span data-ttu-id="9cdc0-129">La palabra de orden superior indica qué botón se liberó.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-129">The high-order word indicates which button was released.</span></span> <span data-ttu-id="9cdc0-130">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="9cdc0-130">It can be one of the following values:</span></span>



| <span data-ttu-id="9cdc0-131">Value</span><span class="sxs-lookup"><span data-stu-id="9cdc0-131">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="9cdc0-132">Significado</span><span class="sxs-lookup"><span data-stu-id="9cdc0-132">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="9cdc0-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="9cdc0-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="9cdc0-134">Se liberó el primer botón X.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-134">The first X button was released.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="9cdc0-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="9cdc0-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="9cdc0-136">Se liberó el segundo botón X.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-136">The second X button was released.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9cdc0-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9cdc0-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cdc0-138">La palabra de orden inferior especifica la coordenada x del cursor.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-138">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="9cdc0-139">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-139">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="9cdc0-140">La palabra de orden superior especifica la coordenada y del cursor.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-140">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="9cdc0-141">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-141">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cdc0-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9cdc0-142">Return value</span></span>

<span data-ttu-id="9cdc0-143">Si una aplicación procesa este mensaje, debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-143">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="9cdc0-144">Para obtener más información sobre cómo procesar el valor devuelto, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-144">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cdc0-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9cdc0-145">Remarks</span></span>

<span data-ttu-id="9cdc0-146">Use el código siguiente para obtener la información del parámetro *wParam* :</span><span class="sxs-lookup"><span data-stu-id="9cdc0-146">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



<span data-ttu-id="9cdc0-147">Use el código siguiente para obtener la posición horizontal y vertical:</span><span class="sxs-lookup"><span data-stu-id="9cdc0-147">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="9cdc0-148">Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores).</span><span class="sxs-lookup"><span data-stu-id="9cdc0-148">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="9cdc0-149">Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-149">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="9cdc0-150">También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-150">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9cdc0-151">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-151">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="9cdc0-152">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-152">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="9cdc0-153">A diferencia de los mensajes [**WM \_ LBUTTONUP**](wm-lbuttonup.md), [**WM \_ MBUTTONUP**](wm-mbuttonup.md)y [**WM \_ RBUTTONUP**](wm-rbuttonup.md) , una aplicación debe devolver **true** desde este mensaje si lo procesa.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-153">Unlike the [**WM\_LBUTTONUP**](wm-lbuttonup.md), [**WM\_MBUTTONUP**](wm-mbuttonup.md), and [**WM\_RBUTTONUP**](wm-rbuttonup.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="9cdc0-154">Esto permitirá que el software que simula este mensaje en sistemas Windows anteriores a Windows 2000 determine si el procedimiento de ventana procesó el mensaje o llamó a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para procesarlo.</span><span class="sxs-lookup"><span data-stu-id="9cdc0-154">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cdc0-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cdc0-155">Requirements</span></span>



| <span data-ttu-id="9cdc0-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cdc0-156">Requirement</span></span> | <span data-ttu-id="9cdc0-157">Value</span><span class="sxs-lookup"><span data-stu-id="9cdc0-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cdc0-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cdc0-158">Minimum supported client</span></span><br/> | <span data-ttu-id="9cdc0-159">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9cdc0-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9cdc0-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cdc0-160">Minimum supported server</span></span><br/> | <span data-ttu-id="9cdc0-161">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9cdc0-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9cdc0-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9cdc0-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cdc0-163"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9cdc0-163"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cdc0-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cdc0-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="9cdc0-165">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9cdc0-165">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9cdc0-166">**OBTENER \_ KEYSTATE \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="9cdc0-166">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="9cdc0-167">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="9cdc0-167">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="9cdc0-168">**OBTENER \_ botón xbutton \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="9cdc0-168">**GET\_XBUTTON\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[<span data-ttu-id="9cdc0-169">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="9cdc0-169">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="9cdc0-170">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="9cdc0-170">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="9cdc0-171">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="9cdc0-171">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="9cdc0-172">**XBUTTONDBLCLK de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9cdc0-172">**WM\_XBUTTONDBLCLK**</span></span>](wm-xbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="9cdc0-173">**XBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9cdc0-173">**WM\_XBUTTONDOWN**</span></span>](wm-xbuttondown.md)
</dt> <dt>

<span data-ttu-id="9cdc0-174">**Vista**</span><span class="sxs-lookup"><span data-stu-id="9cdc0-174">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9cdc0-175">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="9cdc0-175">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="9cdc0-176">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="9cdc0-176">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9cdc0-177">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="9cdc0-177">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="9cdc0-178">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9cdc0-178">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

