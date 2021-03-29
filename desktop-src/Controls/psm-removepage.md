---
title: Mensaje de PSM_REMOVEPAGE (Prsht. h)
description: Quita una página de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ RemovePage.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- PSM_REMOVEPAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cae1611e1ed9540fce23d20681f44849903e5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905470"
---
# <a name="psm_removepage-message"></a><span data-ttu-id="23fb7-105">Mensaje de PSM \_ REMOVEPAGE</span><span class="sxs-lookup"><span data-stu-id="23fb7-105">PSM\_REMOVEPAGE message</span></span>

<span data-ttu-id="23fb7-106">Quita una página de una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="23fb7-106">Removes a page from a property sheet.</span></span> <span data-ttu-id="23fb7-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) .</span><span class="sxs-lookup"><span data-stu-id="23fb7-107">You can send this message explicitly or by using the [**PropSheet\_RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="23fb7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23fb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23fb7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23fb7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23fb7-110">Índice de base cero de la página que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="23fb7-110">Zero-based index of the page to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="23fb7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23fb7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23fb7-112">Identificador de HPROPSHEETPAGE de la página que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="23fb7-112">The HPROPSHEETPAGE handle of the page to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23fb7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23fb7-113">Return value</span></span>

<span data-ttu-id="23fb7-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="23fb7-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23fb7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23fb7-115">Remarks</span></span>

<span data-ttu-id="23fb7-116">Una aplicación puede especificar el índice o el identificador, o ambos.</span><span class="sxs-lookup"><span data-stu-id="23fb7-116">An application can specify the index or the handle, or both.</span></span> <span data-ttu-id="23fb7-117">Si se especifican ambos, *lParam* tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="23fb7-117">If both are specified, *lParam* takes precedence.</span></span>

<span data-ttu-id="23fb7-118">El envío de **PSM \_ REMOVEPAGE** destruye la página de la hoja de propiedades que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="23fb7-118">Sending **PSM\_REMOVEPAGE** destroys the property sheet page that is being removed.</span></span>

<span data-ttu-id="23fb7-119">Se producen varios mensajes y una llamada de función mientras la hoja de propiedades manipula la lista de páginas.</span><span class="sxs-lookup"><span data-stu-id="23fb7-119">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="23fb7-120">Mientras se realiza esta acción, el intento de modificar la lista de páginas tendrá resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="23fb7-120">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="23fb7-121">En consecuencia, no debe usar el mensaje **PSM \_ REMOVEPAGE** en la implementación de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o mientras controla las siguientes notificaciones y mensajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="23fb7-121">Accordingly, you should not use the **PSM\_REMOVEPAGE** message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="23fb7-122">PSN \_ aplicar</span><span class="sxs-lookup"><span data-stu-id="23fb7-122">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="23fb7-123">PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="23fb7-123">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="23fb7-124">restablecimiento de PSN \_</span><span class="sxs-lookup"><span data-stu-id="23fb7-124">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="23fb7-125">PSN \_ SETACTIVE</span><span class="sxs-lookup"><span data-stu-id="23fb7-125">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="23fb7-126">**destrucción de WM \_**</span><span class="sxs-lookup"><span data-stu-id="23fb7-126">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="23fb7-127">**INITDIALOG de WM \_**</span><span class="sxs-lookup"><span data-stu-id="23fb7-127">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="23fb7-128">Si tiene que modificar una página de la hoja de propiedades mientras está controlando uno de estos mensajes o mientras [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) está en funcionamiento, envíese a sí mismo un mensaje de Windows privado.</span><span class="sxs-lookup"><span data-stu-id="23fb7-128">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="23fb7-129">La aplicación no recibirá ese mensaje hasta que el administrador de la hoja de propiedades haya finalizado sus tareas.</span><span class="sxs-lookup"><span data-stu-id="23fb7-129">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="23fb7-130">A continuación, puede modificar la lista de páginas.</span><span class="sxs-lookup"><span data-stu-id="23fb7-130">Then you can modify the list of pages.</span></span>

<span data-ttu-id="23fb7-131">Las siguientes notificaciones también se ven afectadas por la modificación de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="23fb7-131">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="23fb7-132">PSN \_ WIZBACK</span><span class="sxs-lookup"><span data-stu-id="23fb7-132">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="23fb7-133">PSN \_ WIZNEXT</span><span class="sxs-lookup"><span data-stu-id="23fb7-133">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="23fb7-134">Puede Agregar o quitar páginas en respuesta a estas notificaciones, siempre que devuelva (a través de DWL \_ MSGRESULT) un valor distinto de cero para especificar la nueva página deseada.</span><span class="sxs-lookup"><span data-stu-id="23fb7-134">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="23fb7-135">Sin embargo, tenga en cuenta que si quita una página que se encuentra antes de la página actual (que tiene un índice más pequeño que la página actual), [PSN \_ KILLACTIVE](psn-killactive.md) podría enviarse a una página equivocada.</span><span class="sxs-lookup"><span data-stu-id="23fb7-135">Note, however, that if you remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

## <a name="requirements"></a><span data-ttu-id="23fb7-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23fb7-136">Requirements</span></span>



| <span data-ttu-id="23fb7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="23fb7-137">Requirement</span></span> | <span data-ttu-id="23fb7-138">Value</span><span class="sxs-lookup"><span data-stu-id="23fb7-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23fb7-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23fb7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="23fb7-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="23fb7-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="23fb7-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23fb7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="23fb7-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="23fb7-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="23fb7-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23fb7-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="23fb7-144"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="23fb7-144"><dt>Prsht.h</dt></span></span> </dl> |



 

