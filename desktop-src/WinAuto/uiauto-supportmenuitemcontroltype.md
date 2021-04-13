---
title: MenuItem (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control MenuItem.
ms.assetid: a6a04489-8e28-44ff-a3b0-ecf19c24daab
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control MenuItem
- Automatización de la interfaz de usuario, tipo de control MenuItem
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control MenuItem
- Automatización de la interfaz de usuario, propiedades para el tipo de control MenuItem
- Automatización de la interfaz de usuario, patrones de control para el tipo de control MenuItem
- Automatización de la interfaz de usuario, eventos para el tipo de control MenuItem
- estructuras de árbol, tipo de control MenuItem
- propiedades, tipo de control MenuItem
- patrones de control, MenuItem (tipo de control)
- Events, MenuItem (tipo de control)
- compatibilidad con el tipo de control MenuItem
- MenuItem (tipo de control)
- tipos de control, estructura de árbol para el tipo de control MenuItem
- tipos de control, patrones de control para el tipo de control MenuItem
- tipos de control, compatibilidad con MenuItem
- tipos de control, MenuItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24033866f749974a41d39094b416e70f3c40f796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357059"
---
# <a name="menuitem-control-type"></a>MenuItem (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **MenuItem** .

Un control de menú permite organizar jerárquicamente los elementos asociados a comandos y controladores de eventos. En una aplicación Windows típica, una barra de menús contiene varios elementos de menú (como **archivo**, **Editar** y **ventana**) y cada elemento de menú muestra un menú. Un menú contiene una colección de elementos de menú (como **Nuevo**, **Abierto** y **Cerrar**), que se puede expandir para mostrar elementos de menú adicionales o realizar una acción específica cuando se haga clic en ella.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **MenuItem** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de elemento de menú donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Problemas heredados](#legacy-issues)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de elemento de menú y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Ayuda de MenuItem &quot;&quot;
<ul>
<li>Menú (submenú de elemento de menú Ayuda)
<ul>
<li>Temas de ayuda de MenuItem &quot;&quot;</li>
<li>MenuItem &quot; acerca del Bloc de notas&quot;</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Ayuda de MenuItem &quot;&quot;
<ul>
<li>Temas de ayuda de MenuItem &quot;&quot;</li>
<li>MenuItem &quot; acerca del Bloc de notas&quot;</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

La vista de control del control de elemento de menú tiene la estructura de árbol de automatización de la interfaz de usuario mostrada anteriormente. Tenga en cuenta que se ha agregado el elemento de menú de **ayuda** en la barra de menús para ilustrar mejor la estructura.

En la vista de contenido, el **menú** no está presente en el árbol de automatización de la interfaz de usuario porque no transmite información significativa al usuario final.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **MenuItem** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value        | Notas                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario. Asigne la propiedad **AutomationId** para un elemento de menú si se sabe que el elemento es coherente entre las distintas instancias de la interfaz de usuario. Si el elemento de menú se rellena dinámicamente y no es predecible, deje la propiedad **AutomationId** en blanco. |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | Se admite si hay un rectángulo delimitador. Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.                                                                                                                                                                     |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **MenuItem** |                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | El control de elemento de menú siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | El control de elemento de menú siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada que corresponde al tipo de control **MenuItem** . El valor predeterminado es "elemento de menú" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | El nombre del control de elemento de menú es el texto que se utiliza para etiquetarlo.                                                                                                                                                                                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que deben admitir los controles de elemento de menú. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico | Notas                                                                                                                                                |
|-------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Si el control se puede expandir o contraer, implemente [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider).                            |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Depende | Si el control ejecuta una acción o un comando único, implemente [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider).                                     |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depende | Si el control se usa para seleccionar de una lista de opciones entre los elementos de menú, implemente [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider). |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depende | Si el control representa una opción que se puede activar o desactivar, implemente [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).                       |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de elemento de menú deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                                | Notas                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ExpandCollapseExpandCollapseStatePropertyId. | Si el control admite el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) , debe admitir este evento. |
| [**\_InvokedEventId de invocación de UIA \_**](uiauto-event-ids.md)                                                                                  | Si el control admite el patrón de control [Invoke](uiauto-implementinginvoke.md) , debe admitir este evento.                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                              | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                          | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.       |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento.   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento.   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) , debe admitir este evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ToggleToggleStatePropertyId.                                 | Si el control admite el patrón de control [Toggle](uiauto-implementingtoggle.md) , debe admitir este evento.                 |



 

## <a name="legacy-issues"></a>Problemas heredados

En el caso de los elementos de menú de Microsoft Win32, el patrón de control [Toggle](uiauto-implementingtoggle.md) solo se admite cuando se activa un elemento de menú y es posible determinar mediante programación si se requiere compatibilidad con el patrón de control Toggle. Dado que un elemento de menú de Win32 no expone si se puede activar, se admite el patrón de control Invoke cuando no se comprueba el elemento de menú. Siempre se admite el patrón de control Invoke, incluso para los elementos de menú que solo son necesarios para admitir el patrón de control Toggle. Esto es para que los clientes no se confundan cuando un elemento de menú que era compatible con el patrón de control [Invoke](uiauto-implementinginvoke.md) (cuando el elemento de menú estaba desactivado) ya no admite ese patrón cuando se activa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




