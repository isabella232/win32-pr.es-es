---
title: HeaderItem (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control HeaderItem.
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control HeaderItem
- Automatización de la interfaz de usuario, tipo de control HeaderItem
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control HeaderItem
- Automatización de la interfaz de usuario, propiedades para el tipo de control HeaderItem
- Automatización de la interfaz de usuario, patrones de control para el tipo de control HeaderItem
- Automatización de la interfaz de usuario, eventos para el tipo de control HeaderItem
- estructuras de árbol, tipo de control HeaderItem
- propiedades, HeaderItem (tipo de control)
- patrones de control, HeaderItem (tipo de control)
- Events, HeaderItem (tipo de control)
- compatibilidad con el tipo de control HeaderItem
- HeaderItem (tipo de control)
- tipos de control, estructura de árbol para el tipo de control HeaderItem
- tipos de control, patrones de control para el tipo de control HeaderItem
- tipos de control, compatibilidad con HeaderItem
- tipos de control, HeaderItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bab61f92a6ab4db221810f9f083279ade4bf353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704639"
---
# <a name="headeritem-control-type"></a><span data-ttu-id="04186-119">HeaderItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="04186-119">HeaderItem Control Type</span></span>

<span data-ttu-id="04186-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="04186-120">This topic provides information about Microsoft UI Automation support for the **HeaderItem** control type.</span></span>

<span data-ttu-id="04186-121">El tipo de control **HeaderItem** proporciona una etiqueta visual para una fila o columna de información.</span><span class="sxs-lookup"><span data-stu-id="04186-121">The **HeaderItem** control type provides a visual label for a row or column of information.</span></span>

<span data-ttu-id="04186-122">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="04186-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **HeaderItem** control type.</span></span> <span data-ttu-id="04186-123">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de elemento de encabezado donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control</span><span class="sxs-lookup"><span data-stu-id="04186-123">The UI Automation requirements apply to all header item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="04186-124">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="04186-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="04186-125">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="04186-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="04186-126">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="04186-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="04186-127">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="04186-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="04186-128">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="04186-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="04186-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04186-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="04186-130">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="04186-130">Typical Tree Structure</span></span>

<span data-ttu-id="04186-131">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de elemento de encabezado y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="04186-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="04186-132">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="04186-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04186-133">Vista de control</span><span class="sxs-lookup"><span data-stu-id="04186-133">Control View</span></span></th>
<th><span data-ttu-id="04186-134">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="04186-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="04186-135">HeaderItem</span><span class="sxs-lookup"><span data-stu-id="04186-135">HeaderItem</span></span></li>
</ul></td>
<td><span data-ttu-id="04186-136">(No aplicable)</span><span class="sxs-lookup"><span data-stu-id="04186-136">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="04186-137">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="04186-137">Relevant Properties</span></span>

<span data-ttu-id="04186-138">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="04186-138">The following table lists the UI Automation properties whose value or definition is especially relevant to the **HeaderItem** control type.</span></span> <span data-ttu-id="04186-139">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="04186-139">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="04186-140">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="04186-140">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="04186-141">Value</span><span class="sxs-lookup"><span data-stu-id="04186-141">Value</span></span>          | <span data-ttu-id="04186-142">Notas</span><span class="sxs-lookup"><span data-stu-id="04186-142">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04186-143">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="04186-143">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="04186-144">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="04186-144">See notes.</span></span>     | <span data-ttu-id="04186-145">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="04186-145">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="04186-146">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="04186-146">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="04186-147">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="04186-147">See notes.</span></span>     | <span data-ttu-id="04186-148">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="04186-148">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="04186-149">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="04186-149">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="04186-150">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="04186-150">See notes.</span></span>     | <span data-ttu-id="04186-151">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="04186-151">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="04186-152">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="04186-152">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="04186-153">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="04186-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="04186-154">**HeaderItem**</span><span class="sxs-lookup"><span data-stu-id="04186-154">**HeaderItem**</span></span> | <span data-ttu-id="04186-155">Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="04186-155">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="04186-156">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="04186-156">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="04186-157">false</span><span class="sxs-lookup"><span data-stu-id="04186-157">FALSE</span></span>          | <span data-ttu-id="04186-158">El control de elemento de encabezado no se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="04186-158">The header item control is not included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="04186-159">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="04186-159">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="04186-160">TRUE</span><span class="sxs-lookup"><span data-stu-id="04186-160">TRUE</span></span>           | <span data-ttu-id="04186-161">El control de elemento de encabezado siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="04186-161">The header item control is always included in the control view of the UI Automation tree.</span></span>                                                                                                            |
| [<span data-ttu-id="04186-162">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="04186-162">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="04186-163">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="04186-163">See notes.</span></span>     | <span data-ttu-id="04186-164">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="04186-164">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="04186-165">**UIA \_ ItemStatusPropertyId**</span><span class="sxs-lookup"><span data-stu-id="04186-165">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="04186-166">Vea las notas</span><span class="sxs-lookup"><span data-stu-id="04186-166">See notes</span></span>      | <span data-ttu-id="04186-167">Esta propiedad ofrece información para los criterios de ordenación mediante el elemento de encabezado.</span><span class="sxs-lookup"><span data-stu-id="04186-167">This property provides information for sort orders by the header item.</span></span>                                                                                                                               |
| [<span data-ttu-id="04186-168">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="04186-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="04186-169">NULL</span><span class="sxs-lookup"><span data-stu-id="04186-169">NULL</span></span>           | <span data-ttu-id="04186-170">Los controles de elemento de encabezado no tienen una etiqueta de texto estático.</span><span class="sxs-lookup"><span data-stu-id="04186-170">Header item controls do not have a static text label.</span></span>                                                                                                                                                |
| [<span data-ttu-id="04186-171">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="04186-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="04186-172">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="04186-172">See notes.</span></span>     | <span data-ttu-id="04186-173">Cadena localizada que corresponde al tipo de control **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="04186-173">Localized string corresponding to the **HeaderItem** control type.</span></span> <span data-ttu-id="04186-174">El valor predeterminado es "header Item" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="04186-174">The default value is "header item" for en-US or English (United States).</span></span>                                                          |
| [<span data-ttu-id="04186-175">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="04186-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="04186-176">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="04186-176">See notes.</span></span>     | <span data-ttu-id="04186-177">El control de elemento de encabezado siempre se etiqueta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="04186-177">The header item control is always self-labeling.</span></span>                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="04186-178">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="04186-178">Required Control Patterns</span></span>

<span data-ttu-id="04186-179">En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de elemento de encabezado.</span><span class="sxs-lookup"><span data-stu-id="04186-179">The following table lists the UI Automation control patterns required to be supported by all header item controls.</span></span> <span data-ttu-id="04186-180">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="04186-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="04186-181">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="04186-181">Control Pattern</span></span>                                         | <span data-ttu-id="04186-182">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="04186-182">Support</span></span> | <span data-ttu-id="04186-183">Notas</span><span class="sxs-lookup"><span data-stu-id="04186-183">Notes</span></span>                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04186-184">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="04186-184">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | <span data-ttu-id="04186-185">Depende</span><span class="sxs-lookup"><span data-stu-id="04186-185">Depends</span></span> | <span data-ttu-id="04186-186">Implemente el patrón de control [Invoke](uiauto-implementinginvoke.md) si se puede hacer clic en el control de elemento de encabezado para ordenar los datos.</span><span class="sxs-lookup"><span data-stu-id="04186-186">Implement the [Invoke](uiauto-implementinginvoke.md) control pattern if the header item control can be clicked to sort the data.</span></span> |
| [<span data-ttu-id="04186-187">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="04186-187">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="04186-188">Depende</span><span class="sxs-lookup"><span data-stu-id="04186-188">Depends</span></span> | <span data-ttu-id="04186-189">Implemente el patrón de control [Transform](uiauto-implementingtransform.md) si se puede cambiar el tamaño del control de elemento de encabezado.</span><span class="sxs-lookup"><span data-stu-id="04186-189">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header item control can be resized.</span></span>            |



 

## <a name="required-events"></a><span data-ttu-id="04186-190">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="04186-190">Required Events</span></span>

<span data-ttu-id="04186-191">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de elemento de encabezado son necesarios para admitir.</span><span class="sxs-lookup"><span data-stu-id="04186-191">The following table lists the UI Automation events that header item controls are required to support.</span></span> <span data-ttu-id="04186-192">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="04186-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="04186-193">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="04186-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="04186-194">Notas</span><span class="sxs-lookup"><span data-stu-id="04186-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04186-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="04186-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="04186-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="04186-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="04186-197">**\_InvokedEventId de invocación de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="04186-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="04186-198">Si el control admite el patrón de control [Invoke](uiauto-implementinginvoke.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="04186-198">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="04186-199">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="04186-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="04186-200">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="04186-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="04186-201">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="04186-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="04186-202">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="04186-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="04186-203">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="04186-203">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="04186-204">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04186-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="04186-205">**Vista**</span><span class="sxs-lookup"><span data-stu-id="04186-205">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="04186-206">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="04186-206">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="04186-207">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="04186-207">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




