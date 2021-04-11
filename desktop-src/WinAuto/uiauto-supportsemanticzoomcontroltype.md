---
title: SemanticZoom (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de UI Automation para el tipo de control SemanticZoom.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control SemanticZoom
- Automatización de la interfaz de usuario, tipo de control SemanticZoom
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control SemanticZoom
- Automatización de la interfaz de usuario, propiedades para el tipo de control SemanticZoom
- Automatización de la interfaz de usuario, patrones de control para el tipo de control SemanticZoom
- Automatización de la interfaz de usuario, eventos para el tipo de control SemanticZoom
- estructuras de árbol, tipo de control SemanticZoom
- propiedades, tipo de control SemanticZoom
- patrones de control, tipo de control SemanticZoom
- Events, tipo de control SemanticZoom
- compatibilidad con el tipo de control SemanticZoom
- SemanticZoom (tipo de control)
- tipos de control, estructura de árbol para el tipo de control SemanticZoom
- tipos de control, patrones de control para el tipo de control SemanticZoom
- tipos de control, compatibilidad con SemanticZoom
- tipos de control, SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4712aa4f10489081b1b5d0f69fed849080bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149294"
---
# <a name="semanticzoom-control-type"></a><span data-ttu-id="654ed-119">SemanticZoom (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="654ed-119">SemanticZoom Control Type</span></span>

<span data-ttu-id="654ed-120">En este tema se proporciona información sobre la compatibilidad de UI Automation para el tipo de control **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="654ed-120">This topic provides information about UI Automation support for the **SemanticZoom** control type.</span></span>

<span data-ttu-id="654ed-121">El zoom semántico es una técnica introducida en Windows 8 para presentar y navegar por grandes conjuntos de datos o contenido relacionados en una sola vista, como un álbum de fotos, una lista de aplicaciones o una libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="654ed-121">Semantic Zoom is a technique introduced in Windows 8 for presenting and navigating large sets of related data or content within a single view, such as a photo album, app list, or address book.</span></span> <span data-ttu-id="654ed-122">El zoom semántico usa dos modos distintos de clasificación, o *niveles de zoom*, para organizar y presentar el contenido.</span><span class="sxs-lookup"><span data-stu-id="654ed-122">Semantic Zoom uses two distinct modes of classification, or *zoom levels*, for organizing and presenting the content.</span></span> <span data-ttu-id="654ed-123">El modo de bajo nivel (o *de zoom en*) muestra los elementos en una estructura plana "todo arriba"; y el modo de alto nivel (o *alejado*) muestra los elementos en grupos, lo que permite al usuario navegar rápidamente por el contenido y desplazarse por él.</span><span class="sxs-lookup"><span data-stu-id="654ed-123">The low-level (or *zoomed in*) mode displays items in a flat, "all-up" structure; and the high-level (or *zoomed out*) mode displays items in groups, enabling the user to quickly navigate and browse through the content.</span></span> <span data-ttu-id="654ed-124">Por ejemplo, la ampliación de una lista de ciudades podría cambiar a una lista de Estados que contengan esas ciudades.</span><span class="sxs-lookup"><span data-stu-id="654ed-124">For example, zooming a list of cities might change to a list of states containing those cities.</span></span> <span data-ttu-id="654ed-125">La ampliación de una lista de programas podría cambiar a una lista de grupos de programas lógicos.</span><span class="sxs-lookup"><span data-stu-id="654ed-125">Zooming a list of programs might change to a list of logical program groups.</span></span>

<span data-ttu-id="654ed-126">Para obtener más información sobre el zoom semántico específicamente tal como se usa para las aplicaciones de la tienda Windows, consulte [directrices para el zoom semántico](/windows/uwp/controls-and-patterns/semantic-zoom).</span><span class="sxs-lookup"><span data-stu-id="654ed-126">For more information about Semantic Zoom specifically as used for Windows Store apps, see [Guidelines for Semantic Zoom](/windows/uwp/controls-and-patterns/semantic-zoom).</span></span>

<span data-ttu-id="654ed-127">El modelo de uso para el tipo de control **SemanticZoom** es inusual en que existe principalmente para el acceso mediante programación.</span><span class="sxs-lookup"><span data-stu-id="654ed-127">The usage model for the **SemanticZoom** control type is unusual in that it exists mainly for programmatic access.</span></span> <span data-ttu-id="654ed-128">Los clientes de automatización de la interfaz de usuario de Microsoft pueden supervisar y manipular el control de zoom semántico para controlar el estado de la lista.</span><span class="sxs-lookup"><span data-stu-id="654ed-128">Microsoft UI Automation clients can monitor and manipulate the Semantic Zoom control to control the zoomed-in state of the list.</span></span> <span data-ttu-id="654ed-129">Los usuarios que no usan la tecnología de asistencia normalmente manipulan el control de zoom semántico directamente a través de gestos táctiles o métodos abreviados de teclado.</span><span class="sxs-lookup"><span data-stu-id="654ed-129">Users who are not using assistive technology would typically manipulate the Semantic Zoom control directly through touch gestures or keyboard shortcuts.</span></span>

<span data-ttu-id="654ed-130">En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario necesaria, las propiedades, los patrones de control y los eventos para el tipo de control **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="654ed-130">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SemanticZoom** control type.</span></span> <span data-ttu-id="654ed-131">Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles semánticos de zoom en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y</span><span class="sxs-lookup"><span data-stu-id="654ed-131">The UI Automation requirements apply to all Semantic Zoom controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="654ed-132">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="654ed-132">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="654ed-133">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="654ed-133">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="654ed-134">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="654ed-134">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="654ed-135">Patrones de control y propiedades necesarios</span><span class="sxs-lookup"><span data-stu-id="654ed-135">Required Control Patterns and Properties</span></span>](#required-control-patterns-and-properties)
-   [<span data-ttu-id="654ed-136">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="654ed-136">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="654ed-137">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="654ed-137">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="654ed-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="654ed-138">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="654ed-139">Estructura de árbol típica</span><span class="sxs-lookup"><span data-stu-id="654ed-139">Typical Tree Structure</span></span>

<span data-ttu-id="654ed-140">En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece al tipo de control **SemanticZoom** y se describe lo que puede incluirse en cada vista.</span><span class="sxs-lookup"><span data-stu-id="654ed-140">The following table depicts a typical control and content view of the UI Automation tree that pertains to the **SemanticZoom** control type and describes what can be contained in each view.</span></span> <span data-ttu-id="654ed-141">Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="654ed-141">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="654ed-142">Vista de control</span><span class="sxs-lookup"><span data-stu-id="654ed-142">Control View</span></span></th>
<th><span data-ttu-id="654ed-143">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="654ed-143">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="654ed-144">List</span><span class="sxs-lookup"><span data-stu-id="654ed-144">List</span></span>
<ul>
<li><span data-ttu-id="654ed-145">SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="654ed-145">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="654ed-146">Elemento de lista (0 o más)</span><span class="sxs-lookup"><span data-stu-id="654ed-146">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="654ed-147">List</span><span class="sxs-lookup"><span data-stu-id="654ed-147">List</span></span>
<ul>
<li><span data-ttu-id="654ed-148">Elemento de lista (0 o más)</span><span class="sxs-lookup"><span data-stu-id="654ed-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="654ed-149">O:</span><span class="sxs-lookup"><span data-stu-id="654ed-149">Or:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="654ed-150">Vista de control</span><span class="sxs-lookup"><span data-stu-id="654ed-150">Control View</span></span></th>
<th><span data-ttu-id="654ed-151">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="654ed-151">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="654ed-152">SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="654ed-152">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="654ed-153">List</span><span class="sxs-lookup"><span data-stu-id="654ed-153">List</span></span>
<ul>
<li><span data-ttu-id="654ed-154">Elemento de lista (0 o más)</span><span class="sxs-lookup"><span data-stu-id="654ed-154">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="654ed-155">List</span><span class="sxs-lookup"><span data-stu-id="654ed-155">List</span></span>
<ul>
<li><span data-ttu-id="654ed-156">Elemento de lista (0 o más)</span><span class="sxs-lookup"><span data-stu-id="654ed-156">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="654ed-157">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="654ed-157">Relevant Properties</span></span>

<span data-ttu-id="654ed-158">En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles que implementan el tipo de control **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="654ed-158">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **SemanticZoom** control type.</span></span> <span data-ttu-id="654ed-159">Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="654ed-159">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="654ed-160">Propiedad de automatización de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="654ed-160">UI Automation Property</span></span></th>
<th><span data-ttu-id="654ed-161">Value</span><span class="sxs-lookup"><span data-stu-id="654ed-161">Value</span></span></th>
<th><span data-ttu-id="654ed-162">Notas</span><span class="sxs-lookup"><span data-stu-id="654ed-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="654ed-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="654ed-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="654ed-164">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="654ed-164">See notes.</span></span></td>
<td><span data-ttu-id="654ed-165">El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="654ed-165">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="654ed-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="654ed-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="654ed-167">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="654ed-167">See notes.</span></span></td>
<td><span data-ttu-id="654ed-168">El rectángulo exterior que contiene el control completo.</span><span class="sxs-lookup"><span data-stu-id="654ed-168">The outermost rectangle that contains the whole control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="654ed-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="654ed-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="654ed-170">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="654ed-170">See notes.</span></span></td>
<td><span data-ttu-id="654ed-171">Si el control de lista tiene un punto seleccionable (un punto en el que se puede hacer clic para que la lista tenga el foco), dicho punto se debe exponer a través de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="654ed-171">If the list control has a clickable point (a point that can be clicked to cause the list to take focus), that point must be exposed through this property.</span></span> <span data-ttu-id="654ed-172">Si el valor de la propiedad <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> es <strong>true</strong>, el intento de recuperar esta propiedad produce el error de <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="654ed-172">If the value of the <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> property is <strong>TRUE</strong>, attempting to retrieve this property results in the <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> error.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="654ed-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="654ed-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="654ed-174"><strong>SemanticZoom</strong></span><span class="sxs-lookup"><span data-stu-id="654ed-174"><strong>SemanticZoom</strong></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="654ed-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="654ed-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="654ed-176">TRUE</span><span class="sxs-lookup"><span data-stu-id="654ed-176">TRUE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="654ed-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="654ed-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="654ed-178">TRUE</span><span class="sxs-lookup"><span data-stu-id="654ed-178">TRUE</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="654ed-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="654ed-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="654ed-180">false</span><span class="sxs-lookup"><span data-stu-id="654ed-180">FALSE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="654ed-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="654ed-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="654ed-182">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="654ed-182">See notes.</span></span></td>
<td><span data-ttu-id="654ed-183">Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.</span><span class="sxs-lookup"><span data-stu-id="654ed-183">If there is a static text label, this property must expose a reference to that control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="654ed-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="654ed-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="654ed-185">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="654ed-185">See notes.</span></span></td>
<td><span data-ttu-id="654ed-186">Cadena localizada que corresponde al tipo de control <strong>SemanticZoom</strong> .</span><span class="sxs-lookup"><span data-stu-id="654ed-186">A localized string corresponding to the <strong>SemanticZoom</strong> control type.</span></span> <span data-ttu-id="654ed-187">El valor predeterminado es el &quot; zoom semántico &quot; para en-US o inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="654ed-187">The default value is &quot;semantic zoom&quot; for en-US or English (United States).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="654ed-188">Algunos Marcos concatenaron esto como &quot; semanticzoom &quot; .</span><span class="sxs-lookup"><span data-stu-id="654ed-188">Some frameworks concatenated this as &quot;semanticzoom&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="654ed-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="654ed-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="654ed-190">Vea las notas.</span><span class="sxs-lookup"><span data-stu-id="654ed-190">See notes.</span></span></td>
<td><span data-ttu-id="654ed-191">Una cadena vacía es aceptable, o se puede proporcionar un nombre más útil, siempre y cuando no contenga el término zoom semántico, lo que haría que la combinación de tipo de control y el nombre resulten confusas.</span><span class="sxs-lookup"><span data-stu-id="654ed-191">An empty string is acceptable, or a more useful name could be provided, as long as it does not contain the term  semantic zoom , which would make the combination of control type and name confusing.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a><span data-ttu-id="654ed-192">Patrones de control y propiedades necesarios</span><span class="sxs-lookup"><span data-stu-id="654ed-192">Required Control Patterns and Properties</span></span>

<span data-ttu-id="654ed-193">En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que se deben admitir por todos los controles semánticos de zoom.</span><span class="sxs-lookup"><span data-stu-id="654ed-193">The following table lists the UI Automation control patterns required to be supported by all Semantic Zoom controls.</span></span> <span data-ttu-id="654ed-194">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="654ed-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="654ed-195">Patrón de control/Propiedad de patrón</span><span class="sxs-lookup"><span data-stu-id="654ed-195">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="654ed-196">Soporte técnico/valor</span><span class="sxs-lookup"><span data-stu-id="654ed-196">Support/Value</span></span> | <span data-ttu-id="654ed-197">Notas</span><span class="sxs-lookup"><span data-stu-id="654ed-197">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="654ed-198">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="654ed-198">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="654ed-199">Depende</span><span class="sxs-lookup"><span data-stu-id="654ed-199">Depends</span></span>       | <span data-ttu-id="654ed-200">Los controles de zoom semántico admiten el patrón de control [Toggle](uiauto-implementingtoggle.md) para permitir que el zoom se habilite o deshabilite.</span><span class="sxs-lookup"><span data-stu-id="654ed-200">Semantic Zoom controls support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the zoom to be enabled or disabled.</span></span> <span data-ttu-id="654ed-201">[**ToggleState \_ Desactivado**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) se corresponde con el estado plano, todo el activo y [**ToggleState \_ en**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponde a la vista alejada de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="654ed-201">[**ToggleState\_Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the flat, all-up state, and [**ToggleState\_On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the high level, zoomed-out view.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="654ed-202">Eventos necesarios</span><span class="sxs-lookup"><span data-stu-id="654ed-202">Required Events</span></span>

<span data-ttu-id="654ed-203">En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que deben admitir los controles de zoom semántico.</span><span class="sxs-lookup"><span data-stu-id="654ed-203">The following table lists the UI Automation events that Semantic Zoom controls are required to support.</span></span> <span data-ttu-id="654ed-204">Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="654ed-204">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="654ed-205">Evento de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="654ed-205">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="654ed-206">Notas</span><span class="sxs-lookup"><span data-stu-id="654ed-206">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="654ed-207">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="654ed-207">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="654ed-208">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="654ed-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="654ed-209">Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="654ed-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="654ed-210">[**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="654ed-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="654ed-211">Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.</span><span class="sxs-lookup"><span data-stu-id="654ed-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="654ed-212">[**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="654ed-212">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="654ed-213">Observaciones</span><span class="sxs-lookup"><span data-stu-id="654ed-213">Remarks</span></span>

<span data-ttu-id="654ed-214">Si una interfaz de usuario tiene un botón visible para alternar el comportamiento del control de zoom semántico, este botón no debe tener un tipo de control **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="654ed-214">If a UI has a visible button to toggle Semantic Zoom control behavior, this button should not have a **SemanticZoom** control type.</span></span> <span data-ttu-id="654ed-215">Esto es un contador intuitivo, pero el tipo de control **SemanticZoom** caracteriza el contenedor del contenido de zoom, no un botón que controla el zoom.</span><span class="sxs-lookup"><span data-stu-id="654ed-215">This is counter-intuitive, but the **SemanticZoom** control type characterizes the container of the zooming content, not a button that controls the zoom.</span></span> <span data-ttu-id="654ed-216">(Este tipo de botón podría representarse simplemente como un tipo de control [Button](uiauto-supportbuttoncontroltype.md) con el patrón de control [Toggle](uiauto-implementingtoggle.md) ).</span><span class="sxs-lookup"><span data-stu-id="654ed-216">(Such a button could be represented simply as a [Button](uiauto-supportbuttoncontroltype.md) control type with the [Toggle](uiauto-implementingtoggle.md) control pattern.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="654ed-217">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="654ed-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="654ed-218">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="654ed-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="654ed-219">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="654ed-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

