---
title: Button (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Button.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Button
- UI Automation, Button (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Button
- Automatización de la interfaz de usuario, propiedades para el tipo de control Button
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Button
- Automatización de la interfaz de usuario, eventos para el tipo de control Button
- estructuras de árbol, Button (tipo de control)
- Properties, Button (tipo de control)
- patrones de control, Button (tipo de control)
- Events, Button (tipo de control)
- compatibilidad con el tipo de control Button
- Button (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Button
- tipos de control, patrones de control para el tipo de control Button
- tipos de control, compatibilidad con Button
- tipos de control, botón
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def18e7094e297303a70fc0980bfdd0cb4413c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269456"
---
# <a name="button-control-type"></a>Button (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Button** .

Un botón es un objeto con el que un usuario interactúa para realizar una acción, como por ejemplo los botones Aceptar y Cancelar de un cuadro de diálogo. El control de botón es un control simple de exponer porque se asigna a un único comando que el usuario quiere realizar.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Button** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de botón donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de botón y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Botón
<ul>
<li>Imagen (0 o más)</li>
<li>Text (0 o más)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Botón</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles que implementan el tipo de control **Button** (como los controles de botón). Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Un control de botón normalmente admite una tecla de aceleración para permitir que el usuario final realice rápidamente la acción representada por el botón del teclado.                                             |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Se admite si hay un rectángulo delimitador. Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Botón** |                                                                                                                                                                                                      |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas. | El texto de ayuda debe indicar cuál será el resultado final de la activación del botón. Suele ser el mismo tipo de información que se presenta a través de una información sobre herramientas.                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control de botón siempre debe ser contenido.                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control de botón siempre debe ser un control.                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null       | Los controles de botón se etiquetan automáticamente con su contenido.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **Button** . El valor predeterminado es "Button" para en-US o inglés (Estados Unidos).                                                                   |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El nombre del control de botón es el texto que se utiliza para etiquetarlo. Siempre que se utiliza una imagen para etiquetar un botón, se debe proporcionar texto alternativo para la propiedad **nombre** del botón.                        |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de botón. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                  | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Vea las notas.    | Cuando un botón se hospeda como elemento secundario de un botón de expansión, el botón secundario puede admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) en lugar del patrón de control [Invoke](uiauto-implementinginvoke.md) o [Toggle](uiauto-implementingtoggle.md) . El patrón de control ExpandCollapse se puede usar para abrir o cerrar un menú u otra subestructura asociada con el elemento de botón. |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Vea las notas.    | Todos los botones deben admitir el patrón de control [Invoke](uiauto-implementinginvoke.md) o el patrón de control [Toggle](uiauto-implementingtoggle.md) , pero no ambos. Se debe admitir el patrón de control Invoke cuando el botón ejecuta un comando en la solicitud del usuario. Este comando se asigna a una única operación, como cortar, copiar, pegar o eliminar.                                                              |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Vea las notas.    | Todos los botones deben admitir el patrón de control [Invoke](uiauto-implementinginvoke.md) o el patrón de control [Toggle](uiauto-implementingtoggle.md) , pero no ambos. Se debe admitir el patrón de control Toggle si el botón puede recorrer una serie de hasta tres Estados. Normalmente, se considera como un conmutador de encendido y apagado para características específicas.                                                                        |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de botón deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**\_InvokedEventId de invocación de UIA \_**](uiauto-event-ids.md)                                                     | Si el control admite el patrón de control [Invoke](uiauto-implementinginvoke.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ToggleToggleStatePropertyId.    | Si el control admite el patrón de control [Toggle](uiauto-implementingtoggle.md) , debe admitir este evento.           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




