---
title: Transform (patrón de control)
description: Describe las directrices y convenciones para implementar ITransformProvider y ITransformProvider2, incluida información sobre propiedades y métodos.
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Transform
- Automatización de la interfaz de usuario, patrón de control Transform
- Automatización de la interfaz de usuario, ITransformProvider
- ITransformProvider
- implementar patrones de control de transformación de automatización de la interfaz de usuario
- Transformar patrones de control
- patrones de control, ITransformProvider
- patrones de control, implementar la transformación de automatización de la interfaz de usuario
- patrones de control, transformación
- interfaces, ITransformProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533345"
---
# <a name="transform-control-pattern"></a><span data-ttu-id="db33f-113">Transform (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="db33f-113">Transform Control Pattern</span></span>

<span data-ttu-id="db33f-114">Describe las directrices y convenciones para implementar [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) y [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="db33f-114">Describes guidelines and conventions for implementing [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) and [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), including information about properties and methods.</span></span> <span data-ttu-id="db33f-115">El patrón de control Transform se usa para admitir controles que se pueden desplazar, cambiar de tamaño o girar dentro de un espacio bidimensional.</span><span class="sxs-lookup"><span data-stu-id="db33f-115">The Transform control pattern is used to support controls that can be moved, resized, or rotated within a two-dimensional space.</span></span>

<span data-ttu-id="db33f-116">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="db33f-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="db33f-117">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="db33f-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="db33f-118">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="db33f-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="db33f-119">Miembros requeridos para **ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="db33f-119">Required Members for **ITransformProvider**</span></span>](#required-members-for-itransformprovider)
-   [<span data-ttu-id="db33f-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db33f-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="db33f-121">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="db33f-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="db33f-122">Al implementar el patrón de control **Transform** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="db33f-122">When implementing the **Transform** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="db33f-123">La compatibilidad con este patrón de control no se limita a los objetos del escritorio.</span><span class="sxs-lookup"><span data-stu-id="db33f-123">Support for this control pattern is not limited to objects on the desktop.</span></span> <span data-ttu-id="db33f-124">Este patrón de control también lo admite los elementos secundarios de un objeto contenedor si los elementos secundarios se pueden mover, cambiar de tamaño o girar libremente dentro de los límites del contenedor.</span><span class="sxs-lookup"><span data-stu-id="db33f-124">This control pattern must also be supported by the children of a container object if the children can be moved, resized, or rotated freely within the boundaries of the container.</span></span>
-   <span data-ttu-id="db33f-125">Un objeto no se puede mover, cambiar de tamaño o girar de manera que su ubicación en pantalla resultante quede completamente fuera de las coordenadas de su contenedor y que, por tanto, sea inaccesible para el teclado o el mouse (por ejemplo, cuando una ventana de nivel superior se mueva fuera de la pantalla o un objeto secundario se mueva fuera de los límites de la ventanilla del contenedor).</span><span class="sxs-lookup"><span data-stu-id="db33f-125">An object cannot be moved, resized, or rotated such that its resulting screen location would be completely outside the coordinates of its container and therefore inaccessible to the keyboard or mouse (for example, when a top-level window is moved off-screen or a child object is moved outside the boundaries of the container's viewport).</span></span> <span data-ttu-id="db33f-126">En estos casos, el objeto se coloca lo más cerca posible de las coordenadas de pantalla solicitadas reemplazando las coordenadas superiores o izquierdas para que se encuentren dentro de los límites del contenedor.</span><span class="sxs-lookup"><span data-stu-id="db33f-126">In these cases, the object is placed as close to the requested screen coordinates as possible with the top or left coordinates overridden to be within the container boundaries.</span></span>
-   <span data-ttu-id="db33f-127">Para sistemas de varios monitores, si se mueve un objeto, cambia de tamaño o gira completamente fuera de las coordenadas de pantalla de escritorio combinadas, el objeto se coloca en el monitor principal lo más cerca posible de las coordenadas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="db33f-127">For multi-monitor systems, if an object is moved, resized, or rotated completely outside the combined desktop screen coordinates, the object is placed on the primary monitor as close to the requested coordinates as possible.</span></span>
-   <span data-ttu-id="db33f-128">Todos los parámetros y los valores de propiedad son absolutos e independientes de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="db33f-128">All parameters and property values are absolute and independent of locale.</span></span>

## <a name="required-members-for-itransformprovider"></a><span data-ttu-id="db33f-129">Miembros requeridos para **ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="db33f-129">Required Members for **ITransformProvider**</span></span>

<span data-ttu-id="db33f-130">Se requieren las siguientes propiedades y métodos para implementar la interfaz [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .</span><span class="sxs-lookup"><span data-stu-id="db33f-130">The following properties and methods are required for implementing the [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="db33f-131">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="db33f-131">Required members</span></span>                                         | <span data-ttu-id="db33f-132">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="db33f-132">Member type</span></span> | <span data-ttu-id="db33f-133">Notas</span><span class="sxs-lookup"><span data-stu-id="db33f-133">Notes</span></span> |
|----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="db33f-134">**CanMove**</span><span class="sxs-lookup"><span data-stu-id="db33f-134">**CanMove**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | <span data-ttu-id="db33f-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="db33f-135">Property</span></span>    | <span data-ttu-id="db33f-136">None</span><span class="sxs-lookup"><span data-stu-id="db33f-136">None</span></span>  |
| [<span data-ttu-id="db33f-137">**CanResize**</span><span class="sxs-lookup"><span data-stu-id="db33f-137">**CanResize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | <span data-ttu-id="db33f-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="db33f-138">Property</span></span>    | <span data-ttu-id="db33f-139">None</span><span class="sxs-lookup"><span data-stu-id="db33f-139">None</span></span>  |
| [<span data-ttu-id="db33f-140">**CanRotate**</span><span class="sxs-lookup"><span data-stu-id="db33f-140">**CanRotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | <span data-ttu-id="db33f-141">Propiedad</span><span class="sxs-lookup"><span data-stu-id="db33f-141">Property</span></span>    | <span data-ttu-id="db33f-142">None</span><span class="sxs-lookup"><span data-stu-id="db33f-142">None</span></span>  |
| [<span data-ttu-id="db33f-143">**Move**</span><span class="sxs-lookup"><span data-stu-id="db33f-143">**Move**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | <span data-ttu-id="db33f-144">Método</span><span class="sxs-lookup"><span data-stu-id="db33f-144">Method</span></span>      | <span data-ttu-id="db33f-145">None</span><span class="sxs-lookup"><span data-stu-id="db33f-145">None</span></span>  |
| [<span data-ttu-id="db33f-146">**Cambiar de tamaño**</span><span class="sxs-lookup"><span data-stu-id="db33f-146">**Resize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | <span data-ttu-id="db33f-147">Método</span><span class="sxs-lookup"><span data-stu-id="db33f-147">Method</span></span>      | <span data-ttu-id="db33f-148">None</span><span class="sxs-lookup"><span data-stu-id="db33f-148">None</span></span>  |
| [<span data-ttu-id="db33f-149">**Girar**</span><span class="sxs-lookup"><span data-stu-id="db33f-149">**Rotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | <span data-ttu-id="db33f-150">Método</span><span class="sxs-lookup"><span data-stu-id="db33f-150">Method</span></span>      | <span data-ttu-id="db33f-151">None</span><span class="sxs-lookup"><span data-stu-id="db33f-151">None</span></span>  |



 

<span data-ttu-id="db33f-152">Se requieren las siguientes propiedades y métodos adicionales para implementar la interfaz [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .</span><span class="sxs-lookup"><span data-stu-id="db33f-152">The following additional properties and methods are required for implementing the [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="db33f-153">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="db33f-153">Required members</span></span>                                              | <span data-ttu-id="db33f-154">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="db33f-154">Member type</span></span> | <span data-ttu-id="db33f-155">Notas</span><span class="sxs-lookup"><span data-stu-id="db33f-155">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="db33f-156">**CanZoom**</span><span class="sxs-lookup"><span data-stu-id="db33f-156">**CanZoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | <span data-ttu-id="db33f-157">Propiedad</span><span class="sxs-lookup"><span data-stu-id="db33f-157">Property</span></span>    | <span data-ttu-id="db33f-158">None</span><span class="sxs-lookup"><span data-stu-id="db33f-158">None</span></span>  |
| [<span data-ttu-id="db33f-159">**Zoom**</span><span class="sxs-lookup"><span data-stu-id="db33f-159">**Zoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | <span data-ttu-id="db33f-160">Método</span><span class="sxs-lookup"><span data-stu-id="db33f-160">Method</span></span>      | <span data-ttu-id="db33f-161">None</span><span class="sxs-lookup"><span data-stu-id="db33f-161">None</span></span>  |
| [<span data-ttu-id="db33f-162">**ZoomByUnit**</span><span class="sxs-lookup"><span data-stu-id="db33f-162">**ZoomByUnit**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | <span data-ttu-id="db33f-163">Método</span><span class="sxs-lookup"><span data-stu-id="db33f-163">Method</span></span>      | <span data-ttu-id="db33f-164">None</span><span class="sxs-lookup"><span data-stu-id="db33f-164">None</span></span>  |
| [<span data-ttu-id="db33f-165">**ZoomLevel (**</span><span class="sxs-lookup"><span data-stu-id="db33f-165">**ZoomLevel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | <span data-ttu-id="db33f-166">Propiedad</span><span class="sxs-lookup"><span data-stu-id="db33f-166">Property</span></span>    | <span data-ttu-id="db33f-167">None</span><span class="sxs-lookup"><span data-stu-id="db33f-167">None</span></span>  |
| [<span data-ttu-id="db33f-168">**ZoomMaximum**</span><span class="sxs-lookup"><span data-stu-id="db33f-168">**ZoomMaximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | <span data-ttu-id="db33f-169">Propiedad</span><span class="sxs-lookup"><span data-stu-id="db33f-169">Property</span></span>    | <span data-ttu-id="db33f-170">None</span><span class="sxs-lookup"><span data-stu-id="db33f-170">None</span></span>  |
| [<span data-ttu-id="db33f-171">**ZoomMinimum**</span><span class="sxs-lookup"><span data-stu-id="db33f-171">**ZoomMinimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | <span data-ttu-id="db33f-172">Propiedad</span><span class="sxs-lookup"><span data-stu-id="db33f-172">Property</span></span>    | <span data-ttu-id="db33f-173">None</span><span class="sxs-lookup"><span data-stu-id="db33f-173">None</span></span>  |



 

<span data-ttu-id="db33f-174">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="db33f-174">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db33f-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db33f-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db33f-176">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="db33f-176">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="db33f-177">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="db33f-177">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="db33f-178">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="db33f-178">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 