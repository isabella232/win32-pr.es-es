---
title: Atributos de texto de automatización de la interfaz de usuario
description: En este tema se describe cómo la automatización de la interfaz de usuario de Microsoft expone el formato y las propiedades de estilo (atributos de texto) de contenido textual y proporciona una lista de atributos de texto admitidos.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- Automatización de la interfaz de usuario, atributos de texto
- atributos de texto, acerca de
- atributos de texto, tipos Variant
- atributos de texto, tipos de datos
- Automatización de la interfaz de usuario, lista de atributos
- Automatización de la interfaz de usuario, lista de atributos de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b011203111a6484156921d63cc27bb11b017e596
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714413"
---
# <a name="ui-automation-text-attributes"></a><span data-ttu-id="752fa-109">Atributos de texto de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="752fa-109">UI Automation Text Attributes</span></span>

<span data-ttu-id="752fa-110">En este tema se describe cómo la automatización de la interfaz de usuario de Microsoft expone el formato y las propiedades de estilo (*atributos de texto*) de contenido textual y proporciona una lista de atributos de texto admitidos.</span><span class="sxs-lookup"><span data-stu-id="752fa-110">This topic describes how Microsoft UI Automation exposes the format and style properties (*text attributes*) of textual content, and provides a list of supported text attributes.</span></span>

