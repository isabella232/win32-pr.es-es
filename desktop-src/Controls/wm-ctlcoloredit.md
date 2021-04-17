---
title: Mensaje de WM_CTLCOLOREDIT (Winuser. h)
description: Un control de edición que no es de solo lectura o está deshabilitado envía el mensaje de CTLCOLOREDIT de WM \_ a su ventana primaria cuando el control está a punto de dibujarse.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- WM_CTLCOLOREDIT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489004"
---
# <a name="wm_ctlcoloredit-message"></a><span data-ttu-id="a8bb7-104">Mensaje de CTLCOLOREDIT de WM \_</span><span class="sxs-lookup"><span data-stu-id="a8bb7-104">WM\_CTLCOLOREDIT message</span></span>

<span data-ttu-id="a8bb7-105">Un control de edición que no es de solo lectura o está deshabilitado envía el mensaje de **\_ CTLCOLOREDIT de WM** a su ventana primaria cuando el control está a punto de dibujarse.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-105">An edit control that is not read-only or disabled sends the **WM\_CTLCOLOREDIT** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="a8bb7-106">Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de dispositivo especificado para establecer los colores de texto y de fondo del control de edición.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-106">By responding to this message, the parent window can use the specified device context handle to set the text and background colors of the edit control.</span></span>


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a8bb7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8bb7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8bb7-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8bb7-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8bb7-109">Identificador del contexto de dispositivo para la ventana de control de edición.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-109">A handle to the device context for the edit control window.</span></span>

</dd> <dt>

<span data-ttu-id="a8bb7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8bb7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8bb7-111">Identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-111">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8bb7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8bb7-112">Return value</span></span>

<span data-ttu-id="a8bb7-113">Si una aplicación procesa este mensaje, debe devolver el identificador de un pincel.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-113">If an application processes this message, it must return the handle of a brush.</span></span> <span data-ttu-id="a8bb7-114">El sistema utiliza el pincel para pintar el fondo del control de edición.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-114">The system uses the brush to paint the background of the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8bb7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8bb7-115">Remarks</span></span>

<span data-ttu-id="a8bb7-116">Si la aplicación devuelve un pincel que creó (por ejemplo, mediante la función [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), la aplicación debe liberar el pincel.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="a8bb7-117">Si la aplicación devuelve un pincel del sistema (por ejemplo, uno recuperado por la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), no es necesario que la aplicación libere el pincel.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="a8bb7-118">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el control de edición.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the edit control.</span></span>

<span data-ttu-id="a8bb7-119">Los controles de edición de solo lectura o deshabilitados no envían el mensaje de **\_ CTLCOLOREDIT de WM** ; en su lugar, envían el mensaje de [**\_ CTLCOLORSTATIC de WM**](wm-ctlcolorstatic.md) .</span><span class="sxs-lookup"><span data-stu-id="a8bb7-119">Read-only or disabled edit controls do not send the **WM\_CTLCOLOREDIT** message; instead, they send the [**WM\_CTLCOLORSTATIC**](wm-ctlcolorstatic.md) message.</span></span>

<span data-ttu-id="a8bb7-120">El mensaje de **\_ CTLCOLOREDIT de WM** nunca se envía entre subprocesos, solo se envía dentro del mismo subproceso.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-120">The **WM\_CTLCOLOREDIT** message is never sent between threads, it is only sent within the same thread.</span></span>

<span data-ttu-id="a8bb7-121">Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado a **int \_ ptr** y devolver el valor directamente.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="a8bb7-122">Si el procedimiento del cuadro de diálogo devuelve **false**, se realiza el control de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="a8bb7-123">\_Se omite el valor de DWL MSGRESULT establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="a8bb7-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="a8bb7-124">**Edición enriquecida:** Este mensaje no se admite.</span><span class="sxs-lookup"><span data-stu-id="a8bb7-124">**Rich Edit:** This message is not supported.</span></span> <span data-ttu-id="a8bb7-125">Para establecer el color de fondo de un control Rich Edit, utilice el mensaje [**\_ SETBKGNDCOLOR em**](em-setbkgndcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="a8bb7-125">To set the background color for a rich edit control, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8bb7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8bb7-126">Requirements</span></span>



| <span data-ttu-id="a8bb7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8bb7-127">Requirement</span></span> | <span data-ttu-id="a8bb7-128">Value</span><span class="sxs-lookup"><span data-stu-id="a8bb7-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bb7-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8bb7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a8bb7-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a8bb7-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8bb7-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8bb7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a8bb7-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8bb7-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8bb7-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8bb7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8bb7-134"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8bb7-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8bb7-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8bb7-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8bb7-136">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a8bb7-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a8bb7-137">**\_SETBKGNDCOLOR em**</span><span class="sxs-lookup"><span data-stu-id="a8bb7-137">**EM\_SETBKGNDCOLOR**</span></span>](em-setbkgndcolor.md)
</dt> <dt>

[<span data-ttu-id="a8bb7-138">**CTLCOLORSTATIC de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a8bb7-138">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="a8bb7-139">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="a8bb7-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a8bb7-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="a8bb7-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="a8bb7-141">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="a8bb7-141">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="a8bb7-142">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="a8bb7-142">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

