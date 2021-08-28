---
title: Tipo de control TabItem
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control TabItem.
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control TabItem
- Automatización de la interfaz de usuario, tipo de control TabItem
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control TabItem
- Automatización de la interfaz de usuario,properties para el tipo de control TabItem
- Automatización de la interfaz de usuario,patrones de control para el tipo de control TabItem
- Automatización de la interfaz de usuario,events para el tipo de control TabItem
- estructuras de árbol, tipo de control TabItem
- properties,TabItem (tipo de control)
- patrones de control, tipo de control TabItem
- events,TabItem (tipo de control)
- compatibilidad con el tipo de control TabItem
- Tipo de control TabItem
- tipos de control, estructura de árbol para el tipo de control TabItem
- tipos de control, patrones de control para el tipo de control TabItem
- tipos de control, compatibilidad con TabItem
- tipos de control,TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f82b96f5ae64b4cb22d650d6d349f18cb68619d5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469112"
---
# <a name="tabitem-control-type"></a>Tipo de control TabItem

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **TabItem.**

Un control de elemento de ficha se utiliza como el control dentro de un control de ficha que selecciona una página concreta para que se muestre en una ventana.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **TabItem.** Los Automatización de la interfaz de usuario se aplican a todos los controles de elementos de pestaña en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece a los controles de elemento de tabulación y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, [vea información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>TabItem<ul><li>Image (0 o 1)</li><li>Texto</li><li>Panel<ul><li>Varios controles (0 o más)</li></ul></li></ul></li></ul> | <ul><li>TabItem<ul><li>Panel<ul><li>Varios controles (0 o más)</li></ul></li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **TabItem.** Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor       | Notas                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.  | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.  | El rectángulo exterior que contiene el control completo.                                                                                    |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.  | El control de elemento de ficha debe tener un punto en el que se pueda hacer clic que haga que se seleccione el elemento.                                                   |
| [**UIA \_ ControllerForPropertyId**](uiauto-automation-element-propids.md)               | Vea las notas.  | Esta propiedad se puede utilizar como un puntero al panel de ficha asociado. Esto es útil cuando no se puede hospedar un panel como un elemento secundario del objeto de elemento de ficha. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **TabItem** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                               |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE        | El control de elemento de pestaña siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario pestaña.                                                      |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE        | El control de elemento de pestaña siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                      |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.  | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null        | El control de elemento de ficha no tiene una etiqueta de texto estático.                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.  | Cadena localizada correspondiente al tipo de control **TabItem.** El valor predeterminado es "elemento de tabulación" para en-US o inglés (Estados Unidos).       |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.  | Control de elemento de pestaña autoetiqueta.                                                                                                          |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de elemento de pestaña. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                 | Soporte técnico  | Notas                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | Requerido | El control de elemento de pestaña debe admitir [**IUIAutomationSelectionItemPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern) |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | Nunca    | El control de elemento de pestaña nunca [**admite IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).             |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de elemento de tabulación son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                     | Notas                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                        |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)   |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                   | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)               | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**Elemento \_ SelectionItem \_ de UIARemovedFromSelectionEventId**](uiauto-event-ids.md) |                                                                                                                            |
| [**Elementos \_ SelectionItem \_ de UIASelectedEventId**](uiauto-event-ids.md)                         |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




