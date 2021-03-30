---
title: Spinner (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Spinner.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Spinner
- Automatización de la interfaz de usuario, tipo de control Spinner
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Spinner
- Automatización de la interfaz de usuario, propiedades para el tipo de control Spinner
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Spinner
- Automatización de la interfaz de usuario, eventos para el tipo de control Spinner
- estructuras de árbol, tipo de control Spinner
- propiedades, tipo de control Spinner
- patrones de control, tipo de control Spinner
- Events, Spinner (tipo de control)
- compatibilidad con el tipo de control Spinner
- Spinner (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Spinner
- tipos de control, patrones de control para el tipo de control Spinner
- tipos de controles, compatibilidad con el control de número
- tipos de controles, control de número
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9681160bf82c9a541412bb6dde8958c603fcfe22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778235"
---
# <a name="spinner-control-type"></a><span data-ttu-id="ff8b6-119">Spinner (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="ff8b6-119">Spinner Control Type</span></span>

<span data-ttu-id="ff8b6-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="ff8b6-120">This topic provides information about Microsoft UI Automation support for the **Spinner** control type.</span></span>

<span data-ttu-id="ff8b6-121">Los controles Spinner se usan para seleccionar desde un dominio de elementos o un intervalo de números.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-121">Spinner controls are used to select from a domain of items or a range of numbers.</span></span>

<span data-ttu-id="ff8b6-122">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="ff8b6-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Spinner** control type.</span></span> <span data-ttu-id="ff8b6-123">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de número donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control</span><span class="sxs-lookup"><span data-stu-id="ff8b6-123">The UI Automation requirements apply to all spinner controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="ff8b6-124">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ff8b6-125">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="ff8b6-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="ff8b6-126">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="ff8b6-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="ff8b6-127">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="ff8b6-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="ff8b6-128">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="ff8b6-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="ff8b6-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff8b6-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="ff8b6-130">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="ff8b6-130">Typical Tree Structure</span></span>

<span data-ttu-id="ff8b6-131">En la tabla siguiente se muestra una vista de contenido y control típica del árbol de automatización de la interfaz de usuario que pertenece a los controles de número cuando admiten los patrones de control de **RangeValue** y de **selección** y describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-131">The following table depicts a typical control and content view of the UI Automation tree that pertain to spinner controls when they support the **RangeValue** and **Selection** control patterns and describes what can be contained in each view.</span></span> <span data-ttu-id="ff8b6-132">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ff8b6-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="ff8b6-133">**Patrón de control RangeValue**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-133">**RangeValue control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff8b6-134">Vista de control</span><span class="sxs-lookup"><span data-stu-id="ff8b6-134">Control View</span></span></th>
<th><span data-ttu-id="ff8b6-135">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="ff8b6-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ff8b6-136">Spinner</span><span class="sxs-lookup"><span data-stu-id="ff8b6-136">Spinner</span></span>
<ul>
<li><span data-ttu-id="ff8b6-137">Edición (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="ff8b6-137">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="ff8b6-138">Botón (2)</span><span class="sxs-lookup"><span data-stu-id="ff8b6-138">Button (2)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ff8b6-139">Spinner</span><span class="sxs-lookup"><span data-stu-id="ff8b6-139">Spinner</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ff8b6-140">**Selection (patrón de control)**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-140">**Selection control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff8b6-141">Vista de control</span><span class="sxs-lookup"><span data-stu-id="ff8b6-141">Control View</span></span></th>
<th><span data-ttu-id="ff8b6-142">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="ff8b6-142">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ff8b6-143">Spinner</span><span class="sxs-lookup"><span data-stu-id="ff8b6-143">Spinner</span></span>
<ul>
<li><span data-ttu-id="ff8b6-144">Edición (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="ff8b6-144">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="ff8b6-145">Botón (2)</span><span class="sxs-lookup"><span data-stu-id="ff8b6-145">Button (2)</span></span></li>
<li><span data-ttu-id="ff8b6-146">Elemento de lista (0 o más)</span><span class="sxs-lookup"><span data-stu-id="ff8b6-146">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ff8b6-147">Spinner</span><span class="sxs-lookup"><span data-stu-id="ff8b6-147">Spinner</span></span>
<ul>
<li><span data-ttu-id="ff8b6-148">Elemento de lista (0 o más)</span><span class="sxs-lookup"><span data-stu-id="ff8b6-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ff8b6-149">Para asegurarse de que los dos botones del subárbol de la vista de control se pueden distinguir por herramientas de pruebas automatizadas, asigne el valor **ScrollAmount \_ SmallIncrement** o [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) a la propiedad **AutomationId** según corresponda.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-149">To ensure that the two buttons in the control view subtree can be distinguished by automated test tools, assign the **ScrollAmount\_SmallIncrement** or [**ScrollAmount\_SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) value to the **AutomationId** property as appropriate.</span></span> <span data-ttu-id="ff8b6-150">En algunas implementaciones, el control de edición asociado puede ser un elemento del mismo nivel que el control de número.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-150">For some implementations, the associated edit control may be a peer of the spinner control.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="ff8b6-151">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="ff8b6-151">Relevant Properties</span></span>

<span data-ttu-id="ff8b6-152">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de número.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-152">The following table lists the UI Automation properties whose value or definition is especially relevant to spinner controls.</span></span> <span data-ttu-id="ff8b6-153">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="ff8b6-153">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="ff8b6-154">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="ff8b6-154">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="ff8b6-155">Value</span><span class="sxs-lookup"><span data-stu-id="ff8b6-155">Value</span></span>       | <span data-ttu-id="ff8b6-156">Notas</span><span class="sxs-lookup"><span data-stu-id="ff8b6-156">Notes</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff8b6-157">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-157">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="ff8b6-158">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-158">See notes.</span></span>  | <span data-ttu-id="ff8b6-159">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-159">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="ff8b6-160">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-160">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="ff8b6-161">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-161">See notes.</span></span>  | <span data-ttu-id="ff8b6-162">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-162">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="ff8b6-163">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-163">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="ff8b6-164">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-164">See notes.</span></span>  | <span data-ttu-id="ff8b6-165">El punto en el que se puede hacer clic del control de número enfoca la parte de edición del control.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-165">The spinner control's clickable point gives focus to the edit portion of the control.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="ff8b6-166">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-166">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ff8b6-167">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-167">**Spinner**</span></span> | <span data-ttu-id="ff8b6-168">Este valor es el mismo para todos los marcos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-168">This value is the same for all frameworks.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="ff8b6-169">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-169">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ff8b6-170">TRUE</span><span class="sxs-lookup"><span data-stu-id="ff8b6-170">TRUE</span></span>        | <span data-ttu-id="ff8b6-171">El control de número siempre debe ser contenido.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-171">The spinner control must always be content.</span></span>                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="ff8b6-172">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-172">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ff8b6-173">TRUE</span><span class="sxs-lookup"><span data-stu-id="ff8b6-173">TRUE</span></span>        | <span data-ttu-id="ff8b6-174">El control de número siempre debe ser un control.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-174">The spinner control must always be a control.</span></span>                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="ff8b6-175">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-175">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="ff8b6-176">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-176">See notes.</span></span>  | <span data-ttu-id="ff8b6-177">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-177">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="ff8b6-178">Un control de número raramente toma el foco, pero cuando lo hace, el foco debe permanecer en el control de número en sí, no en los botones secundarios.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-178">A spinner control rarely takes the focus, but when it does, the focus should remain on the spinner control itself, not on the child buttons.</span></span> <span data-ttu-id="ff8b6-179">El usuario debe poder realizar todas las acciones de desplazamiento mediante las teclas flecha arriba y flecha abajo.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-179">The user should be able to perform all scrolling actions by using the UP ARROW and DOWN ARROW keys.</span></span> |
| [<span data-ttu-id="ff8b6-180">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-180">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="ff8b6-181">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-181">See notes.</span></span>  | <span data-ttu-id="ff8b6-182">Los controles de número tienen una etiqueta de texto estático.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-182">Spinner controls have a static text label.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="ff8b6-183">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-183">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="ff8b6-184">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-184">See notes.</span></span>  | <span data-ttu-id="ff8b6-185">Cadena localizada que corresponde al tipo de control **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="ff8b6-185">Localized string corresponding to the **Spinner** control type.</span></span> <span data-ttu-id="ff8b6-186">El valor predeterminado es "Spinner" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="ff8b6-186">The default value is "spinner" for en-US or English (United States).</span></span>                                                                                                                                                                                       |
| [<span data-ttu-id="ff8b6-187">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-187">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="ff8b6-188">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-188">See notes.</span></span>  | <span data-ttu-id="ff8b6-189">El control de número suele recibir su nombre de una etiqueta de texto estático.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-189">The spinner control typically gets its name from a static text label.</span></span>                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="ff8b6-190">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="ff8b6-190">Required Control Patterns</span></span>

<span data-ttu-id="ff8b6-191">En la tabla siguiente se muestran los patrones de control de UI Automation que se deben admitir por todos los controles de número.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-191">The following table lists the UI Automation control patterns required to be supported by all spinner controls.</span></span> <span data-ttu-id="ff8b6-192">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ff8b6-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="ff8b6-193">Patrón de control/Propiedad de patrón</span><span class="sxs-lookup"><span data-stu-id="ff8b6-193">Control Pattern/Pattern Property</span></span>                                         | <span data-ttu-id="ff8b6-194">Soporte técnico/valor</span><span class="sxs-lookup"><span data-stu-id="ff8b6-194">Support/Value</span></span> | <span data-ttu-id="ff8b6-195">Notas</span><span class="sxs-lookup"><span data-stu-id="ff8b6-195">Notes</span></span>                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff8b6-196">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-196">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | <span data-ttu-id="ff8b6-197">Depende</span><span class="sxs-lookup"><span data-stu-id="ff8b6-197">Depends</span></span>       | <span data-ttu-id="ff8b6-198">Los controles de número que abarcan un intervalo numérico pueden admitir el patrón de control [RangeValue](uiauto-implementingrangevalue.md) .</span><span class="sxs-lookup"><span data-stu-id="ff8b6-198">Spinner controls that span a numeric range can support the [RangeValue](uiauto-implementingrangevalue.md) control pattern.</span></span>               |
| [<span data-ttu-id="ff8b6-199">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-199">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | <span data-ttu-id="ff8b6-200">Depende</span><span class="sxs-lookup"><span data-stu-id="ff8b6-200">Depends</span></span>       | <span data-ttu-id="ff8b6-201">Los controles de número que tienen una lista de elementos que se van a seleccionar deben admitir el patrón de control [Selection](uiauto-implementingselection.md) .</span><span class="sxs-lookup"><span data-stu-id="ff8b6-201">Spinner controls that have a list of items to be selected must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span> |
| [<span data-ttu-id="ff8b6-202">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-202">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | <span data-ttu-id="ff8b6-203">false</span><span class="sxs-lookup"><span data-stu-id="ff8b6-203">FALSE</span></span>         | <span data-ttu-id="ff8b6-204">Los controles de número siempre son contenedores de selección única.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-204">Spinner controls are always single selection containers.</span></span>                                                                                  |
| [<span data-ttu-id="ff8b6-205">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-205">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | <span data-ttu-id="ff8b6-206">Depende</span><span class="sxs-lookup"><span data-stu-id="ff8b6-206">Depends</span></span>       | <span data-ttu-id="ff8b6-207">Los controles de número que abarcan un conjunto de opciones o números pueden admitir el patrón de control [Value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="ff8b6-207">Spinner controls that span a descrete set of options or numbers can support the [Value](uiauto-implementingvalue.md) control pattern.</span></span>    |



 

## <a name="required-events"></a><span data-ttu-id="ff8b6-208">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="ff8b6-208">Required Events</span></span>

<span data-ttu-id="ff8b6-209">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles Spinner deben admitir.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-209">The following table lists the UI Automation events that spinner controls are required to support.</span></span> <span data-ttu-id="ff8b6-210">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ff8b6-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="ff8b6-211">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="ff8b6-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="ff8b6-212">Notas</span><span class="sxs-lookup"><span data-stu-id="ff8b6-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff8b6-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="ff8b6-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="ff8b6-215">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="ff8b6-216">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="ff8b6-217">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="ff8b6-218">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="ff8b6-219">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de RangeValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-219">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="ff8b6-220">Si el control admite el patrón de control [RangeValue](uiauto-implementingrangevalue.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-220">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| <span data-ttu-id="ff8b6-221">[**UIA \_ Propiedad \_ InvalidatedEventId de selección**](uiauto-event-ids.md) : evento cambiado.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-221">[**UIA\_Selection\_InvalidatedEventId**](uiauto-event-ids.md) property-changed event.</span></span>               | <span data-ttu-id="ff8b6-222">Si el control admite el patrón de control [Selection](uiauto-implementingselection.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-222">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="ff8b6-223">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-223">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="ff8b6-224">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-224">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="ff8b6-225">Si el control admite el patrón de control [Value](uiauto-implementingvalue.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="ff8b6-225">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="ff8b6-226">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff8b6-226">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ff8b6-227">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ff8b6-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff8b6-228">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ff8b6-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="ff8b6-229">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="ff8b6-229">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




