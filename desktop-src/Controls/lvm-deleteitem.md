---
title: Mensaje de LVM_DELETEITEM (commctrl. h)
description: Quita un elemento de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro DeleteItem de ListView.
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- LVM_DELETEITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19fce5afbbaa6702f296df12acf7dad4edac16fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149905"
---
# <a name="lvm_deleteitem-message"></a><span data-ttu-id="eb173-105">Mensaje de LVM \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="eb173-105">LVM\_DELETEITEM message</span></span>

<span data-ttu-id="eb173-106">Quita un elemento de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="eb173-106">Removes an item from a list-view control.</span></span> <span data-ttu-id="eb173-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ DeleteItem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="eb173-107">You can send this message explicitly or by using the [**ListView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb173-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb173-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb173-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb173-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb173-110">Índice del elemento de vista de lista que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="eb173-110">The index of the list-view item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="eb173-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb173-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eb173-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="eb173-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb173-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb173-113">Return value</span></span>

<span data-ttu-id="eb173-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="eb173-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb173-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb173-115">Requirements</span></span>



| <span data-ttu-id="eb173-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb173-116">Requirement</span></span> | <span data-ttu-id="eb173-117">Value</span><span class="sxs-lookup"><span data-stu-id="eb173-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb173-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb173-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eb173-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eb173-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb173-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb173-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eb173-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="eb173-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb173-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb173-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb173-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb173-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





