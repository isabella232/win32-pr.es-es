---
title: CheckBox (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control CheckBox.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control CheckBox
- UI Automation, CheckBox (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control CheckBox
- Automatización de la interfaz de usuario, propiedades para el tipo de control CheckBox
- Automatización de la interfaz de usuario, patrones de control para el tipo de control CheckBox
- Automatización de la interfaz de usuario, eventos para el tipo de control CheckBox
- estructuras de árbol, CheckBox (tipo de control)
- Properties, CheckBox (tipo de control)
- patrones de control, CheckBox (tipo de control)
- Events, CheckBox (tipo de control)
- compatibilidad con el tipo de control CheckBox
- CheckBox (tipo de control)
- tipos de control, estructura de árbol para el tipo de control CheckBox
- tipos de control, patrones de control para el tipo de control CheckBox
- tipos de control, compatibilidad con CheckBox
- tipos de control, CheckBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e5bac106c8ba3bbf58c7f5b06c087ceb7b3418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903444"
---
# <a name="checkbox-control-type"></a><span data-ttu-id="4bfe1-119">CheckBox (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="4bfe1-119">CheckBox Control Type</span></span>

<span data-ttu-id="4bfe1-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="4bfe1-120">This topic provides information about Microsoft UI Automation support for the **CheckBox** control type.</span></span>

<span data-ttu-id="4bfe1-121">Una casilla es un objeto que se usa para indicar un estado con el que los usuarios pueden interactuar para recorrer cíclicamente dicho estado.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-121">A check box is an object used to indicate a state that users can interact with to cycle through that state.</span></span> <span data-ttu-id="4bfe1-122">Las casillas le presentan al usuario una opción binaria (Sí/No), (Activado/Desactivado) o terciaria (Activado, Desactivado, Indeterminado).</span><span class="sxs-lookup"><span data-stu-id="4bfe1-122">Check boxes either present a binary (Yes/No), (On/Off), or tertiary (On, Off, Indeterminate) option to the user.</span></span>

<span data-ttu-id="4bfe1-123">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="4bfe1-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **CheckBox** control type.</span></span> <span data-ttu-id="4bfe1-124">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de casilla donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-124">The UI Automation requirements apply to all check box controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="4bfe1-125">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4bfe1-126">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="4bfe1-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="4bfe1-127">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="4bfe1-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="4bfe1-128">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="4bfe1-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="4bfe1-129">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="4bfe1-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="4bfe1-130">DefaultAction</span><span class="sxs-lookup"><span data-stu-id="4bfe1-130">DefaultAction</span></span>](#defaultaction)
-   [<span data-ttu-id="4bfe1-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4bfe1-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="4bfe1-132">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="4bfe1-132">Typical Tree Structure</span></span>

<span data-ttu-id="4bfe1-133">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de casilla y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to check box controls and describes what can be contained in each view.</span></span> <span data-ttu-id="4bfe1-134">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4bfe1-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bfe1-135">Vista de control</span><span class="sxs-lookup"><span data-stu-id="4bfe1-135">Control View</span></span></th>
<th><span data-ttu-id="4bfe1-136">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="4bfe1-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4bfe1-137">CheckBox</span><span class="sxs-lookup"><span data-stu-id="4bfe1-137">CheckBox</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4bfe1-138">CheckBox</span><span class="sxs-lookup"><span data-stu-id="4bfe1-138">CheckBox</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="4bfe1-139">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="4bfe1-139">Relevant Properties</span></span>

<span data-ttu-id="4bfe1-140">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="4bfe1-140">The following table lists the UI Automation properties whose value or definition is especially relevant to the **CheckBox** control type.</span></span> <span data-ttu-id="4bfe1-141">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="4bfe1-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="4bfe1-142">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="4bfe1-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="4bfe1-143">Value</span><span class="sxs-lookup"><span data-stu-id="4bfe1-143">Value</span></span>        | <span data-ttu-id="4bfe1-144">Notas</span><span class="sxs-lookup"><span data-stu-id="4bfe1-144">Notes</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bfe1-145">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="4bfe1-146">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-146">See notes.</span></span>   | <span data-ttu-id="4bfe1-147">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="4bfe1-148">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="4bfe1-149">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-149">See notes.</span></span>   | <span data-ttu-id="4bfe1-150">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="4bfe1-151">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="4bfe1-152">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-152">See notes.</span></span>   | <span data-ttu-id="4bfe1-153">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="4bfe1-154">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                               |
| [<span data-ttu-id="4bfe1-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="4bfe1-156">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-156">**CheckBox**</span></span> |                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="4bfe1-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4bfe1-158">TRUE</span><span class="sxs-lookup"><span data-stu-id="4bfe1-158">TRUE</span></span>         | <span data-ttu-id="4bfe1-159">El valor de esta propiedad siempre debe ser **true**.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-159">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="4bfe1-160">Esto significa que el control de casilla siempre debe incluirse en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-160">This means that the check box control must always be included in the content view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="4bfe1-161">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4bfe1-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="4bfe1-162">TRUE</span></span>         | <span data-ttu-id="4bfe1-163">El valor de esta propiedad siempre debe ser **true**.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-163">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="4bfe1-164">Esto significa que el control de casilla siempre debe incluirse en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-164">This means that the check box control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="4bfe1-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="4bfe1-166">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-166">See notes.</span></span>   | <span data-ttu-id="4bfe1-167">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-167">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="4bfe1-168">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="4bfe1-169">Null</span><span class="sxs-lookup"><span data-stu-id="4bfe1-169">Null</span></span>         | <span data-ttu-id="4bfe1-170">Los controles de casilla se etiquetan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-170">Check box controls are self-labeling.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="4bfe1-171">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="4bfe1-172">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-172">See notes.</span></span>   | <span data-ttu-id="4bfe1-173">Cadena localizada que corresponde al tipo de control **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="4bfe1-173">Localized string corresponding to the **CheckBox** control type.</span></span> <span data-ttu-id="4bfe1-174">El valor predeterminado es "casilla" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="4bfe1-174">The default value is "check box" for en-US or English (United States).</span></span>                                                                                                                                            |
| [<span data-ttu-id="4bfe1-175">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="4bfe1-176">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-176">See notes.</span></span>   | <span data-ttu-id="4bfe1-177">El valor de la propiedad [**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (o [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) del control de casilla es el texto que se muestra junto al cuadro que mantiene el estado de alternancia.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-177">The value of the check box control's [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (or [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) property is the text that is displayed beside the box that maintains the toggle state.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="4bfe1-178">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="4bfe1-178">Required Control Patterns</span></span>

<span data-ttu-id="4bfe1-179">En la tabla siguiente se muestran los patrones de control de UI Automation que se deben admitir por todos los controles de casilla.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-179">The following table lists the UI Automation control patterns required to be supported by all check box controls.</span></span> <span data-ttu-id="4bfe1-180">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4bfe1-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="4bfe1-181">Patrón de control/Propiedad de patrón</span><span class="sxs-lookup"><span data-stu-id="4bfe1-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="4bfe1-182">Soporte técnico/valor</span><span class="sxs-lookup"><span data-stu-id="4bfe1-182">Support/Value</span></span> | <span data-ttu-id="4bfe1-183">Notas</span><span class="sxs-lookup"><span data-stu-id="4bfe1-183">Notes</span></span>                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bfe1-184">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-184">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="4bfe1-185">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4bfe1-185">Required</span></span>      | <span data-ttu-id="4bfe1-186">Las casillas admiten el patrón de control [Toggle](uiauto-implementingtoggle.md) para permitir que la casilla se recorra mediante programación a través de sus Estados internos.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-186">Check boxes support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the check box to be programmatically cycled through its internal states.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="4bfe1-187">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="4bfe1-187">Required Events</span></span>

<span data-ttu-id="4bfe1-188">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que deben admitir los controles de casilla.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-188">The following table lists the UI Automation events that check box controls are required to support.</span></span> <span data-ttu-id="4bfe1-189">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4bfe1-189">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="4bfe1-190">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="4bfe1-190">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="4bfe1-191">Notas</span><span class="sxs-lookup"><span data-stu-id="4bfe1-191">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bfe1-192">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-192">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="4bfe1-193">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-193">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="4bfe1-194">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-194">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="4bfe1-195">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-195">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="4bfe1-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="4bfe1-197">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| [<span data-ttu-id="4bfe1-198">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-198">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="4bfe1-199">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-199">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="defaultaction"></a><span data-ttu-id="4bfe1-200">DefaultAction</span><span class="sxs-lookup"><span data-stu-id="4bfe1-200">DefaultAction</span></span>

<span data-ttu-id="4bfe1-201">La acción predeterminada de la casilla es hacer que un botón de radio reciba el foco y alterne su estado actual.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-201">The default action of the check box is to cause a radio button to become focused and toggle its current state.</span></span> <span data-ttu-id="4bfe1-202">Como se mencionó anteriormente, las casillas presentan una decisión binaria (sí/no o activada/desactivada) para el usuario o una terciaria (activado, desactivado, indeterminado).</span><span class="sxs-lookup"><span data-stu-id="4bfe1-202">As mentioned previously, check boxes either present a binary (Yes/No or On/Off) decision to the user or a tertiary (On, Off, Indeterminate).</span></span> <span data-ttu-id="4bfe1-203">Si la casilla es binaria, la acción predeterminada hace que el estado "activado" se convierta en "desactivado" o que el estado "desactivado" pase a "activado".</span><span class="sxs-lookup"><span data-stu-id="4bfe1-203">If the check box is binary the default action causes the "on" state to become "off" or the "off" state to become "on".</span></span> <span data-ttu-id="4bfe1-204">En una casilla terciaria, la acción predeterminada recorre los Estados de la casilla en el mismo orden que si el usuario hubiera enviado sucesivos clics del mouse al control.</span><span class="sxs-lookup"><span data-stu-id="4bfe1-204">In a tertiary check box the default action cycles through the states of the check box in the same order as if the user had sent successive mouse clicks to the control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bfe1-205">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4bfe1-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4bfe1-206">**Vista**</span><span class="sxs-lookup"><span data-stu-id="4bfe1-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4bfe1-207">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4bfe1-207">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="4bfe1-208">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="4bfe1-208">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




