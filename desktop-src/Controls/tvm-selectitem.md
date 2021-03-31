---
title: Mensaje de TVM_SELECTITEM (commctrl. h)
description: Selecciona el elemento de vista de árbol especificado, desplaza el elemento a la vista o vuelve a dibujar el elemento en el estilo utilizado para indicar el destino de una operación de arrastrar y colocar.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- TVM_SELECTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905080"
---
# <a name="tvm_selectitem-message"></a><span data-ttu-id="2ac2c-104">\_Mensaje de SELECTITEM TVM</span><span class="sxs-lookup"><span data-stu-id="2ac2c-104">TVM\_SELECTITEM message</span></span>

<span data-ttu-id="2ac2c-105">Selecciona el elemento de vista de árbol especificado, desplaza el elemento a la vista o vuelve a dibujar el elemento en el estilo utilizado para indicar el destino de una operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-105">Selects the specified tree-view item, scrolls the item into view, or redraws the item in the style used to indicate the target of a drag-and-drop operation.</span></span> <span data-ttu-id="2ac2c-106">Puede enviar este mensaje explícitamente o mediante la macro [**\_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)o [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) de TreeView.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-106">You can send this message explicitly or by using the [**TreeView\_Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem), or [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ac2c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ac2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ac2c-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ac2c-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ac2c-109">Marca de acción.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-109">Action flag.</span></span> <span data-ttu-id="2ac2c-110">Este parámetro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="2ac2c-110">This parameter can be one of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2ac2c-111">Value</span><span class="sxs-lookup"><span data-stu-id="2ac2c-111">Value</span></span></th>
<th><span data-ttu-id="2ac2c-112">Significado</span><span class="sxs-lookup"><span data-stu-id="2ac2c-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <span data-ttu-id="2ac2c-113"><dt><strong>TVGN_CARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2ac2c-113"><dt><strong>TVGN_CARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2ac2c-114">Establece la selección en el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-114">Sets the selection to the specified item.</span></span> <span data-ttu-id="2ac2c-115">La ventana primaria del control de vista de árbol recibe los códigos de notificación de <a href="tvn-selchanging.md">TVN_SELCHANGING</a> y <a href="tvn-selchanged.md">TVN_SELCHANGED</a> .</span><span class="sxs-lookup"><span data-stu-id="2ac2c-115">The tree-view control's parent window receives the <a href="tvn-selchanging.md">TVN_SELCHANGING</a> and <a href="tvn-selchanged.md">TVN_SELCHANGED</a> notification codes.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <span data-ttu-id="2ac2c-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2ac2c-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2ac2c-117">Vuelve a dibujar el elemento especificado en el estilo utilizado para indicar el destino de una operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-117">Redraws the specified item in the style used to indicate the target of a drag-and-drop operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <span data-ttu-id="2ac2c-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2ac2c-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2ac2c-119">Garantiza que el elemento especificado esté visible y, si es posible, lo muestra en la parte superior de la ventana del control.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-119">Ensures that the specified item is visible, and, if possible, displays it at the top of the control's window.</span></span> <span data-ttu-id="2ac2c-120">Los controles de vista de árbol muestran tantos elementos como quepan en la ventana.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-120">Tree-view controls display as many items as will fit in the window.</span></span> <span data-ttu-id="2ac2c-121">Si el elemento especificado está cerca de la parte inferior de la jerarquía de elementos del control, puede que no se convierta en el primer elemento visible, en función de cuántos elementos quepan en la ventana.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-121">If the specified item is near the bottom of the control's hierarchy of items, it might not become the first visible item, depending on how many items fit in the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <span data-ttu-id="2ac2c-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2ac2c-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2ac2c-123">Cuando se selecciona un solo elemento, garantiza que la vista de árbol no expande los elementos secundarios de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-123">When a single item is selected, ensures that the treeview does not expand the children of that item.</span></span> <span data-ttu-id="2ac2c-124">Esto solo es válido si se usa con la marca TVGN_CARET.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-124">This is valid only if used with the TVGN_CARET flag.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2ac2c-125">Para usar esta marca, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-125">To use this flag, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2ac2c-126">Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">habilitar estilos visuales</a>.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-126">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="2ac2c-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ac2c-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ac2c-128">Identificador de un elemento.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-128">Handle to an item.</span></span> <span data-ttu-id="2ac2c-129">Si *lParam* es **null**, el control se establece para que no tenga ningún elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-129">If *lParam* is **NULL**, the control is set to have no selected item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ac2c-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ac2c-130">Return value</span></span>

<span data-ttu-id="2ac2c-131">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ac2c-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ac2c-132">Remarks</span></span>

<span data-ttu-id="2ac2c-133">Si el elemento especificado es el elemento secundario de un elemento primario contraído, la lista de elementos secundarios del elemento primario se expande para mostrar el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-133">If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item.</span></span> <span data-ttu-id="2ac2c-134">En este caso, la ventana primaria del control recibe los códigos de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .</span><span class="sxs-lookup"><span data-stu-id="2ac2c-134">In this case, the control's parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

<span data-ttu-id="2ac2c-135">Usar la [**macro \_ SelectItem de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) es equivalente a enviar el mensaje **TVM \_ SelectItem** con *wParam* establecido en el \_ valor del símbolo de intercalación TVGN.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-135">Using the [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_CARET value.</span></span> <span data-ttu-id="2ac2c-136">Usar la [**macro \_ SelectDropTarget de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) es equivalente a enviar el mensaje **TVM \_ SELECTITEM** con *wParam* establecido en el \_ valor de TVGN DROPHILITE.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-136">Using the [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_DROPHILITE value.</span></span> <span data-ttu-id="2ac2c-137">El uso de [**TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) es equivalente a enviar el mensaje **TVM \_ SELECTITEM** con *wParam* establecido en el valor de TVGN \_ FIRSTVISIBLE.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-137">Using [**TreeView\_SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_FIRSTVISIBLE value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ac2c-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ac2c-138">Requirements</span></span>



| <span data-ttu-id="2ac2c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ac2c-139">Requirement</span></span> | <span data-ttu-id="2ac2c-140">Value</span><span class="sxs-lookup"><span data-stu-id="2ac2c-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac2c-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ac2c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2ac2c-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2ac2c-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ac2c-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ac2c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2ac2c-144">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ac2c-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ac2c-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ac2c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ac2c-146"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ac2c-146"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





