---
title: Mensaje de TVM_GETTOOLTIPS (commctrl. h)
description: Recupera el identificador del control de información sobre herramientas secundario utilizado por un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetToolTips de TreeView.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- TVM_GETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489790"
---
# <a name="tvm_gettooltips-message"></a><span data-ttu-id="d1977-105">\_Mensaje de GETTOOLTIPS TVM</span><span class="sxs-lookup"><span data-stu-id="d1977-105">TVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="d1977-106">Recupera el identificador del control de información sobre herramientas secundario utilizado por un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="d1977-106">Retrieves the handle to the child tooltip control used by a tree-view control.</span></span> <span data-ttu-id="d1977-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetToolTips de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="d1977-107">You can send this message explicitly or by using the [**TreeView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1977-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1977-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1977-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1977-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d1977-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d1977-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d1977-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1977-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d1977-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d1977-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1977-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1977-113">Return value</span></span>

<span data-ttu-id="d1977-114">Devuelve el identificador del control de información sobre herramientas secundario, o **null** si el control no usa información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="d1977-114">Returns the handle to the child tooltip control, or **NULL** if the control is not using tooltips.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1977-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1977-115">Remarks</span></span>

<span data-ttu-id="d1977-116">Cuando se crean, los controles de vista de árbol crean automáticamente un control ToolTip secundario.</span><span class="sxs-lookup"><span data-stu-id="d1977-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="d1977-117">Para hacer que un control de vista de árbol no use la información sobre herramientas, cree el control con el estilo [**TV \_ notooltips**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d1977-117">To cause a tree-view control not to use tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1977-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1977-118">Requirements</span></span>



| <span data-ttu-id="d1977-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1977-119">Requirement</span></span> | <span data-ttu-id="d1977-120">Value</span><span class="sxs-lookup"><span data-stu-id="d1977-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1977-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1977-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d1977-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d1977-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1977-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1977-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d1977-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1977-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1977-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1977-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1977-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1977-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1977-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1977-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1977-128">**TVM \_ SETTOOLTIPS**</span><span class="sxs-lookup"><span data-stu-id="d1977-128">**TVM\_SETTOOLTIPS**</span></span>](tvm-settooltips.md)
</dt> </dl>

 

 





