---
title: Compatibilidad de UI Automation para arrastrar y colocar
description: En este tema se describen los patrones de control que exponen información sobre la funcionalidad de arrastrar y colocar de un elemento.
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- Automatización de la interfaz de usuario, compatibilidad con arrastrar y colocar
- Automatización de la interfaz de usuario, arrastrar información general del patrón
- Automatización de la interfaz de usuario, introducción al patrón DropTarget
- Automatización de la interfaz de usuario, información general de arrastrar y colocar
- patrones de arrastrar y colocar, acerca de
- Arrastrar patrón de control
- Patrón de control DropTarget
- patrones de control, arrastrar
- patrones de control, DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4194613d15aadac4a925303ef2322d4cf53c341c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685750"
---
# <a name="ui-automation-support-for-drag-and-drop"></a><span data-ttu-id="feb03-112">Compatibilidad de UI Automation para arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="feb03-112">UI Automation Support for Drag-and-Drop</span></span>

<span data-ttu-id="feb03-113">La automatización de la interfaz de usuario de Microsoft define dos patrones de control para admitir escenarios de arrastrar y colocar, el patrón de control de [arrastre](/windows/desktop/WinAuto/uiauto-implementingdrag) y el patrón de control [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="feb03-113">Microsoft UI Automation defines two control patterns for supporting drag-and-drop scenarios, the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern, and the [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) control pattern.</span></span> <span data-ttu-id="feb03-114">Se implementa el patrón de control de arrastrar para un elemento que se puede arrastrar y el patrón de control DropTarget para un elemento que puede recibir un elemento arrastrado; es decir, un destino de colocación.</span><span class="sxs-lookup"><span data-stu-id="feb03-114">You implement the Drag control pattern for an element that can be dragged, and the DropTarget control pattern for an element that can receive a dragged element; that is, a drop target.</span></span> <span data-ttu-id="feb03-115">Los dos patrones de control exponen información que una tecnología de ayuda puede usar para ayudar a un usuario de accesibilidad a completar una operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="feb03-115">The two control patterns expose information that an assistive technology can use to help an accessibility user complete a drag-and-drop operation.</span></span>

-   [<span data-ttu-id="feb03-116">Arrastrar estilos</span><span class="sxs-lookup"><span data-stu-id="feb03-116">Dragging Styles</span></span>](#dragging-styles)
    -   [<span data-ttu-id="feb03-117">Estilo de origen/destino</span><span class="sxs-lookup"><span data-stu-id="feb03-117">Source/target Style</span></span>](#sourcetarget-style)
    -   [<span data-ttu-id="feb03-118">Estilo de solo origen</span><span class="sxs-lookup"><span data-stu-id="feb03-118">Source-only Style</span></span>](#source-only-style)
-   [<span data-ttu-id="feb03-119">Arrastrar varios elementos</span><span class="sxs-lookup"><span data-stu-id="feb03-119">Dragging Multiple Items</span></span>](#dragging-multiple-items)
-   [<span data-ttu-id="feb03-120">Interfaces de cliente para arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="feb03-120">Client Interfaces for Drag-and-Drop</span></span>](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a><span data-ttu-id="feb03-121">Arrastrar estilos</span><span class="sxs-lookup"><span data-stu-id="feb03-121">Dragging Styles</span></span>

<span data-ttu-id="feb03-122">Al implementar el patrón de control de [arrastrar](/windows/desktop/WinAuto/uiauto-implementingdrag) para un elemento arrastrable, debe decidir si implementar el estilo de arrastre de *origen o destino* , o el estilo *de arrastre solo de origen* .</span><span class="sxs-lookup"><span data-stu-id="feb03-122">When you implement the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern for a draggable element, you need to decide whether to implement the *source/target* dragging style, or the *source-only* dragging style.</span></span>

### <a name="sourcetarget-style"></a><span data-ttu-id="feb03-123">Estilo de origen/destino</span><span class="sxs-lookup"><span data-stu-id="feb03-123">Source/target Style</span></span>

<span data-ttu-id="feb03-124">En el estilo de origen/destino de arrastrar y colocar, el elemento arrastrado (el "origen") y el elemento de destino de colocación (el "destino") son distintos, y cada uno de ellos genera un conjunto distinto de eventos.</span><span class="sxs-lookup"><span data-stu-id="feb03-124">In the source/target style of drag-and-drop, the dragged element (the "source") and the drop-target element (the "target") are distinct, and each raises a distinct set of events.</span></span> <span data-ttu-id="feb03-125">A continuación se muestra el ciclo de vida de una operación de arrastre que usa el estilo de origen/destino:</span><span class="sxs-lookup"><span data-stu-id="feb03-125">Here's the life cycle for a drag operation that uses the source/target style:</span></span> <dl> <span data-ttu-id="feb03-126">Cuando el usuario inicia una operación de arrastre:</span><span class="sxs-lookup"><span data-stu-id="feb03-126">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="feb03-127">El origen genera el evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="feb03-127">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="feb03-128">El origen establece la propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **true**.</span><span class="sxs-lookup"><span data-stu-id="feb03-128">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="feb03-129">Los destinos actualizan sus propiedades [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) .</span><span class="sxs-lookup"><span data-stu-id="feb03-129">Targets update their [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) properties.</span></span>

  
<span data-ttu-id="feb03-130">Cuando la operación de arrastrar entra en una región de destino:</span><span class="sxs-lookup"><span data-stu-id="feb03-130">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="feb03-131">El destino genera el evento DragEnter ([**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="feb03-131">The target raises the DragEnter ([**UIA\_DropTarget\_DragEnterEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="feb03-132">Cuando la operación de arrastrar sale de una región de destino:</span><span class="sxs-lookup"><span data-stu-id="feb03-132">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="feb03-133">El destino genera el evento DragLeave ([**UIA \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="feb03-133">The target raises the DragLeave ([**UIA\_DropTarget\_DragLeaveEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="feb03-134">Cuando el usuario suelta el elemento arrastrado a través de un objeto que no es de destino:</span><span class="sxs-lookup"><span data-stu-id="feb03-134">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="feb03-135">El origen genera el evento DragCancel ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="feb03-135">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="feb03-136">El origen establece la propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **false**.</span><span class="sxs-lookup"><span data-stu-id="feb03-136">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="feb03-137">Cuando el usuario suelta el elemento arrastrado a través de un destino:</span><span class="sxs-lookup"><span data-stu-id="feb03-137">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="feb03-138">El origen genera el evento DragComplete ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="feb03-138">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="feb03-139">El origen establece la propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **false**.</span><span class="sxs-lookup"><span data-stu-id="feb03-139">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>
-   <span data-ttu-id="feb03-140">El destino establece la propiedad [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) para indicar el efecto que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="feb03-140">The target sets the [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property to indicate the effect that occurred.</span></span>
-   <span data-ttu-id="feb03-141">El destino provoca el evento quitado ([**UIA \_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="feb03-141">The target raises the Dropped ([**UIA\_DropTarget\_DroppedEventId**](uiauto-event-ids.md)) event.</span></span>

  
</dl>

<span data-ttu-id="feb03-142">Los eventos de los objetos de origen y de destino están estrechamente relacionados, pero distintos.</span><span class="sxs-lookup"><span data-stu-id="feb03-142">The events from the source and target objects are closely related, but distinct.</span></span> <span data-ttu-id="feb03-143">Los datos sobre lo que se está arrastrando provienen del origen, mientras que los datos sobre "lo que podría suceder" y "Qué sucedió" provienen del destino.</span><span class="sxs-lookup"><span data-stu-id="feb03-143">The data about what is being dragged comes from the source, while the data about "what could happen" and "what did happen" comes from the target.</span></span>

<span data-ttu-id="feb03-144">Cuando una operación de arrastre está en curso, el elemento arrastrado se puede arrastrar hacia dentro y fuera de las regiones de destino cualquier número de veces antes de que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="feb03-144">When a drag operation is in progress, the dragged item can be dragged in and out of target regions any number of times before the operation completes.</span></span>

<span data-ttu-id="feb03-145">Cualquier destino de colocación que necesite actualizar su propiedad [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) sobre la marcha debe generar un evento de cambio de propiedad adicional en esa propiedad.</span><span class="sxs-lookup"><span data-stu-id="feb03-145">Any drop target that needs to update its [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property on the fly should raise an additional property changed event on that property.</span></span>

### <a name="source-only-style"></a><span data-ttu-id="feb03-146">Estilo de solo origen</span><span class="sxs-lookup"><span data-stu-id="feb03-146">Source-only Style</span></span>

<span data-ttu-id="feb03-147">El estilo de arrastre solo de origen permite a un proveedor evitar la implementación de destinos de colocación.</span><span class="sxs-lookup"><span data-stu-id="feb03-147">The source-only dragging style lets a provider avoid implementing drop targets.</span></span> <span data-ttu-id="feb03-148">No implementar destinos de colocación ayuda a reducir el costo de implementación, pero no proporciona a las aplicaciones cliente de accesibilidad ninguna información sobre el objeto que recibió la eliminación.</span><span class="sxs-lookup"><span data-stu-id="feb03-148">Not implementing drop targets helps lower the implementation cost, but does not give accessibility client applications any information about the object that received the drop.</span></span> <span data-ttu-id="feb03-149">A continuación se muestra el ciclo de vida de una operación de arrastre que usa el estilo de solo origen:</span><span class="sxs-lookup"><span data-stu-id="feb03-149">Here's the life cycle for a drag operation that uses the source-only style:</span></span> <dl> <span data-ttu-id="feb03-150">Cuando el usuario inicia una operación de arrastre:</span><span class="sxs-lookup"><span data-stu-id="feb03-150">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="feb03-151">El origen genera el evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="feb03-151">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="feb03-152">El origen establece la propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **true**.</span><span class="sxs-lookup"><span data-stu-id="feb03-152">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>

  
<span data-ttu-id="feb03-153">Cuando la operación de arrastrar entra en una región de destino:</span><span class="sxs-lookup"><span data-stu-id="feb03-153">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="feb03-154">El origen establece la propiedad [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) en el valor adecuado.</span><span class="sxs-lookup"><span data-stu-id="feb03-154">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="feb03-155">Cuando la operación de arrastrar sale de una región de destino:</span><span class="sxs-lookup"><span data-stu-id="feb03-155">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="feb03-156">El origen establece la propiedad [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) en el valor adecuado.</span><span class="sxs-lookup"><span data-stu-id="feb03-156">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="feb03-157">Cuando el usuario suelta el elemento arrastrado a través de un objeto que no es de destino:</span><span class="sxs-lookup"><span data-stu-id="feb03-157">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="feb03-158">El origen genera el evento DragCancel ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="feb03-158">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="feb03-159">El origen establece la propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **false**.</span><span class="sxs-lookup"><span data-stu-id="feb03-159">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="feb03-160">Cuando el usuario suelta el elemento arrastrado a través de un destino:</span><span class="sxs-lookup"><span data-stu-id="feb03-160">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="feb03-161">El origen genera el evento DragComplete ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="feb03-161">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="feb03-162">El origen establece la propiedad [**IDragProvider::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) para indicar el efecto que tuvo lugar cuando se quitó el elemento.</span><span class="sxs-lookup"><span data-stu-id="feb03-162">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to indicate the effect that took place when the item was dropped.</span></span>

  
</dl>

## <a name="dragging-multiple-items"></a><span data-ttu-id="feb03-163">Arrastrar varios elementos</span><span class="sxs-lookup"><span data-stu-id="feb03-163">Dragging Multiple Items</span></span>

<span data-ttu-id="feb03-164">Si un proveedor implementa operaciones de arrastrar y colocar en las que el usuario puede arrastrar varios objetos al mismo tiempo, el proveedor utiliza los estilos de origen/destino o solo de origen, tal y como se describe en la sección anterior, pero con una pequeña diferencia.</span><span class="sxs-lookup"><span data-stu-id="feb03-164">If a provider implements drag-and-drop operations where the user can drag multiple objects at the same time, the provider uses the source/target or source-only styles as described in the previous section, but with a small difference.</span></span> <span data-ttu-id="feb03-165">Cuando el usuario inicia la operación de arrastre, el proveedor crea un elemento de origen maestro que representa el conjunto completo de elementos que se arrastran.</span><span class="sxs-lookup"><span data-stu-id="feb03-165">When the user begins the drag operation, the provider creates a master source element that represents the full set of items that are being dragged.</span></span> <span data-ttu-id="feb03-166">El elemento de origen maestro genera todos los eventos en nombre del conjunto de elementos arrastrados; los elementos no generan eventos propios.</span><span class="sxs-lookup"><span data-stu-id="feb03-166">The master source element raises all events on behalf of the set of dragged items; the items don't raise any events of their own.</span></span><dl> <span data-ttu-id="feb03-167">Cuando el usuario inicia una operación de arrastre:</span><span class="sxs-lookup"><span data-stu-id="feb03-167">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="feb03-168">El proveedor crea el elemento de origen principal.</span><span class="sxs-lookup"><span data-stu-id="feb03-168">The provider creates the master source element.</span></span>
-   <span data-ttu-id="feb03-169">El elemento de origen maestro genera el evento DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="feb03-169">The master source element raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="feb03-170">El elemento de origen Maestro establece la propiedad [**IDragProvider:: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) en **true**.</span><span class="sxs-lookup"><span data-stu-id="feb03-170">The master source element sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="feb03-171">El elemento de origen principal actualiza la lista de elementos capturados para incluir todos los elementos que se arrastran para que el método [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) pueda recuperar la lista.</span><span class="sxs-lookup"><span data-stu-id="feb03-171">The master source element updates the list of grabbed items to include all items being dragged so that the [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) method can retrieve the list.</span></span>

  
</dl>

<span data-ttu-id="feb03-172">En ese momento, el elemento de origen maestro realiza el mismo rol que el elemento de origen, tal y como se describe en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="feb03-172">For that point on, the master source element performs the same role as that of the source element as described in the previous section.</span></span>

## <a name="client-interfaces-for-drag-and-drop"></a><span data-ttu-id="feb03-173">Interfaces de cliente para arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="feb03-173">Client Interfaces for Drag-and-Drop</span></span>

<span data-ttu-id="feb03-174">Las aplicaciones cliente de automatización de la interfaz de usuario usan las interfaces [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) y [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) para tener acceso a la información de arrastrar y colocar desde los elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="feb03-174">UI Automation client applications use the [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) and [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) interfaces to access drag-and-drop information from UI elements.</span></span>

 

 