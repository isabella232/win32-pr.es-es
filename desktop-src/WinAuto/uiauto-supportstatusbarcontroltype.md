---
title: Tipo de control StatusBar
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control StatusBar.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control StatusBar
- Automatización de la interfaz de usuario, tipo de control StatusBar
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control StatusBar
- Automatización de la interfaz de usuario,properties para el tipo de control StatusBar
- Automatización de la interfaz de usuario,patrones de control para el tipo de control StatusBar
- Automatización de la interfaz de usuario,events para el tipo de control StatusBar
- estructuras de árbol, tipo de control StatusBar
- properties,Tipo de control StatusBar
- patrones de control, tipo de control StatusBar
- events,Tipo de control StatusBar
- Compatibilidad con el tipo de control StatusBar
- StatusBar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control StatusBar
- tipos de control, patrones de control para el tipo de control StatusBar
- tipos de control, compatibilidad con StatusBar
- tipos de control, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f52f3f04db86a8c8ff0e9cad9a3938a17e996e8210960912c3abc5039468e178
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614255"
---
# <a name="statusbar-control-type"></a>Tipo de control StatusBar

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **StatusBar.**

Un control de barra de estado muestra información sobre un objeto que se ve en una ventana de una aplicación, el componente del objeto o información contextual relativa a esa operación del objeto en la aplicación.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **StatusBar.** Los Automatización de la interfaz de usuario se aplican a todos los controles de barra de estado en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de barra de estado y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario árbol, [vea información general Automatización de la interfaz de usuario árbol de árbol de datos.](uiauto-treeoverview.md)



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
<li>StatusBar
<ul>
<li>Edición (0 o más)</li>
<li>ProgressBar (0 o muchos)</li>
<li>Imagen (0 o muchos)</li>
<li>Botón (0 o muchos)</li>
</ul></li>
</ul></td>
<td><ul>
<li>StatusBar
<ul>
<li>Edición (0 o más)</li>
<li>ProgressBar (0 o muchos)</li>
<li>Imagen (0 o muchos)</li>
<li>Botón (0 o muchos)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de la barra de estado. Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value         | Notas                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.    | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.    | El rectángulo delimitador de una barra de estado debe abarcar todos los controles que incluye.                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.    | Se admite si hay un rectángulo delimitador. Si hay áreas dentro del rectángulo delimitador que no se pueden hacer clic y el elemento realiza pruebas de acceso especializadas, invalide esta opción y proporcione un punto en el que se pueda hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **StatusBar** |                                                                                                                                                                                                                     |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE          | El control de barra de estado siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario estado.                                                                                                                            |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE          | El control de barra de estado siempre se incluye en la vista de control del Automatización de la interfaz de usuario estado.                                                                                                                            |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Depende       | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                           |
| [**IsOffscreenPropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | Depende       | Si un control de barra de estado no está visible actualmente, devolverá TRUE para esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | Normalmente, el control de barra de estado no tiene una etiqueta.                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.    | Cadena localizada correspondiente al tipo de control **StatusBar.** El valor predeterminado es "barra de estado" para en-US o inglés (Estados Unidos).                                                                           |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.    | El control de barra de estado no necesita un nombre a menos que se use más de uno dentro de una aplicación. En este caso, distinga cada barra con nombres como "Estado de Internet" o "Estado de la aplicación".                    |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Depende       | Valor que indica la orientación del control: horizontal o vertical.                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control necesarios para ser compatibles con los controles de barra de estado. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                               | Soporte técnico  | Notas                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | Opcionales | Los controles de barra de estado deben admitir [el patrón de](uiauto-implementinggrid.md) control Grid para que se puedan supervisar partes individuales y hacer referencia a estas fácilmente para obtener información. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que los controles de la barra de estado son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                   |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                   |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la **propiedad IsEnabled,** debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la **propiedad IsOffscreen,** debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a>Comentarios

Se recomienda usar controles de edición como elementos de cuadrícula secundarios en una barra de estado. El uso de controles de edición facilita la asociación del propósito del campo de estado con su valor mediante el uso de la propiedad de nombre y valor del elemento. Dado que los controles de texto no deben admitir el **patrón de** control Valor, no deben usarse como elementos de cuadrícula secundarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




