---
title: ToolBar (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control ToolBar. Los controles de barra de herramientas permiten a los usuarios finales activar comandos y herramientas incluidos en una aplicación.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control ToolBar
- UI Automation, ToolBar (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control ToolBar
- Automatización de la interfaz de usuario, propiedades para el tipo de control ToolBar
- Automatización de la interfaz de usuario, patrones de control para el tipo de control ToolBar
- Automatización de la interfaz de usuario, eventos para el tipo de control ToolBar
- estructuras de árbol, ToolBar (tipo de control)
- Properties, ToolBar (tipo de control)
- patrones de control, ToolBar (tipo de control)
- Events, ToolBar (tipo de control)
- compatibilidad con el tipo de control ToolBar
- ToolBar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control ToolBar
- tipos de control, patrones de control para el tipo de control ToolBar
- tipos de control, compatibilidad con la barra de herramientas
- tipos de controles, barra de herramientas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327c187a86ace6f02b93082675c345eae4d4edf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419081"
---
# <a name="toolbar-control-type"></a><span data-ttu-id="baa56-120">ToolBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="baa56-120">ToolBar Control Type</span></span>

<span data-ttu-id="baa56-121">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="baa56-121">This topic provides information about Microsoft UI Automation support for the **ToolBar** control type.</span></span> <span data-ttu-id="baa56-122">Los controles de barra de herramientas permiten a los usuarios finales activar comandos y herramientas incluidos en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="baa56-122">Toolbar controls enable end users to activate commands and tools contained within a application.</span></span>

<span data-ttu-id="baa56-123">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="baa56-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **ToolBar** control type.</span></span> <span data-ttu-id="baa56-124">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de barra de herramientas donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones</span><span class="sxs-lookup"><span data-stu-id="baa56-124">The UI Automation requirements apply to all toolbar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="baa56-125">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="baa56-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="baa56-126">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="baa56-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="baa56-127">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="baa56-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="baa56-128">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="baa56-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="baa56-129">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="baa56-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="baa56-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="baa56-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="baa56-131">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="baa56-131">Typical Tree Structure</span></span>

<span data-ttu-id="baa56-132">En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de barra de herramientas y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="baa56-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to toolbar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="baa56-133">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="baa56-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="baa56-134">Vista de control</span><span class="sxs-lookup"><span data-stu-id="baa56-134">Control View</span></span></th>
<th><span data-ttu-id="baa56-135">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="baa56-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="baa56-136">ToolBar</span><span class="sxs-lookup"><span data-stu-id="baa56-136">ToolBar</span></span>
<ul>
<li><span data-ttu-id="baa56-137">Varios controles (0 o más)</span><span class="sxs-lookup"><span data-stu-id="baa56-137">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="baa56-138">ToolBar</span><span class="sxs-lookup"><span data-stu-id="baa56-138">ToolBar</span></span>
<ul>
<li><span data-ttu-id="baa56-139">Varios controles (0 o más)</span><span class="sxs-lookup"><span data-stu-id="baa56-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="baa56-140">Un control de barra de herramientas puede contener cualquier tipo de control dentro de su subárbol.</span><span class="sxs-lookup"><span data-stu-id="baa56-140">A toolbar control can contain any type of control within its subtree.</span></span> <span data-ttu-id="baa56-141">Más a menudo contienen botones, cuadros combinados y botones de expansión.</span><span class="sxs-lookup"><span data-stu-id="baa56-141">They most often contain buttons, combo boxes, and split buttons.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="baa56-142">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="baa56-142">Relevant Properties</span></span>

<span data-ttu-id="baa56-143">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="baa56-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the **ToolBar** control type.</span></span> <span data-ttu-id="baa56-144">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="baa56-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="baa56-145">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="baa56-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="baa56-146">Value</span><span class="sxs-lookup"><span data-stu-id="baa56-146">Value</span></span>       | <span data-ttu-id="baa56-147">Notas</span><span class="sxs-lookup"><span data-stu-id="baa56-147">Notes</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="baa56-148">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="baa56-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="baa56-149">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="baa56-149">See notes.</span></span>  | <span data-ttu-id="baa56-150">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="baa56-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                               |
| [<span data-ttu-id="baa56-151">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="baa56-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="baa56-152">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="baa56-152">See notes.</span></span>  | <span data-ttu-id="baa56-153">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="baa56-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="baa56-154">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="baa56-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="baa56-155">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="baa56-155">See notes.</span></span>  | <span data-ttu-id="baa56-156">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="baa56-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="baa56-157">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="baa56-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>       |
| [<span data-ttu-id="baa56-158">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="baa56-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="baa56-159">**Barra**</span><span class="sxs-lookup"><span data-stu-id="baa56-159">**ToolBar**</span></span> | <span data-ttu-id="baa56-160">Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="baa56-160">This value is the same for all UI frameworks.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="baa56-161">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="baa56-161">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="baa56-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="baa56-162">TRUE</span></span>        | <span data-ttu-id="baa56-163">El control de barra de herramientas siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="baa56-163">The toolbar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="baa56-164">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="baa56-164">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="baa56-165">TRUE</span><span class="sxs-lookup"><span data-stu-id="baa56-165">TRUE</span></span>        | <span data-ttu-id="baa56-166">El control de barra de herramientas siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="baa56-166">The toolbar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="baa56-167">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="baa56-167">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="baa56-168">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="baa56-168">See notes.</span></span>  | <span data-ttu-id="baa56-169">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="baa56-169">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                  |
| [<span data-ttu-id="baa56-170">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="baa56-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="baa56-171">NULL</span><span class="sxs-lookup"><span data-stu-id="baa56-171">NULL</span></span>        | <span data-ttu-id="baa56-172">Un control de barra de herramientas nunca tiene una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="baa56-172">A toolbar control never has a label.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="baa56-173">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="baa56-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="baa56-174">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="baa56-174">See notes.</span></span>  | <span data-ttu-id="baa56-175">Cadena localizada que corresponde al tipo de control **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="baa56-175">Localized string corresponding to the **ToolBar** control type.</span></span> <span data-ttu-id="baa56-176">El valor predeterminado es "barra de herramientas" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="baa56-176">The default value is "tool bar" for en-US or English (United States).</span></span>                                                                      |
| [<span data-ttu-id="baa56-177">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="baa56-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="baa56-178">Depende</span><span class="sxs-lookup"><span data-stu-id="baa56-178">Depends</span></span>     | <span data-ttu-id="baa56-179">El control de barra de herramientas no necesita un nombre a menos que se use más de uno dentro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="baa56-179">The toolbar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="baa56-180">Si hay más de uno, cada uno debe tener un nombre distintivo (por ejemplo, "formato" o "esquematización").</span><span class="sxs-lookup"><span data-stu-id="baa56-180">If more than one is present, each must have a distinguishing name (for example, "Formatting" or "Outlining").</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="baa56-181">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="baa56-181">Required Control Patterns</span></span>

<span data-ttu-id="baa56-182">En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que deben admitir los controles de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="baa56-182">The following table lists the UI Automation control patterns required to be supported by toolbar controls.</span></span> <span data-ttu-id="baa56-183">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="baa56-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="baa56-184">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="baa56-184">Control Pattern</span></span>                                                   | <span data-ttu-id="baa56-185">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="baa56-185">Support</span></span> | <span data-ttu-id="baa56-186">Notas</span><span class="sxs-lookup"><span data-stu-id="baa56-186">Notes</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="baa56-187">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="baa56-187">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="baa56-188">Depende</span><span class="sxs-lookup"><span data-stu-id="baa56-188">Depends</span></span> | <span data-ttu-id="baa56-189">Si la barra de herramientas se puede acoplar a diferentes partes de la pantalla, debe admitir el patrón de control [Dock](uiauto-implementingdock.md) .</span><span class="sxs-lookup"><span data-stu-id="baa56-189">If the toolbar can be docked to different parts of the screen, it must support the [Dock](uiauto-implementingdock.md) control pattern.</span></span>                       |
| [<span data-ttu-id="baa56-190">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="baa56-190">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="baa56-191">Depende</span><span class="sxs-lookup"><span data-stu-id="baa56-191">Depends</span></span> | <span data-ttu-id="baa56-192">Si la barra de herramientas se puede expandir y contraer para mostrar más elementos, debe admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="baa56-192">If the toolbar can be expanded and collapsed to show more items, it must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="baa56-193">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="baa56-193">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="baa56-194">Depende</span><span class="sxs-lookup"><span data-stu-id="baa56-194">Depends</span></span> | <span data-ttu-id="baa56-195">Si la barra de herramientas puede cambiar de tamaño, girarse o moverse, debe admitir el patrón de control [Transform](uiauto-implementingtransform.md) .</span><span class="sxs-lookup"><span data-stu-id="baa56-195">If the toolbar can be resized, rotated, or moved, it must support the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>                          |



 

## <a name="required-events"></a><span data-ttu-id="baa56-196">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="baa56-196">Required Events</span></span>

<span data-ttu-id="baa56-197">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de barra de herramientas deben admitir.</span><span class="sxs-lookup"><span data-stu-id="baa56-197">The following table lists the UI Automation events that toolbar controls are required to support.</span></span> <span data-ttu-id="baa56-198">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="baa56-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="baa56-199">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="baa56-199">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="baa56-200">Notas</span><span class="sxs-lookup"><span data-stu-id="baa56-200">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="baa56-201">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="baa56-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="baa56-202">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="baa56-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="baa56-203">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="baa56-203">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="baa56-204">Si el control admite el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="baa56-204">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="baa56-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="baa56-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="baa56-206">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="baa56-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="baa56-207">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="baa56-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="baa56-208">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="baa56-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="baa56-209">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="baa56-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="baa56-210">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="baa56-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="baa56-211">**Vista**</span><span class="sxs-lookup"><span data-stu-id="baa56-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="baa56-212">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="baa56-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="baa56-213">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="baa56-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




