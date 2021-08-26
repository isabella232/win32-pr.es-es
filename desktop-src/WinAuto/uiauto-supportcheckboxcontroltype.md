---
title: Tipo de control CheckBox
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control CheckBox.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control CheckBox
- Automatización de la interfaz de usuario,tipo de control CheckBox
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control CheckBox
- Automatización de la interfaz de usuario,properties para el tipo de control CheckBox
- Automatización de la interfaz de usuario,patrones de control para el tipo de control CheckBox
- Automatización de la interfaz de usuario,events para el tipo de control CheckBox
- estructuras de árbol, tipo de control CheckBox
- properties,Tipo de control CheckBox
- patrones de control, tipo de control CheckBox
- events,Tipo de control CheckBox
- Compatibilidad con el tipo de control CheckBox
- CheckBox (tipo de control)
- tipos de control, estructura de árbol para el tipo de control CheckBox
- tipos de control, patrones de control para el tipo de control CheckBox
- tipos de control, compatibilidad con CheckBox
- tipos de control,CheckBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec20bc259095c41bd1bdc4c3d4e5953be2e883d2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467812"
---
# <a name="checkbox-control-type"></a>Tipo de control CheckBox

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **CheckBox.**

Una casilla es un objeto que se usa para indicar un estado con el que los usuarios pueden interactuar para recorrer cíclicamente dicho estado. Las casillas le presentan al usuario una opción binaria (Sí/No), (Activado/Desactivado) o terciaria (Activado, Desactivado, Indeterminado).

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **CheckBox.** Los Automatización de la interfaz de usuario se aplican a todos los controles de casilla en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [DefaultAction](#defaultaction)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de Automatización de la interfaz de usuario que pertenece a los controles de casilla y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>CheckBox</li></ul> | <ul><li>CheckBox</li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **CheckBox.** Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor        | Notas                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                                                                                                       |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                           |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic.                                                                               |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **CheckBox** |                                                                                                                                                                                                                                                                                    |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE         | El valor de esta propiedad siempre debe ser **TRUE.** Esto significa que el control de casilla siempre debe incluirse en la vista de contenido del Automatización de la interfaz de usuario árbol.                                                                                                                   |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE         | El valor de esta propiedad siempre debe ser **TRUE.** Esto significa que el control de casilla siempre debe incluirse en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                   |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null         | Los controles de casilla son autoetiquete.                                                                                                                                                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada correspondiente al tipo de control **CheckBox.** El valor predeterminado es "casilla" para en-US o inglés (Estados Unidos).                                                                                                                                            |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | El valor de la propiedad [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (o [**CachedName)**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)del control de casilla es el texto que se muestra junto al cuadro que mantiene el estado de alternancia. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control necesarios para que todos los controles de casilla sean compatibles. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                  | Soporte técnico/valor | Notas                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Requerido      | Las casillas admiten [el patrón de](uiauto-implementingtoggle.md) control Alternar para permitir que la casilla se redonde mediante programación a través de sus estados internos. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que los controles de casilla son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)    |                                                                                                                            |



 

## <a name="defaultaction"></a>DefaultAction

La acción predeterminada de la casilla es hacer que un botón de radio reciba el foco y alterne su estado actual. Como se mencionó anteriormente, las casillas presentan una decisión binaria (Sí/No o On/Off) al usuario o una decisión terciaria (On, Off, Indeterminate). Si la casilla es binaria, la acción predeterminada hace que el estado "activado" se convierta en "desactivado" o que el estado "desactivado" pase a "activado". En una casilla terciaria, la acción predeterminada se mueve por los estados de la casilla en el mismo orden que si el usuario hubiera enviado sucesivos clics del mouse al control.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




