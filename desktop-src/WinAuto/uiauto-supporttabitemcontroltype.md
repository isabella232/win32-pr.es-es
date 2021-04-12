---
title: TabItem (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control TabItem.
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control TabItem
- Automatización de la interfaz de usuario, tipo de control TabItem
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control TabItem
- Automatización de la interfaz de usuario, propiedades para el tipo de control TabItem
- Automatización de la interfaz de usuario, patrones de control para el tipo de control TabItem
- Automatización de la interfaz de usuario, eventos para el tipo de control TabItem
- estructuras de árbol, tipo de control TabItem
- Properties, tipo de control TabItem
- patrones de control, tipo de control TabItem
- Events, tipo de control TabItem
- compatibilidad con el tipo de control TabItem
- TabItem (tipo de control)
- tipos de control, estructura de árbol para el tipo de control TabItem
- tipos de control, patrones de control para el tipo de control TabItem
- tipos de control, compatibilidad con TabItem
- tipos de control, TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8f9f900240318de8629048f242cd755994c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269208"
---
# <a name="tabitem-control-type"></a><span data-ttu-id="c9cea-119">TabItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="c9cea-119">TabItem Control Type</span></span>

<span data-ttu-id="c9cea-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="c9cea-120">This topic provides information about Microsoft UI Automation support for the **TabItem** control type.</span></span>

<span data-ttu-id="c9cea-121">Un control de elemento de ficha se utiliza como el control dentro de un control de ficha que selecciona una página concreta para que se muestre en una ventana.</span><span class="sxs-lookup"><span data-stu-id="c9cea-121">A tab item control is used as the control within a tab control that selects a specific page to be shown in a window.</span></span>

<span data-ttu-id="c9cea-122">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="c9cea-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TabItem** control type.</span></span> <span data-ttu-id="c9cea-123">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de elemento de pestaña en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y</span><span class="sxs-lookup"><span data-stu-id="c9cea-123">The UI Automation requirements apply to all tab item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="c9cea-124">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="c9cea-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c9cea-125">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="c9cea-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="c9cea-126">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="c9cea-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="c9cea-127">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="c9cea-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="c9cea-128">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="c9cea-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="c9cea-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9cea-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="c9cea-130">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="c9cea-130">Typical Tree Structure</span></span>

<span data-ttu-id="c9cea-131">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de elemento de ficha y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="c9cea-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="c9cea-132">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c9cea-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9cea-133">Vista de control</span><span class="sxs-lookup"><span data-stu-id="c9cea-133">Control View</span></span></th>
<th><span data-ttu-id="c9cea-134">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="c9cea-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="c9cea-135">TabItem</span><span class="sxs-lookup"><span data-stu-id="c9cea-135">TabItem</span></span>
<ul>
<li><span data-ttu-id="c9cea-136">Image (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="c9cea-136">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="c9cea-137">Texto</span><span class="sxs-lookup"><span data-stu-id="c9cea-137">Text</span></span></li>
<li><span data-ttu-id="c9cea-138">Panel</span><span class="sxs-lookup"><span data-stu-id="c9cea-138">Pane</span></span>
<ul>
<li><span data-ttu-id="c9cea-139">Varios controles (0 o más)</span><span class="sxs-lookup"><span data-stu-id="c9cea-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c9cea-140">TabItem</span><span class="sxs-lookup"><span data-stu-id="c9cea-140">TabItem</span></span>
<ul>
<li><span data-ttu-id="c9cea-141">Panel</span><span class="sxs-lookup"><span data-stu-id="c9cea-141">Pane</span></span>
<ul>
<li><span data-ttu-id="c9cea-142">Varios controles (0 o más)</span><span class="sxs-lookup"><span data-stu-id="c9cea-142">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="c9cea-143">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="c9cea-143">Relevant Properties</span></span>

<span data-ttu-id="c9cea-144">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="c9cea-144">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TabItem** control type.</span></span> <span data-ttu-id="c9cea-145">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="c9cea-145">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="c9cea-146">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="c9cea-146">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="c9cea-147">Value</span><span class="sxs-lookup"><span data-stu-id="c9cea-147">Value</span></span>       | <span data-ttu-id="c9cea-148">Notas</span><span class="sxs-lookup"><span data-stu-id="c9cea-148">Notes</span></span>                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9cea-149">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="c9cea-150">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="c9cea-150">See notes.</span></span>  | <span data-ttu-id="c9cea-151">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c9cea-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                |
| [<span data-ttu-id="c9cea-152">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="c9cea-153">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="c9cea-153">See notes.</span></span>  | <span data-ttu-id="c9cea-154">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="c9cea-154">The outermost rectangle that contains the whole control.</span></span>                                                                                    |
| [<span data-ttu-id="c9cea-155">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="c9cea-156">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="c9cea-156">See notes.</span></span>  | <span data-ttu-id="c9cea-157">El control de elemento de ficha debe tener un punto en el que se pueda hacer clic que haga que se seleccione el elemento.</span><span class="sxs-lookup"><span data-stu-id="c9cea-157">The tab item control must have a clickable point that causes the item to become selected.</span></span>                                                   |
| [<span data-ttu-id="c9cea-158">**UIA \_ ControllerForPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-158">**UIA\_ControllerForPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="c9cea-159">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="c9cea-159">See notes.</span></span>  | <span data-ttu-id="c9cea-160">Esta propiedad se puede utilizar como un puntero al panel de ficha asociado.</span><span class="sxs-lookup"><span data-stu-id="c9cea-160">This property can be used as pointer to the associated tab pane.</span></span> <span data-ttu-id="c9cea-161">Esto es útil cuando no se puede hospedar un panel como un elemento secundario del objeto de elemento de ficha.</span><span class="sxs-lookup"><span data-stu-id="c9cea-161">This is useful when it cannot host a pane as child of the tab item object.</span></span> |
| [<span data-ttu-id="c9cea-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="c9cea-163">**TabItem**</span><span class="sxs-lookup"><span data-stu-id="c9cea-163">**TabItem**</span></span> | <span data-ttu-id="c9cea-164">Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c9cea-164">This value is the same for all UI frameworks.</span></span>                                                                                               |
| [<span data-ttu-id="c9cea-165">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c9cea-166">TRUE</span><span class="sxs-lookup"><span data-stu-id="c9cea-166">TRUE</span></span>        | <span data-ttu-id="c9cea-167">El control de elemento de ficha siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c9cea-167">The tab item control is always included in the content view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="c9cea-168">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c9cea-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="c9cea-169">TRUE</span></span>        | <span data-ttu-id="c9cea-170">El control de elemento de ficha siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c9cea-170">The tab item control is always included in the control view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="c9cea-171">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="c9cea-172">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="c9cea-172">See notes.</span></span>  | <span data-ttu-id="c9cea-173">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c9cea-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                   |
| [<span data-ttu-id="c9cea-174">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="c9cea-175">Null</span><span class="sxs-lookup"><span data-stu-id="c9cea-175">Null</span></span>        | <span data-ttu-id="c9cea-176">El control de elemento de ficha no tiene una etiqueta de texto estático.</span><span class="sxs-lookup"><span data-stu-id="c9cea-176">The tab item control does not have a static text label.</span></span>                                                                                     |
| [<span data-ttu-id="c9cea-177">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="c9cea-178">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="c9cea-178">See notes.</span></span>  | <span data-ttu-id="c9cea-179">Cadena localizada que corresponde al tipo de control **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="c9cea-179">Localized string corresponding to the **TabItem** control type.</span></span> <span data-ttu-id="c9cea-180">El valor predeterminado es "Tab Item" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="c9cea-180">The default value is "tab item" for en-US or English (United States).</span></span>       |
| [<span data-ttu-id="c9cea-181">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="c9cea-182">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="c9cea-182">See notes.</span></span>  | <span data-ttu-id="c9cea-183">Control de elemento de ficha con etiqueta automática.</span><span class="sxs-lookup"><span data-stu-id="c9cea-183">The tab item control self-labeled.</span></span>                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="c9cea-184">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="c9cea-184">Required Control Patterns</span></span>

<span data-ttu-id="c9cea-185">En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de elemento de ficha.</span><span class="sxs-lookup"><span data-stu-id="c9cea-185">The following table lists the UI Automation control patterns required to be supported by all tab item controls.</span></span> <span data-ttu-id="c9cea-186">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c9cea-186">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="c9cea-187">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="c9cea-187">Control Pattern</span></span>                                                 | <span data-ttu-id="c9cea-188">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="c9cea-188">Support</span></span>  | <span data-ttu-id="c9cea-189">Notas</span><span class="sxs-lookup"><span data-stu-id="c9cea-189">Notes</span></span>                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9cea-190">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="c9cea-190">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | <span data-ttu-id="c9cea-191">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c9cea-191">Required</span></span> | <span data-ttu-id="c9cea-192">El control de elemento de ficha debe admitir [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern).</span><span class="sxs-lookup"><span data-stu-id="c9cea-192">The tab item control must support [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern).</span></span> |
| [<span data-ttu-id="c9cea-193">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="c9cea-193">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | <span data-ttu-id="c9cea-194">Nunca</span><span class="sxs-lookup"><span data-stu-id="c9cea-194">Never</span></span>    | <span data-ttu-id="c9cea-195">El control de elemento de ficha nunca admite [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span><span class="sxs-lookup"><span data-stu-id="c9cea-195">The tab item control never supports [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span></span>             |



 

## <a name="required-events"></a><span data-ttu-id="c9cea-196">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="c9cea-196">Required Events</span></span>

<span data-ttu-id="c9cea-197">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que son necesarios para admitir los controles de elemento de pestaña.</span><span class="sxs-lookup"><span data-stu-id="c9cea-197">The following table lists the UI Automation events that tab item controls are required to support.</span></span> <span data-ttu-id="c9cea-198">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c9cea-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="c9cea-199">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="c9cea-199">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="c9cea-200">Notas</span><span class="sxs-lookup"><span data-stu-id="c9cea-200">Notes</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9cea-201">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                            |
| <span data-ttu-id="c9cea-202">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c9cea-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                            |
| <span data-ttu-id="c9cea-203">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c9cea-203">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="c9cea-204">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="c9cea-204">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="c9cea-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c9cea-205">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="c9cea-206">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="c9cea-206">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="c9cea-207">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-207">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) |                                                                                                                            |
| [<span data-ttu-id="c9cea-208">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-208">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         |                                                                                                                            |
| [<span data-ttu-id="c9cea-209">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="c9cea-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="c9cea-210">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9cea-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c9cea-211">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c9cea-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c9cea-212">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="c9cea-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="c9cea-213">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="c9cea-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




