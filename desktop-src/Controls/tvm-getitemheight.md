---
title: Mensaje de TVM_GETITEMHEIGHT (commctrl. h)
description: Recupera el alto actual de cada elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemHeight de TreeView.
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- TVM_GETITEMHEIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905675"
---
# <a name="tvm_getitemheight-message"></a><span data-ttu-id="39a0d-105">\_Mensaje de GETITEMHEIGHT TVM</span><span class="sxs-lookup"><span data-stu-id="39a0d-105">TVM\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="39a0d-106">Recupera el alto actual de cada elemento de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="39a0d-106">Retrieves the current height of the each tree-view item.</span></span> <span data-ttu-id="39a0d-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemHeight de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) .</span><span class="sxs-lookup"><span data-stu-id="39a0d-107">You can send this message explicitly or by using the [**TreeView\_GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="39a0d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39a0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a0d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39a0d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="39a0d-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="39a0d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="39a0d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39a0d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="39a0d-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="39a0d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39a0d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39a0d-113">Return value</span></span>

<span data-ttu-id="39a0d-114">Devuelve el alto de cada elemento, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="39a0d-114">Returns the height of each item, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="39a0d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39a0d-115">Requirements</span></span>



| <span data-ttu-id="39a0d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="39a0d-116">Requirement</span></span> | <span data-ttu-id="39a0d-117">Value</span><span class="sxs-lookup"><span data-stu-id="39a0d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39a0d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39a0d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="39a0d-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="39a0d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39a0d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39a0d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="39a0d-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="39a0d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39a0d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39a0d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="39a0d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="39a0d-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a0d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="39a0d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a0d-125">**TVM \_ SETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="39a0d-125">**TVM\_SETITEMHEIGHT**</span></span>](tvm-setitemheight.md)
</dt> </dl>

 

 





