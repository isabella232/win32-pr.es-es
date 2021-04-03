---
title: DataItem (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control DataItem.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control DataItem
- Automatización de la interfaz de usuario, tipo de control DataItem
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control DataItem
- UI Automation, propiedades para el tipo de control DataItem
- Automatización de la interfaz de usuario, patrones de control para el tipo de control DataItem
- Automatización de la interfaz de usuario, eventos para el tipo de control DataItem
- Automatización de la interfaz de usuario, listas grandes y tipo de control DataItem
- estructuras de árbol, tipo de control DataItem
- Properties, DataItem (tipo de control)
- patrones de control, tipo de control DataItem
- Events, DataItem (tipo de control)
- listas grandes
- compatibilidad con el tipo de control DataItem
- DataItem (tipo de control)
- tipos de control, estructura de árbol para el tipo de control DataItem
- tipos de control, patrones de control para el tipo de control DataItem
- tipos de control, listas grandes y tipo de control DataItem
- tipos de control, compatibilidad con DataItem
- tipos de control, DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0902cc593ec7f9104ed27031caa2785b7cb9756
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075617"
---
# <a name="dataitem-control-type"></a>DataItem (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **DataItem** .

Una entrada de una lista de contactos es un ejemplo de un control de elemento de datos. Un control de elemento de datos contiene información de interés para un usuario final. Es más complicado que el elemento de lista simple porque contiene información más completa.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **DataItem** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de elemento de datos donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y los patrones

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Trabajar con elementos de trabajo en listas grandes](#working-with-dataitems-in-large-lists)
-   [Eventos necesarios](#required-events)
-   [Ejemplo de tipo de control DataItem](#dataitem-control-type-example)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de elemento de datos y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>DataItem
<ul>
<li>Varía (0 o más; se puede estructurar en jerarquía)</li>
</ul></li>
</ul></td>
<td><ul>
<li>DataItem
<ul>
<li>Varía (0 o más; se puede estructurar en jerarquía)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Un elemento de datos de una cuadrícula de datos puede hospedar diversos objetos, entre los que se incluye otra capa de elementos de datos o elementos de cuadrícula concretos como controles de edición, texto o imágenes. Si el elemento de datos tiene un rol de objeto concreto, el elemento debe exponerse como un tipo de control concreto; por ejemplo, un tipo de control [ListItem](uiauto-supportlistitemcontroltype.md) para un elemento de datos seleccionable de la cuadrícula.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control DataItem. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value        | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | Se admite si hay un rectángulo delimitador. Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataItem** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | El control de elemento de datos siempre debe ser contenido.                                                                                                                                                        |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | El control de elemento de datos siempre debe ser un control.                                                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Vea las notas.   | Si el control contiene un estado que se está actualizando dinámicamente, se debe admitir esta propiedad para que una tecnología de asistencia pueda recibir actualizaciones cuando cambie el estado del elemento.        |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas.   | Este es el valor de cadena que transmite al usuario final el objeto subyacente que representa el elemento. Algunos ejemplos son "archivo multimedia" y "contacto".                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null         | Los controles de elemento de datos no tienen una etiqueta de texto estático.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada que corresponde al tipo de control **DataItem** . El valor predeterminado es "Data Item" para en-US o inglés (Estados Unidos).                                                              |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | El control de elemento de datos siempre contiene un elemento de texto principal que el usuario reconocerá como el identificador del elemento.                                                                           |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de elemento de datos. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico | Notas                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Si el elemento de datos se puede expandir o contraer para mostrar u ocultar información, se debe admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) .                                            |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depende | Los elementos de datos admitirán el patrón de control [GridItem](uiauto-implementinggriditem.md) cuando una colección de elementos de datos está disponible dentro de un contenedor que se puede navegar espacialmente de elemento a elemento.                 |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Depende | Todos los elementos de datos admiten la posibilidad de desplazarse en la vista con el patrón de control [ScrollItem](uiauto-implementingscrollitem.md) cuando su contenedor de datos tiene más elementos de los que caben en la pantalla.             |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depende | La capacidad de seleccionar los elementos de datos depende del contenido.                                                                                                                                                          |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | Depende | Si el elemento de datos está contenido dentro de un tipo de control [DataGrid](uiauto-supportdatagridcontroltype.md) que tiene un elemento header, debe admitir el patrón de control [TableItem](uiauto-implementingtableitem.md) . |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depende | Si el elemento de datos contiene un estado que se puede recorrer, debe admitir el patrón de control [Toggle](uiauto-implementingtoggle.md) .                                                                          |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depende | Si el texto primario del elemento de datos es editable, se debe admitir el patrón de control [Value](uiauto-implementingvalue.md) .                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a>Trabajar con elementos de trabajo en listas grandes

Dado que las listas grandes suelen virtualizarse en marcos de interfaz de usuario para ayudar en el rendimiento, un cliente de automatización de la interfaz de usuario no puede usar la característica de consulta de automatización de la interfaz de usuario para buscar el contenido del árbol completo de la misma manera que en otros contenedores de elementos. Un cliente debe desplazar el elemento a la vista (o expandir el control para mostrar todas las opciones disponibles) antes de obtener acceso al conjunto completo de información del elemento de datos.

Al llamar a [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) en el elemento de automatización de la interfaz de usuario para el elemento de datos, el explorador de Microsoft Windows vuelve correctamente y hace que el foco se establezca en el control de edición dentro del subárbol del elemento de datos.

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de elemento de datos deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



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



 

## <a name="dataitem-control-type-example"></a>Ejemplo de tipo de control DataItem

En la imagen siguiente se muestra un tipo de control DataItem en un control de vista de lista.

![captura de pantalla del control de vista de lista con el tipo de control DataItem](images/dataitemxmpl.jpg)

A continuación se muestra la vista de control y la vista de contenido del árbol de automatización de la interfaz de usuario que pertenece al control de elemento de datos. Los patrones de control de cada elemento de automatización se muestran entre paréntesis. El **Grupo** "Contoso" también forma parte de la cuadrícula del control host de la cuadrícula de datos. Para obtener un ejemplo de una estructura de cuadrícula de nivel superior, vea [DataGrid (tipo de control](uiauto-supportdatagridcontroltype.md)).



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
<td><ul>
<li>Grupo &quot; contoso &quot; (tabla, cuadrícula)
<ul>
<li>&quot;Receivable.doc&quot; de cuentas de DataItem (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>Cuentas de imagen &quot; Receivable.doc&quot;</li>
<li>Editar &quot; nombre &quot; (TableItem, GridItem, cuentas de valor &quot; Receivable.doc&quot; )</li>
<li>Editar &quot; fecha &quot; de modificación (TableItem, GridItem, valor &quot; 8/25/2006 3:29 PM &quot; )</li>
<li>Editar &quot; tamaño &quot; (GridItem, TableItem, valor &quot; 11,0 KB &quot; )</li>
</ul></li>
<li>&quot;Payable.doc&quot; de cuentas de DataItem (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Grupo &quot; contoso &quot; (tabla, cuadrícula)
<ul>
<li>&quot;Receivable.doc&quot; de cuentas de DataItem (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>Cuentas de imagen &quot; Receivable.doc&quot;</li>
<li>Editar &quot; nombre &quot; (TableItem, GridItem, cuentas de valor &quot; Receivable.doc&quot; )</li>
<li>Editar &quot; fecha &quot; de modificación (TableItem, GridItem, valor &quot; 8/25/2006 3:29 PM &quot; )</li>
<li>Editar &quot; tamaño &quot; (GridItem, TableItem, valor &quot; 11,0 KB &quot; )</li>
</ul></li>
<li>&quot;Payable.doc&quot; de cuentas de DataItem (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Si una cuadrícula representa una lista de elementos seleccionables, los elementos de la interfaz de usuario seleccionables correspondientes se pueden exponer con el tipo de control [ListItem](uiauto-supportlistitemcontroltype.md) en lugar del tipo de control DataItem. En el ejemplo anterior, los elementos **DataItem** ("accounts Receivable.doc" y "accounts Payable.doc") en **Group** ("Contoso") se pueden mejorar si se exponen como tipos de control ListItem, porque ese tipo ya admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




