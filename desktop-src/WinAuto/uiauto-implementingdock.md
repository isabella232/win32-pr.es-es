---
title: Dock (patrón de control)
description: Describe las directrices y convenciones para implementar IDockProvider, incluida información sobre propiedades y métodos. El patrón de control Dock se usa para exponer las propiedades de acoplamiento de un control dentro de un contenedor de acoplamiento.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Dock
- Automatización de la interfaz de usuario, patrón de control Dock
- Automatización de la interfaz de usuario, IDockProvider
- IDockProvider
- implementación de patrones de control Dock de UI Automation
- patrones de control Dock
- patrones de control, IDockProvider
- patrones de control, implementar el Dock de automatización de la interfaz de usuario
- patrones de control, Dock
- interfaces, IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87381669889ca7dd33811a030a718448f4b79cb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903397"
---
# <a name="dock-control-pattern"></a><span data-ttu-id="a4a7c-114">Dock (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="a4a7c-114">Dock Control Pattern</span></span>

<span data-ttu-id="a4a7c-115">Describe las directrices y convenciones para implementar [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-115">Describes guidelines and conventions for implementing [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), including information about properties and methods.</span></span> <span data-ttu-id="a4a7c-116">El patrón de control **Dock** se usa para exponer las propiedades de acoplamiento de un control dentro de un contenedor de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-116">The **Dock** control pattern is used to expose the dock properties of a control within a docking container.</span></span>

<span data-ttu-id="a4a7c-117">Un contenedor de acoplamiento es un control que permite organizar elementos secundarios horizontal y verticalmente, relacionados entre sí.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-117">A docking container is a control that allows you to arrange child elements horizontally and vertically, relative to each other.</span></span> <span data-ttu-id="a4a7c-118">La siguiente imagen muestra un contenedor de acoplamiento con dos elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-118">The following image shows a docking container with two child elements.</span></span> <span data-ttu-id="a4a7c-119">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="a4a7c-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![captura de pantalla que muestra el contenedor de acoplamiento con dos elementos secundarios acoplados](images/dockxmpl.jpg)

<span data-ttu-id="a4a7c-121">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a4a7c-122">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="a4a7c-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="a4a7c-123">Miembros requeridos para **IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="a4a7c-123">Required Members for **IDockProvider**</span></span>](#required-members-for-idockprovider)
-   [<span data-ttu-id="a4a7c-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a4a7c-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="a4a7c-125">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="a4a7c-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="a4a7c-126">Al implementar el patrón de control **Dock** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="a4a7c-126">When implementing the **Dock** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="a4a7c-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) no expone ninguna propiedad del contenedor de acoplamiento ni propiedades de controles que estén acoplados adyacentes al control actual dentro del contenedor de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) does not expose any properties of the docking container or any properties of controls that are docked adjacent to the current control within the docking container.</span></span>
-   <span data-ttu-id="a4a7c-128">Los controles se acoplan de forma relativa entre ellos, según su valor actual de orden Z; cuanto mayor es su ubicación de orden Z, más lejos se colocan del borde especificado del contenedor de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-128">Controls are docked relative to each other based on their current z-order; the higher their z-order placement, the farther they are placed from the specified edge of the docking container.</span></span>
-   <span data-ttu-id="a4a7c-129">Si se cambia el tamaño del contenedor de acoplamiento, los controles acoplados dentro del contenedor cambiarán de posición y se alinearán con el mismo borde en el que estaban originalmente acoplados.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-129">If the docking container is resized, any docked controls within the container will be repositioned flush to the same edge to which they were originally docked.</span></span> <span data-ttu-id="a4a7c-130">Los controles acoplados también cambiarán de tamaño para rellenar cualquier espacio dentro del contenedor según el comportamiento de acoplamiento de la propiedad [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) .</span><span class="sxs-lookup"><span data-stu-id="a4a7c-130">The docked controls will also resize to fill any space within the container according to the docking behavior of their [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) property.</span></span> <span data-ttu-id="a4a7c-131">Por ejemplo, si se especifica **DockPosition \_ Top** , los lados izquierdo y derecho del control se expandirán para rellenar el espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-131">For example, if **DockPosition\_Top** is specified, the left and right sides of the control will expand to fill any available space.</span></span> <span data-ttu-id="a4a7c-132">Si se especifica **DockPosition \_ Fill** , los cuatro lados del control se expandirán para rellenar el espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-132">If **DockPosition\_Fill** is specified, all four sides of the control will expand to fill any available space.</span></span>
-   <span data-ttu-id="a4a7c-133">En un sistema de varios monitores, los controles se deben acoplar en el lado izquierdo o derecho del monitor actual.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-133">On a multi-monitor system, controls should dock to the left or right side of the current monitor.</span></span> <span data-ttu-id="a4a7c-134">Si no es posible, deben acoplarse en el lado izquierdo del monitor que se encuentre más a la izquierda o en el lado derecho del monitor que se encuentre más a la derecha.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-134">If that is not possible, they should dock to the left side of the leftmost monitor or the right side of the rightmost monitor.</span></span>

## <a name="required-members-for-idockprovider"></a><span data-ttu-id="a4a7c-135">Miembros requeridos para **IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="a4a7c-135">Required Members for **IDockProvider**</span></span>

<span data-ttu-id="a4a7c-136">Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) .</span><span class="sxs-lookup"><span data-stu-id="a4a7c-136">The following properties and methods are required for implementing the [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) interface.</span></span>



| <span data-ttu-id="a4a7c-137">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="a4a7c-137">Required members</span></span>                                                | <span data-ttu-id="a4a7c-138">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="a4a7c-138">Member type</span></span> | <span data-ttu-id="a4a7c-139">Notas</span><span class="sxs-lookup"><span data-stu-id="a4a7c-139">Notes</span></span> |
|-----------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="a4a7c-140">**DockPosition**</span><span class="sxs-lookup"><span data-stu-id="a4a7c-140">**DockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | <span data-ttu-id="a4a7c-141">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4a7c-141">Property</span></span>    | <span data-ttu-id="a4a7c-142">None</span><span class="sxs-lookup"><span data-stu-id="a4a7c-142">None</span></span>  |
| [<span data-ttu-id="a4a7c-143">**SetDockPosition**</span><span class="sxs-lookup"><span data-stu-id="a4a7c-143">**SetDockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | <span data-ttu-id="a4a7c-144">Método</span><span class="sxs-lookup"><span data-stu-id="a4a7c-144">Method</span></span>      | <span data-ttu-id="a4a7c-145">None</span><span class="sxs-lookup"><span data-stu-id="a4a7c-145">None</span></span>  |



 

<span data-ttu-id="a4a7c-146">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="a4a7c-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4a7c-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a4a7c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4a7c-148">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="a4a7c-148">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="a4a7c-149">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="a4a7c-149">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="a4a7c-150">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="a4a7c-150">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




