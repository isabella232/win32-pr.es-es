---
title: Tipo de control AppBar
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control AppBar.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control AppBar
- Automatización de la interfaz de usuario,tipo de control AppBar
- Automatización de la interfaz de usuario,patrones de control para el tipo de control AppBar
- patrones de control, tipo de control AppBar
- Compatibilidad con el tipo de control AppBar
- Tipo de control AppBar
- tipos de control, AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf562b125267e9b35239e8490f11ed6ae830
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472891"
---
# <a name="appbar-control-type"></a>Tipo de control AppBar

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **AppBar.**

Una barra de aplicación es un elemento de la interfaz de usuario que presenta al usuario navegación, comandos y herramientas. Para Windows store, las barras de aplicaciones de las aplicaciones se pueden mostrar presionando Windows Tecla + Z.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **AppBar.**

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Eventos necesarios](#required-events)
-   [Eventos relevantes](#relevant-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles **AppBar** y se describe lo que puede incluirse en cada vista. **Button** es el elemento más común dentro de **appBar,** pero también son posibles otros controles que invocan acciones para una aplicación. Una **barra de** aplicaciones también puede tener 0 o más separadores (tipo de control Separador), que aparecen en la vista de control tal como se colocan entre los demás controles. Para obtener más información sobre el árbol Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>AppBar<ul><li>Botón (0 o muchos)</li><li>Otros controles (0 o varios)</li></ul></li></ul> | <ul><li>No aplicable<ul><li>Botón (0 o muchos)</li><li>Otros controles (0 o varios)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles que implementan el tipo de control **AppBar.** Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor      | Notas                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El valor que expone esta propiedad debe incluir todos los controles que se contienen dentro de ella.                                                                                                                                    |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **AppBar** |                                                                                                                                                                                                                             |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | FALSE      | Un control de barra de aplicación no se incluye en la vista de contenido del Automatización de la interfaz de usuario aplicación.                                                                                                                                           |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | Un control de barra de aplicación siempre se incluye en la vista de control del Automatización de la interfaz de usuario aplicación.                                                                                                                                        |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas  | Si el control puede recibir el foco del teclado, debe admitir esta propiedad. Los controles dentro de la barra de la aplicación normalmente pueden tomar el foco del teclado.                                                                                    |
| [**IsOffscreenPropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | Vea las notas. | El valor de esta propiedad depende de si el control es visible en la pantalla.                                                                                                                                        |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null       | Normalmente, los controles de la barra de aplicaciones no tienen una etiqueta.                                                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo de control **AppBar.** El valor predeterminado es "app bar" para en-US o inglés (Estados Unidos).                                                                                         |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El control de barra de la aplicación no necesita un nombre a menos que una aplicación tenga más de una barra de aplicación. Si hay más de una barra de aplicación en una aplicación, use esta propiedad para exponer nombres distintivos, como "Top" o "Bottom". |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que los controles de la barra de aplicaciones son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a>Eventos relevantes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que son especialmente relevantes para los controles que implementan el tipo de control **AppBar,** pero que no son estrictamente obligatorios.



| Automatización de la interfaz de usuario evento                                                                                 | Notas                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                            | Las implementaciones de plataforma pueden desanimar este evento cuando se cierra el control de la barra de la aplicación. |
| [**Menú de \_ UIAOpenedEventId**](uiauto-event-ids.md)                            | Las implementaciones de plataforma pueden desanimar este evento cuando se abre el control de la barra de aplicaciones. |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Controlador de eventos con cambios de propiedad.                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> <dt>

**Referencia**
</dt> <dt>

[**Control XAML AppBar**](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

[**Objeto WinJS.UI.AppBar**](/previous-versions/windows/apps/br229670(v=win.10))
</dt> </dl>

 

 
