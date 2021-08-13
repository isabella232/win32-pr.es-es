---
description: Los botones de radio no se tratan como controles individuales, pero forman parte de un grupo de botones de radio que funciona como un control RadioButtonGroup. En la tabla RadioButton se enumeran los botones de todos los grupos.
ms.assetid: 7f8f278a-a737-4116-9938-2850dbb611fa
title: Tabla RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc91ece6b5c71cd6ba46143f33e49b90b0278139d194a218a2fddb797bb55a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381055"
---
# <a name="radiobutton-table"></a>Tabla RadioButton

Los botones de radio no se tratan como controles individuales, pero forman parte de un grupo de botones de radio que funciona como [un control RadioButtonGroup](radiobuttongroup-control.md). En la tabla RadioButton se enumeran los botones de todos los grupos.

La tabla RadioButton tiene las siguientes columnas.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Propiedad | [Identificador](identifier.md) | Y   | N        |
| Pedido    | [Entero](integer.md)       | Y   | N        |
| Valor    | [Formato](formatted.md)   | N   | N        |
| X        | [Entero](integer.md)       | N   | N        |
| Y        | [Entero](integer.md)       | N   | N        |
| Ancho    | [Entero](integer.md)       | N   | N        |
| Alto   | [Entero](integer.md)       | N   | N        |
| Texto     | [Formato](formatted.md)   | N   | Y        |
| Ayuda     | [Texto](text.md)             | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Propiedad con nombre que se va a vincular a este botón de radio. Todos los botones asociados a la misma propiedad se convierten en parte del mismo grupo.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden
</dt> <dd>

Entero positivo que se usa para determinar el orden de los elementos de una lista. Los enteros no tienen que ser consecutivos.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Cadena de valor asociada a este botón. Al seleccionar el botón, se establece la propiedad asociada en este valor.

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Coordenada horizontal dentro del grupo de la esquina superior izquierda del rectángulo delimitador del botón de radio. Debe ser un número no negativo.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Coordenada vertical dentro del grupo de la esquina superior izquierda del rectángulo delimitador del botón de radio. Debe ser un número no negativo.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Ancho
</dt> <dd>

El ancho del botón. Debe ser un número no negativo.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Altura
</dt> <dd>

Alto del botón. Debe ser un número no negativo.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

Título localizable y visible que se va a asignar al botón de radio. Si el texto es demasiado largo para caber en el control, se trunca. Si el botón muestra un icono o un mapa de bits, esta columna contiene el nombre de la imagen, que es una clave en la [tabla binaria](binary-table.md). No hay ninguna manera de mostrar una imagen y un texto en un botón.

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>Ayuda
</dt> <dd>

Cadenas de Ayuda usadas con el botón . El texto es opcional y es localizable. La cadena se divide en dos partes separadas por un carácter ( \| ). La primera parte de la cadena se usa como texto de información sobre herramientas. Los lectores de pantalla muestran este texto para los controles que contienen una imagen. La segunda parte se usa para la Ayuda contextual, aunque todavía no se ha implementado la ayuda contextual. El carácter separador es necesario aunque solo uno de los dos tipos de texto esté presente.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los valores enteros de x, y, width y height se encuentran en las unidades [del instalador,](installer-units.md)no en las unidades de diálogo. Una unidad del instalador es igual a una duodécima parte del alto del tamaño de fuente de MS Sans Serif de 10 puntos. Las coordenadas de los controles son relativas a la ciudad.

Las coordenadas de los botones se dan en relación con el grupo. Si se cambian las coordenadas del grupo, los botones del grupo permanecen en la misma posición relativa entre sí.

El contenido de los campos Value y Text tiene el formato de la función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) cuando se crea el control, por lo que pueden contener cualquier expresión que la **función MsiFormatRecord** pueda interpretar. El formato solo se produce cuando se crea el control y no se actualiza si una propiedad implicada en la expresión se modifica durante la vida del control.

Cada control RadioButtonGroup está asociado a una propiedad . El valor predeterminado de esta propiedad debe inicializarse en la [tabla Property](property-table.md). Dentro de cada RadioButtonGroup especificado en la tabla RadioButton, puede haber un botón de radio que tenga un valor en el campo Valor que coincida con el valor predeterminado de esta propiedad. Este es el botón predeterminado para el control RadioButtonGroup. El botón predeterminado se muestra inicialmente como seleccionado en el control .

Tenga en cuenta que el usuario no puede cambiar el foco en un cuadro de diálogo presionando la tecla TAB en un control RadioButtonGroup hasta que se haya seleccionado uno de los botones del grupo. Para que el foco se mueva a este grupo de botones presionando la tecla TAB, especifique uno de los botones como botón predeterminado para el grupo.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE34](ice34.md)  
[ICE46](ice46.md)  
</dl>

 

 



