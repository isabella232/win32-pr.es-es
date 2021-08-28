---
title: Tipo de control MenuBar
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control MenuBar.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control MenuBar
- Automatización de la interfaz de usuario, tipo de control MenuBar
- Automatización de la interfaz de usuario,estructura de árbol para el tipo de control MenuBar
- Automatización de la interfaz de usuario,properties para el tipo de control MenuBar
- Automatización de la interfaz de usuario,patrones de control para el tipo de control MenuBar
- Automatización de la interfaz de usuario,events para el tipo de control MenuBar
- estructuras de árbol, tipo de control MenuBar
- properties,MenuBar (tipo de control)
- patrones de control, tipo de control MenuBar
- events,MenuBar (tipo de control)
- compatibilidad con el tipo de control MenuBar
- Tipo de control MenuBar
- tipos de control, estructura de árbol para el tipo de control MenuBar
- tipos de control, patrones de control para el tipo de control MenuBar
- tipos de control, compatibilidad con MenuBar
- tipos de control, MenuBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558a734d69a9197b3e0a8d6c5655405074878bca
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468162"
---
# <a name="menubar-control-type"></a>Tipo de control MenuBar

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **MenuBar.**

Los controles de barra de menús son un ejemplo de controles que implementan el tipo de control **MenuBar.** Las barras de menús proporcionan un medio para que los usuarios activen los comandos y las opciones contenidos en una aplicación.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **MenuBar.** Los Automatización de la interfaz de usuario se aplican a todos los controles de barra de menús en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece a los controles de la barra de menús y se describe lo que se puede incluir en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, [vea información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>MenuBar<ul><li>MenuItem (1 o más)</li><li>Otros controles (0 o varios)</li></ul></li></ul> | <ul><li>No aplicable<ul><li>MenuItem (1 o más)</li><li>Otros controles (0 o varios)</li></ul></li></ul> | 




 

Un control de barra de menús siempre aparece en la vista de control, pero no en la vista de contenido porque normalmente no transmite información significativa al usuario final (a menos que la aplicación contenga más de una barra de menús).

Automatización de la interfaz de usuario clientes pueden escuchar el evento [**\_ MenuModeStartEventId**](uiauto-event-ids.md) de UIA para asegurarse de que se les notifica de forma coherente cuando la interfaz de usuario entra en modo de menú. Cuando la aplicación está en modo de menú, se puede capturar toda la entrada del  teclado para la navegación por el menú (por ejemplo, escribir "s" podría invocar el menú Guardar en lugar de escribir el carácter en el área de cliente de la aplicación). El **evento \_ MenuModeStartEventId** de UIA debe preceder al primer evento [**\_ MenuOpenedEventId**](uiauto-event-ids.md) de UIA para garantizar la coherencia lógica. El [**evento \_ MenuModeEndEventId de UIA**](uiauto-event-ids.md) sigue al último evento [**\_ MenuClosedEventId de UIA.**](uiauto-event-ids.md) Al hacer clic en un elemento de menú también se puede desencadenar inmediatamente el evento **\_ MenuModeStartEventId de UIA,** seguido de un evento **\_ MenuOpenedEventId de UIA.**

Un control de barra de menús puede contener otros controles, como controles de edición y cuadros combinados, dentro de su estructura. Estos controles adicionales corresponden a la categoría "otros controles" que se indica anteriormente en las vistas de control y de contenido.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **MenuBar.** Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor       | Notas                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcceleratorKeyPropertyId de UIA \_**](uiauto-automation-element-propids.md)             | NULL        | Normalmente, las barras de menús no tienen teclas de aceleración.                                                                                                                                                                                          |
| [**AccessKeyPropertyId de UIA \_**](uiauto-automation-element-propids.md)                       | "Alt"       | Al presionar la tecla ALT, normalmente debería aparecer el foco en la barra de menús dentro de la aplicación.                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.  | El valor que expone esta propiedad debe incluir todos los controles que se contienen dentro de ella.                                                                                                                                                 |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **MenuBar** |                                                                                                                                                                                                                                          |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | FALSE       | El control de barra de menús no se incluye en la vista de contenido del Automatización de la interfaz de usuario menú.                                                                                                                                                      |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE        | El control de barra de menús siempre se incluye en la vista de control del Automatización de la interfaz de usuario menú.                                                                                                                                                   |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | TRUE        | Los controles de barra de menús pueden recibir el foco del teclado porque los controles que contienen pueden recibir el foco de teclado.                                                                                                                                      |
| [**IsOffscreenPropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | Vea las notas.  | El valor de esta propiedad depende de si el control es visible en la pantalla.                                                                                                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | Normalmente, los controles de la barra de menús no tienen una etiqueta.                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.  | Cadena localizada correspondiente al tipo de control **MenuBar.** El valor predeterminado es "barra de menús" para en-US o inglés (Estados Unidos).                                                                                                    |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.  | El control de barra de menús no necesita un nombre a menos que una aplicación tenga más de una barra de menús. Si hay más de una barra de menús en una aplicación, use esta propiedad para exponer nombres distintivos, como "Formatting" o "Outlining". |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Depende     | Esta propiedad expone si el control de barra de menús es horizontal o vertical.                                                                                                                                                            |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con los controles de la barra de menús. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico | Notas                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Si el control se puede expandir o contraer, debe implementar el patrón de control [ExpandCollapse.](uiauto-implementingexpandcollapse.md) |
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Depende | Si el control se puede acoplar a diferentes partes de la pantalla, debe implementar el patrón de control [Dock.](uiauto-implementingdock.md)   |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Depende | Si el control se puede cambiar de tamaño, girar o mover, debe implementar el patrón de control [Transformar.](uiauto-implementingtransform.md)      |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que los controles de la barra de menús son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                                | Notas                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) | Si el control admite el patrón de control [ExpandCollapse,](uiauto-implementingexpandcollapse.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.         |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




