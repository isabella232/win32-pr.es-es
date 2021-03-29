---
title: RadioButton (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control RadioButton.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control RadioButton
- Automatización de la interfaz de usuario, RadioButton (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control RadioButton
- Automatización de la interfaz de usuario, propiedades para el tipo de control RadioButton
- Automatización de la interfaz de usuario, patrones de control para el tipo de control RadioButton
- Automatización de la interfaz de usuario, eventos para el tipo de control RadioButton
- estructuras de árbol, tipo de control RadioButton
- propiedades, RadioButton (tipo de control)
- patrones de control, RadioButton (tipo de control)
- Events, RadioButton (tipo de control)
- compatibilidad con el tipo de control RadioButton
- RadioButton (tipo de control)
- tipos de control, estructura de árbol para el tipo de control RadioButton
- tipos de control, patrones de control para el tipo de control RadioButton
- tipos de control, compatibilidad con RadioButton
- tipos de control, RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702a2227a5164ff694378c82fa3b7cde33f9823
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778240"
---
# <a name="radiobutton-control-type"></a>RadioButton (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **RadioButton** .

Un botón de opción consta de un botón redondo y de texto definido por la aplicación (una etiqueta), un icono o un mapa de bits que indica una opción que el usuario puede realizar seleccionando el botón. Normalmente, una aplicación usa botones de radio en un cuadro de grupo para permitir al usuario elegir entre un conjunto de opciones relacionadas, aunque mutuamente excluyentes. Por ejemplo, la aplicación puede presentar un grupo de botones de radio desde el que el usuario puede seleccionar una preferencia de formato para el texto seleccionado en el área del cliente. El usuario podría seleccionar un formato alineado a la izquierda, alineado a la derecha o centrado seleccionando el botón de radio correspondiente. Normalmente, el usuario solo puede seleccionar una opción cada vez a partir de un conjunto de botones de radio.

> [!Note]  
> Otra generalización del control para los botones en los que solo se puede seleccionar uno de los grupos es el contenido de un botón de alternancia. Algunos marcos de interfaz de usuario consideran que un botón de radio sea un botón de alternancia especializado.

 

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **RadioButton** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de botón donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de botón de radio y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>RadioButton</li>
</ul></td>
<td><ul>
<li>RadioButton</li>
</ul></td>
</tr>
</tbody>
</table>



 

No hay ningún elemento secundario en la vista de control o la vista de contenido.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles que implementan el tipo de control **RadioButton** (como los controles de botón). Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value           | Notas                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.      | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.      | El rectángulo exterior que contiene el control completo.                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.      | El punto en el que se puede hacer clic debe ser un punto que, al hacer clic en él, seleccione el botón de radio.                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **RadioButton** |                                                                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | El control de botón de radio siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | El control de botón de radio siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.      | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | Los controles de botón de radio se etiquetan automáticamente por su contenido.                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.      | Cadena localizada que corresponde al tipo de control **RadioButton** . El valor predeterminado es "botón de radio" para en-US o inglés (Estados Unidos). |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.      | El nombre del control de botón de radio es el texto que se muestra junto al botón que mantiene el estado de la selección.                      |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de botón de radio. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                               | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | Obligatorio      | Todos los controles de botón de radio deben admitir el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) para permitir que se seleccionen.                                                                                                                                                                                                                                                             |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | Vea las notas.    | La propiedad [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) siempre se debe completar para que un cliente de automatización de la interfaz de usuario pueda determinar qué otros botones de radio dentro de un contexto específico se relacionan entre sí. En la versión de Microsoft Win32 del botón de radio, esta propiedad no se admite porque no es posible obtener esta información de ese marco de trabajo heredado. |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | Nunca         | El botón de radio no puede recorrer cíclicamente su estado una vez que se ha establecido. Nunca se debe admitir el patrón de control [Toggle](uiauto-implementingtoggle.md) en un botón de radio.                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de botón deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                     | Notas                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                        |                                                                                                                                |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.   |                                                                                                                                |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                   | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.               | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.     |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) | Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento. |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                         | Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a>Observaciones

Un botón de radio representa una única opción seleccionable entre un grupo de botones de radio del mismo nivel. Idealmente, los botones de radio deben tener un elemento de agrupación que clarifica los límites de los botones de radio del mismo nivel. Sin embargo, a menudo el límite está implícito en la estructura del elemento de la interfaz de usuario. Por ejemplo, un menú puede contener un conjunto de botones de radio consecutivos en lugar de elementos de menú, o un conjunto de botones de radio que se producen después de una etiqueta de grupo, pero antes de un elemento accionable como Button.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




