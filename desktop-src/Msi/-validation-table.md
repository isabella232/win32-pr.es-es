---
description: La \_ tabla de validación es una tabla del sistema que contiene los nombres de columna y los valores de columna de todas las tablas de la base de datos.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: _Validation tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666f00ccccda11706dce6a8d7e04e0efea91b7cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909161"
---
# <a name="_validation-table"></a>\_Tabla de validación

La \_ tabla de validación es una tabla del sistema que contiene los nombres de columna y los valores de columna de todas las tablas de la base de datos. Se utiliza durante el proceso de validación de la base de datos para asegurarse de que todas las columnas se han contabilizado y tienen los valores correctos. Esta tabla no se incluye con la base de datos del instalador.

La \_ tabla de validación tiene las columnas siguientes.



| Columna      | Tipo                               | Clave | Nullable |
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

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro
</dt> <dd>

Se utiliza para identificar una tabla determinada. Esta clave y la clave de columna forman la clave principal de la \_ tabla de validación.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Artículo
</dt> <dd>

Se utiliza para identificar una columna determinada de la tabla. Esta clave y la clave de tabla forman la clave principal de la \_ tabla de validación.

</dd> <dt>

<span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Acepta valores NULL
</dt> <dd>

Identifica si la columna puede contener un valor null.

Esta columna puede tener uno de los valores siguientes.



| String | Significado                                   |
|--------|-------------------------------------------|
| Y      | Sí, la columna puede tener un valor null.    |
| N      | No, la columna no puede tener un valor null. |



 

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue
</dt> <dd>

Este campo se aplica a las columnas que tienen un valor numérico. El campo contiene el valor mínimo permitido. Puede ser el valor mínimo de un entero o el valor mínimo de una fecha o una cadena de versión.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue
</dt> <dd>

Este campo se aplica a las columnas que tienen un valor numérico. El campo es el valor máximo permitido. Puede ser el valor máximo de un entero o el valor máximo de una fecha o una cadena de versión.

</dd> <dt>

<span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable
</dt> <dd>

Este campo se aplica a las columnas que son claves externas. El campo identificado en la columna debe vincularse al número de columna especificado por KeyColumn en la tabla denominada en KeyTable. Puede ser una lista de tablas separadas por punto y coma.

</dd> <dt>

<span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn
</dt> <dd>

Este campo se aplica a las columnas de la tabla que son claves externas. El campo identificado en la columna debe vincularse al número de columna especificado por KeyColumn en la tabla denominada en KeyTable. El intervalo permitido del campo KeyColumn es 1-32.

</dd> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría
</dt> <dd>

Es el tipo de datos que contiene el campo de base de datos especificado por las columnas de tabla y columna de la \_ tabla de validación. Si se trata de un tipo que tiene un valor numérico, como [Integer](integer.md), [DoubleInteger](doubleinteger.md) o [Time/Date](time-date.md), escriba null en este campo y especifique el intervalo del valor mediante las columnas MinValue y MaxValue. Utilice la columna categoría para especificar los tipos de datos no numéricos que se describen en [tipos de datos de columna](column-data-types.md).

</dd> <dt>

<span id="Set"></span><span id="set"></span><span id="SET"></span>Conjunto
</dt> <dd>

Esta es una lista de valores permitidos para este campo separados por punto y coma. Este campo se utiliza normalmente para las enumeraciones.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

Descripción de los datos que se almacenan en la columna.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

## <a name="remarks"></a>Observaciones

El campo Category de esta tabla solo se aplica a los datos de cadena. Si el campo de columna hace referencia a una columna con datos binarios, el tipo de datos binarios debe especificarse en el campo categoría. Los tipos de columna de datos enteros omiten el campo de categoría durante la validación.

 

 



