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
# <a name="ui-automation-text-attributes"></a>Atributos de texto de automatización de la interfaz de usuario

En este tema se describe cómo la automatización de la interfaz de usuario de Microsoft expone el formato y las propiedades de estilo (*atributos de texto*) de contenido textual y proporciona una lista de atributos de texto admitidos.

Los proveedores de automatización de la interfaz de usuario exponen atributos de texto a través de los métodos [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) y [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) del patrón de control [TextRange](uiauto-about-text-and-textrange-patterns.md) . Las aplicaciones cliente usan el método [**IUIAutomationTextRange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) para recuperar el valor de un atributo de texto determinado para un intervalo de texto. Los clientes pueden usar el método [**IUIAutomationTextRange:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) para buscar texto en un intervalo de texto que tiene un atributo determinado. Si se encuentra cualquier texto coincidente, el método crea un nuevo intervalo de texto que contiene el texto coincidente.

El patrón de control **TextRange** admite los atributos de texto de la lista siguiente. Los nombres de atributo se derivan de los identificadores de atributo de texto de automatización de la interfaz de usuario. Por ejemplo, el atributo **AnimationStyle** lo identifican los clientes como [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definido en Uiautomationclient. h) y los proveedores como **Text \_ AnimationStyle \_ Attribute \_ GUID** (definido en Uiautomationcoreapi. h). Para obtener más información sobre cada atributo de texto compatible, vea [**identificadores de atributos de texto**](uiauto-textattribute-ids.md).

> [!Note]  
> Algunos de los atributos enumerados se admiten a partir de Windows 8. Vea [**identificadores de atributos de texto**](uiauto-textattribute-ids.md) para las notas relacionadas con la compatibilidad de versiones.

 

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

Los objetos Annotation y los tipos de anotación están disponibles a través de los siguientes atributos.



| Atributo             | Identificador                                                            |
|-----------------------|-----------------------------------------------------------------------|
| **AnnotationObjects** | [**UIA \_ AnnotationObjectsAttributeId**](uiauto-textattribute-ids.md) |
| **AnnotationTypes**   | [**UIA \_ AnnotationTypesAttributeId**](uiauto-textattribute-ids.md)   |



 

## <a name="font-attributes"></a>Atributos de fuente

El nombre, el tamaño y el peso de una fuente están disponibles a través de los siguientes atributos.



