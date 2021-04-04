---
description: La tabla de control define los controles que aparecen en cada cuadro de diálogo.
ms.assetid: cbe7acd6-b916-45f3-b694-d2345c5a892a
title: Tabla de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ced41fcaf020a043962b16cf12d9c339901b415
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278164"
---
# <a name="control-table"></a>Tabla de control

La tabla de control define los controles que aparecen en cada cuadro de diálogo.

La tabla de control tiene las columnas siguientes.



| Columna        | Tipo                               | Clave | Nullable |
|---------------|------------------------------------|-----|----------|
| Diálogo\_      | [Identificador](identifier.md)       | Y   | N        |
| Control       | [Identificador](identifier.md)       | Y   | N        |
| Tipo          | [Identificador](identifier.md)       | N   | N        |
| X             | [Entero](integer.md)             | N   | N        |
| Y             | [Entero](integer.md)             | N   | N        |
| Ancho         | [Entero](integer.md)             | N   | N        |
| Alto        | [Entero](integer.md)             | N   | N        |
| Atributos    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Propiedad      | [Identificador](identifier.md)       | N   | Y        |
| Texto          | [Formatea](formatted.md)         | N   | Y        |
| Control \_ siguiente | [Identificador](identifier.md)       | N   | Y        |
| Ayuda          | [Texto](text.md)                   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Diálogo\_
</dt> <dd>

Clave externa a la primera columna de la [tabla de diálogo](dialog-table.md), el nombre del cuadro de diálogo.

</dd> <dt>

<span id="Control"></span><span id="control"></span><span id="CONTROL"></span>Control
</dt> <dd>

Nombre del control. Este nombre debe ser único dentro de un cuadro de diálogo, pero se puede repetir en distintos cuadros de diálogo. La columna de control combinada con la columna de cuadro de diálogo \_ forma la clave principal de esta tabla.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Automáticamente
</dt> <dd>

Tipo del control. Para obtener una lista de tipos de control, vea [controles](controls.md).

</dd> <dt>

<span id="X"></span><span id="x"></span>X1
</dt> <dd>

Coordenada horizontal de la esquina superior izquierda del límite rectangular del control. Debe ser un número no negativo. Vea [Position control Attribute](position-control-attribute.md).

</dd> <dt>

<span id="Y"></span><span id="y"></span>Sí
</dt> <dd>

Coordenada vertical de la esquina superior izquierda del límite rectangular del control. Debe ser un número no negativo. Vea [Position control Attribute](position-control-attribute.md).

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Ancho
</dt> <dd>

Ancho del límite rectangular del control. Debe ser un número no negativo. Vea [Position control Attribute](position-control-attribute.md).

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Alto
</dt> <dd>

Alto del límite rectangular del control. Debe ser un número no negativo. Vea [Position control Attribute](position-control-attribute.md).

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus
</dt> <dd>

Palabra de 32 bits que especifica las marcas de bits que se van a aplicar a este control. Debe ser un número no negativo y los valores permitidos dependen del tipo de control. Para obtener una lista de todos los atributos de control y el valor que se va a escribir en este campo, vea [atributos de control](control-attributes.md).

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Nombre de una propiedad definida que se va a vincular a este control. Los valores del botón de radio, el cuadro de lista y el cuadro combinado se asocian a un grupo mediante la vinculación a la misma propiedad. Esta columna es necesaria para los controles activos.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Negrita
</dt> <dd>

Una cadena localizable que se usa para establecer el texto inicial contenido en un control. La cadena también puede contener propiedades incrustadas. Para obtener la sintaxis de una cadena con formato que contiene propiedades, vea la función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) . Especifique el tamaño, la fuente y el color del texto mediante el prefijo de la cadena de texto { \\ Style}, donde Style es un estilo de texto creado en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). La cadena de texto se trunca si es demasiado largo para el control. La cadena de texto puede estar en blanco.

Se requiere la creación especial de la cadena de texto [con formato](formatted.md) en este campo si el texto se va a mostrar en un [control de texto](text-control.md) situado en un cuadro de diálogo con el atributo TrackDiskpace. Este es el caso especificado por el [bit de estilo del cuadro de diálogo TrackDiskSpace](trackdiskspace-dialog-style-bit.md) que aparece en los atributos de la [tabla del cuadro de diálogo](dialog-table.md). En este caso, si la cadena con formato de la columna de texto de la tabla de control comienza por " \[ " y termina por " \] ", debe agregar un espacio al final de la cadena. Por ejemplo, si DlgTextFont es una propiedad que se establecerá en "{ \\ DlgFontBold}", la cadena con formato " \[ DlgTextFont @ \] Text \[ ProductName \] " requiere el espacio al final del corchete de cierre. El instalador necesita este espacio adicional para mostrar correctamente el texto en el control de texto.

Puede escribir una cadena de texto descriptivo breve para los controles [VolumeCostList](volumecostlist-control.md), [ListView](listview-control.md), [DirectoryList](directorylist-control.md)y [SelectionTree](selectiontree-control.md). Este texto no es visible para el usuario, pero puede ser leído por lectores de pantalla como la descripción del control.

Vea también [accesibilidad](accessibility.md).

</dd> <dt>

<span id="Control_Next"></span><span id="control_next"></span><span id="CONTROL_NEXT"></span>Control \_ siguiente
</dt> <dd>

El nombre de otro control en el mismo cuadro de diálogo y una clave externa para la segunda columna de la tabla de control. Si el foco en el cuadro de diálogo está en el control de la columna de control, al presionar la tecla Tab se mueve el foco al control que aparece en la \_ columna control siguiente. Por lo tanto, esta columna se utiliza para especificar el orden de tabulación de los controles en el cuadro de diálogo. Los vínculos entre los controles deben formar un ciclo cerrado. Algunos controles, como los controles de texto estático, se pueden dejar fuera del ciclo. En este caso, este campo puede dejarse en blanco.

Vea también [accesibilidad](accessibility.md).

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>Ayuda
</dt> <dd>

Cadenas de texto opcional y localizables que se usan con el botón ayuda. La cadena se divide en dos partes por un carácter separador ( \| ). La primera parte de la cadena se usa como texto de información sobre herramientas. Los lectores de pantalla utilizan este texto para los controles que contienen una imagen. La segunda parte de la cadena se reserva para uso futuro. El carácter separador es necesario incluso si solo uno de los dos tipos de texto está presente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores enteros para x, y, ancho y alto se encuentran en las [unidades de instalador](installer-units.md), no en las unidades de cuadro de diálogo. Una unidad de instalador es igual a una duodécima el alto del tamaño de fuente MS Sans Serif de 10 puntos. Las coordenadas de los controles son relativas a la cartelera.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE31](ice31.md)  
[ICE32](ice32.md)  
[ICE34](ice34.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE95](ice95.md)  
</dl>

 

 



