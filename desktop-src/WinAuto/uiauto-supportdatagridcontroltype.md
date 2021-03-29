---
title: DataGrid (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control DataGrid.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control DataGrid
- Automatización de la interfaz de usuario, tipo de control DataGrid
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control DataGrid
- Automatización de la interfaz de usuario, propiedades para el tipo de control DataGrid
- Automatización de la interfaz de usuario, patrones de control para el tipo de control DataGrid
- Automatización de la interfaz de usuario, eventos para el tipo de control DataGrid
- estructuras de árbol, tipo de control DataGrid
- Properties, DataGrid (tipo de control)
- patrones de control, DataGrid (tipo de control)
- Events, DataGrid (tipo de control)
- compatibilidad con el tipo de control DataGrid
- DataGrid (tipo de control)
- tipos de control, estructura de árbol para el tipo de control DataGrid
- tipos de control, patrones de control para el tipo de control DataGrid
- tipos de control, compatibilidad con DataGrid
- tipos de control, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8af1e35e062c778285d1cb7edcca9ac6192792b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994163"
---
# <a name="datagrid-control-type"></a><span data-ttu-id="4179f-119">DataGrid (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="4179f-119">DataGrid Control Type</span></span>

<span data-ttu-id="4179f-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="4179f-120">This topic provides information about Microsoft UI Automation support for the **DataGrid** control type.</span></span>

<span data-ttu-id="4179f-121">El tipo de control **DataGrid** permite a un usuario trabajar fácilmente con elementos que contienen datos o elementos de automatización presentados en columnas o filas.</span><span class="sxs-lookup"><span data-stu-id="4179f-121">The **DataGrid** control type lets a user easily work with items that contain data or automation elements presented in columns or rows.</span></span> <span data-ttu-id="4179f-122">Los controles de cuadrícula de datos tienen filas de elementos y columnas de información sobre esos elementos.</span><span class="sxs-lookup"><span data-stu-id="4179f-122">Data grid controls have rows of items and columns of information about those items.</span></span> <span data-ttu-id="4179f-123">Un control de vista de lista en el explorador de Windows Vista es un ejemplo que admite el tipo de control **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="4179f-123">A list-view control in Windows Vista Explorer is an example that supports the **DataGrid** control type.</span></span>

<span data-ttu-id="4179f-124">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="4179f-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataGrid** control type.</span></span> <span data-ttu-id="4179f-125">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de cuadrícula de datos donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y los patrones</span><span class="sxs-lookup"><span data-stu-id="4179f-125">The UI Automation requirements apply to all data grid controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="4179f-126">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="4179f-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4179f-127">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="4179f-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="4179f-128">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="4179f-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="4179f-129">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="4179f-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="4179f-130">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="4179f-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="4179f-131">Ejemplo de tipo de control DataGrid</span><span class="sxs-lookup"><span data-stu-id="4179f-131">DataGrid Control Type Example</span></span>](#datagrid-control-type-example)
-   [<span data-ttu-id="4179f-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4179f-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="4179f-133">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="4179f-133">Typical Tree Structure</span></span>

<span data-ttu-id="4179f-134">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de cuadrícula de datos y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="4179f-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to data grid controls and describes what can be contained in each view.</span></span> <span data-ttu-id="4179f-135">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4179f-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4179f-136">Vista de control</span><span class="sxs-lookup"><span data-stu-id="4179f-136">Control View</span></span></th>
<th><span data-ttu-id="4179f-137">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="4179f-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4179f-138">DataGrid</span><span class="sxs-lookup"><span data-stu-id="4179f-138">DataGrid</span></span>
<ul>
<li><span data-ttu-id="4179f-139">Header (0, 1 o 2)</span><span class="sxs-lookup"><span data-stu-id="4179f-139">Header (0, 1, or 2)</span></span>
<ul>
<li><span data-ttu-id="4179f-140">HeaderItem (número de columnas o filas)</span><span class="sxs-lookup"><span data-stu-id="4179f-140">HeaderItem (number of columns or rows)</span></span></li>
</ul></li>
<li><span data-ttu-id="4179f-141">DataItem (0 o más; se puede estructurar en una jerarquía)</span><span class="sxs-lookup"><span data-stu-id="4179f-141">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4179f-142">DataGrid</span><span class="sxs-lookup"><span data-stu-id="4179f-142">DataGrid</span></span>
<ul>
<li><span data-ttu-id="4179f-143">DataItem (0 o más; se puede estructurar en una jerarquía)</span><span class="sxs-lookup"><span data-stu-id="4179f-143">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="4179f-144">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="4179f-144">Relevant Properties</span></span>

<span data-ttu-id="4179f-145">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="4179f-145">The following table lists the UI Automation properties whose value or definition is especially relevant to the **DataGrid** control type.</span></span> <span data-ttu-id="4179f-146">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="4179f-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="4179f-147">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="4179f-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="4179f-148">Value</span><span class="sxs-lookup"><span data-stu-id="4179f-148">Value</span></span>        | <span data-ttu-id="4179f-149">Notas</span><span class="sxs-lookup"><span data-stu-id="4179f-149">Notes</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4179f-150">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4179f-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="4179f-151">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4179f-151">See notes.</span></span>   | <span data-ttu-id="4179f-152">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4179f-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="4179f-153">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4179f-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="4179f-154">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4179f-154">See notes.</span></span>   | <span data-ttu-id="4179f-155">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="4179f-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="4179f-156">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4179f-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="4179f-157">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4179f-157">See notes.</span></span>   | <span data-ttu-id="4179f-158">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="4179f-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="4179f-159">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="4179f-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                         |
| [<span data-ttu-id="4179f-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4179f-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="4179f-161">**DataGrid**</span><span class="sxs-lookup"><span data-stu-id="4179f-161">**DataGrid**</span></span> |                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="4179f-162">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4179f-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4179f-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="4179f-163">TRUE</span></span>         | <span data-ttu-id="4179f-164">El valor de esta propiedad siempre debe ser **true**.</span><span class="sxs-lookup"><span data-stu-id="4179f-164">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="4179f-165">Esto significa que el control de cuadrícula de datos siempre debe estar en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4179f-165">This means that the data grid control must always be in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="4179f-166">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4179f-166">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4179f-167">TRUE</span><span class="sxs-lookup"><span data-stu-id="4179f-167">TRUE</span></span>         | <span data-ttu-id="4179f-168">El valor de esta propiedad siempre debe ser **true**.</span><span class="sxs-lookup"><span data-stu-id="4179f-168">The value of this property must always **TRUE**.</span></span> <span data-ttu-id="4179f-169">Esto significa que el control de cuadrícula de datos siempre debe estar incluido en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4179f-169">This means that the data grid control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                                                |
| [<span data-ttu-id="4179f-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4179f-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="4179f-171">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4179f-171">See notes.</span></span>   | <span data-ttu-id="4179f-172">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4179f-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="4179f-173">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4179f-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="4179f-174">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4179f-174">See notes.</span></span>   | <span data-ttu-id="4179f-175">Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.</span><span class="sxs-lookup"><span data-stu-id="4179f-175">If there is a static text label, this property must expose a reference to that control.</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="4179f-176">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4179f-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="4179f-177">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4179f-177">See notes.</span></span>   | <span data-ttu-id="4179f-178">Cadena localizada que corresponde al tipo de control **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="4179f-178">Localized string corresponding to the **DataGrid** control type.</span></span> <span data-ttu-id="4179f-179">El valor predeterminado es "Data Grid" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="4179f-179">The default value is "data grid" for en-US or English (United States).</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="4179f-180">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4179f-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="4179f-181">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="4179f-181">See notes.</span></span>   | <span data-ttu-id="4179f-182">Normalmente, el control de cuadrícula de datos obtiene el valor de su propiedad **Name** de una etiqueta de texto estático.</span><span class="sxs-lookup"><span data-stu-id="4179f-182">The data grid control typically gets the value for its **Name** property from a static text label.</span></span> <span data-ttu-id="4179f-183">Si no hay una etiqueta de texto estático, un desarrollador de aplicaciones debe asignar un valor a para la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="4179f-183">If there is not a static text label an application developer must assign a value to for the **Name** property.</span></span> <span data-ttu-id="4179f-184">El valor de la propiedad **Name** nunca debe ser el contenido textual del control de edición.</span><span class="sxs-lookup"><span data-stu-id="4179f-184">The value of the **Name** property must never be the textual contents of the edit control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="4179f-185">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="4179f-185">Required Control Patterns</span></span>

<span data-ttu-id="4179f-186">En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de cuadrícula de datos.</span><span class="sxs-lookup"><span data-stu-id="4179f-186">The following table lists the UI Automation control patterns required to be supported by all data grid controls.</span></span> <span data-ttu-id="4179f-187">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4179f-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="4179f-188">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="4179f-188">Control Pattern</span></span>                                         | <span data-ttu-id="4179f-189">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="4179f-189">Support</span></span>  | <span data-ttu-id="4179f-190">Notas</span><span class="sxs-lookup"><span data-stu-id="4179f-190">Notes</span></span>                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4179f-191">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="4179f-191">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="4179f-192">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4179f-192">Required</span></span> | <span data-ttu-id="4179f-193">El propio control de cuadrícula de datos siempre admite el patrón de control [Grid](uiauto-implementinggrid.md) porque los elementos que contiene tienen metadatos que se colocan en una cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="4179f-193">The data grid control itself always supports the [Grid](uiauto-implementinggrid.md) control pattern because the items that it contains have metadata that is laid out in a grid.</span></span> |
| [<span data-ttu-id="4179f-194">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="4179f-194">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="4179f-195">Depende</span><span class="sxs-lookup"><span data-stu-id="4179f-195">Depends</span></span>  | <span data-ttu-id="4179f-196">La capacidad de desplazar la cuadrícula de datos depende del contenido y de si las barras de desplazamiento están presentes.</span><span class="sxs-lookup"><span data-stu-id="4179f-196">The ability to scroll the data grid depends on content and whether scroll bars are present.</span></span>                                                                                       |
| [<span data-ttu-id="4179f-197">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="4179f-197">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | <span data-ttu-id="4179f-198">Depende</span><span class="sxs-lookup"><span data-stu-id="4179f-198">Depends</span></span>  | <span data-ttu-id="4179f-199">La capacidad de seleccionar la cuadrícula de datos depende del contenido.</span><span class="sxs-lookup"><span data-stu-id="4179f-199">The ability to select the data grid depends on content.</span></span>                                                                                                                           |
| [<span data-ttu-id="4179f-200">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="4179f-200">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="4179f-201">Depende</span><span class="sxs-lookup"><span data-stu-id="4179f-201">Depends</span></span>  | <span data-ttu-id="4179f-202">Un control de cuadrícula de datos que tiene un encabezado debe admitir el patrón de control [TABLE](uiauto-implementingtable.md) .</span><span class="sxs-lookup"><span data-stu-id="4179f-202">A data grid control that has a header should support the [Table](uiauto-implementingtable.md) control pattern.</span></span>                                                                   |



 

<span data-ttu-id="4179f-203">Los elementos de datos dentro de los contenedores de la cuadrícula de datos admitirán como mínimo:</span><span class="sxs-lookup"><span data-stu-id="4179f-203">Data items within the data grid containers will support at a minimum:</span></span>

-   <span data-ttu-id="4179f-204">Patrón de control [SelectionItem](uiauto-implementingselectionitem.md) (si la cuadrícula de datos es seleccionable)</span><span class="sxs-lookup"><span data-stu-id="4179f-204">[SelectionItem](uiauto-implementingselectionitem.md) control pattern (if the data grid is selectable)</span></span>
-   <span data-ttu-id="4179f-205">Patrón de control [ScrollItem](uiauto-implementingscrollitem.md) (si la cuadrícula de datos es desplazable)</span><span class="sxs-lookup"><span data-stu-id="4179f-205">[ScrollItem](uiauto-implementingscrollitem.md) control pattern (if the data grid is scrollable)</span></span>
-   <span data-ttu-id="4179f-206">[GridItem](uiauto-implementinggriditem.md) (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="4179f-206">[GridItem](uiauto-implementinggriditem.md) control pattern</span></span>
-   <span data-ttu-id="4179f-207">Patrón de control [TableItem](uiauto-implementingtableitem.md) (si la cuadrícula de datos tiene un encabezado)</span><span class="sxs-lookup"><span data-stu-id="4179f-207">[TableItem](uiauto-implementingtableitem.md) control pattern (if the data grid has a header)</span></span>

## <a name="required-events"></a><span data-ttu-id="4179f-208">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="4179f-208">Required Events</span></span>

<span data-ttu-id="4179f-209">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de cuadrícula de datos deben admitir.</span><span class="sxs-lookup"><span data-stu-id="4179f-209">The following table lists the UI Automation events that data grid controls are required to support.</span></span> <span data-ttu-id="4179f-210">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4179f-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="4179f-211">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="4179f-211">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="4179f-212">Notas</span><span class="sxs-lookup"><span data-stu-id="4179f-212">Notes</span></span>                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4179f-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4179f-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| <span data-ttu-id="4179f-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4179f-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                                                          |
| <span data-ttu-id="4179f-215">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4179f-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="4179f-216">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="4179f-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                                 |
| <span data-ttu-id="4179f-217">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4179f-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="4179f-218">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="4179f-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                               |
| [<span data-ttu-id="4179f-219">**UIA \_ LayoutInvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="4179f-219">**UIA\_LayoutInvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [<span data-ttu-id="4179f-220">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4179f-220">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| <span data-ttu-id="4179f-221">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de MultipleViewCurrentViewPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4179f-221">[**UIA\_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>             | <span data-ttu-id="4179f-222">Si el control admite la propiedad CurrentView del patrón de control [MultipleView](uiauto-implementingmultipleview.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="4179f-222">If the control supports the CurrentView property of the [MultipleView](uiauto-implementingmultipleview.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="4179f-223">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4179f-223">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="4179f-224">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="4179f-224">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="4179f-225">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4179f-225">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="4179f-226">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="4179f-226">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="4179f-227">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4179f-227">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="4179f-228">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="4179f-228">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="4179f-229">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4179f-229">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="4179f-230">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="4179f-230">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="4179f-231">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4179f-231">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="4179f-232">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="4179f-232">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="4179f-233">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4179f-233">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="4179f-234">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="4179f-234">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| [<span data-ttu-id="4179f-235">**\_InvalidatedEventId de selección de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="4179f-235">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a><span data-ttu-id="4179f-236">Ejemplo de tipo de control DataGrid</span><span class="sxs-lookup"><span data-stu-id="4179f-236">DataGrid Control Type Example</span></span>

<span data-ttu-id="4179f-237">En la imagen siguiente se muestra un control de vista de lista que implementa el tipo de control **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="4179f-237">The following image illustrates a list-view control that implements the **DataGrid** control type.</span></span>

![captura de pantalla del control de vista de lista con el tipo de control DataGrid](images/datagridxmpl.jpg)

<span data-ttu-id="4179f-239">A continuación se muestra la vista de control y la vista de contenido del árbol de automatización de la interfaz de usuario que pertenece al control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="4179f-239">The control view and the content view of the UI Automation tree that pertains to the list-view control is displayed below.</span></span> <span data-ttu-id="4179f-240">Los patrones de control de cada elemento de automatización se muestran entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="4179f-240">The control patterns for each automation element are shown in parentheses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4179f-241">Árbol de automatización de la interfaz de usuario (vista de control)</span><span class="sxs-lookup"><span data-stu-id="4179f-241">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="4179f-242">Árbol de UI Automation: vista de contenido</span><span class="sxs-lookup"><span data-stu-id="4179f-242">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4179f-243">DataGrid (ordenar, tabla, selección, cuadrícula)</span><span class="sxs-lookup"><span data-stu-id="4179f-243">DataGrid (Sort, Table, Selection, Grid)</span></span>
<ul>
<li><span data-ttu-id="4179f-244">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4179f-244">Header</span></span>
<ul>
<li><span data-ttu-id="4179f-245">Nombre de HeaderItem &quot; &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="4179f-245">HeaderItem &quot;Name&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="4179f-246">HeaderItem &quot; fecha de modificación &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="4179f-246">HeaderItem &quot;Date Modified&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="4179f-247">Tamaño de HeaderItem &quot; &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="4179f-247">HeaderItem &quot;Size&quot; (Invoke)</span></span></li>
</ul></li>
<li><span data-ttu-id="4179f-248">Grupo &quot; contoso &quot; (TableItem, GridItem, SelectionItem, TABLE *, Grid*)</span><span class="sxs-lookup"><span data-stu-id="4179f-248">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="4179f-249">&quot;Receivable.doc&quot; de cuentas de DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="4179f-249">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="4179f-250">&quot;Payable.doc&quot; de cuentas de DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="4179f-250">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="4179f-251">DataGrid (Table, Grid, Selection)</span><span class="sxs-lookup"><span data-stu-id="4179f-251">DataGrid (Table, Grid, Selection)</span></span>
<ul>
<li><span data-ttu-id="4179f-252">Grupo &quot; contoso &quot; (TableItem, GridItem, SelectionItem, TABLE *, Grid*)</span><span class="sxs-lookup"><span data-stu-id="4179f-252">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="4179f-253">&quot;Receivable.doc&quot; de cuentas de DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="4179f-253">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="4179f-254">&quot;Payable.doc&quot; de cuentas de DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="4179f-254">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4179f-255">\*En el ejemplo anterior se muestra una cuadrícula de datos que contiene varios niveles de controles.</span><span class="sxs-lookup"><span data-stu-id="4179f-255">\*The preceding example shows a data grid that contains multiple levels of controls.</span></span> <span data-ttu-id="4179f-256">El control **Group** ("Contoso") contiene dos controles **DataItem** ("accounts Receivable.doc" y "accounts Payable.doc").</span><span class="sxs-lookup"><span data-stu-id="4179f-256">The **Group** ("Contoso") control contains two **DataItem** controls ("Accounts Receivable.doc" and "Accounts Payable.doc").</span></span> <span data-ttu-id="4179f-257">Un par **DataGrid** / **GridItem** es independiente de un par en otro nivel.</span><span class="sxs-lookup"><span data-stu-id="4179f-257">A **DataGrid**/**GridItem** pair is independent of a pair at another level.</span></span> <span data-ttu-id="4179f-258">Los controles **DataItem** de un **Grupo** también se pueden exponer como un tipo de control [ListItem](uiauto-supportlistitemcontroltype.md) , lo que permite que se presenten más claramente como objetos seleccionables, en lugar de como elementos de datos simples.</span><span class="sxs-lookup"><span data-stu-id="4179f-258">The **DataItem** controls under a **Group** can also be exposed as a [ListItem](uiauto-supportlistitemcontroltype.md) control type, enabling them to be presented more clearly as selectable objects, rather than as simple data elements.</span></span> <span data-ttu-id="4179f-259">En este ejemplo no se incluyen los subelementos de los elementos de datos agrupados.</span><span class="sxs-lookup"><span data-stu-id="4179f-259">This example does not include the sub-elements of the grouped data items.</span></span> <span data-ttu-id="4179f-260">Para obtener otro ejemplo de varios niveles de controles, vea el tipo de control [DataItem](uiauto-supportdataitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="4179f-260">For another example of multiple levels of controls, see the [DataItem](uiauto-supportdataitemcontroltype.md) control type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4179f-261">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4179f-261">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4179f-262">**Vista**</span><span class="sxs-lookup"><span data-stu-id="4179f-262">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4179f-263">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4179f-263">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="4179f-264">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="4179f-264">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




