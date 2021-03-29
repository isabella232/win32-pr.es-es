---
title: Mensaje de TVM_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera el estilo extendido para un control de vista de árbol. Envíe este mensaje explícitamente o mediante la \_ macro GetExtendedStyle de TreeView.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- TVM_GETEXTENDEDSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a00e125389ff56c7ff93370ab71945598dba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905584"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a><span data-ttu-id="e5d58-105">Mensaje de TVM_GETEXTENDEDSTYLE (commctrl. h)</span><span class="sxs-lookup"><span data-stu-id="e5d58-105">TVM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="e5d58-106">Recupera el estilo extendido para un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="e5d58-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="e5d58-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetExtendedStyle de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="e5d58-107">Send this message explicitly or by using the [**TreeView\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5d58-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5d58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5d58-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5d58-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e5d58-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e5d58-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e5d58-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5d58-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e5d58-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e5d58-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5d58-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5d58-113">Return value</span></span>

<span data-ttu-id="e5d58-114">Devuelve el valor de estilo extendido. Para obtener más información sobre los estilos, vea los [estilos extendidos del control de vista de árbol](tree-view-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="e5d58-114">Returns the value of extended style.For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e5d58-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5d58-115">Remarks</span></span>

<span data-ttu-id="e5d58-116">Los estilos extendidos para un control de vista de árbol no tienen nada que ver con los estilos extendidos que se usan con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="e5d58-116">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d58-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5d58-117">Requirements</span></span>



| <span data-ttu-id="e5d58-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5d58-118">Requirement</span></span> | <span data-ttu-id="e5d58-119">Value</span><span class="sxs-lookup"><span data-stu-id="e5d58-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d58-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5d58-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d58-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e5d58-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e5d58-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5d58-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d58-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e5d58-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5d58-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5d58-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5d58-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5d58-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

