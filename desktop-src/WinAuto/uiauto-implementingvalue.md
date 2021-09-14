---
title: Patrón de control de valores
description: Describe directrices y convenciones para implementar IValueProvider, incluida información sobre propiedades y métodos.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control Valor
- Automatización de la interfaz de usuario,patrón de control Valor
- Automatización de la interfaz de usuario,IValueProvider
- IValueProvider
- implementar patrones Automatización de la interfaz de usuario control Value
- Patrones de control de valores
- patrones de control,IValueProvider
- patrones de control, implementar Automatización de la interfaz de usuario valor
- patrones de control,Valor
- interfaces,IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40633a21fdd6b59a2aa35c34258037582a647f05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359256"
---
# <a name="value-control-pattern"></a>Patrón de control de valores

Describe directrices y convenciones para implementar [**IValueProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)incluida información sobre propiedades y métodos. El **patrón de** control Valor se usa para admitir controles que tienen un valor intrínseco que no abarca un intervalo y que se puede representar como una cadena.

La cadena de valor puede ser editable, según el control y su configuración. Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y Sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **IValueProvider**](#required-members-for-ivalueprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón **de** control Valor, tenga en cuenta las siguientes directrices y convenciones:

-   Los controles como un elemento de lista o un elemento de árbol deben admitir el patrón de **control** Valor si el valor de cualquiera de los elementos es editable, independientemente del modo de edición actual del control. El control primario también debe admitir el patrón de control **Valor** si los elementos secundarios son editables. En la imagen siguiente se muestra un ejemplo de un elemento de lista modificable.

    ![ilustración en la que se muestra un elemento de lista editable](images/uia-valuepattern-editable-listitem.jpg)

- Los controles de edición de una y varias líneas deben implementar [**ITextProvider para**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) exponer su contenido de solo lectura.
- Los controles de edición de varias líneas deben implementar [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) si se puede cambiar su contenido.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) no admite la recuperación de información de formato o valores de subcadena. Implemente [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) en estos escenarios.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) debe implementarse mediante controles como el control de selección del selector de colores de Microsoft Word (vea la imagen siguiente), que admite la asignación de cadenas entre un valor de color (por ejemplo, "amarillo") y un valor [RGB interno equivalente.](/windows/win32/api/wingdi/nf-wingdi-rgb)

    ![ilustración que muestra la asignación de cadenas de muestra de color](images/uia-valuepattern-colorpicker.jpg)

- Un control debe tener su propiedad **IsEnabled** establecida en **TRUE** y su propiedad [**ITextProvider::IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) establecida en **FALSE** antes de permitir una llamada a [**ITextProvider::SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).

## <a name="required-members-for-ivalueprovider"></a>Miembros necesarios para **IValueProvider**

Las siguientes propiedades y métodos son necesarios para implementar la [**interfaz IValueProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)



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

 

 