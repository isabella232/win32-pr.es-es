---
title: Tipo de control Calendar
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Calendar. Un control de calendario permite al usuario determinar fácilmente la fecha y seleccionar otras fechas.
ms.assetid: 886cf1a4-0e6f-4ae1-9dc4-e97ac6a22359
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Calendar
- Automatización de la interfaz de usuario,Tipo de control Calendar
- Automatización de la interfaz de usuario,tree structure for Calendar (Estructura de árbol para el tipo de control Calendar)
- Automatización de la interfaz de usuario,properties para el tipo de control Calendar
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Calendar
- Automatización de la interfaz de usuario,events para el tipo de control Calendar
- estructuras de árbol, tipo de control Calendar
- properties,Calendar , tipo de control
- patrones de control, tipo de control Calendar
- events,Calendar , tipo de control
- Compatibilidad con el tipo de control Calendar
- Calendar (tipo de control)
- tipos de control, estructura de árbol para tipo de control Calendar
- tipos de control, patrones de control para tipo de control Calendar
- tipos de control, compatibilidad con Calendar
- tipos de control, Calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d51271fb2e9526bc293b9c5d36acc0a65b3b639
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172661"
---
# <a name="calendar-control-type"></a>Tipo de control Calendar

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo **de** control Calendar. Un control de calendario permite al usuario determinar fácilmente la fecha y seleccionar otras fechas.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo **de** control Calendar. Los Automatización de la interfaz de usuario se aplican a todos los controles de calendario en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de calendario y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario árbol, vea [Información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Calendario<ul><li>DataGrid<ul><li>Header (0 o 1)<ul><li>HeaderItem (0 o 7, la cantidad depende de cuántos días se muestran en columnas)</li></ul></li><li>ListItem (la cantidad depende del número de días que se muestren)</li><li>Button (0 o 2; para la paginación de la vista de calendario)</li></ul></li></ul></li></ul> | <ul><li>Calendario<ul><li>ListItem (la cantidad depende del número de días que se muestren)</li></ul></li></ul> | 




 

Los controles de calendario se pueden representar de muchas formas diferentes dentro de la interfaz de usuario. Los únicos controles que se garantiza que se encuentran en la vista de control del árbol de Automatización de la interfaz de usuario son los controles de cuadrícula de datos, encabezado, elemento de encabezado y elemento de lista.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo **de** control Calendar. Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value        | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Calendario** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                        |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true         | El control de calendario siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario árbol.                                                                                                               |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true         | El control de calendario siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                               |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.   | El valor de esta propiedad debe ser la etiqueta del control de documento. Normalmente, se utiliza el título del documento.                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada correspondiente al tipo **de** control Calendar. El valor predeterminado es "calendar" para en-US o inglés (Estados Unidos).                                                               |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | Normalmente, el control de calendario obtiene su nombre de la fecha actual.                                                                                                                                  |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de calendario. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                        | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obligatorio      | El control de calendario siempre admite el [patrón de](uiauto-implementinggrid.md) control Grid porque los días de un mes son elementos que se pueden navegar espacialmente.                                                                                                                                                        |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depende       | La mayoría de los controles de calendario admiten voltear la vista por página. Se [recomienda el](uiauto-implementingscroll.md) patrón de control Scroll para admitir la navegación de paginación.                                                                                                                                                    |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Depende       | La mayoría de los controles de calendario conservan un día, mes o año específicos como una selección del subelemento. Algunos calendarios son seleccionables de forma múltiple y otros solo se pueden seleccionar de forma única. El control de calendario con subelementos seleccionables debe admitir el [patrón de](uiauto-implementingselection.md) control Selección.                         |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Obligatorio      | Dado que el control de calendario siempre tiene un encabezado dentro de su subárbol para los días de la semana, debe ser compatible con el patrón [de](uiauto-implementingtable.md) control Tabla.                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | No            | El [patrón](uiauto-implementingvalue.md) de control Valor no es necesario para los controles de calendario porque el elemento no puede establecer el valor directamente en el control . Si se asocia una fecha específica al control, el patrón de control [Selección](uiauto-implementingselection.md) debe proporcionar la información. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que los controles de calendario son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                        | Notas                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                              |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                                                                                                              |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.                                                                                     |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento.                                                                                   |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                              |
| [**UIA \_ Evento de cambio de propiedad MultipleViewCurrentViewPropertyId.**](uiauto-control-pattern-propids.md)             | Si el control admite la [**propiedad CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview) del patrón de control [MultipleView,](uiauto-implementingmultipleview.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                              |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                                                                             |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                                                                             |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                                                                             |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                                                                             |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                                                                             |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                                                                             |
| [**UIA \_ Selection \_ InvalidtedEventId**](uiauto-event-ids.md)                                                            |                                                                                                                                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




