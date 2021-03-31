---
title: Mensaje de TVM_ENSUREVISIBLE (commctrl. h)
description: Garantiza que un elemento de vista de árbol está visible, expandiendo el elemento primario o desplazándose por el control de vista de árbol, si es necesario. Puede enviar este mensaje explícitamente o mediante la \_ macro ensureVisible de TreeView.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- TVM_ENSUREVISIBLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06100ee33106736076608aa216d2aebc03b76ebe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996205"
---
# <a name="tvm_ensurevisible-message"></a><span data-ttu-id="b7a52-105">Mensaje de la \_ ENSUREVISIBLE TVM</span><span class="sxs-lookup"><span data-stu-id="b7a52-105">TVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="b7a52-106">Garantiza que un elemento de vista de árbol está visible, expandiendo el elemento primario o desplazándose por el control de vista de árbol, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="b7a52-106">Ensures that a tree-view item is visible, expanding the parent item or scrolling the tree-view control, if necessary.</span></span> <span data-ttu-id="b7a52-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ ensureVisible de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) .</span><span class="sxs-lookup"><span data-stu-id="b7a52-107">You can send this message explicitly or by using the [**TreeView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7a52-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7a52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7a52-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7a52-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b7a52-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b7a52-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b7a52-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7a52-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7a52-112">Identificador del elemento.</span><span class="sxs-lookup"><span data-stu-id="b7a52-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7a52-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7a52-113">Return value</span></span>

<span data-ttu-id="b7a52-114">Devuelve un valor distinto de cero si el sistema desplazó los elementos del control de vista de árbol y no se expandió ningún elemento.</span><span class="sxs-lookup"><span data-stu-id="b7a52-114">Returns nonzero if the system scrolled the items in the tree-view control and no items were expanded.</span></span> <span data-ttu-id="b7a52-115">De lo contrario, el mensaje devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="b7a52-115">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7a52-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7a52-116">Remarks</span></span>

<span data-ttu-id="b7a52-117">Si el mensaje de la \_ ENSUREVISIBLE TVM expande el elemento primario, la ventana primaria recibe los códigos de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .</span><span class="sxs-lookup"><span data-stu-id="b7a52-117">If the TVM\_ENSUREVISIBLE message expands the parent item, the parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7a52-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7a52-118">Requirements</span></span>



| <span data-ttu-id="b7a52-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7a52-119">Requirement</span></span> | <span data-ttu-id="b7a52-120">Value</span><span class="sxs-lookup"><span data-stu-id="b7a52-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7a52-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7a52-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7a52-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b7a52-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7a52-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7a52-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7a52-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7a52-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7a52-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7a52-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7a52-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7a52-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





