---
title: Tree-View Estados de elemento de control (CommCtrl. h)
description: En esta sección se enumeran las marcas de estado del elemento que se usan para indicar el estado de un elemento en un control de vista de árbol.
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4a19306855b7f38d03aa00323b26407f108bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660427"
---
# <a name="tree-view-control-item-states"></a><span data-ttu-id="99cbe-103">Estados de los elementos de control Tree-View</span><span class="sxs-lookup"><span data-stu-id="99cbe-103">Tree-View Control Item States</span></span>

<span data-ttu-id="99cbe-104">En esta sección se enumeran las marcas de estado del elemento que se usan para indicar el estado de un elemento en un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="99cbe-104">This section lists the item state flags used to indicate the state of an item in a tree-view control.</span></span>



| <span data-ttu-id="99cbe-105">Constante</span><span class="sxs-lookup"><span data-stu-id="99cbe-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="99cbe-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="99cbe-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <span data-ttu-id="99cbe-107"><dt>**TVIS \_ negrita**</dt></span><span class="sxs-lookup"><span data-stu-id="99cbe-107"><dt>**TVIS\_BOLD**</dt></span></span> </dl>                               | <span data-ttu-id="99cbe-108">El elemento está en negrita.</span><span class="sxs-lookup"><span data-stu-id="99cbe-108">The item is bold.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <span data-ttu-id="99cbe-109"><dt>**TVIS \_ cortar**</dt></span><span class="sxs-lookup"><span data-stu-id="99cbe-109"><dt>**TVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="99cbe-110">El elemento se selecciona como parte de una operación de cortar y pegar.</span><span class="sxs-lookup"><span data-stu-id="99cbe-110">The item is selected as part of a cut-and-paste operation.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <span data-ttu-id="99cbe-111"><dt>**TVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="99cbe-111"><dt>**TVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="99cbe-112">El elemento se selecciona como destino de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="99cbe-112">The item is selected as a drag-and-drop target.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <span data-ttu-id="99cbe-113"><dt>**TVIS \_ expandido**</dt></span><span class="sxs-lookup"><span data-stu-id="99cbe-113"><dt>**TVIS\_EXPANDED**</dt></span></span> </dl>                   | <span data-ttu-id="99cbe-114">La lista de elementos secundarios del elemento está expandida actualmente; es decir, los elementos secundarios son visibles.</span><span class="sxs-lookup"><span data-stu-id="99cbe-114">The item's list of child items is currently expanded; that is, the child items are visible.</span></span> <span data-ttu-id="99cbe-115">Este valor solo se aplica a los elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="99cbe-115">This value applies only to parent items.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <span data-ttu-id="99cbe-116"><dt>**TVIS \_ EXPANDEDONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="99cbe-116"><dt>**TVIS\_EXPANDEDONCE**</dt></span></span> </dl>       | <span data-ttu-id="99cbe-117">La lista de elementos secundarios del elemento se ha expandido al menos una vez.</span><span class="sxs-lookup"><span data-stu-id="99cbe-117">The item's list of child items has been expanded at least once.</span></span> <span data-ttu-id="99cbe-118">Los códigos de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) no se generan para los elementos primarios que tienen este estado establecido en respuesta a un mensaje de [**\_ expansión TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="99cbe-118">The [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes are not generated for parent items that have this state set in response to a [**TVM\_EXPAND**](tvm-expand.md) message.</span></span> <span data-ttu-id="99cbe-119">El uso de TVE \_ Collapse y TVE \_ COLLAPSERESET con **TVM \_ Expand** hará que se restablezca este estado.</span><span class="sxs-lookup"><span data-stu-id="99cbe-119">Using TVE\_COLLAPSE and TVE\_COLLAPSERESET with **TVM\_EXPAND** will cause this state to be reset.</span></span> <span data-ttu-id="99cbe-120">Este valor solo se aplica a los elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="99cbe-120">This value applies only to parent items.</span></span> <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <span data-ttu-id="99cbe-121"><dt>**TVIS \_ EXPANDPARTIAL**</dt></span><span class="sxs-lookup"><span data-stu-id="99cbe-121"><dt>**TVIS\_EXPANDPARTIAL**</dt></span></span> </dl>    | <span data-ttu-id="99cbe-122">**Versión 4,70**.</span><span class="sxs-lookup"><span data-stu-id="99cbe-122">**Version 4.70**.</span></span> <span data-ttu-id="99cbe-123">Un elemento de vista de árbol parcialmente expandido.</span><span class="sxs-lookup"><span data-stu-id="99cbe-123">A partially expanded tree-view item.</span></span> <span data-ttu-id="99cbe-124">En este estado, algunos, pero no todos, de los elementos secundarios son visibles y se muestra el símbolo más del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="99cbe-124">In this state, some, but not all, of the child items are visible and the parent item's plus symbol is displayed.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <span data-ttu-id="99cbe-125"><dt>**TVIS \_ seleccionado**</dt></span><span class="sxs-lookup"><span data-stu-id="99cbe-125"><dt>**TVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="99cbe-126">El elemento está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="99cbe-126">The item is selected.</span></span> <span data-ttu-id="99cbe-127">Su apariencia depende de si tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="99cbe-127">Its appearance depends on whether it has the focus.</span></span> <span data-ttu-id="99cbe-128">El elemento se dibujará con los colores del sistema para la selección.</span><span class="sxs-lookup"><span data-stu-id="99cbe-128">The item will be drawn using the system colors for selection.</span></span> <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <span data-ttu-id="99cbe-129"><dt>**TVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="99cbe-129"><dt>**TVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="99cbe-130">Máscara para los bits que se usan para especificar el índice de imagen de superposición del elemento.</span><span class="sxs-lookup"><span data-stu-id="99cbe-130">Mask for the bits used to specify the item's overlay image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <span data-ttu-id="99cbe-131"><dt>**TVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="99cbe-131"><dt>**TVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="99cbe-132">Máscara para los bits que se usan para especificar el índice de imagen de estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="99cbe-132">Mask for the bits used to specify the item's state image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <span data-ttu-id="99cbe-133"><dt>**TVIS \_ USERMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="99cbe-133"><dt>**TVIS\_USERMASK**</dt></span></span> </dl>                   | <span data-ttu-id="99cbe-134">Igual que **TVIS \_ STATEIMAGEMASK**.</span><span class="sxs-lookup"><span data-stu-id="99cbe-134">Same as **TVIS\_STATEIMAGEMASK**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="99cbe-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99cbe-135">Remarks</span></span>

