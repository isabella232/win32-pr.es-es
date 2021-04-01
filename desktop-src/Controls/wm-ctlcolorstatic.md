---
title: Mensaje de WM_CTLCOLORSTATIC (Winuser. h)
description: Un control estático o un control de edición que sea de solo lectura o deshabilitado, envía el \_ mensaje de CTLCOLORSTATIC de WM a su ventana primaria cuando el control está a punto de dibujarse.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- WM_CTLCOLORSTATIC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851879eeb65a00f95f8cb81cef1b6c23ece8028d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802174"
---
# <a name="wm_ctlcolorstatic-message"></a><span data-ttu-id="e80ac-104">Mensaje de CTLCOLORSTATIC de WM \_</span><span class="sxs-lookup"><span data-stu-id="e80ac-104">WM\_CTLCOLORSTATIC message</span></span>

<span data-ttu-id="e80ac-105">Un control estático o un control de edición que sea de solo lectura o deshabilitado, envía el mensaje de **\_ CTLCOLORSTATIC de WM** a su ventana primaria cuando el control está a punto de dibujarse.</span><span class="sxs-lookup"><span data-stu-id="e80ac-105">A static control, or an edit control that is read-only or disabled, sends the **WM\_CTLCOLORSTATIC** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="e80ac-106">Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de dispositivo especificado para establecer los colores de primer plano y de fondo del texto del control estático.</span><span class="sxs-lookup"><span data-stu-id="e80ac-106">By responding to this message, the parent window can use the specified device context handle to set the text foreground and background colors of the static control.</span></span>

<span data-ttu-id="e80ac-107">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e80ac-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e80ac-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e80ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e80ac-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e80ac-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e80ac-110">Identificador del contexto de dispositivo para la ventana de control estática.</span><span class="sxs-lookup"><span data-stu-id="e80ac-110">Handle to the device context for the static control window.</span></span>

</dd> <dt>

<span data-ttu-id="e80ac-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e80ac-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e80ac-112">Identificador del control estático.</span><span class="sxs-lookup"><span data-stu-id="e80ac-112">Handle to the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e80ac-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e80ac-113">Return value</span></span>

<span data-ttu-id="e80ac-114">Si una aplicación procesa este mensaje, el valor devuelto es un identificador de un pincel que el sistema utiliza para pintar el fondo del control estático.</span><span class="sxs-lookup"><span data-stu-id="e80ac-114">If an application processes this message, the return value is a handle to a brush that the system uses to paint the background of the static control.</span></span>

## <a name="remarks"></a><span data-ttu-id="e80ac-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e80ac-115">Remarks</span></span>

<span data-ttu-id="e80ac-116">Si la aplicación devuelve un pincel que creó (por ejemplo, mediante la función [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), la aplicación debe liberar el pincel.</span><span class="sxs-lookup"><span data-stu-id="e80ac-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="e80ac-117">Si la aplicación devuelve un pincel del sistema (por ejemplo, uno recuperado por la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), no es necesario que la aplicación libere el pincel.</span><span class="sxs-lookup"><span data-stu-id="e80ac-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="e80ac-118">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el control estático.</span><span class="sxs-lookup"><span data-stu-id="e80ac-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the static control.</span></span>

<span data-ttu-id="e80ac-119">Puede establecer el color de fondo del texto de un control de edición deshabilitado, pero no puede establecer el color de primer plano del texto.</span><span class="sxs-lookup"><span data-stu-id="e80ac-119">You can set the text background color of a disabled edit control, but you cannot set the text foreground color.</span></span> <span data-ttu-id="e80ac-120">El sistema siempre usa el COLOR \_ GRAYTEXT.</span><span class="sxs-lookup"><span data-stu-id="e80ac-120">The system always uses COLOR\_GRAYTEXT.</span></span>

<span data-ttu-id="e80ac-121">Los controles de edición que no son de solo lectura o están deshabilitados no envían el mensaje de **WM \_ CTLCOLORSTATIC** ; en su lugar, envían el mensaje de [**\_ CTLCOLOREDIT de WM**](wm-ctlcoloredit.md) .</span><span class="sxs-lookup"><span data-stu-id="e80ac-121">Edit controls that are not read-only or disabled do not send the **WM\_CTLCOLORSTATIC** message; instead, they send the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

<span data-ttu-id="e80ac-122">El mensaje de **\_ CTLCOLORSTATIC de WM** nunca se envía entre subprocesos; solo se envía dentro del mismo subproceso.</span><span class="sxs-lookup"><span data-stu-id="e80ac-122">The **WM\_CTLCOLORSTATIC** message is never sent between threads; it is sent only within the same thread.</span></span>

<span data-ttu-id="e80ac-123">Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado a **int \_ ptr** y devolver el valor directamente.</span><span class="sxs-lookup"><span data-stu-id="e80ac-123">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="e80ac-124">Si el procedimiento del cuadro de diálogo devuelve **false**, se realiza el control de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e80ac-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="e80ac-125">\_Se omite el valor de DWL MSGRESULT establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="e80ac-125">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="e80ac-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e80ac-126">Examples</span></span>

<span data-ttu-id="e80ac-127">En el siguiente ejemplo de C++ se muestra cómo establecer los colores de fondo y de primer plano del texto de un control estático en respuesta al mensaje de **\_ CTLCOLORSTATIC de WM** .</span><span class="sxs-lookup"><span data-stu-id="e80ac-127">The following C++ example shows how to set the text foreground and background colors of a static control in response to the **WM\_CTLCOLORSTATIC** message.</span></span> <span data-ttu-id="e80ac-128">La `hbrBkgnd` variable es una variable **hbrush** estática que se inicializa en NULL y almacena el pincel de fondo entre las llamadas a **WM \_ CTLCOLORSTATIC**.</span><span class="sxs-lookup"><span data-stu-id="e80ac-128">The `hbrBkgnd` variable is a static **HBRUSH** variable that is initialized to NULL, and stores the background brush between calls to **WM\_CTLCOLORSTATIC**.</span></span> <span data-ttu-id="e80ac-129">El pincel se debe destruir mediante una llamada a la función [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) cuando ya no se necesite, normalmente cuando se destruye el cuadro de diálogo asociado.</span><span class="sxs-lookup"><span data-stu-id="e80ac-129">The brush must be destroyed by a call to the [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) function when it is no longer needed, typically when the associated dialog box is destroyed.</span></span>


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



## <a name="requirements"></a><span data-ttu-id="e80ac-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e80ac-130">Requirements</span></span>



| <span data-ttu-id="e80ac-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e80ac-131">Requirement</span></span> | <span data-ttu-id="e80ac-132">Value</span><span class="sxs-lookup"><span data-stu-id="e80ac-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e80ac-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e80ac-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e80ac-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e80ac-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e80ac-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e80ac-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e80ac-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e80ac-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e80ac-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e80ac-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e80ac-138"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e80ac-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e80ac-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="e80ac-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="e80ac-140">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e80ac-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e80ac-141">**CTLCOLORBTN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e80ac-141">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="e80ac-142">**CTLCOLOREDIT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e80ac-142">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="e80ac-143">**CTLCOLORLISTBOX de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e80ac-143">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="e80ac-144">**CTLCOLORSCROLLBAR de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e80ac-144">**WM\_CTLCOLORSCROLLBAR**</span></span>](wm-ctlcolorscrollbar.md)
</dt> <dt>

<span data-ttu-id="e80ac-145">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="e80ac-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e80ac-146">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="e80ac-146">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="e80ac-147">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="e80ac-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="e80ac-148">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="e80ac-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="e80ac-149">**CTLCOLORDLG de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e80ac-149">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

