---
title: Tipo de control Table
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Table.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Table
- Automatización de la interfaz de usuario,Tipo de control Table
- Automatización de la interfaz de usuario,tree structure for Table control type
- Automatización de la interfaz de usuario,properties para el tipo de control Table
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Table
- Automatización de la interfaz de usuario,events para el tipo de control Table
- estructuras de árbol, tipo de control Table
- properties,Tipo de control Table
- patrones de control, tipo de control Table
- events,Tipo de control Table
- Compatibilidad con el tipo de control Table
- Table (tipo de control)
- tipos de control, estructura de árbol para tipo de control Table
- tipos de control, patrones de control para tipo de control Table
- tipos de control, compatibilidad con Table
- tipos de control, Tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0badb06cfc449140162663625f3fa7282f9c1589
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470082"
---
# <a name="table-control-type"></a>Tipo de control Table

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo **de** control Table.

Los controles de tabla contienen filas y columnas de texto y, opcionalmente, encabezados de fila y encabezados de columna.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, las propiedades, los patrones de control y los eventos necesarios para el tipo **de** control Table. Los Automatización de la interfaz de usuario se aplican a todos los controles de tabla en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de tabla y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Tabla<ul><li>Text (0 o 1)</li><li>Encabezado (0 o más)</li><li>Varios controles (0 o más)</li></ul></li></ul> | <ul><li>Tabla<ul><li>Texto (1 o más)</li><li>Varios controles (0 o más)</li></ul></li></ul> | 




 

Si un control de tabla tiene encabezados de fila o columna, deben exponerse en la vista de control del Automatización de la interfaz de usuario control. La vista de contenido no necesita exponer esta información porque se puede acceder a ella mediante [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de tabla. Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor      | Notas                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic.                              |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Tabla**  |                                                                                                                                                                                                                                   |
| [**UIA \_ DescribedByPropertyId**](uiauto-automation-element-propids.md)                   | Vea las notas. | Si la tabla se anota por otro elemento de la interfaz de usuario (por ejemplo, un elemento de texto que contiene la descripción de la tabla), la propiedad DescribedBy debería exponer una referencia al elemento de automatización del control de texto.           |
| [**HelpTextPropertyId de UIA \_**](uiauto-automation-element-propids.md)                         | Vea las notas. | Se deben exponer más detalles sobre el propósito de la tabla a través de esta propiedad si la propiedad [**\_ NamePropertyId**](uiauto-automation-element-propids.md) de UIA no la explica lo suficiente.      |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | El control de tabla siempre debe aparecer en la vista de contenido del Automatización de la interfaz de usuario tabla.                                                                                                                                               |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | El control de tabla siempre debe aparecer en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                               |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia al elemento de automatización del control.                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo **de** control Table. El valor predeterminado es "table" para en-US o inglés (Estados Unidos).                                                                                                  |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | Normalmente, el control de tabla obtiene el valor de su nombre de una etiqueta de texto estático. Si no hay una etiqueta de texto estático, el elemento debe asignar una propiedad Name que siempre debe estar disponible para explicar el propósito de la tabla. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control necesarios para que todos los controles de tabla sean compatibles. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico                     | Notas                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Requerido                    | Dado que el control de tabla contiene elementos presentados en una cuadrícula, siempre admite el [patrón de](uiauto-implementinggrid.md) control Grid.                                                                                                                                                    |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Requerido con objetos secundarios | Los objetos internos de una tabla deben admitir los patrones de control [GridItem](uiauto-implementinggriditem.md) y [TableItem.](uiauto-implementingtableitem.md) La propia tabla no necesita admitir el patrón de control GridItem o TableItem a menos que la tabla forma parte de otra tabla.  |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Requerido                    | El control de tabla siempre puede tener encabezados asociados al contenido.                                                                                                                                                                                                                       |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Requerido con objetos secundarios | Los objetos internos de una tabla deben admitir los patrones de control [GridItem](uiauto-implementinggriditem.md) y [TableItem.](uiauto-implementingtableitem.md) La propia tabla no necesita admitir los patrones de control GridItem o TableItem, a menos que la tabla forme parte de otra tabla. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que los controles de tabla son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




