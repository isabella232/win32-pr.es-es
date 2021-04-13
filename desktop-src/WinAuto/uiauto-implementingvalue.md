---
title: Value (patrón de control)
description: Describe las directrices y convenciones para implementar IValueProvider, incluida información sobre propiedades y métodos.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Value
- Automatización de la interfaz de usuario, patrón de control Value
- Automatización de la interfaz de usuario, IValueProvider
- IValueProvider
- implementar patrones de control de valor de UI Automation
- Patrones de control de valor
- patrones de control, IValueProvider
- patrones de control, implementar el valor de UI Automation
- patrones de control, valor
- interfaces, IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40633a21fdd6b59a2aa35c34258037582a647f05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421053"
---
# <a name="value-control-pattern"></a><span data-ttu-id="10a00-113">Value (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="10a00-113">Value Control Pattern</span></span>

<span data-ttu-id="10a00-114">Describe las directrices y convenciones para implementar [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="10a00-114">Describes guidelines and conventions for implementing [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="10a00-115">El patrón de control **Value** se usa para admitir controles que tienen un valor intrínseco que no abarca un intervalo y que se puede representar como una cadena.</span><span class="sxs-lookup"><span data-stu-id="10a00-115">The **Value** control pattern is used to support controls that have an intrinsic value not spanning a range and that can be represented as a string.</span></span>

<span data-ttu-id="10a00-116">La cadena de valor puede ser editable, dependiendo del control y su configuración.</span><span class="sxs-lookup"><span data-stu-id="10a00-116">The value string can be editable, depending on the control and its settings.</span></span> <span data-ttu-id="10a00-117">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="10a00-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="10a00-118">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="10a00-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="10a00-119">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="10a00-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="10a00-120">Miembros requeridos para **IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="10a00-120">Required Members for **IValueProvider**</span></span>](#required-members-for-ivalueprovider)
-   [<span data-ttu-id="10a00-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="10a00-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="10a00-122">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="10a00-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="10a00-123">Al implementar el patrón de control **Value** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="10a00-123">When implementing the **Value** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="10a00-124">Los controles como un elemento de lista o un elemento de árbol deben admitir el patrón de control **Value** si el valor de cualquiera de los elementos es editable, independientemente del modo de edición actual del control.</span><span class="sxs-lookup"><span data-stu-id="10a00-124">Controls such as a list item or tree item must support the **Value** control pattern if the value of any of the items is editable, regardless of the current edit mode of the control.</span></span> <span data-ttu-id="10a00-125">El control primario también debe admitir el patrón de control **Value** si los elementos secundarios son editables.</span><span class="sxs-lookup"><span data-stu-id="10a00-125">The parent control must also support the **Value** control pattern if the child items are editable.</span></span> <span data-ttu-id="10a00-126">La imagen siguiente muestra un ejemplo de un elemento de lista modificable.</span><span class="sxs-lookup"><span data-stu-id="10a00-126">The following image shows an example of an editable list item.</span></span>

    ![Ilustración donde se muestra el elemento de lista modificable](images/uia-valuepattern-editable-listitem.jpg)

- <span data-ttu-id="10a00-128">Los controles de edición de una y varias líneas deben implementar [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) para exponer su contenido de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="10a00-128">Single and multi-line edit controls must implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) to expose their read-only content.</span></span>
- <span data-ttu-id="10a00-129">Los controles de edición de varias líneas deben implementar [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) si su contenido se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="10a00-129">Multi-line edit controls must implement [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) if their contents can be changed.</span></span>
- <span data-ttu-id="10a00-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) no admite la recuperación de la información de formato o los valores de subcadena.</span><span class="sxs-lookup"><span data-stu-id="10a00-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) does not support the retrieval of formatting information or substring values.</span></span> <span data-ttu-id="10a00-131">Implemente [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) en estos escenarios.</span><span class="sxs-lookup"><span data-stu-id="10a00-131">Implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in these scenarios.</span></span>
- <span data-ttu-id="10a00-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) debe implementarse mediante controles como el control de selección del selector de colores de Microsoft Word (vea la imagen siguiente), que admite la asignación de cadenas entre un valor de color (por ejemplo, "amarillo") y un valor [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) interno equivalente.</span><span class="sxs-lookup"><span data-stu-id="10a00-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) must be implemented by controls such as the color picker selection control from Microsoft Word (see the following image), which supports string mapping between a color value (for example, "yellow") and an equivalent internal [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) value.</span></span>

    ![Ilustración que muestra la asignación de cadena de muestrario de colores](images/uia-valuepattern-colorpicker.jpg)

- <span data-ttu-id="10a00-134">Un control debe tener su propiedad **IsEnabled** establecida en **true** y su propiedad [**ITextProvider:: IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) establecida en **false** antes de permitir una llamada a [**ITextProvider:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).</span><span class="sxs-lookup"><span data-stu-id="10a00-134">A control should have its **IsEnabled** property set to **TRUE** and its [**ITextProvider::IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) property set to **FALSE** before allowing a call to [**ITextProvider::SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).</span></span>

## <a name="required-members-for-ivalueprovider"></a><span data-ttu-id="10a00-135">Miembros requeridos para **IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="10a00-135">Required Members for **IValueProvider**</span></span>

<span data-ttu-id="10a00-136">Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) .</span><span class="sxs-lookup"><span data-stu-id="10a00-136">The following properties and methods are required for implementing the [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) interface.</span></span>



| <span data-ttu-id="10a00-137">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="10a00-137">Required members</span></span>                                       | <span data-ttu-id="10a00-138">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="10a00-138">Member type</span></span> | <span data-ttu-id="10a00-139">Notas</span><span class="sxs-lookup"><span data-stu-id="10a00-139">Notes</span></span> |
|--------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="10a00-140">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="10a00-140">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | <span data-ttu-id="10a00-141">Propiedad</span><span class="sxs-lookup"><span data-stu-id="10a00-141">Property</span></span>    | <span data-ttu-id="10a00-142">None</span><span class="sxs-lookup"><span data-stu-id="10a00-142">None</span></span>  |
| [<span data-ttu-id="10a00-143">**Valor**</span><span class="sxs-lookup"><span data-stu-id="10a00-143">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | <span data-ttu-id="10a00-144">Propiedad</span><span class="sxs-lookup"><span data-stu-id="10a00-144">Property</span></span>    | <span data-ttu-id="10a00-145">None</span><span class="sxs-lookup"><span data-stu-id="10a00-145">None</span></span>  |
| [<span data-ttu-id="10a00-146">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="10a00-146">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | <span data-ttu-id="10a00-147">Método</span><span class="sxs-lookup"><span data-stu-id="10a00-147">Method</span></span>      | <span data-ttu-id="10a00-148">None</span><span class="sxs-lookup"><span data-stu-id="10a00-148">None</span></span>  |



 

<span data-ttu-id="10a00-149">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="10a00-149">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10a00-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="10a00-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10a00-151">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="10a00-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="10a00-152">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="10a00-152">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="10a00-153">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="10a00-153">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="10a00-154">Patrones de control Text y TextRange</span><span class="sxs-lookup"><span data-stu-id="10a00-154">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 