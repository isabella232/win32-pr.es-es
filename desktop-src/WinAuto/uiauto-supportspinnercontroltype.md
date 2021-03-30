---
title: Spinner (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Spinner.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Spinner
- Automatización de la interfaz de usuario, tipo de control Spinner
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Spinner
- Automatización de la interfaz de usuario, propiedades para el tipo de control Spinner
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Spinner
- Automatización de la interfaz de usuario, eventos para el tipo de control Spinner
- estructuras de árbol, tipo de control Spinner
- propiedades, tipo de control Spinner
- patrones de control, tipo de control Spinner
- Events, Spinner (tipo de control)
- compatibilidad con el tipo de control Spinner
- Spinner (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Spinner
- tipos de control, patrones de control para el tipo de control Spinner
- tipos de controles, compatibilidad con el control de número
- tipos de controles, control de número
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9681160bf82c9a541412bb6dde8958c603fcfe22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778235"
---
# <a name="spinner-control-type"></a>Spinner (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Spinner** .

Los controles Spinner se usan para seleccionar desde un dominio de elementos o un intervalo de números.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Spinner** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de número donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra una vista de contenido y control típica del árbol de automatización de la interfaz de usuario que pertenece a los controles de número cuando admiten los patrones de control de **RangeValue** y de **selección** y describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).

**Patrón de control RangeValue**



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
<li>Spinner
<ul>
<li>Edición (0 o 1)</li>
<li>Botón (2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Spinner</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Selection (patrón de control)**



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
<li>Spinner
<ul>
<li>Edición (0 o 1)</li>
<li>Botón (2)</li>
<li>Elemento de lista (0 o más)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Spinner
<ul>
<li>Elemento de lista (0 o más)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Para asegurarse de que los dos botones del subárbol de la vista de control se pueden distinguir por herramientas de pruebas automatizadas, asigne el valor **ScrollAmount \_ SmallIncrement** o [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) a la propiedad **AutomationId** según corresponda. En algunas implementaciones, el control de edición asociado puede ser un elemento del mismo nivel que el control de número.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de número. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value       | Notas                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.  | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.  | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.  | El punto en el que se puede hacer clic del control de número enfoca la parte de edición del control.                                                                                                                                                                                                                                      |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Spinner** | Este valor es el mismo para todos los marcos de trabajo.                                                                                                                                                                                                                                                                                 |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | El control de número siempre debe ser contenido.                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | El control de número siempre debe ser un control.                                                                                                                                                                                                                                                                              |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.  | Si el control puede recibir el foco del teclado, debe admitir esta propiedad. Un control de número raramente toma el foco, pero cuando lo hace, el foco debe permanecer en el control de número en sí, no en los botones secundarios. El usuario debe poder realizar todas las acciones de desplazamiento mediante las teclas flecha arriba y flecha abajo. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.  | Los controles de número tienen una etiqueta de texto estático.                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.  | Cadena localizada que corresponde al tipo de control **Spinner** . El valor predeterminado es "Spinner" para en-US o inglés (Estados Unidos).                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.  | El control de número suele recibir su nombre de una etiqueta de texto estático.                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se muestran los patrones de control de UI Automation que se deben admitir por todos los controles de número. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                         | Soporte técnico/valor | Notas                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | Depende       | Los controles de número que abarcan un intervalo numérico pueden admitir el patrón de control [RangeValue](uiauto-implementingrangevalue.md) .               |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | Depende       | Los controles de número que tienen una lista de elementos que se van a seleccionar deben admitir el patrón de control [Selection](uiauto-implementingselection.md) . |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | false         | Los controles de número siempre son contenedores de selección única.                                                                                  |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | Depende       | Los controles de número que abarcan un conjunto de opciones o números pueden admitir el patrón de control [Value](uiauto-implementingvalue.md) .    |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles Spinner deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de RangeValueValuePropertyId.        | Si el control admite el patrón de control [RangeValue](uiauto-implementingrangevalue.md) , debe admitir este evento.   |
| [**UIA \_ Propiedad \_ InvalidatedEventId de selección**](uiauto-event-ids.md) : evento cambiado.               | Si el control admite el patrón de control [Selection](uiauto-implementingselection.md) , debe admitir este evento.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ValueValuePropertyId.                  | Si el control admite el patrón de control [Value](uiauto-implementingvalue.md) , debe admitir este evento.             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




