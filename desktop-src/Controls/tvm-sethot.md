---
title: Mensaje de TVM_SETHOT (commctrl. h)
description: Establece el elemento activo para un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ SetHot.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- TVM_SETHOT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beccd5429267350682a6721cde66cca9316cf438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996960"
---
# <a name="tvm_sethot-message"></a><span data-ttu-id="5fc94-105">\_Mensaje TVM SETHOT</span><span class="sxs-lookup"><span data-stu-id="5fc94-105">TVM\_SETHOT message</span></span>

<span data-ttu-id="5fc94-106">\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.</span><span class="sxs-lookup"><span data-stu-id="5fc94-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="5fc94-107">Es posible que este mensaje no se admita en versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5fc94-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="5fc94-108">Establece el elemento activo para un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="5fc94-108">Sets the hot item for a tree-view control.</span></span> <span data-ttu-id="5fc94-109">Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) .</span><span class="sxs-lookup"><span data-stu-id="5fc94-109">You can send this message explicitly or by using the [**TreeView\_SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5fc94-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fc94-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fc94-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5fc94-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fc94-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5fc94-112">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5fc94-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fc94-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fc94-114">Identificador del nuevo elemento activo.</span><span class="sxs-lookup"><span data-stu-id="5fc94-114">Handle to the new hot item.</span></span> <span data-ttu-id="5fc94-115">Si este valor es **null**, el control de vista de árbol se establecerá en no tener ningún elemento activo.</span><span class="sxs-lookup"><span data-stu-id="5fc94-115">If this value is **NULL**, the tree-view control will be set to have no hot item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fc94-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fc94-116">Return value</span></span>

<span data-ttu-id="5fc94-117">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5fc94-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="5fc94-118">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="5fc94-118">Security Considerations</span></span>

<span data-ttu-id="5fc94-119">El uso de este mensaje podría poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="5fc94-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc94-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fc94-120">Remarks</span></span>

<span data-ttu-id="5fc94-121">El *elemento activo* es el elemento sobre el que se mantiene el mouse.</span><span class="sxs-lookup"><span data-stu-id="5fc94-121">The *hot item* is the item that the mouse is hovering over.</span></span> <span data-ttu-id="5fc94-122">Este mensaje hace que un elemento parezca que es el elemento activo, incluso si el mouse no se mantiene sobre él.</span><span class="sxs-lookup"><span data-stu-id="5fc94-122">This message makes an item look like it is the hot item even if the mouse is not hovering over it.</span></span>

<span data-ttu-id="5fc94-123">Este mensaje no tiene ningún efecto visible si no se establece el estilo [**\_ TRACKSELECT de los televisores**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5fc94-123">This message has no visible effect if the [**TVS\_TRACKSELECT**](tree-view-control-window-styles.md) style is not set.</span></span>

<span data-ttu-id="5fc94-124">Si se realiza correctamente, este mensaje hace que el elemento activo se vuelva a dibujar.</span><span class="sxs-lookup"><span data-stu-id="5fc94-124">If it succeeds, this message causes the hot item to be redrawn.</span></span>

<span data-ttu-id="5fc94-125">Este mensaje se omite si *lParam* es **null** y el control de vista de árbol está realizando el seguimiento del mouse.</span><span class="sxs-lookup"><span data-stu-id="5fc94-125">This message is ignored if *lParam* is **NULL** and the tree-view control is tracking the mouse.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fc94-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fc94-126">Requirements</span></span>



| <span data-ttu-id="5fc94-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fc94-127">Requirement</span></span> | <span data-ttu-id="5fc94-128">Value</span><span class="sxs-lookup"><span data-stu-id="5fc94-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc94-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fc94-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc94-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5fc94-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5fc94-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fc94-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc94-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5fc94-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5fc94-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fc94-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fc94-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fc94-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fc94-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fc94-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fc94-136">**Vista de árbol \_ SetHot**</span><span class="sxs-lookup"><span data-stu-id="5fc94-136">**TreeView\_SetHot**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





