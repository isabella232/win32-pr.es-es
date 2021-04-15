---
title: Mensaje de LVM_DELETEALLITEMS (commctrl. h)
description: Quita todos los elementos de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro DeleteAllItems de ListView.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- LVM_DELETEALLITEMS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e92344e3cccf7578b8953206a9550022f6c6095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489094"
---
# <a name="lvm_deleteallitems-message"></a><span data-ttu-id="ee848-105">\_Mensaje DELETEALLITEMS LVM</span><span class="sxs-lookup"><span data-stu-id="ee848-105">LVM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="ee848-106">Quita todos los elementos de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="ee848-106">Removes all items from a list-view control.</span></span> <span data-ttu-id="ee848-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ DeleteAllItems de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) .</span><span class="sxs-lookup"><span data-stu-id="ee848-107">You can send this message explicitly or by using the [**ListView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee848-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee848-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee848-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee848-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ee848-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ee848-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ee848-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee848-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ee848-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ee848-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee848-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee848-113">Return value</span></span>

<span data-ttu-id="ee848-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ee848-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee848-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee848-115">Remarks</span></span>

<span data-ttu-id="ee848-116">Cuando un control de vista de lista recibe el mensaje **\_ DELETEALLITEMS LVM** , envía el código de notificación [**LVN \_ DELETEALLITEMS**](lvn-deleteallitems.md) a su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="ee848-116">When a list-view control receives the **LVM\_DELETEALLITEMS** message, it sends the [**LVN\_DELETEALLITEMS**](lvn-deleteallitems.md) notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee848-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee848-117">Requirements</span></span>



| <span data-ttu-id="ee848-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee848-118">Requirement</span></span> | <span data-ttu-id="ee848-119">Value</span><span class="sxs-lookup"><span data-stu-id="ee848-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee848-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee848-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ee848-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ee848-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee848-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee848-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ee848-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee848-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee848-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee848-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee848-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee848-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





