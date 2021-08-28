---
title: Tipo de control DataGrid
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control DataGrid.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control DataGrid
- Automatización de la interfaz de usuario, tipo de control DataGrid
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control DataGrid
- Automatización de la interfaz de usuario,properties para el tipo de control DataGrid
- Automatización de la interfaz de usuario, patrones de control para el tipo de control DataGrid
- Automatización de la interfaz de usuario,events para el tipo de control DataGrid
- estructuras de árbol, tipo de control DataGrid
- properties,Tipo de control DataGrid
- patrones de control, tipo de control DataGrid
- events,Tipo de control DataGrid
- Compatibilidad con el tipo de control DataGrid
- Tipo de control DataGrid
- tipos de control, estructura de árbol para el tipo de control DataGrid
- tipos de control, patrones de control para el tipo de control DataGrid
- tipos de control, compatibilidad con DataGrid
- tipos de control, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa37093402fc3c4c195b4b68ecc74652af2d6a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475601"
---
# <a name="datagrid-control-type"></a>Tipo de control DataGrid

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **DataGrid.**

El tipo de control **DataGrid** permite a un usuario trabajar fácilmente con elementos que contienen datos o elementos de automatización presentados en columnas o filas. Los controles de cuadrícula de datos tienen filas de elementos y columnas de información sobre esos elementos. Un control de vista de lista en Windows Explorador de Vista es un ejemplo que admite el tipo de control **DataGrid.**

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **DataGrid.** Los Automatización de la interfaz de usuario se aplican a todos los controles de cuadrícula de datos en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Ejemplo de tipo de control DataGrid](#datagrid-control-type-example)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece a los controles de cuadrícula de datos y se describe lo que se puede incluir en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>DataGrid<ul><li>Header (0, 1 o 2)<ul><li>HeaderItem (número de columnas o filas)</li></ul></li><li>DataItem (0 o más; se puede estructurar en una jerarquía)</li></ul></li></ul> | <ul><li>DataGrid<ul><li>DataItem (0 o más; se puede estructurar en una jerarquía)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **DataGrid.** Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor        | Notas                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic.                                                                                                         |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **DataGrid** |                                                                                                                                                                                                                                                                                                              |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE         | El valor de esta propiedad siempre debe ser **TRUE.** Esto significa que el control de cuadrícula de datos siempre debe estar en la vista de contenido del Automatización de la interfaz de usuario datos.                                                                                                                                                      |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE         | El valor de esta propiedad siempre debe **ser TRUE.** Esto significa que el control de cuadrícula de datos siempre debe incluirse en la vista de control del Automatización de la interfaz de usuario datos.                                                                                                                                                |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.   | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada correspondiente al tipo de control **DataGrid.** El valor predeterminado es "cuadrícula de datos" para en-US o inglés (Estados Unidos).                                                                                                                                                                      |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | El control de cuadrícula de datos normalmente obtiene el valor de su **propiedad Name** de una etiqueta de texto estático. Si no hay una etiqueta de texto estático, un desarrollador de aplicaciones debe asignar un valor a para la **propiedad Name.** El valor de la **propiedad Name** nunca debe ser el contenido textual del control de edición. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de cuadrícula de datos. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico  | Notas                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Requerido | El propio control de cuadrícula de datos siempre admite el [patrón de](uiauto-implementinggrid.md) control Grid porque los elementos que contiene tienen metadatos que se disponen en una cuadrícula. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depende  | La capacidad de desplazar la cuadrícula de datos depende del contenido y de si las barras de desplazamiento están presentes.                                                                                       |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Depende  | La capacidad de seleccionar la cuadrícula de datos depende del contenido.                                                                                                                           |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Depende  | Un control de cuadrícula de datos que tenga un encabezado debe admitir el [patrón de](uiauto-implementingtable.md) control Tabla.                                                                   |



 

Los elementos de datos dentro de los contenedores de la cuadrícula de datos admitirán como mínimo:

-   Patrón de control [SelectionItem](uiauto-implementingselectionitem.md) (si se puede seleccionar la cuadrícula de datos)
-   Patrón de control [ScrollItem](uiauto-implementingscrollitem.md) (si la cuadrícula de datos se puede desplazar)
-   Patrón de control [GridItem](uiauto-implementinggriditem.md)
-   Patrón de control [TableItem](uiauto-implementingtableitem.md) (si la cuadrícula de datos tiene un encabezado)

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de cuadrícula de datos son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                        | Notas                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                                                          |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.                                 |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento.                               |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| [**UIA \_ Evento de cambio de propiedad MultipleViewCurrentViewPropertyId.**](uiauto-control-pattern-propids.md)             | Si el control admite la propiedad CurrentView del patrón de control [MultipleView,](uiauto-implementingmultipleview.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                         |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                         |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                         |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                         |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                         |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                         |
| [**Selección de UIA \_ \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a>Ejemplo de tipo de control DataGrid

En la imagen siguiente se muestra un control de vista de lista que implementa el tipo de control **DataGrid.**

![captura de pantalla del control list-view con el tipo de control datagrid](images/datagridxmpl.jpg)

A continuación se muestran la vista de control y la vista de contenido del árbol de Automatización de la interfaz de usuario que pertenece al control list-view. Los patrones de control de cada elemento de automatización se muestran entre paréntesis.




| Automatización de la interfaz de usuario árbol de control: Vista de control | Automatización de la interfaz de usuario árbol de contenido: vista de contenido | 
|-----------------------------------|-----------------------------------|
| DataGrid (Sort, Table, Selection, Grid)<ul><li>Encabezado<ul><li>HeaderItem "Name" (Invoke)</li><li>HeaderItem "Date Modified" (Invoke)</li><li>HeaderItem "Size" (Invoke)</li></ul></li><li>Group "Contoso" (TableItem, GridItem, SelectionItem, Table *, Grid*)<ul><li>DataItem "Accounts Receivable.doc" (SelectionItem, Invoke, TableItem *, GridItem*)</li><li>DataItem "Accounts Payable.doc" (SelectionItem, Invoke, TableItem *, GridItem*)</li></ul></li></ul> | DataGrid (Table, Grid, Selection)<ul><li>Group "Contoso" (TableItem, GridItem, SelectionItem, Table *, Grid*)<ul><li>DataItem "Accounts Receivable.doc" (SelectionItem, Invoke, TableItem *, GridItem*)</li><li>DataItem "Accounts Payable.doc" (SelectionItem, Invoke, TableItem *, GridItem*)</li></ul></li></ul> | 




 

\*En el ejemplo anterior se muestra una cuadrícula de datos que contiene varios niveles de controles. El **control Group** ("Contoso") contiene dos controles **DataItem** ("Accounts Receivable.doc" y "Accounts Payable.doc"). Un **par GridItem** de DataGrid es independiente de un par en otro /  nivel. Los **controles DataItem** de un **grupo** también se pueden exponer como un tipo de control [ListItem,](uiauto-supportlistitemcontroltype.md) lo que permite que se presenten más claramente como objetos seleccionables, en lugar de como elementos de datos simples. En este ejemplo no se incluyen los subelementos de los elementos de datos agrupados. Para obtener otro ejemplo de varios niveles de controles, vea el tipo de control [DataItem.](uiauto-supportdataitemcontroltype.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