| Atributo      | Identificador                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| **FontName**   | [**UIA \_ FontNameAttributeId**](uiauto-textattribute-ids.md)     |
| **FontSize**   | [**UIA \_ FontSizeAttributeId**](uiauto-textattribute-ids.md)     |
| **FontWeight** | [**UIA \_ FontWeightAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a>Atributos de lenguaje

La información sobre el idioma del texto está disponible a través de los siguientes atributos.



| Atributo              | Identificador                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **Referencia cultural**            | [**UIA \_ CultureAttributeId**](uiauto-textattribute-ids.md)                       |
| **TextFlowDirections** | [**UIA \_ TextFlowDirectionsAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a>Atributo de vínculo

El atributo siguiente proporciona el intervalo de texto que es el destino de un vínculo de un documento.



| Atributo | Identificador                                                                   |
|-----------|------------------------------------------------------------------------------|
| **Vínculo**  | [**UIA \_ LinkAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a>Atributos de margen de página

Los rectángulos delimitadores de un intervalo de texto no exponen las coordenadas del texto en la página. Sin embargo, un proveedor puede exponer la información del margen de la página mediante los siguientes atributos de texto.



| Atributo          | Identificador                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| **MarginBottom**   | [**UIA \_ MarginBottomAttributeId**](uiauto-textattribute-ids.md)     |
| **MarginLeading**  | [**UIA \_ MarginLeadingAttributeId**](uiauto-textattribute-ids.md)   |
| **MarginTop**      | [**UIA \_ MarginTopAttributeId**](uiauto-textattribute-ids.md)           |
| **MarginTrailing** | [**UIA \_ MarginTrailingAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a>Atributos de alineación de texto

La información sobre la alineación del texto como la sangría, la configuración de las tabulaciones y la alineación horizontal está disponible a través de los siguientes atributos.



| Atributo                   | Identificador                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| **HorizontalTextAlignment** | [**UIA \_ HorizontalTextAlignmentAttributeId**](uiauto-textattribute-ids.md) |
| **IndentationFirstLine**    | [**UIA \_ IndentationFirstLineAttributeId**](uiauto-textattribute-ids.md)       |
| **IndentationLeading**      | [**UIA \_ IndentationLeadingAttributeId**](uiauto-textattribute-ids.md)           |
| **IndentationTrailing**     | [**UIA \_ IndentationTrailingAttributeId**](uiauto-textattribute-ids.md)         |
| **Pestañas**                    | [**UIA \_ TabsAttributeId**](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a>Atributos de color de texto

Los colores de primer plano y de fondo están disponibles a través de los siguientes atributos de texto. Ambos colores se especifican como un tipo de datos [**COLORREF**](/windows/desktop/gdi/colorref) .



| Atributo           | Identificador                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| **BackgroundColor** | [**UIA \_ BackgroundColorAttributeId**](uiauto-textattribute-ids.md) |
| **ForegroundColor** | [**UIA \_ ForegroundColorAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a>Atributos de decoración de texto

Las decoraciones de texto incluyen áreas como viñetas, subrayado y animaciones. Si el texto incluye viñetas o números iniciales, el símbolo o el texto utilizado para la viñeta o el número debe estar incluido en la secuencia de texto, si procede.

La información sobre las decoraciones de texto está disponible a través de los siguientes atributos.



| Atributo              | Identificador                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **AnimationStyle**     | [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md)         |
| **BulletStyle**        | [**UIA \_ BulletStyleAttributeId**](uiauto-textattribute-ids.md)               |
| **OutlineStyles**      | [**UIA \_ OutlineStylesAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineColor**      | [**UIA \_ OverlineColorAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineStyle**      | [**UIA \_ OverlineStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **StrikethroughColor** | [**UIA \_ StrikethroughColorAttributeId**](uiauto-textattribute-ids.md) |
| **StrikethroughStyle** | [**UIA \_ StrikethroughStyleAttributeId**](uiauto-textattribute-ids.md) |
| **UnderlineColor**     | [**UIA \_ UnderlineColorAttributeId**](uiauto-textattribute-ids.md)         |
| **UnderlineStyle**     | [**UIA \_ UnderlineStyleAttributeId**](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a>Atributos de estilo de texto

La información sobre los estilos de texto está disponible a través de los siguientes atributos.



| Atributo         | Identificador                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| **CapStyle**      | [**UIA \_ CapStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **IsHidden**      | [**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)           |
| **IsItalic**      | [**UIA \_ IsItalicAttributeId**](uiauto-textattribute-ids.md)           |
| **IsReadOnly**    | [**UIA \_ IsReadOnlyAttributeId**](uiauto-textattribute-ids.md)       |
| **IsSuperscript** | [**UIA \_ IsSuperscriptAttributeId**](uiauto-textattribute-ids.md) |
| **IsSubscript**   | [**UIA \_ IsSubscriptAttributeId**](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a>Atributos de interacción y selección

La información sobre la selección de texto actual en el intervalo y el estado de foco está disponible a través de los siguientes atributos.



| Atributo              | Identificador                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| **IsActive**           | [**UIA \_ IsActiveAttributeId**](uiauto-textattribute-ids.md)           |
| **SelectionActiveEnd** | [**UIA \_ SelectionActiveEndAttributeId**](uiauto-textattribute-ids.md) |
| **CaretPosition**      | [**UIA \_ CaretPositionAttributeId**](uiauto-textattribute-ids.md)      |
| **CaretBidiMode**      | [**UIA \_ CaretBidiModeAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Acerca de los patrones de control Text y TextRange de UI Automation](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[Patrones de control Text y TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 