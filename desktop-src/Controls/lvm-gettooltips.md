---
title: Mensaje de LVM_GETTOOLTIPS (commctrl. h)
description: Recupera el control de información sobre herramientas que el control de vista de lista utiliza para mostrar la información sobre herramientas. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetToolTips de ListView.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- LVM_GETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492401"
---
# <a name="lvm_gettooltips-message"></a><span data-ttu-id="17a18-105">\_Mensaje GETTOOLTIPS LVM</span><span class="sxs-lookup"><span data-stu-id="17a18-105">LVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="17a18-106">Recupera el control de información sobre herramientas que el control de vista de lista utiliza para mostrar la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="17a18-106">Retrieves the tooltip control that the list-view control uses to display tooltips.</span></span> <span data-ttu-id="17a18-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetToolTips de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="17a18-107">You can send this message explicitly or use the [**ListView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="17a18-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17a18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17a18-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17a18-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="17a18-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="17a18-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="17a18-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17a18-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="17a18-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="17a18-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17a18-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17a18-113">Return value</span></span>

<span data-ttu-id="17a18-114">Devuelve el identificador del control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="17a18-114">Returns the handle of the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a18-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17a18-115">Requirements</span></span>



| <span data-ttu-id="17a18-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="17a18-116">Requirement</span></span> | <span data-ttu-id="17a18-117">Value</span><span class="sxs-lookup"><span data-stu-id="17a18-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17a18-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17a18-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17a18-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="17a18-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17a18-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17a18-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17a18-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="17a18-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17a18-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17a18-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="17a18-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="17a18-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17a18-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="17a18-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a18-125">**\_SETTOOLTIPS LVM**</span><span class="sxs-lookup"><span data-stu-id="17a18-125">**LVM\_SETTOOLTIPS**</span></span>](lvm-settooltips.md)
</dt> </dl>

 

 





