---
description: El control PathEdit muestra un campo de edición que permite a un usuario seleccionar la sección final de una ruta de acceso.
ms.assetid: 074ef4d5-3ac1-4bdb-90c5-9798d89a749f
title: PathEdit (Control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed7655cc893c30f417c9a7ef374eb6d4ade10dfd618ca328e1be2fc7a0e0a9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377618"
---
# <a name="pathedit-control"></a>PathEdit (Control)

El control PathEdit muestra un campo de edición que permite a un usuario seleccionar la sección final de una ruta de acceso. Este control permite escribir el nombre de la carpeta seleccionada o la ruta de acceso completa en el campo de edición. Un usuario también puede escribir una ruta de acceso de convención de nomenclatura universal (UNC) a una unidad que no tenga ninguna letra de unidad. Si el usuario escribe un segmento final para la ruta de acceso que no es válida para el volumen actual, el control PathEdit no puede transferir el foco al control siguiente.

Los controles PathEdit, [DirectoryCombo](directorycombo-control.md)y [DirectoryList](directorylist-control.md) están asociados a la misma propiedad con valores de cadena. Esa propiedad es la ruta de acceso seleccionada por el usuario. Escriba el nombre de la propiedad en la columna Propiedad de la [tabla Control](control-table.md). Esta propiedad debe tener un valor inicial que contenga al menos un volumen y un subnivel. Especifique el valor inicial de la propiedad en la columna Valor de la [tabla Property](property-table.md).

Este control está pensado para usarse en un cuadro de [diálogo Examinar](browse-dialog.md) junto con los controles PathEdit y [DirectoryList.](directorylist-control.md)

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con este control. Para cambiar el valor de un atributo mediante un evento, suscriba el control a un control ControlEvent en la [tabla EventMapping](eventmapping-table.md) y enumézcalo en la columna Attribute . Escriba el identificador de ControlEvent en la columna Evento.



| Identificador de atributo                                               | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Este es el nombre de una propiedad indirecta asociada al control . Si se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Si se establece el bit de atributo indirecto, este nombre también es el valor de la propiedad enumerada en la columna Propiedad de la [tabla Control](control-table.md).                                                                                                                                                                              |
| [Position](position-control-attribute.md)                         |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas del control de la esquina izquierda del control en las columnas Ancho, Alto, X e Y de la [tabla Control](control-table.md). Use [las unidades del](installer-units.md) instalador para la longitud y la distancia.<br/>                                                                                                                                                                                                                                   |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Este es el nombre de la propiedad asociada a este control. Si no se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Este atributo se especifica en la columna Property de la [tabla Control](control-table.md).                                                                                                                                                                                                                                              |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor actual de la propiedad mostrada o modificada por este control. Si no se establece el bit de atributo indirecto, este es el valor de PropertyName. Si se establece el bit de atributo indirecto, este es el valor de IndirectPropertyName. Si el atributo cambia, el control refleja el nuevo valor.                                                                                                                                                                                                                                 |
| [Texto](text-control-attribute.md)                                 |                                  | Para establecer la fuente y el estilo de fuente de una cadena de texto, antefise la cadena de caracteres mostrados con { style} o \\ {&style}. Donde style es un identificador enumerado en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la [**propiedad DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente. Para especificar el número de caracteres que el usuario puede escribir, anexe {n} después de cualquier especificaciones de fuente, donde n es un entero positivo.<br/> |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Atributos de la [tabla Control](control-table.md) para que el control sea visible u oculto tras su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                           |
| [Habilitado](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Control en estado deshabilitado. Control en un estado habilitado.<br/> Incluya este bit en la palabra bit en la columna Atributos del [control para](control-table.md) habilitar el control durante la creación.<br/> También puede habilitar o deshabilitar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto 3D desconsolado.<br/> Incluya estos bits en la palabra de bits en la columna Atributos de la [tabla Control](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                  |
| [Indirecto](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | El control muestra o cambia el valor de la propiedad en la columna Propiedad de la [tabla Control](control-table.md). El control muestra o cambia el valor de la propiedad que tiene el identificador enumerado en la columna Propiedad de la tabla Control .<br/> Determina si se hace referencia indirectamente a la propiedad asociada a este control.<br/>                                                                                                                                                       |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | El texto del control se muestra en orden de lectura de izquierda a derecha. El texto del control se muestra en orden de lectura de derecha a izquierda.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [Alineado a la derecha](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | El texto del control se alinea a la izquierda. El texto del control se alinea a la derecha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Comentarios

El control PathEdit se deriva del control [Edit.](edit-control.md)

Por compatibilidad con lectores de pantalla, al crear un cuadro de diálogo con un control PathEdit como primer control activo, debe convertir el campo de texto que pertenece al campo de edición en el primer control activo de la tabla [Dialog](dialog-table.md). Puesto que el texto estático no puede tomar el foco, cuando se crea el cuadro de diálogo, el campo de edición tendrá el foco inicialmente según lo previsto; esto garantiza que los lectores de pantalla muestren la información correcta.

 

 




