---
title: Patrón de control MultipleView
description: Describe las directrices y convenciones para implementar IMultipleViewProvider, incluida información sobre propiedades y métodos.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control MultipleView
- Automatización de la interfaz de usuario, patrón de control MultipleView
- Automatización de la interfaz de usuario, IMultipleViewProvider
- IMultipleViewProvider
- implementación de patrones de control MultipleView de UI Automation
- Patrones de control de MultipleView
- patrones de control, IMultipleViewProvider
- patrones de control, implementar la automatización de la interfaz de usuario MultipleView
- patrones de control, MultipleView
- interfaces, IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418845"
---
# <a name="multipleview-control-pattern"></a><span data-ttu-id="c80d4-113">Patrón de control MultipleView</span><span class="sxs-lookup"><span data-stu-id="c80d4-113">MultipleView Control Pattern</span></span>

<span data-ttu-id="c80d4-114">Describe las directrices y convenciones para implementar [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="c80d4-114">Describes guidelines and conventions for implementing [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), including information about properties and methods.</span></span> <span data-ttu-id="c80d4-115">Al final del tema se ofrecen vínculos a referencias adicionales.</span><span class="sxs-lookup"><span data-stu-id="c80d4-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="c80d4-116">El patrón de control **MultipleView** se usa para admitir controles que proporcionan y pueden cambiar entre varias representaciones de la misma información o el mismo conjunto de controles secundarios.</span><span class="sxs-lookup"><span data-stu-id="c80d4-116">The **MultipleView** control pattern is used to support controls that provide, and are able to switch between, multiple representations of the same information or the same set of child controls.</span></span>

<span data-ttu-id="c80d4-117">Algunos ejemplos de controles que pueden presentar varias vistas son la vista de lista (que puede mostrar su contenido como miniaturas, mosaicos, iconos o detalles), gráficos de Microsoft Excel (circular, línea, barra, valor de celda con una fórmula), documentos de Microsoft Word (normal, diseño web, diseño de impresión, diseño de lectura, esquema), calendario de Microsoft Outlook (año, mes, semana, día) y máscaras de Media Player de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c80d4-117">Examples of controls that can present multiple views include the list view (which can show its contents as thumbnails, tiles, icons, or details), Microsoft Excel charts (pie, line, bar, cell value with a formula), Microsoft Word documents (normal, web layout, print layout, reading layout, outline), Microsoft Outlook calendar (year, month, week, day), and Microsoft Windows Media Player skins.</span></span> <span data-ttu-id="c80d4-118">Las vistas admitidas las determina el desarrollador del control y son específicas de cada control.</span><span class="sxs-lookup"><span data-stu-id="c80d4-118">The supported views are determined by the control developer and are specific to each control.</span></span>

<span data-ttu-id="c80d4-119">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="c80d4-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c80d4-120">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="c80d4-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="c80d4-121">Miembros requeridos para **IMultipleViewProvider**</span><span class="sxs-lookup"><span data-stu-id="c80d4-121">Required Members for **IMultipleViewProvider**</span></span>](#required-members-for-imultipleviewprovider)
-   [<span data-ttu-id="c80d4-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c80d4-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="c80d4-123">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="c80d4-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="c80d4-124">Al implementar el patrón de control **MultipleView** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="c80d4-124">When implementing the **MultipleView** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="c80d4-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) también se debe implementar en un contenedor que administre la vista actual si es diferente de un control que proporciona la vista actual.</span><span class="sxs-lookup"><span data-stu-id="c80d4-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) should also be implemented on a container that manages the current view if it is different from a control that provides the current view.</span></span> <span data-ttu-id="c80d4-126">Por ejemplo, el explorador de Windows contiene un control de lista para el contenido de la carpeta actual mientras que la vista del control se administra desde la aplicación del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="c80d4-126">For example, Windows Explorer contains a list control for the current folder content while the view for the control is managed from the Windows Explorer application.</span></span>
-   <span data-ttu-id="c80d4-127">No se considera que un control que puede ordenar su contenido admita varias vistas.</span><span class="sxs-lookup"><span data-stu-id="c80d4-127">A control that is able to sort its content is not considered to support multiple views.</span></span>
-   <span data-ttu-id="c80d4-128">La colección de vistas debe ser idéntica en todas las instancias.</span><span class="sxs-lookup"><span data-stu-id="c80d4-128">The collection of views must be identical across instances.</span></span>
-   <span data-ttu-id="c80d4-129">Los nombres de vista deben ser adecuados para su uso en texto a voz, Braille y otras aplicaciones legibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="c80d4-129">View names must be suitable for use in text to speech, Braille, and other human-readable applications.</span></span>

## <a name="required-members-for-imultipleviewprovider"></a><span data-ttu-id="c80d4-130">Miembros requeridos para **IMultipleViewProvider**</span><span class="sxs-lookup"><span data-stu-id="c80d4-130">Required Members for **IMultipleViewProvider**</span></span>

<span data-ttu-id="c80d4-131">Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) .</span><span class="sxs-lookup"><span data-stu-id="c80d4-131">The following properties and methods are required for implementing the [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) interface.</span></span>



| <span data-ttu-id="c80d4-132">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="c80d4-132">Required members</span></span>                                                            | <span data-ttu-id="c80d4-133">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="c80d4-133">Member type</span></span> | <span data-ttu-id="c80d4-134">Notas</span><span class="sxs-lookup"><span data-stu-id="c80d4-134">Notes</span></span> |
|-----------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="c80d4-135">**CurrentView**</span><span class="sxs-lookup"><span data-stu-id="c80d4-135">**CurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | <span data-ttu-id="c80d4-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c80d4-136">Property</span></span>    | <span data-ttu-id="c80d4-137">None</span><span class="sxs-lookup"><span data-stu-id="c80d4-137">None</span></span>  |
| [<span data-ttu-id="c80d4-138">**GetSupportedViews**</span><span class="sxs-lookup"><span data-stu-id="c80d4-138">**GetSupportedViews**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | <span data-ttu-id="c80d4-139">Método</span><span class="sxs-lookup"><span data-stu-id="c80d4-139">Method</span></span>      | <span data-ttu-id="c80d4-140">None</span><span class="sxs-lookup"><span data-stu-id="c80d4-140">None</span></span>  |
| [<span data-ttu-id="c80d4-141">**GetViewName**</span><span class="sxs-lookup"><span data-stu-id="c80d4-141">**GetViewName**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | <span data-ttu-id="c80d4-142">Método</span><span class="sxs-lookup"><span data-stu-id="c80d4-142">Method</span></span>      | <span data-ttu-id="c80d4-143">None</span><span class="sxs-lookup"><span data-stu-id="c80d4-143">None</span></span>  |
| [<span data-ttu-id="c80d4-144">**SetCurrentView**</span><span class="sxs-lookup"><span data-stu-id="c80d4-144">**SetCurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | <span data-ttu-id="c80d4-145">Método</span><span class="sxs-lookup"><span data-stu-id="c80d4-145">Method</span></span>      | <span data-ttu-id="c80d4-146">None</span><span class="sxs-lookup"><span data-stu-id="c80d4-146">None</span></span>  |



 

<span data-ttu-id="c80d4-147">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="c80d4-147">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c80d4-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c80d4-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c80d4-149">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="c80d4-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="c80d4-150">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="c80d4-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="c80d4-151">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="c80d4-151">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="c80d4-152">Patrón de control ExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="c80d4-152">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




