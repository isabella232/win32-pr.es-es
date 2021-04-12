---
title: Patrón de control de hoja de cálculo
description: Describe las directrices y convenciones para implementar ISpreadsheetProvider, incluida información sobre los métodos.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- Automatización de la interfaz de usuario, implementar patrón de control de hoja de cálculo
- UI Automation, patrón de control de hoja de cálculo
- Automatización de la interfaz de usuario, ISpreadsheetProvider
- ISpreadsheetProvider
- implementar el patrón de control de hoja de cálculo UI Automation
- patrón de control de hoja de cálculo
- patrones de control, ISpreadsheetProvider
- patrones de control, implementar la hoja de cálculo de UI Automation
- patrones de control, hoja de cálculo
- interfaces, ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359187"
---
# <a name="spreadsheet-control-pattern"></a><span data-ttu-id="5ac59-113">Patrón de control de hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="5ac59-113">Spreadsheet Control Pattern</span></span>

<span data-ttu-id="5ac59-114">Describe las directrices y convenciones para implementar [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), incluida información sobre los métodos.</span><span class="sxs-lookup"><span data-stu-id="5ac59-114">Describes guidelines and conventions for implementing [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), including information about methods.</span></span> <span data-ttu-id="5ac59-115">Al final del tema se ofrecen vínculos a referencias adicionales.</span><span class="sxs-lookup"><span data-stu-id="5ac59-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="5ac59-116">El patrón de control de **hoja de cálculo** se usa para exponer el contenido de una hoja de cálculo u otro documento basado en cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="5ac59-116">The **Spreadsheet** control pattern is used to expose the contents of a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="5ac59-117">El patrón de control de la **hoja de cálculo** está estrechamente relacionado con el patrón de control [Grid](uiauto-implementinggrid.md) ; los controles que implementan el patrón de control de **hoja de cálculo** también deben implementar el patrón de control Grid.</span><span class="sxs-lookup"><span data-stu-id="5ac59-117">The **Spreadsheet** control pattern is closely related to the [Grid](uiauto-implementinggrid.md) control pattern; controls that implement the **Spreadsheet** control pattern should also implement the Grid control pattern.</span></span> <span data-ttu-id="5ac59-118">Los controles también pueden implementar el patrón de control [TABLE](uiauto-implementingtable.md) , si procede.</span><span class="sxs-lookup"><span data-stu-id="5ac59-118">Controls can also implement the [Table](uiauto-implementingtable.md) control pattern, if appropriate.</span></span> <span data-ttu-id="5ac59-119">Para obtener ejemplos de controles que implementan estos patrones de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="5ac59-119">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="5ac59-120">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="5ac59-120">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="5ac59-121">Al implementar el patrón de control de la **hoja de cálculo** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="5ac59-121">When implementing the **Spreadsheet** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="5ac59-122">Si una hoja de cálculo implementa la interfaz [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) , sus celdas deben implementar la interfaz [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="5ac59-122">If a spreadsheet implements the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface, its cells must implement the [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>
-   <span data-ttu-id="5ac59-123">El método [**ISpreadsheetProvider:: GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) está diseñado para proporcionar el mismo tipo de navegación que puede proporcionar una aplicación con una característica de **salto a etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="5ac59-123">The [**ISpreadsheetProvider::GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) method is intended to provide the same kind of navigation that an application might supply with a **Jump to Label** feature.</span></span> <span data-ttu-id="5ac59-124">Muchos programas de hojas de cálculo permiten a las celdas específicas asignarles un nombre descriptivo o una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="5ac59-124">Many spreadsheet programs let specific cells be given a friendly name or label.</span></span> <span data-ttu-id="5ac59-125">**GetItemByName** permite al cliente buscar una celda en función de su nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="5ac59-125">**GetItemByName** enables the client to look up a cell based on its friendly name.</span></span> <span data-ttu-id="5ac59-126">Este método no debe recuperar ninguna celda que contenga el texto del nombre porque los resultados pueden ser muy ambiguos.</span><span class="sxs-lookup"><span data-stu-id="5ac59-126">This method should not retrieve any cells that contain the name text because the results can be highly ambiguous.</span></span> <span data-ttu-id="5ac59-127">Si el programa de hoja de cálculo permite que varias celdas de la misma hoja de cálculo tengan el mismo nombre descriptivo o etiqueta, el comportamiento de la automatización de la interfaz de usuario de Microsoft no está definido.</span><span class="sxs-lookup"><span data-stu-id="5ac59-127">If the spreadsheet program allows multiple cells in the same a spreadsheet to have the same friendly name or label, the Microsoft UI Automation behavior is undefined.</span></span>

## <a name="required-members-for-ispreadsheetprovider"></a><span data-ttu-id="5ac59-128">Miembros requeridos para **ISpreadsheetProvider**</span><span class="sxs-lookup"><span data-stu-id="5ac59-128">Required Members for **ISpreadsheetProvider**</span></span>

<span data-ttu-id="5ac59-129">El método siguiente es necesario para implementar la interfaz [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) .</span><span class="sxs-lookup"><span data-stu-id="5ac59-129">The following method is required for implementing the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface.</span></span>



| <span data-ttu-id="5ac59-130">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="5ac59-130">Required members</span></span>                                                       | <span data-ttu-id="5ac59-131">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="5ac59-131">Member type</span></span> | <span data-ttu-id="5ac59-132">Notas</span><span class="sxs-lookup"><span data-stu-id="5ac59-132">Notes</span></span> |
|------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="5ac59-133">**GetItemByName**</span><span class="sxs-lookup"><span data-stu-id="5ac59-133">**GetItemByName**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | <span data-ttu-id="5ac59-134">Método</span><span class="sxs-lookup"><span data-stu-id="5ac59-134">Method</span></span>      | <span data-ttu-id="5ac59-135">None</span><span class="sxs-lookup"><span data-stu-id="5ac59-135">None</span></span>  |



 

<span data-ttu-id="5ac59-136">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="5ac59-136">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ac59-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ac59-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ac59-138">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="5ac59-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="5ac59-139">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="5ac59-139">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="5ac59-140">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="5ac59-140">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 