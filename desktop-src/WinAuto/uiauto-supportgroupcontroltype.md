---
title: Group (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Group.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Group
- Automatización de la interfaz de usuario, tipo de control Group
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Group
- Automatización de la interfaz de usuario, propiedades para el tipo de control Group
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Group
- Automatización de la interfaz de usuario, eventos para el tipo de control Group
- estructuras de árbol, tipo de control Group
- propiedades, Group (tipo de control)
- patrones de control, Group (tipo de control)
- Events, Group (tipo de control)
- compatibilidad con el tipo de control Group
- Group (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Group
- tipos de control, patrones de control para el tipo de control Group
- tipos de control, compatibilidad con grupos
- tipos de control, grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b630d0ef736d937e4f024c8131adc4c843b6e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418639"
---
# <a name="group-control-type"></a><span data-ttu-id="55943-119">Group (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="55943-119">Group Control Type</span></span>

<span data-ttu-id="55943-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Group** .</span><span class="sxs-lookup"><span data-stu-id="55943-120">This topic provides information about Microsoft UI Automation support for the **Group** control type.</span></span>

<span data-ttu-id="55943-121">Un control de grupo representa un nodo dentro de una jerarquía.</span><span class="sxs-lookup"><span data-stu-id="55943-121">A group control represents a node within a hierarchy.</span></span> <span data-ttu-id="55943-122">El tipo de control **Group** crea una separación en el árbol de automatización de la interfaz de usuario para que los elementos que se agrupan tienen una división lógica dentro del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="55943-122">The **Group** control type creates a separation in the UI Automation tree so items that are grouped together have a logical division within the UI Automation tree.</span></span>

<span data-ttu-id="55943-123">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Group** .</span><span class="sxs-lookup"><span data-stu-id="55943-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Group** control type.</span></span> <span data-ttu-id="55943-124">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de grupo donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y los patrones</span><span class="sxs-lookup"><span data-stu-id="55943-124">The UI Automation requirements apply to all group controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="55943-125">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="55943-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="55943-126">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="55943-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="55943-127">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="55943-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="55943-128">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="55943-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="55943-129">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="55943-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="55943-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55943-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="55943-131">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="55943-131">Typical Tree Structure</span></span>

<span data-ttu-id="55943-132">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de grupo y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="55943-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to group controls and describes what can be contained in each view.</span></span> <span data-ttu-id="55943-133">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55943-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55943-134">Vista de control</span><span class="sxs-lookup"><span data-stu-id="55943-134">Control View</span></span></th>
<th><span data-ttu-id="55943-135">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="55943-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="55943-136">Grupo</span><span class="sxs-lookup"><span data-stu-id="55943-136">Group</span></span>
<ul>
<li><span data-ttu-id="55943-137">0 o varios controles</span><span class="sxs-lookup"><span data-stu-id="55943-137">0 or many controls</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="55943-138">Grupo</span><span class="sxs-lookup"><span data-stu-id="55943-138">Group</span></span>
<ul>
<li><span data-ttu-id="55943-139">0 o varios controles</span><span class="sxs-lookup"><span data-stu-id="55943-139">0 or many controls</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="55943-140">Los controles de grupo suelen incluir compatibilidad de UI Automation para los tipos de control que se encuentran debajo de ellos en el subárbol, incluidos los tipos de control [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md)y [DataItem](uiauto-supportdataitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="55943-140">Group controls typically include UI Automation support for control types found below them in the subtree, including the [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md), and [DataItem](uiauto-supportdataitemcontroltype.md) control types.</span></span> <span data-ttu-id="55943-141">Dado que un control de grupo es un contenedor genérico, es posible que cualquier tipo de control esté bajo el control de grupo en el árbol.</span><span class="sxs-lookup"><span data-stu-id="55943-141">Because a group control is a generic container, it is possible for any type of control to be under the group control in the tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="55943-142">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="55943-142">Relevant Properties</span></span>

<span data-ttu-id="55943-143">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de grupo.</span><span class="sxs-lookup"><span data-stu-id="55943-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the group controls.</span></span> <span data-ttu-id="55943-144">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="55943-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="55943-145">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="55943-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="55943-146">Value</span><span class="sxs-lookup"><span data-stu-id="55943-146">Value</span></span>      | <span data-ttu-id="55943-147">Notas</span><span class="sxs-lookup"><span data-stu-id="55943-147">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55943-148">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55943-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="55943-149">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="55943-149">See notes.</span></span> | <span data-ttu-id="55943-150">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="55943-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="55943-151">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="55943-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="55943-152">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="55943-152">See notes.</span></span> | <span data-ttu-id="55943-153">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="55943-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="55943-154">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55943-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="55943-155">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="55943-155">See notes.</span></span> | <span data-ttu-id="55943-156">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="55943-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="55943-157">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="55943-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="55943-158">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="55943-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="55943-159">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="55943-159">**Group**</span></span>  |                                                                                                                                                                                                      |
| [<span data-ttu-id="55943-160">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55943-160">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="55943-161">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="55943-161">**TRUE**</span></span>   | <span data-ttu-id="55943-162">El control de grupo siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="55943-162">The group control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="55943-163">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55943-163">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="55943-164">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="55943-164">**TRUE**</span></span>   | <span data-ttu-id="55943-165">El control de grupo siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="55943-165">The group control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="55943-166">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="55943-166">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="55943-167">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="55943-167">See notes.</span></span> | <span data-ttu-id="55943-168">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="55943-168">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="55943-169">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55943-169">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="55943-170">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="55943-170">See notes.</span></span> | <span data-ttu-id="55943-171">Los controles de grupo suelen etiquetarse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="55943-171">Group controls are typically self-labeling.</span></span> <span data-ttu-id="55943-172">En estos casos, devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="55943-172">In these cases, return **NULL**.</span></span> <span data-ttu-id="55943-173">Si el grupo tiene una etiqueta de texto estático, devuelva la etiqueta como el valor de la propiedad **LabeledBy** .</span><span class="sxs-lookup"><span data-stu-id="55943-173">If the group has a static text label, return the label as the value of the **LabeledBy** property.</span></span>                      |
| [<span data-ttu-id="55943-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="55943-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="55943-175">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="55943-175">See notes.</span></span> | <span data-ttu-id="55943-176">Cadena localizada que corresponde al tipo de control **Group** .</span><span class="sxs-lookup"><span data-stu-id="55943-176">Localized string corresponding to the **Group** control type.</span></span> <span data-ttu-id="55943-177">El valor predeterminado es "Group" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="55943-177">The default value is "group" for en-US or English (United States).</span></span>                                                                     |
| [<span data-ttu-id="55943-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="55943-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="55943-179">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="55943-179">See notes.</span></span> | <span data-ttu-id="55943-180">El control de grupo suele recibir su nombre del texto que etiqueta el control.</span><span class="sxs-lookup"><span data-stu-id="55943-180">The group control typically gets its name from the text that labels the control.</span></span>                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="55943-181">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="55943-181">Required Control Patterns</span></span>

<span data-ttu-id="55943-182">En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que se deben admitir para el tipo de control **Group** .</span><span class="sxs-lookup"><span data-stu-id="55943-182">The following table lists the UI Automation control patterns required to be supported for the **Group** control type.</span></span> <span data-ttu-id="55943-183">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55943-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="55943-184">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="55943-184">Control Pattern</span></span>                                                   | <span data-ttu-id="55943-185">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="55943-185">Support</span></span> | <span data-ttu-id="55943-186">Notas</span><span class="sxs-lookup"><span data-stu-id="55943-186">Notes</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55943-187">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="55943-187">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="55943-188">Depende</span><span class="sxs-lookup"><span data-stu-id="55943-188">Depends</span></span> | <span data-ttu-id="55943-189">Los controles de grupo que se pueden usar para mostrar u ocultar información deben admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="55943-189">Group controls that can be used to show or hide information must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="55943-190">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="55943-190">Required Events</span></span>

<span data-ttu-id="55943-191">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de grupo deben admitir.</span><span class="sxs-lookup"><span data-stu-id="55943-191">The following table lists the UI Automation events that group controls are required to support.</span></span> <span data-ttu-id="55943-192">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55943-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="55943-193">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="55943-193">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="55943-194">Notas</span><span class="sxs-lookup"><span data-stu-id="55943-194">Notes</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55943-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="55943-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| <span data-ttu-id="55943-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="55943-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                                  |
| <span data-ttu-id="55943-197">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="55943-197">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="55943-198">Si el control admite el patrón de control patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="55943-198">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern control pattern, it must support this event.</span></span> |
| <span data-ttu-id="55943-199">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="55943-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="55943-200">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="55943-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                         |
| <span data-ttu-id="55943-201">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="55943-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="55943-202">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="55943-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                       |
| <span data-ttu-id="55943-203">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="55943-203">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="55943-204">Si el control admite el patrón de control [Toggle](uiauto-implementingtoggle.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="55943-204">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                                 |
| [<span data-ttu-id="55943-205">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="55943-205">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="55943-206">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55943-206">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="55943-207">**Vista**</span><span class="sxs-lookup"><span data-stu-id="55943-207">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="55943-208">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="55943-208">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="55943-209">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="55943-209">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




