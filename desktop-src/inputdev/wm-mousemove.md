---
title: Mensaje de WM_MOUSEMOVE (Winuser. h)
description: Se envía a una ventana cuando el cursor se mueve. Si no se captura el mouse, el mensaje se envía a la ventana que contiene el cursor. De lo contrario, el mensaje se envía a la ventana que ha capturado el mouse.
ms.assetid: 9b99387e-e176-4b20-a05a-bc75928a1367
keywords:
- Entrada de mouse y teclado de mensaje de WM_MOUSEMOVE
topic_type:
- apiref
api_name:
- WM_MOUSEMOVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61ffd10edbd58d11c5667fbda9dc0408ea1d72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533993"
---
# <a name="wm_mousemove-message"></a><span data-ttu-id="11438-106">Mensaje de la MOUSEMOVE de WM \_</span><span class="sxs-lookup"><span data-stu-id="11438-106">WM\_MOUSEMOVE message</span></span>

<span data-ttu-id="11438-107">Se envía a una ventana cuando el cursor se mueve.</span><span class="sxs-lookup"><span data-stu-id="11438-107">Posted to a window when the cursor moves.</span></span> <span data-ttu-id="11438-108">Si no se captura el mouse, el mensaje se envía a la ventana que contiene el cursor.</span><span class="sxs-lookup"><span data-stu-id="11438-108">If the mouse is not captured, the message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="11438-109">De lo contrario, el mensaje se envía a la ventana que ha capturado el mouse.</span><span class="sxs-lookup"><span data-stu-id="11438-109">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="11438-110">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="11438-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEMOVE                    0x0200
```



## <a name="parameters"></a><span data-ttu-id="11438-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11438-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11438-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11438-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11438-113">Indica si varias claves virtuales están inactivas.</span><span class="sxs-lookup"><span data-stu-id="11438-113">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="11438-114">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="11438-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="11438-115">Value</span><span class="sxs-lookup"><span data-stu-id="11438-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="11438-116">Significado</span><span class="sxs-lookup"><span data-stu-id="11438-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="11438-117"><dt>**MK \_**</dt> <dt>0X0008</dt> de control</span><span class="sxs-lookup"><span data-stu-id="11438-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="11438-118">La tecla CTRL está presionada.</span><span class="sxs-lookup"><span data-stu-id="11438-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="11438-119"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="11438-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="11438-120">El botón primario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="11438-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="11438-121"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="11438-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="11438-122">El botón central del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="11438-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="11438-123"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="11438-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="11438-124">El botón secundario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="11438-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="11438-125"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="11438-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="11438-126">La tecla Mayús está presionada.</span><span class="sxs-lookup"><span data-stu-id="11438-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="11438-127"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="11438-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="11438-128">El primer botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="11438-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="11438-129"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="11438-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="11438-130">El segundo botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="11438-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="11438-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11438-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11438-132">La palabra de orden inferior especifica la coordenada x del cursor.</span><span class="sxs-lookup"><span data-stu-id="11438-132">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="11438-133">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="11438-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="11438-134">La palabra de orden superior especifica la coordenada y del cursor.</span><span class="sxs-lookup"><span data-stu-id="11438-134">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="11438-135">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="11438-135">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11438-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11438-136">Return value</span></span>

<span data-ttu-id="11438-137">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="11438-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="11438-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11438-138">Remarks</span></span>

<span data-ttu-id="11438-139">Use el código siguiente para obtener la posición horizontal y vertical:</span><span class="sxs-lookup"><span data-stu-id="11438-139">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="11438-140">Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores).</span><span class="sxs-lookup"><span data-stu-id="11438-140">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="11438-141">Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="11438-141">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="11438-142">También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.</span><span class="sxs-lookup"><span data-stu-id="11438-142">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11438-143">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="11438-143">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="11438-144">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="11438-144">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11438-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11438-145">Requirements</span></span>



| <span data-ttu-id="11438-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="11438-146">Requirement</span></span> | <span data-ttu-id="11438-147">Value</span><span class="sxs-lookup"><span data-stu-id="11438-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11438-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11438-148">Minimum supported client</span></span><br/> | <span data-ttu-id="11438-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="11438-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="11438-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11438-150">Minimum supported server</span></span><br/> | <span data-ttu-id="11438-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="11438-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="11438-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11438-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="11438-153"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11438-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11438-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="11438-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="11438-155">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="11438-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="11438-156">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="11438-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="11438-157">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="11438-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="11438-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="11438-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="11438-159">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="11438-159">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

<span data-ttu-id="11438-160">**Vista**</span><span class="sxs-lookup"><span data-stu-id="11438-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="11438-161">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="11438-161">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="11438-162">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="11438-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="11438-163">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="11438-163">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="11438-164">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="11438-164">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

