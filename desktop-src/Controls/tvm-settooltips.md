---
title: Mensaje de TVM_SETTOOLTIPS (commctrl. h)
description: Establece un control de información sobre herramientas secundario del control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro SetToolTips de TreeView.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- TVM_SETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd9d5957a38d873993405a5283545472433e958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150265"
---
# <a name="tvm_settooltips-message"></a><span data-ttu-id="018a5-105">\_Mensaje de SETTOOLTIPS TVM</span><span class="sxs-lookup"><span data-stu-id="018a5-105">TVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="018a5-106">Establece un control de información sobre herramientas secundario del control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="018a5-106">Sets a tree-view control's child tooltip control.</span></span> <span data-ttu-id="018a5-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetToolTips de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="018a5-107">You can send this message explicitly or by using the [**TreeView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="018a5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="018a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="018a5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="018a5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="018a5-110">Identificador de un control de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="018a5-110">Handle to a tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="018a5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="018a5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="018a5-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="018a5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="018a5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="018a5-113">Return value</span></span>

<span data-ttu-id="018a5-114">Devuelve el identificador del control de información sobre herramientas previamente establecido para el control de vista de árbol o **null** si no se ha usado anteriormente la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="018a5-114">Returns the handle to tooltip control previously set for the tree-view control, or **NULL** if tooltips were not previously used.</span></span>

## <a name="remarks"></a><span data-ttu-id="018a5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="018a5-115">Remarks</span></span>

<span data-ttu-id="018a5-116">Cuando se crean, los controles de vista de árbol crean automáticamente un control ToolTip secundario.</span><span class="sxs-lookup"><span data-stu-id="018a5-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="018a5-117">Para evitar que un control de vista de árbol use la información sobre herramientas, cree el control con el estilo [**TV \_ notooltips**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="018a5-117">To prevent a tree-view control from using tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="018a5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="018a5-118">Requirements</span></span>



| <span data-ttu-id="018a5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="018a5-119">Requirement</span></span> | <span data-ttu-id="018a5-120">Value</span><span class="sxs-lookup"><span data-stu-id="018a5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="018a5-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="018a5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="018a5-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="018a5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="018a5-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="018a5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="018a5-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="018a5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="018a5-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="018a5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="018a5-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="018a5-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="018a5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="018a5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="018a5-128">**TVM \_ GETTOOLTIPS**</span><span class="sxs-lookup"><span data-stu-id="018a5-128">**TVM\_GETTOOLTIPS**</span></span>](tvm-gettooltips.md)
</dt> </dl>

 

 





