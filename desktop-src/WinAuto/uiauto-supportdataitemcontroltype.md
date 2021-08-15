---
title: Tipo de control DataItem
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control DataItem.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control DataItem
- Automatización de la interfaz de usuario, tipo de control DataItem
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control DataItem
- Automatización de la interfaz de usuario,properties para el tipo de control DataItem
- Automatización de la interfaz de usuario,patrones de control para el tipo de control DataItem
- Automatización de la interfaz de usuario,events para el tipo de control DataItem
- Automatización de la interfaz de usuario,listas grandes y tipo de control DataItem
- estructuras de árbol, tipo de control DataItem
- properties,Tipo de control DataItem
- patrones de control, tipo de control DataItem
- events,Tipo de control DataItem
- listas grandes
- compatibilidad con el tipo de control DataItem
- Tipo de control DataItem
- tipos de control, estructura de árbol para el tipo de control DataItem
- tipos de control, patrones de control para el tipo de control DataItem
- tipos de control, listas grandes y tipo de control DataItem
- tipos de control, compatibilidad con DataItem
- tipos de control, DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ec4612b43855578256d52bf6647b105ea666882cfe2f72dcdbf355559a7e5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118826325"
---
# <a name="dataitem-control-type"></a>Tipo de control DataItem

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **DataItem.**

