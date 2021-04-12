---
title: Button (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Button.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Button
- UI Automation, Button (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Button
- Automatización de la interfaz de usuario, propiedades para el tipo de control Button
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Button
- Automatización de la interfaz de usuario, eventos para el tipo de control Button
- estructuras de árbol, Button (tipo de control)
- Properties, Button (tipo de control)
- patrones de control, Button (tipo de control)
- Events, Button (tipo de control)
- compatibilidad con el tipo de control Button
- Button (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Button
- tipos de control, patrones de control para el tipo de control Button
- tipos de control, compatibilidad con Button
- tipos de control, botón
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def18e7094e297303a70fc0980bfdd0cb4413c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269456"
---
# <a name="button-control-type"></a><span data-ttu-id="40fc9-119">Button (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="40fc9-119">Button Control Type</span></span>

<span data-ttu-id="40fc9-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Button** .</span><span class="sxs-lookup"><span data-stu-id="40fc9-120">This topic provides information about Microsoft UI Automation support for the **Button** control type.</span></span>

<span data-ttu-id="40fc9-121">Un botón es un objeto con el que un usuario interactúa para realizar una acción, como por ejemplo los botones Aceptar y Cancelar de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="40fc9-121">A button is an object that a user interacts with to perform an action such as the OK and Cancel buttons on a dialog box.</span></span> <span data-ttu-id="40fc9-122">El control de botón es un control simple de exponer porque se asigna a un único comando que el usuario quiere realizar.</span><span class="sxs-lookup"><span data-stu-id="40fc9-122">The button control is a simple control to expose because it maps to a single command that the user wishes to complete.</span></span>

<span data-ttu-id="40fc9-123">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Button** .</span><span class="sxs-lookup"><span data-stu-id="40fc9-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Button** control type.</span></span> <span data-ttu-id="40fc9-124">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de botón donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control</span><span class="sxs-lookup"><span data-stu-id="40fc9-124">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="40fc9-125">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="40fc9-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="40fc9-126">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="40fc9-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="40fc9-127">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="40fc9-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="40fc9-128">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="40fc9-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="40fc9-129">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="40fc9-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="40fc9-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40fc9-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="40fc9-131">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="40fc9-131">Typical Tree Structure</span></span>

<span data-ttu-id="40fc9-132">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de botón y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="40fc9-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="40fc9-133">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="40fc9-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40fc9-134">Vista de control</span><span class="sxs-lookup"><span data-stu-id="40fc9-134">Control View</span></span></th>
<th><span data-ttu-id="40fc9-135">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="40fc9-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="40fc9-136">Botón</span><span class="sxs-lookup"><span data-stu-id="40fc9-136">Button</span></span>
<ul>
<li><span data-ttu-id="40fc9-137">Imagen (0 o más)</span><span class="sxs-lookup"><span data-stu-id="40fc9-137">Image (0 or more)</span></span></li>
<li><span data-ttu-id="40fc9-138">Text (0 o más)</span><span class="sxs-lookup"><span data-stu-id="40fc9-138">Text (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="40fc9-139">Botón</span><span class="sxs-lookup"><span data-stu-id="40fc9-139">Button</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="40fc9-140">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="40fc9-140">Relevant Properties</span></span>

<span data-ttu-id="40fc9-141">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles que implementan el tipo de control **Button** (como los controles de botón).</span><span class="sxs-lookup"><span data-stu-id="40fc9-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **Button** control type (such as button controls).</span></span> <span data-ttu-id="40fc9-142">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="40fc9-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="40fc9-143">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="40fc9-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="40fc9-144">Value</span><span class="sxs-lookup"><span data-stu-id="40fc9-144">Value</span></span>      | <span data-ttu-id="40fc9-145">Notas</span><span class="sxs-lookup"><span data-stu-id="40fc9-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40fc9-146">**UIA \_ AcceleratorKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-146">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="40fc9-147">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-147">See notes.</span></span> | <span data-ttu-id="40fc9-148">Un control de botón normalmente admite una tecla de aceleración para permitir que el usuario final realice rápidamente la acción representada por el botón del teclado.</span><span class="sxs-lookup"><span data-stu-id="40fc9-148">A button control typically supports an accelerator key to enable the end user to quickly perform the action represented by the button from the keyboard.</span></span>                                             |
| [<span data-ttu-id="40fc9-149">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="40fc9-150">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-150">See notes.</span></span> | <span data-ttu-id="40fc9-151">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="40fc9-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="40fc9-152">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="40fc9-153">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-153">See notes.</span></span> | <span data-ttu-id="40fc9-154">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="40fc9-154">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="40fc9-155">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="40fc9-156">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-156">See notes.</span></span> | <span data-ttu-id="40fc9-157">Se admite si hay un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="40fc9-157">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="40fc9-158">Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.</span><span class="sxs-lookup"><span data-stu-id="40fc9-158">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="40fc9-159">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-159">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="40fc9-160">**Botón**</span><span class="sxs-lookup"><span data-stu-id="40fc9-160">**Button**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="40fc9-161">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-161">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="40fc9-162">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-162">See notes.</span></span> | <span data-ttu-id="40fc9-163">El texto de ayuda debe indicar cuál será el resultado final de la activación del botón.</span><span class="sxs-lookup"><span data-stu-id="40fc9-163">The help text should indicate what the end result of activating the button will be.</span></span> <span data-ttu-id="40fc9-164">Suele ser el mismo tipo de información que se presenta a través de una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-164">This is typically the same type of information presented through a tooltip.</span></span>                                      |
| [<span data-ttu-id="40fc9-165">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="40fc9-166">TRUE</span><span class="sxs-lookup"><span data-stu-id="40fc9-166">TRUE</span></span>       | <span data-ttu-id="40fc9-167">El control de botón siempre debe ser contenido.</span><span class="sxs-lookup"><span data-stu-id="40fc9-167">The button control must always be content.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="40fc9-168">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="40fc9-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="40fc9-169">TRUE</span></span>       | <span data-ttu-id="40fc9-170">El control de botón siempre debe ser un control.</span><span class="sxs-lookup"><span data-stu-id="40fc9-170">The button control must always be a control.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="40fc9-171">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="40fc9-172">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-172">See notes.</span></span> | <span data-ttu-id="40fc9-173">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="40fc9-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="40fc9-174">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="40fc9-175">Null</span><span class="sxs-lookup"><span data-stu-id="40fc9-175">Null</span></span>       | <span data-ttu-id="40fc9-176">Los controles de botón se etiquetan automáticamente con su contenido.</span><span class="sxs-lookup"><span data-stu-id="40fc9-176">Button controls are self-labeled by their contents.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="40fc9-177">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="40fc9-178">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-178">See notes.</span></span> | <span data-ttu-id="40fc9-179">Cadena localizada que corresponde al tipo de control **Button** .</span><span class="sxs-lookup"><span data-stu-id="40fc9-179">Localized string corresponding to the **Button** control type.</span></span> <span data-ttu-id="40fc9-180">El valor predeterminado es "Button" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="40fc9-180">The default value is "button" for en-US or English (United States).</span></span>                                                                   |
| [<span data-ttu-id="40fc9-181">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="40fc9-182">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-182">See notes.</span></span> | <span data-ttu-id="40fc9-183">El nombre del control de botón es el texto que se utiliza para etiquetarlo.</span><span class="sxs-lookup"><span data-stu-id="40fc9-183">The name of the button control is the text used to label it.</span></span> <span data-ttu-id="40fc9-184">Siempre que se utiliza una imagen para etiquetar un botón, se debe proporcionar texto alternativo para la propiedad **nombre** del botón.</span><span class="sxs-lookup"><span data-stu-id="40fc9-184">Whenever an image is used to label a button, alternate text must be supplied for the button's **Name** property.</span></span>                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="40fc9-185">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="40fc9-185">Required Control Patterns</span></span>

<span data-ttu-id="40fc9-186">En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de botón.</span><span class="sxs-lookup"><span data-stu-id="40fc9-186">The following table lists the UI Automation control patterns required to be supported by all button controls.</span></span> <span data-ttu-id="40fc9-187">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="40fc9-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="40fc9-188">Patrón de control/Propiedad de patrón</span><span class="sxs-lookup"><span data-stu-id="40fc9-188">Control Pattern/Pattern Property</span></span>                                  | <span data-ttu-id="40fc9-189">Soporte técnico/valor</span><span class="sxs-lookup"><span data-stu-id="40fc9-189">Support/Value</span></span> | <span data-ttu-id="40fc9-190">Notas</span><span class="sxs-lookup"><span data-stu-id="40fc9-190">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40fc9-191">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="40fc9-191">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="40fc9-192">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-192">See notes.</span></span>    | <span data-ttu-id="40fc9-193">Cuando un botón se hospeda como elemento secundario de un botón de expansión, el botón secundario puede admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) en lugar del patrón de control [Invoke](uiauto-implementinginvoke.md) o [Toggle](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="40fc9-193">When a button is hosted as a child of a split button, the child button can support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern instead of the [Invoke](uiauto-implementinginvoke.md) or [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="40fc9-194">El patrón de control ExpandCollapse se puede usar para abrir o cerrar un menú u otra subestructura asociada con el elemento de botón.</span><span class="sxs-lookup"><span data-stu-id="40fc9-194">The ExpandCollapse control pattern can be used for opening or closing a menu or other sub-structure associated with the button element.</span></span> |
| [<span data-ttu-id="40fc9-195">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="40fc9-195">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="40fc9-196">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-196">See notes.</span></span>    | <span data-ttu-id="40fc9-197">Todos los botones deben admitir el patrón de control [Invoke](uiauto-implementinginvoke.md) o el patrón de control [Toggle](uiauto-implementingtoggle.md) , pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="40fc9-197">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="40fc9-198">Se debe admitir el patrón de control Invoke cuando el botón ejecuta un comando en la solicitud del usuario.</span><span class="sxs-lookup"><span data-stu-id="40fc9-198">The Invoke control pattern must be supported when the button performs a command at the request of the user.</span></span> <span data-ttu-id="40fc9-199">Este comando se asigna a una única operación, como cortar, copiar, pegar o eliminar.</span><span class="sxs-lookup"><span data-stu-id="40fc9-199">This command maps to a single operation such as Cut, Copy, Paste, or Delete.</span></span>                                                              |
| [<span data-ttu-id="40fc9-200">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="40fc9-200">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="40fc9-201">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-201">See notes.</span></span>    | <span data-ttu-id="40fc9-202">Todos los botones deben admitir el patrón de control [Invoke](uiauto-implementinginvoke.md) o el patrón de control [Toggle](uiauto-implementingtoggle.md) , pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="40fc9-202">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="40fc9-203">Se debe admitir el patrón de control Toggle si el botón puede recorrer una serie de hasta tres Estados.</span><span class="sxs-lookup"><span data-stu-id="40fc9-203">The Toggle control pattern must be supported if the button can cycle through a series of up to three states.</span></span> <span data-ttu-id="40fc9-204">Normalmente, se considera como un conmutador de encendido y apagado para características específicas.</span><span class="sxs-lookup"><span data-stu-id="40fc9-204">Typically this is seen as an on/off switch for specific features.</span></span>                                                                        |



 

## <a name="required-events"></a><span data-ttu-id="40fc9-205">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="40fc9-205">Required Events</span></span>

<span data-ttu-id="40fc9-206">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de botón deben admitir.</span><span class="sxs-lookup"><span data-stu-id="40fc9-206">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="40fc9-207">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="40fc9-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="40fc9-208">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="40fc9-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="40fc9-209">Notas</span><span class="sxs-lookup"><span data-stu-id="40fc9-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40fc9-210">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="40fc9-211">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="40fc9-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="40fc9-212">**\_InvokedEventId de invocación de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="40fc9-212">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="40fc9-213">Si el control admite el patrón de control [Invoke](uiauto-implementinginvoke.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="40fc9-213">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="40fc9-214">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="40fc9-214">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="40fc9-215">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="40fc9-215">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="40fc9-216">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="40fc9-216">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="40fc9-217">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="40fc9-217">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="40fc9-218">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de NamePropertyId.</span><span class="sxs-lookup"><span data-stu-id="40fc9-218">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="40fc9-219">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="40fc9-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="40fc9-220">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="40fc9-220">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    | <span data-ttu-id="40fc9-221">Si el control admite el patrón de control [Toggle](uiauto-implementingtoggle.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="40fc9-221">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="40fc9-222">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40fc9-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="40fc9-223">**Vista**</span><span class="sxs-lookup"><span data-stu-id="40fc9-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="40fc9-224">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="40fc9-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="40fc9-225">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="40fc9-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




