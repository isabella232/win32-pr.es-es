---
title: Información general sobre proveedores de UI Automation
description: En este tema se proporciona información general sobre cómo los desarrolladores de controles implementan proveedores de automatización de la interfaz de usuario.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- Automatización de la interfaz de usuario, información general de proveedores
- Automatización de la interfaz de usuario, tipos de proveedor
- Automatización de la interfaz de usuario, conceptos del proveedor
- proveedores, acerca de
- proveedores, tipos
- proveedores, conceptos
- proveedores, elementos
- proveedores, navegación
- proveedores, vistas
- proveedores, marcos de trabajo
- proveedores, fragmentos
- proveedores, hosts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994111"
---
# <a name="ui-automation-providers-overview"></a><span data-ttu-id="51920-115">Información general sobre proveedores de UI Automation</span><span class="sxs-lookup"><span data-stu-id="51920-115">UI Automation Providers Overview</span></span>

<span data-ttu-id="51920-116">Un proveedor de automatización de la interfaz de usuario de Microsoft es un objeto de software que expone un elemento de la interfaz de usuario de una aplicación para que las aplicaciones cliente de accesibilidad puedan recuperar información sobre el elemento e invocar su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="51920-116">A Microsoft UI Automation provider is a software object that exposes an element of an application's UI so that accessibility client applications can retrieve information about the element and invoke its functionality.</span></span> <span data-ttu-id="51920-117">En general, cada control u otro elemento distinto de una interfaz de usuario tiene un proveedor.</span><span class="sxs-lookup"><span data-stu-id="51920-117">In general, each control or other distinct element in a UI has a provider.</span></span>

<span data-ttu-id="51920-118">Microsoft incluye un proveedor para cada uno de los controles estándar que se proporcionan con Microsoft Win32, Windows Forms y Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="51920-118">Microsoft includes a provider for each of the standard controls that are supplied with Microsoft Win32, Windows Forms, and Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="51920-119">Esto significa que los controles estándar se exponen automáticamente a los clientes de automatización de la interfaz de usuario; no es necesario implementar ninguna interfaz de accesibilidad para los controles estándar.</span><span class="sxs-lookup"><span data-stu-id="51920-119">This means that the standard controls are automatically exposed to UI Automation clients; you do not need to implement any accessibility interfaces for the standard controls.</span></span>

<span data-ttu-id="51920-120">Si su aplicación incluye controles personalizados, debe implementar proveedores de automatización de la interfaz de usuario para esos controles para que puedan tener acceso a ellos las aplicaciones cliente de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="51920-120">If your application includes any custom controls, you need to implement UI Automation providers for those controls to make them accessible to accessibility client applications.</span></span> <span data-ttu-id="51920-121">También debe implementar proveedores para cualquier control de terceros que no incluya un proveedor.</span><span class="sxs-lookup"><span data-stu-id="51920-121">You also need to implement providers for any third party controls that do not include a provider.</span></span> <span data-ttu-id="51920-122">Para implementar un proveedor, implemente interfaces del proveedor de automatización de la interfaz de usuario e interfaces de patrón de control.</span><span class="sxs-lookup"><span data-stu-id="51920-122">You implement a provider by implementing UI Automation provider interfaces and control pattern interfaces.</span></span>

<span data-ttu-id="51920-123">En este tema se proporciona información general sobre cómo los desarrolladores de controles implementan proveedores de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="51920-123">This topic provides an overview of how control developers implement UI Automation providers.</span></span> <span data-ttu-id="51920-124">Incluye las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="51920-124">It includes the following sections.</span></span>

