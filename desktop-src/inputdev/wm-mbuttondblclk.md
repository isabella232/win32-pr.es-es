---
title: Mensaje de WM_MBUTTONDBLCLK (Winuser. h)
description: Se envía cuando el usuario hace doble clic en el botón central del mouse mientras el cursor se encuentra en el área cliente de una ventana.
ms.assetid: 97167941-93bc-4b83-adff-8ca7a3b2591e
keywords:
- Entrada de mouse y teclado de mensaje de WM_MBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_MBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9dd012051e9845fa2de608725f0f8b6af38334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533999"
---
# <a name="wm_mbuttondblclk-message"></a><span data-ttu-id="f884d-104">Mensaje de MBUTTONDBLCLK de WM \_</span><span class="sxs-lookup"><span data-stu-id="f884d-104">WM\_MBUTTONDBLCLK message</span></span>

<span data-ttu-id="f884d-105">Se envía cuando el usuario hace doble clic en el botón central del mouse mientras el cursor se encuentra en el área cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="f884d-105">Posted when the user double-clicks the middle mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="f884d-106">Si no se captura el mouse, el mensaje se envía a la ventana debajo del cursor.</span><span class="sxs-lookup"><span data-stu-id="f884d-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="f884d-107">De lo contrario, el mensaje se envía a la ventana que ha capturado el mouse.</span><span class="sxs-lookup"><span data-stu-id="f884d-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="f884d-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f884d-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MBUTTONDBLCLK                0x0209
```



## <a name="parameters"></a><span data-ttu-id="f884d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f884d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f884d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f884d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f884d-111">Indica si varias claves virtuales están inactivas.</span><span class="sxs-lookup"><span data-stu-id="f884d-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="f884d-112">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f884d-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="f884d-113">Value</span><span class="sxs-lookup"><span data-stu-id="f884d-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="f884d-114">Significado</span><span class="sxs-lookup"><span data-stu-id="f884d-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="f884d-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de control</span><span class="sxs-lookup"><span data-stu-id="f884d-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="f884d-116">La tecla CTRL está presionada.</span><span class="sxs-lookup"><span data-stu-id="f884d-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="f884d-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="f884d-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="f884d-118">El botón primario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="f884d-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="f884d-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="f884d-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="f884d-120">El botón central del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="f884d-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="f884d-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="f884d-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="f884d-122">El botón secundario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="f884d-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="f884d-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="f884d-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="f884d-124">La tecla Mayús está presionada.</span><span class="sxs-lookup"><span data-stu-id="f884d-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="f884d-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="f884d-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="f884d-126">El primer botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="f884d-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="f884d-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="f884d-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="f884d-128">El segundo botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="f884d-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="f884d-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f884d-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f884d-130">La palabra de orden inferior especifica la coordenada x del cursor.</span><span class="sxs-lookup"><span data-stu-id="f884d-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="f884d-131">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="f884d-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="f884d-132">La palabra de orden superior especifica la coordenada y del cursor.</span><span class="sxs-lookup"><span data-stu-id="f884d-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="f884d-133">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="f884d-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f884d-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f884d-134">Return value</span></span>

<span data-ttu-id="f884d-135">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="f884d-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f884d-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f884d-136">Remarks</span></span>

<span data-ttu-id="f884d-137">Use el código siguiente para obtener la posición horizontal y vertical:</span><span class="sxs-lookup"><span data-stu-id="f884d-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="f884d-138">Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores).</span><span class="sxs-lookup"><span data-stu-id="f884d-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="f884d-139">Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f884d-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="f884d-140">También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.</span><span class="sxs-lookup"><span data-stu-id="f884d-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f884d-141">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="f884d-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="f884d-142">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="f884d-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="f884d-143">Solo las ventanas que tienen el estilo **CS \_ DBLCLKS** pueden recibir mensajes de **WM \_ MBUTTONDBLCLK** , que el sistema genera cuando el usuario presiona, suelta y presiona el botón central del mouse dentro del límite de tiempo de doble clic del sistema.</span><span class="sxs-lookup"><span data-stu-id="f884d-143">Only windows that have the **CS\_DBLCLKS** style can receive **WM\_MBUTTONDBLCLK** messages, which the system generates when the user presses, releases, and again presses the middle mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="f884d-144">Al hacer doble clic en el botón central del mouse, se generan cuatro mensajes: [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md), [**WM \_ MBUTTONUP**](wm-mbuttonup.md), **WM \_ MBUTTONDBLCLK** y **WM \_ MBUTTONUP** de nuevo.</span><span class="sxs-lookup"><span data-stu-id="f884d-144">Double-clicking the middle mouse button actually generates four messages: [**WM\_MBUTTONDOWN**](wm-mbuttondown.md), [**WM\_MBUTTONUP**](wm-mbuttonup.md), **WM\_MBUTTONDBLCLK**, and **WM\_MBUTTONUP** again.</span></span>

## <a name="requirements"></a><span data-ttu-id="f884d-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f884d-145">Requirements</span></span>



| <span data-ttu-id="f884d-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f884d-146">Requirement</span></span> | <span data-ttu-id="f884d-147">Value</span><span class="sxs-lookup"><span data-stu-id="f884d-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f884d-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f884d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f884d-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f884d-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f884d-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f884d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f884d-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f884d-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f884d-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f884d-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="f884d-153"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f884d-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f884d-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="f884d-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="f884d-155">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f884d-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f884d-156">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="f884d-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="f884d-157">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="f884d-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="f884d-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="f884d-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="f884d-159">**GetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="f884d-159">**GetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="f884d-160">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="f884d-160">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="f884d-161">**SetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="f884d-161">**SetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="f884d-162">**MBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f884d-162">**WM\_MBUTTONDOWN**</span></span>](wm-mbuttondown.md)
</dt> <dt>

[<span data-ttu-id="f884d-163">**MBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f884d-163">**WM\_MBUTTONUP**</span></span>](wm-mbuttonup.md)
</dt> <dt>

<span data-ttu-id="f884d-164">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f884d-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f884d-165">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="f884d-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="f884d-166">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="f884d-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f884d-167">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="f884d-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="f884d-168">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f884d-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

