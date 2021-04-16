---
title: Mensaje de WM_LBUTTONDOWN (Winuser. h)
description: Se envía cuando el usuario presiona el botón primario del mouse mientras el cursor está en el área de cliente de una ventana.
ms.assetid: 2e43720a-98e6-407a-9430-34c288c3da51
keywords:
- Entrada de mouse y teclado de mensaje de WM_LBUTTONDOWN
topic_type:
- apiref
api_name:
- WM_LBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: c8ac54e813d622f47462b73b763534977ba0932f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699961"
---
# <a name="wm_lbuttondown-message"></a><span data-ttu-id="e523e-104">Mensaje de LBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="e523e-104">WM\_LBUTTONDOWN message</span></span>

<span data-ttu-id="e523e-105">Se envía cuando el usuario presiona el botón primario del mouse mientras el cursor está en el área de cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="e523e-105">Posted when the user presses the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="e523e-106">Si no se captura el mouse, el mensaje se envía a la ventana debajo del cursor.</span><span class="sxs-lookup"><span data-stu-id="e523e-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="e523e-107">De lo contrario, el mensaje se envía a la ventana que ha capturado el mouse.</span><span class="sxs-lookup"><span data-stu-id="e523e-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="e523e-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e523e-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONDOWN                  0x0201
```



## <a name="parameters"></a><span data-ttu-id="e523e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e523e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e523e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e523e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e523e-111">Indica si varias claves virtuales están inactivas.</span><span class="sxs-lookup"><span data-stu-id="e523e-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="e523e-112">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e523e-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="e523e-113">Value</span><span class="sxs-lookup"><span data-stu-id="e523e-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="e523e-114">Significado</span><span class="sxs-lookup"><span data-stu-id="e523e-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="e523e-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de control</span><span class="sxs-lookup"><span data-stu-id="e523e-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="e523e-116">La tecla CTRL está presionada.</span><span class="sxs-lookup"><span data-stu-id="e523e-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="e523e-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="e523e-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="e523e-118">El botón primario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="e523e-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="e523e-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="e523e-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="e523e-120">El botón central del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="e523e-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="e523e-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="e523e-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="e523e-122">El botón secundario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="e523e-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="e523e-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="e523e-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="e523e-124">La tecla Mayús está presionada.</span><span class="sxs-lookup"><span data-stu-id="e523e-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="e523e-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="e523e-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="e523e-126">El primer botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="e523e-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="e523e-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="e523e-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="e523e-128">El segundo botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="e523e-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="e523e-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e523e-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e523e-130">La palabra de orden inferior especifica la coordenada x del cursor.</span><span class="sxs-lookup"><span data-stu-id="e523e-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="e523e-131">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="e523e-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="e523e-132">La palabra de orden superior especifica la coordenada y del cursor.</span><span class="sxs-lookup"><span data-stu-id="e523e-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="e523e-133">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="e523e-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e523e-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e523e-134">Return value</span></span>

<span data-ttu-id="e523e-135">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="e523e-135">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="e523e-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e523e-136">Example</span></span>


```cpp
LRESULT CALLBACK WndProc(_In_ HWND hWnd, _In_ UINT msg, _In_ WPARAM wParam, _In_ LPARAM lParam)
{
    POINT pt;

    switch (msg)
    {

    case WM_LBUTTONDOWN:
            {
                pt.x = GET_X_LPARAM(lParam);
                pt.y = GET_Y_LPARAM(lParam);
            }
        }
        break;

    default:
        return DefWindowProc(hWnd, msg, wParam, lParam);
    }
    return 0;
}
```

<span data-ttu-id="e523e-137">Para obtener más ejemplos, vea [ejemplos de Windows clásico](https://github.com/microsoft/Windows-classic-samples) en github.</span><span class="sxs-lookup"><span data-stu-id="e523e-137">For more examples see [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="e523e-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e523e-138">Remarks</span></span>

<span data-ttu-id="e523e-139">Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores).</span><span class="sxs-lookup"><span data-stu-id="e523e-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="e523e-140">Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e523e-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="e523e-141">También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.</span><span class="sxs-lookup"><span data-stu-id="e523e-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e523e-142">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="e523e-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="e523e-143">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="e523e-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="e523e-144">Para detectar que se presionó la tecla ALT, compruebe si [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) con el **\_ menú VK** < 0.</span><span class="sxs-lookup"><span data-stu-id="e523e-144">To detect that the ALT key was pressed, check whether [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) with **VK\_MENU** < 0.</span></span> <span data-ttu-id="e523e-145">Tenga en cuenta que no debe ser [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="e523e-145">Note, this must not be [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span></span>

## <a name="requirements"></a><span data-ttu-id="e523e-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e523e-146">Requirements</span></span>



| <span data-ttu-id="e523e-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="e523e-147">Requirement</span></span> | <span data-ttu-id="e523e-148">Value</span><span class="sxs-lookup"><span data-stu-id="e523e-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e523e-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e523e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="e523e-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e523e-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e523e-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e523e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="e523e-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e523e-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e523e-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e523e-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="e523e-154"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e523e-154"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e523e-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="e523e-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="e523e-156">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e523e-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e523e-157">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="e523e-157">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="e523e-158">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="e523e-158">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="e523e-159">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="e523e-159">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="e523e-160">**GetKeyState**</span><span class="sxs-lookup"><span data-stu-id="e523e-160">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
</dt> <dt>

[<span data-ttu-id="e523e-161">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="e523e-161">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="e523e-162">**LBUTTONDBLCLK de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e523e-162">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="e523e-163">**LBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e523e-163">**WM\_LBUTTONUP**</span></span>](wm-lbuttonup.md)
</dt> <dt>

<span data-ttu-id="e523e-164">**Vista**</span><span class="sxs-lookup"><span data-stu-id="e523e-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e523e-165">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="e523e-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="e523e-166">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="e523e-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e523e-167">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="e523e-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="e523e-168">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e523e-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

