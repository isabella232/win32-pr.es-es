---
title: Tipo de control Separador
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Separador.
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Separador
- Automatización de la interfaz de usuario,Tipo de control Separator
- Automatización de la interfaz de usuario,estructura de árbol para el tipo de control Separador
- Automatización de la interfaz de usuario,properties para el tipo de control Separator
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Separador
- Automatización de la interfaz de usuario,events para el tipo de control Separator
- estructuras de árbol, tipo de control Separador
- properties,Separator (tipo de control)
- patrones de control, tipo de control Separador
- events,Separator (tipo de control)
- Compatibilidad con el tipo de control Separador
- Separator (tipo de control)
- tipos de control, estructura de árbol para tipo de control Separador
- tipos de control, patrones de control para el tipo de control Separador
- tipos de control, compatibilidad con Separador
- tipos de control, Separador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0685f21565a6252febfadad115c8edf10990995c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477721"
---
# <a name="separator-control-type"></a>Tipo de control Separador

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo **de** control Separador.

Los controles de separador se usan para dividir visualmente un espacio en dos regiones. Por ejemplo, un control de separador puede ser una barra que defina dos paneles en una ventana. Si se puede mover el separador, el control debe exponerse como Thumb en el tipo de control.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **Separador.** Los Automatización de la interfaz de usuario se aplican a todos los controles separadores en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece a los controles separadores y se describe lo que se puede incluir en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Separador</li></ul> | <ul><li>El <strong>tipo de</strong> control Separador nunca tiene contenido.</li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles separadores. Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor         | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.    | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.    | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.    | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Separador** |                                                                                                                                                                                                      |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | FALSE         | El control Separator nunca es contenido.                                                                                                                                                              |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE          | El control de separador siempre debe ser un control.                                                                                                                                                      |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.    | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | El control de separador no tiene una etiqueta estática.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.    | Cadena localizada correspondiente al tipo **de** control Separador. El valor predeterminado es "Separador" para en-US o inglés (Estados Unidos).                                                             |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | ""            | El control separador no requiere una **propiedad Name.**                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

El control de separador no debe admitir ningún patrón de control. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles separadores son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




