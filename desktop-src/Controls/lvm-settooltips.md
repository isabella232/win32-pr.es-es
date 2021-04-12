---
title: Mensaje de LVM_SETTOOLTIPS (commctrl. h)
description: Establece el control de información sobre herramientas que el control de vista de lista usará para mostrar la información sobre herramientas. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetToolTips de ListView.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- LVM_SETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489965"
---
# <a name="lvm_settooltips-message"></a><span data-ttu-id="413f1-105">\_Mensaje SETTOOLTIPS LVM</span><span class="sxs-lookup"><span data-stu-id="413f1-105">LVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="413f1-106">Establece el control de información sobre herramientas que el control de vista de lista usará para mostrar la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="413f1-106">Sets the tooltip control that the list-view control will use to display tooltips.</span></span> <span data-ttu-id="413f1-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetToolTips de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="413f1-107">You can send this message explicitly or use the [**ListView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="413f1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="413f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="413f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="413f1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="413f1-110">Identificador del control de información sobre herramientas que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="413f1-110">Handle to the tooltip control to be set.</span></span></dd> <dt>

<span data-ttu-id="413f1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="413f1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="413f1-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="413f1-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="413f1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="413f1-113">Return value</span></span>

<span data-ttu-id="413f1-114">Devuelve el identificador del control de información sobre herramientas anterior.</span><span class="sxs-lookup"><span data-stu-id="413f1-114">Returns the handle to the previous tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="413f1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="413f1-115">Requirements</span></span>



| <span data-ttu-id="413f1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="413f1-116">Requirement</span></span> | <span data-ttu-id="413f1-117">Value</span><span class="sxs-lookup"><span data-stu-id="413f1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="413f1-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="413f1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="413f1-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="413f1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="413f1-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="413f1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="413f1-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="413f1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="413f1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="413f1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="413f1-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="413f1-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="413f1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="413f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="413f1-125">**\_GETTOOLTIPS LVM**</span><span class="sxs-lookup"><span data-stu-id="413f1-125">**LVM\_GETTOOLTIPS**</span></span>](lvm-gettooltips.md)
</dt> </dl>

 

 





