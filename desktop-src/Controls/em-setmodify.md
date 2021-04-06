---
title: Mensaje de EM_SETMODIFY (Winuser. h)
description: Establece o borra la marca de modificación de un control de edición. La marca de modificación indica si se ha modificado el texto del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_SETMODIFY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905362"
---
# <a name="em_setmodify-message"></a><span data-ttu-id="674f2-106">\_Mensaje SETMODIFY em</span><span class="sxs-lookup"><span data-stu-id="674f2-106">EM\_SETMODIFY message</span></span>

<span data-ttu-id="674f2-107">Establece o borra la marca de modificación de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="674f2-107">Sets or clears the modification flag for an edit control.</span></span> <span data-ttu-id="674f2-108">La marca de modificación indica si se ha modificado el texto del control de edición.</span><span class="sxs-lookup"><span data-stu-id="674f2-108">The modification flag indicates whether the text within the edit control has been modified.</span></span> <span data-ttu-id="674f2-109">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="674f2-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="674f2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="674f2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="674f2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="674f2-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="674f2-112">Nuevo valor para la marca de modificación.</span><span class="sxs-lookup"><span data-stu-id="674f2-112">The new value for the modification flag.</span></span> <span data-ttu-id="674f2-113">Un valor de **true** indica que el texto se ha modificado y el valor **false** indica que no se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="674f2-113">A value of **TRUE** indicates the text has been modified, and a value of **FALSE** indicates it has not been modified.</span></span>

</dd> <dt>

<span data-ttu-id="674f2-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="674f2-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="674f2-115">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="674f2-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="674f2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="674f2-116">Return value</span></span>

<span data-ttu-id="674f2-117">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="674f2-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="674f2-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="674f2-118">Remarks</span></span>

<span data-ttu-id="674f2-119">El sistema borra automáticamente la marca de modificación a cero cuando se crea el control.</span><span class="sxs-lookup"><span data-stu-id="674f2-119">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="674f2-120">Si el usuario cambia el texto del control, el sistema establece la marca en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="674f2-120">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="674f2-121">Puede enviar el mensaje [**\_ GETMODIFY em**](em-getmodify.md) al control de edición para recuperar el estado actual de la marca.</span><span class="sxs-lookup"><span data-stu-id="674f2-121">You can send the [**EM\_GETMODIFY**](em-getmodify.md) message to the edit control to retrieve the current state of the flag.</span></span>

<span data-ttu-id="674f2-122">**Rich Edit 1,0:** Los objetos creados sin la marca **reo de \_ Dynamics** se bloquearán en sus extensiones cuando la marca de modificación esté establecida en **false**.</span><span class="sxs-lookup"><span data-stu-id="674f2-122">**Rich Edit 1.0:** Objects created without the **REO\_DYNAMICSIZE** flag will lock in their extents when the modify flag is set to **FALSE**.</span></span>

<span data-ttu-id="674f2-123">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="674f2-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="674f2-124">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="674f2-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="674f2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="674f2-125">Requirements</span></span>



| <span data-ttu-id="674f2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="674f2-126">Requirement</span></span> | <span data-ttu-id="674f2-127">Value</span><span class="sxs-lookup"><span data-stu-id="674f2-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="674f2-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="674f2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="674f2-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="674f2-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="674f2-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="674f2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="674f2-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="674f2-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="674f2-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="674f2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="674f2-133"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="674f2-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="674f2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="674f2-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="674f2-135">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="674f2-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="674f2-136">**\_GETMODIFY em**</span><span class="sxs-lookup"><span data-stu-id="674f2-136">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> <dt>

[<span data-ttu-id="674f2-137">**Reobject**</span><span class="sxs-lookup"><span data-stu-id="674f2-137">**REOBJECT**</span></span>](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





