---
description: 'Más información acerca de: JetCreateTableColumnIndex3 (función)'
title: JetCreateTableColumnIndex3 función)
TOCTitle: JetCreateTableColumnIndex3 Function
ms:assetid: c1a1b091-b4a6-4cdc-a0ea-af21c1462449
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294079(v=EXCHG.10)
ms:contentKeyID: 32765694
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex3
- JetCreateTableColumnIndex3W
- JetCreateTableColumnIndex3A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf1d6aed3178f5593826097f8c5d6b01bd8c72d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720754"
---
# <a name="jetcreatetablecolumnindex3-function"></a>JetCreateTableColumnIndex3 función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetcreatetablecolumnindex3-function"></a>JetCreateTableColumnIndex3 función)

La función **JetCreateTableColumnIndex3** crea una tabla en una base de datos de ese con un conjunto inicial de índices y un conjunto inicial de columnas de una matriz de estructuras [JET_TABLECREATE3](./jet-tablecreate3-structure.md) . La estructura de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) permite especificar una función de devolución de llamada.

**Windows 7:** **JetCreateTableColumnIndex3** se incluye en el sistema operativo Windows 7.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex3(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE3* ptablecreate
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se va a usar para la llamada API.

*DBID*

Identificador de base de datos que se va a usar para la llamada API.

*ptablecreate*

Puntero a una estructura de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) que define la tabla que se va a crear. Consulte [JET_TABLECREATE3](./jet-tablecreate3-structure.md) para obtener más detalles.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>No se pudo resolver la función de devolución de llamada. Es posible que no se haya encontrado el archivo DLL o que no se haya encontrado la función del archivo DLL. Con el registro suficiente habilitado, el registro de eventos proporcionará más detalles.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotIndex</p></td>
<td><p>Se intentó indexar sobre una columna de actualización de custodia o de SLV (tenga en cuenta que las columnas de SLV están desusadas).</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL</p></td>
<td><p>Si ptablecreate- &gt; grbit especifica JET_bitTableCreateTemplateTable, pero ptablecreate- &gt; szTemplateTableName se establece en NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Ya existe una columna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Se intentó indizar una columna que no existe. El intento de indizar condicionalmente en una columna que no existe también puede generar este error.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Se intentó agregar una columna redundante. No debe haber más de una columna de incremento automático y no más de una columna de versión por tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Este error se devolverá si el miembro <strong>ulDensity</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> está establecido en un número inferior a 20 o superior a 100.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>Significa que la tabla con el nombre del miembro <strong>szTemplateTableName</strong> de la estructura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> no se marcó como tabla de plantilla (es decir, que la tabla no tenía JET_bitTableCreateTemplateTable Set).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>Se ha intentado definir dos índices idénticos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>Se intentó especificar más de un índice principal para una tabla. Una tabla debe tener exactamente un índice principal. Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Se especificó una definición de índice no válida. A continuación se indican algunas de las razones posibles para recibir este error:</p>
<ul>
<li><p>Un índice principal es condicional (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene JET_bitIndexPrimary establecido y el miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> es mayor que cero).</p></li>
<li><p>Windows Server 2003 y versiones posteriores de Windows. Se ha intentado crear un índice de tupla con límites de tupla, pero sin pasar el miembro <strong>ptuplelimits</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (es decir, el miembro <strong>grbit</strong> de la estructura JET_INDEXCREATE2 tiene JET_bitIndexTupleLimits establecido, pero el puntero <strong>ptuplelimits</strong> es null).</p></li>
<li><p>Pasando una definición de clave no válida en el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obtener una descripción de las definiciones válidas.</p></li>
<li><p>Establecer el miembro <strong>cbVarSegMac</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para que sea mayor que JET_cbPrimaryKeyMost (para un índice principal) o mayor que JET_cbSecondaryKeyMost (para un índice secundario).</p></li>
<li><p>Pasar una combinación no válida para un índice Unicode definido por el usuario (una que tiene el bit de JET_bitIndexUnicode establecido en el miembro <strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>). Algunas causas comunes incluyen el miembro <strong>pidxunicode</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> es null o el LCID especificado en la estructura <strong>pidxunicode</strong> no es válido.</p></li>
<li><p>Especificar una columna de varios valores para un índice principal.</p></li>
<li><p>Intentando indexar demasiadas columnas condicionales. El miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe ser mayor que JET_ccolKeyMost.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Windows XP y versiones posteriores de Windows. Se especificó una estructura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> y no se admiten sus límites. Vea la sección Comentarios de la estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Windows XP y versiones posteriores de Windows. Un índice de tupla no puede ser único (es decir, el miembro <em>grbit</em> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexUnique).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Windows XP y versiones posteriores de Windows. Un índice de tupla solo puede estar en una sola columna (es decir, si el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene JET_bitIndexTuples establecido y el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica más de una columna).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Windows XP y versiones posteriores de Windows. Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexTuples).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP y versiones posteriores de Windows. Un índice de tupla solo puede estar en una columna de texto o Unicode. Un intento de indizar otras columnas (como columnas binarias) dará como resultado JET_errIndexTuplesTextColumnsOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP y versiones posteriores de Windows. Un índice de tupla no permite establecer el miembro <strong>cbVarSegMac</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Se intentó crear un índice sin información de versión mientras estaba en una transacción.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>El miembro <strong>CP</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> no se ha establecido en una página de códigos válida. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>El miembro <strong>coltyp</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> no se ha establecido en un tipo de columna válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCreateIndex</p></td>
<td><p>A continuación se indican algunos de los motivos por los que puede producirse este error:</p>
<ul>
<li><p>El miembro <strong>rgindexcreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> se estableció en NULL.</p></li>
<li><p>El miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> se estableció en NULL.</p></li>
<li><p>El miembro <strong>cbStruct</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no se ha establecido en un valor válido.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Se especificó una combinación no válida de miembros de <strong>grbit</strong> en <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</p>
<p>La definición del índice no es válida porque el miembro <strong>grbit</strong> contiene valores incoherentes. A continuación se indican algunas razones posibles:</p>
<ul>
<li><p>Un índice principal tenía un bit ignore especificado (es decir, JET_bitIndexPrimary se pasó con JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</p></li>
<li><p>Un índice vacío no omite ningún miembro nulo (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene JET_bitIndexEmpty establecido, pero no tiene JET_bitIndexIgnoreAnyNull establecida).</p></li>
<li><p>Pasando una estructura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un miembro <strong>grbit</strong> no válido.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Se pasó un ID. de configuración regional (LCID) no válido (ya sea a través del miembro <strong>LCID</strong> de la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a la que apunta el miembro <strong>pidxunicode</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> , o a través del campo <strong>LCID</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Se proporcionó un parámetro no válido. A continuación se indican algunas razones posibles:</p>
<ul>
<li><p>El miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> es NULL.</p></li>
<li><p>El miembro <strong>cbStruct</strong> de una de las estructuras <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> proporcionadas en el miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> no se estableció en sizeof (JET_COLUMNCREATE).</p></li>
<li><p>El miembro <strong>cbKey</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> se establece en cero.</p></li>
<li><p>El miembro <strong>cbStruct</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no se establece en sizeof (JET_INDEXCREATE2).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>El registro es demasiado grande. La suma del miembro <strong>cbMax</strong> de la estructura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas las columnas fijas no debe superar un valor determinado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate</p></td>
<td><p>La tabla ya existe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Se intentó agregar demasiadas columnas a la tabla. Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Error al intentar normalizar una columna Unicode. Esto puede deberse a la falta de recursos del sistema.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSpaceHintsInvalid</p></td>
<td><p>Un elemento de la estructura de sugerencias de espacio JET no era correcto o accionable.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

El nombre **JetCreateTableColumnIndex3** procede del orden de creación de los objetos: primero crea una tabla, columnas y, finalmente, índices. **JetCreateTableColumnIndex3** crea una tabla con un conjunto inicial de columnas e índices. Las columnas e índices adicionales se pueden agregar y quitar dinámicamente con [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md)y [JetDeleteIndex](./jetdeleteindex-function.md).

Al igual que [JetOpenTable](./jetopentable-function.md), cuando la aplicación se realiza utilizando el ID *. de tipo devuelto,* normalmente se debe cerrar con [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisitos

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
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetCreateTableColumnIndex3W</strong> (Unicode) y <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_CBTYP](./jet-cbtyp.md)  
[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateIndex3](./jetcreateindex3-function.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
