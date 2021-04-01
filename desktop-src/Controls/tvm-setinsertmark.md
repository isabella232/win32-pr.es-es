---
title: Mensaje de TVM_SETINSERTMARK (commctrl. h)
description: Establece la marca de inserción en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro SetInsertMark de TreeView.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- TVM_SETINSERTMARK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5a9cc9b05e9cd7dc3281d778734bee1048ffd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905348"
---
# <a name="tvm_setinsertmark-message"></a><span data-ttu-id="3c085-105">\_Mensaje de SETINSERTMARK TVM</span><span class="sxs-lookup"><span data-stu-id="3c085-105">TVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="3c085-106">Establece la marca de inserción en un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="3c085-106">Sets the insertion mark in a tree-view control.</span></span> <span data-ttu-id="3c085-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetInsertMark de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) .</span><span class="sxs-lookup"><span data-stu-id="3c085-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c085-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c085-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c085-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c085-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c085-110">Valor **booleano** que especifica si la marca de inserción se coloca antes o después del elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="3c085-110">**BOOL** value that specifies if the insertion mark is placed before or after the specified item.</span></span> <span data-ttu-id="3c085-111">Si este argumento es distinto de cero, la marca de inserción se colocará después del elemento.</span><span class="sxs-lookup"><span data-stu-id="3c085-111">If this argument is nonzero, the insertion mark will be placed after the item.</span></span> <span data-ttu-id="3c085-112">Si este argumento es cero, la marca de inserción se colocará delante del elemento.</span><span class="sxs-lookup"><span data-stu-id="3c085-112">If this argument is zero, the insertion mark will be placed before the item.</span></span>

</dd> <dt>

<span data-ttu-id="3c085-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c085-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c085-114">**HTREEITEM** que especifica en qué elemento se colocará la marca de inserción.</span><span class="sxs-lookup"><span data-stu-id="3c085-114">**HTREEITEM** that specifies at which item the insertion mark will be placed.</span></span> <span data-ttu-id="3c085-115">Si este argumento es **null**, se quita la marca de inserción.</span><span class="sxs-lookup"><span data-stu-id="3c085-115">If this argument is **NULL**, the insertion mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c085-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c085-116">Return value</span></span>

<span data-ttu-id="3c085-117">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="3c085-117">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c085-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c085-118">Remarks</span></span>

<span data-ttu-id="3c085-119">En algunas circunstancias, la marca de inserción puede aparecer en dos lugares después de expandir un nodo.</span><span class="sxs-lookup"><span data-stu-id="3c085-119">In some circumstances, the insert mark can appear in two places after a node is expanded.</span></span> <span data-ttu-id="3c085-120">Si usa marcas de inserción, se recomienda forzar una actualización del control después de expandir un nodo.</span><span class="sxs-lookup"><span data-stu-id="3c085-120">If you are using insertion marks, it is recommended that you force a refresh of the control after expanding a node.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c085-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c085-121">Requirements</span></span>



| <span data-ttu-id="3c085-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c085-122">Requirement</span></span> | <span data-ttu-id="3c085-123">Value</span><span class="sxs-lookup"><span data-stu-id="3c085-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c085-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c085-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3c085-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3c085-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c085-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c085-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3c085-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c085-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c085-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c085-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c085-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c085-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





