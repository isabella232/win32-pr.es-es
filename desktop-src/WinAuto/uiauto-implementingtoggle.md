---
title: Alternar patrón de control
description: Describe las directrices y convenciones para implementar IToggleProvider, incluida información sobre propiedades y métodos. El patrón de control Toggle se usa para admitir controles que pueden recorrer un conjunto de Estados y mantener un estado una vez establecido.
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Toggle
- Automatización de la interfaz de usuario, alternar patrón de control
- Automatización de la interfaz de usuario, IToggleProvider
- IToggleProvider
- implementar patrones de control de alternancia de la automatización de la interfaz de usuario
- Alternar patrones de control
- patrones de control, IToggleProvider
- patrones de control, alternancia de la automatización de la interfaz de usuario
- patrones de control, alternar
- interfaces, IToggleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418515"
---
# <a name="toggle-control-pattern"></a><span data-ttu-id="ae8ae-114">Alternar patrón de control</span><span class="sxs-lookup"><span data-stu-id="ae8ae-114">Toggle Control Pattern</span></span>

<span data-ttu-id="ae8ae-115">Describe las directrices y convenciones para implementar [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="ae8ae-115">Describes guidelines and conventions for implementing [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), including information about properties and methods.</span></span> <span data-ttu-id="ae8ae-116">El patrón de control **Toggle** se usa para admitir controles que pueden recorrer un conjunto de Estados y mantener un estado una vez establecido.</span><span class="sxs-lookup"><span data-stu-id="ae8ae-116">The **Toggle** control pattern is used to support controls that can cycle through a set of states and maintain a state once set.</span></span>

<span data-ttu-id="ae8ae-117">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="ae8ae-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="ae8ae-118">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="ae8ae-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ae8ae-119">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="ae8ae-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="ae8ae-120">Miembros requeridos para **IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="ae8ae-120">Required Members for **IToggleProvider**</span></span>](#required-members-for-itoggleprovider)
-   [<span data-ttu-id="ae8ae-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae8ae-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="ae8ae-122">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="ae8ae-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="ae8ae-123">Al implementar el patrón de control **Toggle** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="ae8ae-123">When implementing the **Toggle** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="ae8ae-124">Los controles que no mantienen el estado cuando se activan, como botones, botones de barra de herramientas e hipervínculos, deben implementar [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ae8ae-124">Controls that do not maintain state when activated, such as buttons, toolbar buttons, and hyperlinks, must implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) instead.</span></span>
-   <span data-ttu-id="ae8ae-125">Un control debe recorrer sus Estados de alternancia ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) en el siguiente orden: **ToggleState \_ on**, **ToggleState \_ OFF** y, si se admite, **ToggleState \_ indeterminada**.</span><span class="sxs-lookup"><span data-stu-id="ae8ae-125">A control must cycle through its toggle states ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) in the following order: **ToggleState\_On**, **ToggleState\_Off** and, if supported, **ToggleState\_Indeterminate**.</span></span>
-   <span data-ttu-id="ae8ae-126">La **alternancia** no proporciona un método de estado de conjunto debido a problemas relacionados con la configuración directa de una casilla de tres Estados sin recorrer la secuencia [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) adecuada.</span><span class="sxs-lookup"><span data-stu-id="ae8ae-126">**Toggle** does not provide a set-state method because of issues surrounding the direct setting of a three-state check box without cycling through its appropriate [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) sequence.</span></span>
-   <span data-ttu-id="ae8ae-127">El control de botón de radio no implementa [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), porque no es capaz de recorrer sus Estados válidos.</span><span class="sxs-lookup"><span data-stu-id="ae8ae-127">The radio button control does not implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), because it is not capable of cycling through its valid states.</span></span>

## <a name="required-members-for-itoggleprovider"></a><span data-ttu-id="ae8ae-128">Miembros requeridos para **IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="ae8ae-128">Required Members for **IToggleProvider**</span></span>

<span data-ttu-id="ae8ae-129">Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) .</span><span class="sxs-lookup"><span data-stu-id="ae8ae-129">The following properties and methods are required for implementing the [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) interface.</span></span>



| <span data-ttu-id="ae8ae-130">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="ae8ae-130">Required members</span></span>                                          | <span data-ttu-id="ae8ae-131">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="ae8ae-131">Member type</span></span> | <span data-ttu-id="ae8ae-132">Notas</span><span class="sxs-lookup"><span data-stu-id="ae8ae-132">Notes</span></span> |
|-----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="ae8ae-133">**Alternancia**</span><span class="sxs-lookup"><span data-stu-id="ae8ae-133">**Toggle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | <span data-ttu-id="ae8ae-134">Método</span><span class="sxs-lookup"><span data-stu-id="ae8ae-134">Method</span></span>      | <span data-ttu-id="ae8ae-135">None</span><span class="sxs-lookup"><span data-stu-id="ae8ae-135">None</span></span>  |
| [<span data-ttu-id="ae8ae-136">**ToggleState**</span><span class="sxs-lookup"><span data-stu-id="ae8ae-136">**ToggleState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | <span data-ttu-id="ae8ae-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ae8ae-137">Property</span></span>    | <span data-ttu-id="ae8ae-138">None</span><span class="sxs-lookup"><span data-stu-id="ae8ae-138">None</span></span>  |



 

<span data-ttu-id="ae8ae-139">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="ae8ae-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae8ae-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae8ae-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae8ae-141">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="ae8ae-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="ae8ae-142">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ae8ae-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="ae8ae-143">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="ae8ae-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




