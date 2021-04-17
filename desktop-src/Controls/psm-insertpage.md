---
title: Mensaje de PSM_INSERTPAGE (Prsht. h)
description: Inserta una nueva página en una hoja de propiedades existente. La página puede insertarse en un índice especificado o después de una página especificada. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ InsertPage.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- PSM_INSERTPAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afdd58536a5cdd18d39a331df4b18c9bbae93842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658234"
---
# <a name="psm_insertpage-message"></a><span data-ttu-id="63bb9-106">Mensaje de PSM \_ INSERTPAGE</span><span class="sxs-lookup"><span data-stu-id="63bb9-106">PSM\_INSERTPAGE message</span></span>

<span data-ttu-id="63bb9-107">Inserta una nueva página en una hoja de propiedades existente.</span><span class="sxs-lookup"><span data-stu-id="63bb9-107">Inserts a new page into an existing property sheet.</span></span> <span data-ttu-id="63bb9-108">La página puede insertarse en un índice especificado o después de una página especificada.</span><span class="sxs-lookup"><span data-stu-id="63bb9-108">The page can be inserted either at a specified index or after a specified page.</span></span> <span data-ttu-id="63bb9-109">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) .</span><span class="sxs-lookup"><span data-stu-id="63bb9-109">You can send this message explicitly or by using the [**PropSheet\_InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="63bb9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63bb9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63bb9-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63bb9-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63bb9-112">Donde se va a insertar la página.</span><span class="sxs-lookup"><span data-stu-id="63bb9-112">Where the page is to be inserted.</span></span> <span data-ttu-id="63bb9-113">Establezca este parámetro en **null** para que la nueva página sea la primera página.</span><span class="sxs-lookup"><span data-stu-id="63bb9-113">Set this parameter to **NULL** to make the new page the first page.</span></span> <span data-ttu-id="63bb9-114">Para especificar dónde se va a insertar la nueva página, puede pasar un índice o el identificador HPROPSHEETPAGE de una página existente.</span><span class="sxs-lookup"><span data-stu-id="63bb9-114">To specify where the new page is to be inserted, you can either pass an index or an existing page's HPROPSHEETPAGE handle.</span></span>



| <span data-ttu-id="63bb9-115">Value</span><span class="sxs-lookup"><span data-stu-id="63bb9-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="63bb9-116">Significado</span><span class="sxs-lookup"><span data-stu-id="63bb9-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63bb9-117"><dt></dt> <dt>index</dt></span><span class="sxs-lookup"><span data-stu-id="63bb9-117"><dt></dt> <dt>index</dt></span></span> </dl>            | <span data-ttu-id="63bb9-118">Si el parámetro *wParam* es menor que MAXUSHORT (el entero corto sin signo más grande), *wParam* especifica el índice de base cero para la nueva página.</span><span class="sxs-lookup"><span data-stu-id="63bb9-118">If the *wParam* parameter is less than MAXUSHORT (the largest unsigned short integer), the *wParam* specifies the zero-based index for the new page.</span></span> <span data-ttu-id="63bb9-119">Por ejemplo, para convertir la página insertada en la tercera página de la hoja de propiedades, establezca *wParam* en 2.</span><span class="sxs-lookup"><span data-stu-id="63bb9-119">For example, to make the inserted page the third page on the property sheet, set *wParam* to 2.</span></span> <span data-ttu-id="63bb9-120">Para convertirlo en la primera página, establezca *wParam* en 0.</span><span class="sxs-lookup"><span data-stu-id="63bb9-120">To make it the first page, set *wParam* to 0.</span></span> <span data-ttu-id="63bb9-121">Si *wParam* tiene un valor mayor que el número de páginas y menor que MAXUSHORT, se anexará la página.</span><span class="sxs-lookup"><span data-stu-id="63bb9-121">If *wParam* has a value greater than the number of pages and less than MAXUSHORT, the page will be appended.</span></span><br/> |
| <dl> <span data-ttu-id="63bb9-122"><dt></dt><dt>hpageInsertAfter</dt></span><span class="sxs-lookup"><span data-stu-id="63bb9-122"><dt></dt> <dt>hpageInsertAfter</dt></span></span> </dl> | <span data-ttu-id="63bb9-123">Si establece el parámetro *wParam* en el identificador de HPROPSHEETPAGE de una página existente, la nueva página se insertará después.</span><span class="sxs-lookup"><span data-stu-id="63bb9-123">If you set the *wParam* parameter to an existing page's HPROPSHEETPAGE handle, the new page will be inserted after it.</span></span><br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="63bb9-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63bb9-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63bb9-125">Identificador de la página que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="63bb9-125">Handle to the page to be inserted.</span></span> <span data-ttu-id="63bb9-126">La página debe crearse primero mediante una llamada a la función [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="63bb9-126">The page must first be created by a call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63bb9-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63bb9-127">Return value</span></span>

<span data-ttu-id="63bb9-128">Devuelve un valor distinto de cero si la página se insertó correctamente o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="63bb9-128">Returns a nonzero value if the page was successfully inserted, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="63bb9-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63bb9-129">Remarks</span></span>

<span data-ttu-id="63bb9-130">Las páginas después del punto de inserción se desplazan hacia la derecha para dar cabida a la nueva página.</span><span class="sxs-lookup"><span data-stu-id="63bb9-130">The pages after the insertion point are shifted to the right to accommodate the new page.</span></span>

<span data-ttu-id="63bb9-131">No se cambia el tamaño de la hoja de propiedades para ajustarse a la nueva página.</span><span class="sxs-lookup"><span data-stu-id="63bb9-131">The property sheet is not resized to fit the new page.</span></span> <span data-ttu-id="63bb9-132">No haga que la nueva página sea más grande que la página más grande de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="63bb9-132">Do not make the new page larger than the property sheet's largest page.</span></span>

<span data-ttu-id="63bb9-133">Se producen varios mensajes y una llamada de función mientras la hoja de propiedades manipula la lista de páginas.</span><span class="sxs-lookup"><span data-stu-id="63bb9-133">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="63bb9-134">Mientras se realiza esta acción, el intento de modificar la lista de páginas tendrá resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="63bb9-134">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="63bb9-135">En consecuencia, no debe usar el \_ mensaje PSM INSERTPAGE en la implementación de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o mientras controla las siguientes notificaciones y mensajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="63bb9-135">Accordingly, you should not use the PSM\_INSERTPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="63bb9-136">PSN \_ aplicar</span><span class="sxs-lookup"><span data-stu-id="63bb9-136">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="63bb9-137">PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="63bb9-137">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="63bb9-138">restablecimiento de PSN \_</span><span class="sxs-lookup"><span data-stu-id="63bb9-138">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="63bb9-139">PSN \_ SETACTIVE</span><span class="sxs-lookup"><span data-stu-id="63bb9-139">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="63bb9-140">**destrucción de WM \_**</span><span class="sxs-lookup"><span data-stu-id="63bb9-140">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="63bb9-141">**INITDIALOG de WM \_**</span><span class="sxs-lookup"><span data-stu-id="63bb9-141">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="63bb9-142">Si tiene que modificar una página de la hoja de propiedades mientras está controlando uno de estos mensajes o mientras [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) está en funcionamiento, envíese a sí mismo un mensaje de Windows privado.</span><span class="sxs-lookup"><span data-stu-id="63bb9-142">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="63bb9-143">La aplicación no recibirá ese mensaje hasta que el administrador de la hoja de propiedades haya finalizado sus tareas.</span><span class="sxs-lookup"><span data-stu-id="63bb9-143">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="63bb9-144">A continuación, puede modificar la lista de páginas.</span><span class="sxs-lookup"><span data-stu-id="63bb9-144">Then you can modify the list of pages.</span></span>

<span data-ttu-id="63bb9-145">Las siguientes notificaciones también se ven afectadas por la modificación de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="63bb9-145">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="63bb9-146">PSN \_ WIZBACK</span><span class="sxs-lookup"><span data-stu-id="63bb9-146">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="63bb9-147">PSN \_ WIZNEXT</span><span class="sxs-lookup"><span data-stu-id="63bb9-147">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="63bb9-148">Puede Agregar o quitar páginas en respuesta a estas notificaciones, siempre que devuelva (a través de DWL \_ MSGRESULT) un valor distinto de cero para especificar la nueva página deseada.</span><span class="sxs-lookup"><span data-stu-id="63bb9-148">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="63bb9-149">Tenga en cuenta, sin embargo, que si inserta una página que se encuentra antes de la página actual (que tiene un índice menor que la página actual), [PSN \_ KILLACTIVE](psn-killactive.md) podría enviarse a una página equivocada.</span><span class="sxs-lookup"><span data-stu-id="63bb9-149">Note, however, that if you insert a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

> [!Note]  
> <span data-ttu-id="63bb9-150">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="63bb9-150">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="63bb9-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63bb9-151">Requirements</span></span>



| <span data-ttu-id="63bb9-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="63bb9-152">Requirement</span></span> | <span data-ttu-id="63bb9-153">Value</span><span class="sxs-lookup"><span data-stu-id="63bb9-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63bb9-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63bb9-154">Minimum supported client</span></span><br/> | <span data-ttu-id="63bb9-155">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="63bb9-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="63bb9-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63bb9-156">Minimum supported server</span></span><br/> | <span data-ttu-id="63bb9-157">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="63bb9-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="63bb9-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63bb9-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="63bb9-159"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="63bb9-159"><dt>Prsht.h</dt></span></span> </dl> |



 

