---
title: Tab (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Tab.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Tab
- UI Automation, Tab (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Tab
- UI Automation, propiedades para el tipo de control Tab
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Tab
- Automatización de la interfaz de usuario, eventos para el tipo de control Tab
- estructuras de árbol, tipo de control Tab
- Properties, Tab (tipo de control)
- patrones de control, Tab (tipo de control)
- Events, Tab (tipo de control)
- compatibilidad con el tipo de control Tab
- Tab (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Tab
- tipos de control, patrones de control para el tipo de control Tab
- tipos de control, compatibilidad con Tab
- tipos de control, pestaña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769a03617830c33fce4a8f64c594010b2120785b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994356"
---
# <a name="tab-control-type"></a><span data-ttu-id="6c64b-119">Tab (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="6c64b-119">Tab Control Type</span></span>

<span data-ttu-id="6c64b-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Tab** .</span><span class="sxs-lookup"><span data-stu-id="6c64b-120">This topic provides information about Microsoft UI Automation support for the **Tab** control type.</span></span>

<span data-ttu-id="6c64b-121">Un control de ficha es análogo a los divisores de un bloc de notas o las etiquetas de un archivador.</span><span class="sxs-lookup"><span data-stu-id="6c64b-121">A tab control is analogous to the dividers in a notebook or the labels in a file cabinet.</span></span> <span data-ttu-id="6c64b-122">Mediante el uso de un control de ficha, una aplicación puede definir varias páginas para la misma área de un cuadro de diálogo o de una ventana.</span><span class="sxs-lookup"><span data-stu-id="6c64b-122">By using a tab control, an application can define multiple pages for the same area of a window or dialog box.</span></span>

<span data-ttu-id="6c64b-123">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Tab** .</span><span class="sxs-lookup"><span data-stu-id="6c64b-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Tab** control type.</span></span> <span data-ttu-id="6c64b-124">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de ficha en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones</span><span class="sxs-lookup"><span data-stu-id="6c64b-124">The UI Automation requirements apply to all tab controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="6c64b-125">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="6c64b-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6c64b-126">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="6c64b-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="6c64b-127">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="6c64b-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="6c64b-128">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="6c64b-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="6c64b-129">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="6c64b-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="6c64b-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c64b-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="6c64b-131">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="6c64b-131">Typical Tree Structure</span></span>

<span data-ttu-id="6c64b-132">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de ficha y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="6c64b-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab controls and describes what can be contained in each view.</span></span> <span data-ttu-id="6c64b-133">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6c64b-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c64b-134">Vista de control</span><span class="sxs-lookup"><span data-stu-id="6c64b-134">Control View</span></span></th>
<th><span data-ttu-id="6c64b-135">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="6c64b-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="6c64b-136">Pestaña</span><span class="sxs-lookup"><span data-stu-id="6c64b-136">Tab</span></span>
<ul>
<li><span data-ttu-id="6c64b-137">TabItem (1 o más)</span><span class="sxs-lookup"><span data-stu-id="6c64b-137">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="6c64b-138">ScrollBar (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="6c64b-138">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="6c64b-139">Button (0 o 2)</span><span class="sxs-lookup"><span data-stu-id="6c64b-139">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6c64b-140">Pestaña</span><span class="sxs-lookup"><span data-stu-id="6c64b-140">Tab</span></span>
<ul>
<li><span data-ttu-id="6c64b-141">TabItem (1 o más)</span><span class="sxs-lookup"><span data-stu-id="6c64b-141">TabItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6c64b-142">Los controles de ficha tienen elementos de automatización de la interfaz de usuario secundarios basados en el tipo de control [TabItem](uiauto-supporttabitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="6c64b-142">Tab controls have child UI Automation elements based on the [TabItem](uiauto-supporttabitemcontroltype.md) control type.</span></span> <span data-ttu-id="6c64b-143">Cuando se agrupan los elementos de ficha (por ejemplo, como en Microsoft Office aplicaciones) el tipo de control **Tab** también puede hospedar los tipos de control **Groups** para los elementos de ficha agrupados, como muestra la siguiente estructura de árbol.</span><span class="sxs-lookup"><span data-stu-id="6c64b-143">When tab items are grouped (for example, as in Microsoft Office applications) the **Tab** control type can also host **Groups** control types for the grouped tab items, as the following tree structure shows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c64b-144">Vista de control</span><span class="sxs-lookup"><span data-stu-id="6c64b-144">Control View</span></span></th>
<th><span data-ttu-id="6c64b-145">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="6c64b-145">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="6c64b-146">Pestaña</span><span class="sxs-lookup"><span data-stu-id="6c64b-146">Tab</span></span>
<ul>
<li><span data-ttu-id="6c64b-147">TabItem (1 o más)</span><span class="sxs-lookup"><span data-stu-id="6c64b-147">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="6c64b-148">Group (0 o más)</span><span class="sxs-lookup"><span data-stu-id="6c64b-148">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="6c64b-149">TabItem (0 o más)</span><span class="sxs-lookup"><span data-stu-id="6c64b-149">TabItem (0 or more)</span></span></li>
</ul></li>
<li><span data-ttu-id="6c64b-150">ScrollBar (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="6c64b-150">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="6c64b-151">Button (0 o 2)</span><span class="sxs-lookup"><span data-stu-id="6c64b-151">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6c64b-152">Pestaña</span><span class="sxs-lookup"><span data-stu-id="6c64b-152">Tab</span></span>
<ul>
<li><span data-ttu-id="6c64b-153">TabItem (1 o más)</span><span class="sxs-lookup"><span data-stu-id="6c64b-153">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="6c64b-154">Group (0 o más)</span><span class="sxs-lookup"><span data-stu-id="6c64b-154">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="6c64b-155">TabItem (0 o más)</span><span class="sxs-lookup"><span data-stu-id="6c64b-155">TabItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="6c64b-156">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="6c64b-156">Relevant Properties</span></span>

<span data-ttu-id="6c64b-157">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de ficha.</span><span class="sxs-lookup"><span data-stu-id="6c64b-157">The following table lists the UI Automation properties whose value or definition is especially relevant to tab controls.</span></span> <span data-ttu-id="6c64b-158">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="6c64b-158">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="6c64b-159">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="6c64b-159">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="6c64b-160">Value</span><span class="sxs-lookup"><span data-stu-id="6c64b-160">Value</span></span>      | <span data-ttu-id="6c64b-161">Notas</span><span class="sxs-lookup"><span data-stu-id="6c64b-161">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c64b-162">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-162">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="6c64b-163">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="6c64b-163">See notes.</span></span> | <span data-ttu-id="6c64b-164">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6c64b-164">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="6c64b-165">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-165">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="6c64b-166">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="6c64b-166">See notes.</span></span> | <span data-ttu-id="6c64b-167">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="6c64b-167">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="6c64b-168">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-168">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="6c64b-169">No</span><span class="sxs-lookup"><span data-stu-id="6c64b-169">No</span></span>         | <span data-ttu-id="6c64b-170">El control de ficha no tiene puntos seleccionables.</span><span class="sxs-lookup"><span data-stu-id="6c64b-170">The tab control does not have clickable points.</span></span>                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="6c64b-171">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-171">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="6c64b-172">**Tabulación**</span><span class="sxs-lookup"><span data-stu-id="6c64b-172">**Tab**</span></span>    |                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="6c64b-173">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-173">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6c64b-174">TRUE</span><span class="sxs-lookup"><span data-stu-id="6c64b-174">TRUE</span></span>       | <span data-ttu-id="6c64b-175">El control de pestaña siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6c64b-175">The tab control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="6c64b-176">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-176">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6c64b-177">TRUE</span><span class="sxs-lookup"><span data-stu-id="6c64b-177">TRUE</span></span>       | <span data-ttu-id="6c64b-178">El control de pestaña siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6c64b-178">The tab control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="6c64b-179">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-179">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="6c64b-180">TRUE</span><span class="sxs-lookup"><span data-stu-id="6c64b-180">TRUE</span></span>       | <span data-ttu-id="6c64b-181">El tipo de control Tab debe poder recibir el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="6c64b-181">The Tab control type must be able to receive keyboard focus.</span></span> <span data-ttu-id="6c64b-182">Normalmente, un cliente de automatización de la interfaz de usuario llama a [**IUIAutomationElement:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) en un control de ficha y uno de sus elementos reenvía el foco del teclado al control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="6c64b-182">Typically, a UI Automation client calls [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on a tab control and one of its items will forward the keyboard focus to the tab control.</span></span> <span data-ttu-id="6c64b-183">Es posible que algunos contenedores de ficha obtengan el foco sin haber establecido el foco en uno de sus elementos.</span><span class="sxs-lookup"><span data-stu-id="6c64b-183">It is possible for some tab containers to take focus without setting focus to one of its items.</span></span> |
| [<span data-ttu-id="6c64b-184">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-184">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="6c64b-185">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="6c64b-185">See notes.</span></span> | <span data-ttu-id="6c64b-186">Los controles de ficha suelen tener una etiqueta de texto estático que se expone a través de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="6c64b-186">Tab controls typically have a static text label that is exposed through this property.</span></span>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="6c64b-187">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-187">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="6c64b-188">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="6c64b-188">See notes.</span></span> | <span data-ttu-id="6c64b-189">Cadena localizada que corresponde al tipo de control **Tab** .</span><span class="sxs-lookup"><span data-stu-id="6c64b-189">Localized string corresponding to the **Tab** control type.</span></span> <span data-ttu-id="6c64b-190">El valor predeterminado es "Tab" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="6c64b-190">The default value is "tab" for en-US or English (United States).</span></span>                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="6c64b-191">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-191">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="6c64b-192">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="6c64b-192">See notes.</span></span> | <span data-ttu-id="6c64b-193">El control de ficha rara vez requiere una propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="6c64b-193">The tab control rarely requires a **Name** property.</span></span>                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="6c64b-194">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-194">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="6c64b-195">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="6c64b-195">See notes.</span></span> | <span data-ttu-id="6c64b-196">El control de ficha siempre debe indicar si está colocado horizontal o verticalmente.</span><span class="sxs-lookup"><span data-stu-id="6c64b-196">The tab control must always indicate whether it is positioned horizontally or vertically.</span></span>                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="6c64b-197">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="6c64b-197">Required Control Patterns</span></span>

<span data-ttu-id="6c64b-198">En la tabla siguiente se muestran los patrones de control de UI Automation que se deben admitir por todos los controles de ficha.</span><span class="sxs-lookup"><span data-stu-id="6c64b-198">The following table lists the UI Automation control patterns required to be supported by all tab controls.</span></span> <span data-ttu-id="6c64b-199">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6c64b-199">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="6c64b-200">Patrón de control/Propiedad de patrón</span><span class="sxs-lookup"><span data-stu-id="6c64b-200">Control Pattern/Pattern Property</span></span>                                             | <span data-ttu-id="6c64b-201">Soporte técnico/valor</span><span class="sxs-lookup"><span data-stu-id="6c64b-201">Support/Value</span></span> | <span data-ttu-id="6c64b-202">Notas</span><span class="sxs-lookup"><span data-stu-id="6c64b-202">Notes</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c64b-203">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="6c64b-203">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | <span data-ttu-id="6c64b-204">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6c64b-204">Required</span></span>      | <span data-ttu-id="6c64b-205">Todos los controles de ficha deben admitir el patrón de control [Selection](uiauto-implementingselection.md) .</span><span class="sxs-lookup"><span data-stu-id="6c64b-205">All tab controls must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span>                                                                       |
| [<span data-ttu-id="6c64b-206">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="6c64b-206">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | <span data-ttu-id="6c64b-207">TRUE</span><span class="sxs-lookup"><span data-stu-id="6c64b-207">TRUE</span></span>          | <span data-ttu-id="6c64b-208">Los controles de ficha siempre requieren que se realice una selección.</span><span class="sxs-lookup"><span data-stu-id="6c64b-208">Tab controls always require that a selection be made.</span></span>                                                                                                                  |
| [<span data-ttu-id="6c64b-209">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="6c64b-209">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | <span data-ttu-id="6c64b-210">false</span><span class="sxs-lookup"><span data-stu-id="6c64b-210">FALSE</span></span>         | <span data-ttu-id="6c64b-211">Los controles de ficha siempre son contenedores de selección única.</span><span class="sxs-lookup"><span data-stu-id="6c64b-211">Tab controls are always single-selection containers.</span></span>                                                                                                                   |
| [<span data-ttu-id="6c64b-212">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="6c64b-212">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | <span data-ttu-id="6c64b-213">Depende</span><span class="sxs-lookup"><span data-stu-id="6c64b-213">Depends</span></span>       | <span data-ttu-id="6c64b-214">Se debe admitir el patrón de control [Scroll](uiauto-implementingscroll.md) si el control de pestaña tiene widgets que permiten desplazarse por un conjunto de elementos de ficha.</span><span class="sxs-lookup"><span data-stu-id="6c64b-214">The [Scroll](uiauto-implementingscroll.md) control pattern must be supported if the tab control has widgets that allow for a set of tab items to be scrolled through.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="6c64b-215">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="6c64b-215">Required Events</span></span>

<span data-ttu-id="6c64b-216">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que deben admitir los controles de ficha.</span><span class="sxs-lookup"><span data-stu-id="6c64b-216">The following table lists the UI Automation events that tab controls are required to support.</span></span> <span data-ttu-id="6c64b-217">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6c64b-217">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="6c64b-218">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="6c64b-218">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="6c64b-219">Notas</span><span class="sxs-lookup"><span data-stu-id="6c64b-219">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c64b-220">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-220">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="6c64b-221">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="6c64b-221">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="6c64b-222">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="6c64b-222">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="6c64b-223">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="6c64b-223">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="6c64b-224">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="6c64b-224">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="6c64b-225">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="6c64b-225">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="6c64b-226">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="6c64b-226">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="6c64b-227">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="6c64b-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="6c64b-228">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="6c64b-228">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="6c64b-229">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="6c64b-229">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="6c64b-230">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="6c64b-230">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="6c64b-231">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="6c64b-231">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="6c64b-232">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="6c64b-232">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="6c64b-233">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="6c64b-233">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="6c64b-234">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="6c64b-234">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="6c64b-235">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="6c64b-235">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="6c64b-236">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="6c64b-236">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="6c64b-237">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="6c64b-237">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="6c64b-238">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="6c64b-238">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="6c64b-239">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c64b-239">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6c64b-240">**Vista**</span><span class="sxs-lookup"><span data-stu-id="6c64b-240">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6c64b-241">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="6c64b-241">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="6c64b-242">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="6c64b-242">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




