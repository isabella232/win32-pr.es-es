---
title: SplitButton (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control SplitButton
- Automatización de la interfaz de usuario, tipo de control SplitButton
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control SplitButton
- Automatización de la interfaz de usuario, propiedades para el tipo de control SplitButton
- Automatización de la interfaz de usuario, patrones de control para el tipo de control SplitButton
- Automatización de la interfaz de usuario, eventos para el tipo de control SplitButton
- estructuras de árbol, tipo de control SplitButton
- propiedades, tipo de control SplitButton
- patrones de control, tipo de control SplitButton
- Events, tipo de control SplitButton
- compatibilidad con el tipo de control SplitButton
- SplitButton (tipo de control)
- tipos de control, estructura de árbol para el tipo de control SplitButton
- tipos de control, patrones de control para el tipo de control SplitButton
- tipos de control, compatibilidad con SplitButton
- tipos de control, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c56cd6b22838dfa92ba25ce05e74d228f4173ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778234"
---
# <a name="splitbutton-control-type"></a><span data-ttu-id="a3461-119">SplitButton (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="a3461-119">SplitButton Control Type</span></span>

<span data-ttu-id="a3461-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **splitButton** .</span><span class="sxs-lookup"><span data-stu-id="a3461-120">This topic provides information about Microsoft UI Automation support for the **SplitButton** control type.</span></span>

<span data-ttu-id="a3461-121">El control de botón de expansión permite realizar una acción en un control y expandir el control para ver una lista de otras acciones posibles que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="a3461-121">The split button control enables an action to be performed on a control, and to expand the control to see a list of other possible actions that can be performed.</span></span>

<span data-ttu-id="a3461-122">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario necesaria, las propiedades, los patrones de control y los eventos para el tipo de control **splitButton** .</span><span class="sxs-lookup"><span data-stu-id="a3461-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SplitButton** control type.</span></span> <span data-ttu-id="a3461-123">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de botón de expansión en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y</span><span class="sxs-lookup"><span data-stu-id="a3461-123">The UI Automation requirements apply to all split button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="a3461-124">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="a3461-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a3461-125">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="a3461-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="a3461-126">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="a3461-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="a3461-127">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="a3461-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="a3461-128">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="a3461-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="a3461-129">Ejemplo de tipo de control SplitButton</span><span class="sxs-lookup"><span data-stu-id="a3461-129">SplitButton Control Type Example</span></span>](#splitbutton-control-type-example)
-   [<span data-ttu-id="a3461-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3461-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="a3461-131">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="a3461-131">Typical Tree Structure</span></span>

<span data-ttu-id="a3461-132">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de botón de expansión y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="a3461-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to split button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="a3461-133">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a3461-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3461-134">Vista de control</span><span class="sxs-lookup"><span data-stu-id="a3461-134">Control View</span></span></th>
<th><span data-ttu-id="a3461-135">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="a3461-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="a3461-136">SplitButton</span><span class="sxs-lookup"><span data-stu-id="a3461-136">SplitButton</span></span>
<ul>
<li><span data-ttu-id="a3461-137">Image (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="a3461-137">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="a3461-138">Text (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="a3461-138">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="a3461-139">Button (1 o 2)</span><span class="sxs-lookup"><span data-stu-id="a3461-139">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="a3461-140">Menu (0 o 1; aparece como elemento secundario de un subbotón que admite el patrón ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="a3461-140">Menu (0 or 1; appears as a child of a sub-button that supports the ExpandCollapse pattern)</span></span>
<ul>
<li><span data-ttu-id="a3461-141">MenuItem (1 o varios)</span><span class="sxs-lookup"><span data-stu-id="a3461-141">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a3461-142">SplitButton</span><span class="sxs-lookup"><span data-stu-id="a3461-142">SplitButton</span></span>
<ul>
<li><span data-ttu-id="a3461-143">Button (1 o 2)</span><span class="sxs-lookup"><span data-stu-id="a3461-143">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="a3461-144">MenuItem (1 o varios)</span><span class="sxs-lookup"><span data-stu-id="a3461-144">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="a3461-145">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="a3461-145">Relevant Properties</span></span>

<span data-ttu-id="a3461-146">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **splitButton** .</span><span class="sxs-lookup"><span data-stu-id="a3461-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the **SplitButton** control type.</span></span> <span data-ttu-id="a3461-147">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="a3461-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="a3461-148">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="a3461-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="a3461-149">Value</span><span class="sxs-lookup"><span data-stu-id="a3461-149">Value</span></span>           | <span data-ttu-id="a3461-150">Notas</span><span class="sxs-lookup"><span data-stu-id="a3461-150">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3461-151">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a3461-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="a3461-152">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="a3461-152">See notes.</span></span>      | <span data-ttu-id="a3461-153">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a3461-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="a3461-154">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a3461-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="a3461-155">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="a3461-155">See notes.</span></span>      | <span data-ttu-id="a3461-156">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="a3461-156">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="a3461-157">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a3461-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="a3461-158">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="a3461-158">See notes.</span></span>      | <span data-ttu-id="a3461-159">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="a3461-159">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="a3461-160">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="a3461-160">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="a3461-161">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a3461-161">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="a3461-162">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="a3461-162">**SplitButton**</span></span> | <span data-ttu-id="a3461-163">Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a3461-163">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="a3461-164">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a3461-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="a3461-165">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="a3461-165">See notes.</span></span>      | <span data-ttu-id="a3461-166">El texto de ayuda puede indicar el resultado de la activación del botón de división, que normalmente es el mismo tipo de información que se presenta mediante un elemento de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="a3461-166">The help text can indicate the result of activating the split button, which is typically the same type of information presented through a tooltip.</span></span>                                                   |
| [<span data-ttu-id="a3461-167">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a3461-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="a3461-168">TRUE</span><span class="sxs-lookup"><span data-stu-id="a3461-168">TRUE</span></span>            | <span data-ttu-id="a3461-169">El control de botón de división contiene información para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="a3461-169">The split button control contains information for the end user.</span></span>                                                                                                                                      |
| [<span data-ttu-id="a3461-170">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a3461-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="a3461-171">TRUE</span><span class="sxs-lookup"><span data-stu-id="a3461-171">TRUE</span></span>            | <span data-ttu-id="a3461-172">El control de botón de división es visible para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="a3461-172">The split button control is visible to the end user.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="a3461-173">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a3461-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="a3461-174">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="a3461-174">See notes.</span></span>      | <span data-ttu-id="a3461-175">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="a3461-175">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="a3461-176">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a3461-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="a3461-177">NULL</span><span class="sxs-lookup"><span data-stu-id="a3461-177">NULL</span></span>            | <span data-ttu-id="a3461-178">Los controles de botón de expansión no tienen una etiqueta de texto estático.</span><span class="sxs-lookup"><span data-stu-id="a3461-178">Split button controls do not have a static text label.</span></span>                                                                                                                                               |
| [<span data-ttu-id="a3461-179">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a3461-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="a3461-180">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="a3461-180">See notes.</span></span>      | <span data-ttu-id="a3461-181">Cadena localizada que corresponde al tipo de control **splitButton** .</span><span class="sxs-lookup"><span data-stu-id="a3461-181">Localized string corresponding to the **SplitButton** control type.</span></span> <span data-ttu-id="a3461-182">El valor predeterminado es "Split Button" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="a3461-182">The default value is "split button" for en-US or English (United States).</span></span>                                                        |
| [<span data-ttu-id="a3461-183">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a3461-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="a3461-184">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="a3461-184">See notes.</span></span>      | <span data-ttu-id="a3461-185">Texto que se usa para etiquetar el botón de expansión.</span><span class="sxs-lookup"><span data-stu-id="a3461-185">The text that is used to label the split button.</span></span> <span data-ttu-id="a3461-186">Siempre que se utiliza una imagen para etiquetar un botón de expansión, se debe proporcionar texto alternativo para la propiedad nombre de botón de expansión.</span><span class="sxs-lookup"><span data-stu-id="a3461-186">Whenever an image is used to label a split button, alternate text must be supplied for the split button Name property.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="a3461-187">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="a3461-187">Required Control Patterns</span></span>

<span data-ttu-id="a3461-188">En la tabla siguiente se muestran los patrones de control de UI Automation que se deben admitir por todos los controles de botón de expansión.</span><span class="sxs-lookup"><span data-stu-id="a3461-188">The following table lists the UI Automation control patterns required to be supported by all split button controls.</span></span> <span data-ttu-id="a3461-189">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a3461-189">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="a3461-190">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="a3461-190">Control Pattern</span></span>                                                   | <span data-ttu-id="a3461-191">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="a3461-191">Support</span></span>  | <span data-ttu-id="a3461-192">Notas</span><span class="sxs-lookup"><span data-stu-id="a3461-192">Notes</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3461-193">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="a3461-193">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="a3461-194">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a3461-194">Required</span></span> | <span data-ttu-id="a3461-195">Dado que los botones de expansión siempre tienen la capacidad de expandir una lista de opciones, deben admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="a3461-195">Because split buttons always have the ability to expand a list of options, they must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span>                                                      |
| [<span data-ttu-id="a3461-196">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="a3461-196">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="a3461-197">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a3461-197">Required</span></span> | <span data-ttu-id="a3461-198">Dado que los botones de expansión siempre tienen una acción predeterminada asociada con el método [**IInvokeProvider:: Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) , deben admitir el patrón de control [Invoke](uiauto-implementinginvoke.md) .</span><span class="sxs-lookup"><span data-stu-id="a3461-198">Because split buttons always have a default action associated with the [**IInvokeProvider::Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) method, they must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="a3461-199">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="a3461-199">Required Events</span></span>

<span data-ttu-id="a3461-200">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que son necesarios para admitir.</span><span class="sxs-lookup"><span data-stu-id="a3461-200">The following table lists the UI Automation events that split button controls are required to support.</span></span> <span data-ttu-id="a3461-201">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a3461-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="a3461-202">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="a3461-202">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="a3461-203">Notas</span><span class="sxs-lookup"><span data-stu-id="a3461-203">Notes</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3461-204">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="a3461-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| <span data-ttu-id="a3461-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="a3461-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                            |
| <span data-ttu-id="a3461-206">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="a3461-206">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="a3461-207">**\_InvokedEventId de invocación de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="a3461-207">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| <span data-ttu-id="a3461-208">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="a3461-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="a3461-209">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="a3461-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="a3461-210">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="a3461-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="a3461-211">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="a3461-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="a3461-212">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="a3461-212">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a><span data-ttu-id="a3461-213">Ejemplo de tipo de control SplitButton</span><span class="sxs-lookup"><span data-stu-id="a3461-213">SplitButton Control Type Example</span></span>

<span data-ttu-id="a3461-214">En la imagen siguiente se muestra un control que implementa el tipo de control **splitButton** .</span><span class="sxs-lookup"><span data-stu-id="a3461-214">The following image illustrates a control that implements the **SplitButton** control type.</span></span>

![captura de pantalla que muestra un ejemplo de un control splitbutton](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3461-216">Árbol de UI Automation: vista de control</span><span class="sxs-lookup"><span data-stu-id="a3461-216">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="a3461-217">Árbol de UI Automation: vista de contenido</span><span class="sxs-lookup"><span data-stu-id="a3461-217">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="a3461-218">&quot;Nombre &quot; de splitButton (Invoke, ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="a3461-218">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="a3461-219">Opción de botón &quot; más &quot; (invocar)</span><span class="sxs-lookup"><span data-stu-id="a3461-219">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="a3461-220">Menú</span><span class="sxs-lookup"><span data-stu-id="a3461-220">Menu</span></span>
<ul>
<li><span data-ttu-id="a3461-221">MenuItem</span><span class="sxs-lookup"><span data-stu-id="a3461-221">MenuItem</span></span></li>
<li><span data-ttu-id="a3461-222">...</span><span class="sxs-lookup"><span data-stu-id="a3461-222">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a3461-223">&quot;Nombre &quot; de splitButton (Invoke, ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="a3461-223">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="a3461-224">Opción de botón &quot; más &quot; (invocar)</span><span class="sxs-lookup"><span data-stu-id="a3461-224">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="a3461-225">Menú</span><span class="sxs-lookup"><span data-stu-id="a3461-225">Menu</span></span>
<ul>
<li><span data-ttu-id="a3461-226">MenuItem</span><span class="sxs-lookup"><span data-stu-id="a3461-226">MenuItem</span></span></li>
<li><span data-ttu-id="a3461-227">...</span><span class="sxs-lookup"><span data-stu-id="a3461-227">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a3461-228">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3461-228">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a3461-229">**Vista**</span><span class="sxs-lookup"><span data-stu-id="a3461-229">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a3461-230">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="a3461-230">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="a3461-231">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="a3461-231">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




