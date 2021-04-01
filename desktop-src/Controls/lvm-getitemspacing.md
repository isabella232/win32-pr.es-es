---
title: Mensaje de LVM_GETITEMSPACING (commctrl. h)
description: Determina el espaciado entre los elementos de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemSpacing de ListView.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- LVM_GETITEMSPACING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996914"
---
# <a name="lvm_getitemspacing-message"></a><span data-ttu-id="ad040-105">\_Mensaje GETITEMSPACING LVM</span><span class="sxs-lookup"><span data-stu-id="ad040-105">LVM\_GETITEMSPACING message</span></span>

<span data-ttu-id="ad040-106">Determina el espaciado entre los elementos de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="ad040-106">Determines the spacing between items in a list-view control.</span></span> <span data-ttu-id="ad040-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemSpacing de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) .</span><span class="sxs-lookup"><span data-stu-id="ad040-107">You can send this message explicitly or by using the [**ListView\_GetItemSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ad040-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad040-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad040-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad040-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad040-110">Vista para la que se va a recuperar el espaciado del elemento.</span><span class="sxs-lookup"><span data-stu-id="ad040-110">View for which to retrieve the item spacing.</span></span> <span data-ttu-id="ad040-111">Este parámetro es **true** para la vista de iconos pequeños o **false** para la vista de iconos.</span><span class="sxs-lookup"><span data-stu-id="ad040-111">This parameter is **TRUE** for small icon view, or **FALSE** for icon view.</span></span>

</dd> <dt>

<span data-ttu-id="ad040-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad040-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ad040-113">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ad040-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad040-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad040-114">Return value</span></span>

<span data-ttu-id="ad040-115">Devuelve la cantidad de espaciado entre los elementos.</span><span class="sxs-lookup"><span data-stu-id="ad040-115">Returns the amount of spacing between items.</span></span> <span data-ttu-id="ad040-116">El espaciado horizontal está contenido en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y el espaciado vertical está incluido en el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ad040-116">The horizontal spacing is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical spacing is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad040-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad040-117">Requirements</span></span>



| <span data-ttu-id="ad040-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad040-118">Requirement</span></span> | <span data-ttu-id="ad040-119">Value</span><span class="sxs-lookup"><span data-stu-id="ad040-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad040-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad040-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ad040-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ad040-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad040-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad040-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ad040-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad040-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad040-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad040-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad040-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad040-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

