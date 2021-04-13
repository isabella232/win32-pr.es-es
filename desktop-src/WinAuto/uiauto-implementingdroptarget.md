---
title: Patrón de control DropTarget
description: Proporciona directrices y convenciones para implementar el patrón de control DropTarget mediante IDropTargetProvider, incluida información sobre propiedades y métodos.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control DropTarget
- Automatización de la interfaz de usuario, patrón de control DropTarget
- Automatización de la interfaz de usuario, IDropTargetProvider
- IDropTargetProvider
- implementación de patrones de control DropTarget de UI Automation
- Patrones de control de DropTarget
- patrones de control, IDropTargetProvider
- patrones de control, implementar la automatización de la interfaz de usuario DropTarget
- patrones de control, DropTarget
- interfaces, IDropTargetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd03d219ce8b26a0ac01806ebab09892a027fbd1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359152"
---
# <a name="droptarget-control-pattern"></a><span data-ttu-id="82167-113">Patrón de control DropTarget</span><span class="sxs-lookup"><span data-stu-id="82167-113">DropTarget Control Pattern</span></span>

<span data-ttu-id="82167-114">Proporciona directrices y convenciones para implementar el patrón de control **DropTarget** mediante [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="82167-114">Provides guidelines and conventions for implementing the **DropTarget** control pattern by using [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), including information about properties and methods.</span></span> <span data-ttu-id="82167-115">El patrón de control **DropTarget** se usa para admitir controles que pueden ser el destino de una operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="82167-115">The **DropTarget** control pattern is used to support controls that can be the target of a drag-and-drop operation.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="82167-116">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="82167-116">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="82167-117">Al implementar el patrón de control **DropTarget** , use las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="82167-117">When implementing the **DropTarget** control pattern, use the following guidelines and conventions:</span></span>

-   <span data-ttu-id="82167-118">Se debe admitir el patrón **DropTarget** mientras se está realizando una operación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="82167-118">The **DropTarget** pattern must be supported while a drag operation is in progress.</span></span> <span data-ttu-id="82167-119">Se puede admitir incluso cuando una operación de arrastre no está en curso.</span><span class="sxs-lookup"><span data-stu-id="82167-119">It can be supported even when a drag operation is not in progress.</span></span>
-   <span data-ttu-id="82167-120">La propiedad [**IDropTargetProvider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="82167-120">The [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property is required.</span></span>
-   <span data-ttu-id="82167-121">La propiedad [**IDropTargetProvider::D roptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) es necesaria cuando hay más de un efecto de colocación posible para el destino.</span><span class="sxs-lookup"><span data-stu-id="82167-121">The [**IDropTargetProvider::DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) property is required when there is more than one possible drop effect for the target.</span></span>
-   <span data-ttu-id="82167-122">El elemento debe provocar eventos de cambio de propiedad para las propiedades **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) y **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) cuando cambien.</span><span class="sxs-lookup"><span data-stu-id="82167-122">The element must raise property changed events for the **DropTargetEffect** ([**UIA\_DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) and **DropTargetEffects** ([**UIA\_DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) properties when they change.</span></span>

## <a name="required-members-for-idroptargetprovider"></a><span data-ttu-id="82167-123">Miembros requeridos para **IDropTargetProvider**</span><span class="sxs-lookup"><span data-stu-id="82167-123">Required Members for **IDropTargetProvider**</span></span>

<span data-ttu-id="82167-124">Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) .</span><span class="sxs-lookup"><span data-stu-id="82167-124">The following properties and methods are required for implementing the [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) interface.</span></span>



| <span data-ttu-id="82167-125">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="82167-125">Required members</span></span>                                                                              | <span data-ttu-id="82167-126">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="82167-126">Member type</span></span> | <span data-ttu-id="82167-127">Notas</span><span class="sxs-lookup"><span data-stu-id="82167-127">Notes</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="82167-128">**DropTargetEffect**</span><span class="sxs-lookup"><span data-stu-id="82167-128">**DropTargetEffect**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | <span data-ttu-id="82167-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82167-129">Property</span></span>    | <span data-ttu-id="82167-130">None</span><span class="sxs-lookup"><span data-stu-id="82167-130">None</span></span>                                                                     |
| [<span data-ttu-id="82167-131">**DropTargetEffects**</span><span class="sxs-lookup"><span data-stu-id="82167-131">**DropTargetEffects**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | <span data-ttu-id="82167-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82167-132">Property</span></span>    | <span data-ttu-id="82167-133">Obligatorio si el destino de colocación admite más de un posible efecto de colocación.</span><span class="sxs-lookup"><span data-stu-id="82167-133">Required if the drop target supports more than one possible drop effect.</span></span> |
| [<span data-ttu-id="82167-134">**UIA \_ DropTarget \_ DragEnterEventId**</span><span class="sxs-lookup"><span data-stu-id="82167-134">**UIA\_DropTarget\_DragEnterEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="82167-135">Evento</span><span class="sxs-lookup"><span data-stu-id="82167-135">Event</span></span>       | <span data-ttu-id="82167-136">None</span><span class="sxs-lookup"><span data-stu-id="82167-136">None</span></span>                                                                     |
| [<span data-ttu-id="82167-137">**UIA \_ DropTarget \_ DragLeaveEventId**</span><span class="sxs-lookup"><span data-stu-id="82167-137">**UIA\_DropTarget\_DragLeaveEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="82167-138">Evento</span><span class="sxs-lookup"><span data-stu-id="82167-138">Event</span></span>       | <span data-ttu-id="82167-139">None</span><span class="sxs-lookup"><span data-stu-id="82167-139">None</span></span>                                                                     |
| [<span data-ttu-id="82167-140">**UIA \_ DropTarget \_ DroppedEventId**</span><span class="sxs-lookup"><span data-stu-id="82167-140">**UIA\_DropTarget\_DroppedEventId**</span></span>](uiauto-event-ids.md)     | <span data-ttu-id="82167-141">Evento</span><span class="sxs-lookup"><span data-stu-id="82167-141">Event</span></span>       | <span data-ttu-id="82167-142">None</span><span class="sxs-lookup"><span data-stu-id="82167-142">None</span></span>                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="82167-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82167-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82167-144">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="82167-144">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="82167-145">Arrastrar patrón de control</span><span class="sxs-lookup"><span data-stu-id="82167-145">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[<span data-ttu-id="82167-146">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="82167-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="82167-147">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="82167-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="82167-148">Compatibilidad de UI Automation para arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="82167-148">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 