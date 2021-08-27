---
description: Un control DirectoryList muestra una parte de la ruta de acceso que se muestra actualmente en el control PathEdit. El control DirectoryList muestra las carpetas debajo del directorio mostrado actualmente por el control DirectoryCombo.
ms.assetid: 05e70381-28c0-4568-808e-ff2dee8ff790
title: DirectoryList Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce0cf409f4ca7335bd032f1fc63831db88ace14424ef7a73cd3853c9ff3e2de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086195"
---
# <a name="directorylist-control"></a>DirectoryList Control

Un control DirectoryList muestra una parte de la ruta de acceso que se muestra actualmente en el [control PathEdit](pathedit-control.md). El control DirectoryList muestra las carpetas debajo del directorio mostrado actualmente por el [control DirectoryCombo](directorycombo-control.md).

Los controles PathEdit, DirectoryCombo y DirectoryList están asociados a la misma propiedad con valores de cadena. Esa propiedad es la ruta de acceso seleccionada por el usuario. Escriba el nombre de la propiedad en la columna Propiedad de la [tabla Control](control-table.md). Esta propiedad debe tener un valor inicial que contenga al menos un volumen y un subnivel. Especifique el valor inicial de la propiedad en la columna Valor de la [tabla Property](property-table.md).

Este control está pensado para usarse en un cuadro de [diálogo Examinar](browse-dialog.md) junto con los controles [PathEdit](pathedit-control.md) y DirectoryList.

El control DirectoryList publica los siguientes controles ControlEvents.



| ControlEvent                                            | Descripción                                                       |
|---------------------------------------------------------|-------------------------------------------------------------------|
| [DirectoryListNew](directorylistnew-controlevent.md)   | Crea una nueva carpeta y selecciona el campo de nombre para editarlo.      |
| [IgnoreChange](ignorechange-controlevent.md)           | Resalta, pero no abre, una carpeta en el directorio actual. |
| [DirectoryListUp](directorylistup-controlevent.md)     | Selecciona el elemento primario del directorio actual.                      |
| [DirectoryListOpen](directorylistopen-controlevent.md) | Selecciona y resalta un directorio.                               |



 

El control DirectoryList nunca muestra el contenido del campo Texto de la [tabla](control-table.md) Control. En su lugar, este campo especifica el estilo de texto que va a mostrar el control y contiene una descripción del control utilizado por las utilidades de revisión de pantalla. Para establecer la fuente y el estilo de fuente de una cadena de texto, antefirima la cadena de caracteres mostrados con { style} o \\ {&*style*}. Donde style es un identificador enumerado en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la [**propiedad DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente. Las utilidades de revisión de pantalla leen la información siguiente como la descripción del control. Consulte [Accesibilidad.](accessibility.md)

## <a name="control-attributes"></a>Atributos de control

Puede usar los atributos siguientes con este control. Para cambiar el valor de un atributo mediante un evento, suscribe el control a un control ControlEvent en la [tabla EventMapping](eventmapping-table.md) y enumera el identificador del atributo en la columna Atributo . Escriba el identificador de ControlEvent en la columna Evento.



| Identificador de atributo                                               | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Este es el nombre de una propiedad indirecta asociada al control . Si se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Si se establece el bit de atributo indirecto, este nombre también es el valor de la propiedad enumerada en la columna Propiedad de la [tabla Control](control-table.md).                        |
| [Position](position-control-attribute.md)                         |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas de la esquina izquierda del control en las columnas Width, Height, X e Y de la [tabla Control](control-table.md). Use [las unidades del](installer-units.md) instalador para la longitud y la distancia.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Este es el nombre de la propiedad asociada a este control. Si no se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Este atributo se especifica en la columna Property de la [tabla Control](control-table.md).                                                                                        |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor actual de la propiedad mostrada o modificada por este control. Si no se establece el bit de atributo indirecto, este es el valor de PropertyName. Si se establece el bit de atributo indirecto, este es el valor de IndirectPropertyName. Si el atributo cambia, el control refleja el nuevo valor.                                                                           |
| [Texto](text-control-attribute.md)                                 |                                  | Para mostrar texto en lectores de pantalla, escriba el texto en la columna Texto de la [tabla Control](control-table.md). Consulte [Accesibilidad.](accessibility.md)                                                                                                                                                                                                                 |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Atributos de la [tabla Control](control-table.md)para que el control sea visible u oculto tras su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                     |
| [Habilitado](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Control en estado deshabilitado. Control en un estado habilitado.<br/> Incluya este bit en la palabra de bits en la columna Atributos del [control para](control-table.md) habilitar el control en la creación.<br/> También puede habilitar o deshabilitar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto 3D y bloqueado.<br/> Incluya estos bits en la palabra de bits en la columna Atributos de la [tabla Control](control-table.md).<br/>                                                                                                                                                             |
| [Indirecto](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | El control muestra o cambia el valor de la propiedad en la columna Propiedad de la [tabla Control](control-table.md). El control muestra o cambia el valor de la propiedad que tiene el identificador enumerado en la columna Propiedad de la tabla Control.<br/> Determina si se hace referencia indirectamente a la propiedad asociada a este control.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | El texto del control se muestra en orden de lectura de izquierda a derecha. El texto del control se muestra en orden de lectura de derecha a izquierda.<br/>                                                                                                                                                                                                                              |
| [Alineado a la derecha](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | El texto del control se alinea a la izquierda. El texto del control se alinea a la derecha.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | La barra de desplazamiento se encuentra en el lado derecho del control. La barra de desplazamiento se encuentra en el lado izquierdo del control.<br/>                                                                                                                                                                                                                                         |
| [BiDi Control](bidi-control-attribute.md)                         | 0x000000E0                       | Establezca este valor para una combinación de los atributos [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)y [LeftScroll.](leftscroll-control-attribute.md)                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentarios

Este control se puede crear desde la clase \_ WC LISTVIEW mediante la [**función CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Tiene los estilos **LVS \_ LIST**, **LVS \_ EDITLABELS,** **WS \_ VSCROLL,** **LVS \_ SHAREIMAGELISTS**, **LVS \_ AUTOARRANGE**, **LVS \_ SINGLESEL,** **WS \_ BORDER**, **LVS \_ SORTASCENDING,** **WS \_ CHILD,** **WS \_ GROUP** y **WS \_ TABSTOP.**

Este control permite al usuario seleccionar una subcarpeta de la selección actual. Con botones adicionales, también permite al usuario seleccionar una nueva carpeta en la selección actual o subir un nivel de la ruta de acceso. Si el usuario  elige el botón Crear nueva carpeta en una carpeta donde ya existe una nueva carpeta, no se crea una segunda carpeta y se selecciona el nombre de la nueva carpeta existente para su edición.

 

