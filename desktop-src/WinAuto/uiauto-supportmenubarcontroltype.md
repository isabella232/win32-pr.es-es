---
title: MenuBar (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control MenuBar.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control MenuBar
- UI Automation, MenuBar (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control MenuBar
- Automatización de la interfaz de usuario, propiedades para el tipo de control MenuBar
- Automatización de la interfaz de usuario, patrones de control para el tipo de control MenuBar
- Automatización de la interfaz de usuario, eventos para el tipo de control MenuBar
- estructuras de árbol, tipo de control MenuBar
- Properties, MenuBar (tipo de control)
- patrones de control, MenuBar (tipo de control)
- Events, MenuBar (tipo de control)
- compatibilidad con el tipo de control MenuBar
- MenuBar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control MenuBar
- tipos de control, patrones de control para el tipo de control MenuBar
- tipos de control, compatibilidad con MenuBar
- tipos de control, barra de menús
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94bb60c13b5999bc8020eb70b84f6c932a2fb94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695302"
---
# <a name="menubar-control-type"></a><span data-ttu-id="c0b29-119">MenuBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="c0b29-119">MenuBar Control Type</span></span>

<span data-ttu-id="c0b29-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="c0b29-120">This topic provides information about Microsoft UI Automation support for the **MenuBar** control type.</span></span>

<span data-ttu-id="c0b29-121">Los controles de barra de menús son un ejemplo de controles que implementan el tipo de control **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="c0b29-121">Menu bar controls are an example of controls that implement the **MenuBar** control type.</span></span> <span data-ttu-id="c0b29-122">Las barras de menús proporcionan un medio para que los usuarios activen los comandos y las opciones contenidos en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c0b29-122">Menu bars provide a means for users to activate commands and options contained in an application.</span></span>

<span data-ttu-id="c0b29-123">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="c0b29-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **MenuBar** control type.</span></span> <span data-ttu-id="c0b29-124">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de barra de menús donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control</span><span class="sxs-lookup"><span data-stu-id="c0b29-124">The UI Automation requirements apply to all menu bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="c0b29-125">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="c0b29-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c0b29-126">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="c0b29-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="c0b29-127">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="c0b29-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="c0b29-128">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="c0b29-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="c0b29-129">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="c0b29-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="c0b29-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0b29-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="c0b29-131">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="c0b29-131">Typical Tree Structure</span></span>

<span data-ttu-id="c0b29-132">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de barra de menús y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="c0b29-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="c0b29-133">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c0b29-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0b29-134">Vista de control</span><span class="sxs-lookup"><span data-stu-id="c0b29-134">Control View</span></span></th>
<th><span data-ttu-id="c0b29-135">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="c0b29-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="c0b29-136">MenuBar</span><span class="sxs-lookup"><span data-stu-id="c0b29-136">MenuBar</span></span>
<ul>
<li><span data-ttu-id="c0b29-137">MenuItem (1 o más)</span><span class="sxs-lookup"><span data-stu-id="c0b29-137">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="c0b29-138">Otros controles (0 o varios)</span><span class="sxs-lookup"><span data-stu-id="c0b29-138">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c0b29-139">No aplicable</span><span class="sxs-lookup"><span data-stu-id="c0b29-139">Not applicable</span></span>
<ul>
<li><span data-ttu-id="c0b29-140">MenuItem (1 o más)</span><span class="sxs-lookup"><span data-stu-id="c0b29-140">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="c0b29-141">Otros controles (0 o varios)</span><span class="sxs-lookup"><span data-stu-id="c0b29-141">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c0b29-142">Un control de barra de menús siempre aparece en la vista de control, pero no en la vista de contenido porque normalmente no transmite información significativa al usuario final (a menos que la aplicación contenga más de una barra de menús).</span><span class="sxs-lookup"><span data-stu-id="c0b29-142">A menu bar control always appears in the control view, but not in content view because it usually does not convey meaningful information to the end user (unless the application contains more than one menu bar).</span></span>

<span data-ttu-id="c0b29-143">Los clientes de automatización de la interfaz de usuario pueden escuchar el evento [**\_ MenuModeStartEventId de UIA**](uiauto-event-ids.md) para asegurarse de que se notifican de forma coherente cuando la interfaz de usuario entra en modo de menú.</span><span class="sxs-lookup"><span data-stu-id="c0b29-143">UI Automation clients can listen for the [**UIA\_MenuModeStartEventId**](uiauto-event-ids.md) event to ensure that they are consistently notified when the UI enters menu mode.</span></span> <span data-ttu-id="c0b29-144">Cuando la aplicación está en modo de menú, es posible que todas las entradas de teclado se capturen para la navegación del menú (por ejemplo, si escribe "" puede invocar el menú **Guardar** en lugar de escribir el carácter en el área cliente de la aplicación).</span><span class="sxs-lookup"><span data-stu-id="c0b29-144">When the application is in menu mode, all of the keyboard input may be captured for menu navigation (for example, typing 's' might invoke the **Save** menu instead of typing the character on the application client area).</span></span> <span data-ttu-id="c0b29-145">El **evento \_ MenuModeStartEventId de UIA** debe preceder al primer evento [**\_ MenuOpenedEventId de UIA**](uiauto-event-ids.md) para garantizar la coherencia lógica.</span><span class="sxs-lookup"><span data-stu-id="c0b29-145">The **UIA\_MenuModeStartEventId** event must precede the first [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event to ensure logical consistency.</span></span> <span data-ttu-id="c0b29-146">El [**evento \_ MenuModeEndEventId de UIA**](uiauto-event-ids.md) sigue el último evento [**\_ MenuClosedEventId de UIA**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="c0b29-146">The [**UIA\_MenuModeEndEventId**](uiauto-event-ids.md) event follows the last [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event.</span></span> <span data-ttu-id="c0b29-147">Hacer clic en un elemento de menú también puede desencadenar inmediatamente el evento **UIA \_ MenuModeStartEventId** , seguido de un evento **\_ MenuOpenedEventId de UIA** .</span><span class="sxs-lookup"><span data-stu-id="c0b29-147">Clicking a menu item may also immediately trigger the **UIA\_MenuModeStartEventId** event, followed by a **UIA\_MenuOpenedEventId** event.</span></span>

<span data-ttu-id="c0b29-148">Un control de barra de menús puede contener otros controles, como controles de edición y cuadros combinados, dentro de su estructura.</span><span class="sxs-lookup"><span data-stu-id="c0b29-148">A menu bar control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="c0b29-149">Estos controles adicionales corresponden a la categoría "otros controles" que se indica anteriormente en las vistas de control y de contenido.</span><span class="sxs-lookup"><span data-stu-id="c0b29-149">These additional controls correspond to the "other controls" listed above in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="c0b29-150">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="c0b29-150">Relevant Properties</span></span>

<span data-ttu-id="c0b29-151">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="c0b29-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **MenuBar** control type.</span></span> <span data-ttu-id="c0b29-152">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="c0b29-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="c0b29-153">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="c0b29-153">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="c0b29-154">Value</span><span class="sxs-lookup"><span data-stu-id="c0b29-154">Value</span></span>       | <span data-ttu-id="c0b29-155">Notas</span><span class="sxs-lookup"><span data-stu-id="c0b29-155">Notes</span></span>                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0b29-156">**UIA \_ AcceleratorKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-156">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="c0b29-157">NULL</span><span class="sxs-lookup"><span data-stu-id="c0b29-157">NULL</span></span>        | <span data-ttu-id="c0b29-158">Las barras de menús no suelen tener teclas de aceleración.</span><span class="sxs-lookup"><span data-stu-id="c0b29-158">Menu bars usually do not have accelerator keys.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="c0b29-159">**UIA \_ AccessKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-159">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="c0b29-160">"Alt"</span><span class="sxs-lookup"><span data-stu-id="c0b29-160">"ALT"</span></span>       | <span data-ttu-id="c0b29-161">Presionar la tecla ALT normalmente debe traer el foco a la barra de menús dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c0b29-161">Pressing the ALT key should usually bring focus to the menu bar within the application.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="c0b29-162">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-162">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="c0b29-163">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="c0b29-163">See notes.</span></span>  | <span data-ttu-id="c0b29-164">El valor que expone esta propiedad debe incluir todos los controles que se contienen dentro de ella.</span><span class="sxs-lookup"><span data-stu-id="c0b29-164">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="c0b29-165">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-165">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="c0b29-166">**MenuBar**</span><span class="sxs-lookup"><span data-stu-id="c0b29-166">**MenuBar**</span></span> |                                                                                                                                                                                                                                          |
| [<span data-ttu-id="c0b29-167">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c0b29-168">false</span><span class="sxs-lookup"><span data-stu-id="c0b29-168">FALSE</span></span>       | <span data-ttu-id="c0b29-169">El control de barra de menús no se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c0b29-169">The menu bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="c0b29-170">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c0b29-171">TRUE</span><span class="sxs-lookup"><span data-stu-id="c0b29-171">TRUE</span></span>        | <span data-ttu-id="c0b29-172">El control de barra de menús siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c0b29-172">The menu bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="c0b29-173">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="c0b29-174">TRUE</span><span class="sxs-lookup"><span data-stu-id="c0b29-174">TRUE</span></span>        | <span data-ttu-id="c0b29-175">Los controles de barra de menús pueden recibir el foco del teclado porque los controles que contienen pueden recibir el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="c0b29-175">Menu bar controls are keyboard-focusable because the controls they contain can take keyboard focus.</span></span>                                                                                                                                      |
| [<span data-ttu-id="c0b29-176">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-176">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="c0b29-177">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="c0b29-177">See notes.</span></span>  | <span data-ttu-id="c0b29-178">El valor de esta propiedad depende de si el control es visible en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0b29-178">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="c0b29-179">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-179">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="c0b29-180">NULL</span><span class="sxs-lookup"><span data-stu-id="c0b29-180">NULL</span></span>        | <span data-ttu-id="c0b29-181">Normalmente, los controles de barra de menús no tienen una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="c0b29-181">Menu bar controls usually do not have a label.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="c0b29-182">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-182">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="c0b29-183">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="c0b29-183">See notes.</span></span>  | <span data-ttu-id="c0b29-184">Cadena localizada que corresponde al tipo de control **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="c0b29-184">Localized string corresponding to the **MenuBar** control type.</span></span> <span data-ttu-id="c0b29-185">El valor predeterminado es "barra de menús" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="c0b29-185">The default value is "menu bar" for en-US or English (United States).</span></span>                                                                                                    |
| [<span data-ttu-id="c0b29-186">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-186">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="c0b29-187">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="c0b29-187">See notes.</span></span>  | <span data-ttu-id="c0b29-188">El control de barra de menús no necesita un nombre a menos que una aplicación tenga más de una barra de menús.</span><span class="sxs-lookup"><span data-stu-id="c0b29-188">The menu bar control does not need a name unless an application has more than one menu bar.</span></span> <span data-ttu-id="c0b29-189">Si hay más de una barra de menús en una aplicación, use esta propiedad para exponer nombres distintivos, como "formato" o "esquematización".</span><span class="sxs-lookup"><span data-stu-id="c0b29-189">If there is more than one menu bar in an application, use this property to expose distinguishing names, such as "Formatting" or "Outlining".</span></span> |
| [<span data-ttu-id="c0b29-190">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-190">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="c0b29-191">Depende</span><span class="sxs-lookup"><span data-stu-id="c0b29-191">Depends</span></span>     | <span data-ttu-id="c0b29-192">Esta propiedad expone si el control de barra de menús es horizontal o vertical.</span><span class="sxs-lookup"><span data-stu-id="c0b29-192">This property exposes whether the menu bar control is horizontal or vertical.</span></span>                                                                                                                                                            |



 

## <a name="required-control-patterns"></a><span data-ttu-id="c0b29-193">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="c0b29-193">Required Control Patterns</span></span>

<span data-ttu-id="c0b29-194">En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que deben admitir los controles de barra de menús.</span><span class="sxs-lookup"><span data-stu-id="c0b29-194">The following table lists the UI Automation control patterns required to be supported by menu bar controls.</span></span> <span data-ttu-id="c0b29-195">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c0b29-195">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="c0b29-196">Patrón de control</span><span class="sxs-lookup"><span data-stu-id="c0b29-196">Control Pattern</span></span>                                                   | <span data-ttu-id="c0b29-197">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="c0b29-197">Support</span></span> | <span data-ttu-id="c0b29-198">Notas</span><span class="sxs-lookup"><span data-stu-id="c0b29-198">Notes</span></span>                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0b29-199">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="c0b29-199">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="c0b29-200">Depende</span><span class="sxs-lookup"><span data-stu-id="c0b29-200">Depends</span></span> | <span data-ttu-id="c0b29-201">Si el control se puede expandir o contraer, debe implementar el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="c0b29-201">If the control can be expanded or collapsed, it must implement the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="c0b29-202">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="c0b29-202">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="c0b29-203">Depende</span><span class="sxs-lookup"><span data-stu-id="c0b29-203">Depends</span></span> | <span data-ttu-id="c0b29-204">Si el control se puede acoplar a diferentes partes de la pantalla, debe implementar el patrón de control [Dock](uiauto-implementingdock.md) .</span><span class="sxs-lookup"><span data-stu-id="c0b29-204">If the control can be docked to different parts of the screen, it must implement the [Dock](uiauto-implementingdock.md) control pattern.</span></span>   |
| [<span data-ttu-id="c0b29-205">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="c0b29-205">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="c0b29-206">Depende</span><span class="sxs-lookup"><span data-stu-id="c0b29-206">Depends</span></span> | <span data-ttu-id="c0b29-207">Si el control puede cambiar de tamaño, girarse o moverse, debe implementar el patrón de control [Transform](uiauto-implementingtransform.md) .</span><span class="sxs-lookup"><span data-stu-id="c0b29-207">If the control can be resized, rotated, or moved, it must implement the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>      |



 

## <a name="required-events"></a><span data-ttu-id="c0b29-208">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="c0b29-208">Required Events</span></span>

<span data-ttu-id="c0b29-209">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de barra de menús son necesarios para admitir.</span><span class="sxs-lookup"><span data-stu-id="c0b29-209">The following table lists the UI Automation events that menu bar controls are required to support.</span></span> <span data-ttu-id="c0b29-210">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c0b29-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="c0b29-211">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="c0b29-211">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="c0b29-212">Notas</span><span class="sxs-lookup"><span data-stu-id="c0b29-212">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0b29-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="c0b29-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c0b29-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="c0b29-215">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c0b29-215">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="c0b29-216">Si el control admite el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="c0b29-216">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="c0b29-217">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c0b29-217">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="c0b29-218">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="c0b29-218">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="c0b29-219">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c0b29-219">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="c0b29-220">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="c0b29-220">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="c0b29-221">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="c0b29-221">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="c0b29-222">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0b29-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c0b29-223">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c0b29-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c0b29-224">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="c0b29-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="c0b29-225">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="c0b29-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




