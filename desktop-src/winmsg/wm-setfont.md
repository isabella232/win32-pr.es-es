---
description: Establece la fuente que un control va a utilizar al dibujar texto.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: Mensaje de WM_SETFONT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fc334e6b8c937759555c471f00ec56254a629c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002024"
---
# <a name="wm_setfont-message"></a><span data-ttu-id="9812d-103">Mensaje de WM \_ SETFONT</span><span class="sxs-lookup"><span data-stu-id="9812d-103">WM\_SETFONT message</span></span>

<span data-ttu-id="9812d-104">Establece la fuente que un control va a utilizar al dibujar texto.</span><span class="sxs-lookup"><span data-stu-id="9812d-104">Sets the font that a control is to use when drawing text.</span></span>


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a><span data-ttu-id="9812d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9812d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9812d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9812d-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9812d-107">Identificador de la fuente (**HFONT**).</span><span class="sxs-lookup"><span data-stu-id="9812d-107">A handle to the font (**HFONT**).</span></span> <span data-ttu-id="9812d-108">Si este parámetro es **null**, el control utiliza la fuente predeterminada del sistema para dibujar el texto.</span><span class="sxs-lookup"><span data-stu-id="9812d-108">If this parameter is **NULL**, the control uses the default system font to draw text.</span></span>

</dd> <dt>

<span data-ttu-id="9812d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9812d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9812d-110">La palabra de orden inferior de *lParam* especifica si el control debe volver a dibujarse inmediatamente después de establecer la fuente.</span><span class="sxs-lookup"><span data-stu-id="9812d-110">The low-order word of *lParam* specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="9812d-111">Si este parámetro es **true**, el control vuelve a dibujarse.</span><span class="sxs-lookup"><span data-stu-id="9812d-111">If this parameter is **TRUE**, the control redraws itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9812d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9812d-112">Return value</span></span>

<span data-ttu-id="9812d-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9812d-113">Type: **LRESULT**</span></span>

<span data-ttu-id="9812d-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9812d-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9812d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9812d-115">Remarks</span></span>

<span data-ttu-id="9812d-116">El mensaje de **WM \_ SETFONT** se aplica a todos los controles, no solo a los de los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9812d-116">The **WM\_SETFONT** message applies to all controls, not just those in dialog boxes.</span></span>

<span data-ttu-id="9812d-117">El mejor momento para que el propietario de un control de cuadro de diálogo establezca la fuente del control es cuando recibe el mensaje de [**\_ INITDIALOG de WM**](../dlgbox/wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="9812d-117">The best time for the owner of a dialog box control to set the font of the control is when it receives the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span> <span data-ttu-id="9812d-118">La aplicación debe llamar a la función [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) para eliminar la fuente cuando ya no se necesite; por ejemplo, después de que destruya el control.</span><span class="sxs-lookup"><span data-stu-id="9812d-118">The application should call the [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) function to delete the font when it is no longer needed; for example, after it destroys the control.</span></span>

<span data-ttu-id="9812d-119">El tamaño del control no cambia como resultado de recibir este mensaje.</span><span class="sxs-lookup"><span data-stu-id="9812d-119">The size of the control does not change as a result of receiving this message.</span></span> <span data-ttu-id="9812d-120">Para evitar el recorte de texto que no cabe dentro de los límites del control, la aplicación debe corregir el tamaño de la ventana de control antes de establecer la fuente.</span><span class="sxs-lookup"><span data-stu-id="9812d-120">To avoid clipping text that does not fit within the boundaries of the control, the application should correct the size of the control window before it sets the font.</span></span>

<span data-ttu-id="9812d-121">Cuando un cuadro de diálogo utiliza el estilo de [DS \_ SetFont](../dlgbox/about-dialog-boxes.md) para establecer el texto en sus controles, el sistema envía el mensaje de **WM \_ SetFont** al procedimiento del cuadro de diálogo antes de crear los controles.</span><span class="sxs-lookup"><span data-stu-id="9812d-121">When a dialog box uses the [DS\_SETFONT](../dlgbox/about-dialog-boxes.md) style to set the text in its controls, the system sends the **WM\_SETFONT** message to the dialog box procedure before it creates the controls.</span></span> <span data-ttu-id="9812d-122">Una aplicación puede crear un cuadro de diálogo que contenga el estilo de DS \_ SETFONT mediante una llamada a cualquiera de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="9812d-122">An application can create a dialog box that contains the DS\_SETFONT style by calling any of the following functions:</span></span>

-   [<span data-ttu-id="9812d-123">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="9812d-123">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [<span data-ttu-id="9812d-124">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="9812d-124">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [<span data-ttu-id="9812d-125">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="9812d-125">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [<span data-ttu-id="9812d-126">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="9812d-126">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a><span data-ttu-id="9812d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9812d-127">Requirements</span></span>



| <span data-ttu-id="9812d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9812d-128">Requirement</span></span> | <span data-ttu-id="9812d-129">Value</span><span class="sxs-lookup"><span data-stu-id="9812d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9812d-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9812d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9812d-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9812d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9812d-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9812d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9812d-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9812d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9812d-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9812d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9812d-135"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9812d-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9812d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="9812d-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="9812d-137">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9812d-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9812d-138">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="9812d-138">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="9812d-139">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="9812d-139">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="9812d-140">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="9812d-140">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="9812d-141">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="9812d-141">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="9812d-142">**DLGTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="9812d-142">**DLGTEMPLATE**</span></span>](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[<span data-ttu-id="9812d-143">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="9812d-143">**MAKELPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="9812d-144">**GETFONT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9812d-144">**WM\_GETFONT**</span></span>](wm-getfont.md)
</dt> <dt>

[<span data-ttu-id="9812d-145">**INITDIALOG de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9812d-145">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> <dt>

<span data-ttu-id="9812d-146">**Vista**</span><span class="sxs-lookup"><span data-stu-id="9812d-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9812d-147">Windows</span><span class="sxs-lookup"><span data-stu-id="9812d-147">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="9812d-148">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="9812d-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9812d-149">**DeleteObject**</span><span class="sxs-lookup"><span data-stu-id="9812d-149">**DeleteObject**</span></span>](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
