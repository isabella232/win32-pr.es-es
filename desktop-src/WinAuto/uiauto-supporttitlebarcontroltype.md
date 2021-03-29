---
title: TitleBar (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control TitleBar. Un control de barra de título representa el título o la barra de título de una ventana.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control TitleBar
- UI Automation, TitleBar (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control TitleBar
- Automatización de la interfaz de usuario, propiedades para el tipo de control TitleBar
- Automatización de la interfaz de usuario, patrones de control para el tipo de control TitleBar
- Automatización de la interfaz de usuario, eventos para el tipo de control TitleBar
- estructuras de árbol, tipo de control TitleBar
- Properties, TitleBar (tipo de control)
- patrones de control, TitleBar (tipo de control)
- Events, TitleBar (tipo de control)
- compatibilidad con el tipo de control TitleBar
- TitleBar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control TitleBar
- tipos de control, patrones de control para el tipo de control TitleBar
- tipos de control, compatibilidad con TitleBar
- tipos de control, TitleBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9471d08479345bf8c1df118f720bf273d4d89d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994556"
---
# <a name="titlebar-control-type"></a><span data-ttu-id="e5ea8-120">TitleBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="e5ea8-120">TitleBar Control Type</span></span>

<span data-ttu-id="e5ea8-121">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **TitleBar** .</span><span class="sxs-lookup"><span data-stu-id="e5ea8-121">This topic provides information about Microsoft UI Automation support for the **TitleBar** control type.</span></span> <span data-ttu-id="e5ea8-122">Un control de barra de título representa el título o la barra de título de una ventana.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-122">A title bar control represents a title or caption bar in a window.</span></span>

<span data-ttu-id="e5ea8-123">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario necesaria, las propiedades, los patrones de control y los eventos para el tipo de control **TitleBar** .</span><span class="sxs-lookup"><span data-stu-id="e5ea8-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TitleBar** control type.</span></span> <span data-ttu-id="e5ea8-124">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de barra de título donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control</span><span class="sxs-lookup"><span data-stu-id="e5ea8-124">The UI Automation requirements apply to all title bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="e5ea8-125">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e5ea8-126">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="e5ea8-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="e5ea8-127">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="e5ea8-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="e5ea8-128">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="e5ea8-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="e5ea8-129">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="e5ea8-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="e5ea8-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5ea8-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="e5ea8-131">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="e5ea8-131">Typical Tree Structure</span></span>

<span data-ttu-id="e5ea8-132">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de barra de título y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to title bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="e5ea8-133">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e5ea8-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5ea8-134">Vista de control</span><span class="sxs-lookup"><span data-stu-id="e5ea8-134">Control View</span></span></th>
<th><span data-ttu-id="e5ea8-135">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="e5ea8-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e5ea8-136">TitleBar</span><span class="sxs-lookup"><span data-stu-id="e5ea8-136">TitleBar</span></span>
<ul>
<li><span data-ttu-id="e5ea8-137">Menú (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="e5ea8-137">Menu (0 or 1)</span></span></li>
<li><span data-ttu-id="e5ea8-138">Botón (0 o más)</span><span class="sxs-lookup"><span data-stu-id="e5ea8-138">Button (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="e5ea8-139">(No es aplicable; el control de barra de título no tiene contenido)</span><span class="sxs-lookup"><span data-stu-id="e5ea8-139">(Not applicable; the title bar control has no content)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="e5ea8-140">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="e5ea8-140">Relevant Properties</span></span>

<span data-ttu-id="e5ea8-141">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **TitleBar** .</span><span class="sxs-lookup"><span data-stu-id="e5ea8-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TitleBar** control type.</span></span> <span data-ttu-id="e5ea8-142">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="e5ea8-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="e5ea8-143">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="e5ea8-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="e5ea8-144">Value</span><span class="sxs-lookup"><span data-stu-id="e5ea8-144">Value</span></span>        | <span data-ttu-id="e5ea8-145">Notas</span><span class="sxs-lookup"><span data-stu-id="e5ea8-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5ea8-146">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="e5ea8-147">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-147">See notes.</span></span>   | <span data-ttu-id="e5ea8-148">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="e5ea8-149">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="e5ea8-150">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-150">See notes.</span></span>   | <span data-ttu-id="e5ea8-151">El valor que expone esta propiedad debe incluir todos los controles que se contienen dentro de ella.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-151">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                             |
| [<span data-ttu-id="e5ea8-152">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="e5ea8-153">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-153">See notes.</span></span>   | <span data-ttu-id="e5ea8-154">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="e5ea8-155">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="e5ea8-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="e5ea8-157">**TitleBar**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-157">**TitleBar**</span></span> | <span data-ttu-id="e5ea8-158">Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-158">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="e5ea8-159">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="e5ea8-160">false</span><span class="sxs-lookup"><span data-stu-id="e5ea8-160">FALSE</span></span>        | <span data-ttu-id="e5ea8-161">El control de barra de título nunca se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-161">The title bar control is never included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="e5ea8-162">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="e5ea8-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="e5ea8-163">TRUE</span></span>         | <span data-ttu-id="e5ea8-164">El control de barra de título siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-164">The title bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                              |
| [<span data-ttu-id="e5ea8-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="e5ea8-166">false</span><span class="sxs-lookup"><span data-stu-id="e5ea8-166">FALSE</span></span>        | <span data-ttu-id="e5ea8-167">Un control de barra de título nunca tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-167">A title bar control never has keyboard focus.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="e5ea8-168">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-168">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="e5ea8-169">Depende</span><span class="sxs-lookup"><span data-stu-id="e5ea8-169">Depends</span></span>      | <span data-ttu-id="e5ea8-170">Un control de barra de título devuelve un valor dependiendo de si está visible en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-170">A title bar control returns a value depending on whether it is visible on the screen.</span></span>                                                                                                                |
| [<span data-ttu-id="e5ea8-171">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="e5ea8-172">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-172">See notes.</span></span>   | <span data-ttu-id="e5ea8-173">Normalmente, un control de barra de título no tiene una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-173">A title bar control typically does not have a label.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="e5ea8-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="e5ea8-175">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-175">See notes.</span></span>   | <span data-ttu-id="e5ea8-176">Cadena localizada que corresponde al tipo de control TitleBar.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-176">Localized string corresponding to the TitleBar control type.</span></span> <span data-ttu-id="e5ea8-177">El valor predeterminado es "barra de título" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="e5ea8-177">The default value is "title bar" for en-US or English (United States).</span></span>                                                                  |
| [<span data-ttu-id="e5ea8-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="e5ea8-179">""</span><span class="sxs-lookup"><span data-stu-id="e5ea8-179">""</span></span>           | <span data-ttu-id="e5ea8-180">Una barra de título no es contenido; su información de texto se expone mediante el nombre de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-180">A title bar is not content; its textual information is exposed by the name of the parent window.</span></span>                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="e5ea8-181">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="e5ea8-181">Required Control Patterns</span></span>

<span data-ttu-id="e5ea8-182">No es necesario que el tipo de control **TitleBar** admita ningún patrón de control.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-182">The **TitleBar** control type is not required to support any control patterns.</span></span> <span data-ttu-id="e5ea8-183">Su funcionalidad se expone a través del patrón de control [Window](uiauto-implementingwindow.md) en el tipo de control [Window](uiauto-supportwindowcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="e5ea8-183">Its functionality is exposed through the [Window](uiauto-implementingwindow.md) control pattern on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="e5ea8-184">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="e5ea8-184">Required Events</span></span>

<span data-ttu-id="e5ea8-185">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de barra de título deben admitir.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-185">The following table lists the UI Automation events that title bar controls are required to support.</span></span> <span data-ttu-id="e5ea8-186">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e5ea8-186">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="e5ea8-187">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="e5ea8-187">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="e5ea8-188">Notas</span><span class="sxs-lookup"><span data-stu-id="e5ea8-188">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5ea8-189">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-189">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="e5ea8-190">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-190">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="e5ea8-191">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-191">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="e5ea8-192">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-192">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="e5ea8-193">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-193">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="e5ea8-194">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="e5ea8-194">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="e5ea8-195">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-195">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="e5ea8-196">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5ea8-196">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e5ea8-197">**Vista**</span><span class="sxs-lookup"><span data-stu-id="e5ea8-197">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e5ea8-198">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="e5ea8-198">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="e5ea8-199">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="e5ea8-199">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




