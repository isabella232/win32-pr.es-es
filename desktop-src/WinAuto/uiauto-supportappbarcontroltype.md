---
title: AppBar (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control AppBar.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control AppBar
- Automatización de la interfaz de usuario, tipo de control AppBar
- Automatización de la interfaz de usuario, patrones de control para el tipo de control AppBar
- patrones de control, tipo de control AppBar
- compatibilidad con el tipo de control AppBar
- AppBar (tipo de control)
- tipos de control, AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151aecc0f5f97878e10b59b091c4c59ec98cb26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488091"
---
# <a name="appbar-control-type"></a>AppBar (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **AppBar** .

Una barra de aplicación es un elemento de la interfaz de usuario que presenta navegación, comandos y herramientas al usuario. En el caso de las aplicaciones de la tienda Windows, las barras de la aplicación para aplicaciones se pueden mostrar presionando tecla Windows + Z.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario necesaria, las propiedades, los patrones de control y los eventos para el tipo de control **AppBar** .

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Eventos necesarios](#required-events)
-   [Eventos relevantes](#relevant-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de **AppBar** y se describe lo que puede incluirse en cada vista. El **botón** es el elemento más común dentro de un control **AppBar** , pero también se pueden realizar otros controles que invoquen acciones para una aplicación. Un **AppBar** también puede tener 0 o más separadores (tipo de control de **separador** ), que aparecen en la vista de control tal y como se colocan entre los demás controles. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vista de control</th>
<th>Vista de contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>AppBar
<ul>
<li>Botón (0 o muchos)</li>
<li>Otros controles (0 o varios)</li>
</ul></li>
</ul></td>
<td><ul>
<li>No aplicable
<ul>
<li>Botón (0 o muchos)</li>
<li>Otros controles (0 o varios)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles que implementan el tipo de control **AppBar** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El valor que expone esta propiedad debe incluir todos los controles que se contienen dentro de ella.                                                                                                                                    |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **AppBar** |                                                                                                                                                                                                                             |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | false      | Un control de barra de la aplicación no se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Un control de barra de la aplicación siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas  | Si el control puede recibir el foco del teclado, debe admitir esta propiedad. Normalmente, los controles de la barra de la aplicación pueden tomar el foco del teclado.                                                                                    |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Vea las notas. | El valor de esta propiedad depende de si el control es visible en la pantalla.                                                                                                                                        |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null       | Normalmente, los controles de barra de la aplicación no tienen una etiqueta.                                                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **AppBar** . El valor predeterminado es "App bar" para en-US o inglés (Estados Unidos).                                                                                         |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El control de barra de la aplicación no necesita un nombre a menos que una aplicación tenga más de una barra de la aplicación. Si hay más de una barra de aplicación en una aplicación, use esta propiedad para exponer los nombres distintivos, como "Top" o "Bottom". |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de barra de la aplicación deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a>Eventos relevantes

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que son especialmente relevantes para los controles que implementan el tipo de control **AppBar** pero no son estrictamente necesarios.



| Evento de automatización de la interfaz de usuario                                                                                 | Notas                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                            | Las implementaciones de la plataforma pueden activar este evento cuando se cierra el control de la barra de la aplicación. |
| [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md)                            | Las implementaciones de la plataforma pueden activar este evento cuando se abre el control de barra de la aplicación. |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Controlador de eventos de cambio de propiedad.                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> <dt>

**Referencia**
</dt> <dt>

[**Control XAML de AppBar**](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

[**Objeto WinJS. UI. AppBar**](/previous-versions/windows/apps/br229670(v=win.10))
</dt> </dl>

 

 