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
# <a name="value-control-pattern"></a>Value (patrón de control)

Describe las directrices y convenciones para implementar [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), incluida información sobre propiedades y métodos. El patrón de control **Value** se usa para admitir controles que tienen un valor intrínseco que no abarca un intervalo y que se puede representar como una cadena.

La cadena de valor puede ser editable, dependiendo del control y su configuración. Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IValueProvider**](#required-members-for-ivalueprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Value** , tenga en cuenta las siguientes directrices y convenciones:

-   Los controles como un elemento de lista o un elemento de árbol deben admitir el patrón de control **Value** si el valor de cualquiera de los elementos es editable, independientemente del modo de edición actual del control. El control primario también debe admitir el patrón de control **Value** si los elementos secundarios son editables. La imagen siguiente muestra un ejemplo de un elemento de lista modificable.

    ![Ilustración donde se muestra el elemento de lista modificable](images/uia-valuepattern-editable-listitem.jpg)

- Los controles de edición de una y varias líneas deben implementar [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) para exponer su contenido de solo lectura.
- Los controles de edición de varias líneas deben implementar [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) si su contenido se puede cambiar.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) no admite la recuperación de la información de formato o los valores de subcadena. Implemente [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) en estos escenarios.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) debe implementarse mediante controles como el control de selección del selector de colores de Microsoft Word (vea la imagen siguiente), que admite la asignación de cadenas entre un valor de color (por ejemplo, "amarillo") y un valor [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) interno equivalente.

    ![Ilustración que muestra la asignación de cadena de muestrario de colores](images/uia-valuepattern-colorpicker.jpg)

- Un control debe tener su propiedad **IsEnabled** establecida en **true** y su propiedad [**ITextProvider:: IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) establecida en **false** antes de permitir una llamada a [**ITextProvider:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).

## <a name="required-members-for-ivalueprovider"></a>Miembros requeridos para **IValueProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) .



| Miembros requeridos                                       | Tipo de miembro | Notas |
|--------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | Propiedad    | None  |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | Propiedad    | None  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | Método      | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Patrones de control Text y TextRange](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 