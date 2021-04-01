---
title: Mensaje de TVM_GETITEM (commctrl. h)
description: Recupera algunos o todos los atributos de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItem de TreeView.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- TVM_GETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151250"
---
# <a name="tvm_getitem-message"></a><span data-ttu-id="042ad-105">Mensaje de GETITEM de TVM \_</span><span class="sxs-lookup"><span data-stu-id="042ad-105">TVM\_GETITEM message</span></span>

<span data-ttu-id="042ad-106">Recupera algunos o todos los atributos de un elemento de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="042ad-106">Retrieves some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="042ad-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItem de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) .</span><span class="sxs-lookup"><span data-stu-id="042ad-107">You can send this message explicitly or by using the [**TreeView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="042ad-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="042ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="042ad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="042ad-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="042ad-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="042ad-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="042ad-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="042ad-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="042ad-112">Puntero a una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que especifica la información que se va a recuperar y recibe información sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="042ad-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that specifies the information to retrieve and receives information about the item.</span></span> <span data-ttu-id="042ad-113">Con la [versión 4,71](common-control-versions.md) y versiones posteriores, puede usar una estructura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="042ad-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="042ad-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="042ad-114">Return value</span></span>

<span data-ttu-id="042ad-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="042ad-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="042ad-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="042ad-116">Remarks</span></span>

<span data-ttu-id="042ad-117">Cuando se envía el mensaje, el miembro **hItem** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica el elemento del que se va a recuperar información y el miembro **Mask** especifica los atributos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="042ad-117">When the message is sent, the **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item to retrieve information about, and the **mask** member specifies the attributes to retrieve.</span></span>

<span data-ttu-id="042ad-118">Si la \_ marca de texto TVIF se establece en el miembro **Mask** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) , el miembro **miembros pszText** debe apuntar a un búfer válido y el miembro **cchTextMax** debe establecerse en el número de caracteres de ese búfer.</span><span class="sxs-lookup"><span data-stu-id="042ad-118">If the TVIF\_TEXT flag is set in the **mask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="042ad-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="042ad-119">Requirements</span></span>



| <span data-ttu-id="042ad-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="042ad-120">Requirement</span></span> | <span data-ttu-id="042ad-121">Value</span><span class="sxs-lookup"><span data-stu-id="042ad-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="042ad-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="042ad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="042ad-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="042ad-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="042ad-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="042ad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="042ad-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="042ad-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="042ad-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="042ad-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="042ad-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="042ad-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="042ad-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="042ad-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="042ad-129">**TVM \_ GETITEMW** (Unicode) y **TVM \_ GETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="042ad-129">**TVM\_GETITEMW** (Unicode) and **TVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





