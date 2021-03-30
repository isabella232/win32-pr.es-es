---
title: Patrón de control TableItem
description: Describe las directrices y convenciones para implementar ITableItemProvider, incluida información sobre los métodos. El patrón de control TableItem se usa para admitir controles secundarios de contenedores que implementan ITableProvider.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control TableItem
- Automatización de la interfaz de usuario, patrón de control TableItem
- Automatización de la interfaz de usuario, ITableItemProvider
- ITableItemProvider
- implementación de patrones de control TableItem de UI Automation
- Patrones de control de TableItem
- patrones de control, ITableItemProvider
- patrones de control, implementar la automatización de la interfaz de usuario TableItem
- patrones de control, TableItem
- interfaces, ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bae3e6d5379ec9a662e31ec6181476b112631381
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774814"
---
# <a name="tableitem-control-pattern"></a><span data-ttu-id="f8c38-114">Patrón de control TableItem</span><span class="sxs-lookup"><span data-stu-id="f8c38-114">TableItem Control Pattern</span></span>

<span data-ttu-id="f8c38-115">Describe las directrices y convenciones para implementar [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), incluida información sobre los métodos.</span><span class="sxs-lookup"><span data-stu-id="f8c38-115">Describes guidelines and conventions for implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), including information about methods.</span></span> <span data-ttu-id="f8c38-116">El patrón de control **TableItem** se usa para admitir controles secundarios de contenedores que implementan [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).</span><span class="sxs-lookup"><span data-stu-id="f8c38-116">The **TableItem** control pattern is used to support child controls of containers that implement [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).</span></span>

<span data-ttu-id="f8c38-117">El acceso a la funcionalidad de celda individual se proporciona mediante la implementación simultánea necesaria de [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider).</span><span class="sxs-lookup"><span data-stu-id="f8c38-117">Access to individual cell functionality is provided by the required, concurrent implementation of [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider).</span></span> <span data-ttu-id="f8c38-118">Este patrón de control es análogo a **IGridItemProvider** , con la diferencia de que cualquier control que implemente [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) debe exponer mediante programación la relación entre la celda individual y su información de fila y columna.</span><span class="sxs-lookup"><span data-stu-id="f8c38-118">This control pattern is analogous to **IGridItemProvider** with the distinction that any control implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) must programmatically expose the relationship between the individual cell and its row and column information.</span></span> <span data-ttu-id="f8c38-119">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="f8c38-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="f8c38-120">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="f8c38-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f8c38-121">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="f8c38-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="f8c38-122">Miembros requeridos para **ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="f8c38-122">Required Members for **ITableItemProvider**</span></span>](#required-members-for-itableitemprovider)
-   [<span data-ttu-id="f8c38-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8c38-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="f8c38-124">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="f8c38-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="f8c38-125">Al implementar el patrón de control **TableItem** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="f8c38-125">When implementing the **TableItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="f8c38-126">Para obtener la funcionalidad de elemento de cuadrícula relacionada, vea el [patrón de control GridItem](uiauto-implementinggriditem.md).</span><span class="sxs-lookup"><span data-stu-id="f8c38-126">For related grid item functionality, see [GridItem Control Pattern](uiauto-implementinggriditem.md).</span></span>

## <a name="required-members-for-itableitemprovider"></a><span data-ttu-id="f8c38-127">Miembros requeridos para **ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="f8c38-127">Required Members for **ITableItemProvider**</span></span>

<span data-ttu-id="f8c38-128">Los métodos siguientes son necesarios para implementar la interfaz [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="f8c38-128">The following methods are required for implementing the [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) interface.</span></span>



| <span data-ttu-id="f8c38-129">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="f8c38-129">Required members</span></span>                                                               | <span data-ttu-id="f8c38-130">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="f8c38-130">Member type</span></span> | <span data-ttu-id="f8c38-131">Notas</span><span class="sxs-lookup"><span data-stu-id="f8c38-131">Notes</span></span> |
|--------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="f8c38-132">**GetColumnHeaderItems**</span><span class="sxs-lookup"><span data-stu-id="f8c38-132">**GetColumnHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | <span data-ttu-id="f8c38-133">Método</span><span class="sxs-lookup"><span data-stu-id="f8c38-133">Method</span></span>      | <span data-ttu-id="f8c38-134">None</span><span class="sxs-lookup"><span data-stu-id="f8c38-134">None</span></span>  |
| [<span data-ttu-id="f8c38-135">**GetRowHeaderItems**</span><span class="sxs-lookup"><span data-stu-id="f8c38-135">**GetRowHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | <span data-ttu-id="f8c38-136">Método</span><span class="sxs-lookup"><span data-stu-id="f8c38-136">Method</span></span>      | <span data-ttu-id="f8c38-137">None</span><span class="sxs-lookup"><span data-stu-id="f8c38-137">None</span></span>  |



 

<span data-ttu-id="f8c38-138">Este patrón de control no tiene eventos o propiedades asociados.</span><span class="sxs-lookup"><span data-stu-id="f8c38-138">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8c38-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8c38-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f8c38-140">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f8c38-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f8c38-141">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="f8c38-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="f8c38-142">Table (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="f8c38-142">Table Control Pattern</span></span>](uiauto-implementingtable.md)
</dt> <dt>

[<span data-ttu-id="f8c38-143">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="f8c38-143">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="f8c38-144">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="f8c38-144">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




