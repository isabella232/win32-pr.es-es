---
title: Tipo de control ToolBar
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control ToolBar. Los controles de la barra de herramientas permiten a los usuarios finales activar comandos y herramientas contenidos en una aplicación.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control ToolBar
- Automatización de la interfaz de usuario,Tipo de control ToolBar
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control ToolBar
- Automatización de la interfaz de usuario,properties para el tipo de control ToolBar
- Automatización de la interfaz de usuario,patrones de control para el tipo de control ToolBar
- Automatización de la interfaz de usuario,events para el tipo de control ToolBar
- estructuras de árbol, tipo de control ToolBar
- properties,Tipo de control ToolBar
- patrones de control, tipo de control ToolBar
- events,Tipo de control ToolBar
- Compatibilidad con el tipo de control ToolBar
- ToolBar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control ToolBar
- tipos de control, patrones de control para el tipo de control ToolBar
- tipos de control, compatibilidad con la barra de herramientas
- tipos de control, ToolBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194c9aabaa684370b99d23d91c979ff3410305b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172606"
---
# <a name="toolbar-control-type"></a>Tipo de control ToolBar

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **ToolBar.** Los controles de la barra de herramientas permiten a los usuarios finales activar comandos y herramientas contenidos en una aplicación.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **ToolBar.** Los Automatización de la interfaz de usuario se aplican a todos los controles de la barra de herramientas en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de Automatización de la interfaz de usuario que pertenece a los controles de la barra de herramientas y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario árbol, vea [Información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>ToolBar<ul><li>Varios controles (0 o más)</li></ul></li></ul> | <ul><li>ToolBar<ul><li>Varios controles (0 o más)</li></ul></li></ul> | 




 

Un control de barra de herramientas puede contener cualquier tipo de control dentro de su subárbol. Más a menudo contienen botones, cuadros combinados y botones de expansión.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **ToolBar.** Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value       | Notas                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.  | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.  | El rectángulo exterior que contiene el control completo.                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.  | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic.       |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Barra** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                              |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true        | El control de barra de herramientas siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario árbol.                                                                                                                      |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true        | El control de barra de herramientas siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                      |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.  | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | Un control de barra de herramientas nunca tiene una etiqueta.                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.  | Cadena localizada correspondiente al tipo de control **ToolBar.** El valor predeterminado es "barra de herramientas" para en-US o inglés (Estados Unidos).                                                                      |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Depende     | El control de barra de herramientas no necesita un nombre a menos que se utilice más de uno dentro de una aplicación. Si hay más de uno, cada uno debe tener un nombre distintivo (por ejemplo, "Formato" o "Delineación"). |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con los controles de la barra de herramientas. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico | Notas                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Depende | Si la barra de herramientas se puede acoplar a diferentes partes de la pantalla, debe admitir el patrón de control [Dock.](uiauto-implementingdock.md)                       |
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Si la barra de herramientas se puede expandir y contraer para mostrar más elementos, debe admitir el patrón de control [ExpandCollapse.](uiauto-implementingexpandcollapse.md) |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Depende | Si la barra de herramientas se puede cambiar de tamaño, girar o mover, debe admitir el patrón de control [Transformar.](uiauto-implementingtransform.md)                          |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos Automatización de la interfaz de usuario que los controles de la barra de herramientas son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                                | Notas                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**UIA \_ Evento expandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) cambiado por la propiedad . | Si el control admite el patrón de control [ExpandCollapse,](uiauto-implementingexpandcollapse.md) debe admitir este evento. |
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

 

 




