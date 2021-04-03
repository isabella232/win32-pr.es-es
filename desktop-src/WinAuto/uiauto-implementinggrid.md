---
title: Grid (patrón de control)
description: Describe las directrices y convenciones para implementar IGridProvider, incluida información sobre propiedades y métodos. El patrón de control Grid se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Grid
- Automatización de la interfaz de usuario, patrón de control Grid
- Automatización de la interfaz de usuario, IGridProvider
- IGridProvider
- implementar patrones de control de cuadrícula de UI Automation
- Patrones de control de cuadrícula
- patrones de control, IGridProvider
- patrones de control, implementar cuadrícula de UI Automation
- patrones de control, cuadrícula
- interfaces, IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075485"
---
# <a name="grid-control-pattern"></a><span data-ttu-id="ebf13-114">Grid (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="ebf13-114">Grid Control Pattern</span></span>

<span data-ttu-id="ebf13-115">Describe las directrices y convenciones para implementar [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="ebf13-115">Describes guidelines and conventions for implementing [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), including information about properties and methods.</span></span> <span data-ttu-id="ebf13-116">El patrón de control **Grid** se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="ebf13-116">The **Grid** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="ebf13-117">Los elementos secundarios de este elemento deben implementar [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) y organizarse en un sistema de coordenadas lógico bidimensional que se pueda atravesar por fila y columna.</span><span class="sxs-lookup"><span data-stu-id="ebf13-117">The children of this element must implement [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="ebf13-118">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="ebf13-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="ebf13-119">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="ebf13-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ebf13-120">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="ebf13-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="ebf13-121">Miembros requeridos para **IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="ebf13-121">Required Members for **IGridProvider**</span></span>](#required-members-for-igridprovider)
-   [<span data-ttu-id="ebf13-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebf13-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="ebf13-123">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="ebf13-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="ebf13-124">Al implementar el patrón de control **Grid** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="ebf13-124">When implementing the **Grid** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="ebf13-125">Las coordenadas de la cuadrícula son de base cero con la parte superior izquierda (o la celda superior derecha, según la configuración regional), con las coordenadas (0,0).</span><span class="sxs-lookup"><span data-stu-id="ebf13-125">Grid coordinates are zero-based with the upper left (or upper right cell depending on locale) having coordinates (0,0).</span></span>
-   <span data-ttu-id="ebf13-126">Si una celda está vacía, todavía debe devolverse un elemento de automatización de la interfaz de usuario de Microsoft para admitir la propiedad [**IGridItemProvider:: ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) para esa celda.</span><span class="sxs-lookup"><span data-stu-id="ebf13-126">If a cell is empty, a Microsoft UI Automation element must still be returned in order to support the [**IGridItemProvider::ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) property for that cell.</span></span> <span data-ttu-id="ebf13-127">Esto es posible si el diseño de elementos secundarios de la cuadrícula es similar a una matriz irregular (consulte el ejemplo siguiente).</span><span class="sxs-lookup"><span data-stu-id="ebf13-127">This is possible when the layout of child elements in the grid is similar to a ragged array (see example below).</span></span>

    ![ejemplo de un control Grid con coordenadas vacías](images/grid.png)

-   <span data-ttu-id="ebf13-129">Todavía se requiere una cuadrícula con un elemento único para implementar [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) si se considera una cuadrícula lógicamente.</span><span class="sxs-lookup"><span data-stu-id="ebf13-129">A grid with a single item is still required to implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) if it is logically considered to be a grid.</span></span> <span data-ttu-id="ebf13-130">El número de elementos secundarios de la cuadrícula es irrelevante.</span><span class="sxs-lookup"><span data-stu-id="ebf13-130">The number of child items in the grid is immaterial.</span></span>
-   <span data-ttu-id="ebf13-131">Las filas y columnas ocultas, según la implementación del proveedor, se pueden cargar en el árbol de automatización de la interfaz de usuario y, por tanto, se reflejarán en las propiedades [**IGridProvider:: RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) y [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) .</span><span class="sxs-lookup"><span data-stu-id="ebf13-131">Hidden rows and columns, depending on the provider implementation, may be loaded in the UI Automation tree and will therefore be reflected in the [**IGridProvider::RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) and [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) properties.</span></span> <span data-ttu-id="ebf13-132">Si las filas y columnas ocultas todavía no se han cargado, no deben contarse.</span><span class="sxs-lookup"><span data-stu-id="ebf13-132">If the hidden rows and columns have not yet been loaded, they should not be counted.</span></span>
-   <span data-ttu-id="ebf13-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) no habilita la manipulación activa de una cuadrícula; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) debe implementarse para habilitar esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="ebf13-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not enable active manipulation of a grid; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) must be implemented to enable this functionality.</span></span>
-   <span data-ttu-id="ebf13-134">Use un [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) para escuchar cambios estructurales o de diseño en la cuadrícula, como las celdas que se han agregado, quitado o combinado.</span><span class="sxs-lookup"><span data-stu-id="ebf13-134">Use a [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) to listen for structural or layout changes to the grid such as cells that have been added, removed, or merged.</span></span>
-   <span data-ttu-id="ebf13-135">Use un [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) para realizar un seguimiento del recorrido a través de los elementos o las celdas de una cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="ebf13-135">Use a [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) to track traversal through the items or cells of a grid.</span></span>

## <a name="required-members-for-igridprovider"></a><span data-ttu-id="ebf13-136">Miembros requeridos para **IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="ebf13-136">Required Members for **IGridProvider**</span></span>

<span data-ttu-id="ebf13-137">Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) .</span><span class="sxs-lookup"><span data-stu-id="ebf13-137">The following properties and methods are required for implementing the [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) interface.</span></span>



| <span data-ttu-id="ebf13-138">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="ebf13-138">Required members</span></span>                                        | <span data-ttu-id="ebf13-139">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="ebf13-139">Member type</span></span> | <span data-ttu-id="ebf13-140">Notas</span><span class="sxs-lookup"><span data-stu-id="ebf13-140">Notes</span></span> |
|---------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="ebf13-141">**Empleado**</span><span class="sxs-lookup"><span data-stu-id="ebf13-141">**RowCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | <span data-ttu-id="ebf13-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ebf13-142">Property</span></span>    | <span data-ttu-id="ebf13-143">None</span><span class="sxs-lookup"><span data-stu-id="ebf13-143">None</span></span>  |
| [<span data-ttu-id="ebf13-144">**NúmeroDeColumnas**</span><span class="sxs-lookup"><span data-stu-id="ebf13-144">**ColumnCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | <span data-ttu-id="ebf13-145">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ebf13-145">Property</span></span>    | <span data-ttu-id="ebf13-146">None</span><span class="sxs-lookup"><span data-stu-id="ebf13-146">None</span></span>  |
| [<span data-ttu-id="ebf13-147">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="ebf13-147">**GetItem**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | <span data-ttu-id="ebf13-148">Método</span><span class="sxs-lookup"><span data-stu-id="ebf13-148">Method</span></span>      | <span data-ttu-id="ebf13-149">None</span><span class="sxs-lookup"><span data-stu-id="ebf13-149">None</span></span>  |



 

<span data-ttu-id="ebf13-150">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="ebf13-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebf13-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebf13-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebf13-152">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="ebf13-152">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="ebf13-153">GridItem (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="ebf13-153">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
</dt> <dt>

[<span data-ttu-id="ebf13-154">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ebf13-154">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="ebf13-155">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="ebf13-155">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




