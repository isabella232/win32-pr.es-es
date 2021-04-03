---
title: DataItem (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control DataItem.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control DataItem
- Automatización de la interfaz de usuario, tipo de control DataItem
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control DataItem
- UI Automation, propiedades para el tipo de control DataItem
- Automatización de la interfaz de usuario, patrones de control para el tipo de control DataItem
- Automatización de la interfaz de usuario, eventos para el tipo de control DataItem
- Automatización de la interfaz de usuario, listas grandes y tipo de control DataItem
- estructuras de árbol, tipo de control DataItem
- Properties, DataItem (tipo de control)
- patrones de control, tipo de control DataItem
- Events, DataItem (tipo de control)
- listas grandes
- compatibilidad con el tipo de control DataItem
- DataItem (tipo de control)
- tipos de control, estructura de árbol para el tipo de control DataItem
- tipos de control, patrones de control para el tipo de control DataItem
- tipos de control, listas grandes y tipo de control DataItem
- tipos de control, compatibilidad con DataItem
- tipos de control, DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0902cc593ec7f9104ed27031caa2785b7cb9756
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075617"
---
# <a name="dataitem-control-type"></a><span data-ttu-id="0c208-122">DataItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="0c208-122">DataItem Control Type</span></span>

<span data-ttu-id="0c208-123">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="0c208-123">This topic provides information about Microsoft UI Automation support for the **DataItem** control type.</span></span>

<span data-ttu-id="0c208-124">Una entrada de una lista de contactos es un ejemplo de un control de elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="0c208-124">An entry in a Contacts list is an example of a data item control.</span></span> <span data-ttu-id="0c208-125">Un control de elemento de datos contiene información de interés para un usuario final.</span><span class="sxs-lookup"><span data-stu-id="0c208-125">A data item control contains information that is of interest to an end user.</span></span> <span data-ttu-id="0c208-126">Es más complicado que el elemento de lista simple porque contiene información más completa.</span><span class="sxs-lookup"><span data-stu-id="0c208-126">It is more complicated than the simple list item because it contains richer information.</span></span>

<span data-ttu-id="0c208-127">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="0c208-127">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataItem** control type.</span></span> <span data-ttu-id="0c208-128">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de elemento de datos donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y los patrones</span><span class="sxs-lookup"><span data-stu-id="0c208-128">The UI Automation requirements apply to all data item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="0c208-129">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="0c208-129">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0c208-130">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="0c208-130">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="0c208-131">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="0c208-131">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="0c208-132">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="0c208-132">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="0c208-133">Trabajar con elementos de trabajo en listas grandes</span><span class="sxs-lookup"><span data-stu-id="0c208-133">Working with DataItems in Large Lists</span></span>](#working-with-dataitems-in-large-lists)
-   [<span data-ttu-id="0c208-134">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="0c208-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="0c208-135">Ejemplo de tipo de control DataItem</span><span class="sxs-lookup"><span data-stu-id="0c208-135">DataItem Control Type Example</span></span>](#dataitem-control-type-example)
-   [<span data-ttu-id="0c208-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0c208-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="0c208-137">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="0c208-137">Typical Tree Structure</span></span>

<span data-ttu-id="0c208-138">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de elemento de datos y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="0c208-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to data item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="0c208-139">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0c208-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c208-140">Vista de control</span><span class="sxs-lookup"><span data-stu-id="0c208-140">Control View</span></span></th>
<th><span data-ttu-id="0c208-141">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="0c208-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="0c208-142">DataItem</span><span class="sxs-lookup"><span data-stu-id="0c208-142">DataItem</span></span>
<ul>
<li><span data-ttu-id="0c208-143">Varía (0 o más; se puede estructurar en jerarquía)</span><span class="sxs-lookup"><span data-stu-id="0c208-143">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0c208-144">DataItem</span><span class="sxs-lookup"><span data-stu-id="0c208-144">DataItem</span></span>
<ul>
<li><span data-ttu-id="0c208-145">Varía (0 o más; se puede estructurar en jerarquía)</span><span class="sxs-lookup"><span data-stu-id="0c208-145">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0c208-146">Un elemento de datos de una cuadrícula de datos puede hospedar diversos objetos, entre los que se incluye otra capa de elementos de datos o elementos de cuadrícula concretos como controles de edición, texto o imágenes.</span><span class="sxs-lookup"><span data-stu-id="0c208-146">A data item element in a data grid can host a variety of objects, including another layer of data items, or specific grid elements such as text, images, or edit controls.</span></span> <span data-ttu-id="0c208-147">Si el elemento de datos tiene un rol de objeto concreto, el elemento debe exponerse como un tipo de control concreto; por ejemplo, un tipo de control [ListItem](uiauto-supportlistitemcontroltype.md) para un elemento de datos seleccionable de la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="0c208-147">If the data item element has a specific object role, the element should be exposed as a specific control type; for example, a [ListItem](uiauto-supportlistitemcontroltype.md) control type for a selectable data item in the grid.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="0c208-148">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="0c208-148">Relevant Properties</span></span>

<span data-ttu-id="0c208-149">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control DataItem.</span><span class="sxs-lookup"><span data-stu-id="0c208-149">The following table lists the UI Automation properties whose value or definition is especially relevant to the DataItem control type.</span></span> <span data-ttu-id="0c208-150">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="0c208-150">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="0c208-151">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="0c208-151">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="0c208-152">Value</span><span class="sxs-lookup"><span data-stu-id="0c208-152">Value</span></span>        | <span data-ttu-id="0c208-153">Notas</span><span class="sxs-lookup"><span data-stu-id="0c208-153">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c208-154">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0c208-154">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="0c208-155">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="0c208-155">See notes.</span></span>   | <span data-ttu-id="0c208-156">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0c208-156">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="0c208-157">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0c208-157">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="0c208-158">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="0c208-158">See notes.</span></span>   | <span data-ttu-id="0c208-159">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="0c208-159">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="0c208-160">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0c208-160">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="0c208-161">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="0c208-161">See notes.</span></span>   | <span data-ttu-id="0c208-162">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="0c208-162">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="0c208-163">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="0c208-163">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="0c208-164">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0c208-164">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="0c208-165">**DataItem**</span><span class="sxs-lookup"><span data-stu-id="0c208-165">**DataItem**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="0c208-166">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0c208-166">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0c208-167">TRUE</span><span class="sxs-lookup"><span data-stu-id="0c208-167">TRUE</span></span>         | <span data-ttu-id="0c208-168">El control de elemento de datos siempre debe ser contenido.</span><span class="sxs-lookup"><span data-stu-id="0c208-168">The data item control must always be content.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="0c208-169">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0c208-169">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0c208-170">TRUE</span><span class="sxs-lookup"><span data-stu-id="0c208-170">TRUE</span></span>         | <span data-ttu-id="0c208-171">El control de elemento de datos siempre debe ser un control.</span><span class="sxs-lookup"><span data-stu-id="0c208-171">The data item control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="0c208-172">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0c208-172">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="0c208-173">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="0c208-173">See notes.</span></span>   | <span data-ttu-id="0c208-174">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0c208-174">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="0c208-175">**UIA \_ ItemStatusPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0c208-175">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="0c208-176">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="0c208-176">See notes.</span></span>   | <span data-ttu-id="0c208-177">Si el control contiene un estado que se está actualizando dinámicamente, se debe admitir esta propiedad para que una tecnología de asistencia pueda recibir actualizaciones cuando cambie el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="0c208-177">If the control contains status that is being updated dynamically, this property must be supported so that an assistive technology can receive updates when the status of the element changes.</span></span>        |
| [<span data-ttu-id="0c208-178">**UIA \_ ItemTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0c208-178">**UIA\_ItemTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="0c208-179">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="0c208-179">See notes.</span></span>   | <span data-ttu-id="0c208-180">Este es el valor de cadena que transmite al usuario final el objeto subyacente que representa el elemento.</span><span class="sxs-lookup"><span data-stu-id="0c208-180">This is the string value that conveys to the end user the underlying object that the item represents.</span></span> <span data-ttu-id="0c208-181">Algunos ejemplos son "archivo multimedia" y "contacto".</span><span class="sxs-lookup"><span data-stu-id="0c208-181">Examples include "Media File" and "Contact".</span></span>                                                   |
| [<span data-ttu-id="0c208-182">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0c208-182">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="0c208-183">Null</span><span class="sxs-lookup"><span data-stu-id="0c208-183">Null</span></span>         | <span data-ttu-id="0c208-184">Los controles de elemento de datos no tienen una etiqueta de texto estático.</span><span class="sxs-lookup"><span data-stu-id="0c208-184">Data item controls do not have a static text label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="0c208-185">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0c208-185">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="0c208-186">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="0c208-186">See notes.</span></span>   | <span data-ttu-id="0c208-187">Cadena localizada que corresponde al tipo de control **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="0c208-187">Localized string corresponding to the **DataItem** control type.</span></span> <span data-ttu-id="0c208-188">El valor predeterminado es "Data Item" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="0c208-188">The default value is "data item" for en-US or English (United States).</span></span>                                                              |
| [<span data-ttu-id="0c208-189">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0c208-189">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="0c208-190">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="0c208-190">See notes.</span></span>   | <span data-ttu-id="0c208-191">El control de elemento de datos siempre contiene un elemento de texto principal que el usuario reconocerá como el identificador del elemento.</span><span class="sxs-lookup"><span data-stu-id="0c208-191">The data item control always contains a primary text element that the user would recognize as the identifier for the item.</span></span>                                                                           |



 

## <a name="required-control-patterns"></a><span data-ttu-id="0c208-192">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="0c208-192">Required Control Patterns</span></span>

<span data-ttu-id="0c208-193">En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="0c208-193">The following table lists the UI Automation control patterns required to be supported by all data item controls.</span></span> <span data-ttu-id="0c208-194">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0c208-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="0c208-195">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="0c208-195">Control Pattern</span></span>                                                   | <span data-ttu-id="0c208-196">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0c208-196">Support</span></span> | <span data-ttu-id="0c208-197">Notas</span><span class="sxs-lookup"><span data-stu-id="0c208-197">Notes</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c208-198">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="0c208-198">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="0c208-199">Depende</span><span class="sxs-lookup"><span data-stu-id="0c208-199">Depends</span></span> | <span data-ttu-id="0c208-200">Si el elemento de datos se puede expandir o contraer para mostrar u ocultar información, se debe admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="0c208-200">If the data item can be expanded or collapsed to show and hide information, the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern must be supported.</span></span>                                            |
| [<span data-ttu-id="0c208-201">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="0c208-201">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | <span data-ttu-id="0c208-202">Depende</span><span class="sxs-lookup"><span data-stu-id="0c208-202">Depends</span></span> | <span data-ttu-id="0c208-203">Los elementos de datos admitirán el patrón de control [GridItem](uiauto-implementinggriditem.md) cuando una colección de elementos de datos está disponible dentro de un contenedor que se puede navegar espacialmente de elemento a elemento.</span><span class="sxs-lookup"><span data-stu-id="0c208-203">Data items will support the [GridItem](uiauto-implementinggriditem.md) control pattern when a collection of data items is available within a container that can be spatially navigated item-to-item.</span></span>                 |
| [<span data-ttu-id="0c208-204">**IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="0c208-204">**IScrollItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | <span data-ttu-id="0c208-205">Depende</span><span class="sxs-lookup"><span data-stu-id="0c208-205">Depends</span></span> | <span data-ttu-id="0c208-206">Todos los elementos de datos admiten la posibilidad de desplazarse en la vista con el patrón de control [ScrollItem](uiauto-implementingscrollitem.md) cuando su contenedor de datos tiene más elementos de los que caben en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="0c208-206">All data items support the ability to be scrolled into view with the [ScrollItem](uiauto-implementingscrollitem.md) control pattern when their data container has more items than can fit on the screen.</span></span>             |
| [<span data-ttu-id="0c208-207">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="0c208-207">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | <span data-ttu-id="0c208-208">Depende</span><span class="sxs-lookup"><span data-stu-id="0c208-208">Depends</span></span> | <span data-ttu-id="0c208-209">La capacidad de seleccionar los elementos de datos depende del contenido.</span><span class="sxs-lookup"><span data-stu-id="0c208-209">The ability to select the data items depends on the content.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="0c208-210">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="0c208-210">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | <span data-ttu-id="0c208-211">Depende</span><span class="sxs-lookup"><span data-stu-id="0c208-211">Depends</span></span> | <span data-ttu-id="0c208-212">Si el elemento de datos está contenido dentro de un tipo de control [DataGrid](uiauto-supportdatagridcontroltype.md) que tiene un elemento header, debe admitir el patrón de control [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="0c208-212">If the data item is contained within a [DataGrid](uiauto-supportdatagridcontroltype.md) control type that has a header element, it should support the [TableItem](uiauto-implementingtableitem.md) control pattern.</span></span> |
| [<span data-ttu-id="0c208-213">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="0c208-213">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="0c208-214">Depende</span><span class="sxs-lookup"><span data-stu-id="0c208-214">Depends</span></span> | <span data-ttu-id="0c208-215">Si el elemento de datos contiene un estado que se puede recorrer, debe admitir el patrón de control [Toggle](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="0c208-215">If the data item contains a state that can be cycled through, it should support the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span>                                                                          |
| [<span data-ttu-id="0c208-216">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="0c208-216">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | <span data-ttu-id="0c208-217">Depende</span><span class="sxs-lookup"><span data-stu-id="0c208-217">Depends</span></span> | <span data-ttu-id="0c208-218">Si el texto primario del elemento de datos es editable, se debe admitir el patrón de control [Value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="0c208-218">If the data item's primary text is editable, the [Value](uiauto-implementingvalue.md) control pattern must be supported.</span></span>                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a><span data-ttu-id="0c208-219">Trabajar con elementos de trabajo en listas grandes</span><span class="sxs-lookup"><span data-stu-id="0c208-219">Working with DataItems in Large Lists</span></span>

<span data-ttu-id="0c208-220">Dado que las listas grandes suelen virtualizarse en marcos de interfaz de usuario para ayudar en el rendimiento, un cliente de automatización de la interfaz de usuario no puede usar la característica de consulta de automatización de la interfaz de usuario para buscar el contenido del árbol completo de la misma manera que en otros contenedores de elementos.</span><span class="sxs-lookup"><span data-stu-id="0c208-220">Because large lists are often virtualized within UI frameworks to assist in performance, a UI Automation client cannot use the UI Automation query feature to search the contents of the full tree in the same way that it can in other item containers.</span></span> <span data-ttu-id="0c208-221">Un cliente debe desplazar el elemento a la vista (o expandir el control para mostrar todas las opciones disponibles) antes de obtener acceso al conjunto completo de información del elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="0c208-221">A client should scroll the item into view (or expand the control to show all available options) prior to accessing the full set of information from the data item.</span></span>

<span data-ttu-id="0c208-222">Al llamar a [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) en el elemento de automatización de la interfaz de usuario para el elemento de datos, el explorador de Microsoft Windows vuelve correctamente y hace que el foco se establezca en el control de edición dentro del subárbol del elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="0c208-222">When calling [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on the UI Automation element for the data item, Microsoft Windows Explorer returns successfully and causes focus to be set to the Edit control within the data item subtree.</span></span>

## <a name="required-events"></a><span data-ttu-id="0c208-223">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="0c208-223">Required Events</span></span>

<span data-ttu-id="0c208-224">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de elemento de datos deben admitir.</span><span class="sxs-lookup"><span data-stu-id="0c208-224">The following table lists the UI Automation events that data item controls are required to support.</span></span> <span data-ttu-id="0c208-225">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0c208-225">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="0c208-226">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="0c208-226">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="0c208-227">Notas</span><span class="sxs-lookup"><span data-stu-id="0c208-227">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c208-228">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="0c208-228">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="0c208-229">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c208-229">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="0c208-230">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c208-230">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="0c208-231">Si el control admite el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="0c208-231">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="0c208-232">**\_InvokedEventId de invocación de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="0c208-232">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  | <span data-ttu-id="0c208-233">Si el control admite el patrón de control [Invoke](uiauto-implementinginvoke.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="0c208-233">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="0c208-234">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c208-234">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="0c208-235">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="0c208-235">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="0c208-236">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c208-236">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="0c208-237">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="0c208-237">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="0c208-238">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de ItemStatusPropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c208-238">[**UIA\_ItemStatusPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                            | <span data-ttu-id="0c208-239">Si el control admite la propiedad [**ItemStatus**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="0c208-239">If the control supports the [**ItemStatus**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>        |
| <span data-ttu-id="0c208-240">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de NamePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c208-240">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                                        |                                                                                                                                  |
| [<span data-ttu-id="0c208-241">**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="0c208-241">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)                                    | <span data-ttu-id="0c208-242">Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="0c208-242">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="0c208-243">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="0c208-243">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="0c208-244">Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="0c208-244">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="0c208-245">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="0c208-245">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                                                    | <span data-ttu-id="0c208-246">Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="0c208-246">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="0c208-247">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="0c208-247">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| <span data-ttu-id="0c208-248">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c208-248">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="0c208-249">Si el control admite el patrón de control [Toggle](uiauto-implementingtoggle.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="0c208-249">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="0c208-250">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="0c208-250">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                               | <span data-ttu-id="0c208-251">Si el control admite el patrón de control [Value](uiauto-implementingvalue.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="0c208-251">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>                   |



 

## <a name="dataitem-control-type-example"></a><span data-ttu-id="0c208-252">Ejemplo de tipo de control DataItem</span><span class="sxs-lookup"><span data-stu-id="0c208-252">DataItem Control Type Example</span></span>

<span data-ttu-id="0c208-253">En la imagen siguiente se muestra un tipo de control DataItem en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="0c208-253">The following image illustrates a DataItem control type in a list-view control.</span></span>

![captura de pantalla del control de vista de lista con el tipo de control DataItem](images/dataitemxmpl.jpg)

<span data-ttu-id="0c208-255">A continuación se muestra la vista de control y la vista de contenido del árbol de automatización de la interfaz de usuario que pertenece al control de elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="0c208-255">The control view and the content view of the UI Automation tree that pertains to the data item control is displayed below.</span></span> <span data-ttu-id="0c208-256">Los patrones de control de cada elemento de automatización se muestran entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="0c208-256">The control patterns for each automation element are shown in parentheses.</span></span> <span data-ttu-id="0c208-257">El **Grupo** "Contoso" también forma parte de la cuadrícula del control host de la cuadrícula de datos.</span><span class="sxs-lookup"><span data-stu-id="0c208-257">The **Group** "Contoso" is also part of the grid of the data grid host control.</span></span> <span data-ttu-id="0c208-258">Para obtener un ejemplo de una estructura de cuadrícula de nivel superior, vea [DataGrid (tipo de control](uiauto-supportdatagridcontroltype.md)).</span><span class="sxs-lookup"><span data-stu-id="0c208-258">For an example of a higher level grid structure, see [DataGrid Control Type](uiauto-supportdatagridcontroltype.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c208-259">Árbol de automatización de la interfaz de usuario (vista de control)</span><span class="sxs-lookup"><span data-stu-id="0c208-259">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="0c208-260">Árbol de UI Automation: vista de contenido</span><span class="sxs-lookup"><span data-stu-id="0c208-260">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="0c208-261">Grupo &quot; contoso &quot; (tabla, cuadrícula)</span><span class="sxs-lookup"><span data-stu-id="0c208-261">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="0c208-262">&quot;Receivable.doc&quot; de cuentas de DataItem (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="0c208-262">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="0c208-263">Cuentas de imagen &quot; Receivable.doc&quot;</span><span class="sxs-lookup"><span data-stu-id="0c208-263">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="0c208-264">Editar &quot; nombre &quot; (TableItem, GridItem, cuentas de valor &quot; Receivable.doc&quot; )</span><span class="sxs-lookup"><span data-stu-id="0c208-264">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="0c208-265">Editar &quot; fecha &quot; de modificación (TableItem, GridItem, valor &quot; 8/25/2006 3:29 PM &quot; )</span><span class="sxs-lookup"><span data-stu-id="0c208-265">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="0c208-266">Editar &quot; tamaño &quot; (GridItem, TableItem, valor &quot; 11,0 KB &quot; )</span><span class="sxs-lookup"><span data-stu-id="0c208-266">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="0c208-267">&quot;Payable.doc&quot; de cuentas de DataItem (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="0c208-267">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="0c208-268">...</span><span class="sxs-lookup"><span data-stu-id="0c208-268">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0c208-269">Grupo &quot; contoso &quot; (tabla, cuadrícula)</span><span class="sxs-lookup"><span data-stu-id="0c208-269">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="0c208-270">&quot;Receivable.doc&quot; de cuentas de DataItem (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="0c208-270">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="0c208-271">Cuentas de imagen &quot; Receivable.doc&quot;</span><span class="sxs-lookup"><span data-stu-id="0c208-271">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="0c208-272">Editar &quot; nombre &quot; (TableItem, GridItem, cuentas de valor &quot; Receivable.doc&quot; )</span><span class="sxs-lookup"><span data-stu-id="0c208-272">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="0c208-273">Editar &quot; fecha &quot; de modificación (TableItem, GridItem, valor &quot; 8/25/2006 3:29 PM &quot; )</span><span class="sxs-lookup"><span data-stu-id="0c208-273">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="0c208-274">Editar &quot; tamaño &quot; (GridItem, TableItem, valor &quot; 11,0 KB &quot; )</span><span class="sxs-lookup"><span data-stu-id="0c208-274">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="0c208-275">&quot;Payable.doc&quot; de cuentas de DataItem (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="0c208-275">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="0c208-276">...</span><span class="sxs-lookup"><span data-stu-id="0c208-276">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0c208-277">Si una cuadrícula representa una lista de elementos seleccionables, los elementos de la interfaz de usuario seleccionables correspondientes se pueden exponer con el tipo de control [ListItem](uiauto-supportlistitemcontroltype.md) en lugar del tipo de control DataItem.</span><span class="sxs-lookup"><span data-stu-id="0c208-277">If a grid represents a list of selectable items, the corresponding selectable UI elements can be exposed with the [ListItem](uiauto-supportlistitemcontroltype.md) control type instead of the DataItem control type.</span></span> <span data-ttu-id="0c208-278">En el ejemplo anterior, los elementos **DataItem** ("accounts Receivable.doc" y "accounts Payable.doc") en **Group** ("Contoso") se pueden mejorar si se exponen como tipos de control ListItem, porque ese tipo ya admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) .</span><span class="sxs-lookup"><span data-stu-id="0c208-278">In the preceding example, the **DataItem** elements ("Accounts Receivable.doc" and "Accounts Payable.doc") under **Group** ("Contoso") can be improved by exposing them as ListItem control types because that type already supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c208-279">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0c208-279">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0c208-280">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0c208-280">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0c208-281">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="0c208-281">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="0c208-282">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="0c208-282">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




