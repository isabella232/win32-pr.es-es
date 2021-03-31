---
title: Mensaje de TVM_SETITEM (commctrl. h)
description: El \_ mensaje TVM SETITEM establece algunos o todos los atributos de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro SetItem de TreeView.
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- TVM_SETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95750af3aa43a25f0ff4eae5533df5d9aef23537
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490841"
---
# <a name="tvm_setitem-message"></a><span data-ttu-id="f414f-105">\_Mensaje de SETITEM TVM</span><span class="sxs-lookup"><span data-stu-id="f414f-105">TVM\_SETITEM message</span></span>

<span data-ttu-id="f414f-106">El mensaje **TVM \_ SETITEM** establece algunos o todos los atributos de un elemento de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="f414f-106">The **TVM\_SETITEM** message sets some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="f414f-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItem de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) .</span><span class="sxs-lookup"><span data-stu-id="f414f-107">You can send this message explicitly or by using the [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f414f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f414f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f414f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f414f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f414f-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f414f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f414f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f414f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f414f-112">Puntero a una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene los nuevos atributos de elemento.</span><span class="sxs-lookup"><span data-stu-id="f414f-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="f414f-113">Con la [versión 4,71](common-control-versions.md) y versiones posteriores, puede usar una estructura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f414f-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f414f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f414f-114">Return value</span></span>

<span data-ttu-id="f414f-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f414f-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f414f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f414f-116">Remarks</span></span>

<span data-ttu-id="f414f-117">El miembro **hItem** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica el elemento y el miembro **Mask** especifica los atributos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="f414f-117">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item, and the **mask** member specifies which attributes to set.</span></span>

## <a name="requirements"></a><span data-ttu-id="f414f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f414f-118">Requirements</span></span>



| <span data-ttu-id="f414f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f414f-119">Requirement</span></span> | <span data-ttu-id="f414f-120">Value</span><span class="sxs-lookup"><span data-stu-id="f414f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f414f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f414f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f414f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f414f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f414f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f414f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f414f-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f414f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f414f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f414f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f414f-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f414f-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f414f-127">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f414f-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f414f-128">**TVM \_ SETITEMW** (Unicode) y **TVM \_ SETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f414f-128">**TVM\_SETITEMW** (Unicode) and **TVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





