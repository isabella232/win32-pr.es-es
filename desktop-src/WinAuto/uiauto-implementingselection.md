---
title: Selection (patrón de control)
description: Describe las directrices y convenciones para implementar ISelectionProvider, incluida información sobre propiedades, métodos y eventos.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Selection
- UI Automation, Selection (patrón de control)
- Automatización de la interfaz de usuario, ISelectionProvider
- ISelectionProvider
- implementar patrones de control de selección de UI Automation
- Patrones de control de selección
- patrones de control, ISelectionProvider
- patrones de control, implementar la selección de automatización de la interfaz de usuario
- patrones de control, selección
- interfaces, ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075781"
---
# <a name="selection-control-pattern"></a><span data-ttu-id="947f4-113">Selection (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="947f4-113">Selection Control Pattern</span></span>

<span data-ttu-id="947f4-114">Describe las directrices y convenciones para implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), incluida información sobre propiedades, métodos y eventos.</span><span class="sxs-lookup"><span data-stu-id="947f4-114">Describes guidelines and conventions for implementing [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="947f4-115">El patrón de control **Selection** se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios seleccionables.</span><span class="sxs-lookup"><span data-stu-id="947f4-115">The **Selection** control pattern is used to support controls that act as containers for a collection of selectable child items.</span></span> <span data-ttu-id="947f4-116">Los elementos secundarios de este elemento deben implementar [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="947f4-116">The children of this element must implement [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

<span data-ttu-id="947f4-117">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="947f4-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="947f4-118">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="947f4-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="947f4-119">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="947f4-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="947f4-120">Miembros requeridos para **ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="947f4-120">Required Members for **ISelectionProvider**</span></span>](#required-members-for-iselectionprovider)
-   [<span data-ttu-id="947f4-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="947f4-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="947f4-122">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="947f4-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="947f4-123">Al implementar el patrón de control **Selection** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="947f4-123">When implementing the **Selection** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="947f4-124">Los controles que implementan [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) permiten la selección de uno o varios elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="947f4-124">Controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) allow either single or multiple child items to be selected.</span></span> <span data-ttu-id="947f4-125">Por ejemplo, los cuadros de lista, las vistas de lista y las vistas de árbol admiten varias selecciones, mientras que los cuadros combinados, los controles deslizantes y los grupos de botones de radio admiten la selección única.</span><span class="sxs-lookup"><span data-stu-id="947f4-125">For example, list boxes, list views, and tree views support multiple selections, whereas combo boxes, sliders, and radio button groups support single selection.</span></span>
-   <span data-ttu-id="947f4-126">Los controles que tienen un intervalo mínimo, máximo y continuo, como el control deslizante de **volumen** de un reproductor multimedia, deben implementar [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) en lugar de [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="947f4-126">Controls that have a minimum, maximum, and continuous range, such as the **Volume** slider control of a media player, should implement [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) instead of [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>
-   <span data-ttu-id="947f4-127">Los controles de selección única que administran los controles secundarios que implementan [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), como el control deslizante de **resolución de pantalla** del cuadro de diálogo Propiedades de **pantalla** para Windows, o el control de selección **selector de colores** de Microsoft Word (vea la imagen siguiente), deben implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); sus elementos secundarios deben implementar [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) y [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="947f4-127">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, or the **Color Picker** selection control from Microsoft Word (see the following image), should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

    ![imagen que muestra un ejemplo de asignación de cadena de muestrario de colores](images/uia-valuepattern-colorpicker.jpg)

-   <span data-ttu-id="947f4-129">Los menús no admiten el patrón de control **Selection** .</span><span class="sxs-lookup"><span data-stu-id="947f4-129">Menus do not support the **Selection** control pattern.</span></span> <span data-ttu-id="947f4-130">Si está trabajando con elementos de menú que incluyen tanto gráficos como texto (como los elementos del **Panel de vista previa** en el menú **Ver** de Microsoft Outlook) y necesita transmitir el estado, debe implementar [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span><span class="sxs-lookup"><span data-stu-id="947f4-130">If you are working with menu items that include both graphics and text (such as the **Preview Pane** items in the **View** menu in Microsoft Outlook) and need to convey state, you should implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span></span>

## <a name="required-members-for-iselectionprovider"></a><span data-ttu-id="947f4-131">Miembros requeridos para **ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="947f4-131">Required Members for **ISelectionProvider**</span></span>

<span data-ttu-id="947f4-132">Se requieren las siguientes propiedades, métodos y eventos para implementar la interfaz [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .</span><span class="sxs-lookup"><span data-stu-id="947f4-132">The following properties, methods, and events are required for implementing the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>



| <span data-ttu-id="947f4-133">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="947f4-133">Required members</span></span>                                                                                | <span data-ttu-id="947f4-134">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="947f4-134">Member type</span></span> | <span data-ttu-id="947f4-135">Notas</span><span class="sxs-lookup"><span data-stu-id="947f4-135">Notes</span></span>                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="947f4-136">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="947f4-136">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | <span data-ttu-id="947f4-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="947f4-137">Property</span></span>    | <span data-ttu-id="947f4-138">None</span><span class="sxs-lookup"><span data-stu-id="947f4-138">None</span></span>                                                                        |
| [<span data-ttu-id="947f4-139">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="947f4-139">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | <span data-ttu-id="947f4-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="947f4-140">Property</span></span>    | <span data-ttu-id="947f4-141">None</span><span class="sxs-lookup"><span data-stu-id="947f4-141">None</span></span>                                                                        |
| [<span data-ttu-id="947f4-142">**GetSelection**</span><span class="sxs-lookup"><span data-stu-id="947f4-142">**GetSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | <span data-ttu-id="947f4-143">Método</span><span class="sxs-lookup"><span data-stu-id="947f4-143">Method</span></span>      | <span data-ttu-id="947f4-144">None</span><span class="sxs-lookup"><span data-stu-id="947f4-144">None</span></span>                                                                        |
| [<span data-ttu-id="947f4-145">**\_InvalidatedEventId de selección de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="947f4-145">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="947f4-146">Evento</span><span class="sxs-lookup"><span data-stu-id="947f4-146">Event</span></span>       | <span data-ttu-id="947f4-147">Genera este evento cuando una selección de un contenedor ha cambiado significativamente.</span><span class="sxs-lookup"><span data-stu-id="947f4-147">Raise this event when a selection in a container has changed significantly.</span></span> |



 

<span data-ttu-id="947f4-148">Las propiedades [**ISelectionProvider:: IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) y [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) pueden ser dinámicas.</span><span class="sxs-lookup"><span data-stu-id="947f4-148">The [**ISelectionProvider::IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) and [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) properties can be dynamic.</span></span> <span data-ttu-id="947f4-149">Por ejemplo, es posible que el estado inicial de un control no tenga elementos seleccionados de forma predeterminada, lo que indica que **IsSelectionRequired** es false.</span><span class="sxs-lookup"><span data-stu-id="947f4-149">For example, the initial state of a control might not have any items selected by default, indicating that **IsSelectionRequired** is false.</span></span> <span data-ttu-id="947f4-150">Sin embargo, cuando se haya seleccionado un elemento, el control siempre debe tener al menos un elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="947f4-150">However, after an item is selected, the control must always have at least one item selected.</span></span> <span data-ttu-id="947f4-151">Del mismo modo, en raras ocasiones, un control podría permitir la selección de varios elementos en la inicialización pero solo permitir posteriormente la realización de selecciones únicas.</span><span class="sxs-lookup"><span data-stu-id="947f4-151">Similarly, in rare cases, a control might allow multiple items to be selected on initialization, but subsequently allow only single selections to be made.</span></span>

## <a name="related-topics"></a><span data-ttu-id="947f4-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="947f4-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="947f4-153">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="947f4-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="947f4-154">Patrón de control SelectionItem</span><span class="sxs-lookup"><span data-stu-id="947f4-154">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
</dt> <dt>

[<span data-ttu-id="947f4-155">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="947f4-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="947f4-156">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="947f4-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




