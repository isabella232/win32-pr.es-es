---
title: Mensaje de TVM_DELETEITEM (commctrl. h)
description: Quita un elemento y todos sus elementos secundarios de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro DeleteItem de TreeView.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- TVM_DELETEITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8783fd5acdf7319699cdc67cbb3ea075e4dbbc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490846"
---
# <a name="tvm_deleteitem-message"></a><span data-ttu-id="6f786-105">Mensaje de TVM \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="6f786-105">TVM\_DELETEITEM message</span></span>

<span data-ttu-id="6f786-106">Quita un elemento y todos sus elementos secundarios de un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="6f786-106">Removes an item and all its children from a tree-view control.</span></span> <span data-ttu-id="6f786-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ DeleteItem de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="6f786-107">You can send this message explicitly or by using the [**TreeView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f786-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f786-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f786-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f786-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6f786-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6f786-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6f786-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f786-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f786-112">Identificador de **HTREEITEM** del elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="6f786-112">**HTREEITEM** handle to the item to delete.</span></span> <span data-ttu-id="6f786-113">Si *lParam* se establece en TVI \_ root o en **null**, se eliminan todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="6f786-113">If *lParam* is set to TVI\_ROOT or to **NULL**, all items are deleted.</span></span> <span data-ttu-id="6f786-114">También puede usar la macro [**\_ DeleteAllItems de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) para eliminar todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="6f786-114">You can also use the [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) macro to delete all items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f786-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f786-115">Return value</span></span>

<span data-ttu-id="6f786-116">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6f786-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f786-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f786-117">Remarks</span></span>

<span data-ttu-id="6f786-118">No es seguro eliminar elementos en respuesta a una notificación como [TVN \_ SELCHANGING](tvn-selchanging.md).</span><span class="sxs-lookup"><span data-stu-id="6f786-118">It is not safe to delete items in response to a notification such as [TVN\_SELCHANGING](tvn-selchanging.md).</span></span>

<span data-ttu-id="6f786-119">Una vez que se elimina un elemento, su identificador no es válido y no se puede usar.</span><span class="sxs-lookup"><span data-stu-id="6f786-119">Once an item is deleted, its handle is invalid and cannot be used.</span></span>

<span data-ttu-id="6f786-120">La ventana primaria recibe un código de notificación [TVN \_ DELETEITEM](tvn-deleteitem.md) cuando se quita cada elemento.</span><span class="sxs-lookup"><span data-stu-id="6f786-120">The parent window receives a [TVN\_DELETEITEM](tvn-deleteitem.md) notification code when each item is removed.</span></span>

<span data-ttu-id="6f786-121">Si se está editando la etiqueta del elemento, la operación de edición se cancela y la ventana primaria recibe el código de notificación [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="6f786-121">If the item label is being edited, the edit operation is canceled and the parent window receives the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

<span data-ttu-id="6f786-122">Si elimina todos los elementos de un control de vista de árbol que tenga el estilo de [**\_ desplazamientos de los televisores**](tree-view-control-window-styles.md) , es posible que los elementos agregados posteriormente no se muestren correctamente.</span><span class="sxs-lookup"><span data-stu-id="6f786-122">If you delete all items in a tree-view control that has the [**TVS\_NOSCROLL**](tree-view-control-window-styles.md) style, items subsequently added may not display properly.</span></span> <span data-ttu-id="6f786-123">Para obtener más información, vea [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span><span class="sxs-lookup"><span data-stu-id="6f786-123">For more information, see [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f786-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f786-124">Requirements</span></span>



| <span data-ttu-id="6f786-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f786-125">Requirement</span></span> | <span data-ttu-id="6f786-126">Value</span><span class="sxs-lookup"><span data-stu-id="6f786-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f786-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f786-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6f786-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6f786-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f786-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f786-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6f786-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f786-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f786-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f786-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f786-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f786-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





