---
title: Tipo de control TitleBar
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control TitleBar. Un control de barra de título representa una barra de título o título en una ventana.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control TitleBar
- Automatización de la interfaz de usuario, tipo de control TitleBar
- Automatización de la interfaz de usuario,estructura de árbol para el tipo de control TitleBar
- Automatización de la interfaz de usuario,properties para el tipo de control TitleBar
- Automatización de la interfaz de usuario,patrones de control para el tipo de control TitleBar
- Automatización de la interfaz de usuario,events para el tipo de control TitleBar
- estructuras de árbol, tipo de control TitleBar
- properties,TitleBar (tipo de control)
- patrones de control, tipo de control TitleBar
- events,TitleBar (tipo de control)
- compatibilidad con el tipo de control TitleBar
- Tipo de control TitleBar
- tipos de control, estructura de árbol para el tipo de control TitleBar
- tipos de control, patrones de control para el tipo de control TitleBar
- tipos de control, compatibilidad con TitleBar
- tipos de control, TitleBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e3d3ed0c4a3abc995afab7aec4aa89d02542e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172609"
---
# <a name="titlebar-control-type"></a>Tipo de control TitleBar

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **TitleBar.** Un control de barra de título representa una barra de título o título en una ventana.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **TitleBar.** Los Automatización de la interfaz de usuario se aplican a todos los controles de barra de título en los que el marco o plataforma de la interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece a los controles de la barra de título y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>TitleBar<ul><li>Menú (0 o 1)</li><li>Botón (0 o más)</li></ul></li></ul> | (No aplicable; el control de barra de título no tiene contenido) | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **TitleBar.** Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value        | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El valor que expone esta propiedad debe incluir todos los controles que se contienen dentro de ella.                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **TitleBar** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                        |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | false        | El control de barra de título nunca se incluye en la vista de contenido del Automatización de la interfaz de usuario contenido.                                                                                                               |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true         | El control de barra de título siempre se incluye en la vista de control Automatización de la interfaz de usuario árbol.                                                                                                              |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | false        | Un control de barra de título nunca tiene el foco del teclado.                                                                                                                                                        |
| [**IsOffscreenPropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | Depende      | Un control de barra de título devuelve un valor en función de si está visible en la pantalla.                                                                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.   | Normalmente, un control de barra de título no tiene una etiqueta.                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada que corresponde al tipo de control TitleBar. El valor predeterminado es "barra de título" para en-US o inglés (Estados Unidos).                                                                  |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | ""           | Una barra de título no es contenido; su información textual se expone mediante el nombre de la ventana primaria.                                                                                                     |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

El tipo de control **TitleBar** no es necesario para admitir ningún patrón de control. Su funcionalidad se expone a través del [patrón de](uiauto-implementingwindow.md) control Ventana en el [tipo de](uiauto-supportwindowcontroltype.md) control Ventana.

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de la barra de título son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



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

 

 




