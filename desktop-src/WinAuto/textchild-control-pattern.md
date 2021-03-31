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
# <a name="textchild-control-pattern"></a>Patrón de control TextChild

Presenta directrices y convenciones para implementar [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), incluida información sobre propiedades y métodos. El patrón de control **TextChild** se usa para tener acceso al antecesor más cercano de un elemento que admite el patrón de control [Text](uiauto-implementingtextandtextrange.md) .

Por ejemplo, supongamos que el texto de un documento contiene una imagen incrustada y un hipervínculo, tal como se muestra en la siguiente imagen.

![captura de pantalla que muestra texto que contiene una imagen incrustada y un hipervínculo](images/textchild-pattern.png)

Si usa las herramientas de automatización de la interfaz de usuario de Microsoft para examinar el árbol de automatización de la interfaz de usuario para este contenido de documento, podría mostrar un elemento de documento con un elemento secundario que represente la imagen y otro elemento secundario que represente el hipervínculo. Por ejemplo:

![captura de pantalla que muestra inspeccionar un árbol de elementos de automatización de la interfaz de usuario de ejemplo](images/textchild-pattern-tree.png)

Normalmente, el elemento de documento en el ejemplo anterior admite el patrón de control [Text](uiauto-implementingtextandtextrange.md) , pero no los dos elementos secundarios del elemento de documento. Si una aplicación cliente de automatización de la interfaz de usuario tiene una referencia al elemento de imagen o al elemento de hipervínculo, el cliente puede usar el patrón de control **TextChild** como una manera cómoda de tener acceso al patrón TextControl expuesto por el elemento de documento que lo contiene.

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar la interfaz [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) , tenga en cuenta las siguientes directrices y convenciones:

-   La propiedad [**ITextChildProvider:: TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) debe especificar el elemento antecesor más cercano que admita la interfaz [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) , independientemente de si los elementos situados más arriba en la cadena antecesor también admiten **ITextProvider**.
-   Un elemento no debe ser compatible con la interfaz [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) y [ITextChildProvider * *](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .
- Un elemento que implementa [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) debe ser un elemento secundario, o descendiente, de un elemento que implemente [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider). No es necesario que este elemento también implemente el [patrón de control Text](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).
-   La propiedad [**ITextChildProvider:: TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) debe especificar el mismo intervalo de texto que el que devuelve el elemento del proveedor de texto que contiene cuando se llama a la función [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) con el elemento secundario text como el elemento secundario incluido.

## <a name="required-members-for-itextchildprovider"></a>Miembros requeridos para **ITextChildProvider**

Estas propiedades y métodos son necesarios para implementar la interfaz [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .



| Miembros requeridos                                                     | Tipo de miembro | Notas |
|----------------------------------------------------------------------|-------------|-------|
| [**TextContainer**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | Propiedad    | None  |
| [**TextRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | Propiedad    | None  |



 

Este patrón de control no tiene métodos o propiedades asociados.

## <a name="related-topics"></a>Temas relacionados

**Vista**

- [Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
- [Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
- [Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)