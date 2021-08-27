---
description: 'Más información sobre: JET_TABLECREATE2 estructura'
title: Estructura de JET_TABLECREATE2
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 95e4d60ba80317624004fa7c9335005aa16a9300
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476471"
---
# <a name="jet_tablecreate2-structure"></a>Estructura de JET_TABLECREATE2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_tablecreate2-structure"></a>Estructura de JET_TABLECREATE2

La **JET_TABLECREATE2** contiene la información necesaria para crear una tabla rellenada con columnas e índices en una base de datos ESE y que designa una función de devolución de llamada. [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)usa la estructura JET_TABLECREATE2 estructura . 

**Windows XP:** La **JET_TABLECREATE2** se introduce en Windows XP.

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de esta estructura en bytes (para futuras expansiones). Debe establecerse en sizeof( JET_TABLECREATE2 ) en bytes.

**szTableName**

Nombre de la tabla que se creará.

El nombre debe cumplir las condiciones siguientes:

  - Tenga un valor menor que JET_cbNameMost, sin incluir el valor NULL final.

<!-- end list -->

  - Consta del siguiente conjunto de caracteres: de 0 a 9, de la A a la Z, de la a la z y de todos los demás signos de puntuación excepto el signo de exclamación ( ), la coma (,), el corchete de apertura ( ) y el corchete de cierre ( ), es decir, caracteres ASCII 0x20, 0x22 a través de 0x2d, 0x2f a través de 0x5a, 0x5c y \! 0x5d a \[ \] 0x7f.

<!-- end list -->

  - No comience con un espacio.

<!-- end list -->

  - Consta de al menos un carácter que no es de espacio.

**szTemplateTableName**

Nombre de una tabla ya existente de la que se va a heredar DDL base (lenguaje de definición de datos). El uso de una tabla de plantillas permite crear fácilmente muchas tablas con columnas e índices idénticos.

**ulPages**

Número inicial de páginas de base de datos que se asignarán a la tabla. Especificar un número mayor que uno puede reducir la fragmentación si se insertan muchas filas en esta tabla.

**ulDensity**

Densidad de tabla, en puntos porcentuales. El número debe ser 0 o en el intervalo de 20 a 100. Pasar 0 significa que se debe usar el valor predeterminado. El valor predeterminado es 80.

**rgcolumncreate**

Matriz de [JET_COLUMNCREATE](./jet-columncreate-structure.md) estructura, cada una de las cuales corresponde a una columna que se va a crear en la nueva tabla.

**cColumns**

número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) en **rgcolumncreate**.

**rgindexcreate**

Matriz de [JET_INDEXCREATE](./jet-indexcreate-structure.md) estructura, cada una de las cuales corresponde a un índice que se va a crear en la nueva tabla.

**cIndexes**

Número de elementos [JET_INDEXCREATE](./jet-indexcreate-structure.md) en **rgindexcreate**.

**szCallback**

Función a la que se llama durante determinados eventos. **cbtyp determina** cuándo se llamará a la función de devolución de llamada.

El formato de **szCallback** debe ser "función de módulo"; por ejemplo, "alpha beta" hace referencia a la función beta en el módulo \! \! denominado "alpha". El prototipo de la función debe coincidir con [JET_CALLBACK](./jet-callback-callback-function.md). Para obtener más información, [vea JET_CALLBACK](./jet-callback-callback-function.md).

**cbtyp**

Describe el tipo de función de devolución de llamada designada por **szCallback**. Para obtener más información, [vea JET_CBTYP](./jet-cbtyp.md). Este campo de bits se compone de uno o varios de los bits siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_cbtypFinalize</p> | <p>Se llamará a la función de devolución de llamada cuando una columna que se pueda finalizar haya pasado a cero.</p> | 
| <p>JET_cbtypBeforeInsert</p> | <p>Se llamará a la función de devolución de llamada antes de la inserción del registro.</p> | 
| <p>JET_cbtypAfterInsert</p> | <p>Se llamará a la función de devolución de llamada una vez que el motor de base de datos haya terminado de insertar un registro.</p> | 
| <p>JET_cbtypBeforeReplace</p> | <p>Se llamará a la función de devolución de llamada antes de modificar un registro.</p> | 
| <p>JET_cbtypAfterReplace</p> | <p>Se llamará a la función de devolución de llamada después de finalizar la modificación de un registro.</p> | 
| <p>JET_cbtypBeforeDelete</p> | <p>Se llamará a la función de devolución de llamada antes de eliminar un registro.</p> | 
| <p>JET_cbtypAfterDelete</p> | <p>Se llamará a la función de devolución de llamada después de eliminar un registro.</p> | 
| <p>JET_cbtypUserDefinedDefaultValue</p> | <p>Se llamará a la función de devolución de llamada para calcular un valor predeterminado definido por el usuario.</p> | 
| <p>JET_cbtypOnlineDefragCompleted</p> | <p>Se llamará a la función de devolución de llamada después de que se haya completado una llamada a <a href="gg294095(v=exchg.10).md">JetDefragment2.</a></p> | 
| <p>JET_cbtypFreeCursorLS</p> | <p>Se llamará a la función de devolución de llamada cuando se deba liberar el almacenamiento local asociado a un cursor.</p> | 
| <p>JET_cbtypFreeTableLS</p> | <p>Se llamará a la función de devolución de llamada cuando se deba liberar el almacenamiento local asociado a una tabla.</p> | 



**grbit**

Grupo de bits que contienen las opciones para esta llamada, que incluyen cero o más de los valores siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>Al JET_bitTableCreateFixedDDL se evitan las operaciones DDL en la tabla (por ejemplo, agregar o quitar columnas).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>Si JET_bitTableCreateTemplateTable hace que la tabla sea una tabla de plantilla. A continuación, las nuevas tablas pueden especificar el nombre de esta tabla como tabla de plantilla. Establecer JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Debe usarse junto con JET_bitTableCreateTemplateTable. Desusado. No utilizar.</p> | 



**tableid**

Campo de salida que contiene el [JET_TABLEID](./jet-tableid.md) de la nueva tabla si la llamada API se realiza correctamente. Si se produce un error en la llamada API, el valor no está definido.

**cCreated**

Campo de salida que contiene el recuento de objetos que se crean si la llamada API se realiza correctamente. Si se produce un error en la llamada API, el valor no está definido.

El recuento de objetos creados es igual a la suma de columnas, tablas e índices creados correctamente.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_TABLECREATE2_W</strong> (Unicode) <strong>y JET_TABLECREATE2_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte también

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetDefragment2](./jetdefragment2-function.md)
