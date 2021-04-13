---
title: Text (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Text.
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Text
- Automatización de la interfaz de usuario, tipo de control Text
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Text
- Automatización de la interfaz de usuario, propiedades para el tipo de control Text
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Text
- Automatización de la interfaz de usuario, eventos para el tipo de control Text
- estructuras de árbol, tipo de control Text
- propiedades, Text (tipo de control)
- patrones de control, Text (tipo de control)
- Events, Text (tipo de control)
- compatibilidad con el tipo de control Text
- Text (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Text
- tipos de control, patrones de control para el tipo de control Text
- tipos de control, compatibilidad con texto
- tipos de control, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902b3c7c523417abde2c60e1f8039ad9f2c322b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357378"
---
# <a name="text-control-type"></a><span data-ttu-id="2f7bf-119">Text (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="2f7bf-119">Text Control Type</span></span>

<span data-ttu-id="2f7bf-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Text** .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-120">This topic provides information about Microsoft UI Automation support for the **Text** control type.</span></span>

<span data-ttu-id="2f7bf-121">Un control de texto es un elemento básico de la interfaz de usuario que representa un fragmento de texto en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-121">A text control is a basic user interface item that represents a piece of text on the screen.</span></span>

<span data-ttu-id="2f7bf-122">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Text** .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Text** control type.</span></span> <span data-ttu-id="2f7bf-123">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de árbol donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-123">The UI Automation requirements apply to all tree controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="2f7bf-124">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2f7bf-125">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="2f7bf-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="2f7bf-126">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="2f7bf-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="2f7bf-127">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="2f7bf-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="2f7bf-128">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="2f7bf-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="2f7bf-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f7bf-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="2f7bf-130">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="2f7bf-130">Typical Tree Structure</span></span>

<span data-ttu-id="2f7bf-131">En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de texto y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to text controls and describes what can be contained in each view.</span></span> <span data-ttu-id="2f7bf-132">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2f7bf-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2f7bf-133">Vista de control</span><span class="sxs-lookup"><span data-stu-id="2f7bf-133">Control View</span></span></th>
<th><span data-ttu-id="2f7bf-134">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="2f7bf-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2f7bf-135">Texto</span><span class="sxs-lookup"><span data-stu-id="2f7bf-135">Text</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2f7bf-136">Texto (si hay contenido)</span><span class="sxs-lookup"><span data-stu-id="2f7bf-136">Text (if content)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2f7bf-137">Un control de texto se puede usar solo como una etiqueta o como texto estático en un formulario.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-137">A text control can be used alone as a label or as static text on a form.</span></span> <span data-ttu-id="2f7bf-138">También puede estar dentro de la estructura de uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2f7bf-138">It can also be contained within the structure of one of the following items:</span></span>

-   [<span data-ttu-id="2f7bf-139">DataItem</span><span class="sxs-lookup"><span data-stu-id="2f7bf-139">DataItem</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="2f7bf-140">ListItem</span><span class="sxs-lookup"><span data-stu-id="2f7bf-140">ListItem</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="2f7bf-141">TreeItem</span><span class="sxs-lookup"><span data-stu-id="2f7bf-141">TreeItem</span></span>](uiauto-supporttreeitemcontroltype.md)

<span data-ttu-id="2f7bf-142">Es posible que los controles de texto no aparezcan en la vista de contenido del árbol de automatización de la interfaz de usuario porque el texto se muestra a menudo a través de la propiedad **Name** de otro control.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-142">Text controls might not appear in the content view of the UI Automation tree because text is often displayed through the **Name** property of another control.</span></span> <span data-ttu-id="2f7bf-143">Por ejemplo, el texto que se usa para etiquetar un control de cuadro combinado se expone a través de la propiedad **Name** del control.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-143">For example, the text used to label a combo box control is exposed through the control's **Name** property.</span></span> <span data-ttu-id="2f7bf-144">Dado que el control de cuadro combinado está en la vista de contenido del árbol de automatización de la interfaz de usuario, no es necesario que el control de texto esté ahí.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-144">Because the combo box control is in the content view of the UI Automation tree, the text control need not be there.</span></span> <span data-ttu-id="2f7bf-145">Los controles de texto pueden tener elementos secundarios en la vista de contenido si hay un objeto incrustado, como un hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-145">Text controls may have children in the content view if there is an embedded object such as a hyperlink.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="2f7bf-146">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="2f7bf-146">Relevant Properties</span></span>

<span data-ttu-id="2f7bf-147">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de texto.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the text controls.</span></span> <span data-ttu-id="2f7bf-148">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="2f7bf-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="2f7bf-149">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="2f7bf-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="2f7bf-150">Value</span><span class="sxs-lookup"><span data-stu-id="2f7bf-150">Value</span></span>      | <span data-ttu-id="2f7bf-151">Notas</span><span class="sxs-lookup"><span data-stu-id="2f7bf-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f7bf-152">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="2f7bf-153">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-153">See notes.</span></span> | <span data-ttu-id="2f7bf-154">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="2f7bf-155">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="2f7bf-156">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-156">See notes.</span></span> | <span data-ttu-id="2f7bf-157">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-157">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="2f7bf-158">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="2f7bf-159">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-159">See notes.</span></span> | <span data-ttu-id="2f7bf-160">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="2f7bf-161">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-161">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                                                                |
| [<span data-ttu-id="2f7bf-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="2f7bf-163">**Texto**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-163">**Text**</span></span>   |                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="2f7bf-164">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="2f7bf-165">Depende</span><span class="sxs-lookup"><span data-stu-id="2f7bf-165">Depends</span></span>    | <span data-ttu-id="2f7bf-166">El control de texto es contenido si contiene información no expuesta en la propiedad nombre de otro control.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-166">The text control is content if it contains information not exposed in another control's Name property.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="2f7bf-167">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="2f7bf-168">TRUE</span><span class="sxs-lookup"><span data-stu-id="2f7bf-168">TRUE</span></span>       | <span data-ttu-id="2f7bf-169">El control de texto siempre debe ser un control.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-169">The text control must always be a control.</span></span>                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="2f7bf-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="2f7bf-171">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-171">See notes.</span></span> | <span data-ttu-id="2f7bf-172">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2f7bf-173">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="2f7bf-174">NULL</span><span class="sxs-lookup"><span data-stu-id="2f7bf-174">NULL</span></span>       | <span data-ttu-id="2f7bf-175">Los controles de texto no tienen una etiqueta de texto estático.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-175">Text controls do not have a static text label.</span></span>                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="2f7bf-176">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="2f7bf-177">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-177">See notes.</span></span> | <span data-ttu-id="2f7bf-178">Cadena localizada que corresponde al tipo de control **Text** .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-178">Localized string corresponding to the **Text** control type.</span></span> <span data-ttu-id="2f7bf-179">El valor predeterminado es "Text" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="2f7bf-179">The default value is "text" for en-US or English (United States).</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="2f7bf-180">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="2f7bf-181">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-181">See notes.</span></span> | <span data-ttu-id="2f7bf-182">El nombre de un control de texto puede ser el texto que muestra.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-182">The name of a text control can be the text that it displays.</span></span> <span data-ttu-id="2f7bf-183">Sin embargo, si el control también admite el patrón de [texto](uiauto-implementingtextandtextrange.md) y el texto es extensivo, no use el contenido de texto completo como valor de **nombre** .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-183">However, if the control also supports the [Text](uiauto-implementingtextandtextrange.md) pattern, and the text is extensive, don't use the full text content as the **Name** value.</span></span> <span data-ttu-id="2f7bf-184">En su lugar, proporcione un valor de **nombre** que sea más corto, derivado de otras propiedades del control.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-184">Instead, provide a **Name** value that is shorter, derived from other properties of your control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="2f7bf-185">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="2f7bf-185">Required Control Patterns</span></span>

<span data-ttu-id="2f7bf-186">En la tabla siguiente se muestran los patrones de control de UI Automation que deben admitir los controles de texto.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-186">The following table lists the UI Automation control patterns required to be supported by text controls.</span></span> <span data-ttu-id="2f7bf-187">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2f7bf-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="2f7bf-188">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="2f7bf-188">Control Pattern</span></span>                                         | <span data-ttu-id="2f7bf-189">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="2f7bf-189">Support</span></span> | <span data-ttu-id="2f7bf-190">Notas</span><span class="sxs-lookup"><span data-stu-id="2f7bf-190">Notes</span></span>                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f7bf-191">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-191">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="2f7bf-192">Depende</span><span class="sxs-lookup"><span data-stu-id="2f7bf-192">Depends</span></span> | <span data-ttu-id="2f7bf-193">Si el control de texto está contenido dentro de un control de tabla, se debe admitir el patrón de control [GridItem](uiauto-implementinggriditem.md) .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-193">If the text control is contained within a table control, the [GridItem](uiauto-implementinggriditem.md) control pattern must be supported.</span></span>                                                                                                                            |
| [<span data-ttu-id="2f7bf-194">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-194">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="2f7bf-195">Depende</span><span class="sxs-lookup"><span data-stu-id="2f7bf-195">Depends</span></span> | <span data-ttu-id="2f7bf-196">Si el control de texto está contenido dentro de un control de tabla, se debe admitir el patrón de control [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-196">If the text control is contained within a table control, the [TableItem](uiauto-implementingtableitem.md) control pattern must be supported.</span></span>                                                                                                                          |
| [<span data-ttu-id="2f7bf-197">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-197">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | <span data-ttu-id="2f7bf-198">Depende</span><span class="sxs-lookup"><span data-stu-id="2f7bf-198">Depends</span></span> | <span data-ttu-id="2f7bf-199">El texto debe admitir el patrón de control [Text](uiauto-implementingtextandtextrange.md) para mejorar la accesibilidad; sin embargo, no es necesario.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-199">Text should support the [Text](uiauto-implementingtextandtextrange.md) control pattern for better accessibility; however, it is not required.</span></span> <span data-ttu-id="2f7bf-200">El patrón de control Text es útil cuando el texto tiene atributos y estilo enriquecidos (por ejemplo, color, negrita y cursiva).</span><span class="sxs-lookup"><span data-stu-id="2f7bf-200">The Text control pattern is useful when the text has rich style and attributes (for example, color, bold, and italics).</span></span> |
| [<span data-ttu-id="2f7bf-201">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-201">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | <span data-ttu-id="2f7bf-202">Nunca</span><span class="sxs-lookup"><span data-stu-id="2f7bf-202">Never</span></span>   | <span data-ttu-id="2f7bf-203">Un control de texto nunca admite el patrón de control [Value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-203">A text control never supports the [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="2f7bf-204">Si el texto es editable, es el tipo de control [Edit](uiauto-supporteditcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-204">If the text is editable, it is the [Edit](uiauto-supporteditcontroltype.md) control type.</span></span>                                                                                    |



 

## <a name="required-events"></a><span data-ttu-id="2f7bf-205">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="2f7bf-205">Required Events</span></span>

<span data-ttu-id="2f7bf-206">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de texto deben admitir.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-206">The following table lists the UI Automation events that text controls are required to support.</span></span> <span data-ttu-id="2f7bf-207">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2f7bf-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="2f7bf-208">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="2f7bf-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="2f7bf-209">Notas</span><span class="sxs-lookup"><span data-stu-id="2f7bf-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f7bf-210">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="2f7bf-211">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="2f7bf-212">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-212">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="2f7bf-213">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-213">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="2f7bf-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="2f7bf-215">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="2f7bf-216">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de NamePropertyId.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-216">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="2f7bf-217">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-217">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [<span data-ttu-id="2f7bf-218">**\_TextChangedEventId de texto de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-218">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                 | <span data-ttu-id="2f7bf-219">Si el control admite el patrón de control [Text](uiauto-implementingtextandtextrange.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-219">If the control supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, it must support this event.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="2f7bf-220">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f7bf-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2f7bf-221">**Vista**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2f7bf-222">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="2f7bf-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="2f7bf-223">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="2f7bf-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




