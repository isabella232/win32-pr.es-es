---
description: 'Más información acerca de: estructura de JET_TABLECREATE3'
title: Estructura de JET_TABLECREATE3
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 587649b592f2b0d213a481c3bfbecc723240e486
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705456"
---
# <a name="jet_tablecreate3-structure"></a>Estructura de JET_TABLECREATE3


_**Se aplica a:** Windows | Windows Server_

La estructura de **JET_TABLECREATE3** contiene la información necesaria para crear una tabla rellenada con columnas e índices en una base de datos del motor de almacenamiento extensible (ese) y que designa una función de devolución de llamada. La función [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) utiliza la estructura **JET_TABLECREATE3** .

La estructura de **JET_TABLECREATE3** se presentó en el sistema operativo Windows 7.

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de esta estructura en bytes (para una futura ampliación). Debe establecerse en sizeof (JET_TABLECREATE3) en bytes.

**szTableName**

El objeto de la tabla que se va a crear.

El nombre debe cumplir las siguientes condiciones:

  - Debe tener un valor menor que JET_cbNameMost, sin incluir el carácter null de terminación.

  - Debe estar formado por el siguiente conjunto de caracteres: de 0 a 9, de la a a la Z, de la a a la z y de todos los demás signos de puntuación, excepto el signo de exclamación ( \! ), la coma (,), el corchete de apertura () y el \[ corchete de cierre ( \] ); es decir, los caracteres ASCII 0x20, de

  - No debe comenzar con un espacio.

  - Debe contener al menos un carácter que no sea un espacio.

**szTemplateTableName**

Nombre de una tabla existente de la que se va a heredar el lenguaje de definición de datos (DDL) base. El uso de una tabla de plantilla permite la creación sencilla de muchas tablas con columnas e índices idénticos.

**ulPages**

Número inicial de páginas de base de datos que se van a asignar a la tabla. Si se especifica un número mayor que uno, se puede reducir la fragmentación si se insertan muchas filas en esta tabla.

**ulDensity**

Densidad de la tabla, en puntos porcentuales. El número debe ser 0 o estar comprendido entre 20 y 100. Pasar 0 significa que se debe usar el valor predeterminado. El valor predeterminado es 80.

**rgcolumncreate**

Matriz de estructuras de [JET_COLUMNCREATE](./jet-columncreate-structure.md) , cada una de las cuales corresponde a una columna que se va a crear en la nueva tabla.

**cColumns**

El número de elementos [JET_COLUMNCREATE](./jet-columncreate-structure.md) en el parámetro *rgcolumncreate* .

**rgindexcreate**

Matriz de estructuras de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , cada una de las cuales corresponde a un índice que se va a crear en la nueva tabla.

**cIndexes**

El número de elementos [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) en el parámetro *rgindexcreate* .

**szCallback**

Función a la que se llama durante ciertos eventos. **cbtyp** determina cuándo se llamará a la función de devolución de llamada.

El formato de **szCallback** debe ser "función de módulo \! ", por ejemplo, "alpha \! beta" hace referencia a la función beta del módulo denominado "Alpha".

El prototipo de la función debe coincidir con la función de devolución de llamada [JET_CALLBACK](./jet-callback-callback-function.md) .

**cbtyp**

Describe el tipo de función de devolución de llamada designado por **szCallback**. Para obtener más información, vea [JET_CBTYP](./jet-cbtyp.md).

Este campo de bits se compone de uno o varios de los valores de bit que se enumeran en la tabla siguiente.

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
<td><p>JET_cbtypFinalize</p></td>
<td><p>Se llamará a la función de devolución de llamada cuando una columna que se pueda finalizar haya pasado a cero.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeInsert</p></td>
<td><p>Se llamará a la función de devolución de llamada antes de la inserción del registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterInsert</p></td>
<td><p>Se llamará a la función de devolución de llamada después de que el motor de base de datos haya terminado de insertar un registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeReplace</p></td>
<td><p>Se llamará a la función de devolución de llamada antes de la modificación de un registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterReplace</p></td>
<td><p>Se llamará a la función de devolución de llamada después de finalizar la modificación de un registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeDelete</p></td>
<td><p>Se llamará a la función de devolución de llamada antes de la eliminación de un registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterDelete</p></td>
<td><p>Se llamará a la función de devolución de llamada después de que se haya eliminado un registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypUserDefinedDefaultValue</p></td>
<td><p>Se llamará a la función de devolución de llamada para calcular un valor predeterminado definido por el usuario.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeCursorLS</p></td>
<td><p>Se llamará a la función de devolución de llamada cuando se debe liberar el almacenamiento local asociado a un cursor.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS</p></td>
<td><p>Se llamará a la función de devolución de llamada cuando se debe liberar el almacenamiento local asociado a una tabla.</p></td>
</tr>
</tbody>
</table>


**grbit**

Grupo de bits que contiene cero o más valores de la opción de llamada que se muestran en la tabla siguiente.

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
<td><p>Impide las operaciones DDL en la tabla (por ejemplo, agregar o quitar columnas).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>Hace que la tabla sea una tabla de plantilla. Las nuevas tablas pueden especificar el nombre de esta tabla como su tabla de plantilla. La configuración de JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Se debe usar junto con JET_bitTableCreateTemplateTable. Desusado. No utilizar.</p></td>
</tr>
</tbody>
</table>


**pSeqSpacehints**

Puntero a una estructura de [JET_SPACEHINTS](./jet-spacehints-structure.md) para el índice secuencial predeterminado.

**pSeqSpacehints** se presentó en Windows 7.

**pLVSpacehints**

Puntero a una estructura de [JET_SPACEHINTS](./jet-spacehints-structure.md) para un árbol de valores largos separados.

**pLVSpacehints** se presentó en Windows 7.

**cbSeparateLV**

Tamaño para separar una LV intrínseca del registro principal. Cualquier estructura de c de valor largo para un árbol de LV separado. Para obtener más información, consulte ng-Value en [JET_SPACEHINTS](./jet-spacehints-structure.md). Las columnas de valor largo menores que este valor pueden estar separadas si el registro es demasiado grande.

**cbSeparateLV** se presentó en Windows 7.

**TABLEID**

Un campo de salida que contiene el [JET_TABLEID](./jet-tableid.md) de la nueva tabla si la llamada a la API se realiza correctamente. Si se produce un error en la llamada API, el valor es indefinido. Esta tabla se abre exclusivamente.

**Creado**

Un campo de salida que contiene el recuento de objetos que se crean si la llamada de API se realiza correctamente. Si se produce un error en la llamada API, el valor es indefinido.

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
<td><p>Requiere Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JET_TABLECREATE3_W</strong> (Unicode) y <strong>JET_TABLECREATE3_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vea también

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
