---
title: StatusBar (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control StatusBar.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control StatusBar
- Automatización de la interfaz de usuario, tipo de control StatusBar
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control StatusBar
- Automatización de la interfaz de usuario, propiedades para el tipo de control StatusBar
- Automatización de la interfaz de usuario, patrones de control para el tipo de control StatusBar
- Automatización de la interfaz de usuario, eventos para el tipo de control StatusBar
- estructuras de árbol, tipo de control StatusBar
- Properties, StatusBar (tipo de control)
- patrones de control, StatusBar (tipo de control)
- Events, StatusBar (tipo de control)
- compatibilidad con el tipo de control StatusBar
- StatusBar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control StatusBar
- tipos de control, patrones de control para el tipo de control StatusBar
- tipos de control, compatibilidad con StatusBar
- tipos de control, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ace64d34429a6d381dfdef2d99d82a3693fca2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357379"
---
# <a name="statusbar-control-type"></a>StatusBar (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **StatusBar** .

Un control de barra de estado muestra información sobre un objeto que se ve en una ventana de una aplicación, el componente del objeto o información contextual relativa a esa operación del objeto en la aplicación.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **StatusBar** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de barra de estado donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de barra de estado y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>StatusBar
<ul>
<li>Edición (0 o más)</li>
<li>ProgressBar (0 o muchos)</li>
<li>Imagen (0 o muchos)</li>
<li>Botón (0 o muchos)</li>
</ul></li>
</ul></td>
<td><ul>
<li>StatusBar
<ul>
<li>Edición (0 o más)</li>
<li>ProgressBar (0 o muchos)</li>
<li>Imagen (0 o muchos)</li>
<li>Botón (0 o muchos)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de barra de estado. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value         | Notas                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.    | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.    | El rectángulo delimitador de una barra de estado debe abarcar todos los controles que incluye.                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.    | Se admite si hay un rectángulo delimitador. Si hay áreas dentro del rectángulo delimitador que no son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto en el que se pueden hacer clic. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **StatusBar** |                                                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | El control de barra de estado siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | El control de barra de estado siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Depende       | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Depende       | Si un control de barra de estado no está visible actualmente, devolverá TRUE para esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | Normalmente, el control de barra de estado no tiene una etiqueta.                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.    | Cadena localizada que corresponde al tipo de control **StatusBar** . El valor predeterminado es "barra de estado" para en-US o inglés (Estados Unidos).                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.    | El control de barra de estado no necesita un nombre a menos que se use más de uno dentro de una aplicación. En este caso, distinga cada barra con nombres como "estado de Internet" o "estado de la aplicación".                    |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Depende       | Un valor que indica la orientación del control: horizontal o vertical.                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que se deben admitir para los controles de barra de estado. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                               | Soporte técnico  | Notas                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | Opcionales | Los controles de barra de estado deben admitir el patrón de control de [cuadrícula](uiauto-implementinggrid.md) para que se puedan supervisar y hacer referencia fácilmente a las partes individuales para obtener información. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de barra de estado deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad **IsEnabled** , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad **IsOffscreen** , debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a>Observaciones

Se recomienda utilizar los controles de edición como elementos de cuadrícula secundarios en una barra de estado. El uso de controles de edición facilita la Asociación del propósito del campo de estado con su valor mediante el uso de la propiedad nombre y valor del elemento. Dado que los controles de texto no deben admitir el patrón de control **Value** , no deben usarse como elementos de cuadrícula secundarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




