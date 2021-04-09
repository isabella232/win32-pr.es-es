---
title: ProgressBar (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control ProgressBar.
ms.assetid: 2ea0c1f1-1a0a-4360-bdcb-8edc13cc3c31
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control ProgressBar
- UI Automation, ProgressBar (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control ProgressBar
- Automatización de la interfaz de usuario, propiedades para el tipo de control ProgressBar
- Automatización de la interfaz de usuario, patrones de control para el tipo de control ProgressBar
- Automatización de la interfaz de usuario, eventos para el tipo de control ProgressBar
- estructuras de árbol, ProgressBar (tipo de control)
- Properties, ProgressBar (tipo de control)
- patrones de control, ProgressBar (tipo de control)
- Events, ProgressBar (tipo de control)
- compatibilidad con el tipo de control ProgressBar
- ProgressBar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control ProgressBar
- tipos de control, patrones de control para el tipo de control ProgressBar
- tipos de control, compatibilidad con ProgressBar
- tipos de control, ProgressBar
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 98be22a4a3d3b99e113d3c0d1402f2c45ee25550
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/06/2019
ms.locfileid: "104149027"
---
# <a name="progressbar-control-type"></a>ProgressBar (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **ProgressBar** .

Los controles de barra de progreso indican el progreso de una operación larga. El control está compuesto de un rectángulo que se rellena gradualmente con el color de resaltado del sistema a medida que una operación progresa.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario necesaria, las propiedades, los patrones de control y los eventos para el tipo de control **ProgressBar** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de barra de progreso donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

- [Estructura de árbol típica](#typical-tree-structure)
- [Propiedades relevantes](#relevant-properties)
- [Patrones de control necesarios](#required-control-patterns)
- [Eventos necesarios](#required-events)
- [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de barra de progreso y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).

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
<li>ProgressBar</li>
</ul></td>
<td><ul>
<li>ProgressBar</li>
</ul></td>
</tr>
</tbody>
</table>

Los controles de barra de progreso no tienen elementos secundarios en la vista de control o de contenido del árbol de automatización de la interfaz de usuario.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para las barras de progreso. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).

| Propiedad de automatización de interfaz de usuario                                                                                              | Value           | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.      | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.      | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.      | Se admite si hay un rectángulo delimitador. Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ProgressBar** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**        | El control de barra de progreso siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**        | El control de barra de progreso siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                           |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.      | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.      | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.      | Cadena localizada que corresponde al tipo de control **ProgressBar** . El valor predeterminado es "barra de progreso" para en-US o inglés (Estados Unidos).                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.      | El control de barra de progreso suele recibir su nombre de una etiqueta de texto estático. Si no hay ninguna etiqueta de texto estático, el desarrollador de aplicaciones debe exponer un valor para la propiedad Name.                  |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que deben admitir los controles de barra de progreso. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                              | Soporte técnico/valor | Notas                                                                                                                                      |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Depende       | Los controles de barra de progreso que toman un intervalo numérico deben implementar el patrón de control [RangeValue](uiauto-implementingrangevalue.md) .        |
| [**Mínima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Depende           | El valor de esta propiedad es el valor mínimo en el que se puede establecer el control. Este valor debe ser menor que el [**máximo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum).                                                      |
| [**Máxima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Depende         | El valor de esta propiedad es el valor máximo en el que se puede establecer el control. Este valor debe ser mayor que el [**mínimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum).                                                        |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | **NaN**       | Esta propiedad no es necesaria porque los controles de barra de progreso son de solo lectura.                                                                 |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NaN**       | Esta propiedad no es necesaria porque los controles de barra de progreso son de solo lectura.                                                                 |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Depende       | Los controles de barra de progreso que proporcionan una indicación textual del progreso deben implementar el patrón de control [Value](uiauto-implementingvalue.md) . |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | **TRUE**      | El valor de esta propiedad siempre es **true**.                                                                                            |
| [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Vea las notas.    | Esta propiedad expone el progreso textual de un control de barra de progreso.                                                                          |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de RangeValueValuePropertyId.        | Si el control admite el patrón de control [RangeValue](uiauto-implementingrangevalue.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ValueValuePropertyId.                  | Si el control admite el patrón de control [Value](uiauto-implementingvalue.md) , debe admitir este evento.             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




