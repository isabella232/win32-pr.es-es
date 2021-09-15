---
title: Tipo de control TreeItem
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control TreeItem.
ms.assetid: 03d8a2a7-0b9a-41f8-a9d3-cebba9c25c63
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control TreeItem
- Automatización de la interfaz de usuario,Tipo de control TreeItem
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control TreeItem
- Automatización de la interfaz de usuario,properties para el tipo de control TreeItem
- Automatización de la interfaz de usuario,patrones de control para el tipo de control TreeItem
- Automatización de la interfaz de usuario,events para el tipo de control TreeItem
- estructuras de árbol, tipo de control TreeItem
- properties,TreeItem , tipo de control
- patrones de control, tipo de control TreeItem
- events,TreeItem , tipo de control
- compatibilidad con el tipo de control TreeItem
- Tipo de control TreeItem
- tipos de control, estructura de árbol para el tipo de control TreeItem
- tipos de control, patrones de control para el tipo de control TreeItem
- tipos de control, compatibilidad con TreeItem
- tipos de control, TreeItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07f55ab6d9df8af46253a2428964bdf4ded64c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465991"
---
# <a name="treeitem-control-type"></a>Tipo de control TreeItem

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **TreeItem.**

El tipo de control **TreeItem** representa un nodo dentro de un contenedor de árbol. Cada nodo puede contener otros nodos, llamados nodos secundarios. Los nodos primarios o los nodos que contienen nodos secundarios se pueden mostrar expandidos o contraídos.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **TreeItem.** Los Automatización de la interfaz de usuario se aplican a todos los controles de elementos de árbol en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de elementos de árbol y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario árbol, vea [Información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>TreeItem<ul><li>CheckBox (0 o 1)</li><li>Image (0 o 1)</li><li>Button (0 o 1)</li><li>TreeItem (0 o más)</li></ul></li></ul> | <ul><li>TreeItem<ul><li>TreeItem (0 o más)</li></ul></li></ul> | 




 

Los controles de elemento de árbol pueden tener cero o más elementos secundarios de elemento de árbol en la vista de contenido del Automatización de la interfaz de usuario árbol. Si el control de elemento de árbol tiene una funcionalidad más allá de lo que se expone en los patrones de control enumerados a continuación, el control debe basarse en el tipo de control [DataItem.](uiauto-supportdataitemcontroltype.md)

Los elementos de árbol contraídos no aparecen en la vista de control ni en la vista de contenido hasta que se expanden y se ven (o se pueden desplazar a la vista).

La vista de control puede contener detalles adicionales de un control, entre los que se incluyen una imagen asociada o un botón. Por ejemplo, un elemento de una vista Esquema podría contener una imagen, así como un botón para expandir o contraer el esquema. Estos objetos de detalle no aparecen en la vista de contenido porque la información ya está representada por el elemento de árbol primario.

Los elementos de árbol que se desplazan fuera de la pantalla aparecen en las vistas de control y contenido del árbol de Automatización de la interfaz de usuario y deben tener la propiedad [**IUIAutomationElement::CurrentIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisoffscreen) (o [**CachedIsOffscreen)**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedisoffscreen)establecida en **TRUE.**

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **TreeItem.** Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value        | Notas                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | Esta propiedad debe devolver una ubicación que haga que el elemento de árbol cambie el estado de selección o se centre.                                                                                   |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **TreeItem** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                 |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**     | El control de elemento de árbol siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario árbol.                                                                                                       |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**     | El control de elemento de árbol siempre se incluye en la vista de control del Automatización de la interfaz de usuario árbol.                                                                                                       |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                     |
| [**IsOffscreenPropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | Vea las notas.   | Esta propiedad indica si un control de elemento de árbol se desplaza fuera de la pantalla.                                                                                                               |
| [**ItemStatusPropertyId de UIA \_**](uiauto-automation-element-propids.md)                     | Vea las notas.   | Si el control contiene el estado que se está actualizando dinámicamente, esta propiedad debe ser compatible para que una tecnología de asistencia pueda recibir actualizaciones cuando cambie el estado del elemento. |
| [**ItemTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                         | Vea las notas.   | Si el control de elemento de árbol usa un icono visual para indicar que es un tipo determinado de elemento, esta propiedad debe ser compatible y debe indicar el tipo de elemento.                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | **NULL**     | Los controles de elemento de árbol se etiquetan automáticamente.                                                                                                                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada que corresponde al tipo de control TreeItem. El valor predeterminado es "elemento de árbol" para en-US o inglés (Estados Unidos).                                                           |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | Esta propiedad expone el texto que se muestra para cada control de elemento de árbol.                                                                                                                          |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de elemento de árbol. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                                  | Soporte técnico/valor                     | Notas                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)                 | Obligatorio                          | Todos los elementos de árbol deben admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) porque todos los elementos se pueden expandir o contraer.                                           |
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) | Expanded, Collapsed o Leaf Node | Los elementos de árbol son nodos hoja cuando no se expanden ni se contraen.                                                                                                                                |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                                 | Depende                           | Implemente [el patrón de](uiauto-implementinginvoke.md) control Invoke si el elemento de árbol puede realizar un comando.                                                                                     |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)                         | Depende                           | Implemente el patrón de control [ScrollItem](uiauto-implementingscrollitem.md) si el contenedor de árbol admite el patrón de control [Scroll.](uiauto-implementingscroll.md)                         |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                   | Depende                           | Implemente el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) si es posible tener una selección activa que se mantenga cuando el usuario vuelva al contenedor de árbol. |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)    | Obligatorio                          | Esta propiedad expone el mismo contenedor para todos los elementos del contenedor.                                                                                                                      |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de elementos de árbol son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                                | Notas                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                                   |                                                                                                                                |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                |
| [**UIA \_ Evento expandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) cambiado por la propiedad . |                                                                                                                                |
| [**Invoke \_ InvokedEventId de UIA \_**](uiauto-event-ids.md)                                                                                  | Si el control admite el patrón de control [Invoke,](uiauto-implementinginvoke.md) debe admitir este evento.               |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.       |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento.     |
| [**UIA \_ Evento de cambio de propiedad ItemStatusPropertyId.**](uiauto-automation-element-propids.md)                                            | Si el control admite la [**propiedad ItemStatus,**](uiauto-automation-element-propids.md) debe admitir este evento.      |
| [**UIA \_ Evento de cambio de propiedad MultipleViewCurrentViewPropertyId.**](uiauto-control-pattern-propids.md)                     | Si el control admite el patrón de control [MultipleView,](uiauto-implementingmultipleview.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad NamePropertyId.**](uiauto-automation-element-propids.md)                                                        |                                                                                                                                |
| [**Elemento \_ SelectionItem \_ de UIAAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento. |
| [**Elemento \_ SelectionItem de \_ UIARemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento. |
| [**Elementos \_ SelectionItem \_ de UIASelectedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                |
| [**UIA \_ Evento de cambio de propiedad ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)                                 | Si el control admite el patrón de control [Toggle,](uiauto-implementingtoggle.md) debe admitir este evento.               |
| [**UIA \_ Evento de cambio de propiedad ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                                               | Si el control admite el [patrón de](uiauto-implementingvalue.md) control Valor, debe admitir este evento.                 |



 

## <a name="remarks"></a>Observaciones

Si un elemento de árbol tiene subelementos que no son nodos de esquema secundarios, el proveedor debe controlar la información del objeto secundario con cuidado y claridad. En Automatización de la interfaz de usuario, la propia jerarquía de árbol controla la estructura de árbol. Al tener uno o varios elementos secundarios que no son de esquema, las diferencias entre ellos y los nodos de esquema secundarios reales se vuelven muy ambiguas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




