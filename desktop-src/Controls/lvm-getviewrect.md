---
title: Mensaje de LVM_GETVIEWRECT (commctrl. h)
description: Recupera el rectángulo delimitador de todos los elementos del control de vista de lista. La vista de lista debe estar en el icono o en la vista de iconos pequeños. Puede enviar este mensaje explícitamente o mediante la \_ macro GetViewRect de ListView.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- LVM_GETVIEWRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079650"
---
# <a name="lvm_getviewrect-message"></a><span data-ttu-id="5c332-106">\_Mensaje GETVIEWRECT LVM</span><span class="sxs-lookup"><span data-stu-id="5c332-106">LVM\_GETVIEWRECT message</span></span>

<span data-ttu-id="5c332-107">Recupera el rectángulo delimitador de todos los elementos del control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="5c332-107">Retrieves the bounding rectangle of all items in the list-view control.</span></span> <span data-ttu-id="5c332-108">La vista de lista debe estar en el icono o en la vista de iconos pequeños.</span><span class="sxs-lookup"><span data-stu-id="5c332-108">The list view must be in icon or small icon view.</span></span> <span data-ttu-id="5c332-109">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetViewRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) .</span><span class="sxs-lookup"><span data-stu-id="5c332-109">You can send this message explicitly or by using the [**ListView\_GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c332-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c332-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c332-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c332-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5c332-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5c332-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5c332-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c332-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c332-114">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="5c332-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="5c332-115">Todas las coordenadas son relativas al área visible del control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="5c332-115">All coordinates are relative to the visible area of the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c332-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c332-116">Return value</span></span>

<span data-ttu-id="5c332-117">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5c332-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c332-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c332-118">Requirements</span></span>



| <span data-ttu-id="5c332-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c332-119">Requirement</span></span> | <span data-ttu-id="5c332-120">Value</span><span class="sxs-lookup"><span data-stu-id="5c332-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c332-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c332-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5c332-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5c332-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c332-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c332-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5c332-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c332-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c332-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c332-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c332-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c332-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

