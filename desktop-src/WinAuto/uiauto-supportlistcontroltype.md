---
title: Tipo de control List
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control List.
ms.assetid: e4cde080-32d1-4150-a6be-8bd750e972c9
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control List
- Automatización de la interfaz de usuario,Tipo de control List
- Automatización de la interfaz de usuario,tree structure for List control type
- Automatización de la interfaz de usuario,properties para tipo de control List
- Automatización de la interfaz de usuario,patrones de control para tipo de control List
- Automatización de la interfaz de usuario,events para el tipo de control List
- tree structures,List (Tipo de control)
- properties,List , tipo de control
- patrones de control, Tipo de control List
- events,List ,tipo de control
- Compatibilidad con el tipo de control List
- List (tipo de control)
- tipos de control, estructura de árbol para tipo de control List
- tipos de control, patrones de control para tipo de control List
- tipos de control, compatibilidad con List
- tipos de control, Lista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08b052811e2ebf61214ce8b146740943f4e3d14
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471181"
---
# <a name="list-control-type"></a>Tipo de control List

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo **de** control List.

El **tipo** de control Lista proporciona una manera de organizar un grupo plano o grupos de elementos y permite a un usuario seleccionar uno o varios de esos elementos. El **tipo** de control List tiene una restricción flexible sobre los tipos de elementos secundarios que puede contener. Esto permite que los proveedores de Automatización de la interfaz de usuario admitan un elemento conocido para los contenedores de selección.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, las propiedades, los patrones de control y los eventos necesarios para el tipo **de** control List. Los Automatización de la interfaz de usuario se aplican a todos los controles de lista en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Propiedades y patrones de control necesarios](#required-control-patterns-and-properties)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de lista y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| Contiene los elementos que corresponden a los controles. | Quita la información redundante del árbol para que las tecnologías de asistencia funcionen con el conjunto más pequeño de información que sea significativa para el usuario final. | 
| <ul><li>List<ul><li>DataItem (0 o más)</li><li>Elemento de lista (0 o más)</li><li>Group (0 o más)</li><li>ScrollBar (0, 1 o 2)</li></ul></li></ul> | <ul><li>List<ul><li>DataItem (0 o más)</li><li>Elemento de lista (0 o más)</li><li>Group (0 o más)</li></ul></li></ul> | 




 

La vista de control de un control que implementa el tipo de control List (por ejemplo, un control de lista) consta de:

-   Cero o más elementos dentro del control de lista (los elementos se pueden basar en los tipos de control [ListItem](uiauto-supportlistitemcontroltype.md) [o DataItem)](uiauto-supportdataitemcontroltype.md)
-   Cero o más controles de grupo dentro de un control de lista
-   Cero, uno o dos controles de barra de desplazamiento

La vista de contenido de un control que implementa el tipo de control List (por ejemplo, un control de lista) consta de:

-   Cero o más elementos dentro del control de lista (los elementos se pueden basar en los tipos de control [ListItem](uiauto-supportlistitemcontroltype.md) [o DataItem)](uiauto-supportdataitemcontroltype.md)
-   Cero o más grupos dentro del control de lista

Un control de lista no debe disponer de elementos que tengan una relación jerárquica que no sea estar agrupados. Si los elementos tienen elementos secundarios en el Automatización de la interfaz de usuario, el contenedor de lista debe basarse en el tipo [de](uiauto-supporttreecontroltype.md) control Tree.

Los elementos seleccionables dentro del control de lista estarán disponibles en los descendientes del Automatización de la interfaz de usuario del control de lista. Todos los elementos dentro del control de lista deben pertenecer al mismo grupo de selección. Los elementos seleccionables de la lista deben exponerse como tipos de control [ListItem](uiauto-supportlistitemcontroltype.md) (en lugar [de DataItem).](uiauto-supportdataitemcontroltype.md)

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el **tipo de** control List. Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor      | Notas                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Si el control de lista tiene un punto en el que se puede hacer clic (un punto en el que se puede hacer clic para hacer que la lista tome el foco), ese punto debe exponerse a través de esta propiedad. Si el valor de la propiedad [**\_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md) de UIA es **TRUE,** al intentar recuperar esta propiedad se produce el error [**UIA \_ E \_ NOCLICKABLEPOINT.**](uiauto-error-codes.md)                      |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Lista**   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**HelpTextPropertyId de UIA \_**](uiauto-automation-element-propids.md)                         | Vea las notas. | El texto de ayuda para los controles de lista debe explicar por qué se solicita al usuario que realice una selección de una lista de opciones. Por ejemplo, "Seleccione un elemento de esta lista para establecer la resolución de pantalla del monitor".                                                                                                                                                                                                                                                |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**   | El control de lista siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario lista.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**   | El control de lista siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo **de** control List. El valor predeterminado es "list" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                                                                                                                                       |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El valor de la propiedad **Name** de un control de lista debe transmitir la categoría de opciones entre las que se pide al usuario que seleccione. Esta propiedad suele recibir su nombre de una etiqueta de texto estático. Si no hay una etiqueta de texto estático, el desarrollador de la aplicación debe exponer un valor para la **propiedad Name.**<br/> La única vez que esta propiedad no es necesaria para los controles de lista es si el control se utiliza dentro del subárbol de otro control.<br/> |



 

## <a name="required-control-patterns-and-properties"></a>Propiedades y patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control necesarios para que todos los controles de lista sean compatibles. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                             | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)                                | Depende       | Implemente el [patrón de](uiauto-implementinggrid.md) control Grid cuando la navegación de cuadrícula deba estar disponible en un elemento por elemento.                                                                                                                                                                                                                                           |
| [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)                | Depende       | Implemente el patrón de control [MultipleView](uiauto-implementingmultipleview.md) si el control puede admitir varias vistas de los elementos del contenedor.                                                                                                                                                                                                                       |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depende       | Implemente el [patrón de](uiauto-implementingscroll.md) control Scroll si los elementos del contenedor se pueden desplazar.                                                                                                                                                                                                                                                                  |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Depende       | Si un control admite el tipo de control List que admite la selección, el control debe implementar el patrón de control [Selection](uiauto-implementingselection.md) cuando se mantiene un estado de selección entre los elementos contenidos en el control . Si los elementos del control no se pueden seleccionar, se [puede](uiauto-supportgroupcontroltype.md) usar el tipo de control Grupo. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Depende       | Los controles List pueden ser contenedores de selección única o múltiple.                                                                                                                                                                                                                                                                                                                    |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Depende       | Los controles List no siempre requieren que se seleccione un elemento.                                                                                                                                                                                                                                                                                                                    |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)                              | Nunca         | El [patrón de](uiauto-implementingtable.md) control Table nunca se admite para el tipo **de** control List. Si el control necesita admitir este patrón de control, el control debe basarse en el tipo de control [DataGrid.](uiauto-supportdatagridcontroltype.md)                                                                                                             |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos Automatización de la interfaz de usuario que los controles de lista son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                        | Notas                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                           |                                                                                                                              |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                              |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.     |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     | Si se puede cambiar el diseño de los elementos secundarios, el control debe admitir este evento.                                            |
| [**UIA \_ Evento de cambio de propiedad MultipleViewCurrentViewPropertyId.**](uiauto-control-pattern-propids.md)             | Si el control admite el patrón de control [MultipleView,](uiauto-implementingmultipleview.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.             |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.             |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.             |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.             |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.             |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.             |
| [**UIA \_ Selection \_ InvalidtedEventId**](uiauto-event-ids.md)                                                            | Si el control admite el patrón de control [Selection,](uiauto-implementingselection.md) debe admitir este evento.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 





