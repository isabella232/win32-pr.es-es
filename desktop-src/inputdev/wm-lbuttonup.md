---
title: WM_LBUTTONUP mensaje (Winuser.h)
description: Se publica cuando el usuario suelta el botón primario del mouse mientras el cursor está en el área cliente de una ventana.
ms.assetid: 6efa298f-85f7-40ab-a64b-16b5071f2437
keywords:
- WM_LBUTTONUP entrada de teclado y mouse
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
ms.openlocfilehash: 7fe921ffe68359efe15aa0782c5c8543fd0870fa
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335399"
---
# <a name="wm_lbuttonup-message"></a><span data-ttu-id="49988-104">Mensaje \_ LBUTTONUP de WM</span><span class="sxs-lookup"><span data-stu-id="49988-104">WM\_LBUTTONUP message</span></span>

<span data-ttu-id="49988-105">Se publica cuando el usuario suelta el botón primario del mouse mientras el cursor está en el área cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="49988-105">Posted when the user releases the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="49988-106">Si no se captura el mouse, el mensaje se publica en la ventana debajo del cursor.</span><span class="sxs-lookup"><span data-stu-id="49988-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="49988-107">De lo contrario, el mensaje se publica en la ventana que ha capturado el mouse.</span><span class="sxs-lookup"><span data-stu-id="49988-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="49988-108">Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="49988-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONUP                    0x0202
```



## <a name="parameters"></a><span data-ttu-id="49988-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49988-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49988-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49988-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49988-111">Indica si varias claves virtuales están sin servicio.</span><span class="sxs-lookup"><span data-stu-id="49988-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="49988-112">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="49988-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="49988-113">Valor</span><span class="sxs-lookup"><span data-stu-id="49988-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="49988-114">Significado</span><span class="sxs-lookup"><span data-stu-id="49988-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="49988-115"><dt>**MK \_ Control**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="49988-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="49988-116">La tecla CTRL está presionada.</span><span class="sxs-lookup"><span data-stu-id="49988-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="49988-117"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="49988-117"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="49988-118">El botón central del mouse está apagado.</span><span class="sxs-lookup"><span data-stu-id="49988-118">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="49988-119"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="49988-119"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="49988-120">El botón derecho del mouse está apagado.</span><span class="sxs-lookup"><span data-stu-id="49988-120">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="49988-121"><dt>**MK \_ Mayús**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="49988-121"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="49988-122">La tecla MAYÚS está abajo.</span><span class="sxs-lookup"><span data-stu-id="49988-122">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="49988-123"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="49988-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="49988-124">El primer botón X está apagado.</span><span class="sxs-lookup"><span data-stu-id="49988-124">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="49988-125"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="49988-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="49988-126">El segundo botón X está apagado.</span><span class="sxs-lookup"><span data-stu-id="49988-126">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="49988-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49988-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49988-128">La palabra de orden bajo especifica la coordenada x del cursor.</span><span class="sxs-lookup"><span data-stu-id="49988-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="49988-129">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="49988-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="49988-130">La palabra de orden superior especifica la coordenada y del cursor.</span><span class="sxs-lookup"><span data-stu-id="49988-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="49988-131">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="49988-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49988-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49988-132">Return value</span></span>

<span data-ttu-id="49988-133">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="49988-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="49988-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49988-134">Remarks</span></span>

<span data-ttu-id="49988-135">Use el código siguiente para obtener la posición horizontal y vertical:</span><span class="sxs-lookup"><span data-stu-id="49988-135">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="49988-136">Como se indicó anteriormente, la coordenada x está en el orden bajo **corto** del valor lParam; la coordenada y está en el  orden corto de orden superior **(ambos** representan valores con signo porque pueden tomar valores negativos en sistemas con varios monitores).</span><span class="sxs-lookup"><span data-stu-id="49988-136">As noted above, the x-coordinate is in the low-order **short** of the lParam value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="49988-137">Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**POINTS**](/previous-versions//dd162808(v=vs.85)) del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="49988-137">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="49988-138">También puede usar la macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.</span><span class="sxs-lookup"><span data-stu-id="49988-138">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49988-139">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y- de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="49988-139">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="49988-140">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="49988-140">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49988-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49988-141">Requirements</span></span>



| <span data-ttu-id="49988-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="49988-142">Requirement</span></span> | <span data-ttu-id="49988-143">Valor</span><span class="sxs-lookup"><span data-stu-id="49988-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49988-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49988-144">Minimum supported client</span></span><br/> | <span data-ttu-id="49988-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="49988-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="49988-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49988-146">Minimum supported server</span></span><br/> | <span data-ttu-id="49988-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="49988-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="49988-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49988-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="49988-149"><dt>Winuser.h (incluir Windowsx.h)</dt></span><span class="sxs-lookup"><span data-stu-id="49988-149"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49988-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="49988-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="49988-151">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="49988-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="49988-152">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="49988-152">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="49988-153">**GET \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="49988-153">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="49988-154">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="49988-154">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="49988-155">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="49988-155">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="49988-156">**WM \_ LBUTTONDBLCLK**</span><span class="sxs-lookup"><span data-stu-id="49988-156">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="49988-157">**WM \_ LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="49988-157">**WM\_LBUTTONDOWN**</span></span>](wm-lbuttondown.md)
</dt> <dt>

<span data-ttu-id="49988-158">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="49988-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="49988-159">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="49988-159">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="49988-160">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="49988-160">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="49988-161">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="49988-161">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="49988-162">[**Puntos**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="49988-162">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

