---
title: Calendar (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Calendar. Un control de calendario permite al usuario determinar fácilmente la fecha y seleccionar otras fechas.
ms.assetid: 886cf1a4-0e6f-4ae1-9dc4-e97ac6a22359
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Calendar
- Automatización de la interfaz de usuario, tipo de control Calendar
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Calendar
- Automatización de la interfaz de usuario, propiedades para el tipo de control Calendar
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Calendar
- Automatización de la interfaz de usuario, eventos para el tipo de control Calendar
- estructuras de árbol, tipo de control Calendar
- propiedades, tipo de control Calendar
- patrones de control, tipo de control Calendar
- Events, Calendar (tipo de control)
- compatibilidad con el tipo de control Calendar
- Calendar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Calendar
- tipos de control, patrones de control para el tipo de control Calendar
- tipos de control, compatibilidad con el calendario
- tipos de control, calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef936848f764c6937bfe36e6ed919f0a88dac78c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076378"
---
# <a name="calendar-control-type"></a>Calendar (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Calendar** . Un control de calendario permite al usuario determinar fácilmente la fecha y seleccionar otras fechas.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Calendar** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de calendario donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y los patrones

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de calendario y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Calendario
<ul>
<li>DataGrid
<ul>
<li>Header (0 o 1)
<ul>
<li>HeaderItem (0 o 7, la cantidad depende del número de días que se muestren en las columnas)</li>
</ul></li>
<li>ListItem (la cantidad depende del número de días que se muestren)</li>
<li>Button (0 o 2; para la paginación de la vista de calendario)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Calendario
<ul>
<li>ListItem (la cantidad depende del número de días que se muestren)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Los controles de calendario se pueden representar de muchas formas diferentes dentro de la interfaz de usuario. Los únicos controles garantizados que están en la vista de control del árbol de automatización de la interfaz de usuario son los controles de cuadrícula de datos, encabezado, elemento de encabezado y elemento de lista.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **Calendar** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value        | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | Se admite si hay un rectángulo delimitador. Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Calendario** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | El control de calendario siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | El control de calendario siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.   | El valor de esta propiedad debe ser la etiqueta del control de documento. Normalmente, se utiliza el título del documento.                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada que corresponde al tipo de control **Calendar** . El valor predeterminado es "Calendar" para en-US o inglés (Estados Unidos).                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | Normalmente, el control de calendario recibe su nombre de la fecha actual.                                                                                                                                  |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de calendario. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                        | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obligatorio      | El control de calendario siempre admite el patrón de control [Grid](uiauto-implementinggrid.md) porque los días de un mes son elementos que se pueden explorar espacialmente.                                                                                                                                                        |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depende       | La mayoría de los controles de calendario admiten voltear la vista por página. Se recomienda usar el patrón de control [Scroll](uiauto-implementingscroll.md) para admitir la navegación de paginación.                                                                                                                                                    |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Depende       | La mayoría de los controles de calendario conservan un determinado día, mes o año como una selección del subelemento. Algunos calendarios son de selección múltiple y otros solo seleccionables de forma única. El control de calendario con subelementos seleccionables debe admitir el patrón de control [Selection](uiauto-implementingselection.md) .                         |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Obligatorio      | Dado que el control de calendario siempre tiene un encabezado dentro de su subárbol para los días de la semana, se debe admitir el patrón de control [TABLE](uiauto-implementingtable.md) .                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | No            | El patrón de control [Value](uiauto-implementingvalue.md) no es necesario para los controles de calendario porque el elemento no puede establecer el valor directamente en el control. Si una fecha concreta está asociada con el control, el patrón de control [Selection](uiauto-implementingselection.md) debe proporcionar la información. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que deben admitir los controles de calendario. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                        | Notas                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                      |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                      | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.                                                                                     |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                  | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.                                                                                   |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de MultipleViewCurrentViewPropertyId.             | Si el control admite la propiedad [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview) del patrón de control [MultipleView](uiauto-implementingmultipleview.md) , debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontallyScrollablePropertyId.   | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalScrollPercentPropertyId. | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalViewSizePropertyId.           | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalScrollPercentPropertyId.     | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticallyScrollablePropertyId.       | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalViewSizePropertyId.               | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.                                                                                             |
| [**\_InvalidatedEventId de selección de UIA \_**](uiauto-event-ids.md)                                                            |                                                                                                                                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




