---
title: Mensaje de EM_UNDO (Winuser. h)
description: Este mensaje deshace la última operación de control de edición en la cola de deshacer del control. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- EM_UNDO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c75d79e7ed25e582682830b1323c27878bbdbb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802335"
---
# <a name="em_undo-message"></a><span data-ttu-id="e0d25-105">\_Mensaje de deshacer em</span><span class="sxs-lookup"><span data-stu-id="e0d25-105">EM\_UNDO message</span></span>

<span data-ttu-id="e0d25-106">Este mensaje deshace la última operación de control de edición en la cola de deshacer del control.</span><span class="sxs-lookup"><span data-stu-id="e0d25-106">This message undoes the last edit control operation in the control's undo queue.</span></span> <span data-ttu-id="e0d25-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="e0d25-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0d25-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0d25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0d25-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0d25-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0d25-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e0d25-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e0d25-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0d25-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0d25-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e0d25-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0d25-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0d25-113">Return value</span></span>

<span data-ttu-id="e0d25-114">Para un control de edición de una sola línea, el valor devuelto siempre es **true**.</span><span class="sxs-lookup"><span data-stu-id="e0d25-114">For a single-line edit control, the return value is always **TRUE**.</span></span>

<span data-ttu-id="e0d25-115">Para un control de edición multilínea, el valor devuelto es **true** si la operación de deshacer se realiza correctamente, o **false** si se produce un error en la operación de deshacer.</span><span class="sxs-lookup"><span data-stu-id="e0d25-115">For a multiline edit control, the return value is **TRUE** if the undo operation is successful, or **FALSE** if the undo operation fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0d25-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0d25-116">Remarks</span></span>

<span data-ttu-id="e0d25-117">**Controles de edición y edición enriquecida 1,0:** También se puede deshacer una operación de deshacer.</span><span class="sxs-lookup"><span data-stu-id="e0d25-117">**Edit controls and Rich Edit 1.0:** An undo operation can also be undone.</span></span> <span data-ttu-id="e0d25-118">Por ejemplo, puede restaurar el texto eliminado con el primer mensaje de **\_ Deshacer em** y volver a quitar el texto con un segundo mensaje de **\_ Deshacer de EM** siempre que no haya ninguna operación de edición que intervenga.</span><span class="sxs-lookup"><span data-stu-id="e0d25-118">For example, you can restore deleted text with the first **EM\_UNDO** message, and remove the text again with a second **EM\_UNDO** message as long as there is no intervening edit operation.</span></span>

<span data-ttu-id="e0d25-119">**Edición enriquecida 2,0 y versiones posteriores:** La característica deshacer es multinivel, por lo que el envío de dos mensajes de **\_ Deshacer largos** deshará las dos últimas operaciones en la cola de deshacer.</span><span class="sxs-lookup"><span data-stu-id="e0d25-119">**Rich Edit 2.0 and later:** The undo feature is multilevel so sending two **EM\_UNDO** messages will undo the last two operations in the undo queue.</span></span> <span data-ttu-id="e0d25-120">Para rehacer una operación, envíe el mensaje de [**\_ rehacer em**](em-redo.md) .</span><span class="sxs-lookup"><span data-stu-id="e0d25-120">To redo an operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

<span data-ttu-id="e0d25-121">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e0d25-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="e0d25-122">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e0d25-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0d25-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0d25-123">Requirements</span></span>



| <span data-ttu-id="e0d25-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0d25-124">Requirement</span></span> | <span data-ttu-id="e0d25-125">Value</span><span class="sxs-lookup"><span data-stu-id="e0d25-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d25-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0d25-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e0d25-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e0d25-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e0d25-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0d25-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e0d25-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0d25-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e0d25-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0d25-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0d25-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0d25-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0d25-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0d25-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0d25-133">**la \_ CANUNDO em**</span><span class="sxs-lookup"><span data-stu-id="e0d25-133">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> </dl>

 

 





