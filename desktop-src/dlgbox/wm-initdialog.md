---
title: Mensaje de WM_INITDIALOG (Winuser. h)
description: Se envía al procedimiento del cuadro de diálogo inmediatamente antes de que se muestre un cuadro de diálogo. Los procedimientos del cuadro de diálogo suelen usar este mensaje para inicializar controles y realizar cualquier otra tarea de inicialización que afecte a la apariencia del cuadro de diálogo.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- WM_INITDIALOG cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720226"
---
# <a name="wm_initdialog-message"></a><span data-ttu-id="f9dd1-105">Mensaje de INITDIALOG de WM \_</span><span class="sxs-lookup"><span data-stu-id="f9dd1-105">WM\_INITDIALOG message</span></span>

<span data-ttu-id="f9dd1-106">Se envía al procedimiento del cuadro de diálogo inmediatamente antes de que se muestre un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-106">Sent to the dialog box procedure immediately before a dialog box is displayed.</span></span> <span data-ttu-id="f9dd1-107">Los procedimientos del cuadro de diálogo suelen usar este mensaje para inicializar controles y realizar cualquier otra tarea de inicialización que afecte a la apariencia del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-107">Dialog box procedures typically use this message to initialize controls and carry out any other initialization tasks that affect the appearance of the dialog box.</span></span>


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a><span data-ttu-id="f9dd1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9dd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9dd1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9dd1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9dd1-110">Identificador del control que va a recibir el foco de teclado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-110">A handle to the control to receive the default keyboard focus.</span></span> <span data-ttu-id="f9dd1-111">El sistema asigna el foco de teclado predeterminado solo si el procedimiento de cuadro de diálogo devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-111">The system assigns the default keyboard focus only if the dialog box procedure returns **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="f9dd1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9dd1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9dd1-113">Datos de inicialización adicionales.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-113">Additional initialization data.</span></span> <span data-ttu-id="f9dd1-114">Estos datos se pasan al sistema como el parámetro *lParam* en una llamada a la función [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)o [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) utilizada para crear el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-114">This data is passed to the system as the *lParam* parameter in a call to the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), or [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) function used to create the dialog box.</span></span> <span data-ttu-id="f9dd1-115">En las hojas de propiedades, este parámetro es un puntero a la estructura [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) utilizada para crear la página.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-115">For property sheets, this parameter is a pointer to the [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) structure used to create the page.</span></span> <span data-ttu-id="f9dd1-116">Este parámetro es cero si se utiliza cualquier otra función de creación de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-116">This parameter is zero if any other dialog box creation function is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9dd1-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9dd1-117">Return value</span></span>

<span data-ttu-id="f9dd1-118">El procedimiento de cuadro de diálogo debe devolver **true** para indicar al sistema que establezca el foco de teclado en el control especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-118">The dialog box procedure should return **TRUE** to direct the system to set the keyboard focus to the control specified by *wParam*.</span></span> <span data-ttu-id="f9dd1-119">De lo contrario, debería devolver **false** para evitar que el sistema establezca el foco de teclado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-119">Otherwise, it should return **FALSE** to prevent the system from setting the default keyboard focus.</span></span>

<span data-ttu-id="f9dd1-120">El procedimiento del cuadro de diálogo debe devolver el valor directamente.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-120">The dialog box procedure should return the value directly.</span></span> <span data-ttu-id="f9dd1-121">Se omite el valor de **DWL \_ MSGRESULT** establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="f9dd1-121">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9dd1-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9dd1-122">Remarks</span></span>

<span data-ttu-id="f9dd1-123">El control para recibir el foco de teclado predeterminado siempre es el primer control del cuadro de diálogo que es visible, no deshabilitado y que tiene el estilo **WS \_ TABSTOP** .</span><span class="sxs-lookup"><span data-stu-id="f9dd1-123">The control to receive the default keyboard focus is always the first control in the dialog box that is visible, not disabled, and that has the **WS\_TABSTOP** style.</span></span> <span data-ttu-id="f9dd1-124">Cuando el procedimiento del cuadro de diálogo devuelve **true**, el sistema comprueba el control para asegurarse de que el procedimiento no lo ha deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-124">When the dialog box procedure returns **TRUE**, the system checks the control to ensure that the procedure has not disabled it.</span></span> <span data-ttu-id="f9dd1-125">Si se ha deshabilitado, el sistema establece el foco de teclado en el siguiente control que es visible, no deshabilitado y que tiene el **WS \_ TABSTOP**.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-125">If it has been disabled, the system sets the keyboard focus to the next control that is visible, not disabled, and has the **WS\_TABSTOP**.</span></span>

<span data-ttu-id="f9dd1-126">Una aplicación solo puede devolver **false** si ha establecido el foco de teclado en uno de los controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f9dd1-126">An application can return **FALSE** only if it has set the keyboard focus to one of the controls of the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9dd1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9dd1-127">Requirements</span></span>



| <span data-ttu-id="f9dd1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9dd1-128">Requirement</span></span> | <span data-ttu-id="f9dd1-129">Value</span><span class="sxs-lookup"><span data-stu-id="f9dd1-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9dd1-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9dd1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f9dd1-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f9dd1-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f9dd1-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9dd1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f9dd1-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f9dd1-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f9dd1-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9dd1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9dd1-135"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9dd1-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9dd1-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9dd1-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="f9dd1-137">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f9dd1-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f9dd1-138">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="f9dd1-138">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="f9dd1-139">**CreateDialogParam**</span><span class="sxs-lookup"><span data-stu-id="f9dd1-139">**CreateDialogParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[<span data-ttu-id="f9dd1-140">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="f9dd1-140">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="f9dd1-141">**DialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="f9dd1-141">**DialogBoxParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[<span data-ttu-id="f9dd1-142">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="f9dd1-142">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="f9dd1-143">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f9dd1-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f9dd1-144">Cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="f9dd1-144">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="f9dd1-145">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="f9dd1-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f9dd1-146">**PROPSHEETPAGE**</span><span class="sxs-lookup"><span data-stu-id="f9dd1-146">**PROPSHEETPAGE**</span></span>](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

