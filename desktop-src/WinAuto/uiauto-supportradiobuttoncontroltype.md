---
title: RadioButton (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control RadioButton.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control RadioButton
- Automatización de la interfaz de usuario, RadioButton (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control RadioButton
- Automatización de la interfaz de usuario, propiedades para el tipo de control RadioButton
- Automatización de la interfaz de usuario, patrones de control para el tipo de control RadioButton
- Automatización de la interfaz de usuario, eventos para el tipo de control RadioButton
- estructuras de árbol, tipo de control RadioButton
- propiedades, RadioButton (tipo de control)
- patrones de control, RadioButton (tipo de control)
- Events, RadioButton (tipo de control)
- compatibilidad con el tipo de control RadioButton
- RadioButton (tipo de control)
- tipos de control, estructura de árbol para el tipo de control RadioButton
- tipos de control, patrones de control para el tipo de control RadioButton
- tipos de control, compatibilidad con RadioButton
- tipos de control, RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702a2227a5164ff694378c82fa3b7cde33f9823
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778240"
---
# <a name="radiobutton-control-type"></a><span data-ttu-id="78e56-119">RadioButton (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="78e56-119">RadioButton Control Type</span></span>

<span data-ttu-id="78e56-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="78e56-120">This topic provides information about Microsoft UI Automation support for the **RadioButton** control type.</span></span>

<span data-ttu-id="78e56-121">Un botón de opción consta de un botón redondo y de texto definido por la aplicación (una etiqueta), un icono o un mapa de bits que indica una opción que el usuario puede realizar seleccionando el botón.</span><span class="sxs-lookup"><span data-stu-id="78e56-121">A radio button consists of a round button and application-defined text (a label), an icon, or a bitmap that indicates a choice the user can make by selecting the button.</span></span> <span data-ttu-id="78e56-122">Normalmente, una aplicación usa botones de radio en un cuadro de grupo para permitir al usuario elegir entre un conjunto de opciones relacionadas, aunque mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="78e56-122">An application typically uses radio buttons in a group box to permit the user to choose from a set of related, but mutually exclusive options.</span></span> <span data-ttu-id="78e56-123">Por ejemplo, la aplicación puede presentar un grupo de botones de radio desde el que el usuario puede seleccionar una preferencia de formato para el texto seleccionado en el área del cliente.</span><span class="sxs-lookup"><span data-stu-id="78e56-123">For example, the application might present a group of radio buttons from which the user can select a format preference for text selected in the client area.</span></span> <span data-ttu-id="78e56-124">El usuario podría seleccionar un formato alineado a la izquierda, alineado a la derecha o centrado seleccionando el botón de radio correspondiente.</span><span class="sxs-lookup"><span data-stu-id="78e56-124">The user could select a left-aligned, right-aligned, or centered format by selecting the corresponding radio button.</span></span> <span data-ttu-id="78e56-125">Normalmente, el usuario solo puede seleccionar una opción cada vez a partir de un conjunto de botones de radio.</span><span class="sxs-lookup"><span data-stu-id="78e56-125">Typically, the user can select only one option at a time from a set of radio buttons.</span></span>

> [!Note]  
> <span data-ttu-id="78e56-126">Otra generalización del control para los botones en los que solo se puede seleccionar uno de los grupos es el contenido de un botón de alternancia.</span><span class="sxs-lookup"><span data-stu-id="78e56-126">Another control generalization for buttons where only one in a group can be selected is the content of a toggle button.</span></span> <span data-ttu-id="78e56-127">Algunos marcos de interfaz de usuario consideran que un botón de radio sea un botón de alternancia especializado.</span><span class="sxs-lookup"><span data-stu-id="78e56-127">Some UI frameworks consider a radio button to be a specialized toggle button.</span></span>

 

<span data-ttu-id="78e56-128">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="78e56-128">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **RadioButton** control type.</span></span> <span data-ttu-id="78e56-129">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de botón donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control</span><span class="sxs-lookup"><span data-stu-id="78e56-129">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="78e56-130">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="78e56-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="78e56-131">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="78e56-131">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="78e56-132">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="78e56-132">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="78e56-133">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="78e56-133">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="78e56-134">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="78e56-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="78e56-135">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="78e56-135">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="78e56-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78e56-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="78e56-137">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="78e56-137">Typical Tree Structure</span></span>

<span data-ttu-id="78e56-138">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de botón de radio y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="78e56-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to radio button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="78e56-139">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="78e56-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78e56-140">Vista de control</span><span class="sxs-lookup"><span data-stu-id="78e56-140">Control View</span></span></th>
<th><span data-ttu-id="78e56-141">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="78e56-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="78e56-142">RadioButton</span><span class="sxs-lookup"><span data-stu-id="78e56-142">RadioButton</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="78e56-143">RadioButton</span><span class="sxs-lookup"><span data-stu-id="78e56-143">RadioButton</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="78e56-144">No hay ningún elemento secundario en la vista de control o la vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="78e56-144">There are no children in the control view or the content view.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="78e56-145">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="78e56-145">Relevant Properties</span></span>

<span data-ttu-id="78e56-146">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles que implementan el tipo de control **RadioButton** (como los controles de botón).</span><span class="sxs-lookup"><span data-stu-id="78e56-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **RadioButton** control type (such as button controls).</span></span> <span data-ttu-id="78e56-147">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="78e56-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="78e56-148">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="78e56-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="78e56-149">Value</span><span class="sxs-lookup"><span data-stu-id="78e56-149">Value</span></span>           | <span data-ttu-id="78e56-150">Notas</span><span class="sxs-lookup"><span data-stu-id="78e56-150">Notes</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78e56-151">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="78e56-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="78e56-152">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="78e56-152">See notes.</span></span>      | <span data-ttu-id="78e56-153">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="78e56-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                  |
| [<span data-ttu-id="78e56-154">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="78e56-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="78e56-155">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="78e56-155">See notes.</span></span>      | <span data-ttu-id="78e56-156">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="78e56-156">The outermost rectangle that contains the whole control.</span></span>                                                                                      |
| [<span data-ttu-id="78e56-157">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="78e56-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="78e56-158">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="78e56-158">See notes.</span></span>      | <span data-ttu-id="78e56-159">El punto en el que se puede hacer clic debe ser un punto que, al hacer clic en él, seleccione el botón de radio.</span><span class="sxs-lookup"><span data-stu-id="78e56-159">The clickable point must be a point that, when clicked, selects the radio button.</span></span>                                                             |
| [<span data-ttu-id="78e56-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="78e56-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="78e56-161">**RadioButton**</span><span class="sxs-lookup"><span data-stu-id="78e56-161">**RadioButton**</span></span> |                                                                                                                                               |
| [<span data-ttu-id="78e56-162">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="78e56-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="78e56-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="78e56-163">TRUE</span></span>            | <span data-ttu-id="78e56-164">El control de botón de radio siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="78e56-164">The radio button control is always included in the content view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="78e56-165">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="78e56-165">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="78e56-166">TRUE</span><span class="sxs-lookup"><span data-stu-id="78e56-166">TRUE</span></span>            | <span data-ttu-id="78e56-167">El control de botón de radio siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="78e56-167">The radio button control is always included in the control view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="78e56-168">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="78e56-168">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="78e56-169">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="78e56-169">See notes.</span></span>      | <span data-ttu-id="78e56-170">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="78e56-170">If the control can receive keyboard focus, it must support this property.</span></span>                                                                     |
| [<span data-ttu-id="78e56-171">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="78e56-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="78e56-172">NULL</span><span class="sxs-lookup"><span data-stu-id="78e56-172">NULL</span></span>            | <span data-ttu-id="78e56-173">Los controles de botón de radio se etiquetan automáticamente por su contenido.</span><span class="sxs-lookup"><span data-stu-id="78e56-173">Radio button controls are self-labeled by their contents.</span></span>                                                                                     |
| [<span data-ttu-id="78e56-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="78e56-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="78e56-175">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="78e56-175">See notes.</span></span>      | <span data-ttu-id="78e56-176">Cadena localizada que corresponde al tipo de control **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="78e56-176">Localized string corresponding to the **RadioButton** control type.</span></span> <span data-ttu-id="78e56-177">El valor predeterminado es "botón de radio" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="78e56-177">The default value is "radio button" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="78e56-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="78e56-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="78e56-179">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="78e56-179">See notes.</span></span>      | <span data-ttu-id="78e56-180">El nombre del control de botón de radio es el texto que se muestra junto al botón que mantiene el estado de la selección.</span><span class="sxs-lookup"><span data-stu-id="78e56-180">The name of the radio button control is the text that is displayed beside the button that maintains the selection state.</span></span>                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="78e56-181">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="78e56-181">Required Control Patterns</span></span>

<span data-ttu-id="78e56-182">En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de botón de radio.</span><span class="sxs-lookup"><span data-stu-id="78e56-182">The following table lists the UI Automation control patterns required to be supported by all radio button controls.</span></span> <span data-ttu-id="78e56-183">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="78e56-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="78e56-184">Patrón de control/Propiedad de patrón</span><span class="sxs-lookup"><span data-stu-id="78e56-184">Control Pattern/Pattern Property</span></span>                                               | <span data-ttu-id="78e56-185">Soporte técnico/valor</span><span class="sxs-lookup"><span data-stu-id="78e56-185">Support/Value</span></span> | <span data-ttu-id="78e56-186">Notas</span><span class="sxs-lookup"><span data-stu-id="78e56-186">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78e56-187">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="78e56-187">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | <span data-ttu-id="78e56-188">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="78e56-188">Required</span></span>      | <span data-ttu-id="78e56-189">Todos los controles de botón de radio deben admitir el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) para permitir que se seleccionen.</span><span class="sxs-lookup"><span data-stu-id="78e56-189">All radio button controls must support the [SelectionItem](uiauto-implementingselectionitem.md) control pattern to enable themselves to be selected.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="78e56-190">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="78e56-190">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | <span data-ttu-id="78e56-191">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="78e56-191">See notes.</span></span>    | <span data-ttu-id="78e56-192">La propiedad [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) siempre se debe completar para que un cliente de automatización de la interfaz de usuario pueda determinar qué otros botones de radio dentro de un contexto específico se relacionan entre sí.</span><span class="sxs-lookup"><span data-stu-id="78e56-192">The [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) property must always be completed so that a UI Automation client can determine what other radio buttons within a specific context relate to one another.</span></span> <span data-ttu-id="78e56-193">En la versión de Microsoft Win32 del botón de radio, esta propiedad no se admite porque no es posible obtener esta información de ese marco de trabajo heredado.</span><span class="sxs-lookup"><span data-stu-id="78e56-193">For the Microsoft Win32 version of the radio button, this property is not supported because it is not possible to obtain this information from that legacy framework.</span></span> |
| [<span data-ttu-id="78e56-194">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="78e56-194">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | <span data-ttu-id="78e56-195">Nunca</span><span class="sxs-lookup"><span data-stu-id="78e56-195">Never</span></span>         | <span data-ttu-id="78e56-196">El botón de radio no puede recorrer cíclicamente su estado una vez que se ha establecido.</span><span class="sxs-lookup"><span data-stu-id="78e56-196">The radio button cannot cycle through its state once it has been set.</span></span> <span data-ttu-id="78e56-197">Nunca se debe admitir el patrón de control [Toggle](uiauto-implementingtoggle.md) en un botón de radio.</span><span class="sxs-lookup"><span data-stu-id="78e56-197">The [Toggle](uiauto-implementingtoggle.md) control pattern must never be supported on a radio button.</span></span>                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a><span data-ttu-id="78e56-198">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="78e56-198">Required Events</span></span>

<span data-ttu-id="78e56-199">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de botón deben admitir.</span><span class="sxs-lookup"><span data-stu-id="78e56-199">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="78e56-200">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="78e56-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="78e56-201">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="78e56-201">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="78e56-202">Notas</span><span class="sxs-lookup"><span data-stu-id="78e56-202">Notes</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78e56-203">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="78e56-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                                |
| <span data-ttu-id="78e56-204">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="78e56-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                                |
| <span data-ttu-id="78e56-205">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="78e56-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="78e56-206">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="78e56-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="78e56-207">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="78e56-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="78e56-208">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="78e56-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>     |
| [<span data-ttu-id="78e56-209">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="78e56-209">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="78e56-210">Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="78e56-210">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="78e56-211">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="78e56-211">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="78e56-212">Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="78e56-212">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="78e56-213">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="78e56-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="78e56-214">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78e56-214">Remarks</span></span>

<span data-ttu-id="78e56-215">Un botón de radio representa una única opción seleccionable entre un grupo de botones de radio del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="78e56-215">A radio button represents a single selectable option among a group of peer radio buttons.</span></span> <span data-ttu-id="78e56-216">Idealmente, los botones de radio deben tener un elemento de agrupación que clarifica los límites de los botones de radio del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="78e56-216">Ideally, radio buttons should have a grouping element that clarifies the boundaries of the peer radio buttons.</span></span> <span data-ttu-id="78e56-217">Sin embargo, a menudo el límite está implícito en la estructura del elemento de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="78e56-217">Often, however, the boundary is implied by the UI element structure.</span></span> <span data-ttu-id="78e56-218">Por ejemplo, un menú puede contener un conjunto de botones de radio consecutivos en lugar de elementos de menú, o un conjunto de botones de radio que se producen después de una etiqueta de grupo, pero antes de un elemento accionable como Button.</span><span class="sxs-lookup"><span data-stu-id="78e56-218">For example, a menu might contain a set of consecutive radio buttons instead of menu items, or a set of radio buttons that occur after a group label, but before an actionable element such as button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78e56-219">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78e56-219">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="78e56-220">**Vista**</span><span class="sxs-lookup"><span data-stu-id="78e56-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="78e56-221">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="78e56-221">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="78e56-222">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="78e56-222">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




