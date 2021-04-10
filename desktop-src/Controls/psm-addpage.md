---
title: Mensaje de PSM_ADDPAGE (Prsht. h)
description: Agrega una nueva página al final de una hoja de propiedades existente. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ addPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- PSM_ADDPAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d09e07dfa2be86e11fa33863f091732955714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905473"
---
# <a name="psm_addpage-message"></a><span data-ttu-id="f3a08-105">Mensaje de PSM de PSM \_</span><span class="sxs-lookup"><span data-stu-id="f3a08-105">PSM\_ADDPAGE message</span></span>

<span data-ttu-id="f3a08-106">Agrega una nueva página al final de una hoja de propiedades existente.</span><span class="sxs-lookup"><span data-stu-id="f3a08-106">Adds a new page to the end of an existing property sheet.</span></span> <span data-ttu-id="f3a08-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ addPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) .</span><span class="sxs-lookup"><span data-stu-id="f3a08-107">You can send this message explicitly or by using the [**PropSheet\_AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3a08-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3a08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a08-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3a08-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3a08-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f3a08-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f3a08-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3a08-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3a08-112">Identificador de la página que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="f3a08-112">Handle to the page to add.</span></span> <span data-ttu-id="f3a08-113">La página debe haber sido creada por una llamada anterior a la función [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="f3a08-113">The page must have been created by a previous call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3a08-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3a08-114">Return value</span></span>

<span data-ttu-id="f3a08-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f3a08-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a08-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3a08-116">Remarks</span></span>

<span data-ttu-id="f3a08-117">La nueva página no debe ser mayor que la página más grande que se encuentra actualmente en la hoja de propiedades porque no se cambia el tamaño de la hoja de propiedades para ajustarse a la nueva página.</span><span class="sxs-lookup"><span data-stu-id="f3a08-117">The new page should be no larger than the largest page currently in the property sheet because the property sheet is not resized to fit the new page.</span></span>

<span data-ttu-id="f3a08-118">Se producen varios mensajes y una llamada de función mientras la hoja de propiedades manipula la lista de páginas.</span><span class="sxs-lookup"><span data-stu-id="f3a08-118">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="f3a08-119">Mientras se realiza esta acción, el intento de modificar la lista de páginas tendrá resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="f3a08-119">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="f3a08-120">Por lo tanto, no debe usar el \_ mensaje de PSM en la implementación de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o mientras controla las siguientes notificaciones y mensajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="f3a08-120">Accordingly, you should not use the PSM\_ADDPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="f3a08-121">PSN \_ aplicar</span><span class="sxs-lookup"><span data-stu-id="f3a08-121">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="f3a08-122">PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="f3a08-122">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="f3a08-123">restablecimiento de PSN \_</span><span class="sxs-lookup"><span data-stu-id="f3a08-123">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="f3a08-124">PSN \_ SETACTIVE</span><span class="sxs-lookup"><span data-stu-id="f3a08-124">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="f3a08-125">**destrucción de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f3a08-125">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="f3a08-126">**INITDIALOG de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f3a08-126">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="f3a08-127">Si tiene que modificar una página de la hoja de propiedades mientras está controlando uno de estos mensajes o mientras [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) está en funcionamiento, envíese a sí mismo un mensaje de Windows privado.</span><span class="sxs-lookup"><span data-stu-id="f3a08-127">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="f3a08-128">La aplicación no recibirá ese mensaje hasta que el administrador de la hoja de propiedades haya finalizado sus tareas.</span><span class="sxs-lookup"><span data-stu-id="f3a08-128">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="f3a08-129">A continuación, puede modificar la lista de páginas.</span><span class="sxs-lookup"><span data-stu-id="f3a08-129">Then you can modify the list of pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a08-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3a08-130">Requirements</span></span>



| <span data-ttu-id="f3a08-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3a08-131">Requirement</span></span> | <span data-ttu-id="f3a08-132">Value</span><span class="sxs-lookup"><span data-stu-id="f3a08-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a08-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3a08-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a08-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f3a08-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f3a08-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3a08-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a08-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3a08-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f3a08-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3a08-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3a08-138"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3a08-138"><dt>Prsht.h</dt></span></span> </dl> |



 

