---
title: Tipo de control Button
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Button.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Button
- Automatización de la interfaz de usuario,Tipo de control Button
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control Button
- Automatización de la interfaz de usuario,properties para el tipo de control Button
- Automatización de la interfaz de usuario,patrones de control para tipo de control Button
- Automatización de la interfaz de usuario,events para el tipo de control Button
- estructuras de árbol, tipo de control Button
- properties,Tipo de control Button
- patrones de control, tipo de control Button
- events,Tipo de control Button
- Compatibilidad con el tipo de control Button
- Button (tipo de control)
- tipos de control, estructura de árbol para tipo de control Button
- tipos de control, patrones de control para tipo de control Button
- tipos de control, compatibilidad con Button
- tipos de control,Button
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c080018e0fcaf8cd196204f80c61041d03fc1589
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478041"
---
# <a name="button-control-type"></a>Tipo de control Button

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo **de** control Button.

Un botón es un objeto con el que un usuario interactúa para realizar una acción, como por ejemplo los botones Aceptar y Cancelar de un cuadro de diálogo. El control de botón es un control simple de exponer porque se asigna a un único comando que el usuario quiere realizar.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo **de** control Button. Los Automatización de la interfaz de usuario se aplican a todos los controles de botón en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de botón y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Botón<ul><li>Imagen (0 o más)</li><li>Text (0 o más)</li></ul></li></ul> | <ul><li>Botón</li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles que implementan el tipo de control **Button** (como los controles de botón). Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor      | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcceleratorKeyPropertyId de UIA \_**](uiauto-automation-element-propids.md)             | Vea las notas. | Normalmente, un control de botón admite una tecla de aceleración para permitir que el usuario final realice rápidamente la acción representada por el botón desde el teclado.                                             |
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Botón** |                                                                                                                                                                                                      |
| [**HelpTextPropertyId de UIA \_**](uiauto-automation-element-propids.md)                         | Vea las notas. | El texto de ayuda debe indicar cuál será el resultado final de activar el botón. Suele ser el mismo tipo de información que se presenta a través de una información sobre herramientas.                                      |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | El control de botón siempre debe ser contenido.                                                                                                                                                           |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | El control de botón siempre debe ser un control .                                                                                                                                                         |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null       | Los controles de botón se etiquetan automáticamente con su contenido.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo **de** control Button. El valor predeterminado es "button" para en-US o inglés (Estados Unidos).                                                                   |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El nombre del control de botón es el texto que se usa para etiquetar. Cada vez que se usa una imagen para etiquetar un botón, se debe proporcionar texto alternativo para la propiedad **Name del** botón.                        |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de botón. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                  | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Vea las notas.    | Cuando un botón se hospeda como elemento secundario de un botón de división, el botón secundario puede admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) en lugar del patrón de control [Invoke](uiauto-implementinginvoke.md) o [Toggle.](uiauto-implementingtoggle.md) El patrón de control ExpandCollapse se puede usar para abrir o cerrar un menú u otra subes structure asociada al elemento de botón. |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Vea las notas.    | Todos los botones deben admitir [el patrón de](uiauto-implementinginvoke.md) control Invoke o el patrón de control [Toggle,](uiauto-implementingtoggle.md) pero no ambos. El patrón de control Invoke debe ser compatible cuando el botón realiza un comando a petición del usuario. Este comando se asigna a una única operación, como cortar, copiar, pegar o eliminar.                                                              |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Vea las notas.    | Todos los botones deben admitir [el patrón de](uiauto-implementinginvoke.md) control Invoke o el patrón de control [Toggle,](uiauto-implementingtoggle.md) pero no ambos. El patrón de control Toggle debe ser compatible si el botón puede recorrer una serie de hasta tres estados. Normalmente, se considera como un conmutador de encendido y apagado para características específicas.                                                                        |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que los controles de botón son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Invoke \_ InvokeEventId de UIA \_**](uiauto-event-ids.md)                                                     | Si el control admite el patrón de control [Invoke,](uiauto-implementinginvoke.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad NamePropertyId.**](uiauto-automation-element-propids.md)                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)    | Si el control admite el patrón de control [Toggle,](uiauto-implementingtoggle.md) debe admitir este evento.           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




