---
title: MenuItem (tipo de control)
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control MenuItem.
ms.assetid: a6a04489-8e28-44ff-a3b0-ecf19c24daab
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control MenuItem
- Automatización de la interfaz de usuario, tipo de control MenuItem
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control MenuItem
- Automatización de la interfaz de usuario,properties para el tipo de control MenuItem
- Automatización de la interfaz de usuario,patrones de control para el tipo de control MenuItem
- Automatización de la interfaz de usuario,events para el tipo de control MenuItem
- estructuras de árbol, tipo de control MenuItem
- properties,MenuItem , tipo de control
- patrones de control, tipo de control MenuItem
- events,MenuItem , tipo de control
- compatibilidad con el tipo de control MenuItem
- Tipo de control MenuItem
- tipos de control, estructura de árbol para el tipo de control MenuItem
- tipos de control, patrones de control para el tipo de control MenuItem
- tipos de control, compatibilidad con MenuItem
- tipos de control,MenuItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a48b94d7fc18cb9a8a6fe924fb73a250ab28708
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242312"
---
# <a name="menuitem-control-type"></a>MenuItem (tipo de control)

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **MenuItem.**

Un control de menú permite organizar jerárquicamente los elementos asociados a comandos y controladores de eventos. En una aplicación Windows, una barra de menús contiene varios elementos de menú (como Archivo **,** Editar y **Ventana)** y cada elemento de menú muestra un menú. Un menú contiene una colección de elementos de menú (como **Nuevo**, **Abierto** y **Cerrar**), que se puede expandir para mostrar elementos de menú adicionales o realizar una acción específica cuando se haga clic en ella.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **MenuItem.** Los Automatización de la interfaz de usuario se aplican a todos los controles de elementos de menú en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Problemas heredados](#legacy-issues)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de Automatización de la interfaz de usuario que pertenece a los controles de elementos de menú y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario árbol, vea [Información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>MenuItem "Ayuda"<ul><li>Menú (submenú del elemento de menú Ayuda)<ul><li>MenuItem "Temas de Ayuda"</li><li>MenuItem "Acerca del Bloc de notas"</li></ul></li></ul></li></ul> | <ul><li>MenuItem "Ayuda"<ul><li>MenuItem "Temas de Ayuda"</li><li>MenuItem "Acerca del Bloc de notas"</li></ul></li></ul> | 




 

La vista de control del control de elemento de menú tiene la Automatización de la interfaz de usuario estructura de árbol mostrada anteriormente. Tenga en cuenta que el elemento de menú **ayuda** de la barra de menús se ha agregado para ilustrar mejor la estructura.

Para la vista de contenido, **Menu** no está presente en el Automatización de la interfaz de usuario porque no transmite información significativa al usuario final.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **MenuItem.** Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value        | Notas                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol. Asigne la **propiedad AutomationId** para un elemento de menú si se sabe que el elemento es coherente en diferentes instancias de la interfaz de usuario. Si el elemento de menú se rellena dinámicamente y no es predecible, deje la **propiedad AutomationId** en blanco. |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic.                                                                                                                                                                     |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **MenuItem** |                                                                                                                                                                                                                                                                                                                                                                          |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true         | El control de elemento de menú siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                                                                                                  |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true         | El control de elemento de menú siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                                                                                                                                                                  |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada correspondiente al tipo de control **MenuItem.** El valor predeterminado es "elemento de menú" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                                  |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | El nombre del control de elemento de menú es el texto que se usa para etiquetar.                                                                                                                                                                                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con los controles de elementos de menú. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico | Notas                                                                                                                                                |
|-------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Si el control se puede expandir o contraer, implemente [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider).                            |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Depende | Si el control ejecuta una sola acción o comando, implemente [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider).                                     |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depende | Si el control se usa para seleccionar de una lista de opciones entre los elementos de menú, implemente [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider). |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depende | Si el control representa una opción que puede estar activada o desactivada, implemente [**IToggleProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                       |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de elementos de menú son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                                | Notas                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**UIA \_ Evento expandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) cambiado por la propiedad . | Si el control admite el patrón de control [ExpandCollapse,](uiauto-implementingexpandcollapse.md) debe admitir este evento. |
| [**Invoke \_ InvokedEventId de UIA \_**](uiauto-event-ids.md)                                                                                  | Si el control admite el patrón de control [Invoke,](uiauto-implementinginvoke.md) debe admitir este evento.                 |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.         |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento.       |
| [**Elemento \_ SelectionItem \_ de UIAAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento.   |
| [**Elemento \_ SelectionItem de \_ UIARemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento.   |
| [**Elementos \_ SelectionItem \_ de UIASelectedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)                                 | Si el control admite el patrón de control [Toggle,](uiauto-implementingtoggle.md) debe admitir este evento.                 |



 

## <a name="legacy-issues"></a>Problemas heredados

Para los elementos de menú de Microsoft Win32, el patrón de [control](uiauto-implementingtoggle.md) Alternar solo se admite cuando se activa un elemento de menú y es posible determinar mediante programación si se requiere compatibilidad con el patrón de control Alternar. Dado que un elemento de menú win32 no expone si se puede comprobar, se admite el patrón de control Invocar cuando el elemento de menú no está activado. El patrón de control Invoke siempre se admite, incluso para los elementos de menú que solo son necesarios para admitir el patrón de control Toggle. Esto es para que los clientes no se confundan cuando un elemento de menú que admite el patrón de [control](uiauto-implementinginvoke.md) Invoke (cuando el elemento de menú estaba desactivado) ya no admite ese patrón cuando se activa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




