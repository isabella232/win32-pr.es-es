---
title: Mensaje de TVM_EXPAND (commctrl. h)
description: El \_ mensaje TVM expand expande o contrae la lista de elementos secundarios asociada al elemento primario especificado, si existe. Puede enviar este mensaje explícitamente o mediante la \_ macro Expand de TreeView.
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- TVM_EXPAND controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_EXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d5cd7577c6f4581865569c3aefca93f13aa305
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492377"
---
# <a name="tvm_expand-message"></a><span data-ttu-id="30e06-105">\_Mensaje de expansión TVM</span><span class="sxs-lookup"><span data-stu-id="30e06-105">TVM\_EXPAND message</span></span>

<span data-ttu-id="30e06-106">El mensaje **TVM \_ Expand** expande o contrae la lista de elementos secundarios asociada al elemento primario especificado, si existe.</span><span class="sxs-lookup"><span data-stu-id="30e06-106">The **TVM\_EXPAND** message expands or collapses the list of child items associated with the specified parent item, if any.</span></span> <span data-ttu-id="30e06-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ Expand de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) .</span><span class="sxs-lookup"><span data-stu-id="30e06-107">You can send this message explicitly or by using the [**TreeView\_Expand**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="30e06-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30e06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30e06-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30e06-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30e06-110">Marca de acción.</span><span class="sxs-lookup"><span data-stu-id="30e06-110">Action flag.</span></span> <span data-ttu-id="30e06-111">Este parámetro puede ser uno o varios de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="30e06-111">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="30e06-112">Value</span><span class="sxs-lookup"><span data-stu-id="30e06-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="30e06-113">Significado</span><span class="sxs-lookup"><span data-stu-id="30e06-113">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <span data-ttu-id="30e06-114"><dt>**TVE \_ contraer**</dt></span><span class="sxs-lookup"><span data-stu-id="30e06-114"><dt>**TVE\_COLLAPSE**</dt></span></span> </dl>                | <span data-ttu-id="30e06-115">Contrae la lista.</span><span class="sxs-lookup"><span data-stu-id="30e06-115">Collapses the list.</span></span> <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <span data-ttu-id="30e06-116"><dt>**TVE \_ COLLAPSERESET**</dt></span><span class="sxs-lookup"><span data-stu-id="30e06-116"><dt>**TVE\_COLLAPSERESET**</dt></span></span> </dl> | <span data-ttu-id="30e06-117">Contrae la lista y quita los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="30e06-117">Collapses the list and removes the child items.</span></span> <span data-ttu-id="30e06-118">Se restablece la marca de estado [**TVIS \_ EXPANDEDONCE**](tree-view-control-item-states.md) .</span><span class="sxs-lookup"><span data-stu-id="30e06-118">The [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is reset.</span></span> <span data-ttu-id="30e06-119">Esta marca debe usarse con la \_ marca de contraer TVE.</span><span class="sxs-lookup"><span data-stu-id="30e06-119">This flag must be used with the TVE\_COLLAPSE flag.</span></span><br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <span data-ttu-id="30e06-120"><dt>**TVE \_ expandir**</dt></span><span class="sxs-lookup"><span data-stu-id="30e06-120"><dt>**TVE\_EXPAND**</dt></span></span> </dl>                      | <span data-ttu-id="30e06-121">Expande la lista.</span><span class="sxs-lookup"><span data-stu-id="30e06-121">Expands the list.</span></span><br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <span data-ttu-id="30e06-122"><dt>**TVE \_ EXPANDPARTIAL**</dt></span><span class="sxs-lookup"><span data-stu-id="30e06-122"><dt>**TVE\_EXPANDPARTIAL**</dt></span></span> </dl> | <span data-ttu-id="30e06-123">[Versión 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="30e06-123">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="30e06-124">Expande parcialmente la lista.</span><span class="sxs-lookup"><span data-stu-id="30e06-124">Partially expands the list.</span></span> <span data-ttu-id="30e06-125">En este estado, los elementos secundarios son visibles y se muestra el signo más (+) del elemento primario, que indica que se puede expandir.</span><span class="sxs-lookup"><span data-stu-id="30e06-125">In this state the child items are visible and the parent item's plus sign (+), indicating that it can be expanded, is displayed.</span></span> <span data-ttu-id="30e06-126">Esta marca se debe usar en combinación con la \_ marca de expansión TVE.</span><span class="sxs-lookup"><span data-stu-id="30e06-126">This flag must be used in combination with the TVE\_EXPAND flag.</span></span><br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <span data-ttu-id="30e06-127"><dt>**TVE \_ alternar**</dt></span><span class="sxs-lookup"><span data-stu-id="30e06-127"><dt>**TVE\_TOGGLE**</dt></span></span> </dl>                      | <span data-ttu-id="30e06-128">Contrae la lista si está expandida o la expande si está contraída.</span><span class="sxs-lookup"><span data-stu-id="30e06-128">Collapses the list if it is expanded or expands it if it is collapsed.</span></span><br/>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="30e06-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30e06-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30e06-130">Identificador del elemento primario que se va a expandir o contraer.</span><span class="sxs-lookup"><span data-stu-id="30e06-130">Handle to the parent item to expand or collapse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30e06-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30e06-131">Return value</span></span>

<span data-ttu-id="30e06-132">Devuelve un valor distinto de cero si la operación se realizó correctamente o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="30e06-132">Returns nonzero if the operation was successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="30e06-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30e06-133">Remarks</span></span>

<span data-ttu-id="30e06-134">La expansión de un nodo que ya se ha expandido se considera una operación correcta y [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="30e06-134">Expanding a node that is already expanded is considered a successful operation and [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns a nonzero value.</span></span> <span data-ttu-id="30e06-135">Al contraer un nodo, se devuelve cero si el nodo ya está contraído; en caso contrario, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="30e06-135">Collapsing a node returns zero if the node is already collapsed; otherwise it returns nonzero.</span></span> <span data-ttu-id="30e06-136">El intento de expandir o contraer un nodo que no tiene elementos secundarios se considera un error y **SendMessage** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="30e06-136">Attempting to expand or collapse a node that has no children is considered a failure and **SendMessage** returns zero.</span></span>

<span data-ttu-id="30e06-137">Cuando se expande un elemento por primera vez mediante un mensaje de **\_ expansión TVM** , la acción genera los códigos de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) y se establece la marca de estado [**TVIS \_**](tree-view-control-item-states.md) EXPANDEDONCE del elemento.</span><span class="sxs-lookup"><span data-stu-id="30e06-137">When an item is first expanded by a **TVM\_EXPAND** message, the action generates [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes and the item's [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is set.</span></span> <span data-ttu-id="30e06-138">Siempre y cuando esta marca de estado permanezca establecida, los mensajes de **\_ expansión TVM** posteriores no generarán \_ notificaciones de TVN ITEMEXPANDING o TVN \_ ITEMEXPANDED.</span><span class="sxs-lookup"><span data-stu-id="30e06-138">As long as this state flag remains set, subsequent **TVM\_EXPAND** messages do not generate TVN\_ITEMEXPANDING or TVN\_ITEMEXPANDED notifications.</span></span> <span data-ttu-id="30e06-139">Para restablecer la marca de estado **TVIS \_ EXPANDEDONCE** , debe enviar un mensaje **TVM \_ Expand** con las \_ marcas TVE Collapse y TVE \_ COLLAPSERESET establecidas.</span><span class="sxs-lookup"><span data-stu-id="30e06-139">To reset the **TVIS\_EXPANDEDONCE** state flag, you must send a **TVM\_EXPAND** message with the TVE\_COLLAPSE and TVE\_COLLAPSERESET flags set.</span></span> <span data-ttu-id="30e06-140">Al intentar establecer explícitamente **TVIS \_ EXPANDEDONCE** , se producirá un comportamiento imprevisible.</span><span class="sxs-lookup"><span data-stu-id="30e06-140">Attempting to explicitly set **TVIS\_EXPANDEDONCE** will result in unpredictable behavior.</span></span>

<span data-ttu-id="30e06-141">Se puede producir un error en la operación de expansión si el propietario del control TreeView deniega la operación en respuesta a una notificación [ \_ ITEMEXPANDING de TVN](tvn-itemexpanding.md) .</span><span class="sxs-lookup"><span data-stu-id="30e06-141">The expand operation may fail if the owner of the treeview control denies the operation in response to a [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="30e06-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30e06-142">Requirements</span></span>



| <span data-ttu-id="30e06-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="30e06-143">Requirement</span></span> | <span data-ttu-id="30e06-144">Value</span><span class="sxs-lookup"><span data-stu-id="30e06-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30e06-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30e06-145">Minimum supported client</span></span><br/> | <span data-ttu-id="30e06-146">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="30e06-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30e06-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30e06-147">Minimum supported server</span></span><br/> | <span data-ttu-id="30e06-148">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="30e06-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30e06-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30e06-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="30e06-150"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="30e06-150"><dt>Commctrl.h</dt></span></span> </dl> |



 

