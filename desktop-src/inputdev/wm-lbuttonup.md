---
title: Mensaje de WM_LBUTTONUP (Winuser. h)
description: Se envía cuando el usuario suelta el botón primario del mouse mientras el cursor está en el área de cliente de una ventana.
ms.assetid: 6efa298f-85f7-40ab-a64b-16b5071f2437
keywords:
- Entrada de mouse y teclado de mensaje de WM_LBUTTONUP
topic_type:
- apiref
api_name:
- WM_LBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960023363f500cdec9752a92524f91837d78ef26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490048"
---
# <a name="wm_lbuttonup-message"></a><span data-ttu-id="032f2-104">Mensaje de LBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="032f2-104">WM\_LBUTTONUP message</span></span>

<span data-ttu-id="032f2-105">Se envía cuando el usuario suelta el botón primario del mouse mientras el cursor está en el área de cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="032f2-105">Posted when the user releases the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="032f2-106">Si no se captura el mouse, el mensaje se envía a la ventana debajo del cursor.</span><span class="sxs-lookup"><span data-stu-id="032f2-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="032f2-107">De lo contrario, el mensaje se envía a la ventana que ha capturado el mouse.</span><span class="sxs-lookup"><span data-stu-id="032f2-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="032f2-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="032f2-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONUP                    0x0202
```



## <a name="parameters"></a><span data-ttu-id="032f2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="032f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="032f2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="032f2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="032f2-111">Indica si varias claves virtuales están inactivas.</span><span class="sxs-lookup"><span data-stu-id="032f2-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="032f2-112">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="032f2-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="032f2-113">Value</span><span class="sxs-lookup"><span data-stu-id="032f2-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="032f2-114">Significado</span><span class="sxs-lookup"><span data-stu-id="032f2-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="032f2-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de control</span><span class="sxs-lookup"><span data-stu-id="032f2-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="032f2-116">La tecla CTRL está presionada.</span><span class="sxs-lookup"><span data-stu-id="032f2-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="032f2-117"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="032f2-117"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="032f2-118">El botón central del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="032f2-118">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="032f2-119"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="032f2-119"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="032f2-120">El botón secundario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="032f2-120">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="032f2-121"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="032f2-121"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="032f2-122">La tecla Mayús está presionada.</span><span class="sxs-lookup"><span data-stu-id="032f2-122">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="032f2-123"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="032f2-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="032f2-124">El primer botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="032f2-124">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="032f2-125"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="032f2-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="032f2-126">El segundo botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="032f2-126">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="032f2-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="032f2-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="032f2-128">La palabra de orden inferior especifica la coordenada x del cursor.</span><span class="sxs-lookup"><span data-stu-id="032f2-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="032f2-129">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="032f2-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="032f2-130">La palabra de orden superior especifica la coordenada y del cursor.</span><span class="sxs-lookup"><span data-stu-id="032f2-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="032f2-131">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="032f2-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="032f2-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="032f2-132">Return value</span></span>

<span data-ttu-id="032f2-133">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="032f2-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="032f2-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="032f2-134">Remarks</span></span>

<span data-ttu-id="032f2-135">Use el código siguiente para obtener la posición horizontal y vertical:</span><span class="sxs-lookup"><span data-stu-id="032f2-135">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="032f2-136">Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores).</span><span class="sxs-lookup"><span data-stu-id="032f2-136">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="032f2-137">Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="032f2-137">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="032f2-138">También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.</span><span class="sxs-lookup"><span data-stu-id="032f2-138">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="032f2-139">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="032f2-139">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="032f2-140">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="032f2-140">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="032f2-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="032f2-141">Requirements</span></span>



| <span data-ttu-id="032f2-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="032f2-142">Requirement</span></span> | <span data-ttu-id="032f2-143">Value</span><span class="sxs-lookup"><span data-stu-id="032f2-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="032f2-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="032f2-144">Minimum supported client</span></span><br/> | <span data-ttu-id="032f2-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="032f2-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="032f2-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="032f2-146">Minimum supported server</span></span><br/> | <span data-ttu-id="032f2-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="032f2-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="032f2-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="032f2-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="032f2-149"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="032f2-149"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="032f2-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="032f2-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="032f2-151">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="032f2-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="032f2-152">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="032f2-152">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="032f2-153">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="032f2-153">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="032f2-154">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="032f2-154">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="032f2-155">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="032f2-155">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="032f2-156">**LBUTTONDBLCLK de WM \_**</span><span class="sxs-lookup"><span data-stu-id="032f2-156">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="032f2-157">**LBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="032f2-157">**WM\_LBUTTONDOWN**</span></span>](wm-lbuttondown.md)
</dt> <dt>

<span data-ttu-id="032f2-158">**Vista**</span><span class="sxs-lookup"><span data-stu-id="032f2-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="032f2-159">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="032f2-159">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="032f2-160">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="032f2-160">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="032f2-161">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="032f2-161">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="032f2-162">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="032f2-162">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

