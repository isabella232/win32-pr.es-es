---
title: Mensaje de WM_CTLCOLORSCROLLBAR (Winuser. h)
description: El \_ mensaje de CTLCOLORSCROLLBAR de WM se envía a la ventana primaria de un control de barra de desplazamiento cuando el control está a punto de dibujarse.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- WM_CTLCOLORSCROLLBAR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f8282e8e15bf1d1a668e1f57e17048f0babac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996328"
---
# <a name="wm_ctlcolorscrollbar-message"></a><span data-ttu-id="4183f-104">Mensaje de CTLCOLORSCROLLBAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="4183f-104">WM\_CTLCOLORSCROLLBAR message</span></span>

<span data-ttu-id="4183f-105">El mensaje de **\_ CTLCOLORSCROLLBAR de WM** se envía a la ventana primaria de un control de barra de desplazamiento cuando el control está a punto de dibujarse.</span><span class="sxs-lookup"><span data-stu-id="4183f-105">The **WM\_CTLCOLORSCROLLBAR** message is sent to the parent window of a scroll bar control when the control is about to be drawn.</span></span> <span data-ttu-id="4183f-106">Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de presentación para establecer el color de fondo del control de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="4183f-106">By responding to this message, the parent window can use the display context handle to set the background color of the scroll bar control.</span></span>

<span data-ttu-id="4183f-107">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4183f-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4183f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4183f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4183f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4183f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4183f-110">Identificador del contexto de dispositivo para el control de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="4183f-110">Handle to the device context for the scroll bar control.</span></span>

</dd> <dt>

<span data-ttu-id="4183f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4183f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4183f-112">Identificador de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="4183f-112">Handle to the scroll bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4183f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4183f-113">Return value</span></span>

<span data-ttu-id="4183f-114">Si una aplicación procesa este mensaje, debe devolver el identificador a un pincel.</span><span class="sxs-lookup"><span data-stu-id="4183f-114">If an application processes this message, it must return the handle to a brush.</span></span> <span data-ttu-id="4183f-115">El sistema utiliza el pincel para pintar el fondo del control de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="4183f-115">The system uses the brush to paint the background of the scroll bar control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4183f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4183f-116">Remarks</span></span>

<span data-ttu-id="4183f-117">Si la aplicación devuelve un pincel que creó (por ejemplo, mediante la función [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), la aplicación debe liberar el pincel.</span><span class="sxs-lookup"><span data-stu-id="4183f-117">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="4183f-118">Si la aplicación devuelve un pincel del sistema (por ejemplo, uno recuperado por la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), no es necesario que la aplicación libere el pincel.</span><span class="sxs-lookup"><span data-stu-id="4183f-118">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="4183f-119">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el control de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="4183f-119">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the scroll bar control.</span></span>

<span data-ttu-id="4183f-120">El mensaje de **\_ CTLCOLORSCROLLBAR de WM** nunca se envía entre subprocesos; solo se envía dentro del mismo subproceso.</span><span class="sxs-lookup"><span data-stu-id="4183f-120">The **WM\_CTLCOLORSCROLLBAR** message is never sent between threads; it is only sent within the same thread.</span></span>

<span data-ttu-id="4183f-121">Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado a **int \_ ptr** y devolver el valor directamente.</span><span class="sxs-lookup"><span data-stu-id="4183f-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="4183f-122">Si el procedimiento del cuadro de diálogo devuelve **false**, se realiza el control de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4183f-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="4183f-123">\_Se omite el valor de DWL MSGRESULT establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="4183f-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="4183f-124">El **mensaje \_ CTLCOLORSCROLLBAR de WM** solo lo usan los controles de barra de desplazamiento secundarios.</span><span class="sxs-lookup"><span data-stu-id="4183f-124">The **WM\_CTLCOLORSCROLLBAR** message is used only by child scroll bar controls.</span></span> <span data-ttu-id="4183f-125">Las barras de desplazamiento adjuntas a una ventana (WS \_ Scroll y WS \_ VSCROLL) no generan este mensaje.</span><span class="sxs-lookup"><span data-stu-id="4183f-125">Scrollbars attached to a window (WS\_SCROLL and WS\_VSCROLL) do not generate this message.</span></span> <span data-ttu-id="4183f-126">Para personalizar la apariencia de las barras de desplazamiento asociadas a una ventana, use las funciones de barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="4183f-126">To customize the appearance of scrollbars attached to a window, use the flat scroll bar functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4183f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4183f-127">Requirements</span></span>



| <span data-ttu-id="4183f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4183f-128">Requirement</span></span> | <span data-ttu-id="4183f-129">Value</span><span class="sxs-lookup"><span data-stu-id="4183f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4183f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4183f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4183f-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4183f-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4183f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4183f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4183f-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4183f-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4183f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4183f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4183f-135"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4183f-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4183f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="4183f-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="4183f-137">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="4183f-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4183f-138">**CTLCOLORBTN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4183f-138">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="4183f-139">**CTLCOLOREDIT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4183f-139">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="4183f-140">**CTLCOLORLISTBOX de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4183f-140">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="4183f-141">**CTLCOLORSTATIC de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4183f-141">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="4183f-142">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="4183f-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4183f-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="4183f-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="4183f-144">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="4183f-144">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="4183f-145">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="4183f-145">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="4183f-146">**CTLCOLORDLG de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4183f-146">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

