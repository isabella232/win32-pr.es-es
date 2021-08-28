---
title: Tipo de control SemanticZoom
description: En este tema se proporciona información Automatización de la interfaz de usuario compatibilidad con el tipo de control SemanticZoom.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control SemanticZoom
- Automatización de la interfaz de usuario, tipo de control SemanticZoom
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control SemanticZoom
- Automatización de la interfaz de usuario,properties para el tipo de control SemanticZoom
- Automatización de la interfaz de usuario,patrones de control para el tipo de control SemanticZoom
- Automatización de la interfaz de usuario,events para el tipo de control SemanticZoom
- estructuras de árbol, tipo de control SemanticZoom
- properties,SemanticZoom (tipo de control)
- patrones de control, tipo de control SemanticZoom
- events,SemanticZoom (tipo de control)
- compatibilidad con el tipo de control SemanticZoom
- Tipo de control SemanticZoom
- tipos de control, estructura de árbol para el tipo de control SemanticZoom
- tipos de control, patrones de control para el tipo de control SemanticZoom
- tipos de control, compatibilidad con SemanticZoom
- tipos de control, SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9673c5e9beb0c78ecc7dfccc10b6716d6d3afa3f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467762"
---
# <a name="semanticzoom-control-type"></a>Tipo de control SemanticZoom

En este tema se proporciona información Automatización de la interfaz de usuario compatibilidad con el tipo de control **SemanticZoom.**

Zoom semántico es una técnica introducida en Windows 8 para presentar y navegar por grandes conjuntos de datos relacionados o contenido dentro de una sola vista, como un álbum de fotos, una lista de aplicaciones o una libreta de direcciones. Zoom semántico usa dos modos distintos de clasificación, o niveles *de zoom,* para organizar y presentar el contenido. El modo de bajo nivel (o *acercado)* muestra elementos en una estructura plana "todo hacia arriba"; y el modo de alto nivel (o con zoom) muestra elementos en grupos, lo que permite al usuario navegar y examinar rápidamente el contenido. Por ejemplo, el zoom de una lista de ciudades podría cambiar a una lista de estados que contengan esas ciudades. El zoom de una lista de programas puede cambiar a una lista de grupos de programas lógicos.

Para obtener más información sobre el zoom semántico específicamente como se usa para Windows Store, vea [Directrices para el zoom semántico.](/windows/uwp/controls-and-patterns/semantic-zoom)

El modelo de uso para el tipo de control **SemanticZoom** es inusual, ya que existe principalmente para el acceso mediante programación. Los Automatización de la interfaz de usuario de Microsoft pueden supervisar y manipular el control Zoom semántico para controlar el estado de acercamiento de la lista. Los usuarios que no usan tecnología de asistencia normalmente manipularían el control zoom semántico directamente a través de gestos táctiles o métodos abreviados de teclado.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **SemanticZoom.** Los Automatización de la interfaz de usuario se aplican a todos los controles de zoom semántico en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Propiedades y patrones de control necesarios](#required-control-patterns-and-properties)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece al tipo de control **SemanticZoom** y se describe lo que se puede incluir en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, [vea información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>List<ul><li>[SemanticZoom]<ul><li>Elemento de lista (0 o más)</li></ul></li></ul></li></ul> | <ul><li>List<ul><li>Elemento de lista (0 o más)</li></ul></li></ul> | 




 

O:




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>[SemanticZoom]<ul><li>List<ul><li>Elemento de lista (0 o más)</li></ul></li></ul></li></ul> | <ul><li>List<ul><li>Elemento de lista (0 o más)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles que implementan el tipo de control **SemanticZoom.** Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).




| Propiedad de automatización de interfaz de usuario | Valor | Notas | 
|------------------------|-------|-------|
| <a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a> | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a> | Vea las notas. | El rectángulo exterior que contiene el control completo. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a> | Vea las notas. | Si el control de lista tiene un punto en el que se puede hacer clic (un punto en el que se puede hacer clic para que la lista tome el foco), ese punto debe exponerse a través de esta propiedad. Si el valor de la <a href="uiauto-automation-element-propids.md"><strong>propiedad UIA_IsOffscreenPropertyId</strong></a> es <strong>TRUE</strong>, al intentar recuperar esta propiedad se produce el <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> error. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a> | <strong>SemanticZoom</strong> | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a> | TRUE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a> | TRUE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a> | FALSE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a> | Vea las notas. | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a> | Vea las notas. | Cadena localizada correspondiente al tipo de control <strong>SemanticZoom.</strong> El valor predeterminado es "zoom semántico" para en-US o inglés (Estados Unidos).<blockquote>[!Note]<br />Algunos marcos lo concatenaron como "semanticzoom".</blockquote><br /> | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a> | Vea las notas. | Una cadena vacía es aceptable o se podría proporcionar un nombre más útil, siempre y cuando no contenga el término zoom semántico , lo que haría que la combinación de tipo de control y nombre resultara confusa. | 




 

## <a name="required-control-patterns-and-properties"></a>Propiedades y patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de zoom semántico. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                  | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Depende       | Los controles de zoom semántico [admiten el](uiauto-implementingtoggle.md) patrón de control Alternar para permitir que el zoom se habilite o deshabilite. [**ToggleState \_ Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponde al estado plano, all-up y [**ToggleState \_ On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponde a la vista de alto nivel alejada. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que los controles de zoom semántico son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)    |                                                                                                                            |



 

## <a name="remarks"></a>Comentarios

Si una interfaz de usuario tiene un botón visible para alternar el comportamiento del control de zoom semántico, este botón no debe tener un tipo de control **SemanticZoom.** Esto es intuitivo, pero el tipo de control **SemanticZoom** caracteriza el contenedor del contenido de zoom, no un botón que controla el zoom. (Este botón podría representarse simplemente como un tipo de control [Button](uiauto-supportbuttoncontroltype.md) con el patrón de control [Toggle).](uiauto-implementingtoggle.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

