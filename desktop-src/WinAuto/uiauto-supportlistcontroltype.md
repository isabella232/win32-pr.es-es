---
title: List (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control List.
ms.assetid: e4cde080-32d1-4150-a6be-8bd750e972c9
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control List
- UI Automation, List (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control List
- Automatización de la interfaz de usuario, propiedades para el tipo de control List
- Automatización de la interfaz de usuario, patrones de control para el tipo de control List
- Automatización de la interfaz de usuario, eventos para el tipo de control List
- estructuras de árbol, List (tipo de control)
- propiedades, List (tipo de control)
- patrones de control, List (tipo de control)
- Events, List (tipo de control)
- compatibilidad con el tipo de control List
- List (tipo de control)
- tipos de control, estructura de árbol para el tipo de control List
- tipos de control, patrones de control para el tipo de control List
- tipos de control, compatibilidad con la lista
- tipos de control, lista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a493418750bff1932fe933340b3eb2cb05829e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418636"
---
# <a name="list-control-type"></a>List (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **List** .

El tipo de control **List** proporciona una manera de organizar un grupo o grupos planos de elementos y permite al usuario seleccionar uno o varios de esos elementos. El tipo de control **List** tiene una restricción estricta sobre los tipos de elementos secundarios que puede contener. Esto permite que los proveedores de Automatización de la interfaz de usuario admitan un elemento conocido para los contenedores de selección.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **List** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de lista donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control y propiedades necesarios](#required-control-patterns-and-properties)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de lista y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<td>Contiene los elementos que corresponden a los controles.</td>
<td>Quita la información redundante del árbol para que las tecnologías de asistencia funcionen con el conjunto más pequeño de información que es significativo para el usuario final.</td>
</tr>
<tr class="even">
<td><ul>
<li>List
<ul>
<li>DataItem (0 o más)</li>
<li>Elemento de lista (0 o más)</li>
<li>Group (0 o más)</li>
<li>ScrollBar (0, 1 o 2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>List
<ul>
<li>DataItem (0 o más)</li>
<li>Elemento de lista (0 o más)</li>
<li>Group (0 o más)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

La vista de control de un control que implementa el tipo de control List (por ejemplo, un control de lista) consta de:

-   Cero o más elementos dentro del control de lista (los elementos pueden basarse en los tipos de control [ListItem](uiauto-supportlistitemcontroltype.md) o [DataItem](uiauto-supportdataitemcontroltype.md) )
-   Cero o más controles de grupo dentro de un control de lista
-   Cero, uno o dos controles de barra de desplazamiento

La vista de contenido de un control que implementa el tipo de control List (por ejemplo, un control de lista) consta de:

-   Cero o más elementos dentro del control de lista (los elementos pueden basarse en los tipos de control [ListItem](uiauto-supportlistitemcontroltype.md) o [DataItem](uiauto-supportdataitemcontroltype.md) )
-   Cero o más grupos dentro del control de lista

Un control de lista no debe disponer de elementos que tengan una relación jerárquica que no sea estar agrupados. Si los elementos tienen elementos secundarios en el árbol de automatización de la interfaz de usuario, el contenedor de lista debe basarse en el tipo de control de [árbol](uiauto-supporttreecontroltype.md) .

Los elementos seleccionables dentro del control de lista estarán disponibles en los descendientes del árbol de automatización de la interfaz de usuario del control de lista. Todos los elementos dentro del control de lista deben pertenecer al mismo grupo de selección. Los elementos seleccionables de la lista se deben exponer como tipos de control [ListItem](uiauto-supportlistitemcontroltype.md) (en lugar de [DataItem](uiauto-supportdataitemcontroltype.md)).

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **List** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Si el control de lista tiene un punto seleccionable (un punto en el que se puede hacer clic para que la lista tenga el foco), dicho punto se debe exponer a través de esta propiedad. Si el valor de la [**propiedad \_ IsOffscreenPropertyId de UIA**](uiauto-automation-element-propids.md) es **true**, el intento de recuperar esta propiedad produce el [**error \_ \_ NOCLICKABLEPOINT de UIA E**](uiauto-error-codes.md) .                      |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Lista**   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas. | El texto de ayuda para los controles de lista debe explicar por qué se solicita al usuario que realice una selección de una lista de opciones. Por ejemplo, "Seleccione un elemento de esta lista para establecer la resolución de pantalla del monitor".                                                                                                                                                                                                                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | El control de lista siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | El control de lista siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **List** . El valor predeterminado es "list" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El valor de la propiedad **nombre** de un control de lista debe indicar la categoría de opciones desde las que se solicita al usuario que seleccione. Esta propiedad suele recibir su nombre de una etiqueta de texto estático. Si no hay una etiqueta de texto estático, el desarrollador de aplicaciones debe exponer un valor para la propiedad **Name** .<br/> La única vez que esta propiedad no es necesaria para los controles de lista es si el control se utiliza dentro del subárbol de otro control.<br/> |



 

## <a name="required-control-patterns-and-properties"></a>Patrones de control y propiedades necesarios

En la tabla siguiente se muestran los patrones de control de UI Automation que se deben admitir por todos los controles de lista. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                             | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)                                | Depende       | Implemente el patrón de control [Grid](uiauto-implementinggrid.md) cuando sea necesario que la navegación por cuadrícula esté disponible en cada elemento.                                                                                                                                                                                                                                           |
| [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)                | Depende       | Implemente el patrón de control [MultipleView](uiauto-implementingmultipleview.md) si el control puede admitir varias vistas de los elementos del contenedor.                                                                                                                                                                                                                       |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depende       | Implemente el patrón de control [Scroll](uiauto-implementingscroll.md) si se pueden desplazar los elementos del contenedor.                                                                                                                                                                                                                                                                  |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Depende       | Si un control admite el tipo de control List que admite la selección, el control debe implementar el patrón de control [Selection](uiauto-implementingselection.md) cuando se mantenga un estado de selección entre los elementos contenidos en el control. Si los elementos del control no son seleccionables, se puede usar el tipo de control [Group](uiauto-supportgroupcontroltype.md) . |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Depende       | Los controles List pueden ser contenedores de selección única o múltiple.                                                                                                                                                                                                                                                                                                                    |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Depende       | Los controles List no siempre requieren que se seleccione un elemento.                                                                                                                                                                                                                                                                                                                    |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)                              | Nunca         | El patrón de control [TABLE](uiauto-implementingtable.md) nunca se admite para el tipo de control **List** . Si el control necesita admitir este patrón de control, el control debe basarse en el tipo de control [DataGrid](uiauto-supportdatagridcontroltype.md) .                                                                                                             |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                        | Notas                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                      |                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                      | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.     |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                  | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     | Si se puede cambiar el diseño de los elementos secundarios, el control debe admitir este evento.                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de MultipleViewCurrentViewPropertyId.             | Si el control admite el patrón de control [MultipleView](uiauto-implementingmultipleview.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontallyScrollablePropertyId.   | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalScrollPercentPropertyId. | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalViewSizePropertyId.           | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalScrollPercentPropertyId.     | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticallyScrollablePropertyId.       | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalViewSizePropertyId.               | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.             |
| [**\_InvalidatedEventId de selección de UIA \_**](uiauto-event-ids.md)                                                            | Si el control admite el patrón de control [Selection](uiauto-implementingselection.md) , debe admitir este evento.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 





