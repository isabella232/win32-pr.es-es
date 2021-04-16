---
title: ListItem (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control ListItem.
ms.assetid: 8cb579ab-92c9-4311-aad7-5363f4cf2eaf
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control ListItem
- Automatización de la interfaz de usuario, tipo de control ListItem
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control ListItem
- Automatización de la interfaz de usuario, propiedades para el tipo de control ListItem
- Automatización de la interfaz de usuario, patrones de control para el tipo de control ListItem
- Automatización de la interfaz de usuario, eventos para el tipo de control ListItem
- estructuras de árbol, tipo de control ListItem
- Properties, ListItem (tipo de control)
- patrones de control, ListItem (tipo de control)
- Events, ListItem (tipo de control)
- compatibilidad con el tipo de control ListItem
- ListItem (tipo de control)
- tipos de control, estructura de árbol para el tipo de control ListItem
- tipos de control, patrones de control para el tipo de control ListItem
- tipos de control, compatibilidad con ListItem
- tipos de control, ListItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5093ef62793d96a5438c27edd29e96a96cfa407
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695303"
---
# <a name="listitem-control-type"></a>ListItem (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **ListItem** .

Los controles de elemento de lista son un ejemplo de controles que implementan el tipo de control **ListItem** .

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **ListItem** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de elemento de lista en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de elemento de lista y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>ListItem
<ul>
<li>Imagen (0 o más)</li>
<li>Text (0 o más)</li>
<li>Edición (0 o más)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ListItem</li>
</ul></td>
</tr>
</tbody>
</table>



 

Los elementos secundarios de un control de elemento de lista dentro de la vista de contenido del árbol de automatización de la interfaz de usuario deben mostrar siempre cero elementos secundarios. Si la estructura del control es tal que otros elementos están contenidos debajo del elemento de lista, debe seguir los requisitos de compatibilidad de UI Automation para el tipo de control [TreeItem](uiauto-supporttreeitemcontroltype.md) .

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **ListItem** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value        | Notas                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario. Asigne la propiedad **AutomationId** para un elemento de lista si se sabe que el elemento es coherente entre las distintas instancias de la interfaz de usuario. Si el elemento de lista se rellena dinámicamente y no es predecible, deje la propiedad **AutomationId** en blanco.                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El valor de esta propiedad debe incluir el área del contenido de imagen y texto del elemento de lista.                                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Depende      | Si el control de lista tiene un punto seleccionable (un punto en el que se puede hacer clic para que la lista tenga el foco), dicho punto se debe exponer a través de esta propiedad. Si el control de lista está completamente incluido en los elementos de la lista de descendientes, devolverá el error de [**\_ \_ NOCLICKABLEPOINT de UIA E**](uiauto-error-codes.md) indicará que el cliente debe solicitar un elemento dentro del control de lista para un punto en el que se pueda hacer clic. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ListItem** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas.   | El texto de ayuda para los controles de lista debe explicar por qué se le solicita al usuario que elija una opción en una lista de opciones, que es normalmente el mismo tipo de información presentada a través de una información sobre herramientas. Por ejemplo, "Seleccione un elemento para establecer la resolución de pantalla del monitor".                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | El control de lista siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | El control de lista siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el contenedor puede aceptar la entrada de teclado, este valor de propiedad debe ser **true**.                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Depende      | Esta propiedad debe devolver un valor para si el elemento de lista se desplaza actualmente en la vista dentro del contenedor primario que implementa el patrón de control [Scroll](uiauto-implementingscroll.md) .                                                                                                                                                                                                                                  |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Depende      | Si el control contiene un estado que se está actualizando dinámicamente, se debe admitir esta propiedad para que una tecnología de asistencia pueda recibir actualizaciones cuando cambie el estado del elemento.                                                                                                                                                                                                                                     |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Depende      | Esta propiedad se debe exponer para los controles de elemento de lista que representan un objeto subyacente. Estos controles de elemento de lista suelen tener un icono asociado al control que los usuarios se asocian con el objeto subyacente.                                                                                                                                                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.   | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada que corresponde al tipo de control **ListItem** . El valor predeterminado es "elemento de lista" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | El valor de la propiedad nombre de un control de elemento de lista procede de la etiqueta de texto del elemento.                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de elemento de lista. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico | Notas                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Si el elemento se puede manipular para mostrar u ocultar información, se debe implementar el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) .                                                                                                                                                                                                                        |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depende | Si se admite la navegación espacial de elemento a elemento en el contenedor de lista y el contenedor está organizado en filas y columnas, se debe implementar el patrón de control [GridItem](uiauto-implementinggriditem.md) .                                                                                                                                                                  |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Depende | Si el elemento tiene un comando que se puede ejecutar en él, independiente de la selección, se debe implementar el patrón de control [Invoke](uiauto-implementinginvoke.md) . Se trata normalmente de una acción asociada a hacer doble clic en el control de elemento de lista. Algunos ejemplos serían el inicio de un documento desde el explorador de Windows o la reproducción de un archivo de música en Microsoft Windows Media Player.        |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Depende | Si el elemento de lista se encuentra dentro de un contenedor que se puede desplazar, se debe implementar el patrón de control [ScrollItem](uiauto-implementingscrollitem.md) .                                                                                                                                                                                                                       |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depende | Un control de elemento de lista que admita la selección debe implementar el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) . Esto permite que los controles de elementos de lista transmitan cuando se seleccionan.                                                                                                                                                                             |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depende | Si el elemento de lista se puede activar y la acción no realiza un cambio de estado de selección, se debe implementar el patrón de control [Toggle](uiauto-implementingtoggle.md) .                                                                                                                                                                                                            |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depende | Si se puede editar el elemento, se debe implementar el patrón de control [Value](uiauto-implementingvalue.md) . Los cambios en el control de elemento de lista provocarán cambios en los valores de las propiedades de [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) y [**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md) . |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de elemento de lista deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                                | Notas                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ExpandCollapseExpandCollapseStatePropertyId. | Si el control admite el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) , debe admitir este evento. |
| [**\_InvokedEventId de invocación de UIA \_**](uiauto-event-ids.md)                                                                                  | Si el control admite el patrón de control [Invoke](uiauto-implementinginvoke.md) , debe admitir este evento.                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                              | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                          | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de ItemStatusPropertyId.                                            | Si el control admite la propiedad [**ItemStatus**](uiauto-automation-element-propids.md) , debe admitir este evento.        |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de NamePropertyId.                                                        |                                                                                                                                  |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento.   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento.   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ToggleToggleStatePropertyId.                                 | Si el control admite el patrón de control [Toggle](uiauto-implementingtoggle.md) , debe admitir este evento.                 |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ValueValuePropertyId.                                               | Si el control admite el patrón de control [Value](uiauto-implementingvalue.md) , debe admitir este evento.                   |



 

## <a name="remarks"></a>Observaciones

Si un contenedor hospeda elementos de lista, el medio principal de navegación debe ir a los elementos de la lista. Colocar el foco en subelementos a través de la navegación de lista puede resultar confuso para los usuarios y las herramientas de accesibilidad. Si el contenedor hospeda una lista vertical de elementos, al presionar las teclas flecha arriba y flecha abajo, se desplazará por los elementos, pero la flecha derecha y las teclas de flecha izquierda pueden desplazarse a los subelementos del elemento enfocado, como columnas de la lista o subelementos de la interfaz de usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