Una entrada de una lista de contactos es un ejemplo de un control de elemento de datos. Un control de elemento de datos contiene información de interés para un usuario final. Es más complicado que el elemento de lista simple porque contiene información más completa.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **DataItem.** Los Automatización de la interfaz de usuario se aplican a todos los controles de elementos de datos en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Trabajar con dataitems en listas grandes](#working-with-dataitems-in-large-lists)
-   [Eventos necesarios](#required-events)
-   [Ejemplo de tipo de control DataItem](#dataitem-control-type-example)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de elementos de datos y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario árbol, vea [información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)



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



 

Un elemento de datos de una cuadrícula de datos puede hospedar diversos objetos, entre los que se incluye otra capa de elementos de datos o elementos de cuadrícula concretos como controles de edición, texto o imágenes. Si el elemento de elemento de datos tiene un rol de objeto específico, el elemento debe exponerse como un tipo de control específico; por ejemplo, un tipo de control [ListItem](uiauto-supportlistitemcontroltype.md) para un elemento de datos seleccionable en la cuadrícula.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control DataItem. Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor        | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **DataItem** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | El control de elemento de datos siempre debe ser contenido.                                                                                                                                                        |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE         | El control de elemento de datos siempre debe ser un control.                                                                                                                                                      |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**ItemStatusPropertyId de UIA \_**](uiauto-automation-element-propids.md)                     | Vea las notas.   | Si el control contiene el estado que se actualiza dinámicamente, esta propiedad debe ser compatible para que una tecnología de asistencia pueda recibir actualizaciones cuando cambie el estado del elemento.        |
| [**ItemTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                         | Vea las notas.   | Este es el valor de cadena que transmite al usuario final el objeto subyacente que representa el elemento. Algunos ejemplos son "Archivo multimedia" y "Contacto".                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null         | Los controles de elemento de datos no tienen una etiqueta de texto estático.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada correspondiente al tipo de control **DataItem.** El valor predeterminado es "elemento de datos" para en-US o inglés (Estados Unidos).                                                              |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | El control de elemento de datos siempre contiene un elemento de texto principal que el usuario reconocería como identificador del elemento.                                                                           |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de elementos de datos. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico | Notas                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Si el elemento de datos se puede expandir o contraer para mostrar y ocultar información, debe ser compatible con el patrón de control [ExpandCollapse.](uiauto-implementingexpandcollapse.md)                                            |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depende | Los elementos de datos admitirán el patrón de control [GridItem](uiauto-implementinggriditem.md) cuando haya disponible una colección de elementos de datos dentro de un contenedor que se pueda navegar espacialmente de elemento a elemento.                 |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Depende | Todos los elementos de datos admiten la capacidad de desplazarse a la vista con el patrón de control [ScrollItem](uiauto-implementingscrollitem.md) cuando su contenedor de datos tiene más elementos de los que caben en la pantalla.             |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depende | La capacidad de seleccionar los elementos de datos depende del contenido.                                                                                                                                                          |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | Depende | Si el elemento de datos está incluido en un tipo de control [DataGrid](uiauto-supportdatagridcontroltype.md) que tiene un elemento de encabezado, debe admitir el patrón de control [TableItem.](uiauto-implementingtableitem.md) |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depende | Si el elemento de datos contiene un estado que se puede recorrer en ciclo, debe admitir el patrón de control [Toggle.](uiauto-implementingtoggle.md)                                                                          |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depende | Si el texto principal del elemento de datos es editable, debe ser compatible con [el patrón](uiauto-implementingvalue.md) de control Valor.                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a>Trabajar con DataItems en listas grandes

Dado que las listas grandes a menudo se virtualizan en marcos de interfaz de usuario para ayudar en el rendimiento, un cliente de Automatización de la interfaz de usuario no puede usar la característica de consulta Automatización de la interfaz de usuario para buscar el contenido del árbol completo de la misma manera que en otros contenedores de elementos. Un cliente debe desplazar el elemento a la vista (o expandir el control para mostrar todas las opciones disponibles) antes de acceder al conjunto completo de información desde el elemento de datos.

Al llamar a [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) en el elemento Automatización de la interfaz de usuario para el elemento de datos, Microsoft Windows Explorer devuelve correctamente y hace que el foco se establezca en el control Editar del subárbol del elemento de datos.

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de elementos de datos son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                                | Notas                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**UIA \_ Evento expandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) cambiado por la propiedad . | Si el control admite el patrón de control [ExpandCollapse,](uiauto-implementingexpandcollapse.md) debe admitir este evento. |
| [**Invoke \_ InvokedEventId de UIA \_**](uiauto-event-ids.md)                                                                                  | Si el control admite el patrón de control [Invoke,](uiauto-implementinginvoke.md) debe admitir este evento.                 |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.         |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento.       |
| [**UIA \_ Evento de cambio de propiedad ItemStatusPropertyId.**](uiauto-automation-element-propids.md)                                            | Si el control admite la [**propiedad ItemStatus,**](uiauto-automation-element-propids.md) debe admitir este evento.        |
| [**UIA \_ Evento de cambio de propiedad NamePropertyId.**](uiauto-automation-element-propids.md)                                                        |                                                                                                                                  |
| [**Elemento \_ SelectionItem \_ de UIAAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento.   |
| [**Elemento \_ SelectionItem de \_ UIARemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento.   |
| [**Elementos \_ SelectionItem \_ de UIASelectedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)                                 | Si el control admite el patrón de control [Toggle,](uiauto-implementingtoggle.md) debe admitir este evento.                 |
| [**UIA \_ Evento de cambio de propiedad ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                                               | Si el control admite el [patrón de](uiauto-implementingvalue.md) control Valor, debe admitir este evento.                   |



 

## <a name="dataitem-control-type-example"></a>Ejemplo de tipo de control DataItem

En la imagen siguiente se muestra un tipo de control DataItem en un control list-view.

![captura de pantalla del control list-view con el tipo de control dataitem](images/dataitemxmpl.jpg)

A continuación se muestran la vista de control y la vista de contenido del Automatización de la interfaz de usuario que pertenece al control de elemento de datos. Los patrones de control de cada elemento de automatización se muestran entre paréntesis. El **grupo** "Contoso" también forma parte de la cuadrícula del control host de cuadrícula de datos. Para obtener un ejemplo de una estructura de cuadrícula de nivel superior, vea [Tipo de control DataGrid](uiauto-supportdatagridcontroltype.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Automatización de la interfaz de usuario árbol: Vista de control</th>
<th>Automatización de la interfaz de usuario árbol de contenido: vista de contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Group &quot; Contoso &quot; (Table, Grid)
<ul>
<li>DataItem &quot; Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>Cuentas &quot; de imagen Receivable.doc&quot;</li>
<li>Editar &quot; nombre &quot; (TableItem, GridItem, Cuentas &quot; de valor Receivable.doc&quot; )</li>
<li>Editar &quot; fecha de modificación &quot; (TableItem, GridItem, valor &quot; 25/8/2006 3:29 p. &quot; m.)</li>
<li>Editar &quot; tamaño &quot; (GridItem, TableItem, valor &quot; de 11,0 &quot; KB)</li>
</ul></li>
<li>DataItem &quot; Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Group &quot; Contoso &quot; (Table, Grid)
<ul>
<li>DataItem &quot; Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>Cuentas &quot; de imagen Receivable.doc&quot;</li>
<li>Editar &quot; nombre &quot; (TableItem, GridItem, Cuentas &quot; de valor Receivable.doc&quot; )</li>
<li>Editar &quot; fecha de modificación &quot; (TableItem, GridItem, valor &quot; 25/8/2006 3:29 p. &quot; m.)</li>
<li>Editar &quot; tamaño &quot; (GridItem, TableItem, valor &quot; de 11,0 &quot; KB)</li>
</ul></li>
<li>DataItem &quot; Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Si una cuadrícula representa una lista de elementos seleccionables, los elementos de interfaz de usuario seleccionables correspondientes se pueden exponer con el tipo de control [ListItem](uiauto-supportlistitemcontroltype.md) en lugar del tipo de control DataItem. En el ejemplo anterior, los elementos **DataItem** ("Accounts Receivable.doc" y "Accounts Payable.doc") en **Group** ("Contoso") se pueden mejorar exponiendo como tipos de control ListItem porque ese tipo ya admite el patrón de control [SelectionItem.](uiauto-implementingselectionitem.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




