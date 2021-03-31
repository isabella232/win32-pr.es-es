---
title: Mensaje de WM_CTLCOLORDLG (Winuser. h)
description: Se envía a un cuadro de diálogo antes de que el sistema dibuje el cuadro de diálogo. Al responder a este mensaje, el cuadro de diálogo puede establecer sus colores de texto y de fondo mediante el identificador de contexto de dispositivo de pantalla especificado.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- WM_CTLCOLORDLG cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833d3894a85342b0f26323ceed0f4fb3356c48ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801267"
---
# <a name="wm_ctlcolordlg-message"></a><span data-ttu-id="bd004-105">Mensaje de CTLCOLORDLG de WM \_</span><span class="sxs-lookup"><span data-stu-id="bd004-105">WM\_CTLCOLORDLG message</span></span>

<span data-ttu-id="bd004-106">Se envía a un cuadro de diálogo antes de que el sistema dibuje el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bd004-106">Sent to a dialog box before the system draws the dialog box.</span></span> <span data-ttu-id="bd004-107">Al responder a este mensaje, el cuadro de diálogo puede establecer sus colores de texto y de fondo mediante el identificador de contexto de dispositivo de pantalla especificado.</span><span class="sxs-lookup"><span data-stu-id="bd004-107">By responding to this message, the dialog box can set its text and background colors using the specified display device context handle.</span></span>


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a><span data-ttu-id="bd004-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd004-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd004-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd004-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd004-110">Identificador del contexto de dispositivo para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bd004-110">A handle to the device context for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="bd004-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd004-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd004-112">Identificador del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bd004-112">A handle to the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd004-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd004-113">Return value</span></span>

<span data-ttu-id="bd004-114">Si una aplicación procesa este mensaje, debe devolver un identificador a un pincel.</span><span class="sxs-lookup"><span data-stu-id="bd004-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="bd004-115">El sistema utiliza el pincel para pintar el fondo del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bd004-115">The system uses the brush to paint the background of the dialog box.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd004-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd004-116">Remarks</span></span>

<span data-ttu-id="bd004-117">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bd004-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the dialog box.</span></span>

<span data-ttu-id="bd004-118">El sistema no destruye automáticamente el pincel devuelto.</span><span class="sxs-lookup"><span data-stu-id="bd004-118">The system does not automatically destroy the returned brush.</span></span> <span data-ttu-id="bd004-119">Es responsabilidad de la aplicación destruir el pincel cuando ya no se necesita.</span><span class="sxs-lookup"><span data-stu-id="bd004-119">It is the application's responsibility to destroy the brush when it is no longer needed.</span></span>

<span data-ttu-id="bd004-120">El mensaje de **\_ CTLCOLORDLG de WM** nunca se envía entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="bd004-120">The **WM\_CTLCOLORDLG** message is never sent between threads.</span></span> <span data-ttu-id="bd004-121">Solo se envía dentro de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="bd004-121">It is sent only within one thread.</span></span>

<span data-ttu-id="bd004-122">Tenga en cuenta que el mensaje de **\_ CTLCOLORDLG de WM** se envía al propio cuadro de diálogo; todos los demás mensajes \**WM \_ CTLCOLOR \** _ se envían al propietario del control.</span><span class="sxs-lookup"><span data-stu-id="bd004-122">Note that the **WM\_CTLCOLORDLG** message is sent to the dialog box itself; all of the other \**WM\_CTLCOLOR\** _ messages are sent to the owner of the control.</span></span>

<span data-ttu-id="bd004-123">Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en un _ *int \_ ptr*\* y devolver el valor directamente.</span><span class="sxs-lookup"><span data-stu-id="bd004-123">If a dialog box procedure handles this message, it should cast the desired return value to an _ *INT\_PTR*\* and return the value directly.</span></span> <span data-ttu-id="bd004-124">Si el procedimiento del cuadro de diálogo devuelve **false**, se realiza el control de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bd004-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="bd004-125">Se omite el valor de **DWL \_ MSGRESULT** establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="bd004-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd004-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd004-126">Requirements</span></span>



| <span data-ttu-id="bd004-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd004-127">Requirement</span></span> | <span data-ttu-id="bd004-128">Value</span><span class="sxs-lookup"><span data-stu-id="bd004-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd004-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd004-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bd004-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bd004-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bd004-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd004-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bd004-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bd004-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bd004-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd004-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd004-134"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd004-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd004-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd004-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="bd004-136">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="bd004-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bd004-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="bd004-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="bd004-138">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="bd004-138">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="bd004-139">**Vista**</span><span class="sxs-lookup"><span data-stu-id="bd004-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bd004-140">Cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="bd004-140">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="bd004-141">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="bd004-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="bd004-142">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="bd004-142">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="bd004-143">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="bd004-143">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

