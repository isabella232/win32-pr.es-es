---
title: Información general sobre UI Automation
description: La automatización de la interfaz de usuario de Microsoft es un marco de accesibilidad para Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Automatización de la interfaz de usuario, acerca de
- Automatización de la interfaz de usuario, accesibilidad
- Automatización de la interfaz de usuario, componentes
- Automatización de la interfaz de usuario, API de proveedor
- Automatización de la interfaz de usuario, API de cliente
- Automatización de la interfaz de usuario, archivos de encabezado
- Automatización de la interfaz de usuario, modelo
- components
- accesibilidad
- API de proveedor
- API de cliente
- archivos de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ea29b0abd4c6ed791ae3195f36a0f8184c8596
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420208"
---
# <a name="ui-automation-overview"></a><span data-ttu-id="4d722-115">Información general sobre UI Automation</span><span class="sxs-lookup"><span data-stu-id="4d722-115">UI Automation Overview</span></span>

<span data-ttu-id="4d722-116">La automatización de la interfaz de usuario de Microsoft es un marco de accesibilidad para Windows.</span><span class="sxs-lookup"><span data-stu-id="4d722-116">Microsoft UI Automation is an accessibility framework for Windows.</span></span> <span data-ttu-id="4d722-117">Proporciona acceso mediante programación a la mayoría de los elementos de la interfaz de usuario en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="4d722-117">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="4d722-118">Permite productos de tecnología de asistencia, como lectores de pantalla, para proporcionar información sobre la interfaz de usuario a los usuarios finales y manipular la interfaz de usuario por medios distintos de la entrada estándar.</span><span class="sxs-lookup"><span data-stu-id="4d722-118">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="4d722-119">UI Automation también permite que los scripts de pruebas automatizadas interactúen con la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d722-119">UI Automation also allows automated test scripts to interact with the UI.</span></span>

<span data-ttu-id="4d722-120">La automatización de la interfaz de usuario estaba disponible por primera vez en Windows XP como parte del marco de Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="4d722-120">UI Automation was first available in Windows XP as part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="4d722-121">Aunque una API de C++ no administrada también se publicó en ese momento, la utilidad de las funciones de cliente estaba limitada debido a problemas de interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="4d722-121">Although an unmanaged C++ API was also published at that time, the usefulness of client functions was limited because of interoperability issues.</span></span> <span data-ttu-id="4d722-122">En Windows 7, la API se ha vuelto a escribir en el modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="4d722-122">For Windows 7, the API has been rewritten in the Component Object Model (COM).</span></span>

> [!Note]  
> <span data-ttu-id="4d722-123">Aunque las funciones de la biblioteca introducidas en la versión anterior de la automatización de la interfaz de usuario todavía están documentadas, no se deben usar en nuevas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4d722-123">Although the library functions introduced in the earlier version of UI Automation are still documented, they should not be used in new applications.</span></span>

 

<span data-ttu-id="4d722-124">Las aplicaciones cliente de automatización de la interfaz de usuario se pueden escribir con la certeza de que funcionarán en varios marcos de control de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4d722-124">UI Automation client applications can be written with the assurance that they will work on multiple Microsoft Windows control frameworks.</span></span> <span data-ttu-id="4d722-125">El núcleo de automatización de la interfaz de usuario enmascara cualquier diferencia en los marcos de trabajo que subyacen a varias partes de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d722-125">The UI Automation core masks any differences in the frameworks that underlie various pieces of the UI.</span></span> <span data-ttu-id="4d722-126">Por ejemplo, la propiedad de **contenido** de un botón Windows Presentation Foundation (WPF), la propiedad **título** de un botón de Microsoft Win32 y la propiedad **Alt** de una imagen HTML se asignan todos a una sola propiedad, **nombre**, en la vista de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d722-126">For example, the **Content** property of a Windows Presentation Foundation (WPF) button, the **Caption** property of a Microsoft Win32 button, and the **ALT** property of an HTML image are all mapped to a single property, **Name**, in the UI Automation view.</span></span>

<span data-ttu-id="4d722-127">La automatización de la interfaz de usuario proporciona funcionalidad completa en Windows XP, Windows Server 2003 y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="4d722-127">UI Automation provides full functionality in Windows XP, Windows Server 2003, and later operating systems.</span></span>

