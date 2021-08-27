---
title: Automatización de la interfaz de usuario de texto
description: En este tema se describe cómo Microsoft Automatización de la interfaz de usuario expone las propiedades de formato y estilo (atributos de texto) del contenido textual y proporciona una lista de atributos de texto admitidos.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- Automatización de la interfaz de usuario,atributos de texto
- atributos de texto, acerca de
- atributos de texto, tipos de variante
- atributos de texto, tipos de datos
- Automatización de la interfaz de usuario,lista de atributos
- Automatización de la interfaz de usuario,lista de atributos de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875cad20285cf38c06ab3363be5bc9aee641c2ce42ae4caff5b091cf1a79c63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118824627"
---
# <a name="ui-automation-text-attributes"></a>Automatización de la interfaz de usuario de texto

En este tema se describe cómo Microsoft Automatización de la interfaz de usuario expone las propiedades de formato y estilo *(atributos* de texto) del contenido textual y proporciona una lista de atributos de texto admitidos.

Automatización de la interfaz de usuario proveedores exponen atributos de texto a través de los [**métodos GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) y [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) del patrón de control [TextRange.](uiauto-about-text-and-textrange-patterns.md) Las aplicaciones cliente usan [**el método IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) para recuperar el valor de un atributo de texto determinado para un intervalo de texto. Los clientes pueden usar [**el método IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) para buscar texto en un intervalo de texto que tenga un atributo determinado. Si se encuentra algún texto que coincida, el método crea un nuevo intervalo de texto que contiene el texto correspondiente.

El patrón de control **TextRange** admite los atributos de texto de la lista siguiente. Los nombres de atributo se derivan de los Automatización de la interfaz de usuario de atributo de texto. Por ejemplo, los clientes identifican el atributo **AnimationStyle** como [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definido en Uiautomationclient.h) y por los proveedores como **TEXT \_ AnimationStyle \_ Attribute \_ GUID** (definido en Uiautomationcoreapi.h). Para obtener más información sobre cada atributo de texto admitido, vea [**Identificadores de atributo de texto**](uiauto-textattribute-ids.md).

> [!Note]  
> Algunos de los atributos enumerados se admiten a partir de Windows 8. Consulte [**Identificadores de atributo de texto para**](uiauto-textattribute-ids.md) obtener notas sobre la compatibilidad con versiones.

 

Este tema contiene las siguientes secciones:

