---
title: Scroll (patrón de control)
description: Describe las directrices y convenciones para implementar IScrollProvider, incluida información sobre propiedades y métodos. El patrón de control scroll se usa para admitir un control que actúa como contenedor desplazable para una colección de objetos secundarios.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control scroll
- Automatización de la interfaz de usuario, patrón de control scroll
- Automatización de la interfaz de usuario, IScrollProvider
- IScrollProvider
- implementar patrones de control scroll de UI Automation
- Patrones de control scroll
- patrones de control, IScrollProvider
- patrones de control, implementar la automatización de la interfaz de usuario
- patrones de control, desplazarse
- interfaces, IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c77a7f89f7adc95a3d90d999f8b243cfcdb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777707"
---
# <a name="scroll-control-pattern"></a><span data-ttu-id="5a8a3-114">Scroll (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="5a8a3-114">Scroll Control Pattern</span></span>

<span data-ttu-id="5a8a3-115">Describe las directrices y convenciones para implementar [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="5a8a3-115">Describes guidelines and conventions for implementing [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), including information about properties and methods.</span></span> <span data-ttu-id="5a8a3-116">El patrón de control **Scroll** se usa para admitir un control que actúa como contenedor desplazable para una colección de objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="5a8a3-116">The **Scroll** control pattern is used to support a control that acts as a scrollable container for a collection of child objects.</span></span>

<span data-ttu-id="5a8a3-117">No es necesario que el control use barras de desplazamiento para admitir la funcionalidad de desplazamiento, aunque normalmente lo hace.</span><span class="sxs-lookup"><span data-stu-id="5a8a3-117">The control is not required to use scroll bars to support the scrolling functionality, although it commonly does.</span></span> <span data-ttu-id="5a8a3-118">En la imagen siguiente se muestra un control de desplazamiento que no utiliza barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="5a8a3-118">The following image shows a scrolling control that does not use scroll bars.</span></span> <span data-ttu-id="5a8a3-119">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="5a8a3-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![captura de pantalla que muestra un control de desplazamiento sin barras de desplazamiento](images/uia-scrollpattern-without-scrollbars.jpg)

<span data-ttu-id="5a8a3-121">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="5a8a3-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5a8a3-122">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="5a8a3-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="5a8a3-123">Miembros requeridos para **IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="5a8a3-123">Required Members for **IScrollProvider**</span></span>](#required-members-for-iscrollprovider)
-   [<span data-ttu-id="5a8a3-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a8a3-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="5a8a3-125">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="5a8a3-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="5a8a3-126">Al implementar el patrón de control **Scroll** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="5a8a3-126">When implementing the **Scroll** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="5a8a3-127">Los elementos secundarios de este control deben implementar [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).</span><span class="sxs-lookup"><span data-stu-id="5a8a3-127">The children of this control must implement [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).</span></span>
-   <span data-ttu-id="5a8a3-128">Las barras de desplazamiento de un control contenedor no admiten el patrón de control **Scroll** .</span><span class="sxs-lookup"><span data-stu-id="5a8a3-128">The scroll bars of a container control do not support the **Scroll** control pattern.</span></span> <span data-ttu-id="5a8a3-129">En su lugar, deben admitir el patrón de control [RangeValue](uiauto-implementingrangevalue.md) .</span><span class="sxs-lookup"><span data-stu-id="5a8a3-129">They must support the [RangeValue](uiauto-implementingrangevalue.md) control pattern instead.</span></span>
-   <span data-ttu-id="5a8a3-130">Cuando el desplazamiento se mide en porcentajes, todos los valores o cantidades relacionadas con la graduación del desplazamiento deben normalizarse a un intervalo de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="5a8a3-130">When scrolling is measured in percentages, all values or amounts related to scroll graduation must be normalized to a range of 0 to 100.</span></span>
-   <span data-ttu-id="5a8a3-131">La propiedad [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) y la propiedad [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) son independientes de la propiedad **IsEnabled** .</span><span class="sxs-lookup"><span data-stu-id="5a8a3-131">The [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) property and [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) property are independent of the **IsEnabled** property.</span></span>
-   <span data-ttu-id="5a8a3-132">Si la propiedad [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) es **false**, la propiedad [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) debe establecerse en 100 (100%) y la propiedad [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) debe establecerse en **UIA \_ ScrollPatternNoScroll** (-1).</span><span class="sxs-lookup"><span data-stu-id="5a8a3-132">If the [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) property is **FALSE**, the [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) property should be set to 100 (100%) and [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) property should be set to **UIA\_ScrollPatternNoScroll** (-1).</span></span> <span data-ttu-id="5a8a3-133">Del mismo modo, si la propiedad [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) es **false**, la propiedad [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) debe establecerse en 100 (100%). y la propiedad [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) debe establecerse en **UIA \_ ScrollPatternNoScroll** (-1).</span><span class="sxs-lookup"><span data-stu-id="5a8a3-133">Likewise, if the [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) property is **FALSE**, the [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) property should be set to 100 (100%) and [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) property should be set to **UIA\_ScrollPatternNoScroll** (-1).</span></span> <span data-ttu-id="5a8a3-134">Esto permite que un cliente de automatización de la interfaz de usuario de Microsoft use estos valores de propiedad dentro del método [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) al tiempo que se evita una condición de carrera si se activa una dirección a la que el cliente no está interesado en el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="5a8a3-134">This allows a Microsoft UI Automation client to use these property values within the [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) method while avoiding a race condition if a direction the client is not interested in scrolling becomes activated.</span></span>
-   <span data-ttu-id="5a8a3-135">La propiedad [**IScrollProvider:: HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) es específica de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="5a8a3-135">The [**IScrollProvider::HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) property is locale-specific.</span></span> <span data-ttu-id="5a8a3-136">Establecer **HorizontalScrollPercent** en 100 debe establecer la ubicación de desplazamiento del control en el equivalente de su posición más a la derecha para idiomas como el inglés que se leen de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="5a8a3-136">Setting **HorizontalScrollPercent** to 100 must set the scrolling location of the control to the equivalent of its rightmost position for languages such as English that read left to right.</span></span> <span data-ttu-id="5a8a3-137">Como alternativa, para idiomas como el árabe que se leen de derecha a izquierda, el establecimiento de **HorizontalScrollPercent** en 100 debe establecer la ubicación de desplazamiento en la posición más a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="5a8a3-137">Alternately, for languages such as Arabic that read right to left, setting **HorizontalScrollPercent** to 100 must set the scroll location to the leftmost position.</span></span>

## <a name="required-members-for-iscrollprovider"></a><span data-ttu-id="5a8a3-138">Miembros requeridos para **IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="5a8a3-138">Required Members for **IScrollProvider**</span></span>

<span data-ttu-id="5a8a3-139">Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) .</span><span class="sxs-lookup"><span data-stu-id="5a8a3-139">The following properties and methods are required for implementing the [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) interface.</span></span>



| <span data-ttu-id="5a8a3-140">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="5a8a3-140">Required members</span></span>                                                                  | <span data-ttu-id="5a8a3-141">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="5a8a3-141">Member type</span></span> | <span data-ttu-id="5a8a3-142">Notas</span><span class="sxs-lookup"><span data-stu-id="5a8a3-142">Notes</span></span> |
|-----------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="5a8a3-143">**HorizontalScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="5a8a3-143">**HorizontalScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | <span data-ttu-id="5a8a3-144">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5a8a3-144">Property</span></span>    | <span data-ttu-id="5a8a3-145">None</span><span class="sxs-lookup"><span data-stu-id="5a8a3-145">None</span></span>  |
| [<span data-ttu-id="5a8a3-146">**VerticalScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="5a8a3-146">**VerticalScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | <span data-ttu-id="5a8a3-147">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5a8a3-147">Property</span></span>    | <span data-ttu-id="5a8a3-148">None</span><span class="sxs-lookup"><span data-stu-id="5a8a3-148">None</span></span>  |
| [<span data-ttu-id="5a8a3-149">**HorizontalViewSize**</span><span class="sxs-lookup"><span data-stu-id="5a8a3-149">**HorizontalViewSize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | <span data-ttu-id="5a8a3-150">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5a8a3-150">Property</span></span>    | <span data-ttu-id="5a8a3-151">None</span><span class="sxs-lookup"><span data-stu-id="5a8a3-151">None</span></span>  |
| [<span data-ttu-id="5a8a3-152">**VerticalViewSize**</span><span class="sxs-lookup"><span data-stu-id="5a8a3-152">**VerticalViewSize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | <span data-ttu-id="5a8a3-153">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5a8a3-153">Property</span></span>    | <span data-ttu-id="5a8a3-154">None</span><span class="sxs-lookup"><span data-stu-id="5a8a3-154">None</span></span>  |
| [<span data-ttu-id="5a8a3-155">**HorizontallyScrollable**</span><span class="sxs-lookup"><span data-stu-id="5a8a3-155">**HorizontallyScrollable**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | <span data-ttu-id="5a8a3-156">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5a8a3-156">Property</span></span>    | <span data-ttu-id="5a8a3-157">None</span><span class="sxs-lookup"><span data-stu-id="5a8a3-157">None</span></span>  |
| [<span data-ttu-id="5a8a3-158">**VerticallyScrollable**</span><span class="sxs-lookup"><span data-stu-id="5a8a3-158">**VerticallyScrollable**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | <span data-ttu-id="5a8a3-159">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5a8a3-159">Property</span></span>    | <span data-ttu-id="5a8a3-160">None</span><span class="sxs-lookup"><span data-stu-id="5a8a3-160">None</span></span>  |
| [<span data-ttu-id="5a8a3-161">**Scroll**</span><span class="sxs-lookup"><span data-stu-id="5a8a3-161">**Scroll**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | <span data-ttu-id="5a8a3-162">Método</span><span class="sxs-lookup"><span data-stu-id="5a8a3-162">Method</span></span>      | <span data-ttu-id="5a8a3-163">None</span><span class="sxs-lookup"><span data-stu-id="5a8a3-163">None</span></span>  |
| [<span data-ttu-id="5a8a3-164">**SetScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="5a8a3-164">**SetScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | <span data-ttu-id="5a8a3-165">Método</span><span class="sxs-lookup"><span data-stu-id="5a8a3-165">Method</span></span>      | <span data-ttu-id="5a8a3-166">None</span><span class="sxs-lookup"><span data-stu-id="5a8a3-166">None</span></span>  |



 

<span data-ttu-id="5a8a3-167">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="5a8a3-167">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a8a3-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a8a3-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a8a3-169">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="5a8a3-169">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="5a8a3-170">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="5a8a3-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="5a8a3-171">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="5a8a3-171">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




