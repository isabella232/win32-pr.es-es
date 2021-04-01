---
title: Mensaje de LVM_SETCALLBACKMASK (commctrl. h)
description: Cambia la máscara de devolución de llamada de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetCallbackMask de ListView.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- LVM_SETCALLBACKMASK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef6dd46228c4e4aeada30f469a77f9e67aff3a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150135"
---
# <a name="lvm_setcallbackmask-message"></a><span data-ttu-id="37e88-105">\_Mensaje SETCALLBACKMASK LVM</span><span class="sxs-lookup"><span data-stu-id="37e88-105">LVM\_SETCALLBACKMASK message</span></span>

<span data-ttu-id="37e88-106">Cambia la máscara de devolución de llamada de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="37e88-106">Changes the callback mask for a list-view control.</span></span> <span data-ttu-id="37e88-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetCallbackMask de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) .</span><span class="sxs-lookup"><span data-stu-id="37e88-107">You can send this message explicitly or by using the [**ListView\_SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="37e88-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37e88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37e88-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37e88-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37e88-110">Valor de la máscara de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="37e88-110">Value of the callback mask.</span></span> <span data-ttu-id="37e88-111">Los bits de la máscara indican los Estados o las imágenes del elemento para los que la aplicación almacena los datos de estado actuales.</span><span class="sxs-lookup"><span data-stu-id="37e88-111">The bits of the mask indicate the item states or images for which the application stores the current state data.</span></span> <span data-ttu-id="37e88-112">Este valor puede ser cualquier combinación de las siguientes constantes:</span><span class="sxs-lookup"><span data-stu-id="37e88-112">This value can be any combination of the following constants:</span></span>



| <span data-ttu-id="37e88-113">Value</span><span class="sxs-lookup"><span data-stu-id="37e88-113">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="37e88-114">Significado</span><span class="sxs-lookup"><span data-stu-id="37e88-114">Meaning</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="37e88-115"><dt>**LVIS \_ cortar**</dt></span><span class="sxs-lookup"><span data-stu-id="37e88-115"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="37e88-116">El elemento está marcado para una operación de cortar y pegar.</span><span class="sxs-lookup"><span data-stu-id="37e88-116">The item is marked for a cut-and-paste operation.</span></span><br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="37e88-117"><dt>**LVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="37e88-117"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="37e88-118">El elemento se resalta como un destino de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="37e88-118">The item is highlighted as a drag-and-drop target.</span></span><br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="37e88-119"><dt>**LVIS \_ centrado**</dt></span><span class="sxs-lookup"><span data-stu-id="37e88-119"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="37e88-120">El elemento tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="37e88-120">The item has the focus.</span></span><br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="37e88-121"><dt>**LVIS \_ seleccionado**</dt></span><span class="sxs-lookup"><span data-stu-id="37e88-121"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="37e88-122">El elemento está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="37e88-122">The item is selected.</span></span> <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="37e88-123"><dt>**LVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="37e88-123"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="37e88-124">La aplicación almacena el índice de la lista de imágenes de la imagen de superposición actual para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="37e88-124">The application stores the image list index of the current overlay image for each item.</span></span><br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="37e88-125"><dt>**LVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="37e88-125"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="37e88-126">La aplicación almacena el índice de la lista de imágenes de la imagen de estado actual para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="37e88-126">The application stores the image list index of the current state image for each item.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="37e88-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37e88-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="37e88-128">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="37e88-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37e88-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37e88-129">Return value</span></span>

<span data-ttu-id="37e88-130">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="37e88-130">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="37e88-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37e88-131">Remarks</span></span>

<span data-ttu-id="37e88-132">La *máscara de devolución de llamada* de un control de vista de lista es un conjunto de marcadores de bits que especifican los Estados del elemento para los que la aplicación, en lugar del control, almacena los datos actuales.</span><span class="sxs-lookup"><span data-stu-id="37e88-132">The *callback mask* of a list-view control is a set of bit flags that specify the item states for which the application, rather than the control, stores the current data.</span></span> <span data-ttu-id="37e88-133">La máscara de devolución de llamada se aplica a todos los elementos del control, a diferencia de la designación del elemento de devolución de llamada, que se aplica a un elemento específico.</span><span class="sxs-lookup"><span data-stu-id="37e88-133">The callback mask applies to all of the control's items, unlike the callback item designation, which applies to a specific item.</span></span> <span data-ttu-id="37e88-134">De forma predeterminada, la máscara de devolución de llamada es cero, lo que significa que el control de vista de lista almacena toda la información de estado de los elementos.</span><span class="sxs-lookup"><span data-stu-id="37e88-134">The callback mask is zero by default, meaning that the list-view control stores all item state information.</span></span> <span data-ttu-id="37e88-135">Después de crear un control de vista de lista e inicializar sus elementos, puede enviar el mensaje **LVM \_ SETCALLBACKMASK** para cambiar la máscara de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="37e88-135">After creating a list-view control and initializing its items, you can send the **LVM\_SETCALLBACKMASK** message to change the callback mask.</span></span> <span data-ttu-id="37e88-136">Para recuperar la máscara de devolución de llamada actual, envíe el mensaje [**LVM \_ GETCALLBACKMASK**](lvm-getcallbackmask.md) .</span><span class="sxs-lookup"><span data-stu-id="37e88-136">To retrieve the current callback mask, send the [**LVM\_GETCALLBACKMASK**](lvm-getcallbackmask.md) message.</span></span>

<span data-ttu-id="37e88-137">Para obtener más información sobre las imágenes de superposición y las imágenes de estado, vea [agregar List-View listas de imágenes](using-list-view-controls.md).</span><span class="sxs-lookup"><span data-stu-id="37e88-137">For more information about overlay images and state images, see [Adding List-View Image Lists](using-list-view-controls.md).</span></span>

<span data-ttu-id="37e88-138">Para obtener más información sobre las devoluciones de llamada de vista de lista, vea [elementos de devolución de llamada y máscara de devolución de llamada](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="37e88-138">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37e88-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37e88-139">Requirements</span></span>



| <span data-ttu-id="37e88-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="37e88-140">Requirement</span></span> | <span data-ttu-id="37e88-141">Value</span><span class="sxs-lookup"><span data-stu-id="37e88-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37e88-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37e88-142">Minimum supported client</span></span><br/> | <span data-ttu-id="37e88-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="37e88-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37e88-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37e88-144">Minimum supported server</span></span><br/> | <span data-ttu-id="37e88-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="37e88-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37e88-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37e88-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="37e88-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="37e88-147"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37e88-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="37e88-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37e88-149">**LVN \_ GETDISPINFO**</span><span class="sxs-lookup"><span data-stu-id="37e88-149">**LVN\_GETDISPINFO**</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





