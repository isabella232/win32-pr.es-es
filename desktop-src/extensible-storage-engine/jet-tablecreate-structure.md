---
description: 'Más información acerca de: estructura de JET_TABLECREATE'
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
ms.openlocfilehash: f96b73daaf446023a7fe3a5729dcb1c90b5f14e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153779"
---
# <a name="jet_tablecreate-structure"></a>Estructura de JET_TABLECREATE


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_tablecreate-structure"></a>Estructura de JET_TABLECREATE

La estructura **JET_TABLECREATE** contiene la información necesaria para crear una tabla rellenada con columnas e índices en una base de datos ese. [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) utiliza la estructura de **JET_TABLECREATE**

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

Tamaño de esta estructura en bytes (para una futura ampliación). Debe establecerse en sizeof (JET_TABLECREATE) en bytes.

**szTableName**

El objeto de la tabla que se va a crear.

El nombre debe cumplir las siguientes condiciones:

  - Tener un valor inferior a JET_cbNameMost, sin incluir el carácter NULL de terminación.

<!-- end list -->

  - Consta del siguiente conjunto de caracteres: de 0 a 9, de la a a la Z, de la a a la z, y todos los demás signos de puntuación, excepto el signo de exclamación ( \! ), la coma (,), el corchete de apertura () y el \[ corchete de cierre ( \] ), es decir, caracteres ASCII 0x20, de 0x22 a 0x2d,

<!-- end list -->

  - No comienza con un espacio.

<!-- end list -->

  - Consta de al menos un carácter que no sea un espacio.

**szTemplateTableName**

Nombre de una tabla ya existente de la que se va a heredar el DDL base (lenguaje de definición de datos). El uso de una tabla de plantilla permite la creación sencilla de muchas tablas con columnas e índices idénticos.

**ulPages**

Número inicial de páginas de base de datos que se van a asignar a la tabla. Si se especifica un número mayor que uno, se puede reducir la fragmentación si se insertan muchas filas en esta tabla.

**ulDensity**

Densidad de la tabla, en puntos porcentuales. El número debe ser 0 o estar comprendido entre 20 y 100. Pasar 0 significa que se debe usar el valor predeterminado. El valor predeterminado es 80.

**rgcolumncreate**

Matriz de estructuras de [JET_COLUMNCREATE](./jet-columncreate-structure.md) , cada una de las cuales corresponde a una columna que se va a crear en la nueva tabla.

**cColumns**

El número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) en **rgcolumncreate**.

**rgindexcreate**

Matriz de estructuras de [JET_INDEXCREATE](./jet-indexcreate-structure.md) , cada una de las cuales corresponde a un índice que se va a crear en la nueva tabla.

**cIndexes**

El número de elementos [JET_INDEXCREATE](./jet-indexcreate-structure.md) en **rgindexcreate**.

**grbit**

Grupo de bits que contiene las opciones de esta llamada, que incluyen cero o más de los valores siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitTableCreateFixedDDL</p></td>
<td><p>La configuración de JET_bitTableCreateFixedDDL impide las operaciones DDL en la tabla (por ejemplo, agregar o quitar columnas).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>La configuración de JET_bitTableCreateTemplateTable hace que la tabla sea una tabla de plantilla. Las nuevas tablas pueden especificar el nombre de esta tabla como su tabla de plantilla. La configuración de JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Desusado. No utilizar.</p></td>
</tr>
</tbody>
</table>


**TABLEID**

Un campo de salida que contiene el [JET_TABLEID](./jet-tableid.md) de la nueva tabla si la llamada a la API se realiza correctamente. Si se produce un error en la llamada API, el valor es indefinido.

**Creado**

Un campo de salida que contiene el recuento de objetos creados si la llamada de API se realiza correctamente. Si se produce un error en la llamada API, el valor es indefinido.

El recuento de objetos que se crean es igual a la suma de las columnas, las tablas y los índices que se han creado correctamente.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JET_TABLECREATE_W</strong> (Unicode) y <strong>JET_TABLECREATE_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
