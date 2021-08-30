---
title: Tipo de control Text
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Text.
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control Text
- Automatización de la interfaz de usuario, tipo de control Text
- Automatización de la interfaz de usuario,tree structure for Text control type
- Automatización de la interfaz de usuario,properties para el tipo de control Text
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Text
- Automatización de la interfaz de usuario,events para el tipo de control Text
- tree structures,Text control type
- properties,Tipo de control Text
- patrones de control, tipo de control Text
- events,Text (tipo de control)
- compatibilidad con el tipo de control Text
- Text (tipo de control)
- tipos de control, estructura de árbol para tipo de control Text
- tipos de control, patrones de control para el tipo de control Text
- tipos de control, compatibilidad con texto
- tipos de control,Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc109bfba35f995384447014bc6642dcf3cd7f4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478801"
---
# <a name="text-control-type"></a>Tipo de control Text

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo **de** control Text.

Un control de texto es un elemento básico de la interfaz de usuario que representa un fragmento de texto en la pantalla.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el **tipo de** control Text. Los Automatización de la interfaz de usuario se aplican a todos los controles de árbol en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol de Automatización de la interfaz de usuario que pertenece a los controles de texto y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Texto</li></ul> | <ul><li>Texto (si hay contenido)</li></ul> | 




 

Un control de texto se puede usar solo como una etiqueta o como texto estático en un formulario. También se puede contener dentro de la estructura de uno de los siguientes elementos:

-   [DataItem](uiauto-supportdataitemcontroltype.md)
-   [ListItem](uiauto-supportlistitemcontroltype.md)
-   [TreeItem](uiauto-supporttreeitemcontroltype.md)

Es posible que los controles de texto no aparezcan en la vista de contenido del árbol de Automatización de la interfaz de usuario porque el texto se muestra a menudo a través de la propiedad **Name** de otro control. Por ejemplo, el texto utilizado para etiquetar un control de cuadro combinado se expone a través de la propiedad **Name del** control. Dado que el control de cuadro combinado está en la vista de contenido del Automatización de la interfaz de usuario, el control de texto no necesita estar ahí. Los controles de texto pueden tener secundarios en la vista de contenido si hay un objeto incrustado, como un hipervínculo.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de texto. Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor      | Notas                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                            |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic.                                                                                                                                                |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Texto**   |                                                                                                                                                                                                                                                                                                                                                     |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | Depende    | El control de texto es contenido si contiene información no expuesta en la propiedad Name de otro control.                                                                                                                                                                                                                                              |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | El control de texto siempre debe ser un control.                                                                                                                                                                                                                                                                                                          |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                                                           |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | Los controles de texto no tienen una etiqueta de texto estático.                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo **de** control Text. El valor predeterminado es "text" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                      |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El nombre de un control de texto puede ser el texto que muestra. Sin embargo, si el control también admite el patrón [Text](uiauto-implementingtextandtextrange.md) y el texto es amplio, no use el contenido de texto completo como valor **de** Nombre. En su lugar, **proporcione un valor** De nombre más corto, derivado de otras propiedades del control. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con los controles de texto. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico | Notas                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Depende | Si el control de texto se encuentra dentro de un control de tabla, se debe admite el patrón de control [GridItem.](uiauto-implementinggriditem.md)                                                                                                                            |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Depende | Si el control de texto se encuentra dentro de un control de tabla, se debe admite el patrón de control [TableItem.](uiauto-implementingtableitem.md)                                                                                                                          |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | Depende | El texto debe admitir el [patrón de](uiauto-implementingtextandtextrange.md) control Texto para mejorar la accesibilidad; sin embargo, no es necesario. El patrón de control Text es útil cuando el texto tiene atributos y estilo enriquecidos (por ejemplo, color, negrita y cursiva). |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | Nunca   | Un control de texto nunca admite el [patrón de](uiauto-implementingvalue.md) control Valor. Si el texto se puede editar, es el tipo de control [Editar.](uiauto-supporteditcontroltype.md)                                                                                    |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de texto son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad NamePropertyId.**](uiauto-automation-element-propids.md)                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**Texto de UIA \_ \_ TextChangedEventId**](uiauto-event-ids.md)                                                 | Si el control admite el patrón de control [Text,](uiauto-implementingtextandtextrange.md) debe admitir este evento.   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




