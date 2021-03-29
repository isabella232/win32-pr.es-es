---
title: Mensaje de TVM_GETCOUNT (commctrl. h)
description: Recupera un recuento de los elementos de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro getCount de TreeView.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- TVM_GETCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492371"
---
# <a name="tvm_getcount-message"></a><span data-ttu-id="09d2a-105">Mensaje de la GETCOUNT de TVM \_</span><span class="sxs-lookup"><span data-stu-id="09d2a-105">TVM\_GETCOUNT message</span></span>

<span data-ttu-id="09d2a-106">Recupera un recuento de los elementos de un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="09d2a-106">Retrieves a count of the items in a tree-view control.</span></span> <span data-ttu-id="09d2a-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ getCount de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) .</span><span class="sxs-lookup"><span data-stu-id="09d2a-107">You can send this message explicitly or by using the [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="09d2a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09d2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09d2a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09d2a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="09d2a-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="09d2a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="09d2a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09d2a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="09d2a-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="09d2a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09d2a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09d2a-113">Return value</span></span>

<span data-ttu-id="09d2a-114">Devuelve el recuento de elementos.</span><span class="sxs-lookup"><span data-stu-id="09d2a-114">Returns the count of items.</span></span>

## <a name="remarks"></a><span data-ttu-id="09d2a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09d2a-115">Remarks</span></span>

<span data-ttu-id="09d2a-116">El número de nodos devueltos por la función [**\_ getCount de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) se limita a los valores enteros.</span><span class="sxs-lookup"><span data-stu-id="09d2a-116">The node count returned by [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) is limited to integer values.</span></span> <span data-ttu-id="09d2a-117">Si agrega un nodo más allá de 32767, la macro devuelve un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="09d2a-117">If you add a node beyond 32767 the macro returns a negative value.</span></span> <span data-ttu-id="09d2a-118">Después de agregar 65536 nodos, el recuento vuelve a cero.</span><span class="sxs-lookup"><span data-stu-id="09d2a-118">After adding 65536 nodes the count returns to zero.</span></span> <span data-ttu-id="09d2a-119">Cuando esto ocurre, el control de vista de árbol aparece vacío sin barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="09d2a-119">When this occurs, the tree-view control appears empty with no scrollbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="09d2a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09d2a-120">Requirements</span></span>



| <span data-ttu-id="09d2a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="09d2a-121">Requirement</span></span> | <span data-ttu-id="09d2a-122">Value</span><span class="sxs-lookup"><span data-stu-id="09d2a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09d2a-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09d2a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="09d2a-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="09d2a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09d2a-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09d2a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="09d2a-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="09d2a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09d2a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09d2a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="09d2a-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="09d2a-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





