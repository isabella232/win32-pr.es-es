---
title: Mensaje de WM_MOUSEHOVER (Winuser. h)
description: Se envía a una ventana cuando el cursor se mantiene sobre el área cliente de la ventana durante el período de tiempo especificado en una llamada anterior a TrackMouseEvent.
ms.assetid: efba7f04-2d26-44f1-89df-a565c03ad944
keywords:
- Entrada de mouse y teclado de mensaje de WM_MOUSEHOVER
topic_type:
- apiref
api_name:
- WM_MOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65747ade6bd2ec9456281ac02711de18675a411e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490037"
---
# <a name="wm_mousehover-message"></a><span data-ttu-id="fb600-104">Mensaje de MOUSEHOVER de WM \_</span><span class="sxs-lookup"><span data-stu-id="fb600-104">WM\_MOUSEHOVER message</span></span>

<span data-ttu-id="fb600-105">Se envía a una ventana cuando el cursor se mantiene sobre el área cliente de la ventana durante el período de tiempo especificado en una llamada anterior a [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="fb600-105">Posted to a window when the cursor hovers over the client area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="fb600-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fb600-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEHOVER                   0x02A1
```



## <a name="parameters"></a><span data-ttu-id="fb600-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb600-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb600-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb600-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb600-109">Indica si varias claves virtuales están inactivas.</span><span class="sxs-lookup"><span data-stu-id="fb600-109">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="fb600-110">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fb600-110">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="fb600-111">Value</span><span class="sxs-lookup"><span data-stu-id="fb600-111">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="fb600-112">Significado</span><span class="sxs-lookup"><span data-stu-id="fb600-112">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="fb600-113"><dt>**MK \_**</dt> <dt>0X0008</dt> de control</span><span class="sxs-lookup"><span data-stu-id="fb600-113"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="fb600-114">La tecla CTRL está presionada.</span><span class="sxs-lookup"><span data-stu-id="fb600-114">The CTRL key is depressed.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="fb600-115"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="fb600-115"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="fb600-116">Se presiona el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="fb600-116">The left mouse button is depressed.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="fb600-117"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="fb600-117"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="fb600-118">Se presiona el botón central del mouse.</span><span class="sxs-lookup"><span data-stu-id="fb600-118">The middle mouse button is depressed.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="fb600-119"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="fb600-119"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="fb600-120">Se presiona el botón secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="fb600-120">The right mouse button is depressed.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="fb600-121"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="fb600-121"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="fb600-122">La tecla Mayús está presionada.</span><span class="sxs-lookup"><span data-stu-id="fb600-122">The SHIFT key is depressed.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="fb600-123"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="fb600-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="fb600-124">El primer botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="fb600-124">The first X button is down.</span></span><br/>           |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="fb600-125"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="fb600-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="fb600-126">El segundo botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="fb600-126">The second X button is down.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="fb600-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb600-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb600-128">La palabra de orden inferior especifica la coordenada x del cursor.</span><span class="sxs-lookup"><span data-stu-id="fb600-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="fb600-129">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="fb600-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="fb600-130">La palabra de orden superior especifica la coordenada y del cursor.</span><span class="sxs-lookup"><span data-stu-id="fb600-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="fb600-131">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="fb600-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb600-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb600-132">Return value</span></span>

<span data-ttu-id="fb600-133">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="fb600-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb600-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb600-134">Remarks</span></span>

<span data-ttu-id="fb600-135">El seguimiento de desplazamiento se detiene cuando se genera **\_ MOUSEHOVER de WM** .</span><span class="sxs-lookup"><span data-stu-id="fb600-135">Hover tracking stops when **WM\_MOUSEHOVER** is generated.</span></span> <span data-ttu-id="fb600-136">La aplicación debe volver a llamar a [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) si requiere un seguimiento adicional del comportamiento de desplazamiento del mouse.</span><span class="sxs-lookup"><span data-stu-id="fb600-136">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="fb600-137">Use el código siguiente para obtener la posición horizontal y vertical:</span><span class="sxs-lookup"><span data-stu-id="fb600-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="fb600-138">Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores).</span><span class="sxs-lookup"><span data-stu-id="fb600-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="fb600-139">Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="fb600-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="fb600-140">También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.</span><span class="sxs-lookup"><span data-stu-id="fb600-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb600-141">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="fb600-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="fb600-142">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="fb600-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb600-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb600-143">Requirements</span></span>



| <span data-ttu-id="fb600-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb600-144">Requirement</span></span> | <span data-ttu-id="fb600-145">Value</span><span class="sxs-lookup"><span data-stu-id="fb600-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb600-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb600-146">Minimum supported client</span></span><br/> | <span data-ttu-id="fb600-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fb600-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fb600-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb600-148">Minimum supported server</span></span><br/> | <span data-ttu-id="fb600-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fb600-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fb600-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb600-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb600-151"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb600-151"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb600-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb600-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="fb600-153">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="fb600-153">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fb600-154">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="fb600-154">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="fb600-155">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="fb600-155">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="fb600-156">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="fb600-156">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="fb600-157">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="fb600-157">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="fb600-158">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="fb600-158">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="fb600-159">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="fb600-159">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

<span data-ttu-id="fb600-160">**Vista**</span><span class="sxs-lookup"><span data-stu-id="fb600-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fb600-161">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="fb600-161">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="fb600-162">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="fb600-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="fb600-163">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="fb600-163">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="fb600-164">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fb600-164">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

