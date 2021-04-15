---
title: Mensaje de EM_EMPTYUNDOBUFFER (Winuser. h)
description: Restablece la marca de deshacer de un control de edición. La marca de deshacer se establece siempre que se puede deshacer una operación dentro del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- EM_EMPTYUNDOBUFFER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491495"
---
# <a name="em_emptyundobuffer-message"></a><span data-ttu-id="2b30e-106">\_Mensaje EMPTYUNDOBUFFER em</span><span class="sxs-lookup"><span data-stu-id="2b30e-106">EM\_EMPTYUNDOBUFFER message</span></span>

<span data-ttu-id="2b30e-107">Restablece la marca de deshacer de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="2b30e-107">Resets the undo flag of an edit control.</span></span> <span data-ttu-id="2b30e-108">La marca de deshacer se establece siempre que se puede deshacer una operación dentro del control de edición.</span><span class="sxs-lookup"><span data-stu-id="2b30e-108">The undo flag is set whenever an operation within the edit control can be undone.</span></span> <span data-ttu-id="2b30e-109">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="2b30e-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b30e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b30e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b30e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b30e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b30e-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2b30e-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2b30e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b30e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b30e-114">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2b30e-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b30e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b30e-115">Return value</span></span>

<span data-ttu-id="2b30e-116">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2b30e-116">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b30e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b30e-117">Remarks</span></span>

<span data-ttu-id="2b30e-118">El indicador de deshacer se restablece automáticamente siempre que el control de edición recibe un mensaje de [**\_ SETHANDLE**](em-sethandle.md) de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) o EM.</span><span class="sxs-lookup"><span data-stu-id="2b30e-118">The undo flag is automatically reset whenever the edit control receives a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) or [**EM\_SETHANDLE**](em-sethandle.md) message.</span></span>

<span data-ttu-id="2b30e-119">**Controles de edición y edición enriquecida 1,0:** El control solo puede deshacer o rehacer la operación más reciente.</span><span class="sxs-lookup"><span data-stu-id="2b30e-119">**Edit controls and Rich Edit 1.0:** The control can only undo or redo the most recent operation.</span></span>

<span data-ttu-id="2b30e-120">**Edición enriquecida 2,0 y versiones posteriores:** El **mensaje \_ EMPTYUNDOBUFFER em** vacía todos los búferes de deshacer y rehacer.</span><span class="sxs-lookup"><span data-stu-id="2b30e-120">**Rich Edit 2.0 and later:** The **EM\_EMPTYUNDOBUFFER** message empties all undo and redo buffers.</span></span> <span data-ttu-id="2b30e-121">Los controles Rich Edit permiten al usuario deshacer o rehacer varias operaciones.</span><span class="sxs-lookup"><span data-stu-id="2b30e-121">Rich edit controls enable the user to undo or redo multiple operations.</span></span>

<span data-ttu-id="2b30e-122">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2b30e-122">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="2b30e-123">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="2b30e-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b30e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b30e-124">Requirements</span></span>



| <span data-ttu-id="2b30e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b30e-125">Requirement</span></span> | <span data-ttu-id="2b30e-126">Value</span><span class="sxs-lookup"><span data-stu-id="2b30e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b30e-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b30e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2b30e-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2b30e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b30e-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b30e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2b30e-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b30e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2b30e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b30e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b30e-132"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b30e-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b30e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b30e-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="2b30e-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2b30e-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2b30e-135">**la \_ CANUNDO em**</span><span class="sxs-lookup"><span data-stu-id="2b30e-135">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="2b30e-136">**\_SETHANDLE em**</span><span class="sxs-lookup"><span data-stu-id="2b30e-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

[<span data-ttu-id="2b30e-137">**deshacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="2b30e-137">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

<span data-ttu-id="2b30e-138">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="2b30e-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2b30e-139">**SETTEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="2b30e-139">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

