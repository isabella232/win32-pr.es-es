---
title: AppBar (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control AppBar.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control AppBar
- Automatización de la interfaz de usuario, tipo de control AppBar
- Automatización de la interfaz de usuario, patrones de control para el tipo de control AppBar
- patrones de control, tipo de control AppBar
- compatibilidad con el tipo de control AppBar
- AppBar (tipo de control)
- tipos de control, AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151aecc0f5f97878e10b59b091c4c59ec98cb26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488091"
---
# <a name="appbar-control-type"></a><span data-ttu-id="37710-110">AppBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="37710-110">AppBar Control Type</span></span>

<span data-ttu-id="37710-111">En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **AppBar** .</span><span class="sxs-lookup"><span data-stu-id="37710-111">This topic provides information about Microsoft UI Automation support for the **AppBar** control type.</span></span>

<span data-ttu-id="37710-112">Una barra de aplicación es un elemento de la interfaz de usuario que presenta navegación, comandos y herramientas al usuario.</span><span class="sxs-lookup"><span data-stu-id="37710-112">An app bar is a UI element that presents navigation, commands, and tools to the user.</span></span> <span data-ttu-id="37710-113">En el caso de las aplicaciones de la tienda Windows, las barras de la aplicación para aplicaciones se pueden mostrar presionando tecla Windows + Z.</span><span class="sxs-lookup"><span data-stu-id="37710-113">For Windows Store apps, app bars for apps can be displayed by pressing Windows Key + Z.</span></span>

<span data-ttu-id="37710-114">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario necesaria, las propiedades, los patrones de control y los eventos para el tipo de control **AppBar** .</span><span class="sxs-lookup"><span data-stu-id="37710-114">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **AppBar** control type.</span></span>

<span data-ttu-id="37710-115">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="37710-115">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="37710-116">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="37710-116">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="37710-117">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="37710-117">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="37710-118">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="37710-118">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="37710-119">Eventos relevantes</span><span class="sxs-lookup"><span data-stu-id="37710-119">Relevant Events</span></span>](#relevant-events)
-   [<span data-ttu-id="37710-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37710-120">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="37710-121">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="37710-121">Typical Tree Structure</span></span>

<span data-ttu-id="37710-122">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de **AppBar** y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="37710-122">The following table depicts a typical control and content view of the UI Automation tree that pertains to **AppBar** controls and describes what can be contained in each view.</span></span> <span data-ttu-id="37710-123">El **botón** es el elemento más común dentro de un control **AppBar** , pero también se pueden realizar otros controles que invoquen acciones para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="37710-123">**Button** is the most common element within an **AppBar** but other controls that invoke actions for an app are also possible.</span></span> <span data-ttu-id="37710-124">Un **AppBar** también puede tener 0 o más separadores (tipo de control de **separador** ), que aparecen en la vista de control tal y como se colocan entre los demás controles.</span><span class="sxs-lookup"><span data-stu-id="37710-124">An **AppBar** can also have 0 or more separators (**Separator** control type), which appear in the control view as placed between the other controls.</span></span> <span data-ttu-id="37710-125">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="37710-125">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37710-126">Vista de control</span><span class="sxs-lookup"><span data-stu-id="37710-126">Control View</span></span></th>
<th><span data-ttu-id="37710-127">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="37710-127">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="37710-128">AppBar</span><span class="sxs-lookup"><span data-stu-id="37710-128">AppBar</span></span>
<ul>
<li><span data-ttu-id="37710-129">Botón (0 o muchos)</span><span class="sxs-lookup"><span data-stu-id="37710-129">Button (0 or many)</span></span></li>
<li><span data-ttu-id="37710-130">Otros controles (0 o varios)</span><span class="sxs-lookup"><span data-stu-id="37710-130">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="37710-131">No aplicable</span><span class="sxs-lookup"><span data-stu-id="37710-131">Not applicable</span></span>
<ul>
<li><span data-ttu-id="37710-132">Botón (0 o muchos)</span><span class="sxs-lookup"><span data-stu-id="37710-132">Button (0 or many)</span></span></li>
<li><span data-ttu-id="37710-133">Otros controles (0 o varios)</span><span class="sxs-lookup"><span data-stu-id="37710-133">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="37710-134">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="37710-134">Relevant Properties</span></span>

<span data-ttu-id="37710-135">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles que implementan el tipo de control **AppBar** .</span><span class="sxs-lookup"><span data-stu-id="37710-135">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **AppBar** control type.</span></span> <span data-ttu-id="37710-136">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="37710-136">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="37710-137">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="37710-137">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="37710-138">Value</span><span class="sxs-lookup"><span data-stu-id="37710-138">Value</span></span>      | <span data-ttu-id="37710-139">Notas</span><span class="sxs-lookup"><span data-stu-id="37710-139">Notes</span></span>                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37710-140">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="37710-140">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="37710-141">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="37710-141">See notes.</span></span> | <span data-ttu-id="37710-142">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="37710-142">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                |
| [<span data-ttu-id="37710-143">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="37710-143">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="37710-144">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="37710-144">See notes.</span></span> | <span data-ttu-id="37710-145">El valor que expone esta propiedad debe incluir todos los controles que se contienen dentro de ella.</span><span class="sxs-lookup"><span data-stu-id="37710-145">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                    |
| [<span data-ttu-id="37710-146">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="37710-146">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="37710-147">**AppBar**</span><span class="sxs-lookup"><span data-stu-id="37710-147">**AppBar**</span></span> |                                                                                                                                                                                                                             |
| [<span data-ttu-id="37710-148">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="37710-148">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="37710-149">false</span><span class="sxs-lookup"><span data-stu-id="37710-149">FALSE</span></span>      | <span data-ttu-id="37710-150">Un control de barra de la aplicación no se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="37710-150">An app bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="37710-151">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="37710-151">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="37710-152">TRUE</span><span class="sxs-lookup"><span data-stu-id="37710-152">TRUE</span></span>       | <span data-ttu-id="37710-153">Un control de barra de la aplicación siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="37710-153">An app bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                        |
| [<span data-ttu-id="37710-154">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="37710-154">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="37710-155">Vea las notas</span><span class="sxs-lookup"><span data-stu-id="37710-155">See notes</span></span>  | <span data-ttu-id="37710-156">Si el control puede recibir el foco del teclado, debe admitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="37710-156">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="37710-157">Normalmente, los controles de la barra de la aplicación pueden tomar el foco del teclado.</span><span class="sxs-lookup"><span data-stu-id="37710-157">Controls within the app bar typically can take keyboard focus.</span></span>                                                                                    |
| [<span data-ttu-id="37710-158">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="37710-158">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="37710-159">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="37710-159">See notes.</span></span> | <span data-ttu-id="37710-160">El valor de esta propiedad depende de si el control es visible en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="37710-160">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                        |
| [<span data-ttu-id="37710-161">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="37710-161">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="37710-162">Null</span><span class="sxs-lookup"><span data-stu-id="37710-162">Null</span></span>       | <span data-ttu-id="37710-163">Normalmente, los controles de barra de la aplicación no tienen una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="37710-163">App bar controls usually do not have a label.</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="37710-164">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="37710-164">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="37710-165">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="37710-165">See notes.</span></span> | <span data-ttu-id="37710-166">Cadena localizada que corresponde al tipo de control **AppBar** .</span><span class="sxs-lookup"><span data-stu-id="37710-166">Localized string corresponding to the **AppBar** control type.</span></span> <span data-ttu-id="37710-167">El valor predeterminado es "App bar" para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="37710-167">The default value is "app bar" for en-US or English (United States).</span></span>                                                                                         |
| [<span data-ttu-id="37710-168">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="37710-168">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="37710-169">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="37710-169">See notes.</span></span> | <span data-ttu-id="37710-170">El control de barra de la aplicación no necesita un nombre a menos que una aplicación tenga más de una barra de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="37710-170">The app bar control does not need a name unless an application has more than one app bar.</span></span> <span data-ttu-id="37710-171">Si hay más de una barra de aplicación en una aplicación, use esta propiedad para exponer los nombres distintivos, como "Top" o "Bottom".</span><span class="sxs-lookup"><span data-stu-id="37710-171">If there is more than one app bar in an application, use this property to expose distinguishing names, such as "Top" or "Bottom."</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="37710-172">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="37710-172">Required Events</span></span>

<span data-ttu-id="37710-173">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de barra de la aplicación deben admitir.</span><span class="sxs-lookup"><span data-stu-id="37710-173">The following table lists the UI Automation events that app bar controls are required to support.</span></span> <span data-ttu-id="37710-174">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="37710-174">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="37710-175">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="37710-175">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="37710-176">Notas</span><span class="sxs-lookup"><span data-stu-id="37710-176">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37710-177">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="37710-177">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="37710-178">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="37710-178">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="37710-179">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="37710-179">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="37710-180">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="37710-180">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="37710-181">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="37710-181">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="37710-182">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="37710-182">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="37710-183">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="37710-183">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a><span data-ttu-id="37710-184">Eventos relevantes</span><span class="sxs-lookup"><span data-stu-id="37710-184">Relevant Events</span></span>

<span data-ttu-id="37710-185">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que son especialmente relevantes para los controles que implementan el tipo de control **AppBar** pero no son estrictamente necesarios.</span><span class="sxs-lookup"><span data-stu-id="37710-185">The following table lists the UI Automation events that are especially relevant to the controls that implement the **AppBar** control type but not strictly required.</span></span>



| <span data-ttu-id="37710-186">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="37710-186">UI Automation Event</span></span>                                                                                 | <span data-ttu-id="37710-187">Notas</span><span class="sxs-lookup"><span data-stu-id="37710-187">Notes</span></span>                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="37710-188">**UIA \_ MenuClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="37710-188">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="37710-189">Las implementaciones de la plataforma pueden activar este evento cuando se cierra el control de la barra de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="37710-189">Platform implementations might fire this event when the app bar control is closed.</span></span> |
| [<span data-ttu-id="37710-190">**UIA \_ MenuOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="37710-190">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="37710-191">Las implementaciones de la plataforma pueden activar este evento cuando se abre el control de barra de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="37710-191">Platform implementations might fire this event when the app bar control is opened.</span></span> |
| [<span data-ttu-id="37710-192">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="37710-192">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | <span data-ttu-id="37710-193">Controlador de eventos de cambio de propiedad.</span><span class="sxs-lookup"><span data-stu-id="37710-193">Property-changed event handler.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="37710-194">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37710-194">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="37710-195">**Vista**</span><span class="sxs-lookup"><span data-stu-id="37710-195">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="37710-196">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="37710-196">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="37710-197">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="37710-197">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> <dt>

<span data-ttu-id="37710-198">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="37710-198">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="37710-199">**Control XAML de AppBar**</span><span class="sxs-lookup"><span data-stu-id="37710-199">**AppBar XAML control**</span></span>](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

<span data-ttu-id="37710-200">[**Objeto WinJS. UI. AppBar**](/previous-versions/windows/apps/br229670(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="37710-200">[**WinJS.UI.AppBar object**](/previous-versions/windows/apps/br229670(v=win.10))</span></span>
</dt> </dl>

 

 