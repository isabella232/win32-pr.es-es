---
title: Mensaje de LVM_SETITEMCOUNT (commctrl. h)
description: Hace que el control de vista de lista asigne memoria para el número de elementos especificado o establece el número virtual de elementos en un control de vista de lista virtual.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- LVM_SETITEMCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e390e7ae5913053f91f7f2f8d197af1cf4b7a40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150067"
---
# <a name="lvm_setitemcount-message"></a><span data-ttu-id="d53ad-104">\_Mensaje SETITEMCOUNT LVM</span><span class="sxs-lookup"><span data-stu-id="d53ad-104">LVM\_SETITEMCOUNT message</span></span>

<span data-ttu-id="d53ad-105">Hace que el control de vista de lista asigne memoria para el número de elementos especificado o establece el número virtual de elementos en un [control de vista de lista virtual](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d53ad-105">Causes the list-view control to allocate memory for the specified number of items or sets the virtual number of items in a [virtual list-view control](list-view-controls-overview.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="d53ad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d53ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d53ad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d53ad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d53ad-108">Número de elementos que el control de vista de lista va a contener en última instancia.</span><span class="sxs-lookup"><span data-stu-id="d53ad-108">Number of items that the list-view control will ultimately contain.</span></span>

</dd> <dt>

<span data-ttu-id="d53ad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d53ad-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d53ad-110">[Versión 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="d53ad-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="d53ad-111">Valores que especifican el comportamiento del control de vista de lista después de restablecer el recuento de elementos.</span><span class="sxs-lookup"><span data-stu-id="d53ad-111">Values that specify the behavior of the list-view control after resetting the item count.</span></span> <span data-ttu-id="d53ad-112">Este valor puede ser una combinación de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d53ad-112">This value can be a combination of the following:</span></span>



| <span data-ttu-id="d53ad-113">Value</span><span class="sxs-lookup"><span data-stu-id="d53ad-113">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="d53ad-114">Significado</span><span class="sxs-lookup"><span data-stu-id="d53ad-114">Meaning</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <span data-ttu-id="d53ad-115"><dt>**LVSICF \_ NOINVALIDATEALL**</dt></span><span class="sxs-lookup"><span data-stu-id="d53ad-115"><dt>**LVSICF\_NOINVALIDATEALL**</dt></span></span> </dl> | <span data-ttu-id="d53ad-116">El control de vista de lista no volverá a dibujar a menos que los elementos afectados estén actualmente en la vista.</span><span class="sxs-lookup"><span data-stu-id="d53ad-116">The list-view control will not repaint unless affected items are currently in view.</span></span><br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <span data-ttu-id="d53ad-117"><dt>**LVSICF \_ NOscroll**</dt></span><span class="sxs-lookup"><span data-stu-id="d53ad-117"><dt>**LVSICF\_NOSCROLL**</dt></span></span> </dl>                      | <span data-ttu-id="d53ad-118">El control de vista de lista no cambiará la posición de desplazamiento cuando cambie el número de elementos.</span><span class="sxs-lookup"><span data-stu-id="d53ad-118">The list-view control will not change the scroll position when the item count changes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d53ad-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d53ad-119">Return value</span></span>

<span data-ttu-id="d53ad-120">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="d53ad-120">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d53ad-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d53ad-121">Remarks</span></span>

<span data-ttu-id="d53ad-122">La forma en que se asigna la memoria depende de cómo se creó el control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="d53ad-122">How the memory is allocated depends on how the list-view control was created.</span></span> <span data-ttu-id="d53ad-123">Puede enviar este mensaje explícitamente o usar las macros [**\_ SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) o [**ListView \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) de ListView.</span><span class="sxs-lookup"><span data-stu-id="d53ad-123">You can send this message explicitly or use the [**ListView\_SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) or [**ListView\_SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) macros.</span></span> <span data-ttu-id="d53ad-124">Para obtener más información, consulte [estilo de List-View virtual](/windows/desktop/Controls/list-view-controls-overview).</span><span class="sxs-lookup"><span data-stu-id="d53ad-124">For more information, see [Virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).</span></span>

<span data-ttu-id="d53ad-125">Si el control de vista de lista se creó sin el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) , el envío de este mensaje hace que el control asigne sus estructuras de datos internas para el número de elementos especificado.</span><span class="sxs-lookup"><span data-stu-id="d53ad-125">If the list-view control was created without the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, sending this message causes the control to allocate its internal data structures for the specified number of items.</span></span> <span data-ttu-id="d53ad-126">Esto evita que el control tenga que asignar las estructuras de datos cada vez que se agrega un elemento.</span><span class="sxs-lookup"><span data-stu-id="d53ad-126">This prevents the control from having to allocate the data structures every time an item is added.</span></span>

<span data-ttu-id="d53ad-127">Si el control de vista de lista se creó con el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) (una vista de lista virtual), al enviar este mensaje se establece el número virtual de elementos que contiene el control.</span><span class="sxs-lookup"><span data-stu-id="d53ad-127">If the list-view control was created with the [**LVS\_OWNERDATA**](list-view-window-styles.md) style (a virtual list view), sending this message sets the virtual number of items that the control contains.</span></span>

<span data-ttu-id="d53ad-128">El parámetro *lParam* solo está pensado para los controles de vista de lista que usan los estilos [**LVS \_ OWNERDATA**](list-view-window-styles.md) y [**LVS \_**](list-view-window-styles.md) o [**LVS \_ List**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d53ad-128">The *lParam* parameter is intended only for list-view controls that use the [**LVS\_OWNERDATA**](list-view-window-styles.md) and [**LVS\_REPORT**](list-view-window-styles.md) or [**LVS\_LIST**](list-view-window-styles.md) styles.</span></span>

<span data-ttu-id="d53ad-129">Cuando la vista de lista de controles comunes es una vista de lista virtualizada ([**LVS \_ OWNERDATA**](list-view-window-styles.md)), hay un límite de 100 millones elementos en la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="d53ad-129">When the common control list-view is a virtualized list-view ([**LVS\_OWNERDATA**](list-view-window-styles.md)), there is a 100,000,000 item limit on the list-view.</span></span> <span data-ttu-id="d53ad-130">En este escenario, **el \_ SETITEMCOUNT de LVM** devolverá FALSE cuando tenga un valor de *wParam* de 100.000.001.</span><span class="sxs-lookup"><span data-stu-id="d53ad-130">In this scenario, **LVM\_SETITEMCOUNT** will return FALSE when it has a *wParam* of 100,000,001.</span></span>

## <a name="requirements"></a><span data-ttu-id="d53ad-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d53ad-131">Requirements</span></span>



| <span data-ttu-id="d53ad-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d53ad-132">Requirement</span></span> | <span data-ttu-id="d53ad-133">Value</span><span class="sxs-lookup"><span data-stu-id="d53ad-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d53ad-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d53ad-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d53ad-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d53ad-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d53ad-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d53ad-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d53ad-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d53ad-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d53ad-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d53ad-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d53ad-139"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d53ad-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

