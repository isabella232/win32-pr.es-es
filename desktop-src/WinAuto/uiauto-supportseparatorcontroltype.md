---
title: Separator (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control separator.
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control separator
- UI Automation, separator (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control separator
- Automatización de la interfaz de usuario, propiedades para el tipo de control separator
- Automatización de la interfaz de usuario, patrones de control para el tipo de control separator
- Automatización de la interfaz de usuario, eventos para el tipo de control separator
- estructuras de árbol, tipo de control separator
- Properties, separator (tipo de control)
- patrones de control, tipo de control separator
- Events, separator (tipo de control)
- compatibilidad con el tipo de control separator
- Separator (tipo de control)
- tipos de control, estructura de árbol para el tipo de control separator
- tipos de control, patrones de control para el tipo de control separator
- tipos de control, compatibilidad con separador
- tipos de control, separador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cdf6c15dbe461e78877c6b93f0ff4b52f67fc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532314"
---
# <a name="separator-control-type"></a><span data-ttu-id="38ea0-119">Separator (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="38ea0-119">Separator Control Type</span></span>

<span data-ttu-id="38ea0-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **separator** .</span><span class="sxs-lookup"><span data-stu-id="38ea0-120">This topic provides information about Microsoft UI Automation support for the **Separator** control type.</span></span>

<span data-ttu-id="38ea0-121">Los controles de separador se usan para dividir visualmente un espacio en dos regiones.</span><span class="sxs-lookup"><span data-stu-id="38ea0-121">Separator controls are used to visually divide a space into two regions.</span></span> <span data-ttu-id="38ea0-122">Por ejemplo, un control de separador puede ser una barra que defina dos paneles en una ventana.</span><span class="sxs-lookup"><span data-stu-id="38ea0-122">For example, a separator control can be a bar that defines two panes in a window.</span></span> <span data-ttu-id="38ea0-123">Si se puede mover el separador, el control debe exponerse como Thumb en el tipo de control.</span><span class="sxs-lookup"><span data-stu-id="38ea0-123">If the separator can be moved, the control should be exposed as Thumb in control type.</span></span>

<span data-ttu-id="38ea0-124">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **separator** .</span><span class="sxs-lookup"><span data-stu-id="38ea0-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Separator** control type.</span></span> <span data-ttu-id="38ea0-125">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de separador donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control</span><span class="sxs-lookup"><span data-stu-id="38ea0-125">The UI Automation requirements apply to all separator controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="38ea0-126">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="38ea0-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="38ea0-127">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="38ea0-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="38ea0-128">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="38ea0-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="38ea0-129">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="38ea0-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="38ea0-130">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="38ea0-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="38ea0-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38ea0-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="38ea0-132">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="38ea0-132">Typical Tree Structure</span></span>

<span data-ttu-id="38ea0-133">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de separador y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="38ea0-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to separator controls and describes what can be contained in each view.</span></span> <span data-ttu-id="38ea0-134">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="38ea0-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="38ea0-135">Vista de control</span><span class="sxs-lookup"><span data-stu-id="38ea0-135">Control View</span></span></th>
<th><span data-ttu-id="38ea0-136">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="38ea0-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="38ea0-137">Separador</span><span class="sxs-lookup"><span data-stu-id="38ea0-137">Separator</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="38ea0-138">El tipo de control <strong>separator</strong> nunca tiene contenido.</span><span class="sxs-lookup"><span data-stu-id="38ea0-138">The <strong>Separator</strong> control type never has content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="38ea0-139">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="38ea0-139">Relevant Properties</span></span>

<span data-ttu-id="38ea0-140">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de separador.</span><span class="sxs-lookup"><span data-stu-id="38ea0-140">The following table lists the UI Automation properties whose value or definition is especially relevant to separator controls.</span></span> <span data-ttu-id="38ea0-141">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="38ea0-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="38ea0-142">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="38ea0-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="38ea0-143">Value</span><span class="sxs-lookup"><span data-stu-id="38ea0-143">Value</span></span>         | <span data-ttu-id="38ea0-144">Notas</span><span class="sxs-lookup"><span data-stu-id="38ea0-144">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38ea0-145">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="38ea0-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="38ea0-146">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="38ea0-146">See notes.</span></span>    | <span data-ttu-id="38ea0-147">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="38ea0-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="38ea0-148">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="38ea0-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="38ea0-149">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="38ea0-149">See notes.</span></span>    | <span data-ttu-id="38ea0-150">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="38ea0-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="38ea0-151">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="38ea0-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="38ea0-152">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="38ea0-152">See notes.</span></span>    | <span data-ttu-id="38ea0-153">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="38ea0-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="38ea0-154">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="38ea0-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="38ea0-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="38ea0-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="38ea0-156">**Separador**</span><span class="sxs-lookup"><span data-stu-id="38ea0-156">**Separator**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="38ea0-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="38ea0-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="38ea0-158">false</span><span class="sxs-lookup"><span data-stu-id="38ea0-158">FALSE</span></span>         | <span data-ttu-id="38ea0-159">El control Separator nunca es contenido.</span><span class="sxs-lookup"><span data-stu-id="38ea0-159">The separator control is never content.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="38ea0-160">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="38ea0-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="38ea0-161">TRUE</span><span class="sxs-lookup"><span data-stu-id="38ea0-161">TRUE</span></span>          | <span data-ttu-id="38ea0-162">El control de separador siempre debe ser un control.</span><span class="sxs-lookup"><span data-stu-id="38ea0-162">The separator control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="38ea0-163">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="38ea0-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="38ea0-164">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="38ea0-164">See notes.</span></span>    | <span data-ttu-id="38ea0-165">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="38ea0-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="38ea0-166">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="38ea0-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="38ea0-167">NULL</span><span class="sxs-lookup"><span data-stu-id="38ea0-167">NULL</span></span>          | <span data-ttu-id="38ea0-168">El control de separador no tiene una etiqueta estática.</span><span class="sxs-lookup"><span data-stu-id="38ea0-168">The separator control does not have a static label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="38ea0-169">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="38ea0-169">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="38ea0-170">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="38ea0-170">See notes.</span></span>    | <span data-ttu-id="38ea0-171">Cadena localizada que corresponde al tipo de control **separator** .</span><span class="sxs-lookup"><span data-stu-id="38ea0-171">Localized string corresponding to the **Separator** control type.</span></span> <span data-ttu-id="38ea0-172">El valor predeterminado es "separator" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="38ea0-172">The default value is "Separator" for en-US or English (United States).</span></span>                                                             |
| [<span data-ttu-id="38ea0-173">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="38ea0-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="38ea0-174">""</span><span class="sxs-lookup"><span data-stu-id="38ea0-174">""</span></span>            | <span data-ttu-id="38ea0-175">El control de separador no requiere una propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="38ea0-175">The separator control does not require a **Name** property.</span></span>                                                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="38ea0-176">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="38ea0-176">Required Control Patterns</span></span>

<span data-ttu-id="38ea0-177">El control de separador no debe admitir ningún patrón de control.</span><span class="sxs-lookup"><span data-stu-id="38ea0-177">The separator control is not required to support any control patterns.</span></span> <span data-ttu-id="38ea0-178">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="38ea0-178">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

## <a name="required-events"></a><span data-ttu-id="38ea0-179">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="38ea0-179">Required Events</span></span>

<span data-ttu-id="38ea0-180">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de separador deben admitir.</span><span class="sxs-lookup"><span data-stu-id="38ea0-180">The following table lists the UI Automation events that separator controls are required to support.</span></span> <span data-ttu-id="38ea0-181">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="38ea0-181">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="38ea0-182">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="38ea0-182">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="38ea0-183">Notas</span><span class="sxs-lookup"><span data-stu-id="38ea0-183">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38ea0-184">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="38ea0-184">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="38ea0-185">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="38ea0-185">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="38ea0-186">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="38ea0-186">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="38ea0-187">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="38ea0-187">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="38ea0-188">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="38ea0-188">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="38ea0-189">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="38ea0-189">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="38ea0-190">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="38ea0-190">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="38ea0-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38ea0-191">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="38ea0-192">**Vista**</span><span class="sxs-lookup"><span data-stu-id="38ea0-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="38ea0-193">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="38ea0-193">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="38ea0-194">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="38ea0-194">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




