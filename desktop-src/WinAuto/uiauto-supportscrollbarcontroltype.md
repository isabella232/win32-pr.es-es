---
title: Tipo de control ScrollBar
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control ScrollBar.
ms.assetid: c89ca087-3e93-4e86-ac79-731e3e7a361d
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control ScrollBar
- Automatización de la interfaz de usuario, tipo de control ScrollBar
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control ScrollBar
- Automatización de la interfaz de usuario,properties para el tipo de control ScrollBar
- Automatización de la interfaz de usuario,patrones de control para el tipo de control ScrollBar
- Automatización de la interfaz de usuario,events para el tipo de control ScrollBar
- estructuras de árbol, tipo de control ScrollBar
- properties,Tipo de control ScrollBar
- patrones de control, tipo de control ScrollBar
- events,Tipo de control ScrollBar
- Compatibilidad con el tipo de control ScrollBar
- Tipo de control ScrollBar
- tipos de control, estructura de árbol para el tipo de control ScrollBar
- tipos de control, patrones de control para el tipo de control ScrollBar
- tipos de control, compatibilidad con ScrollBar
- tipos de control,ScrollBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e9da37ec8006eae0c710ed4dcd336caf76cf3a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467792"
---
# <a name="scrollbar-control-type"></a>Tipo de control ScrollBar

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **ScrollBar.**

Los controles de la barra de desplazamiento permiten a un usuario desplazarse por el contenido dentro de una ventana o contenedor de elementos. El control consta de un conjunto de botones y un control de posición.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **ScrollBar.** Los Automatización de la interfaz de usuario se aplican a todos los controles de barra de desplazamiento en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol de Automatización de la interfaz de usuario que pertenece a los controles de barra de desplazamiento y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>ScrollBar<ul><li>Botón (0, 2 o 4)</li><li>Thumb (0 o 1)</li></ul></li></ul> | No es aplicable. (El control de barra de desplazamiento no tiene contenido). | 




 

El control de barra de desplazamiento puede tener de cero a cinco secundarios. Dado que el subárbol tiene más de un control de botón, el elemento debe establecer un valor específico de [**\_ AutomationIdPropertyId de UIA**](uiauto-automation-element-propids.md) en cada elemento para que se detecten para herramientas de prueba automatizadas.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de barra de desplazamiento. Tenga en cuenta que un control de barra de desplazamiento nunca tiene contenido; su funcionalidad se expone a través del patrón de control [Scroll,](uiauto-implementingscroll.md) que se admite en el contenedor que se va a desplazar.

Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor         | Notas                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.    | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.    | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | NaN           | El control de barra de desplazamiento no tiene puntos interactivos.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Scrollbar** | Este valor es el mismo para todos los marcos de trabajo. Las barras de desplazamiento que funcionan como controles deslizantes deben usar el [tipo de](uiauto-supportslidercontroltype.md) control Slider.                                                                                                                                                                                                                                                                                                                        |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | FALSE         | El control de barra de desplazamiento nunca es un elemento de contenido. Si la barra de desplazamiento es un control independiente, debe cumplir el tipo de control [Slider](uiauto-supportslidercontroltype.md) y devolver [**UIA \_ SliderControlTypeId**](uiauto-controltype-ids.md) para la propiedad [**IUIAutomationElement::CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (o [**CachedControlType).**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype) |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE          | El control de barra de desplazamiento siempre se incluye en la vista de control del Automatización de la interfaz de usuario de desplazamiento.                                                                                                                                                                                                                                                                                                                                                                                        |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.    | Si el control puede recibir el foco del teclado, debe admitir esta propiedad. Un control de barra de desplazamiento rara vez toma el foco, pero cuando lo hace, el foco debe permanecer en el propio control de barra de desplazamiento, no en los botones secundarios ni en el control thumb. El usuario debe ser capaz de realizar todas las acciones de desplazamiento mediante las teclas FLECHA ARRIBA y FLECHA ABAJO (o FLECHA DERECHA y FLECHA IZQUIERDA), o las teclas PAGE UP y PAGE DOWN.                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | Las barras de desplazamiento no tienen etiquetas.                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.    | Cadena localizada correspondiente al tipo de control **ScrollBar.** El valor predeterminado es "barra de desplazamiento" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                                                                                                                                       |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | NULL          | El control de barra de desplazamiento no tiene elementos de contenido y no es necesario establecer la propiedad [**\_ NamePropertyId de UIA.**](uiauto-automation-element-propids.md)                                                                                                                                                                                                                                                                                           |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Vea las notas.    | El control de barra de desplazamiento siempre debe exponer su orientación horizontal o vertical.                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de barra de desplazamiento. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> Cuando una barra de desplazamiento se usa como control solo para la manipulación del mouse, no admite patrones de control. Si se usa como control deslizante dentro de una aplicación, se le debe proporcionar el tipo de control [Slider.](uiauto-supportslidercontroltype.md)

 



| Patrón de control                                           | Soporte técnico | Notas                                                                                                                                                                                                                          |
|-----------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Depende | El patrón de control [RangeValue](uiauto-implementingrangevalue.md) solo debe ser compatible si el patrón de control [Scroll](uiauto-implementingscroll.md) no se admite en el contenedor que tiene la barra de desplazamiento. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)         | Nunca   | El [patrón de](uiauto-implementingscroll.md) control Scroll nunca se admite directamente en la barra de desplazamiento.                                                                                                                     |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que los controles de barra de desplazamiento son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)        | Si el control admite el patrón de control [RangeValue,](uiauto-implementingrangevalue.md) debe admitir este evento.   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




