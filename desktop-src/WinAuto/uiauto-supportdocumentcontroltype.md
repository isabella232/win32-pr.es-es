---
title: Document (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Document.
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Document
- Automatización de la interfaz de usuario, tipo de control Document
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Document
- Automatización de la interfaz de usuario, propiedades para el tipo de control Document
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Document
- Automatización de la interfaz de usuario, eventos para el tipo de control Document
- estructuras de árbol, tipo de control Document
- propiedades, tipo de control Document
- patrones de control, tipo de control Document
- Events, Document (tipo de control)
- compatibilidad con el tipo de control Document
- Document (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Document
- tipos de control, patrones de control para el tipo de control Document
- tipos de control, compatibilidad con documentos
- tipos de control, documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ca481df812e3321da7bb4bbb39bdcb5628fb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075616"
---
# <a name="document-control-type"></a><span data-ttu-id="f64ea-119">Document (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="f64ea-119">Document Control Type</span></span>

<span data-ttu-id="f64ea-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Document** .</span><span class="sxs-lookup"><span data-stu-id="f64ea-120">This topic provides information about Microsoft UI Automation support for the **Document** control type.</span></span>

<span data-ttu-id="f64ea-121">Los controles de documento permiten a un usuario ver y manipular varias páginas de texto.</span><span class="sxs-lookup"><span data-stu-id="f64ea-121">Document controls let a user view and manipulate multiple pages of text.</span></span> <span data-ttu-id="f64ea-122">A diferencia de los controles de edición que solo admiten una línea simple de texto sin formato, los controles de documento pueden hospedar texto con estilo y formato enriquecidos.</span><span class="sxs-lookup"><span data-stu-id="f64ea-122">Unlike edit controls which only support a simple line of unformatted text, document controls can host text that is richly styled and formatted</span></span>

<span data-ttu-id="f64ea-123">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Document** .</span><span class="sxs-lookup"><span data-stu-id="f64ea-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Document** control type.</span></span> <span data-ttu-id="f64ea-124">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de documento donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control</span><span class="sxs-lookup"><span data-stu-id="f64ea-124">The UI Automation requirements apply to all document controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="f64ea-125">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="f64ea-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f64ea-126">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="f64ea-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="f64ea-127">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="f64ea-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="f64ea-128">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="f64ea-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="f64ea-129">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="f64ea-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="f64ea-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f64ea-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="f64ea-131">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="f64ea-131">Typical Tree Structure</span></span>

<span data-ttu-id="f64ea-132">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de documento y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="f64ea-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to document controls and describes what can be contained in each view.</span></span> <span data-ttu-id="f64ea-133">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f64ea-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f64ea-134">Vista de control</span><span class="sxs-lookup"><span data-stu-id="f64ea-134">Control View</span></span></th>
<th><span data-ttu-id="f64ea-135">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="f64ea-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="f64ea-136">Documento</span><span class="sxs-lookup"><span data-stu-id="f64ea-136">Document</span></span>
<ul>
<li><span data-ttu-id="f64ea-137">Varía</span><span class="sxs-lookup"><span data-stu-id="f64ea-137">Varies</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f64ea-138">Documento</span><span class="sxs-lookup"><span data-stu-id="f64ea-138">Document</span></span>
<ul>
<li><span data-ttu-id="f64ea-139">Varía</span><span class="sxs-lookup"><span data-stu-id="f64ea-139">Varies</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="f64ea-140">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="f64ea-140">Relevant Properties</span></span>

<span data-ttu-id="f64ea-141">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de documento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-141">The following table lists the UI Automation properties whose value or definition is especially relevant to document controls.</span></span> <span data-ttu-id="f64ea-142">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="f64ea-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="f64ea-143">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="f64ea-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="f64ea-144">Value</span><span class="sxs-lookup"><span data-stu-id="f64ea-144">Value</span></span>        | <span data-ttu-id="f64ea-145">Notas</span><span class="sxs-lookup"><span data-stu-id="f64ea-145">Notes</span></span>                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f64ea-146">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f64ea-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="f64ea-147">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="f64ea-147">See notes.</span></span>   | <span data-ttu-id="f64ea-148">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f64ea-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                      |
| [<span data-ttu-id="f64ea-149">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f64ea-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="f64ea-150">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="f64ea-150">See notes.</span></span>   | <span data-ttu-id="f64ea-151">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="f64ea-151">The outermost rectangle that contains the whole control.</span></span>                                                                                          |
| [<span data-ttu-id="f64ea-152">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f64ea-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="f64ea-153">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="f64ea-153">See notes.</span></span>   | <span data-ttu-id="f64ea-154">El documento tiene un punto en el que se puede hacer clic que provocará que el foco pase al documento de uno de sus elementos del contenedor de documento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-154">The document has a clickable point that will cause the document of one of its elements in the document container to have focus.</span></span>                   |
| [<span data-ttu-id="f64ea-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f64ea-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="f64ea-156">**Documento**</span><span class="sxs-lookup"><span data-stu-id="f64ea-156">**Document**</span></span> |                                                                                                                                                   |
| [<span data-ttu-id="f64ea-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f64ea-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="f64ea-158">TRUE</span><span class="sxs-lookup"><span data-stu-id="f64ea-158">TRUE</span></span>         | <span data-ttu-id="f64ea-159">El control de documento siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f64ea-159">The document control is always included in the content view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="f64ea-160">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f64ea-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="f64ea-161">TRUE</span><span class="sxs-lookup"><span data-stu-id="f64ea-161">TRUE</span></span>         | <span data-ttu-id="f64ea-162">El control de documento siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f64ea-162">The document control is always included in the control view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="f64ea-163">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f64ea-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="f64ea-164">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="f64ea-164">See notes.</span></span>   | <span data-ttu-id="f64ea-165">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f64ea-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                         |
| [<span data-ttu-id="f64ea-166">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f64ea-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="f64ea-167">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="f64ea-167">See notes.</span></span>   | <span data-ttu-id="f64ea-168">El valor de esta propiedad debe ser la etiqueta del control de documento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-168">The value of this property should be the label of the document control.</span></span> <span data-ttu-id="f64ea-169">Normalmente, se utiliza el título del documento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-169">Typically, the title of the document is used.</span></span>                             |
| [<span data-ttu-id="f64ea-170">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f64ea-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="f64ea-171">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="f64ea-171">See notes.</span></span>   | <span data-ttu-id="f64ea-172">Cadena localizada que corresponde al tipo de control **Document** .</span><span class="sxs-lookup"><span data-stu-id="f64ea-172">Localized string corresponding to the **Document** control type.</span></span> <span data-ttu-id="f64ea-173">El valor predeterminado es "Document" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="f64ea-173">The default value is "document" for en-US or English (United States).</span></span>            |
| [<span data-ttu-id="f64ea-174">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f64ea-174">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="f64ea-175">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="f64ea-175">See notes.</span></span>   | <span data-ttu-id="f64ea-176">Normalmente, el control de documento recibe su nombre del nombre del archivo desde el que se carga.</span><span class="sxs-lookup"><span data-stu-id="f64ea-176">The document control typically gets its name from the file name it is loaded from.</span></span> <span data-ttu-id="f64ea-177">A menudo, esto se muestra en el título de un marco o una ventana contenedora.</span><span class="sxs-lookup"><span data-stu-id="f64ea-177">This is often displayed in a containing window or frame title.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="f64ea-178">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="f64ea-178">Required Control Patterns</span></span>

<span data-ttu-id="f64ea-179">En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que deben admitir los controles de documento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-179">The following table lists the UI Automation control patterns required to be supported by document controls.</span></span> <span data-ttu-id="f64ea-180">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f64ea-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="f64ea-181">Patrón de control/Propiedad de patrón</span><span class="sxs-lookup"><span data-stu-id="f64ea-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="f64ea-182">Soporte técnico/valor</span><span class="sxs-lookup"><span data-stu-id="f64ea-182">Support/Value</span></span> | <span data-ttu-id="f64ea-183">Notas</span><span class="sxs-lookup"><span data-stu-id="f64ea-183">Notes</span></span>                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f64ea-184">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="f64ea-184">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | <span data-ttu-id="f64ea-185">Depende</span><span class="sxs-lookup"><span data-stu-id="f64ea-185">Depends</span></span>       | <span data-ttu-id="f64ea-186">El control de documento puede abarcar más de lo que puede la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="f64ea-186">The document control can span larger than that span of the viewport.</span></span> <span data-ttu-id="f64ea-187">El control debe admitir el patrón de control [Scroll](uiauto-implementingscroll.md) si el contenido es desplazable.</span><span class="sxs-lookup"><span data-stu-id="f64ea-187">The control should support the [Scroll](uiauto-implementingscroll.md) control pattern if the content is scrollable.</span></span>                                                                                                                              |
| [<span data-ttu-id="f64ea-188">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="f64ea-188">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | <span data-ttu-id="f64ea-189">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f64ea-189">Required</span></span>      | <span data-ttu-id="f64ea-190">Todos los controles de documento deben admitir el patrón de control [Text](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="f64ea-190">All document controls must support the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="f64ea-191">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="f64ea-191">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="f64ea-192">Depende</span><span class="sxs-lookup"><span data-stu-id="f64ea-192">Depends</span></span>       | <span data-ttu-id="f64ea-193">Aunque los clientes de automatización de la interfaz de usuario pueden usar [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) para obtener información de texto sobre un documento, necesitan el patrón de control [Value](uiauto-implementingvalue.md) para establecer el valor interno.</span><span class="sxs-lookup"><span data-stu-id="f64ea-193">While UI Automation clients can use [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) to obtain text information about a document, they need the [Value](uiauto-implementingvalue.md) control pattern to set the inner value.</span></span> <span data-ttu-id="f64ea-194">La entrada de texto simple solo es posible a través del patrón de control Value.</span><span class="sxs-lookup"><span data-stu-id="f64ea-194">Simple text entry is possible only through the Value control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="f64ea-195">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="f64ea-195">Required Events</span></span>

<span data-ttu-id="f64ea-196">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de documento deben admitir.</span><span class="sxs-lookup"><span data-stu-id="f64ea-196">The following table lists the UI Automation events that document controls are required to support.</span></span> <span data-ttu-id="f64ea-197">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f64ea-197">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="f64ea-198">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="f64ea-198">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="f64ea-199">Notas</span><span class="sxs-lookup"><span data-stu-id="f64ea-199">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f64ea-200">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="f64ea-200">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="f64ea-201">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f64ea-201">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="f64ea-202">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="f64ea-202">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="f64ea-203">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-203">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="f64ea-204">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="f64ea-204">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="f64ea-205">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-205">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="f64ea-206">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="f64ea-206">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| <span data-ttu-id="f64ea-207">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f64ea-207">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="f64ea-208">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-208">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="f64ea-209">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="f64ea-209">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="f64ea-210">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-210">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="f64ea-211">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f64ea-211">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="f64ea-212">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-212">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="f64ea-213">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f64ea-213">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="f64ea-214">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-214">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="f64ea-215">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="f64ea-215">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="f64ea-216">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-216">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="f64ea-217">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f64ea-217">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="f64ea-218">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-218">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="f64ea-219">**\_InvalidatedEventId de selección de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="f64ea-219">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            | <span data-ttu-id="f64ea-220">Si el control admite el patrón de control [Selection](uiauto-implementingselection.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-220">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="f64ea-221">**\_TextSelectionChangedEventId de texto de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="f64ea-221">**UIA\_Text\_TextSelectionChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [<span data-ttu-id="f64ea-222">**\_TextChangedEventId de texto de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="f64ea-222">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| <span data-ttu-id="f64ea-223">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f64ea-223">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                       | <span data-ttu-id="f64ea-224">Si el control admite el patrón de control [Value](uiauto-implementingvalue.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="f64ea-224">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="f64ea-225">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f64ea-225">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f64ea-226">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f64ea-226">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f64ea-227">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="f64ea-227">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="f64ea-228">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="f64ea-228">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




