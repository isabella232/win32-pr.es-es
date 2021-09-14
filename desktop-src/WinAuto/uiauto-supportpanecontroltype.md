---
title: Tipo de control Panel
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Pane.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Panel
- Automatización de la interfaz de usuario,Tipo de control Pane
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control Panel
- Automatización de la interfaz de usuario,properties para el tipo de control Pane
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Panel
- Automatización de la interfaz de usuario,events para el tipo de control Pane
- estructuras de árbol, tipo de control Pane
- properties,Tipo de control Pane
- patrones de control, tipo de control Pane
- events,Tipo de control Pane
- Compatibilidad con el tipo de control Panel
- Pane (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Pane
- tipos de control, patrones de control para el tipo de control Panel
- tipos de control, compatibilidad con el panel
- tipos de control, Panel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b335496d8d40d20ccc68f6bc2b048c87ff608dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242307"
---
# <a name="pane-control-type"></a>Tipo de control Panel

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo **de** control Pane.

El **tipo** de control Pane es para las regiones potencialmente desplazables que tienen contenido dispare. Se usa para representar un objeto dentro de un marco o ventana de documento. Los usuarios pueden navegar entre los controles de panel y dentro del contenido del panel actual. Los controles de panel representan un nivel de agrupación inferior al de ventanas o documentos, pero por encima de los controles individuales. El usuario navega entre paneles presionando TAB, F6 o CTRL+TAB, dependiendo del contexto.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo **de** control Pane. Los Automatización de la interfaz de usuario se aplican a todos los controles de panel en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Ejemplo de tipo de control de panel](#pane-control-type-example)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de panel y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario árbol, vea [Información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Panel</li></ul> | <ul><li>Panel</li></ul> | 




 

Un control de panel siempre aparece en las vistas de control y contenido. No exponga un objeto de diseño como panel en el control o la vista de contenido si el objeto solo se usa para la presentación visual.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de panel. Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessKeyPropertyId de UIA \_**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si una combinación de claves específica proporciona el foco al panel, esa información debe exponerse a través de esta propiedad.                                                                                                                                                                                                      |
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Esta propiedad expone un punto en el que se puede hacer clic del control de panel que hace que el enfoque se sitúe en el panel cuando se hace clic en él.                                                                                                                                                                                                |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Panel**   |                                                                                                                                                                                                                                                                                                                       |
| [**HelpTextPropertyId de UIA \_**](uiauto-automation-element-propids.md)                         | Vea las notas. | El texto de ayuda de los controles de panel debe explicar el propósito del marco y cómo se relaciona con otros fotogramas. Es necesaria una descripción si el propósito y la relación de los fotogramas no están claros del valor de la propiedad [**\_ NamePropertyId de UIA.**](uiauto-automation-element-propids.md) |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true       | El control de panel siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                                                    |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true       | El control de panel siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                                                                                                                    |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                             |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Los controles de panel normalmente no tienen una etiqueta estática. Si hay una etiqueta de texto estático, se debe exponer a través de esta propiedad.                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo **de** control Pane. El valor predeterminado es "panel" para en-US o inglés (Estados Unidos).                                                                                                                                                                                        |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El valor de esta propiedad siempre debe ser un título claro, conciso y significativo.                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con los controles de panel. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico | Notas                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Depende | Implemente [el patrón de](uiauto-implementingdock.md) control Dock si el control de panel se puede acoplar.                                                                                          |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depende | Implemente [el patrón de](uiauto-implementingscroll.md) control Scroll si se puede desplazar el control de panel.                                                                                    |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depende | Implemente [el patrón](uiauto-implementingtransform.md) de control Transformar si el control de panel se puede mover, cambiar de tamaño o girar en la pantalla.                                              |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Nunca   | Si el elemento necesita implementar el patrón de control [Window,](uiauto-implementingwindow.md) el control debe basarse en el tipo de control [Window.](uiauto-supportwindowcontroltype.md) |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de panel son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                        | Notas                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a>Ejemplo de tipo de control de panel

En la imagen siguiente se muestra un control que implementa el tipo de control **Pane.**

![captura de pantalla que muestra un ejemplo de un control de panel](images/panexmpl.jpg)




| Automatización de la interfaz de usuario árbol: Vista de control | Automatización de la interfaz de usuario árbol de contenido: vista de contenido | 
|-----------------------------------|-----------------------------------|
| <ul><li>Panel<ul><li>Tree (patrón de desplazamiento)<ul><li>TreeItem</li><li>...</li></ul></li></ul></li><li>Panel<ul><li>Editar (patrón de desplazamiento)</li></ul></li></ul> | <ul><li>Panel<ul><li>Tree (patrón de desplazamiento)<ul><li>TreeItem</li><li>...</li></ul></li><li>Panel<ul><li>Editar (patrón de desplazamiento)</li></ul></li></ul></li></ul> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




