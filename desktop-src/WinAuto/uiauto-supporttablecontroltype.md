---
title: Table (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Table.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Table
- Automatización de la interfaz de usuario, Table (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Table
- Automatización de la interfaz de usuario, propiedades para el tipo de control Table
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Table
- Automatización de la interfaz de usuario, eventos para el tipo de control Table
- estructuras de árbol, Table (tipo de control)
- propiedades, Table (tipo de control)
- patrones de control, Table (tipo de control)
- Events, Table (tipo de control)
- compatibilidad con el tipo de control Table
- Table (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Table
- tipos de control, patrones de control para el tipo de control Table
- tipos de control, compatibilidad con tablas
- tipos de controles, tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4ee709bd16156a62882aeee014b4744dab2214
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532308"
---
# <a name="table-control-type"></a>Table (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **TABLE** .

Los controles de tabla contienen filas y columnas de texto y, opcionalmente, encabezados de fila y encabezados de columna.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **TABLE** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de tabla donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de tabla y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Tabla
<ul>
<li>Text (0 o 1)</li>
<li>Encabezado (0 o más)</li>
<li>Varios controles (0 o más)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Tabla
<ul>
<li>Texto (1 o más)</li>
<li>Varios controles (0 o más)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Si un control de tabla tiene encabezados de fila o columna, se deben exponer en la vista de control del árbol de automatización de la interfaz de usuario. La vista de contenido no tiene que exponer esta información porque se puede tener acceso a ella mediante [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de tabla. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Se admite si hay un rectángulo delimitador. Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.                              |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Table**  |                                                                                                                                                                                                                                   |
| [**UIA \_ DescribedByPropertyId**](uiauto-automation-element-propids.md)                   | Vea las notas. | Si la tabla se anota por otro elemento de la interfaz de usuario (por ejemplo, un elemento de texto que contiene la descripción de la tabla), la propiedad DescribedBy debería exponer una referencia al elemento de automatización del control de texto.           |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas. | Se deben exponer más detalles sobre la finalidad de la tabla a través de esta propiedad si la propiedad [**\_ NamePropertyId de UIA**](uiauto-automation-element-propids.md) no lo explica suficientemente.      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control de tabla siempre debe aparecer en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control de tabla siempre debe aparecer en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia al elemento de automatización del control.                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **TABLE** . El valor predeterminado es "Table" para en-US o inglés (Estados Unidos).                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | Normalmente, el control de tabla obtiene el valor de su nombre de una etiqueta de texto estático. Si no hay una etiqueta de texto estático, el elemento debe asignar una propiedad Name que siempre debe estar disponible para explicar la finalidad de la tabla. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de tabla. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico                     | Notas                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obligatorio                    | Dado que el control de tabla contiene elementos presentados en una cuadrícula, siempre admite el patrón de control [Grid](uiauto-implementinggrid.md) .                                                                                                                                                    |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Requerido con objetos secundarios | Los objetos internos de una tabla deben admitir los patrones de control [GridItem](uiauto-implementinggriditem.md) y [TableItem](uiauto-implementingtableitem.md) . La propia tabla no necesita admitir el patrón de control GridItem o TableItem, a menos que la tabla forme parte de otra tabla.  |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Obligatorio                    | El control de tabla siempre puede tener encabezados asociados al contenido.                                                                                                                                                                                                                       |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Requerido con objetos secundarios | Los objetos internos de una tabla deben admitir los patrones de control [GridItem](uiauto-implementinggriditem.md) y [TableItem](uiauto-implementingtableitem.md) . La propia tabla no necesita admitir los patrones de control GridItem o TableItem, a menos que la tabla forme parte de otra tabla. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de tabla deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



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

 

 




