---
title: Thumb (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Thumb
- Automatización de la interfaz de usuario, Thumb (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Thumb
- Automatización de la interfaz de usuario, propiedades para el tipo de control Thumb
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Thumb
- Automatización de la interfaz de usuario, eventos para el tipo de control Thumb
- estructuras de árbol, Thumb (tipo de control)
- propiedades, Thumb (tipo de control)
- patrones de control, Thumb (tipo de control)
- Events, Thumb (tipo de control)
- compatibilidad con el tipo de control Thumb
- Thumb (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Thumb
- tipos de control, patrones de control para el tipo de control Thumb
- tipos de control, compatibilidad con Thumb
- tipos de control, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8faf60fab30f54d3ed3e4b5a9f49628a3a35be5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419082"
---
# <a name="thumb-control-type"></a><span data-ttu-id="9772f-119">Thumb (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="9772f-119">Thumb Control Type</span></span>

<span data-ttu-id="9772f-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="9772f-120">This topic provides information about Microsoft UI Automation support for the **Thumb** control type.</span></span>

<span data-ttu-id="9772f-121">Los controles de posición ofrecen la funcionalidad que permite que un control se mueva (o se arrastre), como un botón de barra de desplazamiento, o que cambie su tamaño, como un widget para cambiar el tamaño de una ventana.</span><span class="sxs-lookup"><span data-stu-id="9772f-121">Thumb controls provide the functionality that enables a control to be moved (or dragged), such as a scroll bar button, or resized, such as a window resizing widget.</span></span> <span data-ttu-id="9772f-122">Tenga en cuenta que un control Thumb no proporciona la funcionalidad de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="9772f-122">Note that a thumb control does not provide drag-and-drop functionality.</span></span> <span data-ttu-id="9772f-123">Los controles de posición pueden recibir el foco del mouse, pero no el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="9772f-123">Thumb controls can receive mouse focus but not keyboard focus.</span></span> <span data-ttu-id="9772f-124">El desarrollador del control debe implementar el control para que actúe correctamente (se pueda arrastrar o cambiar de tamaño).</span><span class="sxs-lookup"><span data-stu-id="9772f-124">The control developer must implement the control so that it acts appropriately (can be dragged or resized).</span></span>

<span data-ttu-id="9772f-125">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="9772f-125">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Thumb** control type.</span></span> <span data-ttu-id="9772f-126">Los requisitos de automatización de la interfaz de usuario aplican todos los controles Thumb en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control.</span><span class="sxs-lookup"><span data-stu-id="9772f-126">The UI Automation requirements apply all thumb controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="9772f-127">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="9772f-127">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9772f-128">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="9772f-128">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="9772f-129">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="9772f-129">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="9772f-130">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="9772f-130">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="9772f-131">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="9772f-131">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="9772f-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9772f-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="9772f-133">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="9772f-133">Typical Tree Structure</span></span>

<span data-ttu-id="9772f-134">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de posición y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="9772f-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to thumb controls and describes what can be contained in each view.</span></span> <span data-ttu-id="9772f-135">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9772f-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9772f-136">Vista de control</span><span class="sxs-lookup"><span data-stu-id="9772f-136">Control View</span></span></th>
<th><span data-ttu-id="9772f-137">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="9772f-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9772f-138">Thumb</span><span class="sxs-lookup"><span data-stu-id="9772f-138">Thumb</span></span></li>
</ul></td>
<td><span data-ttu-id="9772f-139">(No aplicable)</span><span class="sxs-lookup"><span data-stu-id="9772f-139">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9772f-140">Los controles de posición nunca aparecen en la vista de contenido porque solo existen para ser manipulados con un mouse.</span><span class="sxs-lookup"><span data-stu-id="9772f-140">Thumb controls never appear in the content view because they exist only to be manipulated with a mouse.</span></span> <span data-ttu-id="9772f-141">Se exponen a través de otro patrón de control, como el patrón de control [Scroll](uiauto-implementingscroll.md) , el patrón de control [Transform](uiauto-implementingtransform.md) o el patrón de control [RangeValue](uiauto-implementingrangevalue.md) , que se admite en el contenedor del control Thumb.</span><span class="sxs-lookup"><span data-stu-id="9772f-141">They are exposed though another control pattern, such as the [Scroll](uiauto-implementingscroll.md) control pattern, [Transform](uiauto-implementingtransform.md) control pattern, or [RangeValue](uiauto-implementingrangevalue.md) control pattern, being supported on the thumb control's container.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="9772f-142">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="9772f-142">Relevant Properties</span></span>

<span data-ttu-id="9772f-143">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles Thumb.</span><span class="sxs-lookup"><span data-stu-id="9772f-143">The following table lists the UI Automation properties whose value or definition is especially relevant to thumb controls.</span></span> <span data-ttu-id="9772f-144">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="9772f-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="9772f-145">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="9772f-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="9772f-146">Value</span><span class="sxs-lookup"><span data-stu-id="9772f-146">Value</span></span>      | <span data-ttu-id="9772f-147">Notas</span><span class="sxs-lookup"><span data-stu-id="9772f-147">Notes</span></span>                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9772f-148">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9772f-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="9772f-149">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="9772f-149">See notes.</span></span> | <span data-ttu-id="9772f-150">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9772f-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="9772f-151">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9772f-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="9772f-152">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="9772f-152">See notes.</span></span> | <span data-ttu-id="9772f-153">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="9772f-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="9772f-154">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9772f-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="9772f-155">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="9772f-155">See notes.</span></span> | <span data-ttu-id="9772f-156">Punto dentro del área de cliente visible del control Thumb.</span><span class="sxs-lookup"><span data-stu-id="9772f-156">A point within the visible client area of the thumb control.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="9772f-157">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9772f-157">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9772f-158">**Útil**</span><span class="sxs-lookup"><span data-stu-id="9772f-158">**Thumb**</span></span>  |                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="9772f-159">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9772f-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9772f-160">false</span><span class="sxs-lookup"><span data-stu-id="9772f-160">FALSE</span></span>      | <span data-ttu-id="9772f-161">El control Thumb nunca se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9772f-161">The thumb control is never included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="9772f-162">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9772f-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9772f-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="9772f-163">TRUE</span></span>       | <span data-ttu-id="9772f-164">El control Thumb siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9772f-164">The thumb control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="9772f-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9772f-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="9772f-166">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="9772f-166">See notes.</span></span> | <span data-ttu-id="9772f-167">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9772f-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="9772f-168">Un control Thumb puede recibir el foco si se usa como un objeto de "agarrador" para ajustar el tamaño de una ventana o un panel.</span><span class="sxs-lookup"><span data-stu-id="9772f-168">A thumb control can receive the focus if it is used as a "gripper" object for sizing a window or a pane.</span></span> <span data-ttu-id="9772f-169">Un control Thumb en un control deslizante o en una barra de desplazamiento nunca debe recibir el foco.</span><span class="sxs-lookup"><span data-stu-id="9772f-169">A thumb control in a slider or scroll bar should never receive the focus.</span></span> |
| [<span data-ttu-id="9772f-170">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9772f-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="9772f-171">NULL</span><span class="sxs-lookup"><span data-stu-id="9772f-171">NULL</span></span>       | <span data-ttu-id="9772f-172">Los controles Thumb nunca tienen una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="9772f-172">Thumb controls never have a label.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="9772f-173">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9772f-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="9772f-174">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="9772f-174">See notes.</span></span> | <span data-ttu-id="9772f-175">Cadena localizada que corresponde al tipo de control **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="9772f-175">Localized string corresponding to the **Thumb** control type.</span></span> <span data-ttu-id="9772f-176">El valor predeterminado es "Thumb" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="9772f-176">The default value is "thumb" for en-US or English (United States).</span></span>                                                                                                                             |
| [<span data-ttu-id="9772f-177">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9772f-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="9772f-178">NULL</span><span class="sxs-lookup"><span data-stu-id="9772f-178">NULL</span></span>       | <span data-ttu-id="9772f-179">Dado que el control Thumb no está disponible en la vista de contenido del árbol de automatización de la interfaz de usuario, no requiere un nombre.</span><span class="sxs-lookup"><span data-stu-id="9772f-179">Because the thumb control is not available in the content view of the UI Automation tree, it does not require a name.</span></span>                                                                                                                                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="9772f-180">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="9772f-180">Required Control Patterns</span></span>

<span data-ttu-id="9772f-181">En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que deben admitir los controles Thumb.</span><span class="sxs-lookup"><span data-stu-id="9772f-181">The following table lists the UI Automation control patterns required to be supported by thumb controls.</span></span> <span data-ttu-id="9772f-182">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9772f-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="9772f-183">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="9772f-183">Control Pattern</span></span>                                         | <span data-ttu-id="9772f-184">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9772f-184">Support</span></span>  | <span data-ttu-id="9772f-185">Notas</span><span class="sxs-lookup"><span data-stu-id="9772f-185">Notes</span></span>                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9772f-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="9772f-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="9772f-187">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9772f-187">Required</span></span> | <span data-ttu-id="9772f-188">Permite que el control de posición se mueva por la pantalla.</span><span class="sxs-lookup"><span data-stu-id="9772f-188">Enables the thumb control to be moved on the screen.</span></span> <span data-ttu-id="9772f-189">Dado que normalmente no se puede cambiar el tamaño del control Thumb o girarlo, el patrón de control [Transform](uiauto-implementingtransform.md) admite principalmente la función [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) .</span><span class="sxs-lookup"><span data-stu-id="9772f-189">Because the thumb control typically cannot be resized or rotated, the [Transform](uiauto-implementingtransform.md) control pattern primarily supports the [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) function.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="9772f-190">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="9772f-190">Required Events</span></span>

<span data-ttu-id="9772f-191">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles Thumb deben admitir.</span><span class="sxs-lookup"><span data-stu-id="9772f-191">The following table lists the UI Automation events that thumb controls are required to support.</span></span> <span data-ttu-id="9772f-192">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9772f-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="9772f-193">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="9772f-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="9772f-194">Notas</span><span class="sxs-lookup"><span data-stu-id="9772f-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9772f-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="9772f-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="9772f-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="9772f-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="9772f-197">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="9772f-197">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="9772f-198">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="9772f-198">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="9772f-199">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="9772f-199">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="9772f-200">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="9772f-200">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="9772f-201">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="9772f-201">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="9772f-202">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9772f-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9772f-203">**Vista**</span><span class="sxs-lookup"><span data-stu-id="9772f-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9772f-204">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="9772f-204">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="9772f-205">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="9772f-205">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




