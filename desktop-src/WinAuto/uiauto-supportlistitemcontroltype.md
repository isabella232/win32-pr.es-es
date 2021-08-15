---
title: Tipo de control ListItem
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control ListItem.
ms.assetid: 8cb579ab-92c9-4311-aad7-5363f4cf2eaf
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control ListItem
- Automatización de la interfaz de usuario,tipo de control ListItem
- Automatización de la interfaz de usuario,estructura de árbol para el tipo de control ListItem
- Automatización de la interfaz de usuario,properties para el tipo de control ListItem
- Automatización de la interfaz de usuario,patrones de control para el tipo de control ListItem
- Automatización de la interfaz de usuario,events para el tipo de control ListItem
- estructuras de árbol, tipo de control ListItem
- properties,Tipo de control ListItem
- patrones de control, tipo de control ListItem
- events,Tipo de control ListItem
- compatibilidad con el tipo de control ListItem
- Tipo de control ListItem
- tipos de control, estructura de árbol para el tipo de control ListItem
- tipos de control, patrones de control para el tipo de control ListItem
- tipos de control, compatibilidad con ListItem
- tipos de control,ListItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fc7df30fc9aeebbabd5a5fdb9572c9f4b81bda4507eac751f283841a14054a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825557"
---
# <a name="listitem-control-type"></a>Tipo de control ListItem

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **ListItem.**

Los controles de elemento de lista son un ejemplo de controles que implementan el tipo de control **ListItem.**

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **ListItem.** Los Automatización de la interfaz de usuario se aplican a todos los controles de elementos de lista en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece a los controles de elemento de lista y se describe lo que se puede incluir en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)



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
<li>ListItem
<ul>
<li>Imagen (0 o más)</li>
<li>Text (0 o más)</li>
<li>Edición (0 o más)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ListItem</li>
</ul></td>
</tr>
</tbody>
</table>



 

