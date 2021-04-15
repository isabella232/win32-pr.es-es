---
title: MenuBar (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control MenuBar.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control MenuBar
- UI Automation, MenuBar (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control MenuBar
- Automatización de la interfaz de usuario, propiedades para el tipo de control MenuBar
- Automatización de la interfaz de usuario, patrones de control para el tipo de control MenuBar
- Automatización de la interfaz de usuario, eventos para el tipo de control MenuBar
- estructuras de árbol, tipo de control MenuBar
- Properties, MenuBar (tipo de control)
- patrones de control, MenuBar (tipo de control)
- Events, MenuBar (tipo de control)
- compatibilidad con el tipo de control MenuBar
- MenuBar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control MenuBar
- tipos de control, patrones de control para el tipo de control MenuBar
- tipos de control, compatibilidad con MenuBar
- tipos de control, barra de menús
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94bb60c13b5999bc8020eb70b84f6c932a2fb94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695302"
---
# <a name="menubar-control-type"></a>MenuBar (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **MenuBar** .

Los controles de barra de menús son un ejemplo de controles que implementan el tipo de control **MenuBar** . Las barras de menús proporcionan un medio para que los usuarios activen los comandos y las opciones contenidos en una aplicación.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **MenuBar** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de barra de menús donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de barra de menús y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>MenuBar
<ul>
<li>MenuItem (1 o más)</li>
<li>Otros controles (0 o varios)</li>
</ul></li>
</ul></td>
<td><ul>
<li>No aplicable
<ul>
<li>MenuItem (1 o más)</li>
<li>Otros controles (0 o varios)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Un control de barra de menús siempre aparece en la vista de control, pero no en la vista de contenido porque normalmente no transmite información significativa al usuario final (a menos que la aplicación contenga más de una barra de menús).

Los clientes de automatización de la interfaz de usuario pueden escuchar el evento [**\_ MenuModeStartEventId de UIA**](uiauto-event-ids.md) para asegurarse de que se notifican de forma coherente cuando la interfaz de usuario entra en modo de menú. Cuando la aplicación está en modo de menú, es posible que todas las entradas de teclado se capturen para la navegación del menú (por ejemplo, si escribe "" puede invocar el menú **Guardar** en lugar de escribir el carácter en el área cliente de la aplicación). El **evento \_ MenuModeStartEventId de UIA** debe preceder al primer evento [**\_ MenuOpenedEventId de UIA**](uiauto-event-ids.md) para garantizar la coherencia lógica. El [**evento \_ MenuModeEndEventId de UIA**](uiauto-event-ids.md) sigue el último evento [**\_ MenuClosedEventId de UIA**](uiauto-event-ids.md) . Hacer clic en un elemento de menú también puede desencadenar inmediatamente el evento **UIA \_ MenuModeStartEventId** , seguido de un evento **\_ MenuOpenedEventId de UIA** .

Un control de barra de menús puede contener otros controles, como controles de edición y cuadros combinados, dentro de su estructura. Estos controles adicionales corresponden a la categoría "otros controles" que se indica anteriormente en las vistas de control y de contenido.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **MenuBar** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value       | Notas                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | NULL        | Las barras de menús no suelen tener teclas de aceleración.                                                                                                                                                                                          |
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | "Alt"       | Presionar la tecla ALT normalmente debe traer el foco a la barra de menús dentro de la aplicación.                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.  | El valor que expone esta propiedad debe incluir todos los controles que se contienen dentro de ella.                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **MenuBar** |                                                                                                                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | false       | El control de barra de menús no se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | El control de barra de menús siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE        | Los controles de barra de menús pueden recibir el foco del teclado porque los controles que contienen pueden recibir el foco de teclado.                                                                                                                                      |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Vea las notas.  | El valor de esta propiedad depende de si el control es visible en la pantalla.                                                                                                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | Normalmente, los controles de barra de menús no tienen una etiqueta.                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.  | Cadena localizada que corresponde al tipo de control **MenuBar** . El valor predeterminado es "barra de menús" para en-US o inglés (Estados Unidos).                                                                                                    |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.  | El control de barra de menús no necesita un nombre a menos que una aplicación tenga más de una barra de menús. Si hay más de una barra de menús en una aplicación, use esta propiedad para exponer nombres distintivos, como "formato" o "esquematización". |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Depende     | Esta propiedad expone si el control de barra de menús es horizontal o vertical.                                                                                                                                                            |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que deben admitir los controles de barra de menús. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico | Notas                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Si el control se puede expandir o contraer, debe implementar el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) . |
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Depende | Si el control se puede acoplar a diferentes partes de la pantalla, debe implementar el patrón de control [Dock](uiauto-implementingdock.md) .   |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Depende | Si el control puede cambiar de tamaño, girarse o moverse, debe implementar el patrón de control [Transform](uiauto-implementingtransform.md) .      |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de barra de menús son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                                | Notas                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ExpandCollapseExpandCollapseStatePropertyId. | Si el control admite el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                              | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                          | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




