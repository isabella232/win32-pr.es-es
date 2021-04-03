---
title: Mensaje de TVM_SORTCHILDREN (commctrl. h)
description: Ordena los elementos secundarios del elemento primario especificado en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro SortChildren de TreeView.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- TVM_SORTCHILDREN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341591c31accb4aab0b49f611359a93ec99c0cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079705"
---
# <a name="tvm_sortchildren-message"></a><span data-ttu-id="90369-105">\_Mensaje de SORTCHILDREN TVM</span><span class="sxs-lookup"><span data-stu-id="90369-105">TVM\_SORTCHILDREN message</span></span>

<span data-ttu-id="90369-106">Ordena los elementos secundarios del elemento primario especificado en un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="90369-106">Sorts the child items of the specified parent item in a tree-view control.</span></span> <span data-ttu-id="90369-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SortChildren de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) .</span><span class="sxs-lookup"><span data-stu-id="90369-107">You can send this message explicitly or by using the [**TreeView\_SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="90369-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90369-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90369-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90369-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90369-110">Valor que especifica si la ordenación es recursiva.</span><span class="sxs-lookup"><span data-stu-id="90369-110">Value that specifies whether the sorting is recursive.</span></span> <span data-ttu-id="90369-111">Establezca *wParam* en **true** para ordenar todos los niveles de los elementos secundarios por debajo del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="90369-111">Set *wParam* to **TRUE** to sort all levels of child items below the parent item.</span></span> <span data-ttu-id="90369-112">De lo contrario, solo se ordenan los elementos secundarios inmediatos del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="90369-112">Otherwise, only the parent's immediate children are sorted.</span></span>

</dd> <dt>

<span data-ttu-id="90369-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90369-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90369-114">Identificador del elemento primario cuyos elementos secundarios se van a ordenar.</span><span class="sxs-lookup"><span data-stu-id="90369-114">Handle to the parent item whose child items are to be sorted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90369-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90369-115">Return value</span></span>

<span data-ttu-id="90369-116">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="90369-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="90369-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90369-117">Remarks</span></span>

<span data-ttu-id="90369-118">Este mensaje alphabetizes los elementos de árbol mediante [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) en el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="90369-118">This message alphabetizes the tree items using [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) on the item name.</span></span> <span data-ttu-id="90369-119">Puede usar el mensaje [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) para personalizar el comportamiento de ordenación.</span><span class="sxs-lookup"><span data-stu-id="90369-119">You can use the [**TVM\_SORTCHILDRENCB**](tvm-sortchildrencb.md) message to customize the ordering behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="90369-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90369-120">Requirements</span></span>



| <span data-ttu-id="90369-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="90369-121">Requirement</span></span> | <span data-ttu-id="90369-122">Value</span><span class="sxs-lookup"><span data-stu-id="90369-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90369-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90369-123">Minimum supported client</span></span><br/> | <span data-ttu-id="90369-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="90369-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90369-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90369-125">Minimum supported server</span></span><br/> | <span data-ttu-id="90369-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="90369-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90369-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90369-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="90369-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90369-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

