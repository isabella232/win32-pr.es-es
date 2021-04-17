---
title: Table (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Table.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Table
- Automatización de la interfaz de usuario, Table (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Table
- Automatización de la interfaz de usuario, propiedades para el tipo de control Table
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Table
- Automatización de la interfaz de usuario, eventos para el tipo de control Table
- estructuras de árbol, Table (tipo de control)
- propiedades, Table (tipo de control)
- patrones de control, Table (tipo de control)
- Events, Table (tipo de control)
- compatibilidad con el tipo de control Table
- Table (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Table
- tipos de control, patrones de control para el tipo de control Table
- tipos de control, compatibilidad con tablas
- tipos de controles, tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4ee709bd16156a62882aeee014b4744dab2214
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532308"
---
# <a name="table-control-type"></a><span data-ttu-id="dee72-119">Table (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="dee72-119">Table Control Type</span></span>

<span data-ttu-id="dee72-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **TABLE** .</span><span class="sxs-lookup"><span data-stu-id="dee72-120">This topic provides information about Microsoft UI Automation support for the **Table** control type.</span></span>

<span data-ttu-id="dee72-121">Los controles de tabla contienen filas y columnas de texto y, opcionalmente, encabezados de fila y encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="dee72-121">Table controls contain rows and columns of text and, optionally, row headers and column headers.</span></span>

<span data-ttu-id="dee72-122">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **TABLE** .</span><span class="sxs-lookup"><span data-stu-id="dee72-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Table** control type.</span></span> <span data-ttu-id="dee72-123">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de tabla donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control.</span><span class="sxs-lookup"><span data-stu-id="dee72-123">The UI Automation requirements apply to all table controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="dee72-124">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="dee72-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="dee72-125">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="dee72-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="dee72-126">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="dee72-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="dee72-127">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="dee72-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="dee72-128">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="dee72-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="dee72-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dee72-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="dee72-130">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="dee72-130">Typical Tree Structure</span></span>

<span data-ttu-id="dee72-131">En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de tabla y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="dee72-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to table controls and describes what can be contained in each view.</span></span> <span data-ttu-id="dee72-132">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="dee72-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dee72-133">Vista de control</span><span class="sxs-lookup"><span data-stu-id="dee72-133">Control View</span></span></th>
<th><span data-ttu-id="dee72-134">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="dee72-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="dee72-135">Tabla</span><span class="sxs-lookup"><span data-stu-id="dee72-135">Table</span></span>
<ul>
<li><span data-ttu-id="dee72-136">Text (0 o 1)</span><span class="sxs-lookup"><span data-stu-id="dee72-136">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="dee72-137">Encabezado (0 o más)</span><span class="sxs-lookup"><span data-stu-id="dee72-137">Header (0 or more)</span></span></li>
<li><span data-ttu-id="dee72-138">Varios controles (0 o más)</span><span class="sxs-lookup"><span data-stu-id="dee72-138">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="dee72-139">Tabla</span><span class="sxs-lookup"><span data-stu-id="dee72-139">Table</span></span>
<ul>
<li><span data-ttu-id="dee72-140">Texto (1 o más)</span><span class="sxs-lookup"><span data-stu-id="dee72-140">Text (1 or more)</span></span></li>
<li><span data-ttu-id="dee72-141">Varios controles (0 o más)</span><span class="sxs-lookup"><span data-stu-id="dee72-141">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="dee72-142">Si un control de tabla tiene encabezados de fila o columna, se deben exponer en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="dee72-142">If a table control has row or column headers, they must be exposed in the control view of the UI Automation tree.</span></span> <span data-ttu-id="dee72-143">La vista de contenido no tiene que exponer esta información porque se puede tener acceso a ella mediante [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).</span><span class="sxs-lookup"><span data-stu-id="dee72-143">The content view does not need to expose this information because it can be accessed using [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="dee72-144">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="dee72-144">Relevant Properties</span></span>

<span data-ttu-id="dee72-145">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de tabla.</span><span class="sxs-lookup"><span data-stu-id="dee72-145">The following table lists the UI Automation properties whose value or definition is especially relevant to table controls.</span></span> <span data-ttu-id="dee72-146">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="dee72-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="dee72-147">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="dee72-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="dee72-148">Value</span><span class="sxs-lookup"><span data-stu-id="dee72-148">Value</span></span>      | <span data-ttu-id="dee72-149">Notas</span><span class="sxs-lookup"><span data-stu-id="dee72-149">Notes</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dee72-150">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="dee72-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="dee72-151">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="dee72-151">See notes.</span></span> | <span data-ttu-id="dee72-152">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="dee72-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="dee72-153">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="dee72-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="dee72-154">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="dee72-154">See notes.</span></span> | <span data-ttu-id="dee72-155">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="dee72-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="dee72-156">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="dee72-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="dee72-157">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="dee72-157">See notes.</span></span> | <span data-ttu-id="dee72-158">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="dee72-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="dee72-159">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="dee72-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                              |
| [<span data-ttu-id="dee72-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="dee72-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="dee72-161">**Table**</span><span class="sxs-lookup"><span data-stu-id="dee72-161">**Table**</span></span>  |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="dee72-162">**UIA \_ DescribedByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="dee72-162">**UIA\_DescribedByPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="dee72-163">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="dee72-163">See notes.</span></span> | <span data-ttu-id="dee72-164">Si la tabla se anota por otro elemento de la interfaz de usuario (por ejemplo, un elemento de texto que contiene la descripción de la tabla), la propiedad DescribedBy debería exponer una referencia al elemento de automatización del control de texto.</span><span class="sxs-lookup"><span data-stu-id="dee72-164">If the table is annotated by other UI element (for example, a text element that holds the description for the table), the DescribedBy property should expose a reference to the automation element of the text control.</span></span>           |
| [<span data-ttu-id="dee72-165">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="dee72-165">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="dee72-166">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="dee72-166">See notes.</span></span> | <span data-ttu-id="dee72-167">Se deben exponer más detalles sobre la finalidad de la tabla a través de esta propiedad si la propiedad [**\_ NamePropertyId de UIA**](uiauto-automation-element-propids.md) no lo explica suficientemente.</span><span class="sxs-lookup"><span data-stu-id="dee72-167">More details about the purpose of the table should be exposed through this property if it is not sufficiently explained by the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span>      |
| [<span data-ttu-id="dee72-168">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="dee72-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="dee72-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="dee72-169">TRUE</span></span>       | <span data-ttu-id="dee72-170">El control de tabla siempre debe aparecer en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="dee72-170">The table control must always appear in the content view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="dee72-171">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="dee72-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="dee72-172">TRUE</span><span class="sxs-lookup"><span data-stu-id="dee72-172">TRUE</span></span>       | <span data-ttu-id="dee72-173">El control de tabla siempre debe aparecer en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="dee72-173">The table control must always appear in the control view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="dee72-174">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="dee72-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="dee72-175">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="dee72-175">See notes.</span></span> | <span data-ttu-id="dee72-176">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="dee72-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="dee72-177">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="dee72-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="dee72-178">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="dee72-178">See notes.</span></span> | <span data-ttu-id="dee72-179">Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia al elemento de automatización del control.</span><span class="sxs-lookup"><span data-stu-id="dee72-179">If there is a static text label, this property should expose a reference to the automation element of the control.</span></span>                                                                                                                |
| [<span data-ttu-id="dee72-180">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="dee72-180">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="dee72-181">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="dee72-181">See notes.</span></span> | <span data-ttu-id="dee72-182">Cadena localizada que corresponde al tipo de control **TABLE** .</span><span class="sxs-lookup"><span data-stu-id="dee72-182">Localized string corresponding to the **Table** control type.</span></span> <span data-ttu-id="dee72-183">El valor predeterminado es "Table" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="dee72-183">The default value is "table" for en-US or English (United States).</span></span>                                                                                                  |
| [<span data-ttu-id="dee72-184">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="dee72-184">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="dee72-185">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="dee72-185">See notes.</span></span> | <span data-ttu-id="dee72-186">Normalmente, el control de tabla obtiene el valor de su nombre de una etiqueta de texto estático.</span><span class="sxs-lookup"><span data-stu-id="dee72-186">The table control typically gets the value for its name from a static text label.</span></span> <span data-ttu-id="dee72-187">Si no hay una etiqueta de texto estático, el elemento debe asignar una propiedad Name que siempre debe estar disponible para explicar la finalidad de la tabla.</span><span class="sxs-lookup"><span data-stu-id="dee72-187">If there is not a static text label, the element must assign a Name property that must always be available to explain the purpose of the table.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="dee72-188">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="dee72-188">Required Control Patterns</span></span>

<span data-ttu-id="dee72-189">En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de tabla.</span><span class="sxs-lookup"><span data-stu-id="dee72-189">The following table lists the UI Automation control patterns required to be supported by all table controls.</span></span> <span data-ttu-id="dee72-190">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="dee72-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="dee72-191">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="dee72-191">Control Pattern</span></span>                                         | <span data-ttu-id="dee72-192">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="dee72-192">Support</span></span>                     | <span data-ttu-id="dee72-193">Notas</span><span class="sxs-lookup"><span data-stu-id="dee72-193">Notes</span></span>                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dee72-194">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="dee72-194">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="dee72-195">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="dee72-195">Required</span></span>                    | <span data-ttu-id="dee72-196">Dado que el control de tabla contiene elementos presentados en una cuadrícula, siempre admite el patrón de control [Grid](uiauto-implementinggrid.md) .</span><span class="sxs-lookup"><span data-stu-id="dee72-196">Because the table control contains items presented in a grid, it always supports the [Grid](uiauto-implementinggrid.md) control pattern.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="dee72-197">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="dee72-197">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="dee72-198">Requerido con objetos secundarios</span><span class="sxs-lookup"><span data-stu-id="dee72-198">Required with child objects</span></span> | <span data-ttu-id="dee72-199">Los objetos internos de una tabla deben admitir los patrones de control [GridItem](uiauto-implementinggriditem.md) y [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="dee72-199">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="dee72-200">La propia tabla no necesita admitir el patrón de control GridItem o TableItem, a menos que la tabla forme parte de otra tabla.</span><span class="sxs-lookup"><span data-stu-id="dee72-200">The table itself need not support the GridItem or TableItem control pattern unless the table is part of another table.</span></span>  |
| [<span data-ttu-id="dee72-201">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="dee72-201">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="dee72-202">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="dee72-202">Required</span></span>                    | <span data-ttu-id="dee72-203">El control de tabla siempre puede tener encabezados asociados al contenido.</span><span class="sxs-lookup"><span data-stu-id="dee72-203">The table control can always have headers associated with the content.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="dee72-204">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="dee72-204">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="dee72-205">Requerido con objetos secundarios</span><span class="sxs-lookup"><span data-stu-id="dee72-205">Required with child objects</span></span> | <span data-ttu-id="dee72-206">Los objetos internos de una tabla deben admitir los patrones de control [GridItem](uiauto-implementinggriditem.md) y [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="dee72-206">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="dee72-207">La propia tabla no necesita admitir los patrones de control GridItem o TableItem, a menos que la tabla forme parte de otra tabla.</span><span class="sxs-lookup"><span data-stu-id="dee72-207">The table itself need not support the GridItem or TableItem control patterns unless the table is part of another table.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="dee72-208">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="dee72-208">Required Events</span></span>

<span data-ttu-id="dee72-209">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de tabla deben admitir.</span><span class="sxs-lookup"><span data-stu-id="dee72-209">The following table lists the UI Automation events that table controls are required to support.</span></span> <span data-ttu-id="dee72-210">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="dee72-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="dee72-211">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="dee72-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="dee72-212">Notas</span><span class="sxs-lookup"><span data-stu-id="dee72-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dee72-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="dee72-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="dee72-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="dee72-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="dee72-215">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="dee72-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="dee72-216">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="dee72-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="dee72-217">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="dee72-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="dee72-218">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="dee72-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="dee72-219">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="dee72-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="dee72-220">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dee72-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dee72-221">**Vista**</span><span class="sxs-lookup"><span data-stu-id="dee72-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dee72-222">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="dee72-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="dee72-223">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="dee72-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




