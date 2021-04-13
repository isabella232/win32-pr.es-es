---
title: Text (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Text.
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Text
- Automatización de la interfaz de usuario, tipo de control Text
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Text
- Automatización de la interfaz de usuario, propiedades para el tipo de control Text
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Text
- Automatización de la interfaz de usuario, eventos para el tipo de control Text
- estructuras de árbol, tipo de control Text
- propiedades, Text (tipo de control)
- patrones de control, Text (tipo de control)
- Events, Text (tipo de control)
- compatibilidad con el tipo de control Text
- Text (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Text
- tipos de control, patrones de control para el tipo de control Text
- tipos de control, compatibilidad con texto
- tipos de control, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902b3c7c523417abde2c60e1f8039ad9f2c322b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357378"
---
# <a name="text-control-type"></a>Text (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Text** .

Un control de texto es un elemento básico de la interfaz de usuario que representa un fragmento de texto en la pantalla.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Text** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de árbol donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de texto y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vista de control</th>
<th>Vista de contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Texto</li>
</ul></td>
<td><ul>
<li>Texto (si hay contenido)</li>
</ul></td>
</tr>
</tbody>
</table>



 

Un control de texto se puede usar solo como una etiqueta o como texto estático en un formulario. También puede estar dentro de la estructura de uno de los siguientes elementos:

-   [DataItem](uiauto-supportdataitemcontroltype.md)
-   [ListItem](uiauto-supportlistitemcontroltype.md)
-   [TreeItem](uiauto-supporttreeitemcontroltype.md)

Es posible que los controles de texto no aparezcan en la vista de contenido del árbol de automatización de la interfaz de usuario porque el texto se muestra a menudo a través de la propiedad **Name** de otro control. Por ejemplo, el texto que se usa para etiquetar un control de cuadro combinado se expone a través de la propiedad **Name** del control. Dado que el control de cuadro combinado está en la vista de contenido del árbol de automatización de la interfaz de usuario, no es necesario que el control de texto esté ahí. Los controles de texto pueden tener elementos secundarios en la vista de contenido si hay un objeto incrustado, como un hipervínculo.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de texto. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                            |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Se admite si hay un rectángulo delimitador. Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Texto**   |                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | Depende    | El control de texto es contenido si contiene información no expuesta en la propiedad nombre de otro control.                                                                                                                                                                                                                                              |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control de texto siempre debe ser un control.                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                                                           |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | Los controles de texto no tienen una etiqueta de texto estático.                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **Text** . El valor predeterminado es "Text" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El nombre de un control de texto puede ser el texto que muestra. Sin embargo, si el control también admite el patrón de [texto](uiauto-implementingtextandtextrange.md) y el texto es extensivo, no use el contenido de texto completo como valor de **nombre** . En su lugar, proporcione un valor de **nombre** que sea más corto, derivado de otras propiedades del control. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se muestran los patrones de control de UI Automation que deben admitir los controles de texto. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico | Notas                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Depende | Si el control de texto está contenido dentro de un control de tabla, se debe admitir el patrón de control [GridItem](uiauto-implementinggriditem.md) .                                                                                                                            |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Depende | Si el control de texto está contenido dentro de un control de tabla, se debe admitir el patrón de control [TableItem](uiauto-implementingtableitem.md) .                                                                                                                          |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | Depende | El texto debe admitir el patrón de control [Text](uiauto-implementingtextandtextrange.md) para mejorar la accesibilidad; sin embargo, no es necesario. El patrón de control Text es útil cuando el texto tiene atributos y estilo enriquecidos (por ejemplo, color, negrita y cursiva). |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | Nunca   | Un control de texto nunca admite el patrón de control [Value](uiauto-implementingvalue.md) . Si el texto es editable, es el tipo de control [Edit](uiauto-supporteditcontroltype.md) .                                                                                    |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de texto deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**\_TextChangedEventId de texto de UIA \_**](uiauto-event-ids.md)                                                 | Si el control admite el patrón de control [Text](uiauto-implementingtextandtextrange.md) , debe admitir este evento.   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




