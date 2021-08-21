---
title: Tipo de control de grupo
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Grupo.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Grupo
- Automatización de la interfaz de usuario, tipo de control Group
- Automatización de la interfaz de usuario,tree structure for Group control type
- Automatización de la interfaz de usuario,properties para el tipo de control Group
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Group
- Automatización de la interfaz de usuario,events para el tipo de control Group
- tree structures,Group control type
- properties,Group control type
- patrones de control, tipo de control Group
- events,Group control type
- compatibilidad con el tipo de control Grupo
- Group (tipo de control)
- tipos de control, estructura de árbol para tipo de control Group
- tipos de control, patrones de control para el tipo de control Grupo
- tipos de control, compatibilidad con group
- tipos de control, Grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe0cee05f7132a35c8dd3f998ae9af5a89ac2a71
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477751"
---
# <a name="group-control-type"></a>Tipo de control de grupo

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo **de** control Grupo.

Un control de grupo representa un nodo dentro de una jerarquía. El **tipo** de control Group crea una separación en el árbol Automatización de la interfaz de usuario para que los elementos que se agrupan tengan una división lógica dentro del Automatización de la interfaz de usuario árbol.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el **tipo de** control Group. Los Automatización de la interfaz de usuario se aplican a todos los controles de grupo en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece a los controles de grupo y se describe lo que se puede incluir en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Group (Grupo)<ul><li>0 o varios controles</li></ul></li></ul> | <ul><li>Group (Grupo)<ul><li>0 o varios controles</li></ul></li></ul> | 




 

Los controles de grupo suelen incluir Automatización de la interfaz de usuario para los tipos de control que se encuentran debajo de ellos en el subárbol, incluidos los tipos de control [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md)y [DataItem.](uiauto-supportdataitemcontroltype.md) Dado que un control de grupo es un contenedor genérico, es posible que cualquier tipo de control esté bajo el control de grupo en el árbol.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de grupo. Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor      | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Grupo**  |                                                                                                                                                                                                      |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**   | El control de grupo siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario contenido.                                                                                                                  |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**   | El control de grupo siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                  |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Los controles de grupo suelen etiquetarse automáticamente. En estos casos, devuelve **NULL**. Si el grupo tiene una etiqueta de texto estático, devuelva la etiqueta como valor de la **propiedad LabeledBy.**                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo **de** control Grupo. El valor predeterminado es "group" para en-US o Inglés (Estados Unidos).                                                                     |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El control de grupo suele recibir su nombre del texto que etiqueta el control.                                                                                                                     |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control necesarios para ser compatibles con el tipo **de** control Group. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico | Notas                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Los controles de grupo que se pueden usar para mostrar u ocultar información deben admitir el patrón de control [ExpandCollapse.](uiauto-implementingexpandcollapse.md) |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario eventos que los controles de grupo son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                                | Notas                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                                  |
| [**UIA \_ Evento expandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) cambiado por la propiedad . | Si el control admite el patrón de control de patrón de control [ExpandCollapse,](uiauto-implementingexpandcollapse.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.                         |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento.                       |
| [**UIA \_ Evento de cambio de propiedad ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)                                 | Si el control admite el patrón de control [Toggle,](uiauto-implementingtoggle.md) debe admitir este evento.                                 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




