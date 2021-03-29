---
title: Tree (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Tree.
ms.assetid: 0fa8f308-7815-4561-a1ce-c5f5582861da
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Tree
- Automatización de la interfaz de usuario, tipo de control de árbol
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Tree
- Automatización de la interfaz de usuario, propiedades para el tipo de control Tree
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Tree
- Automatización de la interfaz de usuario, eventos para el tipo de control Tree
- estructuras de árbol, tipo de control de árbol
- propiedades, tipo de control Tree
- patrones de control, tipo de control Tree
- Events, Tree (tipo de control)
- compatibilidad con el tipo de control Tree
- Tree (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Tree
- tipos de control, patrones de control para el tipo de control Tree
- tipos de control, compatibilidad con árbol
- tipos de control, árbol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4679af32f974cd1611cbd31c71e66db62631391
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078190"
---
# <a name="tree-control-type"></a>Tree (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Tree** .

El tipo de control **Tree** se usa para los contenedores cuyo contenido tiene relevancia como una jerarquía de nodos, como con la manera en que se muestran los archivos y las carpetas en el panel izquierdo del explorador de Windows. Cada nodo tiene el potencial de contener otros nodos, denominados nodos secundarios. Los nodos primarios o los nodos que contienen nodos secundarios se pueden mostrar expandidos o contraídos. El control de vista de árbol de Windows (tal y como lo identifica el [**\_ TREEVIEW de CT**](/windows/desktop/Controls/common-control-window-classes)) es un ejemplo de un control que pertenece al tipo de control de **árbol** .

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario necesaria, las propiedades, los patrones de control y los eventos para el tipo de control **Tree** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de elemento de árbol donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de árbol y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Árbol
<ul>
<li>DataItem (0 o más)</li>
<li>TreeItem (0 o más)
<ul>
<li>TreeItem (0 o más)
<ul>
<li>...</li>
</ul></li>
</ul></li>
<li>ScrollBar (0, 1, 2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Árbol
<ul>
<li>DataItem (0 o más)</li>
<li>TreeItem (0 o más)
<ul>
<li>TreeItem (0 o más)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

La vista de control del árbol de automatización de la interfaz de usuario consta de:

-   Cero de muchos elementos dentro del contenedor (los elementos se pueden basar en los tipos de control [TreeItem](uiauto-supporttreeitemcontroltype.md) o [DataItem](uiauto-supportdataitemcontroltype.md) ).
-   Cero, uno o dos controles de barra de desplazamiento

La vista de contenido del árbol de automatización de la interfaz de usuario consta de cero o muchos elementos dentro del contenedor (los elementos se pueden basar en los tipos de control [TreeItem](uiauto-supporttreeitemcontroltype.md) o [DataItem](uiauto-supportdataitemcontroltype.md) ).

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **Tree** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Los controles de árbol tienen un punto en el que se pueda hacer clic que hace que el árbol o uno de los elementos del contenedor de árbol reciba el foco. Un control de árbol solo puede tener un punto seleccionable si es posible hacer clic en una ubicación del árbol sin hacer que se seleccione un elemento o recibir el foco. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Árbol**   | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control de árbol siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                         |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control de árbol siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si el control de árbol tiene una etiqueta asociada, esta propiedad devuelve un puntero [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para esa etiqueta. De lo contrario, la propiedad devuelve una referencia nula.                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **Tree** . El valor predeterminado es "Tree" para en-US o inglés (Estados Unidos).                                                                                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El valor de la propiedad del nombre de un control de árbol normalmente procede del texto que etiqueta el control. Si no hay ninguna etiqueta de texto, debe proporcionar un valor para esta propiedad.                                                                                                                        |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se muestran los patrones de control de UI Automation que se deben admitir por todos los controles de árbol. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                             | Soporte técnico/valor | Notas                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depende       | Implemente el patrón de control [Scroll](uiauto-implementingscroll.md) si se pueden desplazar los elementos del contenedor de árbol.                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Depende       | Los controles de árbol que contienen un conjunto de elementos seleccionables deben implementar el patrón de control [Selection](uiauto-implementingselection.md) . No es necesario que se implemente si la selección de un elemento no transmite información significativa al usuario. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Vea las notas.    | Implemente esta propiedad si el control del árbol admite selección múltiple (la mayoría de los controles de árbol admiten selección múltiple).                                                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Vea las notas.    | El valor de esta propiedad se expone si el control requiere que se seleccione un elemento.                                                                                                                                               |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que todos los controles de árbol deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                        | Notas                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                      | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                  | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontallyScrollablePropertyId.   | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalScrollPercentPropertyId. | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalViewSizePropertyId.           | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalScrollPercentPropertyId.     | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticallyScrollablePropertyId.       | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalViewSizePropertyId.               | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**\_InvalidatedEventId de selección de UIA \_**](uiauto-event-ids.md)                                                            | Si el control admite el patrón de control [Selection](uiauto-implementingselection.md) , debe admitir este evento.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 