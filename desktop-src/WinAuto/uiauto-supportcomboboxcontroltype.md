---
title: ComboBox (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control ComboBox.
ms.assetid: e7c64dc1-e1e3-4f99-adde-d0d63eb6c4c9
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control ComboBox
- Automatización de la interfaz de usuario, tipo de control ComboBox
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control ComboBox
- Automatización de la interfaz de usuario, propiedades para el tipo de control ComboBox
- Automatización de la interfaz de usuario, patrones de control para el tipo de control ComboBox
- Automatización de la interfaz de usuario, eventos para el tipo de control ComboBox
- estructuras de árbol, tipo de control ComboBox
- Properties, ComboBox (tipo de control)
- patrones de control, ComboBox (tipo de control)
- Events, ComboBox (tipo de control)
- compatibilidad con el tipo de control ComboBox
- ComboBox (tipo de control)
- tipos de control, estructura de árbol para el tipo de control ComboBox
- tipos de control, patrones de control para el tipo de control ComboBox
- tipos de control, compatibilidad con ComboBox
- tipos de control, ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410cca4887c04a00d6da53feb9fcf1242476a979
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775853"
---
# <a name="combobox-control-type"></a>ComboBox (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **ComboBox** .

Un cuadro combinado es un cuadro de lista combinado con un control estático o un control de edición que muestra el elemento seleccionado actualmente en la parte del cuadro de lista del cuadro combinado. La parte de cuadro de lista del control se muestra en todo momento o solo aparece cuando el usuario selecciona la flecha de lista desplegable (que es un botón de comando) junto al control. Si el campo de selección es un control de edición, el usuario puede escribir información que no esté en la lista; de lo contrario, el usuario solo puede seleccionar elementos de la lista.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **ComboBox** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de cuadro combinado donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de cuadro combinado y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>ComboBox
<ul>
<li>Edición (0 o 1)</li>
<li>Lista (0 o 1)</li>
<li>List Item (elemento secundario de List; de 0 a varios)</li>
<li>Button (1)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ComboBox
<ul>
<li>List Item (de 0 a varios)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

El control de edición de la vista de control del cuadro combinado solo es necesario si el cuadro combinado se puede editar para tomar cualquier entrada, como es el caso del cuadro combinado en el cuadro de diálogo **Ejecutar** .

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **ComboBox** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                         |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Se admite si hay un rectángulo delimitador. Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.                                                                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | ComboBox   |                                                                                                                                                                                                                                                                                                                  |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas. | El texto de ayuda de los controles de cuadro combinado debe explicar por qué se le pide al usuario que elija una opción del cuadro combinado. El texto es similar a la información que se presenta mediante un elemento de información sobre herramientas. Por ejemplo, "Seleccione un elemento para establecer la resolución de pantalla del monitor".                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Los controles de cuadro combinado siempre se incluyen en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Los controles de cuadro combinado siempre se incluyen en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE       | Los controles de cuadro combinado pueden recibir el foco de teclado; sin embargo, cuando un cliente de automatización de la interfaz de usuario establece el foco en un cuadro combinado, cualquier elemento del subárbol del cuadro combinado puede recibir el foco.                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Los controles de cuadro combinado suelen tener una etiqueta de texto estático a la que hace referencia esta propiedad.                                                                                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **ComboBox** . El valor predeterminado es "cuadro combinado" para en-US o inglés (Estados Unidos).                                                                                                                                                                          |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El nombre del control de cuadro combinado normalmente se genera a partir de una etiqueta de texto estático. Si no hay una etiqueta de texto estático, debe asignar un valor para la propiedad **Name** . La propiedad **Name** no debe contener nunca el contenido actual del cuadro combinado ni cambiar cuando cambia el contenido del cuadro combinado. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de cuadro combinado. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico  | Notas                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Obligatorio | Se debe admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) porque un control de cuadro combinado siempre debe contener un botón desplegable.                                                                                                                                                                                |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)           | Depende  | Muestra la selección actual en el cuadro combinado. La compatibilidad con el patrón de control [Selection](uiauto-implementingselection.md) se delega en el cuadro de lista situado debajo del cuadro combinado, pero es posible que no siempre sea factible.                                                                                                                               |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depende  | Si el cuadro combinado puede tomar valores de texto arbitrarios, se debe admitir el patrón de control [Value](uiauto-implementingvalue.md) . Este patrón permite establecer mediante programación el contenido de la cadena del cuadro combinado. Si no se admite el patrón de control Value, el usuario debe seleccionar los elementos de la lista dentro del subárbol del cuadro combinado. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                 | Nunca    | El patrón de control [Scroll](uiauto-implementingscroll.md) nunca se admite directamente en un cuadro combinado. Se admite si se puede desplazar un cuadro de lista contenido dentro de un cuadro combinado y solo cuando el cuadro de lista está visible en la pantalla.                                                                                                              |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de cuadro combinado deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                                | Notas                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                              |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                              | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                          | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ExpandCollapseExpandCollapseStatePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ValueValuePropertyId.                                               | Si el control admite el patrón de control [Value](uiauto-implementingvalue.md) , debe admitir este evento.             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