Los elementos secundarios de un control de elemento de lista dentro de la vista de contenido Automatización de la interfaz de usuario árbol deben mostrar siempre cero elementos secundarios. Si la estructura del control es tal que otros elementos se encuentran debajo del elemento de lista, debe seguir los requisitos de la compatibilidad de Automatización de la interfaz de usuario para el tipo de control [TreeItem.](uiauto-supporttreeitemcontroltype.md)

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **ListItem.** Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor        | Notas                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel de la vista sin formato Automatización de la interfaz de usuario árbol. Asigne la **propiedad AutomationId** para un elemento de lista si se sabe que el elemento es coherente en diferentes instancias de la interfaz de usuario. Si el elemento de lista se rellena dinámicamente y no es predecible, deje la **propiedad AutomationId** en blanco.                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El valor de esta propiedad debe incluir el área del contenido de imagen y texto del elemento de lista.                                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Depende      | Si el control de lista tiene un punto en el que se puede hacer clic (un punto en el que se puede hacer clic para que la lista tome el foco), ese punto debe exponerse a través de esta propiedad. Si el control de lista está cubierto por completo por elementos de lista descendientes, devolverá el error [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) para indicar que el cliente debe pedir un elemento dentro del control de lista para un punto en el que se puede hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **ListItem** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas.   | El texto de ayuda para los controles de lista debe explicar por qué se le solicita al usuario que elija una opción en una lista de opciones, que es normalmente el mismo tipo de información presentada a través de una información sobre herramientas. Por ejemplo, "Seleccione un elemento para establecer la resolución de pantalla del monitor".                                                                                                                                                    |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**     | El control de lista siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario lista.                                                                                                                                                                                                                                                                                                                                                |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**     | El control de lista siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                                                                                                                                                                                                                                |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el contenedor puede aceptar la entrada de teclado, este valor de propiedad debe ser **TRUE.**                                                                                                                                                                                                                                                                                                                                           |
| [**IsOffscreenPropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | Depende      | Esta propiedad debe devolver un valor para si el elemento de lista se desplaza actualmente a la vista dentro del contenedor primario que implementa el patrón de control [Scroll.](uiauto-implementingscroll.md)                                                                                                                                                                                                                                  |
| [**ItemStatusPropertyId de UIA \_**](uiauto-automation-element-propids.md)                     | Depende      | Si el control contiene el estado que se actualiza dinámicamente, esta propiedad debe ser compatible para que una tecnología de asistencia pueda recibir actualizaciones cuando cambie el estado del elemento.                                                                                                                                                                                                                                     |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Depende      | Esta propiedad se debe exponer para los controles de elemento de lista que representan un objeto subyacente. Estos controles de elemento de lista suelen tener un icono asociado al control que los usuarios se asocian con el objeto subyacente.                                                                                                                                                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.   | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada correspondiente al tipo de control **ListItem.** El valor predeterminado es "elemento de lista" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                                                                                           |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | El valor de la propiedad name de un control de elemento de lista procede de la etiqueta de texto del elemento.                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de elemento de lista. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico | Notas                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Si el elemento se puede manipular para mostrar u ocultar información, se debe implementar el patrón de control [ExpandCollapse.](uiauto-implementingexpandcollapse.md)                                                                                                                                                                                                                        |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depende | Si se admite la navegación espacial de elemento a elemento dentro del contenedor de lista y el contenedor se organiza en filas y columnas, se debe implementar el patrón de control [GridItem.](uiauto-implementinggriditem.md)                                                                                                                                                                  |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Depende | Si el elemento tiene un comando que se puede realizar en él, independiente de la selección, se debe implementar [el](uiauto-implementinginvoke.md) patrón de control Invoke. Se trata normalmente de una acción asociada a hacer doble clic en el control de elemento de lista. Algunos ejemplos serían iniciar un documento desde Windows Explorer o reproducir un archivo de música en Microsoft Reproductor de Windows Media.        |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Depende | Si el elemento de lista se encuentra dentro de un contenedor que se puede desplazar, se debe implementar el patrón de control [ScrollItem.](uiauto-implementingscrollitem.md)                                                                                                                                                                                                                       |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depende | Un control de elemento de lista que admita la selección debe implementar el patrón de control [SelectionItem.](uiauto-implementingselectionitem.md) Esto permite que los controles de elementos de lista transmitan cuando se seleccionan.                                                                                                                                                                             |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depende | Si el elemento de lista se puede comprobar y la acción no realiza un cambio de estado de selección, se debe implementar el patrón de control [Alternar.](uiauto-implementingtoggle.md)                                                                                                                                                                                                            |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depende | Si se puede editar el elemento, se debe implementar [el patrón](uiauto-implementingvalue.md) de control Valor. Los cambios en el control de elemento de lista provocarán cambios en los valores de las propiedades [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) y [**UIA \_ ValueValuePropertyId.**](uiauto-control-pattern-propids.md) |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos de lista que se requieren para admitir los controles de elemento de lista. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                                | Notas                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**UIA \_ Evento expandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) cambiado por la propiedad . | Si el control admite el patrón de control [ExpandCollapse,](uiauto-implementingexpandcollapse.md) debe admitir este evento. |
| [**Invoke \_ InvokedEventId de UIA \_**](uiauto-event-ids.md)                                                                                  | Si el control admite el patrón de control [Invoke,](uiauto-implementinginvoke.md) debe admitir este evento.                 |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.         |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento.       |
| [**UIA \_ Evento de cambio de propiedad ItemStatusPropertyId.**](uiauto-automation-element-propids.md)                                            | Si el control admite la [**propiedad ItemStatus,**](uiauto-automation-element-propids.md) es debe admitir este evento.        |
| [**UIA \_ Evento de cambio de propiedad NamePropertyId.**](uiauto-automation-element-propids.md)                                                        |                                                                                                                                  |
| [**Elemento \_ SelectionItem \_ de UIAAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento.   |
| [**Elemento \_ SelectionItem de \_ UIARemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento.   |
| [**Elementos \_ SelectionItem \_ de UIASelectedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)                                 | Si el control admite el patrón de control [Toggle,](uiauto-implementingtoggle.md) debe admitir este evento.                 |
| [**UIA \_ Evento de cambio de propiedad ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                                               | Si el control admite el [patrón de](uiauto-implementingvalue.md) control Valor, debe admitir este evento.                   |



 

## <a name="remarks"></a>Comentarios

Si un contenedor hospeda elementos de lista, el medio principal de navegación debe ir a los elementos de lista. Centrarse en los subelementos a través de la navegación de lista puede resultar confuso para los usuarios y las herramientas de accesibilidad. Si el contenedor hospeda una lista vertical de elementos, al presionar las teclas FLECHA ARRIBA y FLECHA ABAJO debe navegar por los elementos, pero al presionar las teclas FLECHA DERECHA y FLECHA IZQUIERDA se pueden navegar a los subelementos del elemento centrado, como columnas de lista o subelementos de interfaz de usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




