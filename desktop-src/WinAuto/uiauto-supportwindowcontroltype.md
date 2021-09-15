---
title: Tipo de control De ventana
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Window.
ms.assetid: 521fb514-e083-48b3-b4a0-52c530154740
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Ventana
- Automatización de la interfaz de usuario,Tipo de control Window
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control Ventana
- Automatización de la interfaz de usuario,properties para el tipo de control Window
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Ventana
- Automatización de la interfaz de usuario,events para el tipo de control Window
- estructuras de árbol, tipo de control De ventana
- properties,Tipo de control Window
- patrones de control, tipo de control De ventana
- events,Tipo de control De ventana
- Compatibilidad con el tipo de control Ventana
- Window (tipo de control)
- tipos de control, estructura de árbol para tipo de control Ventana
- tipos de control, patrones de control para el tipo de control Ventana
- tipos de control, compatibilidad con Window
- tipos de control, Ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59486f12545c0dbe6b38e20e29f6df5397cbca21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465989"
---
# <a name="window-control-type"></a>Tipo de control De ventana

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **Window.**

El control de ventana consta del marco de la ventana, que contiene objetos secundarios como la barra de título, el cliente y otros objetos.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Window.** Los Automatización de la interfaz de usuario se aplican a todos los controles de ventana en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de ventana y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario árbol, vea [Información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Periodo</li></ul> | <ul><li>Periodo</li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de ventana. Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                            |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | El control de ventana debe tener un punto en el que se pueda hacer clic que haga que la ventana se seleccione o no se seleccione.                                                 |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Ventana** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                           |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true       | El control de ventana siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario ventana.                                                                    |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true       | El control de ventana siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                    |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                               |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | Los controles de ventana no tienen una etiqueta de ventana estática.                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo **de** control Ventana. El valor predeterminado es "window" para en-US o inglés (Estados Unidos).                      |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El control de ventana siempre contiene un elemento de ventana principal relacionado con lo que el usuario asociaría como el identificador más semántico del elemento. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con los controles de ventana. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                        | Soporte técnico/valor | Notas                                                                                                                                                                        |
|---------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Condicional   | El [patrón de](uiauto-implementingdock.md) control Dock debe ser compatible si la ventana se puede acoplar.                                                                       |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Obligatorio      | El [patrón](uiauto-implementingtransform.md) de control Transformar permite mover, cambiar el tamaño o girar la ventana en la pantalla. (No se aplica a las Windows Store). |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Obligatorio      | El [patrón de](uiauto-implementingwindow.md) control Ventana habilita operaciones específicas para la ventana.                                                                      |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que los controles **Window** son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                        | Notas                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                                                                                                           |
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                                           |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                                                                                                                           |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento.                                                                                                |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                                           |
| [**UIA \_ Evento de cambio de propiedad NamePropertyId.**](uiauto-automation-element-propids.md)                                                |                                                                                                                                                                                                                           |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                                                                                          |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                                                                                          |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                                                                                          |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                                                                                          |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                                                                                          |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                                           |
| [**Ventana de \_ \_ UIAClosedEventId**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**Ventana de \_ \_ UIAOpenedEventId**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**UIA \_ Evento de cambio de propiedad WindowWindowVisualStatePropertyId.**](uiauto-control-pattern-propids.md)             | Si el control admite la [**propiedad WindowVisualState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-get_cachedwindowvisualstate) del patrón de control [Window,](uiauto-implementingwindow.md) este evento debe ser compatible. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




