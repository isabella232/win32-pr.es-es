---
title: StatusBar (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control StatusBar.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control StatusBar
- Automatización de la interfaz de usuario, tipo de control StatusBar
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control StatusBar
- Automatización de la interfaz de usuario, propiedades para el tipo de control StatusBar
- Automatización de la interfaz de usuario, patrones de control para el tipo de control StatusBar
- Automatización de la interfaz de usuario, eventos para el tipo de control StatusBar
- estructuras de árbol, tipo de control StatusBar
- Properties, StatusBar (tipo de control)
- patrones de control, StatusBar (tipo de control)
- Events, StatusBar (tipo de control)
- compatibilidad con el tipo de control StatusBar
- StatusBar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control StatusBar
- tipos de control, patrones de control para el tipo de control StatusBar
- tipos de control, compatibilidad con StatusBar
- tipos de control, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ace64d34429a6d381dfdef2d99d82a3693fca2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357379"
---
# <a name="statusbar-control-type"></a><span data-ttu-id="76e6c-119">StatusBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="76e6c-119">StatusBar Control Type</span></span>

<span data-ttu-id="76e6c-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="76e6c-120">This topic provides information about Microsoft UI Automation support for the **StatusBar** control type.</span></span>

<span data-ttu-id="76e6c-121">Un control de barra de estado muestra información sobre un objeto que se ve en una ventana de una aplicación, el componente del objeto o información contextual relativa a esa operación del objeto en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="76e6c-121">A status bar control displays information about an object being viewed in a window of an application, the object's component, or contextual information that relates to that object's operation within your application.</span></span>

<span data-ttu-id="76e6c-122">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="76e6c-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **StatusBar** control type.</span></span> <span data-ttu-id="76e6c-123">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de barra de estado donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control</span><span class="sxs-lookup"><span data-stu-id="76e6c-123">The UI Automation requirements apply to all status bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="76e6c-124">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="76e6c-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="76e6c-125">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="76e6c-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="76e6c-126">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="76e6c-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="76e6c-127">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="76e6c-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="76e6c-128">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="76e6c-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="76e6c-129">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="76e6c-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="76e6c-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76e6c-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="76e6c-131">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="76e6c-131">Typical Tree Structure</span></span>

<span data-ttu-id="76e6c-132">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de barra de estado y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="76e6c-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to status bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="76e6c-133">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="76e6c-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="76e6c-134">Vista de control</span><span class="sxs-lookup"><span data-stu-id="76e6c-134">Control View</span></span></th>
<th><span data-ttu-id="76e6c-135">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="76e6c-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="76e6c-136">StatusBar</span><span class="sxs-lookup"><span data-stu-id="76e6c-136">StatusBar</span></span>
<ul>
<li><span data-ttu-id="76e6c-137">Edición (0 o más)</span><span class="sxs-lookup"><span data-stu-id="76e6c-137">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="76e6c-138">ProgressBar (0 o muchos)</span><span class="sxs-lookup"><span data-stu-id="76e6c-138">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="76e6c-139">Imagen (0 o muchos)</span><span class="sxs-lookup"><span data-stu-id="76e6c-139">Image (0 or many)</span></span></li>
<li><span data-ttu-id="76e6c-140">Botón (0 o muchos)</span><span class="sxs-lookup"><span data-stu-id="76e6c-140">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="76e6c-141">StatusBar</span><span class="sxs-lookup"><span data-stu-id="76e6c-141">StatusBar</span></span>
<ul>
<li><span data-ttu-id="76e6c-142">Edición (0 o más)</span><span class="sxs-lookup"><span data-stu-id="76e6c-142">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="76e6c-143">ProgressBar (0 o muchos)</span><span class="sxs-lookup"><span data-stu-id="76e6c-143">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="76e6c-144">Imagen (0 o muchos)</span><span class="sxs-lookup"><span data-stu-id="76e6c-144">Image (0 or many)</span></span></li>
<li><span data-ttu-id="76e6c-145">Botón (0 o muchos)</span><span class="sxs-lookup"><span data-stu-id="76e6c-145">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="76e6c-146">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="76e6c-146">Relevant Properties</span></span>

<span data-ttu-id="76e6c-147">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de barra de estado.</span><span class="sxs-lookup"><span data-stu-id="76e6c-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the status bar controls.</span></span> <span data-ttu-id="76e6c-148">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="76e6c-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="76e6c-149">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="76e6c-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="76e6c-150">Value</span><span class="sxs-lookup"><span data-stu-id="76e6c-150">Value</span></span>         | <span data-ttu-id="76e6c-151">Notas</span><span class="sxs-lookup"><span data-stu-id="76e6c-151">Notes</span></span>                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76e6c-152">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="76e6c-153">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="76e6c-153">See notes.</span></span>    | <span data-ttu-id="76e6c-154">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="76e6c-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                        |
| [<span data-ttu-id="76e6c-155">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="76e6c-156">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="76e6c-156">See notes.</span></span>    | <span data-ttu-id="76e6c-157">El rectángulo delimitador de una barra de estado debe abarcar todos los controles que incluye.</span><span class="sxs-lookup"><span data-stu-id="76e6c-157">The bounding rectangle of a status bar must encompass all of the controls contained within it.</span></span>                                                                                                                      |
| [<span data-ttu-id="76e6c-158">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="76e6c-159">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="76e6c-159">See notes.</span></span>    | <span data-ttu-id="76e6c-160">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="76e6c-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="76e6c-161">Si hay áreas dentro del rectángulo delimitador que no son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto en el que se pueden hacer clic.</span><span class="sxs-lookup"><span data-stu-id="76e6c-161">If there are areas within the bounding rectangle that are not clickable, and the element performs specialized hit testing, override this and provide a clickable point.</span></span> |
| [<span data-ttu-id="76e6c-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="76e6c-163">**StatusBar**</span><span class="sxs-lookup"><span data-stu-id="76e6c-163">**StatusBar**</span></span> |                                                                                                                                                                                                                     |
| [<span data-ttu-id="76e6c-164">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="76e6c-165">TRUE</span><span class="sxs-lookup"><span data-stu-id="76e6c-165">TRUE</span></span>          | <span data-ttu-id="76e6c-166">El control de barra de estado siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="76e6c-166">The status bar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="76e6c-167">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="76e6c-168">TRUE</span><span class="sxs-lookup"><span data-stu-id="76e6c-168">TRUE</span></span>          | <span data-ttu-id="76e6c-169">El control de barra de estado siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="76e6c-169">The status bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="76e6c-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="76e6c-171">Depende</span><span class="sxs-lookup"><span data-stu-id="76e6c-171">Depends</span></span>       | <span data-ttu-id="76e6c-172">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="76e6c-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                           |
| [<span data-ttu-id="76e6c-173">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-173">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="76e6c-174">Depende</span><span class="sxs-lookup"><span data-stu-id="76e6c-174">Depends</span></span>       | <span data-ttu-id="76e6c-175">Si un control de barra de estado no está visible actualmente, devolverá TRUE para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="76e6c-175">If a status bar control is not currently visible, it will return TRUE for this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="76e6c-176">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="76e6c-177">NULL</span><span class="sxs-lookup"><span data-stu-id="76e6c-177">NULL</span></span>          | <span data-ttu-id="76e6c-178">Normalmente, el control de barra de estado no tiene una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="76e6c-178">The status bar control typically does not have a label.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="76e6c-179">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="76e6c-180">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="76e6c-180">See notes.</span></span>    | <span data-ttu-id="76e6c-181">Cadena localizada que corresponde al tipo de control **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="76e6c-181">Localized string corresponding to the **StatusBar** control type.</span></span> <span data-ttu-id="76e6c-182">El valor predeterminado es "barra de estado" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="76e6c-182">The default value is "status bar" for en-US or English (United States).</span></span>                                                                           |
| [<span data-ttu-id="76e6c-183">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="76e6c-184">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="76e6c-184">See notes.</span></span>    | <span data-ttu-id="76e6c-185">El control de barra de estado no necesita un nombre a menos que se use más de uno dentro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="76e6c-185">The status bar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="76e6c-186">En este caso, distinga cada barra con nombres como "estado de Internet" o "estado de la aplicación".</span><span class="sxs-lookup"><span data-stu-id="76e6c-186">In this case, distinguish each bar with names such as "Internet Status" or "Application Status".</span></span>                    |
| [<span data-ttu-id="76e6c-187">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-187">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="76e6c-188">Depende</span><span class="sxs-lookup"><span data-stu-id="76e6c-188">Depends</span></span>       | <span data-ttu-id="76e6c-189">Un valor que indica la orientación del control: horizontal o vertical.</span><span class="sxs-lookup"><span data-stu-id="76e6c-189">A value indicating the control's orientation: horizontal or vertical.</span></span>                                                                                                                                               |



 

## <a name="required-control-patterns"></a><span data-ttu-id="76e6c-190">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="76e6c-190">Required Control Patterns</span></span>

<span data-ttu-id="76e6c-191">En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que se deben admitir para los controles de barra de estado.</span><span class="sxs-lookup"><span data-stu-id="76e6c-191">The following table lists the UI Automation control patterns required to be supported for status bar controls.</span></span> <span data-ttu-id="76e6c-192">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="76e6c-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="76e6c-193">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="76e6c-193">Control Pattern</span></span>                               | <span data-ttu-id="76e6c-194">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="76e6c-194">Support</span></span>  | <span data-ttu-id="76e6c-195">Notas</span><span class="sxs-lookup"><span data-stu-id="76e6c-195">Notes</span></span>                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76e6c-196">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="76e6c-196">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | <span data-ttu-id="76e6c-197">Opcionales</span><span class="sxs-lookup"><span data-stu-id="76e6c-197">Optional</span></span> | <span data-ttu-id="76e6c-198">Los controles de barra de estado deben admitir el patrón de control de [cuadrícula](uiauto-implementinggrid.md) para que se puedan supervisar y hacer referencia fácilmente a las partes individuales para obtener información.</span><span class="sxs-lookup"><span data-stu-id="76e6c-198">Status bar controls should support the [Grid](uiauto-implementinggrid.md) control pattern so that individual pieces can be monitored and easily referenced for information.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="76e6c-199">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="76e6c-199">Required Events</span></span>

<span data-ttu-id="76e6c-200">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de barra de estado deben admitir.</span><span class="sxs-lookup"><span data-stu-id="76e6c-200">The following table lists the UI Automation events that status bar controls are required to support.</span></span> <span data-ttu-id="76e6c-201">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="76e6c-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="76e6c-202">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="76e6c-202">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="76e6c-203">Notas</span><span class="sxs-lookup"><span data-stu-id="76e6c-203">Notes</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="76e6c-204">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                   |
| <span data-ttu-id="76e6c-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="76e6c-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                   |
| <span data-ttu-id="76e6c-206">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="76e6c-206">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="76e6c-207">Si el control admite la propiedad **IsEnabled** , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="76e6c-207">If the control supports the **IsEnabled** property, it must support this event.</span></span>   |
| <span data-ttu-id="76e6c-208">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="76e6c-208">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="76e6c-209">Si el control admite la propiedad **IsOffscreen** , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="76e6c-209">If the control supports the **IsOffscreen** property, it must support this event.</span></span> |
| [<span data-ttu-id="76e6c-210">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="76e6c-210">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="76e6c-211">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76e6c-211">Remarks</span></span>

<span data-ttu-id="76e6c-212">Se recomienda utilizar los controles de edición como elementos de cuadrícula secundarios en una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="76e6c-212">We recommend that edit controls be used as child grid elements in a status bar.</span></span> <span data-ttu-id="76e6c-213">El uso de controles de edición facilita la Asociación del propósito del campo de estado con su valor mediante el uso de la propiedad nombre y valor del elemento.</span><span class="sxs-lookup"><span data-stu-id="76e6c-213">Using edit controls makes it easier to associate the purpose of the status field with its value by using the element name and value property.</span></span> <span data-ttu-id="76e6c-214">Dado que los controles de texto no deben admitir el patrón de control **Value** , no deben usarse como elementos de cuadrícula secundarios.</span><span class="sxs-lookup"><span data-stu-id="76e6c-214">Because text controls should not support the **Value** control pattern, they should not be used as child grid elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76e6c-215">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76e6c-215">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="76e6c-216">**Vista**</span><span class="sxs-lookup"><span data-stu-id="76e6c-216">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="76e6c-217">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="76e6c-217">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="76e6c-218">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="76e6c-218">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




