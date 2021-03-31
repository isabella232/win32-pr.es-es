---
title: Header (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control header.
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control header
- Automatización de la interfaz de usuario, tipo de control header
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control header
- Automatización de la interfaz de usuario, propiedades para el tipo de control header
- Automatización de la interfaz de usuario, patrones de control para el tipo de control header
- Automatización de la interfaz de usuario, eventos para el tipo de control header
- estructuras de árbol, tipo de control header
- Properties, header (tipo de control)
- patrones de control, tipo de control header
- Events, header (tipo de control)
- compatibilidad con el tipo de control header
- Header (tipo de control)
- tipos de control, estructura de árbol para el tipo de control header
- tipos de control, patrones de control para el tipo de control header
- tipos de control, compatibilidad con el encabezado
- tipos de control, encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38ee0a00749888c624b627db247f2d01d24ff1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418637"
---
# <a name="header-control-type"></a><span data-ttu-id="299f4-119">Header (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="299f4-119">Header Control Type</span></span>

<span data-ttu-id="299f4-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Header** .</span><span class="sxs-lookup"><span data-stu-id="299f4-120">This topic provides information about Microsoft UI Automation support for the **Header** control type.</span></span>

<span data-ttu-id="299f4-121">El control de encabezado proporciona un contenedor visual para las etiquetas de filas o columnas de información.</span><span class="sxs-lookup"><span data-stu-id="299f4-121">The header control provides a visual container for the labels for rows or columns of information.</span></span>

<span data-ttu-id="299f4-122">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Header** .</span><span class="sxs-lookup"><span data-stu-id="299f4-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Header** control type.</span></span> <span data-ttu-id="299f4-123">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de encabezado donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control</span><span class="sxs-lookup"><span data-stu-id="299f4-123">The UI Automation requirements apply to all header controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="299f4-124">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="299f4-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="299f4-125">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="299f4-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="299f4-126">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="299f4-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="299f4-127">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="299f4-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="299f4-128">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="299f4-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="299f4-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="299f4-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="299f4-130">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="299f4-130">Typical Tree Structure</span></span>

<span data-ttu-id="299f4-131">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de encabezado y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="299f4-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header controls and describes what can be contained in each view.</span></span> <span data-ttu-id="299f4-132">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="299f4-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="299f4-133">Vista de control</span><span class="sxs-lookup"><span data-stu-id="299f4-133">Control View</span></span></th>
<th><span data-ttu-id="299f4-134">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="299f4-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="299f4-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="299f4-135">Header</span></span>
<ul>
<li><span data-ttu-id="299f4-136">HeaderItem (1 o más)</span><span class="sxs-lookup"><span data-stu-id="299f4-136">HeaderItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="299f4-137">(No aplicable)</span><span class="sxs-lookup"><span data-stu-id="299f4-137">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="299f4-138">Los controles de encabezado siempre tienen uno o más elementos secundarios en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="299f4-138">Header controls always have one or more children in the control view of the UI Automation tree.</span></span>

<span data-ttu-id="299f4-139">Los controles de encabezado tienen cero elementos secundarios en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="299f4-139">Header controls have zero children in the content view of the UI Automation tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="299f4-140">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="299f4-140">Relevant Properties</span></span>

<span data-ttu-id="299f4-141">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de encabezado.</span><span class="sxs-lookup"><span data-stu-id="299f4-141">The following table lists the UI Automation properties whose value or definition is especially relevant to header controls.</span></span> <span data-ttu-id="299f4-142">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="299f4-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="299f4-143">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="299f4-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="299f4-144">Value</span><span class="sxs-lookup"><span data-stu-id="299f4-144">Value</span></span>                                                            | <span data-ttu-id="299f4-145">Notas</span><span class="sxs-lookup"><span data-stu-id="299f4-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="299f4-146">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="299f4-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="299f4-147">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="299f4-147">See notes.</span></span>                                                       | <span data-ttu-id="299f4-148">El valor de esta propiedad debe ser único en todos los controles de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="299f4-148">The value of this property must be unique across all controls in an application.</span></span>                                                                                                                     |
| [<span data-ttu-id="299f4-149">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="299f4-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="299f4-150">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="299f4-150">See notes.</span></span>                                                       | <span data-ttu-id="299f4-151">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="299f4-151">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="299f4-152">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="299f4-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="299f4-153">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="299f4-153">See notes.</span></span>                                                       | <span data-ttu-id="299f4-154">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="299f4-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="299f4-155">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="299f4-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="299f4-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="299f4-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="299f4-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="299f4-157">**Header**</span></span>                                                       |                                                                                                                                                                                                      |
| [<span data-ttu-id="299f4-158">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="299f4-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="299f4-159">false</span><span class="sxs-lookup"><span data-stu-id="299f4-159">FALSE</span></span>                                                            | <span data-ttu-id="299f4-160">El control de encabezado no se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="299f4-160">The header control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                    |
| [<span data-ttu-id="299f4-161">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="299f4-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="299f4-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="299f4-162">TRUE</span></span>                                                             | <span data-ttu-id="299f4-163">El control de encabezado siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="299f4-163">The header control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                 |
| [<span data-ttu-id="299f4-164">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="299f4-164">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="299f4-165">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="299f4-165">See notes.</span></span>                                                       | <span data-ttu-id="299f4-166">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="299f4-166">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="299f4-167">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="299f4-167">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="299f4-168">NULL</span><span class="sxs-lookup"><span data-stu-id="299f4-168">NULL</span></span>                                                             | <span data-ttu-id="299f4-169">Los controles de encabezado no tienen una etiqueta estática.</span><span class="sxs-lookup"><span data-stu-id="299f4-169">Header controls do not have a static label.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="299f4-170">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="299f4-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="299f4-171">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="299f4-171">See notes.</span></span>                                                       | <span data-ttu-id="299f4-172">El valor predeterminado es "header" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="299f4-172">The default value is "header" for en-US or English (United States).</span></span>                                                                                                                                  |
| [<span data-ttu-id="299f4-173">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="299f4-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="299f4-174">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="299f4-174">See notes.</span></span>                                                       | <span data-ttu-id="299f4-175">El control de encabezado necesita un nombre si hay más de un encabezado de fila o más de un encabezado de columna.</span><span class="sxs-lookup"><span data-stu-id="299f4-175">The header control needs a name if there is more than one row header or more than one column header.</span></span> <span data-ttu-id="299f4-176">Esto identifica la información dentro del encabezado.</span><span class="sxs-lookup"><span data-stu-id="299f4-176">This identifies the information within the header.</span></span>                                              |
| [<span data-ttu-id="299f4-177">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="299f4-177">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="299f4-178">**OrientationType \_ Horizontal** o **OrientationType \_ vertical**</span><span class="sxs-lookup"><span data-stu-id="299f4-178">**OrientationType\_Horizontal** or **OrientationType\_Vertical**</span></span> | <span data-ttu-id="299f4-179">El valor de esta propiedad expone la posición del control de encabezado, ya sea un encabezado de fila (**OrientationType \_ horizontal**) o un encabezado de columna (**OrientationType \_ vertical**).</span><span class="sxs-lookup"><span data-stu-id="299f4-179">The value of this property exposes the position of the header control—whether it is a row header (**OrientationType\_Horizontal**) or column header (**OrientationType\_Vertical**).</span></span>                 |



 

## <a name="required-control-patterns"></a><span data-ttu-id="299f4-180">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="299f4-180">Required Control Patterns</span></span>

<span data-ttu-id="299f4-181">En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que se deben admitir para los controles de encabezado.</span><span class="sxs-lookup"><span data-stu-id="299f4-181">The following table lists the UI Automation control patterns required to be supported for header controls.</span></span> <span data-ttu-id="299f4-182">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="299f4-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="299f4-183">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="299f4-183">Control Pattern</span></span>                                         | <span data-ttu-id="299f4-184">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="299f4-184">Support</span></span> | <span data-ttu-id="299f4-185">Notas</span><span class="sxs-lookup"><span data-stu-id="299f4-185">Notes</span></span>                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="299f4-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="299f4-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="299f4-187">Depende</span><span class="sxs-lookup"><span data-stu-id="299f4-187">Depends</span></span> | <span data-ttu-id="299f4-188">Implemente el patrón de control [Transform](uiauto-implementingtransform.md) si se puede cambiar el tamaño del control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="299f4-188">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header control can be resized.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="299f4-189">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="299f4-189">Required Events</span></span>

<span data-ttu-id="299f4-190">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que deben admitir los controles de encabezado.</span><span class="sxs-lookup"><span data-stu-id="299f4-190">The following table lists the UI Automation events that header controls are required to support.</span></span> <span data-ttu-id="299f4-191">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="299f4-191">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="299f4-192">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="299f4-192">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="299f4-193">Notas</span><span class="sxs-lookup"><span data-stu-id="299f4-193">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="299f4-194">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="299f4-194">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="299f4-195">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="299f4-195">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="299f4-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="299f4-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="299f4-197">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="299f4-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="299f4-198">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="299f4-198">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="299f4-199">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="299f4-199">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="299f4-200">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="299f4-200">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="299f4-201">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="299f4-201">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="299f4-202">**Vista**</span><span class="sxs-lookup"><span data-stu-id="299f4-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="299f4-203">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="299f4-203">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="299f4-204">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="299f4-204">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




