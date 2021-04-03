---
title: ToolTip (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control ToolTip. Los controles de información sobre herramientas son ventanas emergentes que contienen texto.
ms.assetid: 810f85a9-4d3b-4ceb-bd2c-bf70e8712ae2
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control ToolTip
- UI Automation, ToolTip (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control ToolTip
- UI Automation, propiedades para el tipo de control ToolTip
- Automatización de la interfaz de usuario, patrones de control para ToolTip (tipo de control)
- Automatización de la interfaz de usuario, eventos para el tipo de control ToolTip
- estructuras de árbol, ToolTip (tipo de control)
- propiedades, ToolTip (tipo de control)
- patrones de control, ToolTip (tipo de control)
- Events, ToolTip (tipo de control)
- compatibilidad con el tipo de control ToolTip
- ToolTip (tipo de control)
- tipos de control, estructura de árbol para el tipo de control ToolTip
- tipos de control, patrones de control para ToolTip (tipo de control)
- tipos de control, compatibilidad con la información sobre herramientas
- tipos de control, información sobre herramientas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3c9f227faf5dd9844f809dac43cf160371490d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775841"
---
# <a name="tooltip-control-type"></a>ToolTip (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **ToolTip** . Los controles de información sobre herramientas son ventanas emergentes que contienen texto.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **ToolTip** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de información sobre herramientas donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de información sobre herramientas y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Información sobre herramientas
<ul>
<li>Text (0 o más)</li>
<li>Imagen (0 o más)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Información sobre herramientas</li>
</ul></td>
</tr>
</tbody>
</table>



 

Los controles de información sobre herramientas solo aparecen en la vista de contenido del árbol de automatización de la interfaz de usuario si pueden recibir el foco de teclado. De lo contrario, toda la información de la información sobre herramientas está disponible en la propiedad [**IUIAutomationElement:: CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (o [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) en el elemento al que hace referencia la información sobre herramientas.

La información sobre herramientas debe aparecer debajo del control al que hace referencia su información. Los clientes deben escuchar el [**\_ ToolTipOpenedEventId de UIA**](uiauto-event-ids.md) para asegurarse de que obtienen de forma coherente la información contenida en la información sobre herramientas.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **ToolTip** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value       | Notas                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.  | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.  | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.  | El punto en el que se puede hacer clic debe ser la parte de la información sobre herramientas que descarta el control. Algunos componentes de información sobre herramientas no tienen esta capacidad y no tendrán un punto en el que se pueda hacer clic.                                                                                                                                                                                                  |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ToolTip** |                                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | Depende     | Si el control de información sobre herramientas puede recibir el foco de teclado, debe aparecer en la vista de contenido del árbol de. Si solo es texto, está disponible como la propiedad [**IUIAutomationElement:: CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (o [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) del control que lo provocó. |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | True        | El control ToolTip siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.  | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | Los controles de información sobre herramientas siempre se etiquetan automáticamente por su contenido.                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.  | Cadena localizada que corresponde al tipo de control ToolTip. El valor predeterminado es "ToolTip" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.  | El nombre del control de información sobre herramientas es el texto que se muestra en la información sobre herramientas.                                                                                                                                                                                                                                                                              |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que deben admitir los controles de información sobre herramientas. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                   | Soporte técnico | Notas                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Depende | Para mejorar la accesibilidad, un control de información sobre herramientas puede admitir el patrón de control [Text](uiauto-implementingtextandtextrange.md) , aunque no es necesario. El patrón de control Text es útil cuando el texto tiene atributos y estilo enriquecidos (por ejemplo, color, negrita y cursiva). |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) | Depende | La información sobre herramientas que se puede cerrar haciendo clic en un elemento de la interfaz de usuario debe admitir el patrón de control [Window](uiauto-implementingwindow.md) para que se puedan cerrar automáticamente.                                                                                                                 |



 

## <a name="required-events"></a>Eventos necesarios

Los controles de información sobre herramientas deben generar el evento de [**\_ ToolTipOpenedEventId de UIA**](uiauto-event-ids.md) cuando aparecen en la pantalla. El evento incluirá una referencia al elemento de automatización de la interfaz de usuario de la información sobre herramientas.

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que deben admitir los controles de información sobre herramientas. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                            | Notas                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                               |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.          |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                          | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                      | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de NamePropertyId.                                    |                                                                                                                            |
| [**\_TextChangedEventId de texto de UIA \_**](uiauto-event-ids.md)                                                          | Si el control admite el patrón de control [Text](uiauto-implementingtextandtextrange.md) , debe admitir este evento.   |
| [**UIA \_ ToolTipClosedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**Ventana de UIA \_ \_ WindowClosedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [Window](uiauto-implementingwindow.md) , debe admitir este evento.           |
| [**Ventana de UIA \_ \_ WindowOpenedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [Window](uiauto-implementingwindow.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de WindowWindowVisualStatePropertyId. | Si el control admite el patrón de control [Window](uiauto-implementingwindow.md) , debe admitir este evento.           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