<span data-ttu-id="4d722-128">Los proveedores de UI Automation son componentes que implementan la compatibilidad con la automatización de la interfaz de usuario en los controles y ofrecen compatibilidad con las aplicaciones cliente de Microsoft Active Accessibility, a través de un servicio de puente integrado.</span><span class="sxs-lookup"><span data-stu-id="4d722-128">UI Automation providers are components that implement UI Automation support on controls and offer some support for Microsoft Active Accessibility client applications, through a built-in bridging service.</span></span>

> [!Note]  
> <span data-ttu-id="4d722-129">La automatización de la interfaz de usuario no permite la comunicación entre procesos iniciados por distintos usuarios mediante el comando **Ejecutar como** .</span><span class="sxs-lookup"><span data-stu-id="4d722-129">UI Automation does not enable communication between processes that are started by different users through the **Run as** command.</span></span>

 

<span data-ttu-id="4d722-130">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="4d722-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4d722-131">Componentes de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4d722-131">UI Automation Components</span></span>](#ui-automation-components)
-   [<span data-ttu-id="4d722-132">Archivos de encabezado de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4d722-132">UI Automation Header Files</span></span>](#ui-automation-header-files)
-   [<span data-ttu-id="4d722-133">Modelo de la automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="4d722-133">UI Automation Model</span></span>](#ui-automation-model)
-   [<span data-ttu-id="4d722-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d722-134">Related topics</span></span>](#related-topics)

## <a name="ui-automation-components"></a><span data-ttu-id="4d722-135">Componentes de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4d722-135">UI Automation Components</span></span>

<span data-ttu-id="4d722-136">La automatización de la interfaz de usuario tiene cuatro componentes principales, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4d722-136">UI Automation has four main components, as shown in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d722-137">Componente</span><span class="sxs-lookup"><span data-stu-id="4d722-137">Component</span></span></th>
<th><span data-ttu-id="4d722-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d722-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d722-139">API de proveedor</span><span class="sxs-lookup"><span data-stu-id="4d722-139">Provider API</span></span></td>
<td><span data-ttu-id="4d722-140">Un conjunto de interfaces COM que implementan los proveedores de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d722-140">A set of COM interfaces that are implemented by UI Automation providers.</span></span> <span data-ttu-id="4d722-141">Los proveedores de UI Automation son objetos que proporcionan información sobre los elementos de la interfaz de usuario y responden a la entrada mediante programación.</span><span class="sxs-lookup"><span data-stu-id="4d722-141">UI Automation providers are objects that provide information about UI elements and respond to programmatic input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d722-142">API de cliente</span><span class="sxs-lookup"><span data-stu-id="4d722-142">Client API</span></span></td>
<td><span data-ttu-id="4d722-143">Un conjunto de interfaces COM que permiten a las aplicaciones cliente obtener información sobre la interfaz de usuario y enviar la entrada a controles.</span><span class="sxs-lookup"><span data-stu-id="4d722-143">A set of COM interfaces that enable client applications to obtain information about the UI and to send input to controls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="4d722-144">Las funciones descritas en <a href="uiauto-entry-cpfunctions.md">funciones de patrón de control desusadas</a> y <a href="uiauto-entry-uianodefunctions.md">funciones de nodo en desuso</a> están desusadas.</span><span class="sxs-lookup"><span data-stu-id="4d722-144">The functions described in <a href="uiauto-entry-cpfunctions.md">Deprecated Control Pattern Functions</a> and <a href="uiauto-entry-uianodefunctions.md">Deprecated Node Functions</a> are deprecated.</span></span> <span data-ttu-id="4d722-145">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario descritas en <a href="uiauto-entry-uiautoclientinterfaces.md">interfaces de elementos de automatización de la interfaz de usuario para clientes</a>.</span><span class="sxs-lookup"><span data-stu-id="4d722-145">Instead, client applications should use the UI Automation COM interfaces described in <a href="uiauto-entry-uiautoclientinterfaces.md">UI Automation Element Interfaces for Clients</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d722-146">UIAutomationCore.dll</span><span class="sxs-lookup"><span data-stu-id="4d722-146">UIAutomationCore.dll</span></span></td>
<td><span data-ttu-id="4d722-147">La biblioteca en tiempo de ejecución, a veces denominada núcleo de automatización de la interfaz de usuario, que controla la comunicación entre proveedores y clientes.</span><span class="sxs-lookup"><span data-stu-id="4d722-147">The run-time library, sometimes called the UI Automation core, that handles communication between providers and clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d722-148">Oleacc.dll</span><span class="sxs-lookup"><span data-stu-id="4d722-148">Oleacc.dll</span></span></td>
<td><span data-ttu-id="4d722-149">Biblioteca en tiempo de ejecución de Microsoft Active Accessibility y los objetos proxy.</span><span class="sxs-lookup"><span data-stu-id="4d722-149">The run-time library for Microsoft Active Accessibility and the proxy objects.</span></span> <span data-ttu-id="4d722-150">La biblioteca también proporciona objetos de proxy utilizados por Microsoft Microsoft Active Accessibility a proxy de automatización de la interfaz de usuario para admitir controles Win32.</span><span class="sxs-lookup"><span data-stu-id="4d722-150">The library also provides proxy objects used by the Microsoft Microsoft Active Accessibility to UI Automation Proxy to support Win32 controls.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4d722-151">Hay dos maneras de usar la automatización de la interfaz de usuario: para crear compatibilidad con controles personalizados mediante la API de proveedor y para crear aplicaciones cliente que usan el núcleo de automatización de la interfaz de usuario para comunicarse con y recuperar información sobre los elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d722-151">There are two ways of using UI Automation: to create support for custom controls by using the provider API, and to create client applications that use the UI Automation core to communicate with, and retrieve information about, UI elements.</span></span> <span data-ttu-id="4d722-152">En función de su enfoque, debe hacer referencia a diferentes partes de la documentación.</span><span class="sxs-lookup"><span data-stu-id="4d722-152">Depending on your focus, you should refer to different parts of the documentation.</span></span> <span data-ttu-id="4d722-153">Si necesita crear compatibilidad para controles personalizados, vea [la guía del programador del proveedor de automatización](uiauto-providerportal.md)de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d722-153">If you need to create support for custom controls, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span> <span data-ttu-id="4d722-154">Si necesita comunicarse con o recuperar información sobre los elementos de la interfaz de usuario, vea [la guía del programador del cliente de UI Automation](uiauto-clientportal.md).</span><span class="sxs-lookup"><span data-stu-id="4d722-154">If you need to communicate with or retrieve information about UI elements, see [UI Automation Client Programmer's Guide](uiauto-clientportal.md).</span></span>

## <a name="ui-automation-header-files"></a><span data-ttu-id="4d722-155">Archivos de encabezado de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4d722-155">UI Automation Header Files</span></span>

<span data-ttu-id="4d722-156">La API de automatización de la interfaz de usuario se define en varios archivos de encabezado de C/C++ diferentes que se incluyen con el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="4d722-156">The UI Automation API is defined in several different C/C++ header files that are included with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4d722-157">Los archivos de encabezado de automatización de la interfaz de usuario se describen en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="4d722-157">The UI Automation header files are described in the following table:</span></span>



| <span data-ttu-id="4d722-158">Archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="4d722-158">Header file</span></span>           | <span data-ttu-id="4d722-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d722-159">Description</span></span>                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d722-160">UIAutomationClient. h</span><span class="sxs-lookup"><span data-stu-id="4d722-160">UIAutomationClient.h</span></span>  | <span data-ttu-id="4d722-161">Define las interfaces y los elementos de programación relacionados usados por los clientes de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d722-161">Defines the interfaces and related programming elements used by UI Automation clients.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="4d722-162">UIAutomationCore. h</span><span class="sxs-lookup"><span data-stu-id="4d722-162">UIAutomationCore.h</span></span>    | <span data-ttu-id="4d722-163">Define las interfaces y los elementos de programación relacionados usados por los proveedores de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d722-163">Defines the interfaces and related programming elements used by UI Automation providers.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="4d722-164">UIAutomationCoreApi. h</span><span class="sxs-lookup"><span data-stu-id="4d722-164">UIAutomationCoreApi.h</span></span> | <span data-ttu-id="4d722-165">Define constantes, GUID, tipos de datos y estructuras generales que usan los clientes y proveedores de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d722-165">Defines general constants, GUIDs, data types, and structures used by UI Automation clients and providers.</span></span> <span data-ttu-id="4d722-166">También contiene definiciones para las funciones de patrón de control y nodo en desuso.</span><span class="sxs-lookup"><span data-stu-id="4d722-166">It also contains definitions for the deprecated node and control pattern functions.</span></span>                                                                                    |
| <span data-ttu-id="4d722-167">UIAutomation. h</span><span class="sxs-lookup"><span data-stu-id="4d722-167">UIAutomation.h</span></span>        | <span data-ttu-id="4d722-168">Incluye todos los demás archivos de encabezado de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d722-168">Includes all of the other UI Automation header files.</span></span> <span data-ttu-id="4d722-169">Dado que la mayoría de las aplicaciones de automatización de la interfaz de usuario requieren elementos de todos los archivos de encabezado de automatización de la interfaz de usuario, es mejor incluir UIAutomation. h en los proyectos de aplicación de automatización de la interfaz de usuario en lugar de incluir cada archivo individualmente.</span><span class="sxs-lookup"><span data-stu-id="4d722-169">Because most UI Automation applications require elements from all UI Automation header files, it is best to include UIAutomation.h in your UI Automation application projects instead of including each file individually.</span></span> |



 

<span data-ttu-id="4d722-170">Si está desarrollando una aplicación que usa la API de automatización de la interfaz de usuario, debe incluir UIAutomation. h en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="4d722-170">If you are developing an application that uses the UI Automation API, you should include UIAutomation.h in your project.</span></span> <span data-ttu-id="4d722-171">Si la aplicación es compatible con Microsoft Active Accessibility, incluya el archivo de encabezado oleacc. h.</span><span class="sxs-lookup"><span data-stu-id="4d722-171">If your application supports Microsoft Active Accessibility, include the Oleacc.h header file.</span></span> <span data-ttu-id="4d722-172">Las aplicaciones de automatización de la interfaz de usuario que usan GUID también requieren el archivo de encabezado Initguid. h.</span><span class="sxs-lookup"><span data-stu-id="4d722-172">UI Automation applications that use GUIDs also require the Initguid.h header file.</span></span> <span data-ttu-id="4d722-173">Si es necesario, se debe incluir Initguid. h antes de UIAutomation. h.</span><span class="sxs-lookup"><span data-stu-id="4d722-173">If needed, Initguid.h should be included before UIAutomation.h.</span></span>

## <a name="ui-automation-model"></a><span data-ttu-id="4d722-174">Modelo de la automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="4d722-174">UI Automation Model</span></span>

<span data-ttu-id="4d722-175">La automatización de la interfaz de usuario expone todos los elementos de la interfaz de usuario a las aplicaciones cliente como un objeto representado por la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) .</span><span class="sxs-lookup"><span data-stu-id="4d722-175">UI Automation exposes every element of the UI to client applications as an object represented by the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="4d722-176">Los elementos se encuentran en una estructura de árbol, con el escritorio como el elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="4d722-176">Elements are contained in a tree structure, with the desktop as the root element.</span></span> <span data-ttu-id="4d722-177">Los clientes pueden filtrar la vista sin formato del árbol como una vista de control o una vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="4d722-177">Clients can filter the raw view of the tree as a control view or a content view.</span></span> <span data-ttu-id="4d722-178">Estas vistas estándar de la estructura se pueden ver fácilmente mediante el uso de la aplicación de [inspección](inspect-objects.md) que se incluye con el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4d722-178">These standard views of the structure can easily be seen by using the [Inspect](inspect-objects.md) application that is included with the Windows SDK.</span></span> <span data-ttu-id="4d722-179">Las aplicaciones también pueden crear vistas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="4d722-179">Applications can also create custom views.</span></span>

<span data-ttu-id="4d722-180">Un elemento de automatización de la interfaz de usuario expone propiedades del control o elemento de la interfaz de usuario que representa.</span><span class="sxs-lookup"><span data-stu-id="4d722-180">A UI Automation element exposes properties of the control or UI element that it represents.</span></span> <span data-ttu-id="4d722-181">Una de estas propiedades es el tipo de control, que define la apariencia y la funcionalidad básicas del control o el elemento de la interfaz de usuario como una única entidad reconocible, por ejemplo, un botón o una casilla.</span><span class="sxs-lookup"><span data-stu-id="4d722-181">One of these properties is the control type, which defines the basic appearance and functionality of the control or UI element as a single recognizable entity, for example, a button or check box.</span></span> <span data-ttu-id="4d722-182">Para obtener más información sobre los tipos de control, vea [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4d722-182">For more information about control types, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="4d722-183">Además, un elemento de automatización de la interfaz de usuario expone uno o más patrones de control.</span><span class="sxs-lookup"><span data-stu-id="4d722-183">In addition, a UI Automation element exposes one or more control patterns.</span></span> <span data-ttu-id="4d722-184">Un patrón de control proporciona un conjunto de propiedades que son específicas de un tipo de control determinado.</span><span class="sxs-lookup"><span data-stu-id="4d722-184">A control pattern provides a set of properties that are specific to a particular control type.</span></span> <span data-ttu-id="4d722-185">Un patrón de control también expone métodos que permiten a las aplicaciones cliente obtener más información sobre el elemento y proporcionar la entrada al elemento.</span><span class="sxs-lookup"><span data-stu-id="4d722-185">A control pattern also exposes methods that enable client applications to get more information about the element and to provide input to the element.</span></span> <span data-ttu-id="4d722-186">Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4d722-186">For more information about control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

> [!Note]  
> <span data-ttu-id="4d722-187">No hay una correspondencia uno a uno entre los tipos de control y los patrones de control.</span><span class="sxs-lookup"><span data-stu-id="4d722-187">There is no one-to-one correspondence between control types and control patterns.</span></span> <span data-ttu-id="4d722-188">Un patrón de control puede ser compatible con varios tipos de control y un control puede admitir varios patrones de control, cada uno de los cuales expone diferentes aspectos de su comportamiento.</span><span class="sxs-lookup"><span data-stu-id="4d722-188">A control pattern may be supported by multiple control types, and a control may support multiple control patterns, each of which exposes different aspects of its behavior.</span></span> <span data-ttu-id="4d722-189">Por ejemplo, un cuadro combinado tiene al menos dos patrones de control: uno que representa su capacidad para expandir y contraer, y otro que representa el mecanismo de selección.</span><span class="sxs-lookup"><span data-stu-id="4d722-189">For example, a combo box has at least two control patterns: one that represents its ability to expand and collapse, and another that represents the selection mechanism.</span></span> <span data-ttu-id="4d722-190">Sin embargo, un control solo puede presentar un tipo de control único.</span><span class="sxs-lookup"><span data-stu-id="4d722-190">However, a control can exhibit only a single control type.</span></span>

 

<span data-ttu-id="4d722-191">La automatización de la interfaz de usuario proporciona información a las aplicaciones cliente a través de eventos.</span><span class="sxs-lookup"><span data-stu-id="4d722-191">UI Automation provides information to client applications through events.</span></span> <span data-ttu-id="4d722-192">A diferencia de WinEvents, los eventos de automatización de la interfaz de usuario no se basan en un mecanismo de difusión.</span><span class="sxs-lookup"><span data-stu-id="4d722-192">Unlike WinEvents, UI Automation events are not based on a broadcast mechanism.</span></span> <span data-ttu-id="4d722-193">Los clientes de automatización de la interfaz de usuario se registran para notificaciones de eventos específicas y pueden solicitar que se pasen propiedades específicas e información de patrón de control a sus controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="4d722-193">UI Automation clients register for specific event notifications and can request that specific properties and control pattern information be passed to their event handlers.</span></span> <span data-ttu-id="4d722-194">Además, un evento de automatización de la interfaz de usuario contiene una referencia al elemento que lo generó.</span><span class="sxs-lookup"><span data-stu-id="4d722-194">In addition, a UI Automation event contains a reference to the element that raised it.</span></span> <span data-ttu-id="4d722-195">Los proveedores pueden mejorar el rendimiento generando eventos de forma selectiva, dependiendo de si los clientes están escuchando.</span><span class="sxs-lookup"><span data-stu-id="4d722-195">Providers can improve performance by raising events selectively, depending on whether any clients are listening.</span></span> <span data-ttu-id="4d722-196">Para más información sobre eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4d722-196">For more information about events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d722-197">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d722-197">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4d722-198">**Vista**</span><span class="sxs-lookup"><span data-stu-id="4d722-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4d722-199">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4d722-199">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="4d722-200">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4d722-200">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="4d722-201">Información general sobre eventos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4d722-201">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 





