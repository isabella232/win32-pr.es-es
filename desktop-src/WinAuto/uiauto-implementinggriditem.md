---
title: GridItem (patrón de control)
description: Describe las directrices y convenciones para implementar IGridItemProvider, incluida información sobre las propiedades. El patrón de control GridItem se usa para admitir controles secundarios individuales de contenedores que implementan IGridProvider.
ms.assetid: ae4b9021-1800-485b-99a2-54ddf9c21f93
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control GridItem
- Automatización de la interfaz de usuario, modelo de control GridItem
- Automatización de la interfaz de usuario, IGridItemProvider
- IGridItemProvider
- implementar patrones de control GridItem de automatización de la interfaz de usuario
- GridItem (patrones de control)
- patrones de control, IGridItemProvider
- patrones de control, implementación de la automatización de la interfaz de usuario
- patrones de control, GridItem
- interfaces, IGridItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef45b5f655e3ef09350c508271233de49f964a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775229"
---
# <a name="griditem-control-pattern"></a><span data-ttu-id="d4cc7-114">GridItem (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="d4cc7-114">GridItem Control Pattern</span></span>

<span data-ttu-id="d4cc7-115">Describe las directrices y convenciones para implementar [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), incluida información sobre las propiedades.</span><span class="sxs-lookup"><span data-stu-id="d4cc7-115">Describes guidelines and conventions for implementing [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), including information about properties.</span></span> <span data-ttu-id="d4cc7-116">El patrón de control **GridItem** se usa para admitir controles secundarios individuales de contenedores que implementan [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span><span class="sxs-lookup"><span data-stu-id="d4cc7-116">The **GridItem** control pattern is used to support individual child controls of containers that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>

<span data-ttu-id="d4cc7-117">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="d4cc7-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="d4cc7-118">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="d4cc7-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d4cc7-119">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="d4cc7-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="d4cc7-120">Miembros requeridos para **IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="d4cc7-120">Required Members for **IGridItemProvider**</span></span>](#required-members-for-igriditemprovider)
-   [<span data-ttu-id="d4cc7-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4cc7-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="d4cc7-122">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="d4cc7-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="d4cc7-123">Al implementar el patrón de control **GridItem** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="d4cc7-123">When implementing the **GridItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="d4cc7-124">Las coordenadas de la cuadrícula son de base, donde la celda superior izquierda tiene las coordenadas (0, 0).</span><span class="sxs-lookup"><span data-stu-id="d4cc7-124">Grid coordinates are zero-based with the upper left cell having coordinates (0, 0).</span></span>
-   <span data-ttu-id="d4cc7-125">Las celdas combinadas informarán de sus propiedades de [**fila**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) y [**columna**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) en función de su celda de anclaje subyacente, tal como se define en el proveedor de automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d4cc7-125">Merged cells will report their [**Row**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) and [**Column**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) properties based on their underlying anchor cell as defined by the Microsoft UI Automation provider.</span></span> <span data-ttu-id="d4cc7-126">Normalmente, será la fila o columna superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="d4cc7-126">Typically, it will be the topmost and leftmost row or column.</span></span>
-   <span data-ttu-id="d4cc7-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) no proporciona una manipulación activa de la cuadrícula, como combinar o dividir celdas.</span><span class="sxs-lookup"><span data-stu-id="d4cc7-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not provide for active manipulation of the grid such as merging or splitting cells.</span></span>
-   <span data-ttu-id="d4cc7-128">Los controles que implementan [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) normalmente se pueden atravesar (es decir, un cliente de automatización de la interfaz de usuario puede moverse a controles adyacentes) con el teclado.</span><span class="sxs-lookup"><span data-stu-id="d4cc7-128">Controls that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) can typically be traversed (that is, a UI Automation client can move to adjacent controls) by using the keyboard.</span></span>

## <a name="required-members-for-igriditemprovider"></a><span data-ttu-id="d4cc7-129">Miembros requeridos para **IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="d4cc7-129">Required Members for **IGridItemProvider**</span></span>

<span data-ttu-id="d4cc7-130">Las siguientes propiedades son necesarias para implementar la interfaz [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) .</span><span class="sxs-lookup"><span data-stu-id="d4cc7-130">The following properties are required for implementing the [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) interface.</span></span>



| <span data-ttu-id="d4cc7-131">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="d4cc7-131">Required members</span></span>                                                  | <span data-ttu-id="d4cc7-132">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="d4cc7-132">Member type</span></span> | <span data-ttu-id="d4cc7-133">Notas</span><span class="sxs-lookup"><span data-stu-id="d4cc7-133">Notes</span></span> |
|-------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="d4cc7-134">**Row**</span><span class="sxs-lookup"><span data-stu-id="d4cc7-134">**Row**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | <span data-ttu-id="d4cc7-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4cc7-135">Property</span></span>    | <span data-ttu-id="d4cc7-136">None</span><span class="sxs-lookup"><span data-stu-id="d4cc7-136">None</span></span>  |
| [<span data-ttu-id="d4cc7-137">**Columna**</span><span class="sxs-lookup"><span data-stu-id="d4cc7-137">**Column**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | <span data-ttu-id="d4cc7-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4cc7-138">Property</span></span>    | <span data-ttu-id="d4cc7-139">None</span><span class="sxs-lookup"><span data-stu-id="d4cc7-139">None</span></span>  |
| [<span data-ttu-id="d4cc7-140">**RowSpan**</span><span class="sxs-lookup"><span data-stu-id="d4cc7-140">**RowSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | <span data-ttu-id="d4cc7-141">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4cc7-141">Property</span></span>    | <span data-ttu-id="d4cc7-142">None</span><span class="sxs-lookup"><span data-stu-id="d4cc7-142">None</span></span>  |
| [<span data-ttu-id="d4cc7-143">**ColumnSpan**</span><span class="sxs-lookup"><span data-stu-id="d4cc7-143">**ColumnSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | <span data-ttu-id="d4cc7-144">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4cc7-144">Property</span></span>    | <span data-ttu-id="d4cc7-145">None</span><span class="sxs-lookup"><span data-stu-id="d4cc7-145">None</span></span>  |
| [<span data-ttu-id="d4cc7-146">**ContainingGrid**</span><span class="sxs-lookup"><span data-stu-id="d4cc7-146">**ContainingGrid**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | <span data-ttu-id="d4cc7-147">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4cc7-147">Property</span></span>    | <span data-ttu-id="d4cc7-148">None</span><span class="sxs-lookup"><span data-stu-id="d4cc7-148">None</span></span>  |



 

<span data-ttu-id="d4cc7-149">Este patrón de control no tiene métodos o propiedades asociados.</span><span class="sxs-lookup"><span data-stu-id="d4cc7-149">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4cc7-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4cc7-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4cc7-151">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="d4cc7-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="d4cc7-152">Grid (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="d4cc7-152">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
</dt> <dt>

[<span data-ttu-id="d4cc7-153">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="d4cc7-153">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="d4cc7-154">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="d4cc7-154">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




