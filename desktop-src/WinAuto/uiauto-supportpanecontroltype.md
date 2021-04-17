---
title: Pane (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control pane.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control pane
- Automatización de la interfaz de usuario, panel (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control pane
- Automatización de la interfaz de usuario, propiedades para el tipo de control pane
- Automatización de la interfaz de usuario, patrones de control para el tipo de control pane
- Automatización de la interfaz de usuario, eventos para el tipo de control pane
- estructuras de árbol, tipo de control pane
- propiedades, panel (tipo de control)
- patrones de control, panel (tipo de control)
- Events, pane (tipo de control)
- compatibilidad con el tipo de control pane
- Pane (tipo de control)
- tipos de control, estructura de árbol para el tipo de control pane
- tipos de control, patrones de control para el tipo de control pane
- tipos de control, compatibilidad con el panel
- tipos de control, panel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51b7f22e6fb302ebb160a174c27c61119b8f09fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104561778"
---
# <a name="pane-control-type"></a>Pane (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **pane** .

El tipo de control **pane** es para las regiones posiblemente desplazables que tienen contenido dispares. Se utiliza para representar un objeto dentro de una ventana de documento o marco. Los usuarios pueden desplazarse entre los controles de panel y dentro del contenido del panel actual. Los controles de panel representan un nivel de agrupación inferior a ventanas o documentos, pero por encima de los controles individuales. El usuario navega entre paneles presionando TAB, F6 o CTRL+TAB, dependiendo del contexto.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **pane** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de panel donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Ejemplo de tipo de control de panel](#pane-control-type-example)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de panel y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Panel</li>
</ul></td>
<td><ul>
<li>Panel</li>
</ul></td>
</tr>
</tbody>
</table>



 

Un control de panel siempre aparece en las vistas de control y de contenido. No exponga un objeto de diseño como un panel en la vista de control o de contenido si el objeto solo se usa para la presentación visual.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de panel. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si una combinación de teclas específica proporciona el foco al panel, dicha información debería exponerse a través de esta propiedad.                                                                                                                                                                                                      |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Esta propiedad expone un punto en el que se puede hacer clic del control de panel que hace que el enfoque se sitúe en el panel cuando se hace clic en él.                                                                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Panel**   |                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas. | El texto de ayuda de los controles de panel debe explicar el propósito del marco y cómo se relaciona con otros marcos. Se necesita una descripción si el propósito y la relación de los marcos no están claros en el valor de la propiedad [**\_ NamePropertyId de UIA**](uiauto-automation-element-propids.md) . |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control de panel siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control de panel siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                             |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Los controles de panel normalmente no tienen una etiqueta estática. Si hay una etiqueta de texto estático, se debe exponer a través de esta propiedad.                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **pane** . El valor predeterminado es "Pane" para en-US o inglés (Estados Unidos).                                                                                                                                                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El valor de esta propiedad siempre debe ser un título claro, conciso y significativo.                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por los controles de panel. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico | Notas                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Depende | Implemente el patrón de control [Dock](uiauto-implementingdock.md) si el control de panel se puede acoplar.                                                                                          |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depende | Implemente el patrón de control [Scroll](uiauto-implementingscroll.md) si se puede desplazar el control de panel.                                                                                    |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depende | Implemente el patrón de control [Transform](uiauto-implementingtransform.md) si el control de panel se puede desplazar, cambiar de tamaño o girar en la pantalla.                                              |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Nunca   | Si el elemento necesita implementar el patrón de control [Window](uiauto-implementingwindow.md) , el control debe basarse en el tipo de control [Window](uiauto-supportwindowcontroltype.md) . |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que admiten los controles de panel. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                        | Notas                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                  | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontallyScrollablePropertyId.   | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalScrollPercentPropertyId. | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalViewSizePropertyId.           | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticallyScrollablePropertyId.       | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalScrollPercentPropertyId.     | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalViewSizePropertyId.               | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a>Ejemplo de tipo de control de panel

En la imagen siguiente se muestra un control que implementa el tipo de control **pane** .

![captura de pantalla que muestra un ejemplo de un control de panel](images/panexmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Árbol de UI Automation: vista de control</th>
<th>Árbol de UI Automation: vista de contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Panel
<ul>
<li>Tree (patrón de desplazamiento)
<ul>
<li>TreeItem</li>
<li>...</li>
</ul></li>
</ul></li>
<li>Panel
<ul>
<li>Edit (patrón de desplazamiento)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Panel
<ul>
<li>Tree (patrón de desplazamiento)
<ul>
<li>TreeItem</li>
<li>...</li>
</ul></li>
<li>Panel
<ul>
<li>Edit (patrón de desplazamiento)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




