---
title: Slide (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Slider.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Slider
- Automatización de la interfaz de usuario, tipo de control Slider
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Slider
- Automatización de la interfaz de usuario, propiedades para el tipo de control Slider
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Slider
- Automatización de la interfaz de usuario, eventos para el tipo de control Slider
- estructuras de árbol, tipo de control Slider
- propiedades, tipo de control Slider
- patrones de control, tipo de control Slider
- Events, Slide (tipo de control)
- compatibilidad con el tipo de control Slider
- Slider (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Slider
- tipos de control, patrones de control para el tipo de control Slider
- tipos de control, compatibilidad con el control deslizante
- tipos de control, control deslizante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be8e82dfc8f011363086745368ed1693c45a6aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994357"
---
# <a name="slider-control-type"></a><span data-ttu-id="d1ff9-119">Slide (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="d1ff9-119">Slider Control Type</span></span>

<span data-ttu-id="d1ff9-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Slider** .</span><span class="sxs-lookup"><span data-stu-id="d1ff9-120">This topic provides information about Microsoft UI Automation support for the **Slider** control type.</span></span>

<span data-ttu-id="d1ff9-121">Un control deslizante es un control compuesto con botones que permiten a un usuario establecer un intervalo numérico o seleccionar un conjunto de elementos.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-121">A slider control is a composite control with buttons that enable a user to set a numerical range or select from a set of items.</span></span>

<span data-ttu-id="d1ff9-122">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Slider** .</span><span class="sxs-lookup"><span data-stu-id="d1ff9-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Slider** control type.</span></span> <span data-ttu-id="d1ff9-123">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles deslizantes donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control</span><span class="sxs-lookup"><span data-stu-id="d1ff9-123">The UI Automation requirements apply to all slider controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="d1ff9-124">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d1ff9-125">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="d1ff9-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="d1ff9-126">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d1ff9-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="d1ff9-127">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="d1ff9-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="d1ff9-128">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="d1ff9-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="d1ff9-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1ff9-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="d1ff9-130">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="d1ff9-130">Typical Tree Structure</span></span>

<span data-ttu-id="d1ff9-131">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles deslizantes y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to slider controls and describes what can be contained in each view.</span></span> <span data-ttu-id="d1ff9-132">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d1ff9-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1ff9-133">Vista de control</span><span class="sxs-lookup"><span data-stu-id="d1ff9-133">Control View</span></span></th>
<th><span data-ttu-id="d1ff9-134">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="d1ff9-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d1ff9-135">Control deslizante</span><span class="sxs-lookup"><span data-stu-id="d1ff9-135">Slider</span></span>
<ul>
<li><span data-ttu-id="d1ff9-136">Button (2 o 4)</span><span class="sxs-lookup"><span data-stu-id="d1ff9-136">Button (2 or 4)</span></span></li>
<li><span data-ttu-id="d1ff9-137">Thumb (1)</span><span class="sxs-lookup"><span data-stu-id="d1ff9-137">Thumb (1)</span></span></li>
<li><span data-ttu-id="d1ff9-138">Elemento de lista (0 o más)</span><span class="sxs-lookup"><span data-stu-id="d1ff9-138">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d1ff9-139">Control deslizante</span><span class="sxs-lookup"><span data-stu-id="d1ff9-139">Slider</span></span>
<ul>
<li><span data-ttu-id="d1ff9-140">Elemento de lista (0 o más)</span><span class="sxs-lookup"><span data-stu-id="d1ff9-140">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="d1ff9-141">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d1ff9-141">Relevant Properties</span></span>

<span data-ttu-id="d1ff9-142">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-142">The following table lists the UI Automation properties whose value or definition is especially relevant to slider controls.</span></span> <span data-ttu-id="d1ff9-143">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="d1ff9-143">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="d1ff9-144">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="d1ff9-144">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="d1ff9-145">Value</span><span class="sxs-lookup"><span data-stu-id="d1ff9-145">Value</span></span>      | <span data-ttu-id="d1ff9-146">Notas</span><span class="sxs-lookup"><span data-stu-id="d1ff9-146">Notes</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1ff9-147">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-147">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="d1ff9-148">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-148">See notes.</span></span> | <span data-ttu-id="d1ff9-149">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-149">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="d1ff9-150">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-150">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="d1ff9-151">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-151">See notes.</span></span> | <span data-ttu-id="d1ff9-152">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-152">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="d1ff9-153">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-153">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="d1ff9-154">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-154">See notes.</span></span> | <span data-ttu-id="d1ff9-155">La mayoría de los controles deslizantes debe devolver el error [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) porque todo el rectángulo delimitador del control deslizante está ocupado por controles secundarios.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-155">The majority of slider controls must return the [**UIA\_E\_NOCLICKABLEPOINT**](uiauto-error-codes.md) error because the entire bounding rectangle of the slider control is occupied by child controls.</span></span> |
| [<span data-ttu-id="d1ff9-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="d1ff9-157">**Control deslizante**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-157">**Slider**</span></span> | <span data-ttu-id="d1ff9-158">Este valor es el mismo para todos los marcos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-158">This value is the same for all frameworks.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="d1ff9-159">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d1ff9-160">TRUE</span><span class="sxs-lookup"><span data-stu-id="d1ff9-160">TRUE</span></span>       | <span data-ttu-id="d1ff9-161">El control deslizante siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-161">The slider control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="d1ff9-162">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d1ff9-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="d1ff9-163">TRUE</span></span>       | <span data-ttu-id="d1ff9-164">El control deslizante siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-164">The slider control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="d1ff9-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="d1ff9-166">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-166">See notes.</span></span> | <span data-ttu-id="d1ff9-167">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="d1ff9-168">Los elementos secundarios (botones y Thumb) de un control deslizante nunca deben tener el foco.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-168">The children (buttons and thumb) of a slider control should never take the focus.</span></span> <span data-ttu-id="d1ff9-169">El foco siempre debe permanecer en el control deslizante.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-169">The focus should always remain on the slider control itself.</span></span>       |
| [<span data-ttu-id="d1ff9-170">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="d1ff9-171">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-171">See notes.</span></span> | <span data-ttu-id="d1ff9-172">Si hay una etiqueta de texto estático asociada al control, esta propiedad debe exponer una referencia a ese control.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-172">If there is a static text label associated with the control, this property must expose a reference to that control.</span></span> <span data-ttu-id="d1ff9-173">Si el control de texto es un subcomponente de otro control, no tendrá un conjunto de propiedades **LabeledBy** .</span><span class="sxs-lookup"><span data-stu-id="d1ff9-173">If the text control is a subcomponent of another control, it will not have a **LabeledBy** property set.</span></span>   |
| [<span data-ttu-id="d1ff9-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="d1ff9-175">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-175">See notes.</span></span> | <span data-ttu-id="d1ff9-176">Cadena localizada que corresponde al tipo de control **Slider** .</span><span class="sxs-lookup"><span data-stu-id="d1ff9-176">Localized string corresponding to the **Slider** control type.</span></span> <span data-ttu-id="d1ff9-177">El valor predeterminado es "slider" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="d1ff9-177">The default value is "slider" for en-US or English (United States).</span></span>                                                                                             |
| [<span data-ttu-id="d1ff9-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="d1ff9-179">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-179">See notes.</span></span> | <span data-ttu-id="d1ff9-180">El nombre del control deslizante se genera normalmente a partir de una etiqueta de texto estático.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-180">The name of the slider control is typically generated from a static text label.</span></span> <span data-ttu-id="d1ff9-181">Si no hay una etiqueta de texto estático, el desarrollador de la aplicación debe asignar un valor de propiedad para **nombre** .</span><span class="sxs-lookup"><span data-stu-id="d1ff9-181">If there is not a static text label, a property value for **Name** must be assigned by the application developer.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="d1ff9-182">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="d1ff9-182">Required Control Patterns</span></span>

<span data-ttu-id="d1ff9-183">En la tabla siguiente se enumeran los patrones de control de UI Automation que deben admitir todos los controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-183">The following table lists the UI Automation control patterns required to be supported by all slider controls.</span></span> <span data-ttu-id="d1ff9-184">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d1ff9-184">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="d1ff9-185">Patrón de control/Propiedad de patrón</span><span class="sxs-lookup"><span data-stu-id="d1ff9-185">Control Pattern/Pattern Property</span></span>                          | <span data-ttu-id="d1ff9-186">Soporte técnico/valor</span><span class="sxs-lookup"><span data-stu-id="d1ff9-186">Support/Value</span></span> | <span data-ttu-id="d1ff9-187">Notas</span><span class="sxs-lookup"><span data-stu-id="d1ff9-187">Notes</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1ff9-188">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-188">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | <span data-ttu-id="d1ff9-189">Depende</span><span class="sxs-lookup"><span data-stu-id="d1ff9-189">Depends</span></span>       | <span data-ttu-id="d1ff9-190">Un control deslizante debe admitir el patrón de control [RangeValue](uiauto-implementingrangevalue.md) si el contenido se puede establecer en un valor dentro de un intervalo numérico.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-190">A slider should support the [RangeValue](uiauto-implementingrangevalue.md) control pattern if the content can be set to a value within a numerical range.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="d1ff9-191">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-191">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | <span data-ttu-id="d1ff9-192">Depende</span><span class="sxs-lookup"><span data-stu-id="d1ff9-192">Depends</span></span>       | <span data-ttu-id="d1ff9-193">Un control deslizante debe admitir el patrón de control [Selection](uiauto-implementingselection.md) si el contenido representa un valor entre un conjunto discreto de opciones.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-193">A slider should support the [Selection](uiauto-implementingselection.md) control pattern if the content represents one value among a discrete set of options.</span></span> <span data-ttu-id="d1ff9-194">Si se admite el patrón de control Selection, la selección correspondiente se debe exponer como uno o varios elementos de lista secundarios del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-194">When the Selection control pattern is supported, the corresponding selection must be exposed as one or more child list items of the slider.</span></span> |
| [<span data-ttu-id="d1ff9-195">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-195">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | <span data-ttu-id="d1ff9-196">Depende</span><span class="sxs-lookup"><span data-stu-id="d1ff9-196">Depends</span></span>       | <span data-ttu-id="d1ff9-197">Un control deslizante debe admitir el patrón de control [Value](uiauto-implementingvalue.md) si el contenido representa un valor entre un conjunto discreto de opciones.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-197">A slider should support the [Value](uiauto-implementingvalue.md) control pattern if the content represents one value among a discrete set of options.</span></span>                                                                                                                                                     |



 

## <a name="required-events"></a><span data-ttu-id="d1ff9-198">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="d1ff9-198">Required Events</span></span>

<span data-ttu-id="d1ff9-199">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles deslizantes deben admitir.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-199">The following table lists the UI Automation events that slider controls are required to support.</span></span> <span data-ttu-id="d1ff9-200">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d1ff9-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="d1ff9-201">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="d1ff9-201">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="d1ff9-202">Notas</span><span class="sxs-lookup"><span data-stu-id="d1ff9-202">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1ff9-203">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="d1ff9-204">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="d1ff9-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="d1ff9-206">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="d1ff9-207">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="d1ff9-208">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="d1ff9-209">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de RangeValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-209">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="d1ff9-210">Si el control admite el patrón de control [RangeValue](uiauto-implementingrangevalue.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-210">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="d1ff9-211">**\_InvalidatedEventId de selección de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-211">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                       | <span data-ttu-id="d1ff9-212">Si el control admite el patrón de control [Selection](uiauto-implementingselection.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-212">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="d1ff9-213">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="d1ff9-214">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-214">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="d1ff9-215">Si el control admite el patrón de control [Value](uiauto-implementingvalue.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-215">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="d1ff9-216">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1ff9-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d1ff9-217">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d1ff9-217">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d1ff9-218">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="d1ff9-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="d1ff9-219">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="d1ff9-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




