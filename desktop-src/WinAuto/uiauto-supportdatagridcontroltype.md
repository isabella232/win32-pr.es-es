---
title: DataGrid (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control DataGrid.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control DataGrid
- Automatización de la interfaz de usuario, tipo de control DataGrid
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control DataGrid
- Automatización de la interfaz de usuario, propiedades para el tipo de control DataGrid
- Automatización de la interfaz de usuario, patrones de control para el tipo de control DataGrid
- Automatización de la interfaz de usuario, eventos para el tipo de control DataGrid
- estructuras de árbol, tipo de control DataGrid
- Properties, DataGrid (tipo de control)
- patrones de control, DataGrid (tipo de control)
- Events, DataGrid (tipo de control)
- compatibilidad con el tipo de control DataGrid
- DataGrid (tipo de control)
- tipos de control, estructura de árbol para el tipo de control DataGrid
- tipos de control, patrones de control para el tipo de control DataGrid
- tipos de control, compatibilidad con DataGrid
- tipos de control, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8af1e35e062c778285d1cb7edcca9ac6192792b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994163"
---
# <a name="datagrid-control-type"></a>DataGrid (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **DataGrid** .

El tipo de control **DataGrid** permite a un usuario trabajar fácilmente con elementos que contienen datos o elementos de automatización presentados en columnas o filas. Los controles de cuadrícula de datos tienen filas de elementos y columnas de información sobre esos elementos. Un control de vista de lista en el explorador de Windows Vista es un ejemplo que admite el tipo de control **DataGrid** .

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **DataGrid** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de cuadrícula de datos donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y los patrones

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Ejemplo de tipo de control DataGrid](#datagrid-control-type-example)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de cuadrícula de datos y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>DataGrid
<ul>
<li>Header (0, 1 o 2)
<ul>
<li>HeaderItem (número de columnas o filas)</li>
</ul></li>
<li>DataItem (0 o más; se puede estructurar en una jerarquía)</li>
</ul></li>
</ul></td>
<td><ul>
<li>DataGrid
<ul>
<li>DataItem (0 o más; se puede estructurar en una jerarquía)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **DataGrid** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value        | Notas                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | Se admite si hay un rectángulo delimitador. Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.                                                                                                         |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataGrid** |                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | El valor de esta propiedad siempre debe ser **true**. Esto significa que el control de cuadrícula de datos siempre debe estar en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | El valor de esta propiedad siempre debe ser **true**. Esto significa que el control de cuadrícula de datos siempre debe estar incluido en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.   | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada que corresponde al tipo de control **DataGrid** . El valor predeterminado es "Data Grid" para en-US o inglés (Estados Unidos).                                                                                                                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | Normalmente, el control de cuadrícula de datos obtiene el valor de su propiedad **Name** de una etiqueta de texto estático. Si no hay una etiqueta de texto estático, un desarrollador de aplicaciones debe asignar un valor a para la propiedad **Name** . El valor de la propiedad **Name** nunca debe ser el contenido textual del control de edición. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de cuadrícula de datos. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico  | Notas                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obligatorio | El propio control de cuadrícula de datos siempre admite el patrón de control [Grid](uiauto-implementinggrid.md) porque los elementos que contiene tienen metadatos que se colocan en una cuadrícula. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depende  | La capacidad de desplazar la cuadrícula de datos depende del contenido y de si las barras de desplazamiento están presentes.                                                                                       |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Depende  | La capacidad de seleccionar la cuadrícula de datos depende del contenido.                                                                                                                           |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Depende  | Un control de cuadrícula de datos que tiene un encabezado debe admitir el patrón de control [TABLE](uiauto-implementingtable.md) .                                                                   |



 

Los elementos de datos dentro de los contenedores de la cuadrícula de datos admitirán como mínimo:

-   Patrón de control [SelectionItem](uiauto-implementingselectionitem.md) (si la cuadrícula de datos es seleccionable)
-   Patrón de control [ScrollItem](uiauto-implementingscrollitem.md) (si la cuadrícula de datos es desplazable)
-   [GridItem](uiauto-implementinggriditem.md) (patrón de control)
-   Patrón de control [TableItem](uiauto-implementingtableitem.md) (si la cuadrícula de datos tiene un encabezado)

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de cuadrícula de datos deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                        | Notas                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                      |                                                                                                                                                          |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                      | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.                                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                  | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.                               |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de MultipleViewCurrentViewPropertyId.             | Si el control admite la propiedad CurrentView del patrón de control [MultipleView](uiauto-implementingmultipleview.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontallyScrollablePropertyId.   | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalScrollPercentPropertyId. | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalViewSizePropertyId.           | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalScrollPercentPropertyId.     | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticallyScrollablePropertyId.       | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalViewSizePropertyId.               | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.                                         |
| [**\_InvalidatedEventId de selección de UIA \_**](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a>Ejemplo de tipo de control DataGrid

En la imagen siguiente se muestra un control de vista de lista que implementa el tipo de control **DataGrid** .

![captura de pantalla del control de vista de lista con el tipo de control DataGrid](images/datagridxmpl.jpg)

A continuación se muestra la vista de control y la vista de contenido del árbol de automatización de la interfaz de usuario que pertenece al control de vista de lista. Los patrones de control de cada elemento de automatización se muestran entre paréntesis.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Árbol de automatización de la interfaz de usuario (vista de control)</th>
<th>Árbol de UI Automation: vista de contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DataGrid (ordenar, tabla, selección, cuadrícula)
<ul>
<li>Encabezado
<ul>
<li>Nombre de HeaderItem &quot; &quot; (Invoke)</li>
<li>HeaderItem &quot; fecha de modificación &quot; (Invoke)</li>
<li>Tamaño de HeaderItem &quot; &quot; (Invoke)</li>
</ul></li>
<li>Grupo &quot; contoso &quot; (TableItem, GridItem, SelectionItem, TABLE *, Grid*)
<ul>
<li>&quot;Receivable.doc&quot; de cuentas de DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</li>
<li>&quot;Payable.doc&quot; de cuentas de DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</li>
</ul></li>
</ul></td>
<td>DataGrid (Table, Grid, Selection)
<ul>
<li>Grupo &quot; contoso &quot; (TableItem, GridItem, SelectionItem, TABLE *, Grid*)
<ul>
<li>&quot;Receivable.doc&quot; de cuentas de DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</li>
<li>&quot;Payable.doc&quot; de cuentas de DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

\*En el ejemplo anterior se muestra una cuadrícula de datos que contiene varios niveles de controles. El control **Group** ("Contoso") contiene dos controles **DataItem** ("accounts Receivable.doc" y "accounts Payable.doc"). Un par **DataGrid** / **GridItem** es independiente de un par en otro nivel. Los controles **DataItem** de un **Grupo** también se pueden exponer como un tipo de control [ListItem](uiauto-supportlistitemcontroltype.md) , lo que permite que se presenten más claramente como objetos seleccionables, en lugar de como elementos de datos simples. En este ejemplo no se incluyen los subelementos de los elementos de datos agrupados. Para obtener otro ejemplo de varios niveles de controles, vea el tipo de control [DataItem](uiauto-supportdataitemcontroltype.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




