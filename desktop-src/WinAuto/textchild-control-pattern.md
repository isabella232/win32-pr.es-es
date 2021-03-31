---
title: Patrón de control TextChild
description: Presenta directrices y convenciones para implementar ITextChildProvider, incluida información sobre propiedades y métodos. El patrón de control TextChild se usa para tener acceso al antecesor más cercano de un elemento que admite el patrón de control Text.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control TextChild
- Automatización de la interfaz de usuario, patrón de control TextChild
- Automatización de la interfaz de usuario, ITextChildProvider
- ITextChildProvider
- implementación de patrones de control TextChild de UI Automation
- Patrones de control de TextChild
- patrones de control, ITextChildProvider
- patrones de control, implementar la automatización de la interfaz de usuario TextChild
- patrones de control, TextChild
- interfaces, ITextChildProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21102abfef7cee0553850ac01c4f759f81988e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793617"
---
# <a name="textchild-control-pattern"></a><span data-ttu-id="a97d0-114">Patrón de control TextChild</span><span class="sxs-lookup"><span data-stu-id="a97d0-114">TextChild Control Pattern</span></span>

<span data-ttu-id="a97d0-115">Presenta directrices y convenciones para implementar [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="a97d0-115">Introduces guidelines and conventions for implementing [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), including information about properties and methods.</span></span> <span data-ttu-id="a97d0-116">El patrón de control **TextChild** se usa para tener acceso al antecesor más cercano de un elemento que admite el patrón de control [Text](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="a97d0-116">The **TextChild** control pattern is used to access an element’s nearest ancestor that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>

<span data-ttu-id="a97d0-117">Por ejemplo, supongamos que el texto de un documento contiene una imagen incrustada y un hipervínculo, tal como se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="a97d0-117">For example, suppose text in a document contains an embedded image and a hyperlink as shown in the following image.</span></span>

![captura de pantalla que muestra texto que contiene una imagen incrustada y un hipervínculo](images/textchild-pattern.png)

<span data-ttu-id="a97d0-119">Si usa las herramientas de automatización de la interfaz de usuario de Microsoft para examinar el árbol de automatización de la interfaz de usuario para este contenido de documento, podría mostrar un elemento de documento con un elemento secundario que represente la imagen y otro elemento secundario que represente el hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="a97d0-119">If you use Microsoft UI Automation tools to examine the UI Automation tree for this document content, it might show a document element with one child element that represents the image, and another child element that represents the hyperlink.</span></span> <span data-ttu-id="a97d0-120">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a97d0-120">For example:</span></span>

![captura de pantalla que muestra inspeccionar un árbol de elementos de automatización de la interfaz de usuario de ejemplo](images/textchild-pattern-tree.png)

<span data-ttu-id="a97d0-122">Normalmente, el elemento de documento en el ejemplo anterior admite el patrón de control [Text](uiauto-implementingtextandtextrange.md) , pero no los dos elementos secundarios del elemento de documento.</span><span class="sxs-lookup"><span data-stu-id="a97d0-122">Typically, the document element in the preceding example supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, but the two children of the document element do not.</span></span> <span data-ttu-id="a97d0-123">Si una aplicación cliente de automatización de la interfaz de usuario tiene una referencia al elemento de imagen o al elemento de hipervínculo, el cliente puede usar el patrón de control **TextChild** como una manera cómoda de tener acceso al patrón TextControl expuesto por el elemento de documento que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="a97d0-123">If a UI Automation client application has a reference to the image element or hyperlink element, the client can use the **TextChild** control pattern as a convenient way to access the Textcontrol pattern exposed by the containing document element.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="a97d0-124">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="a97d0-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="a97d0-125">Al implementar la interfaz [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="a97d0-125">When implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="a97d0-126">La propiedad [**ITextChildProvider:: TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) debe especificar el elemento antecesor más cercano que admita la interfaz [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) , independientemente de si los elementos situados más arriba en la cadena antecesor también admiten **ITextProvider**.</span><span class="sxs-lookup"><span data-stu-id="a97d0-126">The [**ITextChildProvider::TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) property should specify the nearest ancestor element that supports [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) interface, regardless of whether elements higher in the ancestor chain also support **ITextProvider**.</span></span>
-   <span data-ttu-id="a97d0-127">Un elemento no debe ser compatible con la interfaz [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) y [ITextChildProvider \* \*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .</span><span class="sxs-lookup"><span data-stu-id="a97d0-127">An element should not support both the [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) and the [ITextChildProvider\*\*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>
- <span data-ttu-id="a97d0-128">Un elemento que implementa [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) debe ser un elemento secundario, o descendiente, de un elemento que implemente [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).</span><span class="sxs-lookup"><span data-stu-id="a97d0-128">An element that implements [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) must be a child, or descendent, of an element that implements [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).</span></span> <span data-ttu-id="a97d0-129">No es necesario que este elemento también implemente el [patrón de control Text](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).</span><span class="sxs-lookup"><span data-stu-id="a97d0-129">It is not required that this element also implement the [Text control pattern](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).</span></span>
-   <span data-ttu-id="a97d0-130">La propiedad [**ITextChildProvider:: TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) debe especificar el mismo intervalo de texto que el que devuelve el elemento del proveedor de texto que contiene cuando se llama a la función [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) con el elemento secundario text como el elemento secundario incluido.</span><span class="sxs-lookup"><span data-stu-id="a97d0-130">The [**ITextChildProvider::TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) property should specify the same text range as the one that the containing text provider element returns when its [**ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) function is called with the text child element as the enclosed child element.</span></span>

## <a name="required-members-for-itextchildprovider"></a><span data-ttu-id="a97d0-131">Miembros requeridos para **ITextChildProvider**</span><span class="sxs-lookup"><span data-stu-id="a97d0-131">Required Members for **ITextChildProvider**</span></span>

<span data-ttu-id="a97d0-132">Estas propiedades y métodos son necesarios para implementar la interfaz [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .</span><span class="sxs-lookup"><span data-stu-id="a97d0-132">These properties and methods are required for implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>



| <span data-ttu-id="a97d0-133">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="a97d0-133">Required members</span></span>                                                     | <span data-ttu-id="a97d0-134">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="a97d0-134">Member type</span></span> | <span data-ttu-id="a97d0-135">Notas</span><span class="sxs-lookup"><span data-stu-id="a97d0-135">Notes</span></span> |
|----------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="a97d0-136">**TextContainer**</span><span class="sxs-lookup"><span data-stu-id="a97d0-136">**TextContainer**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | <span data-ttu-id="a97d0-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a97d0-137">Property</span></span>    | <span data-ttu-id="a97d0-138">None</span><span class="sxs-lookup"><span data-stu-id="a97d0-138">None</span></span>  |
| [<span data-ttu-id="a97d0-139">**TextRange**</span><span class="sxs-lookup"><span data-stu-id="a97d0-139">**TextRange**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | <span data-ttu-id="a97d0-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a97d0-140">Property</span></span>    | <span data-ttu-id="a97d0-141">None</span><span class="sxs-lookup"><span data-stu-id="a97d0-141">None</span></span>  |



 

<span data-ttu-id="a97d0-142">Este patrón de control no tiene métodos o propiedades asociados.</span><span class="sxs-lookup"><span data-stu-id="a97d0-142">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a97d0-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a97d0-143">Related topics</span></span>

<span data-ttu-id="a97d0-144">**Vista**</span><span class="sxs-lookup"><span data-stu-id="a97d0-144">**Conceptual**</span></span>

- [<span data-ttu-id="a97d0-145">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="a97d0-145">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
- [<span data-ttu-id="a97d0-146">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="a97d0-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
- [<span data-ttu-id="a97d0-147">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="a97d0-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)