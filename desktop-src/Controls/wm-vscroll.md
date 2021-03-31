---
title: Mensaje de WM_VSCROLL (Winuser. h)
description: El mensaje de VSCROLL de WM \_ se envía a una ventana cuando se produce un evento de desplazamiento en la barra de desplazamiento vertical estándar de la ventana.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- WM_VSCROLL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c83888b83e0d5f8d3c77775347ccc9b43a59d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151110"
---
# <a name="wm_vscroll-message"></a><span data-ttu-id="ebe6d-104">Mensaje de VSCROLL de WM \_</span><span class="sxs-lookup"><span data-stu-id="ebe6d-104">WM\_VSCROLL message</span></span>

<span data-ttu-id="ebe6d-105">El mensaje de **\_ VSCROLL de WM** se envía a una ventana cuando se produce un evento de desplazamiento en la barra de desplazamiento vertical estándar de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-105">The **WM\_VSCROLL** message is sent to a window when a scroll event occurs in the window's standard vertical scroll bar.</span></span> <span data-ttu-id="ebe6d-106">Este mensaje también se envía al propietario de un control de barra de desplazamiento vertical cuando se produce un evento de desplazamiento en el control.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-106">This message is also sent to the owner of a vertical scroll bar control when a scroll event occurs in the control.</span></span>

<span data-ttu-id="ebe6d-107">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ebe6d-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ebe6d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ebe6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebe6d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebe6d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebe6d-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición actual del cuadro de desplazamiento si [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es SB \_ THUMBPOSITION o SB \_ THUMBTRACK; de lo contrario, esta palabra no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the scroll box if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is SB\_THUMBPOSITION or SB\_THUMBTRACK; otherwise, this word is not used.</span></span>

<span data-ttu-id="ebe6d-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica un valor de la barra de desplazamiento que indica la solicitud de desplazamiento del usuario.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a scroll bar value that indicates the user's scrolling request.</span></span> <span data-ttu-id="ebe6d-112">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ebe6d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ebe6d-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="ebe6d-114">Significado</span><span class="sxs-lookup"><span data-stu-id="ebe6d-114">Meaning</span></span>                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="ebe6d-115"><dt>**SB \_ inferior**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe6d-115"><dt>**SB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="ebe6d-116">Se desplaza a la parte inferior derecha.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-116">Scrolls to the lower right.</span></span><br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="ebe6d-117"><dt>**SB \_ ENDSCROLL**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe6d-117"><dt>**SB\_ENDSCROLL**</dt></span></span> </dl>             | <span data-ttu-id="ebe6d-118">Finaliza el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-118">Ends scroll.</span></span><br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="ebe6d-119"><dt>**SB \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe6d-119"><dt>**SB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="ebe6d-120">Desplaza una línea hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-120">Scrolls one line down.</span></span><br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="ebe6d-121"><dt>**\_línea SB**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe6d-121"><dt>**SB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="ebe6d-122">Desplaza una línea hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-122">Scrolls one line up.</span></span><br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="ebe6d-123"><dt>**reavpág SB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe6d-123"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="ebe6d-124">Desplaza una página hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-124">Scrolls one page down.</span></span><br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="ebe6d-125"><dt>**\_Re Pág de SB**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe6d-125"><dt>**SB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="ebe6d-126">Desplaza una página hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-126">Scrolls one page up.</span></span><br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="ebe6d-127"><dt>**SB \_ THUMBPOSITION**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe6d-127"><dt>**SB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="ebe6d-128">El usuario ha arrastrado el cuadro de desplazamiento (Thumb) y ha soltado el botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-128">The user has dragged the scroll box (thumb) and released the mouse button.</span></span> <span data-ttu-id="ebe6d-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica la posición del cuadro de desplazamiento al final de la operación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-129">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position of the scroll box at the end of the drag operation.</span></span><br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <span data-ttu-id="ebe6d-130"><dt>**SB \_ THUMBTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe6d-130"><dt>**SB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="ebe6d-131">El usuario está arrastrando el cuadro de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-131">The user is dragging the scroll box.</span></span> <span data-ttu-id="ebe6d-132">Este mensaje se envía repetidamente hasta que el usuario suelta el botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-132">This message is sent repeatedly until the user releases the mouse button.</span></span> <span data-ttu-id="ebe6d-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica la posición a la que se ha arrastrado el cuadro de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-133">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position that the scroll box has been dragged to.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="ebe6d-134"><dt>**SB \_ superior**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe6d-134"><dt>**SB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="ebe6d-135">Se desplaza a la parte superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-135">Scrolls to the upper left.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="ebe6d-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebe6d-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebe6d-137">Si el mensaje se envía mediante un control de barra de desplazamiento, este parámetro es el identificador del control de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-137">If the message is sent by a scroll bar control, this parameter is the handle to the scroll bar control.</span></span> <span data-ttu-id="ebe6d-138">Si el mensaje se envía mediante una barra de desplazamiento estándar, este parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-138">If the message is sent by a standard scroll bar, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebe6d-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebe6d-139">Return value</span></span>

<span data-ttu-id="ebe6d-140">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-140">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebe6d-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebe6d-141">Remarks</span></span>

<span data-ttu-id="ebe6d-142">El \_ código de solicitud THUMBTRACK de SB lo suelen usar las aplicaciones que proporcionan comentarios cuando el usuario arrastra el cuadro de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-142">The SB\_THUMBTRACK request code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="ebe6d-143">Si una aplicación desplaza el contenido de la ventana, también debe restablecer la posición del cuadro de desplazamiento mediante la función [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="ebe6d-143">If an application scrolls the content of the window, it must also reset the position of the scroll box by using the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span>

<span data-ttu-id="ebe6d-144">Tenga en cuenta que el mensaje de **\_ VSCROLL de WM** solo incluye 16 bits de datos de posición del cuadro de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-144">Note that the **WM\_VSCROLL** message carries only 16 bits of scroll box position data.</span></span> <span data-ttu-id="ebe6d-145">Por lo tanto, las aplicaciones que se basan únicamente en **WM \_ VSCROLL** (y [**WM \_ HSCROLL**](wm-hscroll.md)) para los datos de posición de desplazamiento tienen un valor de posición máximo práctico de 65.535.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-145">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll.md)) for scroll position data have a practical maximum position value of 65,535.</span></span>

