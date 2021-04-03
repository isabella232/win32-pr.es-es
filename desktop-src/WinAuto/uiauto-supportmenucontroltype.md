---
title: Menu (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control menu.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control menu
- UI Automation, MENU (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control menu
- Automatización de la interfaz de usuario, propiedades del tipo de control menu
- Automatización de la interfaz de usuario, patrones de control para el tipo de control menu
- Automatización de la interfaz de usuario, eventos para el tipo de control menu
- estructuras de árbol, tipo de control menu
- Properties, MENU (tipo de control)
- patrones de control, tipo de control menu
- Events, MENU (tipo de control)
- compatibilidad con el tipo de control menu
- Menu (tipo de control)
- tipos de control, estructura de árbol para el tipo de control menu
- tipos de control, patrones de control para el tipo de control menu
- tipos de control, compatibilidad con menú
- tipos de control, menú
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075614"
---
# <a name="menu-control-type"></a><span data-ttu-id="55956-119">Menu (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="55956-119">Menu Control Type</span></span>

<span data-ttu-id="55956-120">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Menu** .</span><span class="sxs-lookup"><span data-stu-id="55956-120">This topic provides information about Microsoft UI Automation support for the **Menu** control type.</span></span>

<span data-ttu-id="55956-121">Un control de menú permite organizar jerárquicamente los elementos asociados a comandos y controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="55956-121">A menu control allows hierarchal organization of elements associated with commands and event handlers.</span></span> <span data-ttu-id="55956-122">En una aplicación típica de Microsoft Windows, una barra de menús contiene varios botones de menú (como **archivo**, **Editar** y **ventana**) y cada botón de menú muestra un menú.</span><span class="sxs-lookup"><span data-stu-id="55956-122">In a typical Microsoft Windows application, a menu bar contains several menu buttons (such as **File**, **Edit**, and **Window**), and each menu button displays a menu.</span></span> <span data-ttu-id="55956-123">Un menú contiene una colección de elementos de menú (como **Nuevo**, **Abrir** y **Cerrar**), que se puede expandir para mostrar elementos de menú adicionales o realizar una acción específica cuando se haga clic en ellos.</span><span class="sxs-lookup"><span data-stu-id="55956-123">A menu contains a collection of menu items (such as **New**, **Open**, and **Close**), which can be expanded to display additional menu items or to perform a specific action when clicked.</span></span>

<span data-ttu-id="55956-124">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Menu** .</span><span class="sxs-lookup"><span data-stu-id="55956-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Menu** control type.</span></span> <span data-ttu-id="55956-125">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de menú donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control.</span><span class="sxs-lookup"><span data-stu-id="55956-125">The UI Automation requirements apply to all menu controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="55956-126">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="55956-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="55956-127">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="55956-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="55956-128">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="55956-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="55956-129">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="55956-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="55956-130">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="55956-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="55956-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55956-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="55956-132">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="55956-132">Typical Tree Structure</span></span>

<span data-ttu-id="55956-133">En la tabla siguiente se muestra una vista de contenido y control típica del árbol de automatización de la interfaz de usuario que pertenece a los controles de menú y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="55956-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu controls and describes what can be contained in each view.</span></span> <span data-ttu-id="55956-134">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55956-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55956-135">Vista de control</span><span class="sxs-lookup"><span data-stu-id="55956-135">Control View</span></span></th>
<th><span data-ttu-id="55956-136">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="55956-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="55956-137">Menú</span><span class="sxs-lookup"><span data-stu-id="55956-137">Menu</span></span>
<ul>
<li><span data-ttu-id="55956-138">MenuItem (1 o varios)</span><span class="sxs-lookup"><span data-stu-id="55956-138">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="55956-139">Otros controles (0 o varios)</span><span class="sxs-lookup"><span data-stu-id="55956-139">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="55956-140">Menú</span><span class="sxs-lookup"><span data-stu-id="55956-140">Menu</span></span>
<ul>
<li><span data-ttu-id="55956-141">MenuItem (1 o varios)</span><span class="sxs-lookup"><span data-stu-id="55956-141">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="55956-142">Otros controles (0 o varios)</span><span class="sxs-lookup"><span data-stu-id="55956-142">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="55956-143">Los controles de menú siempre aparecen en la vista de control y la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="55956-143">Menu controls always appear in the control view and the content view of the UI Automation tree.</span></span> <span data-ttu-id="55956-144">Los controles de menú deben aparecer bajo el control al que hace referencia su información.</span><span class="sxs-lookup"><span data-stu-id="55956-144">Menu controls should appear under the control that their information is referring to.</span></span> <span data-ttu-id="55956-145">Los clientes de automatización de la interfaz de usuario pueden escuchar a [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) para asegurarse de que obtienen de forma coherente la información que transmiten los controles de menú.</span><span class="sxs-lookup"><span data-stu-id="55956-145">UI Automation clients can listen for [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) to ensure that they consistently obtain information conveyed by menu controls.</span></span> <span data-ttu-id="55956-146">Los controles de menú contextual son un caso especial.</span><span class="sxs-lookup"><span data-stu-id="55956-146">Context menu controls are a special case.</span></span> <span data-ttu-id="55956-147">Pueden aparecer como elementos secundarios del escritorio o de una ventana de la aplicación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="55956-147">They may appear as children of the desktop or of a top level application window.</span></span>

<span data-ttu-id="55956-148">Un control de menú puede contener otros controles, como controles de edición y cuadros combinados, dentro de su estructura.</span><span class="sxs-lookup"><span data-stu-id="55956-148">A menu control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="55956-149">Estos controles adicionales corresponden a los "otros controles" que se muestran en la tabla anterior en las vistas de control y de contenido.</span><span class="sxs-lookup"><span data-stu-id="55956-149">These additional controls correspond to the "other controls" listed in the previous table in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="55956-150">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="55956-150">Relevant Properties</span></span>

<span data-ttu-id="55956-151">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **Menu** .</span><span class="sxs-lookup"><span data-stu-id="55956-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **Menu** control type.</span></span> <span data-ttu-id="55956-152">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="55956-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="55956-153">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="55956-153">UI Automation Property</span></span>                                                                                      | <span data-ttu-id="55956-154">Value</span><span class="sxs-lookup"><span data-stu-id="55956-154">Value</span></span>      | <span data-ttu-id="55956-155">Notas</span><span class="sxs-lookup"><span data-stu-id="55956-155">Notes</span></span>                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55956-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="55956-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)           | <span data-ttu-id="55956-157">**Menú**</span><span class="sxs-lookup"><span data-stu-id="55956-157">**Menu**</span></span>   |                                                                                                                                                                         |
| [<span data-ttu-id="55956-158">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55956-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="55956-159">TRUE</span><span class="sxs-lookup"><span data-stu-id="55956-159">TRUE</span></span>       | <span data-ttu-id="55956-160">El control de menú siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="55956-160">The menu control is always included in the content view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="55956-161">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55956-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="55956-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="55956-162">TRUE</span></span>       | <span data-ttu-id="55956-163">El control de menú siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="55956-163">The menu control is always included in the control view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="55956-164">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55956-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="55956-165">NULL</span><span class="sxs-lookup"><span data-stu-id="55956-165">NULL</span></span>       | <span data-ttu-id="55956-166">No se espera ninguna etiqueta con un control de menú típico.</span><span class="sxs-lookup"><span data-stu-id="55956-166">No label is anticipated with a typical menu control.</span></span>                                                                                                                    |
| [<span data-ttu-id="55956-167">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="55956-167">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="55956-168">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="55956-168">See notes.</span></span> | <span data-ttu-id="55956-169">El control de menú no requiere que se establezca una propiedad **Name** o puede tener el mismo nombre que el control asociado, como un elemento de menú que abrió el submenú.</span><span class="sxs-lookup"><span data-stu-id="55956-169">The menu control does not require a **Name** property to be set, or it could have the same name as the associated control, such as a menu item that opened the submenu.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="55956-170">Patrones de control necesarios</span><span class="sxs-lookup"><span data-stu-id="55956-170">Required Control Patterns</span></span>

<span data-ttu-id="55956-171">No hay ningún patrón de control necesario para el tipo de control Menu.</span><span class="sxs-lookup"><span data-stu-id="55956-171">There are no required control patterns for the Menu control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="55956-172">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="55956-172">Required Events</span></span>

<span data-ttu-id="55956-173">Los controles de menú deben generar el evento de [**\_ MenuOpenedEventId de UIA**](uiauto-event-ids.md) cuando aparecen en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="55956-173">Menu controls must raise the [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event when they appear on the screen.</span></span> <span data-ttu-id="55956-174">El evento de **\_ MenuOpenedEventId de UIA** incluirá el texto del control.</span><span class="sxs-lookup"><span data-stu-id="55956-174">The **UIA\_MenuOpenedEventId** event will include the text of the control.</span></span> <span data-ttu-id="55956-175">El [**evento \_ MenuClosedEventId de UIA**](uiauto-event-ids.md) se debe generar cuando un menú desaparece de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="55956-175">The [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event must be raised when a menu disappears from the screen.</span></span>

<span data-ttu-id="55956-176">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de menú deben admitir.</span><span class="sxs-lookup"><span data-stu-id="55956-176">The following table lists the UI Automation events that menu controls are required to support.</span></span> <span data-ttu-id="55956-177">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55956-177">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="55956-178">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="55956-178">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="55956-179">Notas</span><span class="sxs-lookup"><span data-stu-id="55956-179">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55956-180">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="55956-180">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="55956-181">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="55956-181">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="55956-182">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="55956-182">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="55956-183">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="55956-183">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="55956-184">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="55956-184">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="55956-185">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="55956-185">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="55956-186">**UIA \_ MenuClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="55956-186">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="55956-187">**UIA \_ MenuOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="55956-187">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="55956-188">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="55956-188">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="55956-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55956-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="55956-190">**Vista**</span><span class="sxs-lookup"><span data-stu-id="55956-190">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="55956-191">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="55956-191">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="55956-192">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="55956-192">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