-   [<span data-ttu-id="51920-125">Tipos de proveedores</span><span class="sxs-lookup"><span data-stu-id="51920-125">Types of Providers</span></span>](#types-of-providers)
-   [<span data-ttu-id="51920-126">Conceptos del proveedor de la automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="51920-126">UI Automation Provider Concepts</span></span>](#ui-automation-provider-concepts)
    -   [<span data-ttu-id="51920-127">Elementos</span><span class="sxs-lookup"><span data-stu-id="51920-127">Elements</span></span>](#elements)
    -   [<span data-ttu-id="51920-128">Marcos de trabajo</span><span class="sxs-lookup"><span data-stu-id="51920-128">Frameworks</span></span>](#frameworks)
    -   [<span data-ttu-id="51920-129">Fragmentos</span><span class="sxs-lookup"><span data-stu-id="51920-129">Fragments</span></span>](#fragments)
    -   [<span data-ttu-id="51920-130">Hosts</span><span class="sxs-lookup"><span data-stu-id="51920-130">Hosts</span></span>](#hosts)
-   [<span data-ttu-id="51920-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51920-131">Related topics</span></span>](#related-topics)

## <a name="types-of-providers"></a><span data-ttu-id="51920-132">Tipos de proveedores</span><span class="sxs-lookup"><span data-stu-id="51920-132">Types of Providers</span></span>

<span data-ttu-id="51920-133">Los proveedores de automatización de la interfaz de usuario se dividen en dos categorías: proveedores del lado servidor y proveedores del lado cliente (o *proxy*).</span><span class="sxs-lookup"><span data-stu-id="51920-133">UI Automation providers fall into two categories: server-side providers, and client-side (or *proxy*) providers.</span></span>

<span data-ttu-id="51920-134">Un proveedor del lado servidor es un objeto, como un control personalizado, que contiene su propia implementación nativa de las interfaces relevantes del proveedor de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="51920-134">A server-side provider is an object, such as a custom control, that contains its own native implementation of the relevant UI Automation provider interfaces.</span></span> <span data-ttu-id="51920-135">Un proveedor del lado servidor se comunica con las aplicaciones cliente a través del límite del proceso al exponer su implementación de las interfaces del proveedor al núcleo de automatización de la interfaz de usuario, que ofrece servicio a las solicitudes de los clientes.</span><span class="sxs-lookup"><span data-stu-id="51920-135">A server-side provider communicates with client applications across the process boundary by exposing its implementation of the provider interfaces to the UI Automation core, which services requests from clients.</span></span> <span data-ttu-id="51920-136">Para obtener más información sobre los proveedores del lado servidor, vea [implementar un Server-Side proveedor de automatización de la interfaz de usuario](uiauto-serversideprovider.md).</span><span class="sxs-lookup"><span data-stu-id="51920-136">For more information about server-side providers, see [Implementing a Server-Side UI Automation Provider](uiauto-serversideprovider.md).</span></span>

<span data-ttu-id="51920-137">Un proveedor del lado cliente, o proxy, es un objeto que implementa las interfaces del proveedor de automatización de la interfaz de usuario en nombre de un control, no incluye una implementación de proveedor completa propia.</span><span class="sxs-lookup"><span data-stu-id="51920-137">A client-side provider, or proxy, is an object that implements UI Automation provider interfaces on behalf of a control does not include a full provider implementation of its own.</span></span> <span data-ttu-id="51920-138">Sin un proxy, este tipo de control es principalmente opaco a la automatización de la interfaz de usuario, que puede proporcionar solo información básica disponible en el identificador de ventana (**hWnd**), como la ubicación del control.</span><span class="sxs-lookup"><span data-stu-id="51920-138">Without a proxy, such a control is largely opaque to UI Automation, which can supply only basic information available from the window handle (**HWND**), such as the control location.</span></span> <span data-ttu-id="51920-139">Normalmente, los proveedores de proxy se comunican con la aplicación a través del límite del proceso mediante el envío y la recepción de mensajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="51920-139">Typically, proxy providers communicate with the application across the process boundary by sending and receiving Windows messages.</span></span> <span data-ttu-id="51920-140">Para obtener más información, vea [implementar un proveedor de automatización de la interfaz de usuario de Client-Side (proxy)](uiauto-clientsideprovider.md).</span><span class="sxs-lookup"><span data-stu-id="51920-140">For more information, see [Implementing a Client-Side (Proxy) UI Automation Provider](uiauto-clientsideprovider.md).</span></span>

## <a name="ui-automation-provider-concepts"></a><span data-ttu-id="51920-141">Conceptos del proveedor de la automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="51920-141">UI Automation Provider Concepts</span></span>

<span data-ttu-id="51920-142">En esta sección se ofrecen breves explicaciones de algunos de los conceptos clave que debe entender para implementar proveedores de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="51920-142">This section provides brief explanations of some of the key concepts you need to understand in order to implement UI Automation providers.</span></span>

### <a name="elements"></a><span data-ttu-id="51920-143">Elementos</span><span class="sxs-lookup"><span data-stu-id="51920-143">Elements</span></span>

<span data-ttu-id="51920-144">Los elementos de automatización de la interfaz de usuario son partes de la interfaz de usuario, normalmente ventanas o controles, que son visibles para los clientes de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="51920-144">UI Automation elements are pieces of the UI—typically windows or controls—that are visible to UI Automation clients.</span></span> <span data-ttu-id="51920-145">Entre los ejemplos se incluyen ventanas de aplicación, paneles, botones, información sobre herramientas, cuadros de lista y elementos de lista.</span><span class="sxs-lookup"><span data-stu-id="51920-145">Examples include application windows, panes, buttons, tooltips, list boxes, and list items.</span></span>

<span data-ttu-id="51920-146">Los elementos de automatización de la interfaz de usuario se exponen a los clientes como un árbol.</span><span class="sxs-lookup"><span data-stu-id="51920-146">UI Automation elements are exposed to clients as a tree.</span></span> <span data-ttu-id="51920-147">La automatización de la interfaz de usuario construye el árbol navegando de un elemento a otro.</span><span class="sxs-lookup"><span data-stu-id="51920-147">UI Automation constructs the tree by navigating from one element to another.</span></span> <span data-ttu-id="51920-148">El proveedor habilita la navegación para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="51920-148">Navigation is enabled by the provider for each element.</span></span> <span data-ttu-id="51920-149">Cada elemento puede apuntar a su propio elemento primario, sus elementos relacionados y su primer y último elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="51920-149">Each element can point to its own parent element, its sibling elements, and its first and last child elements.</span></span>

<span data-ttu-id="51920-150">Un cliente puede ver el árbol de automatización de la interfaz de usuario en tres vistas principales, como se describe en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="51920-150">A client can see the UI Automation tree in three principal views, as described in the following table:</span></span>



| <span data-ttu-id="51920-151">Ver</span><span class="sxs-lookup"><span data-stu-id="51920-151">View</span></span>         | <span data-ttu-id="51920-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="51920-152">Description</span></span>                                                    |
|--------------|----------------------------------------------------------------|
| <span data-ttu-id="51920-153">Vista sin formato</span><span class="sxs-lookup"><span data-stu-id="51920-153">Raw view</span></span>     | <span data-ttu-id="51920-154">Incluye todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="51920-154">Includes all elements.</span></span>                                         |
| <span data-ttu-id="51920-155">Vista de control</span><span class="sxs-lookup"><span data-stu-id="51920-155">Control view</span></span> | <span data-ttu-id="51920-156">Incluye elementos que son controles.</span><span class="sxs-lookup"><span data-stu-id="51920-156">Includes elements that are controls.</span></span>                           |
| <span data-ttu-id="51920-157">Vista de contenido</span><span class="sxs-lookup"><span data-stu-id="51920-157">Content view</span></span> | <span data-ttu-id="51920-158">Incluye elementos de control que transmiten información al usuario.</span><span class="sxs-lookup"><span data-stu-id="51920-158">Includes control elements that convey information to the user.</span></span> |



 

<span data-ttu-id="51920-159">Es responsabilidad de la implementación del proveedor definir un elemento como un elemento de contenido o un elemento de control.</span><span class="sxs-lookup"><span data-stu-id="51920-159">It is the responsibility of the provider implementation to define an element as a content element or a control element.</span></span> <span data-ttu-id="51920-160">Los elementos de control pueden o no ser elementos de contenido, pero todos los elementos de contenido son elementos de control.</span><span class="sxs-lookup"><span data-stu-id="51920-160">Control elements may or may not also be content elements, but all content elements are control elements.</span></span>

<span data-ttu-id="51920-161">Para obtener más información sobre la vista de cliente del árbol, vea [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="51920-161">For more information on the client view of the tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

### <a name="frameworks"></a><span data-ttu-id="51920-162">Marcos de trabajo</span><span class="sxs-lookup"><span data-stu-id="51920-162">Frameworks</span></span>

<span data-ttu-id="51920-163">Un marco de trabajo es un componente que administra controles secundarios, pruebas de aciertos y representación en un área de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="51920-163">A framework is a component that manages child controls, hit-testing, and rendering in an area of the screen.</span></span> <span data-ttu-id="51920-164">Por ejemplo, una ventana de Win32, que a menudo se conoce como **hWnd**, puede actuar como un marco de trabajo que contiene varios elementos de automatización de la interfaz de usuario, como una barra de menús, una barra de estado y botones.</span><span class="sxs-lookup"><span data-stu-id="51920-164">For example, a Win32 window, often referred to as an **HWND**, can serve as a framework that contains multiple UI Automation elements, such as a menu bar, a status bar, and buttons.</span></span>

<span data-ttu-id="51920-165">Los controles de contenedor de Win32, como los cuadros de lista y los controles de vista de árbol, se consideran marcos de trabajo porque contienen su propio código para representar elementos secundarios y realizar pruebas de aciertos en ellos.</span><span class="sxs-lookup"><span data-stu-id="51920-165">Win32 container controls such as list boxes and tree-view controls are considered to be frameworks because they contain their own code for rendering child items and performing hit-testing on them.</span></span> <span data-ttu-id="51920-166">Por el contrario, un cuadro de lista de WPF no es un marco de trabajo, porque la representación y las pruebas de aciertos se controlan mediante la ventana contenedora.</span><span class="sxs-lookup"><span data-stu-id="51920-166">By contrast, a WPF list box is not a framework, because the rendering and hit-testing is being handled by the containing window.</span></span>

<span data-ttu-id="51920-167">La interfaz de usuario de una aplicación se puede componer de diferentes marcos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="51920-167">The UI in an application can be made up of different frameworks.</span></span> <span data-ttu-id="51920-168">Por ejemplo, un **hWnd** en una aplicación podría contener HTML dinámico (DHTML) que a su vez puede contener un componente como un cuadro combinado en un **hWnd**.</span><span class="sxs-lookup"><span data-stu-id="51920-168">For example, an **HWND** in an application might contain Dynamic HTML (DHTML) which in turn can contain a component such as a combo box in an **HWND**.</span></span>

### <a name="fragments"></a><span data-ttu-id="51920-169">Fragments</span><span class="sxs-lookup"><span data-stu-id="51920-169">Fragments</span></span>

<span data-ttu-id="51920-170">Un subárbol completo de elementos de un marco de trabajo determinado se denomina fragmento.</span><span class="sxs-lookup"><span data-stu-id="51920-170">A complete subtree of elements from a particular framework is called a fragment.</span></span> <span data-ttu-id="51920-171">El elemento del nodo raíz del subárbol se denomina raíz del fragmento.</span><span class="sxs-lookup"><span data-stu-id="51920-171">The element at the root node of the subtree is called a fragment root.</span></span> <span data-ttu-id="51920-172">Una raíz de fragmento no tiene un elemento primario, pero se hospeda en otro marco de trabajo, normalmente una ventana Win32 (**hWnd**).</span><span class="sxs-lookup"><span data-stu-id="51920-172">A fragment root does not have a parent, but is hosted within some other framework, usually a Win32 window (**HWND**).</span></span>

### <a name="hosts"></a><span data-ttu-id="51920-173">Hosts</span><span class="sxs-lookup"><span data-stu-id="51920-173">Hosts</span></span>

<span data-ttu-id="51920-174">El nodo raíz de cada fragmento se debe hospedar en un elemento, normalmente una ventana Win32 (**hWnd**).</span><span class="sxs-lookup"><span data-stu-id="51920-174">The root node of every fragment must be hosted in an element, usually a Win32 window (**HWND**).</span></span> <span data-ttu-id="51920-175">La excepción es el escritorio, que no se hospeda en ningún otro elemento.</span><span class="sxs-lookup"><span data-stu-id="51920-175">The exception is the desktop, which is not hosted in any other element.</span></span> <span data-ttu-id="51920-176">El host de un control personalizado es el **hWnd** del propio control, no la ventana de la aplicación o cualquier otra ventana que pueda contener grupos de controles de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="51920-176">The host of a custom control is the **HWND** of the control itself, not the application window or any other window that might contain groups of top-level controls.</span></span>

<span data-ttu-id="51920-177">El host de un fragmento desempeña un papel importante en el suministro de servicios de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="51920-177">The host of a fragment plays an important role in providing UI Automation services.</span></span> <span data-ttu-id="51920-178">Permite la navegación a la raíz del fragmento y ofrece algunas propiedades predeterminadas para que el proveedor personalizado no tenga que implementarlas.</span><span class="sxs-lookup"><span data-stu-id="51920-178">It enables navigation to the fragment root, and supplies some default properties so that the custom provider does not have to implement them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51920-179">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51920-179">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="51920-180">**Vista**</span><span class="sxs-lookup"><span data-stu-id="51920-180">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="51920-181">Implementar un proveedor de automatización de la interfaz de usuario de Client-Side</span><span class="sxs-lookup"><span data-stu-id="51920-181">Implementing a Client-Side UI Automation Provider</span></span>](uiauto-clientsideprovider.md)
</dt> <dt>

[<span data-ttu-id="51920-182">Implementar un proveedor de automatización de la interfaz de usuario de Server-Side</span><span class="sxs-lookup"><span data-stu-id="51920-182">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="51920-183">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="51920-183">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