<span data-ttu-id="ebe6d-146">Sin embargo, dado que las funciones [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)y [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) admiten datos de posición de la barra de desplazamiento de 32 bits, existe una manera de eludir la barrera de 16 bits de los mensajes de [**WM \_ HSCROLL**](wm-hscroll.md) y **WM \_ VSCROLL** .</span><span class="sxs-lookup"><span data-stu-id="ebe6d-146">However, because the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos), and [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the [**WM\_HSCROLL**](wm-hscroll.md) and **WM\_VSCROLL** messages.</span></span> <span data-ttu-id="ebe6d-147">Consulte **GetScrollInfo** para obtener una descripción de la técnica.</span><span class="sxs-lookup"><span data-stu-id="ebe6d-147">See **GetScrollInfo** for a description of the technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe6d-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebe6d-148">Requirements</span></span>



| <span data-ttu-id="ebe6d-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebe6d-149">Requirement</span></span> | <span data-ttu-id="ebe6d-150">Value</span><span class="sxs-lookup"><span data-stu-id="ebe6d-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe6d-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebe6d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="ebe6d-152">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ebe6d-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ebe6d-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebe6d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="ebe6d-154">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ebe6d-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ebe6d-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebe6d-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebe6d-156"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebe6d-156"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe6d-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebe6d-157">See also</span></span>

<dl> <dt>

<span data-ttu-id="ebe6d-158">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ebe6d-158">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ebe6d-159">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="ebe6d-159">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="ebe6d-160">**GetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="ebe6d-160">**GetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[<span data-ttu-id="ebe6d-161">**GetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="ebe6d-161">**GetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[<span data-ttu-id="ebe6d-162">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="ebe6d-162">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[<span data-ttu-id="ebe6d-163">**SetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="ebe6d-163">**SetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[<span data-ttu-id="ebe6d-164">**SetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="ebe6d-164">**SetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[<span data-ttu-id="ebe6d-165">**HSCROLL de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ebe6d-165">**WM\_HSCROLL**</span></span>](wm-hscroll.md)
</dt> <dt>

[<span data-ttu-id="ebe6d-166">**WM \_ VSCROLL (TrackBar)**</span><span class="sxs-lookup"><span data-stu-id="ebe6d-166">**WM\_VSCROLL (Trackbar)**</span></span>](wm-vscroll--trackbar-.md)
</dt> </dl>

 

