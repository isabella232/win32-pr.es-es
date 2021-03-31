---
title: Mensaje de EM_SCROLLCARET (Winuser. h)
description: Desplaza el símbolo de intercalación en la vista de un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 7a33034d-9369-49f8-a881-0c1d2cedff6a
keywords:
- EM_SCROLLCARET controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SCROLLCARET
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa9f4bd69605f5e8fad36a683c9be2894546cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151147"
---
# <a name="em_scrollcaret-message"></a><span data-ttu-id="22fd8-105">\_Mensaje SCROLLCARET em</span><span class="sxs-lookup"><span data-stu-id="22fd8-105">EM\_SCROLLCARET message</span></span>

<span data-ttu-id="22fd8-106">Desplaza el símbolo de intercalación en la vista de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="22fd8-106">Scrolls the caret into view in an edit control.</span></span> <span data-ttu-id="22fd8-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="22fd8-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="22fd8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22fd8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22fd8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22fd8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22fd8-110">Este parámetro está reservado.</span><span class="sxs-lookup"><span data-stu-id="22fd8-110">This parameter is reserved.</span></span> <span data-ttu-id="22fd8-111">Debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="22fd8-111">It should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="22fd8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22fd8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22fd8-113">Este parámetro está reservado.</span><span class="sxs-lookup"><span data-stu-id="22fd8-113">This parameter is reserved.</span></span> <span data-ttu-id="22fd8-114">Debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="22fd8-114">It should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22fd8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22fd8-115">Return value</span></span>

<span data-ttu-id="22fd8-116">El valor devuelto no es significativo.</span><span class="sxs-lookup"><span data-stu-id="22fd8-116">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="22fd8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22fd8-117">Remarks</span></span>

<span data-ttu-id="22fd8-118">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="22fd8-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="22fd8-119">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="22fd8-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22fd8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22fd8-120">Requirements</span></span>



| <span data-ttu-id="22fd8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="22fd8-121">Requirement</span></span> | <span data-ttu-id="22fd8-122">Value</span><span class="sxs-lookup"><span data-stu-id="22fd8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22fd8-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22fd8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="22fd8-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="22fd8-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="22fd8-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22fd8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="22fd8-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="22fd8-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="22fd8-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22fd8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="22fd8-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22fd8-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22fd8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="22fd8-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="22fd8-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="22fd8-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="22fd8-131">**\_LINESCROLL em**</span><span class="sxs-lookup"><span data-stu-id="22fd8-131">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="22fd8-132">**\_desplazar em**</span><span class="sxs-lookup"><span data-stu-id="22fd8-132">**EM\_SCROLL**</span></span>](em-scroll.md)
</dt> <dt>

[<span data-ttu-id="22fd8-133">**VSCROLL de WM \_**</span><span class="sxs-lookup"><span data-stu-id="22fd8-133">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

 





