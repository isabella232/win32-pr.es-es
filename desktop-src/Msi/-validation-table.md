---
description: La tabla Validation es una tabla del sistema que contiene los nombres de columna y los valores de columna \_ de todas las tablas de la base de datos.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: _Validation tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a42fbe2a2f8da4abceb04912eee2a12edd708ff88d979fbf45f7de8051dc80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640450"
---
# <a name="_validation-table"></a>\_Tabla de validación

La tabla Validation es una tabla del sistema que contiene los nombres de columna y los valores de columna \_ de todas las tablas de la base de datos. Se usa durante el proceso de validación de la base de datos para asegurarse de que todas las columnas se tienen en cuenta y tienen los valores correctos. Esta tabla no se incluye con la base de datos del instalador.

La \_ tabla Validation tiene las columnas siguientes.



| Columna      | Tipo                               | Key | Nullable |
|-------------|------------------------------------|-----|----------|
| Tabla       | [Identificador](identifier.md)       | Y   | N        |
| Columna      | [Identificador](identifier.md)       | Y   | N        |
| Nullable    | [Texto](text.md)                   | N   | N        |
| MinValue    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MaxValue    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| KeyTable    | [Identificador](identifier.md)       | N   | Y        |
| KeyColumn   | [Entero](integer.md)             | N   | Y        |
| Category    | [Texto](text.md)                   | N   | Y        |
| Set         | [Texto](text.md)                   | N   | Y        |
| Descripción | [Texto](text.md)                   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Mesa
</dt> <dd>

Se usa para identificar una tabla determinada. Esta clave y la clave de columna forman la clave principal de la \_ tabla Validation.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Columna
</dt> <dd>

Se usa para identificar una columna determinada de la tabla. Esta clave y la clave de tabla forman la clave principal de la \_ tabla Validation.

</dd> <dt>

<span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable
</dt> <dd>

Identifica si la columna puede contener un valor NULL.

Esta columna puede tener uno de los valores siguientes.



| String | Significado                                   |
|--------|-------------------------------------------|
| Y      | Sí, la columna puede tener un valor NULL.    |
| N      | No, es posible que la columna no tenga un valor NULL. |



 

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue
</dt> <dd>

Este campo se aplica a las columnas que tienen un valor numérico. El campo contiene el valor mínimo permitido. Puede ser el valor mínimo para un entero o el valor mínimo para una cadena de fecha o versión.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue
</dt> <dd>

Este campo se aplica a las columnas que tienen un valor numérico. El campo es el valor máximo permitido. Puede ser el valor máximo de un entero o el valor máximo de una cadena de fecha o versión.

</dd> <dt>

<span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable
</dt> <dd>

Este campo se aplica a las columnas que son claves externas. El campo identificado en Column debe vincularse al número de columna especificado por KeyColumn en la tabla denominada en KeyTable. Puede ser una lista de tablas separadas por punto y coma.

</dd> <dt>

<span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn
</dt> <dd>

Este campo se aplica a las columnas de tabla que son claves externas. El campo identificado en Column debe vincularse al número de columna especificado por KeyColumn en la tabla denominada en KeyTable. El intervalo permitido del campo KeyColumn es de 1 a 32.

</dd> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría
</dt> <dd>

Este es el tipo de datos contenido en el campo de base de datos especificado por las columnas Tabla y Columna de la \_ tabla Validación. Si se trata de un tipo que tiene un valor numérico, como [Integer](integer.md), [DoubleInteger](doubleinteger.md) o [Time/Date,](time-date.md)escriba null en este campo y especifique el intervalo del valor mediante las columnas MinValue y MaxValue. Use la columna Categoría para especificar los tipos de datos no numéricos descritos en [Tipos de datos de columna](column-data-types.md).

</dd> <dt>

<span id="Set"></span><span id="set"></span><span id="SET"></span>Establecer
</dt> <dd>

Se trata de una lista de valores permitidos para este campo separados por punto y coma. Este campo se usa normalmente para enumeraciones.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Descripción de los datos almacenados en la columna.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

## <a name="remarks"></a>Observaciones

El campo Categoría de esta tabla solo se aplica a los datos de cadena. Si el campo Columna hace referencia a una columna con datos binarios, el tipo de datos binario debe especificarse en el campo Categoría. Tipos de columna de datos enteros omiten el campo Categoría durante la validación.

 

 