<span data-ttu-id="752fa-111">Los proveedores de automatización de la interfaz de usuario exponen atributos de texto a través de los métodos [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) y [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) del patrón de control [TextRange](uiauto-about-text-and-textrange-patterns.md) .</span><span class="sxs-lookup"><span data-stu-id="752fa-111">UI Automation providers expose text attributes through the [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) and [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) methods of the [TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern.</span></span> <span data-ttu-id="752fa-112">Las aplicaciones cliente usan el método [**IUIAutomationTextRange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) para recuperar el valor de un atributo de texto determinado para un intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="752fa-112">Client applications use the [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) method to retrieve the value of a particular text attribute for a text range.</span></span> <span data-ttu-id="752fa-113">Los clientes pueden usar el método [**IUIAutomationTextRange:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) para buscar texto en un intervalo de texto que tiene un atributo determinado.</span><span class="sxs-lookup"><span data-stu-id="752fa-113">Clients can use the [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) method to search a text range for text that has a particular attribute.</span></span> <span data-ttu-id="752fa-114">Si se encuentra cualquier texto coincidente, el método crea un nuevo intervalo de texto que contiene el texto coincidente.</span><span class="sxs-lookup"><span data-stu-id="752fa-114">If any matching text is found, the method creates a new text range that contains the matching text.</span></span>

<span data-ttu-id="752fa-115">El patrón de control **TextRange** admite los atributos de texto de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="752fa-115">The text attributes in the following list are supported by the **TextRange** control pattern.</span></span> <span data-ttu-id="752fa-116">Los nombres de atributo se derivan de los identificadores de atributo de texto de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="752fa-116">The attribute names are derived from the UI Automation text attribute identifiers.</span></span> <span data-ttu-id="752fa-117">Por ejemplo, el atributo **AnimationStyle** lo identifican los clientes como [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definido en Uiautomationclient. h) y los proveedores como **Text \_ AnimationStyle \_ Attribute \_ GUID** (definido en Uiautomationcoreapi. h).</span><span class="sxs-lookup"><span data-stu-id="752fa-117">For example, the **AnimationStyle** attribute is identified by clients as [**UIA\_AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (defined in Uiautomationclient.h) and by providers as **Text\_AnimationStyle\_Attribute\_GUID** (defined in Uiautomationcoreapi.h).</span></span> <span data-ttu-id="752fa-118">Para obtener más información sobre cada atributo de texto compatible, vea [**identificadores de atributos de texto**](uiauto-textattribute-ids.md).</span><span class="sxs-lookup"><span data-stu-id="752fa-118">For more information about each supported text attribute, see [**Text Attribute Identifiers**](uiauto-textattribute-ids.md).</span></span>

> [!Note]  
> <span data-ttu-id="752fa-119">Algunos de los atributos enumerados se admiten a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="752fa-119">Some of the attributes listed are supported starting with Windows 8.</span></span> <span data-ttu-id="752fa-120">Vea [**identificadores de atributos de texto**](uiauto-textattribute-ids.md) para las notas relacionadas con la compatibilidad de versiones.</span><span class="sxs-lookup"><span data-stu-id="752fa-120">See [**Text Attribute Identifiers**](uiauto-textattribute-ids.md) for notes regarding version support.</span></span>

 

<span data-ttu-id="752fa-121">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="752fa-121">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="752fa-122">Atributos de anotación</span><span class="sxs-lookup"><span data-stu-id="752fa-122">Annotation Attributes</span></span>](#annotation-attributes)
-   [<span data-ttu-id="752fa-123">Atributos de fuente</span><span class="sxs-lookup"><span data-stu-id="752fa-123">Font Attributes</span></span>](#font-attributes)
-   [<span data-ttu-id="752fa-124">Atributos de lenguaje</span><span class="sxs-lookup"><span data-stu-id="752fa-124">Language Attributes</span></span>](#language-attributes)
-   [<span data-ttu-id="752fa-125">Atributo de vínculo</span><span class="sxs-lookup"><span data-stu-id="752fa-125">Link Attribute</span></span>](#link-attribute)
-   [<span data-ttu-id="752fa-126">Atributos de margen de página</span><span class="sxs-lookup"><span data-stu-id="752fa-126">Page Margin Attributes</span></span>](#page-margin-attributes)
-   [<span data-ttu-id="752fa-127">Atributos de alineación de texto</span><span class="sxs-lookup"><span data-stu-id="752fa-127">Text Alignment Attributes</span></span>](#text-alignment-attributes)
-   [<span data-ttu-id="752fa-128">Atributos de color de texto</span><span class="sxs-lookup"><span data-stu-id="752fa-128">Text Color Attributes</span></span>](#text-color-attributes)
-   [<span data-ttu-id="752fa-129">Atributos de decoración de texto</span><span class="sxs-lookup"><span data-stu-id="752fa-129">Text Decoration Attributes</span></span>](#text-decoration-attributes)
-   [<span data-ttu-id="752fa-130">Atributos de estilo de texto</span><span class="sxs-lookup"><span data-stu-id="752fa-130">Text Style Attributes</span></span>](#text-style-attributes)
-   [<span data-ttu-id="752fa-131">Atributos de interacción y selección</span><span class="sxs-lookup"><span data-stu-id="752fa-131">Interaction and Selection Attributes</span></span>](#interaction-and-selection-attributes)
-   [<span data-ttu-id="752fa-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="752fa-132">Related topics</span></span>](#related-topics)

## <a name="annotation-attributes"></a><span data-ttu-id="752fa-133">Atributos de anotación</span><span class="sxs-lookup"><span data-stu-id="752fa-133">Annotation Attributes</span></span>

<span data-ttu-id="752fa-134">Los objetos Annotation y los tipos de anotación están disponibles a través de los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="752fa-134">Annotation objects and annotation types are available through the following attributes.</span></span>



| <span data-ttu-id="752fa-135">Atributo</span><span class="sxs-lookup"><span data-stu-id="752fa-135">Attribute</span></span>             | <span data-ttu-id="752fa-136">Identificador</span><span class="sxs-lookup"><span data-stu-id="752fa-136">Identifier</span></span>                                                            |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="752fa-137">**AnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="752fa-137">**AnnotationObjects**</span></span> | [<span data-ttu-id="752fa-138">**UIA \_ AnnotationObjectsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-138">**UIA\_AnnotationObjectsAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="752fa-139">**AnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="752fa-139">**AnnotationTypes**</span></span>   | [<span data-ttu-id="752fa-140">**UIA \_ AnnotationTypesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-140">**UIA\_AnnotationTypesAttributeId**</span></span>](uiauto-textattribute-ids.md)   |



 

## <a name="font-attributes"></a><span data-ttu-id="752fa-141">Atributos de fuente</span><span class="sxs-lookup"><span data-stu-id="752fa-141">Font Attributes</span></span>

<span data-ttu-id="752fa-142">El nombre, el tamaño y el peso de una fuente están disponibles a través de los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="752fa-142">The name, size, and weight of a font is available through the following attributes.</span></span>



| <span data-ttu-id="752fa-143">Atributo</span><span class="sxs-lookup"><span data-stu-id="752fa-143">Attribute</span></span>      | <span data-ttu-id="752fa-144">Identificador</span><span class="sxs-lookup"><span data-stu-id="752fa-144">Identifier</span></span>                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="752fa-145">**FontName**</span><span class="sxs-lookup"><span data-stu-id="752fa-145">**FontName**</span></span>   | [<span data-ttu-id="752fa-146">**UIA \_ FontNameAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-146">**UIA\_FontNameAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="752fa-147">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="752fa-147">**FontSize**</span></span>   | [<span data-ttu-id="752fa-148">**UIA \_ FontSizeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-148">**UIA\_FontSizeAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="752fa-149">**FontWeight**</span><span class="sxs-lookup"><span data-stu-id="752fa-149">**FontWeight**</span></span> | [<span data-ttu-id="752fa-150">**UIA \_ FontWeightAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-150">**UIA\_FontWeightAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a><span data-ttu-id="752fa-151">Atributos de lenguaje</span><span class="sxs-lookup"><span data-stu-id="752fa-151">Language Attributes</span></span>

<span data-ttu-id="752fa-152">La información sobre el idioma del texto está disponible a través de los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="752fa-152">Information about the language of the text is available through the following attributes.</span></span>



| <span data-ttu-id="752fa-153">Atributo</span><span class="sxs-lookup"><span data-stu-id="752fa-153">Attribute</span></span>              | <span data-ttu-id="752fa-154">Identificador</span><span class="sxs-lookup"><span data-stu-id="752fa-154">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="752fa-155">**Referencia cultural**</span><span class="sxs-lookup"><span data-stu-id="752fa-155">**Culture**</span></span>            | [<span data-ttu-id="752fa-156">**UIA \_ CultureAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-156">**UIA\_CultureAttributeId**</span></span>](uiauto-textattribute-ids.md)                       |
| <span data-ttu-id="752fa-157">**TextFlowDirections**</span><span class="sxs-lookup"><span data-stu-id="752fa-157">**TextFlowDirections**</span></span> | [<span data-ttu-id="752fa-158">**UIA \_ TextFlowDirectionsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-158">**UIA\_TextFlowDirectionsAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a><span data-ttu-id="752fa-159">Atributo de vínculo</span><span class="sxs-lookup"><span data-stu-id="752fa-159">Link Attribute</span></span>

<span data-ttu-id="752fa-160">El atributo siguiente proporciona el intervalo de texto que es el destino de un vínculo de un documento.</span><span class="sxs-lookup"><span data-stu-id="752fa-160">The following attribute provides the text range that is the target of a link in a document.</span></span>



| <span data-ttu-id="752fa-161">Atributo</span><span class="sxs-lookup"><span data-stu-id="752fa-161">Attribute</span></span> | <span data-ttu-id="752fa-162">Identificador</span><span class="sxs-lookup"><span data-stu-id="752fa-162">Identifier</span></span>                                                                   |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="752fa-163">**Vínculo**</span><span class="sxs-lookup"><span data-stu-id="752fa-163">**Link**</span></span>  | [<span data-ttu-id="752fa-164">**UIA \_ LinkAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-164">**UIA\_LinkAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a><span data-ttu-id="752fa-165">Atributos de margen de página</span><span class="sxs-lookup"><span data-stu-id="752fa-165">Page Margin Attributes</span></span>

<span data-ttu-id="752fa-166">Los rectángulos delimitadores de un intervalo de texto no exponen las coordenadas del texto en la página.</span><span class="sxs-lookup"><span data-stu-id="752fa-166">The bounding rectangles of a text range do not expose the coordinates of the text in the page.</span></span> <span data-ttu-id="752fa-167">Sin embargo, un proveedor puede exponer la información del margen de la página mediante los siguientes atributos de texto.</span><span class="sxs-lookup"><span data-stu-id="752fa-167">However, a provider can expose the page margin information using the following text attributes.</span></span>



| <span data-ttu-id="752fa-168">Atributo</span><span class="sxs-lookup"><span data-stu-id="752fa-168">Attribute</span></span>          | <span data-ttu-id="752fa-169">Identificador</span><span class="sxs-lookup"><span data-stu-id="752fa-169">Identifier</span></span>                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="752fa-170">**MarginBottom**</span><span class="sxs-lookup"><span data-stu-id="752fa-170">**MarginBottom**</span></span>   | [<span data-ttu-id="752fa-171">**UIA \_ MarginBottomAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-171">**UIA\_MarginBottomAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="752fa-172">**MarginLeading**</span><span class="sxs-lookup"><span data-stu-id="752fa-172">**MarginLeading**</span></span>  | [<span data-ttu-id="752fa-173">**UIA \_ MarginLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-173">**UIA\_MarginLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)   |
| <span data-ttu-id="752fa-174">**MarginTop**</span><span class="sxs-lookup"><span data-stu-id="752fa-174">**MarginTop**</span></span>      | [<span data-ttu-id="752fa-175">**UIA \_ MarginTopAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-175">**UIA\_MarginTopAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="752fa-176">**MarginTrailing**</span><span class="sxs-lookup"><span data-stu-id="752fa-176">**MarginTrailing**</span></span> | [<span data-ttu-id="752fa-177">**UIA \_ MarginTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-177">**UIA\_MarginTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a><span data-ttu-id="752fa-178">Atributos de alineación de texto</span><span class="sxs-lookup"><span data-stu-id="752fa-178">Text Alignment Attributes</span></span>

<span data-ttu-id="752fa-179">La información sobre la alineación del texto como la sangría, la configuración de las tabulaciones y la alineación horizontal está disponible a través de los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="752fa-179">Information about text alignment such as indentation, tab settings, and horizontal alignment is available through the following attributes.</span></span>



| <span data-ttu-id="752fa-180">Atributo</span><span class="sxs-lookup"><span data-stu-id="752fa-180">Attribute</span></span>                   | <span data-ttu-id="752fa-181">Identificador</span><span class="sxs-lookup"><span data-stu-id="752fa-181">Identifier</span></span>                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="752fa-182">**HorizontalTextAlignment**</span><span class="sxs-lookup"><span data-stu-id="752fa-182">**HorizontalTextAlignment**</span></span> | [<span data-ttu-id="752fa-183">**UIA \_ HorizontalTextAlignmentAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-183">**UIA\_HorizontalTextAlignmentAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="752fa-184">**IndentationFirstLine**</span><span class="sxs-lookup"><span data-stu-id="752fa-184">**IndentationFirstLine**</span></span>    | [<span data-ttu-id="752fa-185">**UIA \_ IndentationFirstLineAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-185">**UIA\_IndentationFirstLineAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="752fa-186">**IndentationLeading**</span><span class="sxs-lookup"><span data-stu-id="752fa-186">**IndentationLeading**</span></span>      | [<span data-ttu-id="752fa-187">**UIA \_ IndentationLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-187">**UIA\_IndentationLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="752fa-188">**IndentationTrailing**</span><span class="sxs-lookup"><span data-stu-id="752fa-188">**IndentationTrailing**</span></span>     | [<span data-ttu-id="752fa-189">**UIA \_ IndentationTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-189">**UIA\_IndentationTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="752fa-190">**Pestañas**</span><span class="sxs-lookup"><span data-stu-id="752fa-190">**Tabs**</span></span>                    | [<span data-ttu-id="752fa-191">**UIA \_ TabsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-191">**UIA\_TabsAttributeId**</span></span>](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a><span data-ttu-id="752fa-192">Atributos de color de texto</span><span class="sxs-lookup"><span data-stu-id="752fa-192">Text Color Attributes</span></span>

<span data-ttu-id="752fa-193">Los colores de primer plano y de fondo están disponibles a través de los siguientes atributos de texto.</span><span class="sxs-lookup"><span data-stu-id="752fa-193">The foreground and background text colors are available through the following text attributes.</span></span> <span data-ttu-id="752fa-194">Ambos colores se especifican como un tipo de datos [**COLORREF**](/windows/desktop/gdi/colorref) .</span><span class="sxs-lookup"><span data-stu-id="752fa-194">Both colors are specified as a [**COLORREF**](/windows/desktop/gdi/colorref) data type.</span></span>



| <span data-ttu-id="752fa-195">Atributo</span><span class="sxs-lookup"><span data-stu-id="752fa-195">Attribute</span></span>           | <span data-ttu-id="752fa-196">Identificador</span><span class="sxs-lookup"><span data-stu-id="752fa-196">Identifier</span></span>                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="752fa-197">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="752fa-197">**BackgroundColor**</span></span> | [<span data-ttu-id="752fa-198">**UIA \_ BackgroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-198">**UIA\_BackgroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="752fa-199">**ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="752fa-199">**ForegroundColor**</span></span> | [<span data-ttu-id="752fa-200">**UIA \_ ForegroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-200">**UIA\_ForegroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a><span data-ttu-id="752fa-201">Atributos de decoración de texto</span><span class="sxs-lookup"><span data-stu-id="752fa-201">Text Decoration Attributes</span></span>

<span data-ttu-id="752fa-202">Las decoraciones de texto incluyen áreas como viñetas, subrayado y animaciones.</span><span class="sxs-lookup"><span data-stu-id="752fa-202">Text decorations include areas such as bullets, underlining, and animations.</span></span> <span data-ttu-id="752fa-203">Si el texto incluye viñetas o números iniciales, el símbolo o el texto utilizado para la viñeta o el número debe estar incluido en la secuencia de texto, si procede.</span><span class="sxs-lookup"><span data-stu-id="752fa-203">If text includes leading bullets or numbers, the symbol or text used for the bullet or number should be included in the text stream, if applicable.</span></span>

<span data-ttu-id="752fa-204">La información sobre las decoraciones de texto está disponible a través de los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="752fa-204">Information about text decorations is available through the following attributes.</span></span>



| <span data-ttu-id="752fa-205">Atributo</span><span class="sxs-lookup"><span data-stu-id="752fa-205">Attribute</span></span>              | <span data-ttu-id="752fa-206">Identificador</span><span class="sxs-lookup"><span data-stu-id="752fa-206">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="752fa-207">**AnimationStyle**</span><span class="sxs-lookup"><span data-stu-id="752fa-207">**AnimationStyle**</span></span>     | [<span data-ttu-id="752fa-208">**UIA \_ AnimationStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-208">**UIA\_AnimationStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="752fa-209">**BulletStyle**</span><span class="sxs-lookup"><span data-stu-id="752fa-209">**BulletStyle**</span></span>        | [<span data-ttu-id="752fa-210">**UIA \_ BulletStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-210">**UIA\_BulletStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)               |
| <span data-ttu-id="752fa-211">**OutlineStyles**</span><span class="sxs-lookup"><span data-stu-id="752fa-211">**OutlineStyles**</span></span>      | [<span data-ttu-id="752fa-212">**UIA \_ OutlineStylesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-212">**UIA\_OutlineStylesAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="752fa-213">**OverlineColor**</span><span class="sxs-lookup"><span data-stu-id="752fa-213">**OverlineColor**</span></span>      | [<span data-ttu-id="752fa-214">**UIA \_ OverlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-214">**UIA\_OverlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="752fa-215">**OverlineStyle**</span><span class="sxs-lookup"><span data-stu-id="752fa-215">**OverlineStyle**</span></span>      | [<span data-ttu-id="752fa-216">**UIA \_ OverlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-216">**UIA\_OverlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="752fa-217">**StrikethroughColor**</span><span class="sxs-lookup"><span data-stu-id="752fa-217">**StrikethroughColor**</span></span> | [<span data-ttu-id="752fa-218">**UIA \_ StrikethroughColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-218">**UIA\_StrikethroughColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="752fa-219">**StrikethroughStyle**</span><span class="sxs-lookup"><span data-stu-id="752fa-219">**StrikethroughStyle**</span></span> | [<span data-ttu-id="752fa-220">**UIA \_ StrikethroughStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-220">**UIA\_StrikethroughStyleAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="752fa-221">**UnderlineColor**</span><span class="sxs-lookup"><span data-stu-id="752fa-221">**UnderlineColor**</span></span>     | [<span data-ttu-id="752fa-222">**UIA \_ UnderlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-222">**UIA\_UnderlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="752fa-223">**UnderlineStyle**</span><span class="sxs-lookup"><span data-stu-id="752fa-223">**UnderlineStyle**</span></span>     | [<span data-ttu-id="752fa-224">**UIA \_ UnderlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-224">**UIA\_UnderlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a><span data-ttu-id="752fa-225">Atributos de estilo de texto</span><span class="sxs-lookup"><span data-stu-id="752fa-225">Text Style Attributes</span></span>

<span data-ttu-id="752fa-226">La información sobre los estilos de texto está disponible a través de los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="752fa-226">Information about text styles is available though the following attributes.</span></span>



| <span data-ttu-id="752fa-227">Atributo</span><span class="sxs-lookup"><span data-stu-id="752fa-227">Attribute</span></span>         | <span data-ttu-id="752fa-228">Identificador</span><span class="sxs-lookup"><span data-stu-id="752fa-228">Identifier</span></span>                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="752fa-229">**CapStyle**</span><span class="sxs-lookup"><span data-stu-id="752fa-229">**CapStyle**</span></span>      | [<span data-ttu-id="752fa-230">**UIA \_ CapStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-230">**UIA\_CapStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="752fa-231">**IsHidden**</span><span class="sxs-lookup"><span data-stu-id="752fa-231">**IsHidden**</span></span>      | [<span data-ttu-id="752fa-232">**UIA \_ IsHiddenAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-232">**UIA\_IsHiddenAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="752fa-233">**IsItalic**</span><span class="sxs-lookup"><span data-stu-id="752fa-233">**IsItalic**</span></span>      | [<span data-ttu-id="752fa-234">**UIA \_ IsItalicAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-234">**UIA\_IsItalicAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="752fa-235">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="752fa-235">**IsReadOnly**</span></span>    | [<span data-ttu-id="752fa-236">**UIA \_ IsReadOnlyAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-236">**UIA\_IsReadOnlyAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="752fa-237">**IsSuperscript**</span><span class="sxs-lookup"><span data-stu-id="752fa-237">**IsSuperscript**</span></span> | [<span data-ttu-id="752fa-238">**UIA \_ IsSuperscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-238">**UIA\_IsSuperscriptAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="752fa-239">**IsSubscript**</span><span class="sxs-lookup"><span data-stu-id="752fa-239">**IsSubscript**</span></span>   | [<span data-ttu-id="752fa-240">**UIA \_ IsSubscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-240">**UIA\_IsSubscriptAttributeId**</span></span>](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a><span data-ttu-id="752fa-241">Atributos de interacción y selección</span><span class="sxs-lookup"><span data-stu-id="752fa-241">Interaction and Selection Attributes</span></span>

<span data-ttu-id="752fa-242">La información sobre la selección de texto actual en el intervalo y el estado de foco está disponible a través de los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="752fa-242">Information about current text selection in the range and focus state is available though the following attributes.</span></span>



| <span data-ttu-id="752fa-243">Atributo</span><span class="sxs-lookup"><span data-stu-id="752fa-243">Attribute</span></span>              | <span data-ttu-id="752fa-244">Identificador</span><span class="sxs-lookup"><span data-stu-id="752fa-244">Identifier</span></span>                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="752fa-245">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="752fa-245">**IsActive**</span></span>           | [<span data-ttu-id="752fa-246">**UIA \_ IsActiveAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-246">**UIA\_IsActiveAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="752fa-247">**SelectionActiveEnd**</span><span class="sxs-lookup"><span data-stu-id="752fa-247">**SelectionActiveEnd**</span></span> | [<span data-ttu-id="752fa-248">**UIA \_ SelectionActiveEndAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-248">**UIA\_SelectionActiveEndAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="752fa-249">**CaretPosition**</span><span class="sxs-lookup"><span data-stu-id="752fa-249">**CaretPosition**</span></span>      | [<span data-ttu-id="752fa-250">**UIA \_ CaretPositionAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-250">**UIA\_CaretPositionAttributeId**</span></span>](uiauto-textattribute-ids.md)      |
| <span data-ttu-id="752fa-251">**CaretBidiMode**</span><span class="sxs-lookup"><span data-stu-id="752fa-251">**CaretBidiMode**</span></span>      | [<span data-ttu-id="752fa-252">**UIA \_ CaretBidiModeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="752fa-252">**UIA\_CaretBidiModeAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a><span data-ttu-id="752fa-253">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="752fa-253">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="752fa-254">**Vista**</span><span class="sxs-lookup"><span data-stu-id="752fa-254">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="752fa-255">Acerca de los patrones de control Text y TextRange de UI Automation</span><span class="sxs-lookup"><span data-stu-id="752fa-255">About the UI Automation Text and TextRange Control Patterns</span></span>](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[<span data-ttu-id="752fa-256">Patrones de control Text y TextRange</span><span class="sxs-lookup"><span data-stu-id="752fa-256">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="752fa-257">Trabajar con controles basados en texto</span><span class="sxs-lookup"><span data-stu-id="752fa-257">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 