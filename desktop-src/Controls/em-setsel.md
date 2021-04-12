---
title: Mensaje de EM_SETSEL (Winuser. h)
description: Selecciona un intervalo de caracteres en un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4981fa179ae4bdd454ab0b0a6d7485185ed31d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489989"
---
# <a name="em_setsel-message"></a><span data-ttu-id="293db-105">\_Mensaje SETSEL em</span><span class="sxs-lookup"><span data-stu-id="293db-105">EM\_SETSEL message</span></span>

<span data-ttu-id="293db-106">Selecciona un intervalo de caracteres en un control de edición.</span><span class="sxs-lookup"><span data-stu-id="293db-106">Selects a range of characters in an edit control.</span></span> <span data-ttu-id="293db-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="293db-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="293db-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="293db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="293db-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="293db-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="293db-110">Posición del carácter inicial de la selección.</span><span class="sxs-lookup"><span data-stu-id="293db-110">The starting character position of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="293db-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="293db-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="293db-112">Posición del carácter final de la selección.</span><span class="sxs-lookup"><span data-stu-id="293db-112">The ending character position of the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="293db-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="293db-113">Return value</span></span>

<span data-ttu-id="293db-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="293db-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="293db-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="293db-115">Remarks</span></span>

<span data-ttu-id="293db-116">El valor inicial puede ser mayor que el valor final.</span><span class="sxs-lookup"><span data-stu-id="293db-116">The start value can be greater than the end value.</span></span> <span data-ttu-id="293db-117">En el nivel inferior de los dos valores se especifica la posición del carácter del primer carácter de la selección.</span><span class="sxs-lookup"><span data-stu-id="293db-117">The lower of the two values specifies the character position of the first character in the selection.</span></span> <span data-ttu-id="293db-118">El valor superior especifica la posición del primer carácter más allá de la selección.</span><span class="sxs-lookup"><span data-stu-id="293db-118">The higher value specifies the position of the first character beyond the selection.</span></span>

<span data-ttu-id="293db-119">El valor inicial es el punto de anclaje de la selección y el valor final es el extremo activo.</span><span class="sxs-lookup"><span data-stu-id="293db-119">The start value is the anchor point of the selection, and the end value is the active end.</span></span> <span data-ttu-id="293db-120">Si el usuario usa la tecla Mayús para ajustar el tamaño de la selección, el extremo activo se puede mover, pero el punto de anclaje sigue siendo el mismo.</span><span class="sxs-lookup"><span data-stu-id="293db-120">If the user uses the SHIFT key to adjust the size of the selection, the active end can move but the anchor point remains the same.</span></span>

<span data-ttu-id="293db-121">Si el inicio es 0 y el final es-1, se selecciona todo el texto del control de edición.</span><span class="sxs-lookup"><span data-stu-id="293db-121">If the start is 0 and the end is -1, all the text in the edit control is selected.</span></span> <span data-ttu-id="293db-122">Si el inicio es-1, se anula la selección de cualquier selección actual.</span><span class="sxs-lookup"><span data-stu-id="293db-122">If the start is -1, any current selection is deselected.</span></span>

<span data-ttu-id="293db-123">**Controles de edición:** El control muestra un símbolo de intercalación parpadeante en la posición final sin tener en cuenta los valores relativos de inicio y fin.</span><span class="sxs-lookup"><span data-stu-id="293db-123">**Edit controls:** The control displays a flashing caret at the end position regardless of the relative values of start and end.</span></span>

<span data-ttu-id="293db-124">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="293db-124">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="293db-125">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="293db-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="293db-126">Si el control de edición tiene el estilo [**es \_ NOHIDESEL**](edit-control-styles.md) , el texto seleccionado se resalta sin tener en cuenta si el control tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="293db-126">If the edit control has the [**ES\_NOHIDESEL**](edit-control-styles.md) style, the selected text is highlighted regardless of whether the control has focus.</span></span> <span data-ttu-id="293db-127">Sin el estilo **es \_ NOHIDESEL** , el texto seleccionado se resalta solo cuando el control de edición tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="293db-127">Without the **ES\_NOHIDESEL** style, the selected text is highlighted only when the edit control has the focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="293db-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="293db-128">Requirements</span></span>



| <span data-ttu-id="293db-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="293db-129">Requirement</span></span> | <span data-ttu-id="293db-130">Value</span><span class="sxs-lookup"><span data-stu-id="293db-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="293db-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="293db-131">Minimum supported client</span></span><br/> | <span data-ttu-id="293db-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="293db-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="293db-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="293db-133">Minimum supported server</span></span><br/> | <span data-ttu-id="293db-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="293db-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="293db-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="293db-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="293db-136"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="293db-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="293db-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="293db-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="293db-138">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="293db-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="293db-139">**\_GETSEL em**</span><span class="sxs-lookup"><span data-stu-id="293db-139">**EM\_GETSEL**</span></span>](em-getsel.md)
</dt> <dt>

[<span data-ttu-id="293db-140">**\_REPLACESEL em**</span><span class="sxs-lookup"><span data-stu-id="293db-140">**EM\_REPLACESEL**</span></span>](em-replacesel.md)
</dt> <dt>

[<span data-ttu-id="293db-141">**\_SCROLLCARET em**</span><span class="sxs-lookup"><span data-stu-id="293db-141">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="293db-142">**\_EXSETSEL em**</span><span class="sxs-lookup"><span data-stu-id="293db-142">**EM\_EXSETSEL**</span></span>](em-exsetsel.md)
</dt> </dl>

 

 





