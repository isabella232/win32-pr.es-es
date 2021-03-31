---
title: Patrón de control SpreadsheetItem
description: Describe las directrices y convenciones para implementar ISpreadsheetItemProvider, incluida información sobre propiedades y métodos.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control SpreadsheetItem
- Automatización de la interfaz de usuario, patrón de control SpreadsheetItem
- Automatización de la interfaz de usuario, ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- implementación del patrón de control SpreadsheetItem de UI Automation
- Patrón de control SpreadsheetItem
- patrones de control, ISpreadsheetItemProvider
- patrones de control, implementar la automatización de la interfaz de usuario SpreadsheetItem
- patrones de control, SpreadsheetItem
- interfaces, ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078240"
---
# <a name="spreadsheetitem-control-pattern"></a><span data-ttu-id="f3205-113">Patrón de control SpreadsheetItem</span><span class="sxs-lookup"><span data-stu-id="f3205-113">SpreadsheetItem Control Pattern</span></span>

<span data-ttu-id="f3205-114">Describe las directrices y convenciones para implementar [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="f3205-114">Describes guidelines and conventions for implementing [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), including information about properties and methods.</span></span> <span data-ttu-id="f3205-115">El patrón de control **SpreadsheetItem** se usa para exponer las propiedades de una celda en una hoja de cálculo u otro documento basado en cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="f3205-115">The **SpreadsheetItem** control pattern is used to expose the properties of a cell in a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="f3205-116">El patrón de control **SpreadsheetItem** está estrechamente relacionado con el patrón de control [GridItem](uiauto-implementinggriditem.md) ; los controles que implementan el patrón de control **SpreadsheetItem** también deben implementar el patrón de control GridItem.</span><span class="sxs-lookup"><span data-stu-id="f3205-116">The **SpreadsheetItem** control pattern is closely related to the [GridItem](uiauto-implementinggriditem.md) control pattern; controls that implement the **SpreadsheetItem** control pattern should also implement the GridItem control pattern.</span></span> <span data-ttu-id="f3205-117">Los controles también pueden implementar el patrón de control [TableItem](uiauto-implementingtableitem.md) , si es necesario.</span><span class="sxs-lookup"><span data-stu-id="f3205-117">Controls can also implement the [TableItem](uiauto-implementingtableitem.md) control pattern, if appropriate.</span></span> <span data-ttu-id="f3205-118">Para obtener ejemplos de controles que implementan estos patrones de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="f3205-118">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="f3205-119">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="f3205-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f3205-120">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="f3205-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="f3205-121">Miembros requeridos para **ISpreadsheetItemProvider**</span><span class="sxs-lookup"><span data-stu-id="f3205-121">Required Members for **ISpreadsheetItemProvider**</span></span>](#required-members-for-ispreadsheetitemprovider)
-   [<span data-ttu-id="f3205-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3205-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="f3205-123">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="f3205-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="f3205-124">Al implementar el patrón de control **SpreadsheetItem** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="f3205-124">When implementing the **SpreadsheetItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="f3205-125">Al implementar los métodos [**ISpreadsheetItemProvider:: GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) y [**ISpreadsheetItemProvider:: GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) , consulte la documentación de [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) .</span><span class="sxs-lookup"><span data-stu-id="f3205-125">When implementing the [**ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) and [**ISpreadsheetItemProvider::GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) methods, please refer to the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) documentation.</span></span> <span data-ttu-id="f3205-126">Estos métodos devuelven matrices para permitir que los proveedores admitan varias anotaciones en una sola celda.</span><span class="sxs-lookup"><span data-stu-id="f3205-126">These methods both return arrays to enable providers to support multiple annotations on a single cell.</span></span>
-   <span data-ttu-id="f3205-127">Algunos tipos de anotaciones no requieren una implementación completa de la interfaz [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) .</span><span class="sxs-lookup"><span data-stu-id="f3205-127">Some kinds of annotations do not require a full implementation of the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) interface.</span></span> <span data-ttu-id="f3205-128">Por ejemplo, un indicador de error ortográfico sencillo podría representarse si [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) devuelve un identificador de atributo de texto de [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)y tiene [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) devuelve un valor null.</span><span class="sxs-lookup"><span data-stu-id="f3205-128">For example, a simple spelling-error indicator could be represented by having [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) return a text attribute identifier of [**AnnotationType\_SpellingError**](uiauto-annotation-type-identifiers.md), and having [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) return a null value.</span></span>

