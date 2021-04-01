---
title: Mensaje de TTM_TRACKACTIVATE (commctrl. h)
description: Activa o desactiva una información sobre herramientas de seguimiento.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- TTM_TRACKACTIVATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996638"
---
# <a name="ttm_trackactivate-message"></a><span data-ttu-id="f25e5-104">TTM \_ TRACKACTIVATE</span><span class="sxs-lookup"><span data-stu-id="f25e5-104">TTM\_TRACKACTIVATE message</span></span>

<span data-ttu-id="f25e5-105">Activa o desactiva una información sobre herramientas de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f25e5-105">Activates or deactivates a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="f25e5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f25e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f25e5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f25e5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f25e5-108">Valor que especifica si el seguimiento se está activando o desactivando.</span><span class="sxs-lookup"><span data-stu-id="f25e5-108">Value specifying whether tracking is being activated or deactivated.</span></span> <span data-ttu-id="f25e5-109">Este valor puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f25e5-109">This value can be one of the following:</span></span>



| <span data-ttu-id="f25e5-110">Value</span><span class="sxs-lookup"><span data-stu-id="f25e5-110">Value</span></span>                                                                                                                                | <span data-ttu-id="f25e5-111">Significado</span><span class="sxs-lookup"><span data-stu-id="f25e5-111">Meaning</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="f25e5-112"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="f25e5-112"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="f25e5-113">Activar seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f25e5-113">Activate tracking.</span></span><br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="f25e5-114"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="f25e5-114"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="f25e5-115">Desactivar seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f25e5-115">Deactivate tracking.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f25e5-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f25e5-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f25e5-117">Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que identifica la herramienta a la que se aplica este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f25e5-117">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that identifies the tool to which this message applies.</span></span> <span data-ttu-id="f25e5-118">Los miembros **hWnd** y **uId** identifican la herramienta y el miembro **cbSize** especifica el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="f25e5-118">The **hwnd** and **uId** members identify the tool, and the **cbSize** member specifies the size of the structure.</span></span> <span data-ttu-id="f25e5-119">Se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="f25e5-119">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f25e5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f25e5-120">Return value</span></span>

<span data-ttu-id="f25e5-121">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f25e5-121">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f25e5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f25e5-122">Requirements</span></span>



| <span data-ttu-id="f25e5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f25e5-123">Requirement</span></span> | <span data-ttu-id="f25e5-124">Value</span><span class="sxs-lookup"><span data-stu-id="f25e5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f25e5-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f25e5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f25e5-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f25e5-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f25e5-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f25e5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f25e5-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f25e5-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f25e5-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f25e5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f25e5-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f25e5-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f25e5-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f25e5-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="f25e5-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f25e5-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f25e5-133">**TTM \_ TRACKPOSITION**</span><span class="sxs-lookup"><span data-stu-id="f25e5-133">**TTM\_TRACKPOSITION**</span></span>](ttm-trackposition.md)
</dt> <dt>

<span data-ttu-id="f25e5-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f25e5-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f25e5-135">Usar controles ToolTip</span><span class="sxs-lookup"><span data-stu-id="f25e5-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 





