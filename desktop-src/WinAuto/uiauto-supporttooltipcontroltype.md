---
title: Tipo de control ToolTip
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control ToolTip. Los controles de información sobre herramientas son ventanas emergentes que contienen texto.
ms.assetid: 810f85a9-4d3b-4ceb-bd2c-bf70e8712ae2
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control ToolTip
- Automatización de la interfaz de usuario,tipo de control ToolTip
- Automatización de la interfaz de usuario,tree structure for ToolTip control type
- Automatización de la interfaz de usuario,properties para el tipo de control ToolTip
- Automatización de la interfaz de usuario,patrones de control para el tipo de control ToolTip
- Automatización de la interfaz de usuario,events para el tipo de control ToolTip
- estructuras de árbol, tipo de control Información sobre herramientas
- properties,Tipo de control ToolTip
- patrones de control, tipo de control De información sobre herramientas
- events,Tipo de control ToolTip
- Compatibilidad con el tipo de control ToolTip
- ToolTip (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Información sobre herramientas
- tipos de control, patrones de control para el tipo de control Información sobre herramientas
- tipos de control, compatibilidad con información sobre herramientas
- tipos de control, Información sobre herramientas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a627114afcdeeb9b6e156572476462fa7ecde75a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472861"
---
# <a name="tooltip-control-type"></a>Tipo de control ToolTip

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **ToolTip.** Los controles de información sobre herramientas son ventanas emergentes que contienen texto.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **ToolTip.** Los Automatización de la interfaz de usuario se aplican a todos los controles de información sobre herramientas en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de Automatización de la interfaz de usuario que pertenece a los controles de información sobre herramientas y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol Automatización de la interfaz de usuario, [vea información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Información sobre herramientas<ul><li>Text (0 o más)</li><li>Imagen (0 o más)</li></ul></li></ul> | <ul><li>Información sobre herramientas</li></ul> | 




 

Los controles de información sobre herramientas solo aparecen en la vista de contenido del Automatización de la interfaz de usuario si pueden recibir el foco del teclado. De lo contrario, toda la información sobre herramientas está disponible en la propiedad [**IUIAutomationElement::CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (o [**CachedHelpText)**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)en el elemento al que hace referencia la información sobre herramientas.

La información sobre herramientas debe aparecer debajo del control al que hace referencia su información. Los clientes deben escuchar la información sobre herramientas [**\_ UIAOpenedEventId**](uiauto-event-ids.md) para asegurarse de que obtienen de forma coherente la información contenida en la información sobre herramientas.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **ToolTip.** Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor       | Notas                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.  | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.  | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.  | El punto en el que se puede hacer clic debe ser la parte de la información sobre herramientas que descarta el control. Algunas informaciones sobre herramientas no tienen esta capacidad y no tendrán un punto en el que se pueda hacer clic.                                                                                                                                                                                                  |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **ToolTip** |                                                                                                                                                                                                                                                                                                                                                                |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | Depende     | Si el control de información sobre herramientas puede recibir el foco del teclado, debe aparecer en la vista de contenido del árbol. Si es solo texto, está disponible como la propiedad [**IUIAutomationElement::CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (o [**CachedHelpText)**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)del control que la ha producido. |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | Verdadero        | El control de información sobre herramientas siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                                                                                                                                                          |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.  | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | Los controles de información sobre herramientas siempre se etiquetan por su contenido.                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.  | Cadena localizada que corresponde al tipo de control ToolTip. El valor predeterminado es "información sobre herramientas" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                               |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.  | El nombre del control de información sobre herramientas es el texto que se muestra dentro de la información sobre herramientas.                                                                                                                                                                                                                                                                              |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control necesarios para ser compatibles con los controles de información sobre herramientas. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                   | Soporte técnico | Notas                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Depende | Para mejorar la accesibilidad, un control de información sobre herramientas puede admitir el [patrón de](uiauto-implementingtextandtextrange.md) control Texto, aunque no es necesario. El patrón de control Text es útil cuando el texto tiene atributos y estilo enriquecidos (por ejemplo, color, negrita y cursiva). |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) | Depende | La información sobre herramientas que se puede cerrar haciendo clic en un elemento de la interfaz de usuario debe admitir el patrón de control [Ventana](uiauto-implementingwindow.md) para que puedan cerrarse automáticamente.                                                                                                                 |



 

## <a name="required-events"></a>Eventos necesarios

Los controles de información sobre herramientas deben generar el evento [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md) cuando aparecen en la pantalla. El evento incluirá una referencia al elemento Automatización de la interfaz de usuario de la propia información sobre herramientas.

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que los controles de información sobre herramientas son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                            | Notas                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                               |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)          |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                          | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                      | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad NamePropertyId.**](uiauto-automation-element-propids.md)                                    |                                                                                                                            |
| [**TextChangedEventId de texto UIA \_ \_**](uiauto-event-ids.md)                                                          | Si el control admite el patrón de control [Text,](uiauto-implementingtextandtextrange.md) debe admitir este evento.   |
| [**UIA \_ ToolTipClosedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**Ventana de \_ \_ UIAClosedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [Window,](uiauto-implementingwindow.md) debe admitir este evento.           |
| [**Ventana de \_ \_ UIAOpenedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [Window,](uiauto-implementingwindow.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad WindowWindowVisualStatePropertyId.**](uiauto-control-pattern-propids.md) | Si el control admite el patrón de control [Window,](uiauto-implementingwindow.md) debe admitir este evento.           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




