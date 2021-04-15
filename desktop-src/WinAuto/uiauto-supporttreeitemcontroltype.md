---
title: Tipo de control TreeItem
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control TreeItem.
ms.assetid: 03d8a2a7-0b9a-41f8-a9d3-cebba9c25c63
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control TreeItem
- Automatización de la interfaz de usuario, tipo de control TreeItem
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control TreeItem
- Automatización de la interfaz de usuario, propiedades para el tipo de control TreeItem
- Automatización de la interfaz de usuario, patrones de control para el tipo de control TreeItem
- Automatización de la interfaz de usuario, eventos para el tipo de control TreeItem
- estructuras de árbol, tipo de control TreeItem
- propiedades, tipo de control TreeItem
- patrones de control, TreeItem (tipo de control)
- Events, TreeItem (tipo de control)
- compatibilidad con el tipo de control TreeItem
- Tipo de control TreeItem
- tipos de control, estructura de árbol para el tipo de control TreeItem
- tipos de control, patrones de control para el tipo de control TreeItem
- tipos de control, compatibilidad con TreeItem
- tipos de control, TreeItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c837428a0aeef900779cfccf0a28b46aa276369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714211"
---
# <a name="treeitem-control-type"></a>Tipo de control TreeItem

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **TreeItem** .

El tipo de control **TreeItem** representa un nodo dentro de un contenedor de árbol. Cada nodo puede contener otros nodos, llamados nodos secundarios. Los nodos primarios o los nodos que contienen nodos secundarios se pueden mostrar expandidos o contraídos.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **TreeItem** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de elemento de árbol donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de elemento de árbol y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>TreeItem
<ul>
<li>CheckBox (0 o 1)</li>
<li>Image (0 o 1)</li>
<li>Button (0 o 1)</li>
<li>TreeItem (0 o más)</li>
</ul></li>
</ul></td>
<td><ul>
<li>TreeItem
<ul>
<li>TreeItem (0 o más)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Los controles de elemento de árbol pueden tener cero o más elementos secundarios de elemento de árbol en la vista de contenido del árbol de automatización de la interfaz de usuario. Si el control de elemento de árbol tiene una funcionalidad más allá de lo expuesto en los patrones de control enumerados a continuación, el control debe basarse en el tipo de control [DataItem](uiauto-supportdataitemcontroltype.md) .

Los elementos de árbol contraídos no aparecen en la vista de control ni en la vista de contenido hasta que se expanden y se ven (o se pueden desplazar en la vista).

La vista de control puede contener detalles adicionales de un control, entre los que se incluyen una imagen asociada o un botón. Por ejemplo, un elemento de una vista Esquema podría contener una imagen, así como un botón para expandir o contraer el esquema. Estos objetos de detalle no aparecen en la vista de contenido porque la información ya está representada por el elemento de árbol primario.

Los elementos de árbol que se desplazan fuera de la pantalla aparecen en las vistas de control y de contenido del árbol de automatización de la interfaz de usuario y deben tener la propiedad [**IUIAutomationElement:: CurrentIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisoffscreen) (o [**CachedIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedisoffscreen)) establecida en **true**.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **TreeItem** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value        | Notas                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | Esta propiedad debe devolver una ubicación que haga que el elemento de árbol cambie el estado de selección o se convierta en el foco.                                                                                   |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TreeItem** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                 |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | El control de elemento de árbol siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                       |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | El control de elemento de árbol siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                       |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                     |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Vea las notas.   | Esta propiedad indica si un control de elemento de árbol se desplaza fuera de la pantalla.                                                                                                               |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Vea las notas.   | Si el control contiene un estado que se está actualizando dinámicamente, se debe admitir esta propiedad para que una tecnología de asistencia pueda recibir actualizaciones cuando cambie el estado del elemento. |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas.   | Si el control de elemento de árbol utiliza un icono visual para indicar que es un tipo de elemento determinado, esta propiedad debe admitirse y debe indicar el tipo de elemento.                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | **NULL**     | Los controles de elemento de árbol se etiquetan automáticamente.                                                                                                                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada que corresponde al tipo de control TreeItem. El valor predeterminado es "elemento de árbol" para en-US o inglés (Estados Unidos).                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | Esta propiedad expone el texto que se muestra para cada control de elemento de árbol.                                                                                                                          |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de elemento de árbol. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                                  | Soporte técnico/valor                     | Notas                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)                 | Obligatorio                          | Todos los elementos de árbol deben admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) porque todos los elementos se pueden expandir o contraer.                                           |
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) | Expanded, Collapsed o Leaf Node | Los elementos de árbol son nodos hoja cuando no se expandan o contraigan.                                                                                                                                |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                                 | Depende                           | Implemente el patrón de control [Invoke](uiauto-implementinginvoke.md) si el elemento de árbol puede ejecutar un comando.                                                                                     |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)                         | Depende                           | Implemente el patrón de control [ScrollItem](uiauto-implementingscrollitem.md) si el contenedor de árbol admite el patrón de control [Scroll](uiauto-implementingscroll.md) .                         |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                   | Depende                           | Implemente el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) si es posible tener una selección activa que se mantenga cuando el usuario vuelva al contenedor de árbol. |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)    | Obligatorio                          | Esta propiedad expone el mismo contenedor para todos los elementos del contenedor.                                                                                                                      |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que deben admitir los controles de elemento de árbol. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                                | Notas                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                              |                                                                                                                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ExpandCollapseExpandCollapseStatePropertyId. |                                                                                                                                |
| [**\_InvokedEventId de invocación de UIA \_**](uiauto-event-ids.md)                                                                                  | Si el control admite el patrón de control [Invoke](uiauto-implementinginvoke.md) , debe admitir este evento.               |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                              | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                          | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.     |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de ItemStatusPropertyId.                                            | Si el control admite la propiedad [**ItemStatus**](uiauto-automation-element-propids.md) , debe admitir este evento.      |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de MultipleViewCurrentViewPropertyId.                     | Si el control admite el patrón de control [MultipleView](uiauto-implementingmultipleview.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de NamePropertyId.                                                        |                                                                                                                                |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento. |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento. |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ToggleToggleStatePropertyId.                                 | Si el control admite el patrón de control [Toggle](uiauto-implementingtoggle.md) , debe admitir este evento.               |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ValueValuePropertyId.                                               | Si el control admite el patrón de control [Value](uiauto-implementingvalue.md) , debe admitir este evento.                 |



 

## <a name="remarks"></a>Observaciones

Si un elemento de árbol tiene subelementos distintos de los nodos de esquema secundarios, el proveedor debe administrar la información del objeto secundario detenidamente y claramente. En la automatización de la interfaz de usuario, la estructura de árbol se controla mediante la propia jerarquía de árbol. Al tener uno o más elementos secundarios que no son de nodo de esquema, las diferencias entre ellos y los nodos de esquema secundarios reales pasan a ser gravemente ambiguas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




