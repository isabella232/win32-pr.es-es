---
title: Tipo de control Tab
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Tab.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Tab
- Automatización de la interfaz de usuario,tipo de control Tab
- Automatización de la interfaz de usuario,estructura de árbol para el tipo de control Tab
- Automatización de la interfaz de usuario,properties para el tipo de control Tab
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Tab
- Automatización de la interfaz de usuario,events para el tipo de control Tab
- estructuras de árbol, tipo de control Tab
- properties,Tab (tipo de control)
- patrones de control, tipo de control Tab
- events,Tab (tipo de control)
- compatibilidad con el tipo de control Tab
- Tab (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Tab
- tipos de control, patrones de control para el tipo de control Tab
- tipos de control, compatibilidad con Tab
- tipos de control,Tab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a83263db87a68e258598ea46ca903af2ddb39c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482501"
---
# <a name="tab-control-type"></a>Tipo de control Tab

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **Tab.**

Un control de ficha es análogo a los divisores de un bloc de notas o las etiquetas de un archivador. Mediante el uso de un control de ficha, una aplicación puede definir varias páginas para la misma área de un cuadro de diálogo o de una ventana.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo **de** control Tab. Los Automatización de la interfaz de usuario se aplican a todos los controles de pestaña en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol de Automatización de la interfaz de usuario que pertenece a los controles de tabulación y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, [vea información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Pestaña<ul><li>TabItem (1 o más)</li><li>ScrollBar (0 o 1)<ul><li>Button (0 o 2)</li></ul></li></ul></li></ul> | <ul><li>Pestaña<ul><li>TabItem (1 o más)</li></ul></li></ul> | 




 

Los controles tab tienen elementos Automatización de la interfaz de usuario secundarios basados en el tipo de control [TabItem.](uiauto-supporttabitemcontroltype.md) Cuando los elementos de tabulación se agrupan (por ejemplo, como en las aplicaciones de Microsoft Office), el tipo de control **Tab** también puede hospedar tipos de **control** Grupos para los elementos de ficha agrupados, como se muestra en la siguiente estructura de árbol.




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Pestaña<ul><li>TabItem (1 o más)</li><li>Group (0 o más)<ul><li>TabItem (0 o más)</li></ul></li><li>ScrollBar (0 o 1)<ul><li>Button (0 o 2)</li></ul></li></ul></li></ul> | <ul><li>Pestaña<ul><li>TabItem (1 o más)</li><li>Group (0 o más)<ul><li>TabItem (0 o más)</li></ul></li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de tabulación. Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor      | Notas                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | No         | El control de pestaña no tiene puntos en los que se puede hacer clic.                                                                                                                                                                                                                                                                                                                               |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Tabulación**    |                                                                                                                                                                                                                                                                                                                                                                               |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | El control de tabulación siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario texto.                                                                                                                                                                                                                                                                                             |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | El control de pestaña siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                                                                                                                                                                             |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | TRUE       | El tipo de control Tab debe poder recibir el foco de teclado. Normalmente, un cliente Automatización de la interfaz de usuario llama a [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) en un control de pestaña y uno de sus elementos reenviará el foco del teclado al control de tabulación. Es posible que algunos contenedores de ficha obtengan el foco sin haber establecido el foco en uno de sus elementos. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Los controles de ficha suelen tener una etiqueta de texto estático que se expone a través de esta propiedad.                                                                                                                                                                                                                                                                                        |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo **de** control Tab. El valor predeterminado es "tab" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                                                  |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El control de pestaña rara vez requiere una **propiedad Name.**                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Vea las notas. | El control de ficha siempre debe indicar si está colocado horizontal o verticalmente.                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de tabulación. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                             | Soporte técnico/valor | Notas                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Requerido      | Todos los controles de pestaña deben admitir el [patrón de](uiauto-implementingselection.md) control Selección.                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | TRUE          | Los controles de ficha siempre requieren que se realice una selección.                                                                                                                  |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | FALSE         | Los controles de ficha siempre son contenedores de selección única.                                                                                                                   |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depende       | El [patrón de](uiauto-implementingscroll.md) control Scroll debe ser compatible si el control de pestaña tiene widgets que permiten desplazarse por un conjunto de elementos de ficha. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de tabulación son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                        | Notas                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




