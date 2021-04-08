---
title: Slide (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Slider.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Slider
- Automatización de la interfaz de usuario, tipo de control Slider
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Slider
- Automatización de la interfaz de usuario, propiedades para el tipo de control Slider
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Slider
- Automatización de la interfaz de usuario, eventos para el tipo de control Slider
- estructuras de árbol, tipo de control Slider
- propiedades, tipo de control Slider
- patrones de control, tipo de control Slider
- Events, Slide (tipo de control)
- compatibilidad con el tipo de control Slider
- Slider (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Slider
- tipos de control, patrones de control para el tipo de control Slider
- tipos de control, compatibilidad con el control deslizante
- tipos de control, control deslizante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be8e82dfc8f011363086745368ed1693c45a6aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994357"
---
# <a name="slider-control-type"></a>Slide (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Slider** .

Un control deslizante es un control compuesto con botones que permiten a un usuario establecer un intervalo numérico o seleccionar un conjunto de elementos.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Slider** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles deslizantes donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles deslizantes y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Control deslizante
<ul>
<li>Button (2 o 4)</li>
<li>Thumb (1)</li>
<li>Elemento de lista (0 o más)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Control deslizante
<ul>
<li>Elemento de lista (0 o más)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles deslizantes. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | La mayoría de los controles deslizantes debe devolver el error [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) porque todo el rectángulo delimitador del control deslizante está ocupado por controles secundarios. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Control deslizante** | Este valor es el mismo para todos los marcos de trabajo.                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control deslizante siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control deslizante siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                           |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad. Los elementos secundarios (botones y Thumb) de un control deslizante nunca deben tener el foco. El foco siempre debe permanecer en el control deslizante.       |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si hay una etiqueta de texto estático asociada al control, esta propiedad debe exponer una referencia a ese control. Si el control de texto es un subcomponente de otro control, no tendrá un conjunto de propiedades **LabeledBy** .   |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **Slider** . El valor predeterminado es "slider" para en-US o inglés (Estados Unidos).                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El nombre del control deslizante se genera normalmente a partir de una etiqueta de texto estático. Si no hay una etiqueta de texto estático, el desarrollador de la aplicación debe asignar un valor de propiedad para **nombre** .                              |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que deben admitir todos los controles deslizantes. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                          | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Depende       | Un control deslizante debe admitir el patrón de control [RangeValue](uiauto-implementingrangevalue.md) si el contenido se puede establecer en un valor dentro de un intervalo numérico.                                                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | Depende       | Un control deslizante debe admitir el patrón de control [Selection](uiauto-implementingselection.md) si el contenido representa un valor entre un conjunto discreto de opciones. Si se admite el patrón de control Selection, la selección correspondiente se debe exponer como uno o varios elementos de lista secundarios del control deslizante. |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | Depende       | Un control deslizante debe admitir el patrón de control [Value](uiauto-implementingvalue.md) si el contenido representa un valor entre un conjunto discreto de opciones.                                                                                                                                                     |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles deslizantes deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de RangeValueValuePropertyId.        | Si el control admite el patrón de control [RangeValue](uiauto-implementingrangevalue.md) , debe admitir este evento.   |
| [**\_InvalidatedEventId de selección de UIA \_**](uiauto-event-ids.md)                                       | Si el control admite el patrón de control [Selection](uiauto-implementingselection.md) , debe admitir este evento.     |
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

 

 




