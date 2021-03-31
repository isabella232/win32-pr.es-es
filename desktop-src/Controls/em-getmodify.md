---
title: Mensaje de EM_GETMODIFY (Winuser. h)
description: Obtiene el estado de la marca de modificación de un control de edición. La marca indica si se ha modificado el contenido del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- EM_GETMODIFY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8c525df061717255051c49abaa3bda88f317b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905060"
---
# <a name="em_getmodify-message"></a><span data-ttu-id="fcab7-106">\_Mensaje GETMODIFY em</span><span class="sxs-lookup"><span data-stu-id="fcab7-106">EM\_GETMODIFY message</span></span>

<span data-ttu-id="fcab7-107">Obtiene el estado de la marca de modificación de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="fcab7-107">Gets the state of an edit control's modification flag.</span></span> <span data-ttu-id="fcab7-108">La marca indica si se ha modificado el contenido del control de edición.</span><span class="sxs-lookup"><span data-stu-id="fcab7-108">The flag indicates whether the contents of the edit control have been modified.</span></span> <span data-ttu-id="fcab7-109">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="fcab7-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fcab7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcab7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcab7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fcab7-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcab7-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fcab7-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fcab7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcab7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcab7-114">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fcab7-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcab7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcab7-115">Return value</span></span>

<span data-ttu-id="fcab7-116">Si se ha modificado el contenido del control de edición, el valor devuelto es distinto de cero; de lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="fcab7-116">If the contents of edit control have been modified, the return value is nonzero; otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcab7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcab7-117">Remarks</span></span>

<span data-ttu-id="fcab7-118">El sistema borra automáticamente la marca de modificación a cero cuando se crea el control.</span><span class="sxs-lookup"><span data-stu-id="fcab7-118">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="fcab7-119">Si el usuario cambia el texto del control, el sistema establece la marca en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="fcab7-119">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="fcab7-120">Puede enviar el mensaje [**\_ SETMODIFY em**](em-setmodify.md) al control Editar para establecer o borrar la marca.</span><span class="sxs-lookup"><span data-stu-id="fcab7-120">You can send the [**EM\_SETMODIFY**](em-setmodify.md) message to the edit control to set or clear the flag.</span></span>

<span data-ttu-id="fcab7-121">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="fcab7-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="fcab7-122">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="fcab7-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcab7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcab7-123">Requirements</span></span>



| <span data-ttu-id="fcab7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcab7-124">Requirement</span></span> | <span data-ttu-id="fcab7-125">Value</span><span class="sxs-lookup"><span data-stu-id="fcab7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcab7-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcab7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fcab7-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fcab7-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fcab7-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcab7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fcab7-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fcab7-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fcab7-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcab7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcab7-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcab7-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcab7-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcab7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcab7-133">**\_SETMODIFY em**</span><span class="sxs-lookup"><span data-stu-id="fcab7-133">**EM\_SETMODIFY**</span></span>](em-setmodify.md)
</dt> </dl>

 

 





