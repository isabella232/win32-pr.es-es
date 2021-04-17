---
title: Patrón de control RangeValue
description: Describe las directrices y convenciones para implementar IRangeValueProvider, incluida información sobre propiedades y métodos. El patrón de control RangeValue se usa para admitir controles que se pueden establecer en un valor dentro de un intervalo.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control RangeValue
- Automatización de la interfaz de usuario, patrón de control RangeValue
- Automatización de la interfaz de usuario, IRangeValueProvider
- IRangeValueProvider
- implementación de patrones de control RangeValue de UI Automation
- Patrones de control de RangeValue
- patrones de control, IRangeValueProvider
- patrones de control, implementar la automatización de la interfaz de usuario RangeValue
- patrones de control, RangeValue
- interfaces, IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf426069ad88ad272fd78c521a220ba7ccf72275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704699"
---
# <a name="rangevalue-control-pattern"></a><span data-ttu-id="66d38-114">Patrón de control RangeValue</span><span class="sxs-lookup"><span data-stu-id="66d38-114">RangeValue Control Pattern</span></span>

<span data-ttu-id="66d38-115">Describe las directrices y convenciones para implementar [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="66d38-115">Describes guidelines and conventions for implementing [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="66d38-116">El patrón de control **RangeValue** se usa para admitir controles que se pueden establecer en un valor dentro de un intervalo.</span><span class="sxs-lookup"><span data-stu-id="66d38-116">The **RangeValue** control pattern is used to support controls that can be set to a value within a range.</span></span>

<span data-ttu-id="66d38-117">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="66d38-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="66d38-118">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="66d38-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="66d38-119">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="66d38-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="66d38-120">Miembros requeridos para **IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="66d38-120">Required Members for **IRangeValueProvider**</span></span>](#required-members-for-irangevalueprovider)
-   [<span data-ttu-id="66d38-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66d38-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="66d38-122">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="66d38-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="66d38-123">Al implementar el patrón de control **RangeValue** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="66d38-123">When implementing the **RangeValue** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="66d38-124">Los controles permiten la recalibración de sus propiedades compatibles según las preferencias de usuario o la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="66d38-124">Controls allow recalibration of their supported properties based upon locale or user preference.</span></span> <span data-ttu-id="66d38-125">Un ejemplo de esto es un control de termómetro que puede establecerse para mostrar la temperatura en grados Fahrenheit o Celsius.</span><span class="sxs-lookup"><span data-stu-id="66d38-125">An example of this is a thermometer control that can be set to display the temperature in Fahrenheit or Celsius.</span></span>
-   <span data-ttu-id="66d38-126">Los controles que tienen valores de intervalo ambiguos, como las barras de progreso o los controles deslizantes, deben tener dichos valores normalizados.</span><span class="sxs-lookup"><span data-stu-id="66d38-126">Controls that have ambiguous range values, such as progress bars or sliders, should have those values normalized.</span></span>

## <a name="required-members-for-irangevalueprovider"></a><span data-ttu-id="66d38-127">Miembros requeridos para **IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="66d38-127">Required Members for **IRangeValueProvider**</span></span>

<span data-ttu-id="66d38-128">Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) .</span><span class="sxs-lookup"><span data-stu-id="66d38-128">The following properties and methods are required for implementing the [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface.</span></span>



| <span data-ttu-id="66d38-129">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="66d38-129">Required members</span></span>                                              | <span data-ttu-id="66d38-130">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="66d38-130">Member type</span></span> | <span data-ttu-id="66d38-131">Notas</span><span class="sxs-lookup"><span data-stu-id="66d38-131">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="66d38-132">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="66d38-132">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | <span data-ttu-id="66d38-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66d38-133">Property</span></span>    | <span data-ttu-id="66d38-134">None</span><span class="sxs-lookup"><span data-stu-id="66d38-134">None</span></span>  |
| [<span data-ttu-id="66d38-135">**Valor**</span><span class="sxs-lookup"><span data-stu-id="66d38-135">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | <span data-ttu-id="66d38-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66d38-136">Property</span></span>    | <span data-ttu-id="66d38-137">None</span><span class="sxs-lookup"><span data-stu-id="66d38-137">None</span></span>  |
| [<span data-ttu-id="66d38-138">**LargeChange**</span><span class="sxs-lookup"><span data-stu-id="66d38-138">**LargeChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | <span data-ttu-id="66d38-139">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66d38-139">Property</span></span>    | <span data-ttu-id="66d38-140">None</span><span class="sxs-lookup"><span data-stu-id="66d38-140">None</span></span>  |
| [<span data-ttu-id="66d38-141">**SmallChange**</span><span class="sxs-lookup"><span data-stu-id="66d38-141">**SmallChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | <span data-ttu-id="66d38-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66d38-142">Property</span></span>    | <span data-ttu-id="66d38-143">None</span><span class="sxs-lookup"><span data-stu-id="66d38-143">None</span></span>  |
| [<span data-ttu-id="66d38-144">**Máxima**</span><span class="sxs-lookup"><span data-stu-id="66d38-144">**Maximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | <span data-ttu-id="66d38-145">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66d38-145">Property</span></span>    | <span data-ttu-id="66d38-146">None</span><span class="sxs-lookup"><span data-stu-id="66d38-146">None</span></span>  |
| [<span data-ttu-id="66d38-147">**Mínima**</span><span class="sxs-lookup"><span data-stu-id="66d38-147">**Minimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | <span data-ttu-id="66d38-148">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66d38-148">Property</span></span>    | <span data-ttu-id="66d38-149">None</span><span class="sxs-lookup"><span data-stu-id="66d38-149">None</span></span>  |
| [<span data-ttu-id="66d38-150">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="66d38-150">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | <span data-ttu-id="66d38-151">Método</span><span class="sxs-lookup"><span data-stu-id="66d38-151">Method</span></span>      | <span data-ttu-id="66d38-152">None</span><span class="sxs-lookup"><span data-stu-id="66d38-152">None</span></span>  |



 

<span data-ttu-id="66d38-153">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="66d38-153">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66d38-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66d38-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66d38-155">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="66d38-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="66d38-156">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="66d38-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="66d38-157">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="66d38-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




