---
title: Tipo de control menu
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Menu.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Menú
- Automatización de la interfaz de usuario,Tipo de control Menu
- Automatización de la interfaz de usuario,tree structure for Menu control type
- Automatización de la interfaz de usuario,properties para tipo de control Menu
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Menu
- Automatización de la interfaz de usuario,events para el tipo de control Menu
- estructuras de árbol, tipo de control Menu
- properties,Menu (Tipo de control)
- patrones de control, tipo de control Menu
- events,Tipo de control Menu
- Compatibilidad con el tipo de control Menú
- Menu (tipo de control)
- tipos de control, estructura de árbol para tipo de control Menu
- tipos de control, patrones de control para tipo de control Menu
- tipos de control, compatibilidad con menu
- tipos de control, Menú
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d86d5aad29519bca4e9cfe03da4b6f0e9ccaeb9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468082"
---
# <a name="menu-control-type"></a>Tipo de control menu

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo **de** control Menu.

Un control de menú permite organizar jerárquicamente los elementos asociados a comandos y controladores de eventos. En una aplicación de Microsoft Windows típica, una barra de menús contiene varios botones de menú (como **Archivo,** Edición y **Ventana)** y cada botón de menú muestra un menú.  Un menú contiene una colección de elementos de menú (como **Nuevo**, **Abrir** y **Cerrar**), que se puede expandir para mostrar elementos de menú adicionales o realizar una acción específica cuando se haga clic en ellos.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, las propiedades, los patrones de control y los eventos necesarios para el tipo **de** control Menu. Los Automatización de la interfaz de usuario se aplican a todos los controles de menú en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de menú y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Menú<ul><li>MenuItem (1 o varios)</li></ul><ul><li>Otros controles (0 o varios)</li></ul></li></ul> | <ul><li>Menú<ul><li>MenuItem (1 o varios)</li></ul><ul><li>Otros controles (0 o varios)</li></ul></li></ul> | 




 

Los controles de menú siempre aparecen en la vista de control y en la vista de contenido Automatización de la interfaz de usuario árbol. Los controles de menú deben aparecer bajo el control al que hace referencia su información. Automatización de la interfaz de usuario clientes pueden escuchar [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) para asegurarse de que obtienen de forma coherente la información que transmiten los controles de menú. Los controles de menú contextual son un caso especial. Pueden aparecer como secundarios del escritorio o de una ventana de aplicación de nivel superior.

Un control de menú puede contener otros controles, como controles de edición y cuadros combinados, dentro de su estructura. Estos controles adicionales corresponden a los "otros controles" enumerados en la tabla anterior en las vistas de control y contenido.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo **de** control Menu. Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                      | Valor      | Notas                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)           | **Menú**   |                                                                                                                                                                         |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md) | TRUE       | El control de menú siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario árbol.                                                                                      |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md) | TRUE       | El control de menú siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)               | NULL       | No se espera ninguna etiqueta con un control de menú típico.                                                                                                                    |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas. | El control de menú no requiere que se establezca una propiedad **Name** o podría tener el mismo nombre que el control asociado, como un elemento de menú que abrió el submenú. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

No hay ningún patrón de control necesario para el tipo de control Menu.

## <a name="required-events"></a>Eventos necesarios

Los controles de menú deben [**generar el evento \_ UIA MenuOpenedEventId**](uiauto-event-ids.md) cuando aparecen en la pantalla. El **evento \_ MenuOpenedEventId de UIA** incluirá el texto del control. El [**evento \_ MenuClosedEventId de UIA**](uiauto-event-ids.md) debe generarse cuando un menú desaparece de la pantalla.

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que los controles de menú son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**Menú de \_ UIAOpenedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