<span data-ttu-id="99cbe-136">Al establecer o recuperar el índice de imagen de superposición de un elemento o el índice de imagen de estado, debe especificar las siguientes máscaras en el miembro **stateMask** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) :</span><span class="sxs-lookup"><span data-stu-id="99cbe-136">When you set or retrieve an item's overlay image index or state image index, you must specify the following masks in the **stateMask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure:</span></span>

-   <span data-ttu-id="99cbe-137">**TVIS \_ OVERLAYMASK**</span><span class="sxs-lookup"><span data-stu-id="99cbe-137">**TVIS\_OVERLAYMASK**</span></span>
-   <span data-ttu-id="99cbe-138">**TVIS \_ STATEIMAGEMASK**</span><span class="sxs-lookup"><span data-stu-id="99cbe-138">**TVIS\_STATEIMAGEMASK**</span></span>
-   <span data-ttu-id="99cbe-139">**TVIS \_ USERMASK**</span><span class="sxs-lookup"><span data-stu-id="99cbe-139">**TVIS\_USERMASK**</span></span>

<span data-ttu-id="99cbe-140">Estos valores también se pueden usar para enmascarar los bits de estado que no son de interés.</span><span class="sxs-lookup"><span data-stu-id="99cbe-140">These values can also be used to mask off the state bits that are not of interest.</span></span>

## <a name="requirements"></a><span data-ttu-id="99cbe-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99cbe-141">Requirements</span></span>



| <span data-ttu-id="99cbe-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="99cbe-142">Requirement</span></span> | <span data-ttu-id="99cbe-143">Value</span><span class="sxs-lookup"><span data-stu-id="99cbe-143">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99cbe-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99cbe-144">Header</span></span><br/> | <dl> <span data-ttu-id="99cbe-145"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="99cbe-145"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





