---
title: Patrón de control ScrollItem
description: Describe las directrices y convenciones para implementar IScrollItemProvider, incluida información sobre los métodos.
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control ScrollItem
- Automatización de la interfaz de usuario, patrón de control ScrollItem
- Automatización de la interfaz de usuario, IScrollItemProvider
- IScrollItemProvider
- implementación de patrones de control ScrollItem de UI Automation
- Patrones de control de ScrollItem
- patrones de control, IScrollItemProvider
- patrones de control, implementar la automatización de la interfaz de usuario ScrollItem
- patrones de control, ScrollItem
- interfaces, IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7233dfe649d166a3172ff2dda3122895f259abcc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268913"
---
# <a name="scrollitem-control-pattern"></a><span data-ttu-id="1a2d3-113">Patrón de control ScrollItem</span><span class="sxs-lookup"><span data-stu-id="1a2d3-113">ScrollItem Control Pattern</span></span>

<span data-ttu-id="1a2d3-114">Describe las directrices y convenciones para implementar [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), incluida información sobre los métodos.</span><span class="sxs-lookup"><span data-stu-id="1a2d3-114">Describes guidelines and conventions for implementing [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), including information about methods.</span></span> <span data-ttu-id="1a2d3-115">El patrón de control **ScrollItem** se usa para admitir controles secundarios individuales de contenedores que implementan [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider).</span><span class="sxs-lookup"><span data-stu-id="1a2d3-115">The **ScrollItem** control pattern is used to support individual child controls of containers that implement [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider).</span></span> <span data-ttu-id="1a2d3-116">La existencia del patrón de control **ScrollItem** en un control no implica que su contenedor o cualquier antecesor debe implementar el patrón de control **Scroll** .</span><span class="sxs-lookup"><span data-stu-id="1a2d3-116">The existence of the **ScrollItem** control pattern on a control does not imply that its container or any ancestor must implement the **Scroll** control pattern.</span></span>

<span data-ttu-id="1a2d3-117">Cuando el contenedor implementa el patrón de control **Scroll** , el patrón de control **ScrollItem** actúa como un canal de comunicación entre un control secundario y su contenedor para asegurarse de que el contenedor puede cambiar el contenido (o región) actualmente visible dentro de su ventanilla para mostrar el control secundario.</span><span class="sxs-lookup"><span data-stu-id="1a2d3-117">When the container does implement the **Scroll** control pattern, the **ScrollItem** control pattern acts as a communication channel between a child control and its container to ensure that the container can change the currently visible content (or region) within its viewport to display the child control.</span></span> <span data-ttu-id="1a2d3-118">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="1a2d3-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="1a2d3-119">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="1a2d3-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1a2d3-120">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="1a2d3-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="1a2d3-121">Miembros requeridos para **IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="1a2d3-121">Required Members for **IScrollItemProvider**</span></span>](#required-members-for-iscrollitemprovider)
-   [<span data-ttu-id="1a2d3-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1a2d3-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="1a2d3-123">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="1a2d3-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="1a2d3-124">Al implementar el patrón de control **ScrollItem** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="1a2d3-124">When implementing the **ScrollItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="1a2d3-125">No es necesario que los elementos contenidos en un control [Window](uiauto-supportwindowcontroltype.md) o **Canvas** implementen la interfaz [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="1a2d3-125">Items contained within a [Window](uiauto-supportwindowcontroltype.md) or **Canvas** control are not required to implement the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span> <span data-ttu-id="1a2d3-126">Sin embargo, como alternativa, deben exponer una ubicación válida para la propiedad [**IUIAutomationElement:: CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (o [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)).</span><span class="sxs-lookup"><span data-stu-id="1a2d3-126">As an alternative, however, they must expose a valid location for the [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (or [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)) property.</span></span> <span data-ttu-id="1a2d3-127">Esto permitirá que una aplicación cliente de automatización de la interfaz de usuario de Microsoft use los métodos de patrón de control [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) en el contenedor para mostrar el elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="1a2d3-127">This will allow a Microsoft UI Automation client application to use the [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) control pattern methods on the container to display the child item.</span></span>

## <a name="required-members-for-iscrollitemprovider"></a><span data-ttu-id="1a2d3-128">Miembros requeridos para **IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="1a2d3-128">Required Members for **IScrollItemProvider**</span></span>

<span data-ttu-id="1a2d3-129">El método siguiente es necesario para implementar la interfaz [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="1a2d3-129">The following method is required for implementing the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span>



| <span data-ttu-id="1a2d3-130">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="1a2d3-130">Required members</span></span>                                                    | <span data-ttu-id="1a2d3-131">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="1a2d3-131">Member type</span></span> | <span data-ttu-id="1a2d3-132">Notas</span><span class="sxs-lookup"><span data-stu-id="1a2d3-132">Notes</span></span> |
|---------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="1a2d3-133">**ScrollIntoView**</span><span class="sxs-lookup"><span data-stu-id="1a2d3-133">**ScrollIntoView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | <span data-ttu-id="1a2d3-134">Método</span><span class="sxs-lookup"><span data-stu-id="1a2d3-134">Method</span></span>      | <span data-ttu-id="1a2d3-135">None</span><span class="sxs-lookup"><span data-stu-id="1a2d3-135">None</span></span>  |



 

<span data-ttu-id="1a2d3-136">Este patrón de control no tiene eventos o propiedades asociados.</span><span class="sxs-lookup"><span data-stu-id="1a2d3-136">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a2d3-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1a2d3-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a2d3-138">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="1a2d3-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="1a2d3-139">Selection (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="1a2d3-139">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
</dt> <dt>

[<span data-ttu-id="1a2d3-140">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="1a2d3-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="1a2d3-141">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="1a2d3-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