## <a name="required-members-for-ispreadsheetitemprovider"></a><span data-ttu-id="f3205-129">Miembros requeridos para **ISpreadsheetItemProvider**</span><span class="sxs-lookup"><span data-stu-id="f3205-129">Required Members for **ISpreadsheetItemProvider**</span></span>

<span data-ttu-id="f3205-130">Se requieren las siguientes propiedades y métodos para implementar la interfaz [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="f3205-130">The following properties and methods are required for implementing the [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>



| <span data-ttu-id="f3205-131">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="f3205-131">Required members</span></span>                                                                         | <span data-ttu-id="f3205-132">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="f3205-132">Member type</span></span> | <span data-ttu-id="f3205-133">Notas</span><span class="sxs-lookup"><span data-stu-id="f3205-133">Notes</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3205-134">**Fórmula**</span><span class="sxs-lookup"><span data-stu-id="f3205-134">**Formula**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | <span data-ttu-id="f3205-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f3205-135">Property</span></span>    | <span data-ttu-id="f3205-136">La implementación de una propiedad de [**fórmula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) independiente es necesaria porque la propiedad [Value](value-property.md) de una celda devuelve normalmente el valor calculado de la celda.</span><span class="sxs-lookup"><span data-stu-id="f3205-136">Implementing a separate [**Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) property is necessary because a cell’s [Value](value-property.md) property typically returns the computed value of the cell.</span></span> <span data-ttu-id="f3205-137">La propiedad de **fórmula** debe ser **null** si no se ha establecido ninguna fórmula.</span><span class="sxs-lookup"><span data-stu-id="f3205-137">The **Formula** property should be **NULL** if no formula is set.</span></span> |
| [<span data-ttu-id="f3205-138">**GetAnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="f3205-138">**GetAnnotationObjects**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | <span data-ttu-id="f3205-139">Método</span><span class="sxs-lookup"><span data-stu-id="f3205-139">Method</span></span>      | <span data-ttu-id="f3205-140">Devuelve una matriz de proveedores de elementos que hacen referencia a las anotaciones vinculadas a esta celda.</span><span class="sxs-lookup"><span data-stu-id="f3205-140">Returns an array of element providers that refer to the annotations linked to this cell.</span></span> <span data-ttu-id="f3205-141">Los punteros dentro de la matriz pueden ser null si una anotación no tiene un proveedor vinculado.</span><span class="sxs-lookup"><span data-stu-id="f3205-141">Pointers within the array can be null if an annotation does not have a linked provider.</span></span>                                                                                                       |
| [<span data-ttu-id="f3205-142">**GetAnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="f3205-142">**GetAnnotationTypes**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | <span data-ttu-id="f3205-143">Método</span><span class="sxs-lookup"><span data-stu-id="f3205-143">Method</span></span>      | <span data-ttu-id="f3205-144">Devuelve una matriz de identificadores de tipo de anotación que describen las anotaciones de esta celda.</span><span class="sxs-lookup"><span data-stu-id="f3205-144">Returns an array of annotation type identifiers that describe the annotations on this cell.</span></span> <span data-ttu-id="f3205-145">La matriz debe tener el mismo tamaño que la matriz devuelta por [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).</span><span class="sxs-lookup"><span data-stu-id="f3205-145">The array must be the same size as the array returned by [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).</span></span>                                         |



 

<span data-ttu-id="f3205-146">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="f3205-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3205-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3205-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f3205-148">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f3205-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f3205-149">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="f3205-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="f3205-150">Patrón de control de hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="f3205-150">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
</dt> <dt>

[<span data-ttu-id="f3205-151">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="f3205-151">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="f3205-152">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="f3205-152">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 