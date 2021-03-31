---
title: Mensaje de TVM_GETITEMSTATE (commctrl. h)
description: Recupera algunos o todos los atributos de estado de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemState de TreeView.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- TVM_GETITEMSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079552"
---
# <a name="tvm_getitemstate-message"></a><span data-ttu-id="cf346-105">\_Mensaje de GETITEMSTATE TVM</span><span class="sxs-lookup"><span data-stu-id="cf346-105">TVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="cf346-106">Recupera algunos o todos los atributos de estado de un elemento de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="cf346-106">Retrieves some or all of a tree-view item's state attributes.</span></span> <span data-ttu-id="cf346-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemState de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) .</span><span class="sxs-lookup"><span data-stu-id="cf346-107">You can send this message explicitly or by using the [**TreeView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf346-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf346-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf346-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf346-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf346-110">Identificador del elemento.</span><span class="sxs-lookup"><span data-stu-id="cf346-110">Handle to the item.</span></span>

</dd> <dt>

<span data-ttu-id="cf346-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf346-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf346-112">Máscara que se usa para especificar los Estados que se van a consultar.</span><span class="sxs-lookup"><span data-stu-id="cf346-112">Mask used to specify the states to query for.</span></span> <span data-ttu-id="cf346-113">Es equivalente al miembro **stateMask** de [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span><span class="sxs-lookup"><span data-stu-id="cf346-113">It is equivalent to the **stateMask** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf346-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf346-114">Return value</span></span>

<span data-ttu-id="cf346-115">Devuelve un valor **uint** con los bits de estado adecuados establecidos en **true**.</span><span class="sxs-lookup"><span data-stu-id="cf346-115">Returns a **UINT** value with the appropriate state bits set to **TRUE**.</span></span> <span data-ttu-id="cf346-116">Solo se establecerán los bits especificados por *lParam* y que sean **true** .</span><span class="sxs-lookup"><span data-stu-id="cf346-116">Only those bits that are specified by *lParam* and that are **TRUE** will be set.</span></span> <span data-ttu-id="cf346-117">Este valor es equivalente al miembro **State** de [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span><span class="sxs-lookup"><span data-stu-id="cf346-117">This value is equivalent to the **state** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf346-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf346-118">Requirements</span></span>



| <span data-ttu-id="cf346-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf346-119">Requirement</span></span> | <span data-ttu-id="cf346-120">Value</span><span class="sxs-lookup"><span data-stu-id="cf346-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf346-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf346-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cf346-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cf346-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf346-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf346-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cf346-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf346-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf346-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf346-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf346-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf346-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





