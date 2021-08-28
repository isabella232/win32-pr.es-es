---
description: 'Más información sobre: JET_TABLECREATE estructura'
title: Estructura de JET_TABLECREATE
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
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
ms.openlocfilehash: fcc6c63b06614eb16379fbb18d59a5459a8e5085
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983038"
---
# <a name="jet_tablecreate-structure"></a>Estructura de JET_TABLECREATE


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_tablecreate-structure"></a>Estructura de JET_TABLECREATE

La **JET_TABLECREATE** contiene la información necesaria para crear una tabla rellenada con columnas e índices en una base de datos ESE. [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) usa la estructura JET_TABLECREATE de datos. 

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de esta estructura en bytes (para futuras expansiones). Debe establecerse en sizeof( JET_TABLECREATE ) en bytes.

**szTableName**

El objeto de la tabla que se va a crear.

El nombre debe usar para cumplir las condiciones siguientes:

  - Tenga un valor menor que JET_cbNameMost, sin incluir el valor NULL final.

<!-- end list -->

  - Consta del siguiente conjunto de caracteres: de 0 a 9, de la A a la Z, de la a la z y de todos los demás signos de puntuación excepto el signo de exclamación ( ), la coma (,), el corchete de apertura ( ) y el corchete de cierre ( ), es decir, caracteres ASCII 0x20, 0x22 a través de 0x2d, 0x2f a través de 0x5a, 0x5c y 0x5d \! \[ a \] 0x7f.

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

Número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) en **rgcolumncreate**.

**rgindexcreate**

Matriz de [JET_INDEXCREATE](./jet-indexcreate-structure.md) estructura, cada una de las cuales corresponde a un índice que se va a crear en la nueva tabla.

**cIndexes**

Número de elementos [JET_INDEXCREATE](./jet-indexcreate-structure.md) en **rgindexcreate**.

**grbit**

Grupo de bits que contienen las opciones para esta llamada, que incluyen cero o más de los valores siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>Al JET_bitTableCreateFixedDDL se evitan las operaciones DDL en la tabla (por ejemplo, agregar o quitar columnas).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>Si JET_bitTableCreateTemplateTable hace que la tabla sea una tabla de plantilla. A continuación, las nuevas tablas pueden especificar el nombre de esta tabla como tabla de plantilla. Establecer JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Desusado. No utilizar.</p> | 



**tableid**

Campo de salida que contiene el [JET_TABLEID](./jet-tableid.md) de la nueva tabla si la llamada API se realiza correctamente. Si se produce un error en la llamada API, el valor no está definido.

**cCreated**

Campo de salida que contiene el recuento de objetos creados si la llamada API se realiza correctamente. Si se produce un error en la llamada API, el valor no está definido.

El recuento de objetos creados es igual a la suma de columnas, tablas e índices creados correctamente.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_TABLECREATE_W</strong> (Unicode) <strong>y JET_TABLECREATE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte también

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
