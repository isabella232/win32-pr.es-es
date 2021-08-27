---
description: 'Más información sobre: JetCreateTableColumnIndex4W (Función)'
title: JetCreateTableColumnIndex4W (Función)
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e0ecb22fe9936c9843c603211b0594599de7fcd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479191"
---
# <a name="jetcreatetablecolumnindex4w-function"></a>JetCreateTableColumnIndex4W (Función)


_**Se aplica a:** Windows | Windows Servidor_

La **función JetCreateTableColumnIndex4W** crea una tabla en un motor de Storage extensible (base de datos ESE( con un conjunto inicial de índices y un conjunto inicial de columnas a partir de una [matriz](./jet-tablecreate3-structure.md) de JET_TABLECREATE3 estructuras. La [JET_TABLECREATE3](./jet-tablecreate3-structure.md) estructura permite especificar una función de devolución de llamada.

La **función JetCreateTableColumnIndex4W** se introdujo en el Windows 8 operativo.

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*Dbid*

Identificador de base de datos que se usará para la llamada API.

*ptablecreate*

Puntero a [un](./jet-tablecreate3-structure.md) JET_TABLECREATE3 estructura que define la tabla que se va a crear. Consulte [JET_TABLECREATE3](./jet-tablecreate3-structure.md) para obtener más detalles.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los códigos de retorno enumerados en la tabla siguiente. Para obtener más información sobre los posibles errores extensibles Storage Enginge (ESE), vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>No se pudo resolver la función de devolución de llamada. Es posible que no se haya encontrado el archivo DLL o que no se haya encontrado la función del archivo DLL. Con el registro suficiente habilitado, el registro de eventos proporcionará más detalles.</p> | 
| <p>JET_errCannotIndex</p> | <p>Se intentó indexar sobre una columna SLV o de actualización de custodia (tenga en cuenta que las columnas SLV están en desuso).</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Se devuelve si <em>el parámetro ptablecreate- &gt; grbit</em> especifica el JET_bitTableCreateTemplateTable, pero el parámetro <em>ptablecreate- &gt; szTemplateTableName</em> se establece en null.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Ya existe una columna.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Se intentó indexar sobre una columna inexistente. Un intento de indexar condicionalmente sobre una columna inexistente también puede producir este error.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Se intentó agregar una columna redundante. No debe existir más de una columna de autoincremento y no debe existir más de una columna de versión por tabla.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Este error se devolverá si el miembro <strong>ulDensity</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> está establecido en un número menor que 20 o más de 100.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Indica que la tabla denominada en el miembro <strong>szTemplateTableName</strong> de la estructura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> no se ha marcado como una tabla de plantilla (es decir, esa tabla no tenía el valor de parámetro JET_bitTableCreateTemplateTable establecido).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Se intentó definir dos índices idénticos.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Se intentó especificar más de un índice principal para una tabla. Una tabla debe tener exactamente un índice principal. Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Se especificó una definición de índice no válida. Estas son algunas de las posibles razones de este error:</p><ul><li><p>Un índice principal es condicional (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene establecido el valor JET_bitIndexPrimary y el miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> es mayor que cero).</p></li><li><p>Se aplica a las versiones del sistema operativo Windows Server a partir de Windows Server 2003. Intento de crear un índice de tupla con límites de tupla, pero sin pasar el miembro <strong>ptuplelimits</strong> en la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (es decir, el miembro <strong>grbit</strong> de la estructura <strong>JET_INDEXCREATE2</strong> JET_bitIndexTupleLimits tiene un valor establecido, pero el <strong>puntero ptuplelimits</strong> es null).</p></li><li><p>Pasar una definición de clave no válida en <strong>el miembro szKey</strong> de la <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> estructura. Para obtener información sobre las definiciones válidas, <a href="gg294082(v=exchg.10).md">vea JET_INDEXCREATE2</a>.</p></li><li><p>Establecer <strong>el miembro cbVarSegMac</strong> en <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para que sea mayor que el valor JET_cbPrimaryKeyMost (para un índice principal) o mayor que el valor JET_cbSecondaryKeyMost (para un índice secundario).</p></li><li><p>Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tenga el bit de valor JET_bitIndexUnicode establecido en el miembro <strong>grbit</strong> de la <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> estructura). Algunas causas comunes incluyen el <strong>miembro pidxunicode</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> es NULL o el LCID especificado en la estructura <strong>pidxunicode</strong> no es válido.</p></li><li><p>Especificar una columna de varios valores para un índice principal.</p></li><li><p>Intentando indexar demasiadas columnas condicionales. El <strong>miembro cConditionalColumn</strong> de la <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> estructura no debe ser mayor que <strong>JET_ccolKeyMost</strong>.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Se aplica a las versiones de Windows a partir de Windows XP. Se <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> estructura de datos y no se admiten sus límites. Para obtener más información, vea la sección comentarios de la <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> estructura.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla no puede ser único (es decir, el miembro <em>grbit</em> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe tener valores JET_bitIndexPrimary y JET_bitIndexUnique establecidos).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla solo puede estar sobre una sola columna (es decir, si el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> JET_bitIndexTuples tiene un valor establecido y el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica más de una columna).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe tener tanto JET_bitIndexPrimary como JET_bitIndexTuples establecidos).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla solo puede estar en una columna de texto o Unicode. Un intento de indexar otras columnas (como las columnas binarias) dará lugar a un JET_errIndexTuplesTextColumnsOnly de respuesta.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla no permite establecer el <strong>miembro cbVarSegMac</strong> de <a href="gg294082(v=exchg.10).md">la JET_INDEXCREATE2</a> estructura.</p> | 
| <p>JET_errInTransaction</p> | <p>Se intentó crear un índice sin información de versión mientras estaba en una transacción.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>El <strong>miembro cp</strong> de la <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> estructura no se estableció en una página de códigos válida. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de 0 significa que se usará el valor predeterminado (inglés, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>El <strong>miembro coltyp</strong> de la <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> estructura no se estableció en un tipo de columna válido.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Estas son algunas de las razones por las que puede producirse este error:</p><ul><li><p>El <strong>miembro rgindexcreate</strong> de la <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> estructura se estableció en null.</p></li><li><p>El <strong>miembro rgcolumncreate</strong> de la <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> estructura se estableció en null.</p></li><li><p>El <strong>miembro cbStruct</strong> de una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> estructura no se estableció en un valor válido.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>Se especificó una combinación no válida de miembros <strong>grbit</strong> en la <a href="gg269264(v=exchg.10).md">estructura JET_TABLECREATE3</a> datos.</p><p>La definición del índice no es válida porque el <strong>miembro grbit</strong> contiene valores incoherentes. Estas son algunas de las posibles razones:</p><ul><li><p>Se especificó un bit de ignore en un índice principal (es decir, JET_bitIndexPrimary se pasó un valor con los valores JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</p></li><li><p>Un índice vacío no omite ningún miembro null (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene el valor JET_bitIndexEmpty establecido, pero no tiene un JET_bitIndexIgnoreAnyNull de valores).</p></li><li><p>Pasar una estructura <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un <strong>miembro grbit</strong> no válido.</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Se pasó un identificador de configuración regional (LCID) no válido (ya sea a través del miembro <strong>lcid</strong> de la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX a</a> la que apunta el miembro <strong>pidxunicode</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> o a través del campo <strong>lcid</strong> de la <a href="gg294082(v=exchg.10).md">estructura JET_INDEXCREATE2).</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>Se ha especificado un parámetro no válido. Estos son algunos de los motivos posibles:</p><ul><li><p>El <strong>miembro rgcolumncreate</strong> de la <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> estructura es NULL.</p></li><li><p>El <strong>miembro cbStruct</strong> de una de las <a href="gg269252(v=exchg.10).md">estructuras JET_COLUMNCREATE</a> dadas en el miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> no se estableció en sizeof( JET_COLUMNCREATE ).</p></li><li><p>El <strong>miembro cbKey</strong> de una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> estructura está establecido en cero.</p></li><li><p>El <strong>miembro cbStruct</strong> de una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> estructura no se establece en sizeof( JET_INDEXCREATE2 ).</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>El registro es demasiado grande. La suma del <strong>miembro cbMax</strong> de la <a href="gg269252(v=exchg.10).md">estructura JET_COLUMNCREATE</a> para todas las columnas fijas no debe superar un valor determinado.</p> | 
| <p>JET_errTableDuplicate</p> | <p>La tabla ya existe.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Se intentó agregar demasiadas columnas a la tabla. Una tabla no puede tener más de <strong>JET_ccolFixedMost</strong> columnas fijas, no más de <strong>JET_ccolVarMost</strong> columnas de longitud variable y no más de <strong>JET_ccolTaggedMost</strong> columnas etiquetadas.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Error al intentar normalizar una columna Unicode. Esto puede deberse a que se están quedando sin recursos del sistema.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Un elemento de la estructura de sugerencias de espacio JET no era correcto ni utilizable.</p> | 



#### <a name="remarks"></a>Comentarios

La **función JetCreateTableColumnIndex4W** crea una tabla con un conjunto inicial de columnas e índices. Las columnas e índices adicionales se pueden agregar y quitar dinámicamente mediante las funciones [JetAddColumn,](./jetaddcolumn-function.md) [JetDeleteColumn,](./jetdeletecolumn-function.md) [JetDeleteColumn2,](./jetdeletecolumn2-function.md) [JetCreateIndex,](./jetcreateindex-function.md) [JetCreateIndex2,](./jetcreateindex2-function.md) [JetCreateIndex3,](./jetcreateindex3-function.md) [JetCreateIndex4W](./jetcreateindex4w-function.md)y [JetDeleteIndex.](./jetdeleteindex-function.md)

Al igual que [con la función JetOpenTable,](./jetopentable-function.md) cuando la aplicación se realiza con el *tableid* devuelto, la función [JetCloseTable](./jetclosetable-function.md) debe cerrar la aplicación.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows 8.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



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
