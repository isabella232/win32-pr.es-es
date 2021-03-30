---
title: Mensaje de LVM_GETITEMSTATE (commctrl. h)
description: Recupera el estado de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemState de ListView.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- LVM_GETITEMSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b355e78f22c01c289f681d256ee6b4d0aa882
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492412"
---
# <a name="lvm_getitemstate-message"></a><span data-ttu-id="509c2-105">\_Mensaje GETITEMSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="509c2-105">LVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="509c2-106">Recupera el estado de un elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="509c2-106">Retrieves the state of a list-view item.</span></span> <span data-ttu-id="509c2-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemState de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) .</span><span class="sxs-lookup"><span data-stu-id="509c2-107">You can send this message explicitly or by using the [**ListView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="509c2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="509c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="509c2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="509c2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="509c2-110">Índice del elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="509c2-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="509c2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="509c2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="509c2-112">Información de estado que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="509c2-112">State information to retrieve.</span></span> <span data-ttu-id="509c2-113">Este parámetro puede ser una combinación de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="509c2-113">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="509c2-114">Value</span><span class="sxs-lookup"><span data-stu-id="509c2-114">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="509c2-115">Significado</span><span class="sxs-lookup"><span data-stu-id="509c2-115">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="509c2-116"><dt>**LVIS \_ cortar**</dt></span><span class="sxs-lookup"><span data-stu-id="509c2-116"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="509c2-117">El elemento está marcado para una operación de cortar y pegar.</span><span class="sxs-lookup"><span data-stu-id="509c2-117">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="509c2-118"><dt>**LVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="509c2-118"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="509c2-119">El elemento se resalta como un destino de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="509c2-119">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="509c2-120"><dt>**LVIS \_ centrado**</dt></span><span class="sxs-lookup"><span data-stu-id="509c2-120"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="509c2-121">El elemento tiene el foco, por lo que está rodeado por un rectángulo de foco estándar.</span><span class="sxs-lookup"><span data-stu-id="509c2-121">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="509c2-122">Aunque se puede seleccionar más de un elemento, solo un elemento puede tener el foco.</span><span class="sxs-lookup"><span data-stu-id="509c2-122">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="509c2-123"><dt>**LVIS \_ seleccionado**</dt></span><span class="sxs-lookup"><span data-stu-id="509c2-123"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="509c2-124">El elemento está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="509c2-124">The item is selected.</span></span> <span data-ttu-id="509c2-125">La apariencia de un elemento seleccionado depende de si tiene el foco y también de los colores del sistema utilizados para la selección.</span><span class="sxs-lookup"><span data-stu-id="509c2-125">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="509c2-126"><dt>**LVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="509c2-126"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="509c2-127">Use esta máscara para recuperar el índice de la imagen de superposición del elemento.</span><span class="sxs-lookup"><span data-stu-id="509c2-127">Use this mask to retrieve the item's overlay image index.</span></span><br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="509c2-128"><dt>**LVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="509c2-128"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="509c2-129">Use esta máscara para recuperar el índice de imagen de estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="509c2-129">Use this mask to retrieve the item's state image index.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="509c2-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="509c2-130">Return value</span></span>

<span data-ttu-id="509c2-131">Devuelve el estado actual del elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="509c2-131">Returns the current state for the specified item.</span></span> <span data-ttu-id="509c2-132">Los únicos bits válidos en el valor devuelto son los que corresponden a los bits establecidos en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="509c2-132">The only valid bits in the return value are those that correspond to the bits set in the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="509c2-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="509c2-133">Remarks</span></span>

<span data-ttu-id="509c2-134">La información de estado de un elemento incluye un conjunto de marcas de bits, así como índices de lista de imágenes que indican la imagen de estado del elemento y la imagen de superposición.</span><span class="sxs-lookup"><span data-stu-id="509c2-134">An item's state information includes a set of bit flags as well as image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="509c2-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="509c2-135">Requirements</span></span>



| <span data-ttu-id="509c2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="509c2-136">Requirement</span></span> | <span data-ttu-id="509c2-137">Value</span><span class="sxs-lookup"><span data-stu-id="509c2-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="509c2-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="509c2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="509c2-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="509c2-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="509c2-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="509c2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="509c2-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="509c2-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="509c2-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="509c2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="509c2-143"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="509c2-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="509c2-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="509c2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="509c2-145">**\_SETITEMSTATE LVM**</span><span class="sxs-lookup"><span data-stu-id="509c2-145">**LVM\_SETITEMSTATE**</span></span>](lvm-setitemstate.md)
</dt> </dl>

 

 





