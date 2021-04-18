---
title: ScrollBar (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control ScrollBar.
ms.assetid: c89ca087-3e93-4e86-ac79-731e3e7a361d
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control ScrollBar
- Automatización de la interfaz de usuario, tipo de control ScrollBar
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control ScrollBar
- Automatización de la interfaz de usuario, propiedades para el tipo de control ScrollBar
- Automatización de la interfaz de usuario, patrones de control para el tipo de control ScrollBar
- Automatización de la interfaz de usuario, eventos para el tipo de control ScrollBar
- estructuras de árbol, tipo de control ScrollBar
- Properties, ScrollBar (tipo de control)
- patrones de control, ScrollBar (tipo de control)
- Events, ScrollBar (tipo de control)
- compatibilidad con el tipo de control ScrollBar
- ScrollBar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control ScrollBar
- tipos de control, patrones de control para el tipo de control ScrollBar
- tipos de control, compatibilidad con ScrollBar
- tipos de control, ScrollBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2168401c313dd9139f44ba615de945802b307d64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695396"
---
# <a name="scrollbar-control-type"></a>ScrollBar (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **ScrollBar** .

Los controles de la barra de desplazamiento permiten a un usuario desplazarse por el contenido dentro de una ventana o contenedor de elementos. El control está compuesto de un conjunto de botones y un control Thumb.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **ScrollBar** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de barra de desplazamiento en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de barra de desplazamiento y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>ScrollBar
<ul>
<li>Button (0, 2 o 4)</li>
<li>Thumb (0 o 1)</li>
</ul></li>
</ul></td>
<td>No es aplicable. (El control de barra de desplazamiento no tiene contenido).</td>
</tr>
</tbody>
</table>



 

El control de barra de desplazamiento puede tener de cero a cinco elementos secundarios. Dado que el subárbol tiene más de un control de botón, el elemento debe establecer un valor específico de [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md) en cada elemento para que se puedan detectar en herramientas de pruebas automatizadas.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de barra de desplazamiento. Tenga en cuenta que un control de barra de desplazamiento nunca tiene contenido; su funcionalidad se expone a través del patrón de control [Scroll](uiauto-implementingscroll.md) , que se admite en el contenedor que se está desplazando.

Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value         | Notas                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.    | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.    | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | NaN           | El control de barra de desplazamiento no tiene puntos interactivos.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Desplazamiento** | Este valor es el mismo para todos los marcos de trabajo. Las barras de desplazamiento que funcionan como controles deslizantes deben usar el tipo de control [Slider](uiauto-supportslidercontroltype.md) .                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | false         | El control de barra de desplazamiento nunca es un elemento de contenido. Si la barra de desplazamiento es un control independiente, debe cumplir el tipo de control [Slider](uiauto-supportslidercontroltype.md) y devolver [**UIA \_ SliderControlTypeId**](uiauto-controltype-ids.md) para la propiedad [**IUIAutomationElement:: CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (o [**CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)). |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | El control de barra de desplazamiento siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.    | Si el control puede recibir el foco del teclado, debe admitir esta propiedad. Un control de barra de desplazamiento raramente toma el foco, pero cuando lo hace, el foco debe permanecer en el propio control de barra de desplazamiento, no en los botones secundarios ni en el control de posición. El usuario debe poder realizar todas las acciones de desplazamiento mediante las teclas flecha arriba y flecha abajo (o flecha derecha y flecha izquierda), o las teclas Re Pág y Av Pág.                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | Las barras de desplazamiento no tienen etiquetas.                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.    | Cadena localizada que corresponde al tipo de control **ScrollBar** . El valor predeterminado es "barra de desplazamiento" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULL          | El control de barra de desplazamiento no tiene elementos de contenido y no es necesario establecer la propiedad [**\_ NamePropertyId de UIA**](uiauto-automation-element-propids.md) .                                                                                                                                                                                                                                                                                           |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Vea las notas.    | El control de barra de desplazamiento siempre debe exponer su orientación horizontal o vertical.                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que se deben admitir por todos los controles de barra de desplazamiento. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> Cuando se usa una barra de desplazamiento como control para la manipulación del mouse únicamente, no es compatible con los patrones de control. Si se usa como control deslizante dentro de una aplicación, se le debe proporcionar el tipo de control [Slider](uiauto-supportslidercontroltype.md) .

 



| Patrón de control                                           | Soporte técnico | Notas                                                                                                                                                                                                                          |
|-----------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Depende | El patrón de control [RangeValue](uiauto-implementingrangevalue.md) solo se admite si el patrón de control [Scroll](uiauto-implementingscroll.md) no se admite en el contenedor que tiene la barra de desplazamiento. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)         | Nunca   | El patrón de control [Scroll](uiauto-implementingscroll.md) nunca se admite directamente en la barra de desplazamiento.                                                                                                                     |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de barra de desplazamiento deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de RangeValueValuePropertyId.        | Si el control admite el patrón de control [RangeValue](uiauto-implementingrangevalue.md) , debe admitir este evento.   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




