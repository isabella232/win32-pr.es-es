---
title: Menu (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control menu.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control menu
- UI Automation, MENU (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control menu
- Automatización de la interfaz de usuario, propiedades del tipo de control menu
- Automatización de la interfaz de usuario, patrones de control para el tipo de control menu
- Automatización de la interfaz de usuario, eventos para el tipo de control menu
- estructuras de árbol, tipo de control menu
- Properties, MENU (tipo de control)
- patrones de control, tipo de control menu
- Events, MENU (tipo de control)
- compatibilidad con el tipo de control menu
- Menu (tipo de control)
- tipos de control, estructura de árbol para el tipo de control menu
- tipos de control, patrones de control para el tipo de control menu
- tipos de control, compatibilidad con menú
- tipos de control, menú
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075614"
---
# <a name="menu-control-type"></a>Menu (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Menu** .

Un control de menú permite organizar jerárquicamente los elementos asociados a comandos y controladores de eventos. En una aplicación típica de Microsoft Windows, una barra de menús contiene varios botones de menú (como **archivo**, **Editar** y **ventana**) y cada botón de menú muestra un menú. Un menú contiene una colección de elementos de menú (como **Nuevo**, **Abrir** y **Cerrar**), que se puede expandir para mostrar elementos de menú adicionales o realizar una acción específica cuando se haga clic en ellos.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Menu** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de menú donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra una vista de contenido y control típica del árbol de automatización de la interfaz de usuario que pertenece a los controles de menú y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Menú
<ul>
<li>MenuItem (1 o varios)</li>
</ul>
<ul>
<li>Otros controles (0 o varios)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Menú
<ul>
<li>MenuItem (1 o varios)</li>
</ul>
<ul>
<li>Otros controles (0 o varios)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Los controles de menú siempre aparecen en la vista de control y la vista de contenido del árbol de automatización de la interfaz de usuario. Los controles de menú deben aparecer bajo el control al que hace referencia su información. Los clientes de automatización de la interfaz de usuario pueden escuchar a [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) para asegurarse de que obtienen de forma coherente la información que transmiten los controles de menú. Los controles de menú contextual son un caso especial. Pueden aparecer como elementos secundarios del escritorio o de una ventana de la aplicación de nivel superior.

Un control de menú puede contener otros controles, como controles de edición y cuadros combinados, dentro de su estructura. Estos controles adicionales corresponden a los "otros controles" que se muestran en la tabla anterior en las vistas de control y de contenido.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **Menu** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                      | Value      | Notas                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)           | **Menú**   |                                                                                                                                                                         |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md) | TRUE       | El control de menú siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md) | TRUE       | El control de menú siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)               | NULL       | No se espera ninguna etiqueta con un control de menú típico.                                                                                                                    |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas. | El control de menú no requiere que se establezca una propiedad **Name** o puede tener el mismo nombre que el control asociado, como un elemento de menú que abrió el submenú. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

No hay ningún patrón de control necesario para el tipo de control Menu.

## <a name="required-events"></a>Eventos necesarios

Los controles de menú deben generar el evento de [**\_ MenuOpenedEventId de UIA**](uiauto-event-ids.md) cuando aparecen en la pantalla. El evento de **\_ MenuOpenedEventId de UIA** incluirá el texto del control. El [**evento \_ MenuClosedEventId de UIA**](uiauto-event-ids.md) se debe generar cuando un menú desaparece de la pantalla.

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de menú deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




