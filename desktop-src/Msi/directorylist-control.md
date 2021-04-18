---
description: Un control DirectoryList muestra una parte de la ruta de acceso que se muestra actualmente en el control PathEdit. El control DirectoryList muestra las carpetas situadas debajo del directorio mostrado actualmente por el control DirectoryCombo.
ms.assetid: 05e70381-28c0-4568-808e-ff2dee8ff790
title: Control DirectoryList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6a1e48a25ae057c836c7b815dae18e7dcf5c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667794"
---
# <a name="directorylist-control"></a>Control DirectoryList

Un control DirectoryList muestra una parte de la ruta de acceso que se muestra actualmente en el [control PathEdit](pathedit-control.md). El control DirectoryList muestra las carpetas situadas debajo del directorio mostrado actualmente por el [control DirectoryCombo](directorycombo-control.md).

Los controles PathEdit, DirectoryCombo y DirectoryList están asociados a la misma propiedad de valor de cadena. Esa propiedad es la ruta de acceso seleccionada por el usuario. Escriba el nombre de la propiedad en la columna de propiedades de la [tabla de control](control-table.md). Esta propiedad debe tener un valor inicial que contenga al menos un volumen y un subnivel. Especifique el valor inicial de la propiedad en la columna valor de la [tabla de propiedades](property-table.md).

Este control está pensado para usarse en un [cuadro de diálogo de exploración](browse-dialog.md) junto con el control [PathEdit](pathedit-control.md) y DirectoryList.

El control DirectoryList publica los siguientes ControlEvents.



| ControlEvent                                            | Descripción                                                       |
|---------------------------------------------------------|-------------------------------------------------------------------|
| [DirectoryListNew](directorylistnew-controlevent.md)   | Crea una carpeta nueva y selecciona el campo de nombre para su edición.      |
| [IgnoreChange](ignorechange-controlevent.md)           | Destaca, pero no abre, una carpeta en el directorio actual. |
| [DirectoryListUp](directorylistup-controlevent.md)     | Selecciona el elemento primario del directorio actual.                      |
| [DirectoryListOpen](directorylistopen-controlevent.md) | Selecciona y resalta un directorio.                               |



 

El control DirectoryList nunca muestra el contenido del campo de texto de la [tabla de control](control-table.md) . En su lugar, este campo especifica el estilo de texto que va a mostrar el control y contiene una descripción del control utilizado por las utilidades de revisión de pantalla. Para establecer la fuente y el estilo de fuente de una cadena de texto, anteponga a la cadena de caracteres mostrados el prefijo { \\ style} o {&*Style*}. Donde Style es un identificador que aparece en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la propiedad [**DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente. La información que aparece a continuación se lee mediante las utilidades de revisión de pantalla como Descripción del control. Vea [accesibilidad](accessibility.md).

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con este control. Para cambiar el valor de un atributo mediante un evento, suscríbase el control a ControlEvent, en la [tabla EventMapping](eventmapping-table.md) y enumere el identificador del atributo en la columna de atributos. Escriba el identificador de ControlEvent, en la columna evento.



| Identificador de atributo                                               | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Es el nombre de una propiedad indirecta asociada al control. Si se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Si se establece el bit de atributo indirecto, este nombre también es el valor de la propiedad que aparece en la columna de propiedades de la [tabla de control](control-table.md).                        |
| [Position](position-control-attribute.md)                         |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas de la esquina izquierda del control en las columnas width, height, X e Y de la tabla de [control](control-table.md). Use [unidades de instalador](installer-units.md) para longitud y distancia.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Es el nombre de la propiedad asociada a este control. Si no se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Este atributo se especifica en la columna de propiedades de la [tabla de control](control-table.md).                                                                                        |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor actual de la propiedad mostrada o modificada por este control. Si no se establece el bit de atributo indirecto, este es el valor de PropertyName. Si se establece el bit de atributo indirecto, este es el valor de IndirectPropertyName. Si cambia el atributo, el control refleja el nuevo valor.                                                                           |
| [Texto](text-control-attribute.md)                                 |                                  | Para mostrar texto en lectores de pantalla, escriba el texto en la columna texto de la [tabla de control](control-table.md). Vea [accesibilidad](accessibility.md).                                                                                                                                                                                                                 |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Attributes de la [tabla de control](control-table.md). para hacer que el control esté visible u oculto durante su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                     |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Control en estado deshabilitado. Control en un estado habilitado.<br/> Incluya este bit en la palabra de bit de la columna Attributes del [control](control-table.md) para habilitar el control al crearlo.<br/> También puede habilitar o deshabilitar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto hundido, 3D.<br/> Incluya estos bits en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md).<br/>                                                                                                                                                             |
| [Indirecto](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | El control muestra o cambia el valor de la propiedad en la columna de propiedades de la [tabla de control](control-table.md). El control muestra o cambia el valor de la propiedad que tiene el identificador que aparece en la columna de propiedades de la tabla de control.<br/> Determina si se hace referencia indirectamente a la propiedad asociada a este control.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | El texto del control se muestra en orden de lectura de izquierda a derecha. El texto del control se muestra en orden de lectura de derecha a izquierda.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | El texto del control se alinea a la izquierda. El texto del control está alineado a la derecha.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | La barra de desplazamiento se encuentra en el lado derecho del control. La barra de desplazamiento se encuentra en el lado izquierdo del control.<br/>                                                                                                                                                                                                                                         |
| [Control BiDi](bidi-control-attribute.md)                         | 0x000000E0                       | Establezca este valor para una combinación de los atributos [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)y [LeftScroll](leftscroll-control-attribute.md) .                                                                                                                                                                          |



 

## <a name="remarks"></a>Observaciones

Este control se puede crear a partir de la clase WC de CT mediante \_ la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Tiene los estilos **\_ List LVS**, **LVS \_ EDITLABELS**, **WS \_ VSCROLL**, **LVS \_ SHAREIMAGELISTS**, **LVS \_ AutoArrange**, **LVS \_ SINGLESEL**, **WS \_ Border**, **LVS \_ SORTASCENDING**, **WS \_ Child**, **WS \_ Group** y **WS \_ TABSTOP** .

Este control permite al usuario seleccionar una subcarpeta de la selección actual. Con botones adicionales también permite al usuario seleccionar una nueva carpeta en la selección actual o subir un nivel en la ruta de acceso. Si el usuario elige el botón **crear nueva carpeta** en una carpeta en la que ya existe una nueva carpeta, no se creará una segunda carpeta nueva y se seleccionará el nombre de la nueva carpeta existente para su edición.

 

