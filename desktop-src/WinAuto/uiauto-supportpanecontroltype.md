---
title: Pane (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control pane.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control pane
- Automatización de la interfaz de usuario, panel (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control pane
- Automatización de la interfaz de usuario, propiedades para el tipo de control pane
- Automatización de la interfaz de usuario, patrones de control para el tipo de control pane
- Automatización de la interfaz de usuario, eventos para el tipo de control pane
- estructuras de árbol, tipo de control pane
- propiedades, panel (tipo de control)
- patrones de control, panel (tipo de control)
- Events, pane (tipo de control)
- compatibilidad con el tipo de control pane
- Pane (tipo de control)
- tipos de control, estructura de árbol para el tipo de control pane
- tipos de control, patrones de control para el tipo de control pane
- tipos de control, compatibilidad con el panel
- tipos de control, panel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51b7f22e6fb302ebb160a174c27c61119b8f09fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104561778"
---
# <a name="pane-control-type"></a><span data-ttu-id="2c1ff-119">Pane (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="2c1ff-119">Pane Control Type</span></span>

<span data-ttu-id="2c1ff-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **pane** .</span><span class="sxs-lookup"><span data-stu-id="2c1ff-120">This topic provides information about Microsoft UI Automation support for the **Pane** control type.</span></span>

<span data-ttu-id="2c1ff-121">El tipo de control **pane** es para las regiones posiblemente desplazables que tienen contenido dispares.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-121">The **Pane** control type is for potentially scrollable regions that have disparate content.</span></span> <span data-ttu-id="2c1ff-122">Se utiliza para representar un objeto dentro de una ventana de documento o marco.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-122">It is used to represent an object within a frame or document window.</span></span> <span data-ttu-id="2c1ff-123">Los usuarios pueden desplazarse entre los controles de panel y dentro del contenido del panel actual.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-123">Users can navigate between pane controls and within the contents of the current pane.</span></span> <span data-ttu-id="2c1ff-124">Los controles de panel representan un nivel de agrupación inferior a ventanas o documentos, pero por encima de los controles individuales.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-124">Pane controls represent a level of grouping lower than windows or documents, but above individual controls.</span></span> <span data-ttu-id="2c1ff-125">El usuario navega entre paneles presionando TAB, F6 o CTRL+TAB, dependiendo del contexto.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-125">The user navigates between panes by pressing TAB, F6, or CTRL+TAB, depending on the context.</span></span>

<span data-ttu-id="2c1ff-126">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **pane** .</span><span class="sxs-lookup"><span data-stu-id="2c1ff-126">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Pane** control type.</span></span> <span data-ttu-id="2c1ff-127">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de panel donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-127">The UI Automation requirements apply to all pane controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="2c1ff-128">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-128">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2c1ff-129">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="2c1ff-129">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="2c1ff-130">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="2c1ff-130">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="2c1ff-131">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="2c1ff-131">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="2c1ff-132">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="2c1ff-132">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="2c1ff-133">Ejemplo de tipo de control de panel</span><span class="sxs-lookup"><span data-stu-id="2c1ff-133">Pane Control Type Example</span></span>](#pane-control-type-example)
-   [<span data-ttu-id="2c1ff-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c1ff-134">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="2c1ff-135">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="2c1ff-135">Typical Tree Structure</span></span>

<span data-ttu-id="2c1ff-136">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de panel y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-136">The following table depicts a typical control and content view of the UI Automation tree that pertains to pane controls and describes what can be contained in each view.</span></span> <span data-ttu-id="2c1ff-137">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2c1ff-137">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c1ff-138">Vista de control</span><span class="sxs-lookup"><span data-stu-id="2c1ff-138">Control View</span></span></th>
<th><span data-ttu-id="2c1ff-139">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="2c1ff-139">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2c1ff-140">Panel</span><span class="sxs-lookup"><span data-stu-id="2c1ff-140">Pane</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2c1ff-141">Panel</span><span class="sxs-lookup"><span data-stu-id="2c1ff-141">Pane</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2c1ff-142">Un control de panel siempre aparece en las vistas de control y de contenido.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-142">A pane control always appears in the control and content views.</span></span> <span data-ttu-id="2c1ff-143">No exponga un objeto de diseño como un panel en la vista de control o de contenido si el objeto solo se usa para la presentación visual.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-143">Do not expose a layout object as a pane in either the control or content view if the object is used only for visual presentation.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="2c1ff-144">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="2c1ff-144">Relevant Properties</span></span>

<span data-ttu-id="2c1ff-145">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de panel.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-145">The following table lists the UI Automation properties whose value or definition is especially relevant to pane controls.</span></span> <span data-ttu-id="2c1ff-146">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="2c1ff-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="2c1ff-147">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="2c1ff-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="2c1ff-148">Value</span><span class="sxs-lookup"><span data-stu-id="2c1ff-148">Value</span></span>      | <span data-ttu-id="2c1ff-149">Notas</span><span class="sxs-lookup"><span data-stu-id="2c1ff-149">Notes</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c1ff-150">**UIA \_ AccessKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-150">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="2c1ff-151">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-151">See notes.</span></span> | <span data-ttu-id="2c1ff-152">Si una combinación de teclas específica proporciona el foco al panel, dicha información debería exponerse a través de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-152">If a specific key combination gives focus to the pane, that information should be exposed through this property.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="2c1ff-153">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-153">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="2c1ff-154">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-154">See notes.</span></span> | <span data-ttu-id="2c1ff-155">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-155">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="2c1ff-156">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-156">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="2c1ff-157">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-157">See notes.</span></span> | <span data-ttu-id="2c1ff-158">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-158">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="2c1ff-159">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-159">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="2c1ff-160">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-160">See notes.</span></span> | <span data-ttu-id="2c1ff-161">Esta propiedad expone un punto en el que se puede hacer clic del control de panel que hace que el enfoque se sitúe en el panel cuando se hace clic en él.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-161">This property exposes a clickable point of the pane control that causes the pane to become focused when it is clicked.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="2c1ff-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="2c1ff-163">**Panel**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-163">**Pane**</span></span>   |                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="2c1ff-164">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="2c1ff-165">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-165">See notes.</span></span> | <span data-ttu-id="2c1ff-166">El texto de ayuda de los controles de panel debe explicar el propósito del marco y cómo se relaciona con otros marcos.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-166">The help text for pane controls should explain the purpose of the frame and how it relates to other frames.</span></span> <span data-ttu-id="2c1ff-167">Se necesita una descripción si el propósito y la relación de los marcos no están claros en el valor de la propiedad [**\_ NamePropertyId de UIA**](uiauto-automation-element-propids.md) .</span><span class="sxs-lookup"><span data-stu-id="2c1ff-167">A description is necessary if the purpose and relationship of the frames is not clear from the value of the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span> |
| [<span data-ttu-id="2c1ff-168">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="2c1ff-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="2c1ff-169">TRUE</span></span>       | <span data-ttu-id="2c1ff-170">El control de panel siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-170">The pane control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="2c1ff-171">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="2c1ff-172">TRUE</span><span class="sxs-lookup"><span data-stu-id="2c1ff-172">TRUE</span></span>       | <span data-ttu-id="2c1ff-173">El control de panel siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-173">The pane control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="2c1ff-174">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="2c1ff-175">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-175">See notes.</span></span> | <span data-ttu-id="2c1ff-176">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="2c1ff-177">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="2c1ff-178">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-178">See notes.</span></span> | <span data-ttu-id="2c1ff-179">Los controles de panel normalmente no tienen una etiqueta estática.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-179">Pane controls typically do not have a static label.</span></span> <span data-ttu-id="2c1ff-180">Si hay una etiqueta de texto estático, se debe exponer a través de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-180">If there is a static text label, it should be exposed through this property.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="2c1ff-181">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-181">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="2c1ff-182">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-182">See notes.</span></span> | <span data-ttu-id="2c1ff-183">Cadena localizada que corresponde al tipo de control **pane** .</span><span class="sxs-lookup"><span data-stu-id="2c1ff-183">Localized string corresponding to the **Pane** control type.</span></span> <span data-ttu-id="2c1ff-184">El valor predeterminado es "Pane" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="2c1ff-184">The default value is "pane" for en-US or English (United States).</span></span>                                                                                                                                                                                        |
| [<span data-ttu-id="2c1ff-185">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-185">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="2c1ff-186">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-186">See notes.</span></span> | <span data-ttu-id="2c1ff-187">El valor de esta propiedad siempre debe ser un título claro, conciso y significativo.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-187">The value for this property must always be a clear, concise and meaningful title.</span></span>                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="2c1ff-188">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="2c1ff-188">Required Control Patterns</span></span>

<span data-ttu-id="2c1ff-189">En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por los controles de panel.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-189">The following table lists the UI Automation control patterns required to be supported by pane controls.</span></span> <span data-ttu-id="2c1ff-190">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2c1ff-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="2c1ff-191">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="2c1ff-191">Control Pattern</span></span>                                         | <span data-ttu-id="2c1ff-192">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="2c1ff-192">Support</span></span> | <span data-ttu-id="2c1ff-193">Notas</span><span class="sxs-lookup"><span data-stu-id="2c1ff-193">Notes</span></span>                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c1ff-194">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-194">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | <span data-ttu-id="2c1ff-195">Depende</span><span class="sxs-lookup"><span data-stu-id="2c1ff-195">Depends</span></span> | <span data-ttu-id="2c1ff-196">Implemente el patrón de control [Dock](uiauto-implementingdock.md) si el control de panel se puede acoplar.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-196">Implement the [Dock](uiauto-implementingdock.md) control pattern if the pane control can be docked.</span></span>                                                                                          |
| [<span data-ttu-id="2c1ff-197">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-197">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="2c1ff-198">Depende</span><span class="sxs-lookup"><span data-stu-id="2c1ff-198">Depends</span></span> | <span data-ttu-id="2c1ff-199">Implemente el patrón de control [Scroll](uiauto-implementingscroll.md) si se puede desplazar el control de panel.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-199">Implement the [Scroll](uiauto-implementingscroll.md) control pattern if the pane control can be scrolled.</span></span>                                                                                    |
| [<span data-ttu-id="2c1ff-200">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-200">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="2c1ff-201">Depende</span><span class="sxs-lookup"><span data-stu-id="2c1ff-201">Depends</span></span> | <span data-ttu-id="2c1ff-202">Implemente el patrón de control [Transform](uiauto-implementingtransform.md) si el control de panel se puede desplazar, cambiar de tamaño o girar en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-202">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the pane control can be moved, resized, or rotated on the screen.</span></span>                                              |
| [<span data-ttu-id="2c1ff-203">**IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-203">**IWindowProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | <span data-ttu-id="2c1ff-204">Nunca</span><span class="sxs-lookup"><span data-stu-id="2c1ff-204">Never</span></span>   | <span data-ttu-id="2c1ff-205">Si el elemento necesita implementar el patrón de control [Window](uiauto-implementingwindow.md) , el control debe basarse en el tipo de control [Window](uiauto-supportwindowcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="2c1ff-205">If the element needs to implement the [Window](uiauto-implementingwindow.md) control pattern, the control should be based on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="2c1ff-206">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="2c1ff-206">Required Events</span></span>

<span data-ttu-id="2c1ff-207">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que admiten los controles de panel.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-207">The following table lists the UI Automation events that pane controls are required to support.</span></span> <span data-ttu-id="2c1ff-208">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2c1ff-208">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="2c1ff-209">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="2c1ff-209">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="2c1ff-210">Notas</span><span class="sxs-lookup"><span data-stu-id="2c1ff-210">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c1ff-211">**UIA \_ AsyncContentLoadedEventId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-211">**UIA\_AsyncContentLoadedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [<span data-ttu-id="2c1ff-212">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-212">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="2c1ff-213">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-213">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="2c1ff-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="2c1ff-215">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="2c1ff-216">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-216">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="2c1ff-217">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-217">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="2c1ff-218">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-218">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="2c1ff-219">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-219">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="2c1ff-220">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-220">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="2c1ff-221">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-221">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="2c1ff-222">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-222">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="2c1ff-223">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-223">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="2c1ff-224">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-224">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="2c1ff-225">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-225">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="2c1ff-226">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-226">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="2c1ff-227">Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="2c1ff-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="2c1ff-228">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-228">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a><span data-ttu-id="2c1ff-229">Ejemplo de tipo de control de panel</span><span class="sxs-lookup"><span data-stu-id="2c1ff-229">Pane Control Type Example</span></span>

<span data-ttu-id="2c1ff-230">En la imagen siguiente se muestra un control que implementa el tipo de control **pane** .</span><span class="sxs-lookup"><span data-stu-id="2c1ff-230">The following image illustrates a control that implements the **Pane** control type.</span></span>

![captura de pantalla que muestra un ejemplo de un control de panel](images/panexmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c1ff-232">Árbol de UI Automation: vista de control</span><span class="sxs-lookup"><span data-stu-id="2c1ff-232">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="2c1ff-233">Árbol de UI Automation: vista de contenido</span><span class="sxs-lookup"><span data-stu-id="2c1ff-233">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2c1ff-234">Panel</span><span class="sxs-lookup"><span data-stu-id="2c1ff-234">Pane</span></span>
<ul>
<li><span data-ttu-id="2c1ff-235">Tree (patrón de desplazamiento)</span><span class="sxs-lookup"><span data-stu-id="2c1ff-235">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="2c1ff-236">TreeItem</span><span class="sxs-lookup"><span data-stu-id="2c1ff-236">TreeItem</span></span></li>
<li><span data-ttu-id="2c1ff-237">...</span><span class="sxs-lookup"><span data-stu-id="2c1ff-237">...</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="2c1ff-238">Panel</span><span class="sxs-lookup"><span data-stu-id="2c1ff-238">Pane</span></span>
<ul>
<li><span data-ttu-id="2c1ff-239">Edit (patrón de desplazamiento)</span><span class="sxs-lookup"><span data-stu-id="2c1ff-239">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2c1ff-240">Panel</span><span class="sxs-lookup"><span data-stu-id="2c1ff-240">Pane</span></span>
<ul>
<li><span data-ttu-id="2c1ff-241">Tree (patrón de desplazamiento)</span><span class="sxs-lookup"><span data-stu-id="2c1ff-241">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="2c1ff-242">TreeItem</span><span class="sxs-lookup"><span data-stu-id="2c1ff-242">TreeItem</span></span></li>
<li><span data-ttu-id="2c1ff-243">...</span><span class="sxs-lookup"><span data-stu-id="2c1ff-243">...</span></span></li>
</ul></li>
<li><span data-ttu-id="2c1ff-244">Panel</span><span class="sxs-lookup"><span data-stu-id="2c1ff-244">Pane</span></span>
<ul>
<li><span data-ttu-id="2c1ff-245">Edit (patrón de desplazamiento)</span><span class="sxs-lookup"><span data-stu-id="2c1ff-245">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2c1ff-246">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c1ff-246">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2c1ff-247">**Vista**</span><span class="sxs-lookup"><span data-stu-id="2c1ff-247">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2c1ff-248">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="2c1ff-248">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="2c1ff-249">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="2c1ff-249">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




