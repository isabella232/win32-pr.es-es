---
title: Mensaje de EM_CANUNDO (Winuser. h)
description: Determina si hay alguna acción en la cola de deshacer del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- EM_CANUNDO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150560"
---
# <a name="em_canundo-message"></a><span data-ttu-id="a3737-105">\_Mensaje de CANUNDO em</span><span class="sxs-lookup"><span data-stu-id="a3737-105">EM\_CANUNDO message</span></span>

<span data-ttu-id="a3737-106">Determina si hay alguna acción en la cola de deshacer del control de edición.</span><span class="sxs-lookup"><span data-stu-id="a3737-106">Determines whether there are any actions in an edit control's undo queue.</span></span> <span data-ttu-id="a3737-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a3737-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3737-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3737-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3737-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3737-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3737-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a3737-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a3737-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3737-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3737-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a3737-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3737-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3737-113">Return value</span></span>

<span data-ttu-id="a3737-114">Si hay acciones en la cola de deshacer del control, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a3737-114">If there are actions in the control's undo queue, the return value is nonzero.</span></span>

<span data-ttu-id="a3737-115">Si la cola de deshacer está vacía, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="a3737-115">If the undo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3737-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3737-116">Remarks</span></span>

<span data-ttu-id="a3737-117">Si la cola de deshacer no está vacía, puede enviar el mensaje de [**\_ Deshacer em**](em-undo.md) al control para deshacer la operación más reciente.</span><span class="sxs-lookup"><span data-stu-id="a3737-117">If the undo queue is not empty, you can send the [**EM\_UNDO**](em-undo.md) message to the control to undo the most recent operation.</span></span>

<span data-ttu-id="a3737-118">**Controles de edición y edición enriquecida 1,0:** La cola de deshacer solo contiene la operación más reciente.</span><span class="sxs-lookup"><span data-stu-id="a3737-118">**Edit controls and Rich Edit 1.0:** The undo queue contains only the most recent operation.</span></span>

<span data-ttu-id="a3737-119">**Edición enriquecida 2,0 y versiones posteriores:** La cola de deshacer puede contener varias operaciones.</span><span class="sxs-lookup"><span data-stu-id="a3737-119">**Rich Edit 2.0 and later:** The undo queue can contain multiple operations.</span></span>

<span data-ttu-id="a3737-120">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a3737-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="a3737-121">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a3737-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3737-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3737-122">Requirements</span></span>



| <span data-ttu-id="a3737-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3737-123">Requirement</span></span> | <span data-ttu-id="a3737-124">Value</span><span class="sxs-lookup"><span data-stu-id="a3737-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3737-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3737-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a3737-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a3737-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a3737-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3737-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a3737-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a3737-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a3737-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3737-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3737-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3737-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3737-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3737-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3737-132">**deshacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="a3737-132">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





