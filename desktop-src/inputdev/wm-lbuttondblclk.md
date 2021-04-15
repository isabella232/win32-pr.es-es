---
title: Mensaje de WM_LBUTTONDBLCLK (Winuser. h)
description: Se envía cuando el usuario hace doble clic en el botón primario del mouse mientras el cursor se encuentra en el área cliente de una ventana.
ms.assetid: 370aa19e-4939-4ac3-9c0b-137a9792e52a
keywords:
- Entrada de mouse y teclado de mensaje de WM_LBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_LBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd91eef026ae027e183b4f304211915e7bbbd95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695906"
---
# <a name="wm_lbuttondblclk-message"></a><span data-ttu-id="d5113-104">Mensaje de LBUTTONDBLCLK de WM \_</span><span class="sxs-lookup"><span data-stu-id="d5113-104">WM\_LBUTTONDBLCLK message</span></span>

<span data-ttu-id="d5113-105">Se envía cuando el usuario hace doble clic en el botón primario del mouse mientras el cursor se encuentra en el área cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="d5113-105">Posted when the user double-clicks the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="d5113-106">Si no se captura el mouse, el mensaje se envía a la ventana debajo del cursor.</span><span class="sxs-lookup"><span data-stu-id="d5113-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="d5113-107">De lo contrario, el mensaje se envía a la ventana que ha capturado el mouse.</span><span class="sxs-lookup"><span data-stu-id="d5113-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="d5113-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d5113-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONDBLCLK                0x0203
```



## <a name="parameters"></a><span data-ttu-id="d5113-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5113-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5113-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5113-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5113-111">Indica si varias claves virtuales están inactivas.</span><span class="sxs-lookup"><span data-stu-id="d5113-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="d5113-112">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d5113-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="d5113-113">Value</span><span class="sxs-lookup"><span data-stu-id="d5113-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="d5113-114">Significado</span><span class="sxs-lookup"><span data-stu-id="d5113-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="d5113-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de control</span><span class="sxs-lookup"><span data-stu-id="d5113-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="d5113-116">La tecla CTRL está presionada.</span><span class="sxs-lookup"><span data-stu-id="d5113-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="d5113-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="d5113-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="d5113-118">El botón primario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="d5113-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="d5113-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="d5113-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="d5113-120">El botón central del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="d5113-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="d5113-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="d5113-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="d5113-122">El botón secundario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="d5113-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="d5113-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="d5113-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="d5113-124">La tecla Mayús está presionada.</span><span class="sxs-lookup"><span data-stu-id="d5113-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="d5113-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="d5113-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="d5113-126">El primer botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="d5113-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="d5113-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="d5113-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="d5113-128">El segundo botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="d5113-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="d5113-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5113-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5113-130">La palabra de orden inferior especifica la coordenada x del cursor.</span><span class="sxs-lookup"><span data-stu-id="d5113-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="d5113-131">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="d5113-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="d5113-132">La palabra de orden superior especifica la coordenada y del cursor.</span><span class="sxs-lookup"><span data-stu-id="d5113-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="d5113-133">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="d5113-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5113-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5113-134">Return value</span></span>

<span data-ttu-id="d5113-135">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="d5113-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5113-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5113-136">Remarks</span></span>

<span data-ttu-id="d5113-137">Use el código siguiente para obtener la posición horizontal y vertical:</span><span class="sxs-lookup"><span data-stu-id="d5113-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="d5113-138">Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores).</span><span class="sxs-lookup"><span data-stu-id="d5113-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="d5113-139">Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="d5113-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="d5113-140">También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.</span><span class="sxs-lookup"><span data-stu-id="d5113-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5113-141">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="d5113-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="d5113-142">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="d5113-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="d5113-143">Solo las ventanas que tienen el estilo **CS \_ DBLCLKS** pueden recibir mensajes de **WM \_ LBUTTONDBLCLK** , que el sistema genera cada vez que el usuario presiona, suelta y presiona el botón primario del mouse dentro del límite de tiempo de doble clic del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5113-143">Only windows that have the **CS\_DBLCLKS** style can receive **WM\_LBUTTONDBLCLK** messages, which the system generates whenever the user presses, releases, and again presses the left mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="d5113-144">Al hacer doble clic en el botón primario del mouse, se genera una secuencia de cuatro mensajes: [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md), [**WM \_ LBUTTONUP**](wm-lbuttonup.md), **WM \_ LBUTTONDBLCLK** y **WM \_ LBUTTONUP**.</span><span class="sxs-lookup"><span data-stu-id="d5113-144">Double-clicking the left mouse button actually generates a sequence of four messages: [**WM\_LBUTTONDOWN**](wm-lbuttondown.md), [**WM\_LBUTTONUP**](wm-lbuttonup.md), **WM\_LBUTTONDBLCLK**, and **WM\_LBUTTONUP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5113-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5113-145">Requirements</span></span>



| <span data-ttu-id="d5113-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5113-146">Requirement</span></span> | <span data-ttu-id="d5113-147">Value</span><span class="sxs-lookup"><span data-stu-id="d5113-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5113-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5113-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d5113-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d5113-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d5113-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5113-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d5113-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5113-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d5113-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5113-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5113-153"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5113-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5113-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5113-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5113-155">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d5113-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d5113-156">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="d5113-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="d5113-157">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="d5113-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="d5113-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="d5113-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="d5113-159">**GetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="d5113-159">**GetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="d5113-160">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="d5113-160">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="d5113-161">**SetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="d5113-161">**SetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="d5113-162">**LBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d5113-162">**WM\_LBUTTONDOWN**</span></span>](wm-lbuttondown.md)
</dt> <dt>

[<span data-ttu-id="d5113-163">**LBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d5113-163">**WM\_LBUTTONUP**</span></span>](wm-lbuttonup.md)
</dt> <dt>

<span data-ttu-id="d5113-164">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d5113-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d5113-165">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="d5113-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="d5113-166">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="d5113-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d5113-167">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="d5113-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="d5113-168">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5113-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

