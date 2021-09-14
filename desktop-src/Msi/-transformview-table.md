---
description: Se trata de una tabla temporal de solo lectura que se usa para ver transformaciones con el modo de vista de transformación. El instalador nunca conserva esta tabla.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: _TransformView tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159291"
---
# <a name="_transformview-table"></a>\_Tabla TransformView

Se trata de una tabla temporal de solo lectura que se usa para ver transformaciones con el modo de vista de transformación. El instalador nunca conserva esta tabla.

Para invocar el modo de vista de transformación, obtenga un identificador y abra la base de datos de referencia. Vea [Obtener un identificador de base de datos](obtaining-a-database-handle.md). Llame [**a MsiDatabaseApplyTransform con**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) EL ERROR DE MSITRANSFORM \_ \_ VIEWTRANSFORM. Esto impide que la transformación se aplique a la base de datos y vuelca el contenido de la transformación en la \_ tabla TransformView. Se puede acceder a los datos de la tabla mediante SQL consultas. Vea [Trabajar con consultas](working-with-queries.md).

La \_ tabla TransformView no se borra cuando se aplica otra transformación. La tabla refleja el efecto acumulativo de las aplicaciones sucesivas. Para ver las transformaciones por separado, debe liberar la tabla.

La \_ tabla TransformView tiene las columnas siguientes.



| Columna  | Tipo                         | Clave | Nullable |
|---------|------------------------------|-----|----------|
| Tabla   | [Identificador](identifier.md) | Y   | N        |
| Columna  | [Texto](text.md)             | Y   | N        |
| Row     | [Texto](text.md)             | Y   | Y        |
| Datos    | [Texto](text.md)             | N   | Y        |
| Current | [Texto](text.md)             | N   | Y        |



 

## <a name="column"></a>Columna

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Mesa
</dt> <dd>

Nombre de una tabla de base de datos modificada.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Columna
</dt> <dd>

Nombre de una columna de tabla modificada o INSERT, DELETE, CREATE o DROP.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Fila
</dt> <dd>

Lista de los valores de clave principal separados por pestañas. Los valores null de clave principal se representan mediante un solo carácter de espacio. Un valor NULL de esta columna indica un cambio de esquema.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Datos
</dt> <dd>

Datos, nombre de un flujo de datos o una definición de columna.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Actual
</dt> <dd>

Valor actual de la base de datos de referencia o columna un número.

</dd> </dl>

## <a name="remarks"></a>Observaciones

TransformView se mantiene en memoria mediante un recuento de bloqueos, que se puede liberar \_ con el siguiente SQL comando.

"ALTER TABLE \_ TransformView FREE".

Se puede acceder a los datos de la tabla mediante SQL consultas. El lenguaje SQL tiene dos divisiones principales: lenguaje de definición de datos (DDL) que se usa para definir todos los objetos de una base de datos de SQL y lenguaje de manipulación de datos (DML) que se usa para seleccionar, insertar, actualizar y eliminar datos en los objetos definidos mediante DDL.

Las operaciones de transformación del lenguaje de manipulación de datos (DML) se indican como sigue. Lenguaje de manipulación de datos (DML) son las instrucciones de SQL que manipulan, en lugar de definir, los datos.



| Operación de transformación | SQL resultado                                    |
|---------------------|-----------------------------------------------|
| Modificar datos         | {table} {column} {row} {data} {valor actual} |
| Insertar fila          | {table} "INSERT" {row} NULL NULL              |
| Eliminar fila          | {table} "DELETE" {row} NULL NULL              |



 

Las operaciones de transformación del lenguaje de definición de datos (DDL) se indican de la manera siguiente. Lenguaje de definición de datos (DDL) son las instrucciones de SQL que definen, en lugar de manipular, los datos.



| Operación de transformación | SQL resultado                                   |
|---------------------|----------------------------------------------|
| Agregar columna          | {table} {column} NULL {defn} {número de columna} |
| Agregar tabla           | {table} "CREATE" NULL NULL NULL              |
| Quitar tabla          | {table} "DROP" NULL NULL NULL                |



 

Cuando la aplicación de una transformación agrega esta tabla, el campo Datos recibe texto que se puede interpretar como un valor entero de 16 bits. El valor describe la columna denominada en el campo Columna. Puede comparar el valor entero con las constantes de la tabla siguiente para determinar la definición de la columna modificada.



| bit                                                                                                       | Descripción                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7<br/>         | Hexadecimal: 0x0000 0x0100<br/> Decimal: 0 255<br/> Ancho de columna<br/>                                                                                                                                                                                                                                  |
| <span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8<br/>                  | Hexadecimal: 0x0100<br/> Decimal: 256<br/> Columna persistente. Cero significa una columna temporal. <br/>                                                                                                                                                                                                   |
| <span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9<br/>                  | Hexadecimal: 0x0200<br/> Decimal: 1023<br/> Columna localizable. Cero significa que la columna no se puede localizar.<br/>                                                                                                                                                                                      |
| <span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11<br/> | Hexadecimal: 0x0000<br/> Decimal: 0<br/> Entero largo<br/> Hexadecimal: 0x0400<br/> Decimal: 1024<br/> Entero corto<br/> Hexadecimal: 0x0800<br/> Decimal: 2048<br/> Objeto binario<br/> Hexadecimal: 0x0C00<br/> Decimal: 3072<br/> String<br/> |
| <span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12<br/>              | Hexadecimal: 0x1000<br/> Decimal: 4096<br/> Columna que acepta valores NULL. Cero significa que la columna no acepta valores NULL.<br/>                                                                                                                                                                                               |
| <span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13<br/>              | Hexadecimal: 0x2000<br/> Decimal: 8192<br/> Columna de clave principal. Cero significa que esta columna no es una clave principal.<br/>                                                                                                                                                                                      |
| <span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15<br/> | Hexadecimal: 0x4000 0x8000<br/> Decimal: 16384 32768<br/> Reservada<br/>                                                                                                                                                                                                                                |



 

Para obtener un ejemplo de script que muestra la \_ tabla TransformView, vea [Ver una transformación](view-a-transform.md).

 

 




