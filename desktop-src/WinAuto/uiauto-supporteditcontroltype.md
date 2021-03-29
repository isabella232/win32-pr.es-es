---
title: Editar tipo de control
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Edit.
ms.assetid: ec45ec5e-4faa-4635-8726-5bbe1f20b843
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Edit
- UI Automation, Edit (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Edit
- UI Automation, propiedades para el tipo de control Edit
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Edit
- Automatización de la interfaz de usuario, eventos para el tipo de control Edit
- estructuras de árbol, editar tipo de control
- propiedades, editar tipo de control
- patrones de control, editar tipo de control
- Events, Edit (tipo de control)
- compatibilidad con el tipo de control Edit
- Edit (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Edit
- tipos de control, patrones de control para el tipo de control Edit
- tipos de control, compatibilidad con la edición
- tipos de control, editar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7dffb572497df47d65def91dda22f3b8e59299
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903443"
---
# <a name="edit-control-type"></a>Editar tipo de control

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Edit** .

Los controles de edición habilitan a un usuario para que vea y edite una línea de texto simple sin compatibilidad con formato enriquecido.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control Edit. Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de edición donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de edición y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Editar</li>
</ul></td>
<td><ul>
<li>Editar</li>
</ul></td>
</tr>
</tbody>
</table>



 

Los controles que implementan el tipo de control **Edit** siempre tendrán cero barras de desplazamiento en la vista de control del árbol de automatización de la interfaz de usuario porque es un control de una sola línea. La única línea de texto puede encapsularse en algunos escenarios de diseño. El tipo de control **Edit** solo está pensado para pequeñas cantidades de texto.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de edición. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | El control de edición debe tener un punto en el que se pueda hacer clic que dé enfoque de entrada a la parte de edición del control cuando un usuario hace clic en el mouse allí.                                                                                                                                           |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Editar**   |                                                                                                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | El control de edición siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | El control de edición siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                            |
| [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md)                     | Vea las notas. | Debe establecerse en **true** en los controles de edición que contienen contraseñas. Si un control de edición contiene el contenido de la contraseña, esta propiedad se puede usar por un lector de pantalla para determinar si las pulsaciones de teclas se deben leer cuando el usuario las introduce.                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si hay una etiqueta de texto estático asociada al control, esta propiedad debe exponer una referencia a ese control. Si el control de texto es un subcomponente de otro control, no tendrá un conjunto de propiedades **LabeledBy** .                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **Edit** . El valor predeterminado es "Edit" para en-US o inglés (Estados Unidos).                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El nombre del control de edición se genera normalmente desde una etiqueta de texto estático. Si no hay una etiqueta de texto estático, el desarrollador de la aplicación debe asignar un valor de propiedad para **nombre** . La propiedad **Name** nunca debe contener el contenido textual del control de edición. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que deben admitir los controles de edición. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                              | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Depende       | Todos los controles de edición que toman un intervalo numérico deben exponer el patrón de control [RangeValue](uiauto-implementingrangevalue.md) .                                                                                                                                                                                                                                                                                       |
| [**Mínima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Vea las notas.    | Esta propiedad debe ser el valor más pequeño en el que se puede establecer el contenido del control de edición.                                                                                                                                                                                                                                                                                                                     |
| [**Máxima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Vea las notas.    | Esta propiedad debe ser el valor más grande en el que se puede establecer el contenido del control de edición.                                                                                                                                                                                                                                                                                                                      |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Vea las notas.    | Esta propiedad debe indicar el número de posiciones decimales en el que se puede establecer el valor. Si el control de edición solo acepta enteros, el valor de la propiedad **SmallChange** debe ser 1. Si el control de edición acepta un intervalo de 1,0 a 2,0, el valor de la propiedad **SmallChange** debe ser 0,1. Si el control de edición acepta un intervalo de 1,00 a 2,00, el valor de la propiedad **SmallChange** debe ser 0,001.                   |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NULL**      | Esta propiedad no necesita exponerse en un control de edición.                                                                                                                                                                                                                                                                                                                                                      |
| [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Vea las notas.    | Esta propiedad indica el contenido numérico del control de edición. Cuando un cliente de automatización de la interfaz de usuario establece un valor más preciso en los intervalos especificados en las propiedades [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum) y [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum) , la propiedad [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) se redondea automáticamente al valor aceptado más cercano. |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)                 | Obligatorio      | Todos los controles de edición deben admitir el patrón de control [Text](uiauto-implementingtextandtextrange.md) porque la información detallada siempre debe estar disponible para los clientes de tecnología de asistencia.                                                                                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Depende       | Todos los controles de edición que toman una cadena deben exponer el patrón de control [Value](uiauto-implementingvalue.md) .                                                                                                                                                                                                                                                                                                        |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | Vea las notas.    | Esta propiedad se debe establecer para indicar si el control puede tener un valor establecido mediante programación o si el usuario puede editarlo.                                                                                                                                                                                                                                                                                |
| [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Vea las notas.    | Esta propiedad contiene el contenido textual del control de edición. Si la [**propiedad \_ IsPasswordPropertyId de UIA**](uiauto-automation-element-propids.md) está establecida en **true**, la consulta de la propiedad [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) debe devolver un error.                                                                                                                      |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de edición deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                        | Notas                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                      | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                  | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de NamePropertyId.                                                |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de RangeValueValuePropertyId.                             | Si el control admite el patrón de control [RangeValue](uiauto-implementingrangevalue.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontallyScrollablePropertyId.   | Un control de edición nunca admite el patrón de control [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalScrollPercentPropertyId. | Un control de edición nunca admite el patrón de control [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalViewSizePropertyId.           | Un control de edición nunca admite el patrón de control [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticallyScrollablePropertyId.       | Un control de edición nunca admite el patrón de control [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalScrollPercentPropertyId.     | Un control de edición nunca admite el patrón de control [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalViewSizePropertyId.               | Un control de edición nunca admite el patrón de control [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**\_TextChangedEventId de texto de UIA \_**](uiauto-event-ids.md)                                                                      | Si el control admite el patrón de control [Text](uiauto-implementingtextandtextrange.md) , debe admitir este evento.   |
| [**\_TextSelectionChangedEventId de texto de UIA \_**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [Text](uiauto-implementingtextandtextrange.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ValueValuePropertyId.                                      | Si el control admite el patrón de control [Value](uiauto-implementingvalue.md) , debe admitir este evento.             |



 

## <a name="remarks"></a>Observaciones

Un control de edición se puede usar como un campo de texto de solo lectura que no admite la selección o edición de texto. Dicho control de edición se comporta como un objeto de campo que tiene un nombre y un valor específicos.

Si un control de edición contiene texto de marcador de posición (por ejemplo, un banner de indicación), se debe usar el texto como la propiedad **HelpText** a menos que el usuario pueda editar el texto y, a continuación, reutilizarlo como texto de marcador de posición. Por ejemplo, la barra de direcciones de Windows Internet Explorer contiene el texto "About: Tabs" cuando se abre una nueva pestaña. Esto no es **HelpText** porque es una dirección de programación que el usuario puede usar o editar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




