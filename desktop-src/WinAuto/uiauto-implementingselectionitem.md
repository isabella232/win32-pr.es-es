---
title: Patrón de control SelectionItem
description: Describe las directrices y convenciones para implementar ISelectionItemProvider, incluida información sobre propiedades, métodos y eventos.
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control SelectionItem
- Automatización de la interfaz de usuario, patrón de control SelectionItem
- Automatización de la interfaz de usuario, ISelectionItemProvider
- ISelectionItemProvider
- implementación de patrones de control SelectionItem de UI Automation
- Patrones de control de SelectionItem
- patrones de control, ISelectionItemProvider
- patrones de control, implementar la automatización de la interfaz de usuario SelectionItem
- patrones de control, SelectionItem
- interfaces, ISelectionItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704581"
---
# <a name="selectionitem-control-pattern"></a><span data-ttu-id="be1c3-113">Patrón de control SelectionItem</span><span class="sxs-lookup"><span data-stu-id="be1c3-113">SelectionItem Control Pattern</span></span>

<span data-ttu-id="be1c3-114">Describe las directrices y convenciones para implementar [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), incluida información sobre propiedades, métodos y eventos.</span><span class="sxs-lookup"><span data-stu-id="be1c3-114">Describes guidelines and conventions for implementing [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="be1c3-115">El patrón de control **SelectionItem** se usa para admitir controles que actúan como elementos secundarios individuales seleccionables de controles de contenedor que implementan [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="be1c3-115">The **SelectionItem** control pattern is used to support controls that act as individual, selectable child items of container controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>

<span data-ttu-id="be1c3-116">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="be1c3-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="be1c3-117">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="be1c3-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="be1c3-118">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="be1c3-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="be1c3-119">Miembros requeridos para **ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="be1c3-119">Required Members for **ISelectionItemProvider**</span></span>](#required-members-for-iselectionitemprovider)
-   [<span data-ttu-id="be1c3-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="be1c3-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="be1c3-121">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="be1c3-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="be1c3-122">Al implementar el patrón de control **SelectionItem** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="be1c3-122">When implementing the **SelectionItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="be1c3-123">Los controles de selección única que administran los controles secundarios que implementan [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), como el control deslizante de **resolución de pantalla** del cuadro de diálogo **propiedades de pantalla** para Windows, deben implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); sus elementos secundarios deben implementar [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) y [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="be1c3-123">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

## <a name="required-members-for-iselectionitemprovider"></a><span data-ttu-id="be1c3-124">Miembros requeridos para **ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="be1c3-124">Required Members for **ISelectionItemProvider**</span></span>

<span data-ttu-id="be1c3-125">Se requieren las siguientes propiedades, métodos y eventos para implementar la interfaz [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="be1c3-125">The following properties, methods, and events are required for implementing the [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) interface.</span></span>



| <span data-ttu-id="be1c3-126">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="be1c3-126">Required members</span></span>                                                                                                                        | <span data-ttu-id="be1c3-127">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="be1c3-127">Member type</span></span> | <span data-ttu-id="be1c3-128">Notas</span><span class="sxs-lookup"><span data-stu-id="be1c3-128">Notes</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="be1c3-129">**AddToSelection**</span><span class="sxs-lookup"><span data-stu-id="be1c3-129">**AddToSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | <span data-ttu-id="be1c3-130">Método</span><span class="sxs-lookup"><span data-stu-id="be1c3-130">Method</span></span>      | <span data-ttu-id="be1c3-131">None</span><span class="sxs-lookup"><span data-stu-id="be1c3-131">None</span></span>  |
| [<span data-ttu-id="be1c3-132">**IsSelected**</span><span class="sxs-lookup"><span data-stu-id="be1c3-132">**IsSelected**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | <span data-ttu-id="be1c3-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="be1c3-133">Property</span></span>    | <span data-ttu-id="be1c3-134">None</span><span class="sxs-lookup"><span data-stu-id="be1c3-134">None</span></span>  |
| [<span data-ttu-id="be1c3-135">**RemoveFromSelection**</span><span class="sxs-lookup"><span data-stu-id="be1c3-135">**RemoveFromSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | <span data-ttu-id="be1c3-136">Método</span><span class="sxs-lookup"><span data-stu-id="be1c3-136">Method</span></span>      | <span data-ttu-id="be1c3-137">None</span><span class="sxs-lookup"><span data-stu-id="be1c3-137">None</span></span>  |
| [<span data-ttu-id="be1c3-138">**Seleccionar**</span><span class="sxs-lookup"><span data-stu-id="be1c3-138">**Select**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | <span data-ttu-id="be1c3-139">Método</span><span class="sxs-lookup"><span data-stu-id="be1c3-139">Method</span></span>      | <span data-ttu-id="be1c3-140">None</span><span class="sxs-lookup"><span data-stu-id="be1c3-140">None</span></span>  |
| [<span data-ttu-id="be1c3-141">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="be1c3-141">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | <span data-ttu-id="be1c3-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="be1c3-142">Property</span></span>    | <span data-ttu-id="be1c3-143">None</span><span class="sxs-lookup"><span data-stu-id="be1c3-143">None</span></span>  |
| [<span data-ttu-id="be1c3-144">**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="be1c3-144">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)         | <span data-ttu-id="be1c3-145">Evento</span><span class="sxs-lookup"><span data-stu-id="be1c3-145">Event</span></span>       | <span data-ttu-id="be1c3-146">None</span><span class="sxs-lookup"><span data-stu-id="be1c3-146">None</span></span>  |
| [<span data-ttu-id="be1c3-147">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="be1c3-147">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="be1c3-148">Evento</span><span class="sxs-lookup"><span data-stu-id="be1c3-148">Event</span></span>       | <span data-ttu-id="be1c3-149">None</span><span class="sxs-lookup"><span data-stu-id="be1c3-149">None</span></span>  |
| [<span data-ttu-id="be1c3-150">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="be1c3-150">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="be1c3-151">Evento</span><span class="sxs-lookup"><span data-stu-id="be1c3-151">Event</span></span>       | <span data-ttu-id="be1c3-152">None</span><span class="sxs-lookup"><span data-stu-id="be1c3-152">None</span></span>  |



 

<span data-ttu-id="be1c3-153">Si el resultado de una [**selección**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), un [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)o un [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) es un elemento seleccionado único, se debe producir un evento **ElementSelected** ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)); de lo contrario, genere los eventos **ElementAddedToSelection** ([**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)) o **ElementRemovedFromSelection** ([**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) según corresponda.</span><span class="sxs-lookup"><span data-stu-id="be1c3-153">If the result of a [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), an [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection), or a [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) is a single selected item, an **ElementSelected** event ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)) should be raised; otherwise raise **ElementAddedToSelection** ([**UIA\_SelectionItem\_ElementAddedToSelectionEventId**](uiauto-event-ids.md)) or **ElementRemovedFromSelection** ([**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) events as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be1c3-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="be1c3-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be1c3-155">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="be1c3-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="be1c3-156">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="be1c3-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="be1c3-157">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="be1c3-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




