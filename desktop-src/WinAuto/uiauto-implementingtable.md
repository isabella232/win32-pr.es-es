---
title: Table (patrón de control)
description: Describe las directrices y convenciones para implementar ITableProvider, incluida información sobre propiedades y métodos. El patrón de control Table se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Table
- Automatización de la interfaz de usuario, patrón de control Table
- Automatización de la interfaz de usuario, ITableProvider
- ITableProvider
- implementación de patrones de control de tabla de UI Automation
- Patrones de control de tabla
- patrones de control, ITableProvider
- patrones de control, implementar la tabla de automatización de la interfaz de usuario
- patrones de control, tabla
- interfaces, ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9879d1589985df0257a1dd7805f474c013b93732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104556988"
---
# <a name="table-control-pattern"></a><span data-ttu-id="a92e3-114">Table (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="a92e3-114">Table Control Pattern</span></span>

<span data-ttu-id="a92e3-115">Describe las directrices y convenciones para implementar [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="a92e3-115">Describes guidelines and conventions for implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), including information about properties and methods.</span></span> <span data-ttu-id="a92e3-116">El patrón de control **TABLE** se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a92e3-116">The **Table** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="a92e3-117">Los elementos secundarios del elemento contenedor deben implementar [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) y organizarse en un sistema de coordenadas lógico bidimensional que se pueda atravesar por fila y columna.</span><span class="sxs-lookup"><span data-stu-id="a92e3-117">The children of the container element must implement [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="a92e3-118">Este patrón de control es análogo a [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) , con la diferencia de que cualquier control que implemente [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) también debe exponer una relación de encabezado de columna o fila para cada elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="a92e3-118">This control pattern is analogous to [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) with the distinction that any control implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) must also expose a column and/or row header relationship for each child element.</span></span> <span data-ttu-id="a92e3-119">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="a92e3-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="a92e3-120">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="a92e3-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a92e3-121">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="a92e3-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="a92e3-122">Miembros requeridos para **ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="a92e3-122">Required Members for **ITableProvider**</span></span>](#required-members-for-itableprovider)
-   [<span data-ttu-id="a92e3-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a92e3-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="a92e3-124">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="a92e3-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="a92e3-125">Al implementar el patrón de control **TABLE** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="a92e3-125">When implementing the **Table** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="a92e3-126">El acceso al contenido de celdas individuales se realiza a través de un sistema de coordenadas lógico bidimensional o una matriz que proporciona la implementación simultánea necesaria de [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span><span class="sxs-lookup"><span data-stu-id="a92e3-126">Access to the content of individual cells is through a two-dimensional logical coordinate system or array provided by the required, concurrent implementation of [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>
-   <span data-ttu-id="a92e3-127">Un encabezado de columna o fila puede estar dentro de un objeto de tabla o ser un objeto de encabezado independiente asociado a un objeto de tabla.</span><span class="sxs-lookup"><span data-stu-id="a92e3-127">A column or row header can be contained within a table object or be a separate header object that is associated with a table object.</span></span>
-   <span data-ttu-id="a92e3-128">Los encabezados de fila y columna pueden incluir tanto un encabezado principal como cualquier encabezado auxiliar.</span><span class="sxs-lookup"><span data-stu-id="a92e3-128">Column and row headers may include both a primary header as well as any supporting headers.</span></span>
    > [!Note]  
    > <span data-ttu-id="a92e3-129">Este concepto se vuelve evidente en una hoja de cálculo de Microsoft Excel en la que un usuario ha definido una columna de **nombre** .</span><span class="sxs-lookup"><span data-stu-id="a92e3-129">This concept becomes evident in a Microsoft Excel spreadsheet where a user has defined a **First name** column.</span></span> <span data-ttu-id="a92e3-130">Esta columna tiene ahora dos encabezados, incluido el encabezado **First Name** definido por el usuario, y la designación alfanumérica para esa columna asignada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a92e3-130">This column now has two headers, including the **First name** header defined by the user, and the alphanumeric designation for that column assigned by the application.</span></span>

     

-   <span data-ttu-id="a92e3-131">Vea [patrón de control de cuadrícula](uiauto-implementinggrid.md) para la funcionalidad de cuadrícula relacionada.</span><span class="sxs-lookup"><span data-stu-id="a92e3-131">See [Grid Control Pattern](uiauto-implementinggrid.md) for related grid functionality.</span></span>

    <span data-ttu-id="a92e3-132">En la imagen siguiente se muestra una tabla con encabezados de columna complejos.</span><span class="sxs-lookup"><span data-stu-id="a92e3-132">The following image shows a table with complex column headers.</span></span>

    ![tabla con encabezados de columna complejos](images/uia-valuepattern-colorpicker.jpg)

    <span data-ttu-id="a92e3-134">En la imagen siguiente se muestra una tabla con una propiedad [**ITableProvider:: RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) ambigua.</span><span class="sxs-lookup"><span data-stu-id="a92e3-134">The following image shows a table with an ambiguous [**ITableProvider::RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) property.</span></span>

    ![tabla con una propiedad RowOrColumnMajor ambigua](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a><span data-ttu-id="a92e3-136">Miembros requeridos para **ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="a92e3-136">Required Members for **ITableProvider**</span></span>

<span data-ttu-id="a92e3-137">Se requieren las siguientes propiedades y métodos para implementar la interfaz [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) .</span><span class="sxs-lookup"><span data-stu-id="a92e3-137">The following properties and methods are required for implementing the [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) interface.</span></span>



| <span data-ttu-id="a92e3-138">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="a92e3-138">Required members</span></span>                                                   | <span data-ttu-id="a92e3-139">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="a92e3-139">Member type</span></span> | <span data-ttu-id="a92e3-140">Notas</span><span class="sxs-lookup"><span data-stu-id="a92e3-140">Notes</span></span> |
|--------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="a92e3-141">**RowOrColumnMajor**</span><span class="sxs-lookup"><span data-stu-id="a92e3-141">**RowOrColumnMajor**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | <span data-ttu-id="a92e3-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a92e3-142">Property</span></span>    | <span data-ttu-id="a92e3-143">None</span><span class="sxs-lookup"><span data-stu-id="a92e3-143">None</span></span>  |
| [<span data-ttu-id="a92e3-144">**GetColumnHeaders**</span><span class="sxs-lookup"><span data-stu-id="a92e3-144">**GetColumnHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | <span data-ttu-id="a92e3-145">Método</span><span class="sxs-lookup"><span data-stu-id="a92e3-145">Method</span></span>      | <span data-ttu-id="a92e3-146">None</span><span class="sxs-lookup"><span data-stu-id="a92e3-146">None</span></span>  |
| [<span data-ttu-id="a92e3-147">**GetRowHeaders**</span><span class="sxs-lookup"><span data-stu-id="a92e3-147">**GetRowHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | <span data-ttu-id="a92e3-148">Método</span><span class="sxs-lookup"><span data-stu-id="a92e3-148">Method</span></span>      | <span data-ttu-id="a92e3-149">None</span><span class="sxs-lookup"><span data-stu-id="a92e3-149">None</span></span>  |



 

<span data-ttu-id="a92e3-150">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="a92e3-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a92e3-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a92e3-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a92e3-152">**Vista**</span><span class="sxs-lookup"><span data-stu-id="a92e3-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a92e3-153">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="a92e3-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="a92e3-154">Patrón de control TableItem</span><span class="sxs-lookup"><span data-stu-id="a92e3-154">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
</dt> <dt>

[<span data-ttu-id="a92e3-155">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="a92e3-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="a92e3-156">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="a92e3-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




