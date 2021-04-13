---
title: Thumb (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Thumb
- Automatización de la interfaz de usuario, Thumb (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Thumb
- Automatización de la interfaz de usuario, propiedades para el tipo de control Thumb
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Thumb
- Automatización de la interfaz de usuario, eventos para el tipo de control Thumb
- estructuras de árbol, Thumb (tipo de control)
- propiedades, Thumb (tipo de control)
- patrones de control, Thumb (tipo de control)
- Events, Thumb (tipo de control)
- compatibilidad con el tipo de control Thumb
- Thumb (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Thumb
- tipos de control, patrones de control para el tipo de control Thumb
- tipos de control, compatibilidad con Thumb
- tipos de control, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8faf60fab30f54d3ed3e4b5a9f49628a3a35be5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419082"
---
# <a name="thumb-control-type"></a>Thumb (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Thumb** .

Los controles de posición ofrecen la funcionalidad que permite que un control se mueva (o se arrastre), como un botón de barra de desplazamiento, o que cambie su tamaño, como un widget para cambiar el tamaño de una ventana. Tenga en cuenta que un control Thumb no proporciona la funcionalidad de arrastrar y colocar. Los controles de posición pueden recibir el foco del mouse, pero no el foco de teclado. El desarrollador del control debe implementar el control para que actúe correctamente (se pueda arrastrar o cambiar de tamaño).

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Thumb** . Los requisitos de automatización de la interfaz de usuario aplican todos los controles Thumb en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de posición y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Thumb</li>
</ul></td>
<td>(No aplicable)</td>
</tr>
</tbody>
</table>



 

Los controles de posición nunca aparecen en la vista de contenido porque solo existen para ser manipulados con un mouse. Se exponen a través de otro patrón de control, como el patrón de control [Scroll](uiauto-implementingscroll.md) , el patrón de control [Transform](uiauto-implementingtransform.md) o el patrón de control [RangeValue](uiauto-implementingrangevalue.md) , que se admite en el contenedor del control Thumb.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles Thumb. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Punto dentro del área de cliente visible del control Thumb.                                                                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Útil**  |                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | false      | El control Thumb nunca se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control Thumb siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad. Un control Thumb puede recibir el foco si se usa como un objeto de "agarrador" para ajustar el tamaño de una ventana o un panel. Un control Thumb en un control deslizante o en una barra de desplazamiento nunca debe recibir el foco. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | Los controles Thumb nunca tienen una etiqueta.                                                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **Thumb** . El valor predeterminado es "Thumb" para en-US o inglés (Estados Unidos).                                                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULL       | Dado que el control Thumb no está disponible en la vista de contenido del árbol de automatización de la interfaz de usuario, no requiere un nombre.                                                                                                                                        |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que deben admitir los controles Thumb. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico  | Notas                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Obligatorio | Permite que el control de posición se mueva por la pantalla. Dado que normalmente no se puede cambiar el tamaño del control Thumb o girarlo, el patrón de control [Transform](uiauto-implementingtransform.md) admite principalmente la función [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) . |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles Thumb deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