-   [Atributos de anotación](#annotation-attributes)
-   [Atributos de fuente](#font-attributes)
-   [Atributos de lenguaje](#language-attributes)
-   [Atributo de vínculo](#link-attribute)
-   [Atributos de margen de página](#page-margin-attributes)
-   [Atributos de alineación de texto](#text-alignment-attributes)
-   [Atributos de color de texto](#text-color-attributes)
-   [Atributos de decoración de texto](#text-decoration-attributes)
-   [Atributos de estilo de texto](#text-style-attributes)
-   [Atributos de interacción y selección](#interaction-and-selection-attributes)
-   [Temas relacionados](#related-topics)

## <a name="annotation-attributes"></a>Atributos de anotación

Los objetos de anotación y los tipos de anotación están disponibles a través de los atributos siguientes.



| Atributo             | Identificador                                                            |
|-----------------------|-----------------------------------------------------------------------|
| **AnnotationObjects** | [**AnnotationObjectsAttributeId de UIA \_**](uiauto-annotation-type-identifiers.md) |
| **AnnotationTypes**   | [**AnnotationTypesAttributeId de UIA \_**](uiauto-annotation-type-identifiers.md)   |



 

## <a name="font-attributes"></a>Atributos de fuente

El nombre, el tamaño y el peso de una fuente están disponibles a través de los atributos siguientes.



| Atributo      | Identificador                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| **FontName**   | [**UIA \_ FontNameAttributeId**](uiauto-textattribute-ids.md)     |
| **FontSize**   | [**UIA \_ FontSizeAttributeId**](uiauto-textattribute-ids.md)     |
| **FontWeight** | [**FontWeightAttributeId de UIA \_**](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a>Atributos de lenguaje

La información sobre el idioma del texto está disponible a través de los atributos siguientes.



| Atributo              | Identificador                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **Referencia cultural**            | [**CultureAttributeId de UIA \_**](uiauto-textattribute-ids.md)                       |
| **TextFlowDirections** | [**UIA \_ TextFlowDirectionsAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a>Atributo de vínculo

El atributo siguiente proporciona el intervalo de texto que es el destino de un vínculo en un documento.



| Atributo | Identificador                                                                   |
|-----------|------------------------------------------------------------------------------|
| **Vínculo**  | [**LinkAttributeId de UIA \_**](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a>Atributos de margen de página

Los rectángulos delimitadores de un intervalo de texto no exponen las coordenadas del texto de la página. Sin embargo, un proveedor puede exponer la información de margen de página mediante los siguientes atributos de texto.



| Atributo          | Identificador                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| **MarginBottom**   | [**UIA \_ MarginBottomAttributeId**](uiauto-textattribute-ids.md)     |
| **MarginLeading**  | [**UIA \_ MarginLeadingAttributeId**](uiauto-textattribute-ids.md)   |
| **MarginTop**      | [**UIA \_ MarginTopAttributeId**](uiauto-textattribute-ids.md)           |
| **MarginTrailing** | [**UIA \_ MarginTrailingAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a>Atributos de alineación de texto

La información sobre la alineación de texto, como la sangría, la configuración de tabulación y la alineación horizontal, está disponible a través de los atributos siguientes.



| Atributo                   | Identificador                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| **HorizontalTextAlignment** | [**UIA \_ HorizontalTextAlignmentAttributeId**](uiauto-textattribute-ids.md) |
| **IndentationFirstLine**    | [**IndentationFirstLineAttributeId de UIA \_**](uiauto-textattribute-ids.md)       |
| **IndentationLeading**      | [**\_IndentationLeadingAttributeId de UIA**](uiauto-textattribute-ids.md)           |
| **IndentationTrailing**     | [**IndentationTrailingAttributeId de UIA \_**](uiauto-textattribute-ids.md)         |
| **Pestañas**                    | [**Pestañas \_ de UIAAttributeId**](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a>Atributos de color de texto

Los colores de texto de primer plano y de fondo están disponibles a través de los siguientes atributos de texto. Ambos colores se especifican como un [**tipo de datos COLORREF.**](/windows/desktop/gdi/colorref)



| Atributo           | Identificador                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| **BackgroundColor** | [**BackgroundColorAttributeId de UIA \_**](uiauto-textattribute-ids.md) |
| **ForegroundColor** | [**UIA \_ ForegroundColorAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a>Atributos de decoración de texto

Las decoracións de texto incluyen áreas como viñetas, líneas de texto y animaciones. Si el texto incluye viñetas o números iniciales, el símbolo o texto que se usa para la viñeta o el número debe incluirse en la secuencia de texto, si procede.

La información sobre las decoración de texto está disponible a través de los atributos siguientes.



| Atributo              | Identificador                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **AnimationStyle**     | [**AnimationStyleAttributeId de UIA \_**](uiauto-textattribute-ids.md)         |
| **BulletStyle**        | [**UIA \_ BulletStyleAttributeId**](uiauto-textattribute-ids.md)               |
| **OutlineStyles**      | [**UIA \_ OutlineStylesAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineColor**      | [**UIA \_ OverlineColorAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineStyle**      | [**UIA \_ OverlineStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **StrikethroughColor** | [**UIA \_ StrikethroughColorAttributeId**](uiauto-textattribute-ids.md) |
| **StrikethroughStyle** | [**UIA \_ StrikethroughStyleAttributeId**](uiauto-textattribute-ids.md) |
| **UnderlineColor**     | [**UIA \_ UnderlineColorAttributeId**](uiauto-textattribute-ids.md)         |
| **UnderlineStyle**     | [**UIA \_ UnderlineStyleAttributeId**](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a>Atributos de estilo de texto

La información sobre los estilos de texto está disponible a través de los atributos siguientes.



| Atributo         | Identificador                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| **CapStyle**      | [**CapStyleAttributeId de UIA \_**](uiauto-textattribute-ids.md)           |
| **IsHidden**      | [**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)           |
| **IsItalic**      | [**UIA \_ IsItalicAttributeId**](uiauto-textattribute-ids.md)           |
| **IsReadOnly**    | [**IsReadOnlyAttributeId de UIA \_**](uiauto-textattribute-ids.md)       |
| **IsSuperscript** | [**IsSuperscriptAttributeId de UIA \_**](uiauto-textattribute-ids.md) |
| **IsSubscript**   | [**IsSubscriptAttributeId de UIA \_**](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a>Atributos de interacción y selección

La información sobre la selección de texto actual en el intervalo y el estado del foco está disponible a través de los atributos siguientes.



| Atributo              | Identificador                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| **IsActive**           | [**IsActiveAttributeId de UIA \_**](uiauto-textattribute-ids.md)           |
| **SelectionActiveEnd** | [**UIA \_ SelectionActiveEndAttributeId**](uiauto-textattribute-ids.md) |
| **CaretPosition**      | [**CaretPositionAttributeId de UIA \_**](uiauto-textattribute-ids.md)      |
| **CaretBidiMode**      | [**\_CaretBidiModeAttributeId de UIA**](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Acerca de los Automatización de la interfaz de usuario de control Text y TextRange](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[Patrones de control Text y TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 