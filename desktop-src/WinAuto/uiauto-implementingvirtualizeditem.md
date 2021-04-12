---
title: Patrón de control VirtualizedItem
description: Describe las directrices y convenciones para implementar IVirtualizedItemProvider, incluida información sobre propiedades y métodos.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control VirtualizedItem
- Automatización de la interfaz de usuario, patrón de control VirtualizedItem
- Automatización de la interfaz de usuario, IVirtualizedItemProvider
- IVirtualizedItemProvider
- implementación de patrones de control VirtualizedItem de UI Automation
- Patrones de control de VirtualizedItem
- patrones de control, IVirtualizedItemProvider
- patrones de control, implementar la automatización de la interfaz de usuario VirtualizedItem
- patrones de control, VirtualizedItem
- interfaces, IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269442"
---
# <a name="virtualizeditem-control-pattern"></a><span data-ttu-id="ec63c-113">Patrón de control VirtualizedItem</span><span class="sxs-lookup"><span data-stu-id="ec63c-113">VirtualizedItem Control Pattern</span></span>

<span data-ttu-id="ec63c-114">Describe las directrices y convenciones para implementar [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="ec63c-114">Describes guidelines and conventions for implementing [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), including information about properties and methods.</span></span> <span data-ttu-id="ec63c-115">El patrón de control **VirtualizedItem** se usa para admitir elementos virtualizados, que son elementos que se representan mediante elementos de automatización de marcadores de posición en el árbol de automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ec63c-115">The **VirtualizedItem** control pattern is used to support virtualized items, which are items that are represented by placeholder automation elements in the Microsoft UI Automation tree.</span></span>

<span data-ttu-id="ec63c-116">Los elementos virtualizados pueden incluir elementos recuperados de un control que admite el patrón de control [ItemContainer](uiauto-implementingitemcontainer.md) o un objeto incrustado virtualizado recuperado de un control que admite el patrón de control [Text](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="ec63c-116">Virtualized items can include items retrieved from a control that supports the [ItemContainer](uiauto-implementingitemcontainer.md) control pattern, or a virtualized embedded object retrieved from a control that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span> <span data-ttu-id="ec63c-117">El marcador de posición de un elemento virtualizado podría no tener datos cargados para todas las propiedades de automatización de la interfaz de usuario y puede devolver [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) en respuesta a las consultas de propiedades que no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="ec63c-117">The placeholder for a virtualized item might not have loaded data for all UI Automation properties, and may return [**UIA\_E\_ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) in response to queries for properties that are not available.</span></span> <span data-ttu-id="ec63c-118">El patrón de control **VirtualizedItem** proporciona un método para obtener un elemento virtual de forma que haya información completa disponible para el elemento, y se puede crear un elemento de automatización completo para el elemento en el árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ec63c-118">The **VirtualizedItem** control pattern provides a method for realizing a virtual item so that full information is made available for the item, and a full automation element can be created for the item in the UI Automation tree.</span></span>

<span data-ttu-id="ec63c-119">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="ec63c-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ec63c-120">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="ec63c-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="ec63c-121">Miembros requeridos para **IVirtualizedItemProvider**</span><span class="sxs-lookup"><span data-stu-id="ec63c-121">Required Members for **IVirtualizedItemProvider**</span></span>](#required-members-for-ivirtualizeditemprovider)
-   [<span data-ttu-id="ec63c-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec63c-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="ec63c-123">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="ec63c-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="ec63c-124">Al implementar el patrón de control **VirtualizedItem** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="ec63c-124">When implementing the **VirtualizedItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="ec63c-125">Cualquier elemento de marcador de posición de automatización de la interfaz de usuario que se pueda virtualizar debe admitir el patrón de control **VirtualizedItem** al exponer la interfaz [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .</span><span class="sxs-lookup"><span data-stu-id="ec63c-125">Any UI Automation placeholder element that can be virtualized must support the **VirtualizedItem** control pattern by exposing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>
-   <span data-ttu-id="ec63c-126">Cuando se llama a [**IVirtualizedItemProvider::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) , el objeto de marcador de posición debe actualizarse con implementaciones completas de sus propiedades y patrones de control.</span><span class="sxs-lookup"><span data-stu-id="ec63c-126">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the placeholder object must be updated with full implementations of its properties and control patterns.</span></span>
-   <span data-ttu-id="ec63c-127">Cuando se llama a [**IVirtualizedItemProvider::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) acview, el proveedor puede cambiar la ventanilla para que el elemento virtualizado se vea en la vista.</span><span class="sxs-lookup"><span data-stu-id="ec63c-127">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the provider can change the viewport so that the virtualized item comes into view.</span></span> <span data-ttu-id="ec63c-128">No es necesario poner el elemento en la vista; sin embargo, los elementos no virtualizados y fuera de la pantalla deben admitir el método [**IScrollItemProvider:: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) .</span><span class="sxs-lookup"><span data-stu-id="ec63c-128">Bringing the item into view is not required; however, off-screen, non-virtualized items should support the [**IScrollItemProvider::ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) method.</span></span>

## <a name="required-members-for-ivirtualizeditemprovider"></a><span data-ttu-id="ec63c-129">Miembros requeridos para **IVirtualizedItemProvider**</span><span class="sxs-lookup"><span data-stu-id="ec63c-129">Required Members for **IVirtualizedItemProvider**</span></span>

<span data-ttu-id="ec63c-130">Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .</span><span class="sxs-lookup"><span data-stu-id="ec63c-130">The following properties and methods are required for implementing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>



| <span data-ttu-id="ec63c-131">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="ec63c-131">Required members</span></span>                                           | <span data-ttu-id="ec63c-132">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="ec63c-132">Member type</span></span> | <span data-ttu-id="ec63c-133">Notas</span><span class="sxs-lookup"><span data-stu-id="ec63c-133">Notes</span></span> |
|------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="ec63c-134">**Alcanzar**</span><span class="sxs-lookup"><span data-stu-id="ec63c-134">**Realize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | <span data-ttu-id="ec63c-135">Método</span><span class="sxs-lookup"><span data-stu-id="ec63c-135">Method</span></span>      | <span data-ttu-id="ec63c-136">None</span><span class="sxs-lookup"><span data-stu-id="ec63c-136">None</span></span>  |



 

<span data-ttu-id="ec63c-137">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="ec63c-137">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec63c-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec63c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec63c-139">Implementar el patrón de control ItemContainer de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ec63c-139">Implementing the UI Automation ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
</dt> <dt>

[<span data-ttu-id="ec63c-140">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ec63c-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="ec63c-141">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="ec63c-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="ec63c-142">Trabajar con elementos virtualizados</span><span class="sxs-lookup"><span data-stu-id="ec63c-142">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




