---
title: Mensaje de TVM_GETVISIBLECOUNT (commctrl. h)
description: Obtiene el número de elementos que pueden estar totalmente visibles en la ventana de cliente de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetVisibleCount de TreeView.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- TVM_GETVISIBLECOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1927d21741b109c5f00aa964b058dc0c34732529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996103"
---
# <a name="tvm_getvisiblecount-message"></a><span data-ttu-id="cb501-105">\_Mensaje de GETVISIBLECOUNT TVM</span><span class="sxs-lookup"><span data-stu-id="cb501-105">TVM\_GETVISIBLECOUNT message</span></span>

<span data-ttu-id="cb501-106">Obtiene el número de elementos que pueden estar totalmente visibles en la ventana de cliente de un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="cb501-106">Obtains the number of items that can be fully visible in the client window of a tree-view control.</span></span> <span data-ttu-id="cb501-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetVisibleCount de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) .</span><span class="sxs-lookup"><span data-stu-id="cb501-107">You can send this message explicitly or by using the [**TreeView\_GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb501-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb501-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb501-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb501-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cb501-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cb501-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cb501-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb501-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cb501-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cb501-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb501-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb501-113">Return value</span></span>

<span data-ttu-id="cb501-114">Devuelve el número de elementos que pueden estar totalmente visibles en la ventana del cliente del control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="cb501-114">Returns the number of items that can be fully visible in the client window of the tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb501-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb501-115">Remarks</span></span>

<span data-ttu-id="cb501-116">El número de elementos que pueden estar totalmente visibles puede ser mayor que el número de elementos del control.</span><span class="sxs-lookup"><span data-stu-id="cb501-116">The number of items that can be fully visible may be greater than the number of items in the control.</span></span> <span data-ttu-id="cb501-117">El control calcula este valor dividiendo el alto de la ventana del cliente por el alto de un elemento.</span><span class="sxs-lookup"><span data-stu-id="cb501-117">The control calculates this value by dividing the height of the client window by the height of an item.</span></span>

<span data-ttu-id="cb501-118">Tenga en cuenta que el valor devuelto es el número de elementos que pueden estar *totalmente* visibles.</span><span class="sxs-lookup"><span data-stu-id="cb501-118">Note that the return value is the number of items that can be *fully* visible.</span></span> <span data-ttu-id="cb501-119">Si puede ver todos los 20 elementos y parte de un elemento más, el valor devuelto es 20.</span><span class="sxs-lookup"><span data-stu-id="cb501-119">If you can see all of 20 items and part of one more item, the return value is 20.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb501-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb501-120">Requirements</span></span>



| <span data-ttu-id="cb501-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb501-121">Requirement</span></span> | <span data-ttu-id="cb501-122">Value</span><span class="sxs-lookup"><span data-stu-id="cb501-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb501-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb501-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cb501-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cb501-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb501-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb501-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cb501-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb501-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb501-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb501-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb501-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb501-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





