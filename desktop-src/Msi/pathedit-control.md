---
description: El control PathEdit muestra un campo de edición que permite al usuario seleccionar la sección final de un trazado.
ms.assetid: 074ef4d5-3ac1-4bdb-90c5-9798d89a749f
title: Control PathEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65d1237199f202e6c674ab4526ccd4747b02c09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276841"
---
# <a name="pathedit-control"></a>Control PathEdit

El control PathEdit muestra un campo de edición que permite al usuario seleccionar la sección final de un trazado. Este control permite escribir el nombre de carpeta seleccionado o la ruta de acceso completa en el campo de edición. Un usuario también puede especificar una ruta de acceso UNC (Convención de nomenclatura universal) para una unidad que no tenga ninguna letra de unidad. Si el usuario escribe un segmento final para la ruta de acceso que no es válida para el volumen actual, el control PathEdit no puede transferir el foco al siguiente control.

Los controles PathEdit control, [DirectoryCombo](directorycombo-control.md)y [DirectoryList](directorylist-control.md) están asociados a la misma propiedad de valor de cadena. Esa propiedad es la ruta de acceso seleccionada por el usuario. Escriba el nombre de la propiedad en la columna de propiedades de la [tabla de control](control-table.md). Esta propiedad debe tener un valor inicial que contenga al menos un volumen y un subnivel. Especifique el valor inicial de la propiedad en la columna valor de la [tabla de propiedades](property-table.md).

Este control está pensado para usarse en un [cuadro de diálogo de exploración](browse-dialog.md) junto con los controles PathEdit y [DirectoryList](directorylist-control.md) .

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con este control. Para cambiar el valor de un atributo mediante un evento, suscríbase el control a ControlEvent, en la [tabla EventMapping](eventmapping-table.md) y enumere el identificador del atributo en la columna de atributos. Escriba el identificador de ControlEvent, en la columna evento.



| Identificador de atributo                                               | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Es el nombre de una propiedad indirecta asociada al control. Si se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Si se establece el bit de atributo indirecto, este nombre también es el valor de la propiedad que aparece en la columna de propiedades de la [tabla de control](control-table.md).                                                                                                                                                                              |
| [Position](position-control-attribute.md)                         |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas de la esquina izquierda del control en las columnas width, height, X e Y de la tabla de [control](control-table.md). Use [unidades de instalador](installer-units.md) para longitud y distancia.<br/>                                                                                                                                                                                                                                   |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Es el nombre de la propiedad asociada a este control. Si no se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Este atributo se especifica en la columna de propiedades de la [tabla de control](control-table.md).                                                                                                                                                                                                                                              |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor actual de la propiedad mostrada o modificada por este control. Si no se establece el bit de atributo indirecto, este es el valor de PropertyName. Si se establece el bit de atributo indirecto, este es el valor de IndirectPropertyName. Si cambia el atributo, el control refleja el nuevo valor.                                                                                                                                                                                                                                 |
| [Texto](text-control-attribute.md)                                 |                                  | Para establecer la fuente y el estilo de fuente de una cadena de texto, anteponga a la cadena de caracteres mostrados el prefijo { \\ style} o {&Style}. Donde Style es un identificador que aparece en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la propiedad [**DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente. Para especificar el número de caracteres que el usuario puede escribir, anexe {n} después de cualquier especificación de fuente, donde n es un entero positivo.<br/> |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Attributes de la [tabla de control](control-table.md) para que el control sea visible u oculto en el momento de su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                           |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Control en estado deshabilitado. Control en un estado habilitado.<br/> Incluya este bit en la palabra de bit de la columna Attributes del [control](control-table.md) para habilitar el control al crearlo.<br/> También puede habilitar o deshabilitar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto hundido, 3D.<br/> Incluya estos bits en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                  |
| [Indirecto](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | El control muestra o cambia el valor de la propiedad en la columna de propiedades de la [tabla de control](control-table.md). El control muestra o cambia el valor de la propiedad que tiene el identificador que aparece en la columna de propiedades de la tabla de control.<br/> Determina si se hace referencia indirectamente a la propiedad asociada a este control.<br/>                                                                                                                                                       |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | El texto del control se muestra en orden de lectura de izquierda a derecha. El texto del control se muestra en orden de lectura de derecha a izquierda.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | El texto del control se alinea a la izquierda. El texto del control está alineado a la derecha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Observaciones

El control PathEdit se deriva del control de [edición](edit-control.md) .

Por compatibilidad con los lectores de pantalla, al crear un cuadro de diálogo con un control PathEdit como primer control activo, debe hacer que el campo de texto pertenezca al campo de edición del primer control activo en la [tabla del cuadro de diálogo](dialog-table.md). Puesto que el texto estático no puede recibir el foco, cuando se crea el cuadro de diálogo, el campo de edición tendrá el foco inicialmente según lo previsto. Esto garantiza que los lectores de pantalla muestren la información correcta.

 

 




