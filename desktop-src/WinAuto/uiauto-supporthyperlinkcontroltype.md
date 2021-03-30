---
title: HYPERLINK (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control HyperLink.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control HyperLink
- Automatización de la interfaz de usuario, tipo de control HyperLink
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control HyperLink
- Automatización de la interfaz de usuario, propiedades para el tipo de control HyperLink
- Automatización de la interfaz de usuario, patrones de control para el tipo de control HyperLink
- Automatización de la interfaz de usuario, eventos para el tipo de control HyperLink
- estructuras de árbol, tipo de control HyperLink
- propiedades, tipo de control HyperLink
- patrones de control, HYPERLINK (tipo de control)
- Events, HYPERLINK (tipo de control)
- compatibilidad con el tipo de control HyperLink
- Hyperlink (tipo de control)
- tipos de control, estructura de árbol para el tipo de control HyperLink
- tipos de control, patrones de control para el tipo de control HyperLink
- tipos de control, compatibilidad con hipervínculo
- tipos de control, hipervínculo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71547f37380aeb029e4f73f8d9b2286b285187ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775847"
---
# <a name="hyperlink-control-type"></a><span data-ttu-id="e31e2-119">HYPERLINK (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="e31e2-119">Hyperlink Control Type</span></span>

<span data-ttu-id="e31e2-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **HYPERLINK** .</span><span class="sxs-lookup"><span data-stu-id="e31e2-120">This topic provides information about Microsoft UI Automation support for the **Hyperlink** control type.</span></span>

<span data-ttu-id="e31e2-121">Los controles de hipervínculo crean vínculos que permiten a los usuarios navegar dentro de la misma página o de una página a otra.</span><span class="sxs-lookup"><span data-stu-id="e31e2-121">Hyperlink controls create links that enable users to navigate within the same page, or from one page to another.</span></span>

<span data-ttu-id="e31e2-122">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **HYPERLINK** .</span><span class="sxs-lookup"><span data-stu-id="e31e2-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Hyperlink** control type.</span></span> <span data-ttu-id="e31e2-123">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de hipervínculo en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y</span><span class="sxs-lookup"><span data-stu-id="e31e2-123">The UI Automation requirements apply to all hyperlink controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="e31e2-124">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="e31e2-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e31e2-125">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="e31e2-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="e31e2-126">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="e31e2-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="e31e2-127">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="e31e2-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="e31e2-128">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="e31e2-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="e31e2-129">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="e31e2-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="e31e2-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e31e2-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="e31e2-131">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="e31e2-131">Typical Tree Structure</span></span>

<span data-ttu-id="e31e2-132">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de hipervínculo y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="e31e2-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to hyperlink controls and describes what can be contained in each view.</span></span> <span data-ttu-id="e31e2-133">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e31e2-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e31e2-134">Vista de control</span><span class="sxs-lookup"><span data-stu-id="e31e2-134">Control View</span></span></th>
<th><span data-ttu-id="e31e2-135">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="e31e2-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e31e2-136">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="e31e2-136">Hyperlink</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e31e2-137">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="e31e2-137">Hyperlink</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="e31e2-138">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="e31e2-138">Relevant Properties</span></span>

<span data-ttu-id="e31e2-139">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="e31e2-139">The following table lists the UI Automation properties whose value or definition is especially relevant to the hyperlink controls.</span></span> <span data-ttu-id="e31e2-140">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="e31e2-140">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="e31e2-141">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="e31e2-141">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="e31e2-142">Value</span><span class="sxs-lookup"><span data-stu-id="e31e2-142">Value</span></span>         | <span data-ttu-id="e31e2-143">Notas</span><span class="sxs-lookup"><span data-stu-id="e31e2-143">Notes</span></span>                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e31e2-144">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e31e2-144">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="e31e2-145">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="e31e2-145">See notes.</span></span>    | <span data-ttu-id="e31e2-146">El valor de esta propiedad debe ser único en todos los controles de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e31e2-146">The value of this property must be unique across all controls in an application.</span></span>                                                         |
| [<span data-ttu-id="e31e2-147">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e31e2-147">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="e31e2-148">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="e31e2-148">See notes.</span></span>    | <span data-ttu-id="e31e2-149">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="e31e2-149">The outermost rectangle that contains the whole control.</span></span>                                                                                 |
| [<span data-ttu-id="e31e2-150">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e31e2-150">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="e31e2-151">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="e31e2-151">See notes.</span></span>    | <span data-ttu-id="e31e2-152">El punto en el que se puede hacer clic del control de hipervínculo debe ser un punto que inicie el hipervínculo si se hace clic con el puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="e31e2-152">The hyperlink control's clickable point must be a point that launches the hyperlink if clicked with a mouse pointer.</span></span>                     |
| [<span data-ttu-id="e31e2-153">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e31e2-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="e31e2-154">**Hipervínculo**</span><span class="sxs-lookup"><span data-stu-id="e31e2-154">**Hyperlink**</span></span> |                                                                                                                                          |
| [<span data-ttu-id="e31e2-155">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e31e2-155">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="e31e2-156">TRUE</span><span class="sxs-lookup"><span data-stu-id="e31e2-156">TRUE</span></span>          | <span data-ttu-id="e31e2-157">El control de hipervínculo siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e31e2-157">The hyperlink control is always included in the content view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="e31e2-158">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e31e2-158">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="e31e2-159">TRUE</span><span class="sxs-lookup"><span data-stu-id="e31e2-159">TRUE</span></span>          | <span data-ttu-id="e31e2-160">El control de hipervínculo siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e31e2-160">The hyperlink control is always included in the control view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="e31e2-161">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e31e2-161">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="e31e2-162">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="e31e2-162">See notes.</span></span>    | <span data-ttu-id="e31e2-163">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e31e2-163">If the control can receive keyboard focus, it must support this property.</span></span>                                                                |
| [<span data-ttu-id="e31e2-164">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="e31e2-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="e31e2-165">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="e31e2-165">See notes.</span></span>    | <span data-ttu-id="e31e2-166">Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.</span><span class="sxs-lookup"><span data-stu-id="e31e2-166">If there is a static text label, this property must expose a reference to that control.</span></span>                                                  |
| [<span data-ttu-id="e31e2-167">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e31e2-167">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="e31e2-168">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="e31e2-168">See notes.</span></span>    | <span data-ttu-id="e31e2-169">Cadena localizada que corresponde al tipo de control **HYPERLINK** .</span><span class="sxs-lookup"><span data-stu-id="e31e2-169">Localized string corresponding to the **Hyperlink** control type.</span></span> <span data-ttu-id="e31e2-170">El valor predeterminado es "HYPERLINK" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="e31e2-170">The default value is "hyperlink" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="e31e2-171">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="e31e2-171">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="e31e2-172">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="e31e2-172">See notes.</span></span>    | <span data-ttu-id="e31e2-173">El nombre del control de hipervínculo es el texto que se muestra en la pantalla como subrayado.</span><span class="sxs-lookup"><span data-stu-id="e31e2-173">The hyperlink control's name is the text that is displayed on the screen as underlined.</span></span>                                                  |



 

## <a name="required-control-patterns"></a><span data-ttu-id="e31e2-174">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="e31e2-174">Required Control Patterns</span></span>

<span data-ttu-id="e31e2-175">En la tabla siguiente se enumeran los patrones de control de UI Automation que los controles de hipervínculo deben admitir.</span><span class="sxs-lookup"><span data-stu-id="e31e2-175">The following table lists the UI Automation control patterns that hyperlink controls are required to support.</span></span> <span data-ttu-id="e31e2-176">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e31e2-176">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="e31e2-177">Patrón de control/Propiedad de patrón</span><span class="sxs-lookup"><span data-stu-id="e31e2-177">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="e31e2-178">Soporte técnico/valor</span><span class="sxs-lookup"><span data-stu-id="e31e2-178">Support/Value</span></span>                | <span data-ttu-id="e31e2-179">Notas</span><span class="sxs-lookup"><span data-stu-id="e31e2-179">Notes</span></span>                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e31e2-180">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="e31e2-180">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | <span data-ttu-id="e31e2-181">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e31e2-181">Required</span></span>                     | <span data-ttu-id="e31e2-182">Todos los controles de hipervínculo deben admitir el patrón de control [Invoke](uiauto-implementinginvoke.md) .</span><span class="sxs-lookup"><span data-stu-id="e31e2-182">All hyperlink controls must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="e31e2-183">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="e31e2-183">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="e31e2-184">Depende</span><span class="sxs-lookup"><span data-stu-id="e31e2-184">Depends</span></span>                      | <span data-ttu-id="e31e2-185">Los controles de hipervínculo deben admitir el patrón de control [Value](uiauto-implementingvalue.md) si el vínculo contiene información que es utilizable y significativa para el usuario.</span><span class="sxs-lookup"><span data-stu-id="e31e2-185">Hyperlink controls should support the [Value](uiauto-implementingvalue.md) control pattern when the link contains information that is usable and meaningful to the user.</span></span>                                                                              |
| [<span data-ttu-id="e31e2-186">**Value**</span><span class="sxs-lookup"><span data-stu-id="e31e2-186">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | <span data-ttu-id="e31e2-187">Por ejemplo, "https://www..".</span><span class="sxs-lookup"><span data-stu-id="e31e2-187">For example, "https://www..."</span></span> | <span data-ttu-id="e31e2-188">Una dirección URL para una dirección de Internet o Intranet es un ejemplo de un hipervínculo que contiene información significativa para el usuario.</span><span class="sxs-lookup"><span data-stu-id="e31e2-188">A URL for an Internet or intranet address is an example of a hyperlink that contains information that is meaningful to the user.</span></span> <span data-ttu-id="e31e2-189">Sin embargo, un vínculo de programación solo es significativo para una aplicación y no se recomienda para la propiedad **Value** .</span><span class="sxs-lookup"><span data-stu-id="e31e2-189">A programmatic link, however, is meaningful only to an application and is not recommended for the **Value** property.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="e31e2-190">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="e31e2-190">Required Events</span></span>

<span data-ttu-id="e31e2-191">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de hipervínculo deben admitir.</span><span class="sxs-lookup"><span data-stu-id="e31e2-191">The following table lists the UI Automation events that hyperlink controls are required to support.</span></span> <span data-ttu-id="e31e2-192">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e31e2-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="e31e2-193">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="e31e2-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="e31e2-194">Notas</span><span class="sxs-lookup"><span data-stu-id="e31e2-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e31e2-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="e31e2-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="e31e2-196">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="e31e2-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="e31e2-197">**\_InvokedEventId de invocación de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="e31e2-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     |                                                                                                                            |
| <span data-ttu-id="e31e2-198">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="e31e2-198">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="e31e2-199">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="e31e2-199">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="e31e2-200">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="e31e2-200">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="e31e2-201">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="e31e2-201">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="e31e2-202">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="e31e2-202">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="e31e2-203">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e31e2-203">Remarks</span></span>

<span data-ttu-id="e31e2-204">El tipo de control HyperLink solo debe aplicarse a un objeto que, cuando se hace clic en él, hace que se produzca la navegación; no se debe aplicar al contenedor del hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="e31e2-204">The Hyperlink control type should be applied only to an object that, when clicked, causes navigation to occur; it should not be applied to the container of the hyperlink.</span></span> <span data-ttu-id="e31e2-205">Por ejemplo, solo las "zonas activas" en las que se hace clic dentro de un mapa de imágenes deben tener el tipo de control **HYPERLINK** .</span><span class="sxs-lookup"><span data-stu-id="e31e2-205">For example, only the clickable "hot spots" inside an image map should have the **Hyperlink** control type.</span></span> <span data-ttu-id="e31e2-206">Lo mismo se aplica a los hipervínculos de un campo de texto o contenedor de documentos.</span><span class="sxs-lookup"><span data-stu-id="e31e2-206">The same is true of hyperlinks in a text field or document container.</span></span> <span data-ttu-id="e31e2-207">En este caso, solo el texto o la imagen del hipervínculo deben tener el tipo de control **HYPERLINK** , no el contenedor.</span><span class="sxs-lookup"><span data-stu-id="e31e2-207">In this case, only the hyperlink text or image should have the **Hyperlink** control type, not the container.</span></span>

<span data-ttu-id="e31e2-208">El patrón de control [Text](uiauto-implementingtextandtextrange.md) es idóneo para admitir hipervínculos incrustados en elementos de texto o de documento.</span><span class="sxs-lookup"><span data-stu-id="e31e2-208">The [Text](uiauto-implementingtextandtextrange.md) control pattern is ideal for supporting embedded hyperlinks in text or document elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e31e2-209">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e31e2-209">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e31e2-210">**Vista**</span><span class="sxs-lookup"><span data-stu-id="e31e2-210">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e31e2-211">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="e31e2-211">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="e31e2-212">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="e31e2-212">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




