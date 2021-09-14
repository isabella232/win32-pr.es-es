---
description: 'Más información sobre: JetCreateTableColumnIndex2 (Función)'
title: Función JetCreateTableColumnIndex2
TOCTitle: JetCreateTableColumnIndex2 Function
ms:assetid: ad9caaf3-8cd2-453f-894d-8ac438c50b73
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294057(v=EXCHG.10)
ms:contentKeyID: 32765672
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex2W
- JetCreateTableColumnIndex2
- JetCreateTableColumnIndex2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d653de45603b572ed910ccd5d6f4ccc600fdcdff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965548"
---
# <a name="jetcreatetablecolumnindex2-function"></a>Función JetCreateTableColumnIndex2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcreatetablecolumnindex2-function"></a>Función JetCreateTableColumnIndex2

La **función JetCreateTableColumnIndex2** crea una tabla en una base de datos ESE con un conjunto inicial de índices y un conjunto inicial de columnas a partir de una [matriz de JET_TABLECREATE2](./jet-tablecreate2-structure.md) estructuras. La [JET_TABLECREATE2](./jet-tablecreate2-structure.md) estructura permite especificar una función de devolución de llamada.

**Windows XP: JetCreateTableColumnIndex2** se introdujo en Windows XP.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex2(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE2* ptablecreate
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*Dbid*

Identificador de base de datos que se usará para la llamada API.

*ptablecreate*

Puntero a una [estructura JET_TABLECREATE2](./jet-tablecreate2-structure.md) que define la tabla que se va a crear. Consulte [JET_TABLECREATE2](./jet-tablecreate2-structure.md) para obtener más detalles.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores ese, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>No se pudo resolver la función de devolución de llamada. Es posible que no se haya encontrado el archivo DLL o que la función del archivo DLL no se haya encontrado. Con el registro suficiente habilitado, el registro de eventos proporcionará más detalles.</p> | 
| <p>JET_errCannotIndex</p> | <p>Se intentó indexar sobre una columna de actualización de custodia o SLV (tenga en cuenta que las columnas SLV están en desuso).</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Si ptablecreate- &gt; grbit especifica JET_bitTableCreateTemplateTable, pero ptablecreate- &gt; szTemplateTableName se establece en NULL.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Ya existe una columna.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Se intentó indexar sobre una columna inexistente. El intento de indexar condicionalmente una columna inexistente también puede producir este error.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Se intentó agregar una columna redundante. No debería haber más de una columna de autoincremento y no más de una columna de versión por tabla.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Este error se devolverá si el miembro <strong>ulDensity</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> está establecido en un número menor que 20 o más de 100.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Significa que la tabla denominada en el miembro <strong>szTemplateTableName</strong> de la estructura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> no era una tabla marcada como una tabla de plantilla (es decir, esa tabla no tenía JET_bitTableCreateTemplateTable establecido).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Se intentó definir dos índices idénticos.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Se intentó especificar más de un índice principal para una tabla. Una tabla debe tener exactamente un índice principal. Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Se especificó una definición de índice no válida. Algunas de las posibles razones para recibir este error son:</p><ul><li><p>Un índice principal es condicional (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexPrimary establecido y el miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es mayor que cero).</p></li><li><p>Windows Server 2003 y versiones posteriores. Intentando crear un índice de tupla con límites de tupla, pero sin pasar el miembro <strong>ptuplelimits</strong> en la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexTupleLimits establecido, pero el <strong>puntero ptuplelimits</strong> es NULL).</p></li><li><p>Pasar una definición de clave no válida en el <strong>miembro szKey</strong> <a href="gg269186(v=exchg.10).md">de la JET_INDEXCREATE</a> estructura . Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una explicación de las definiciones válidas.</p></li><li><p>Establecer el <strong>miembro cbVarSegMac</strong> en <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> sea mayor que JET_cbPrimaryKeyMost (para un índice principal) o mayor que JET_cbSecondaryKeyMost (para un índice secundario).</p></li><li><p>Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tenga el bit JET_bitIndexUnicode establecido en el miembro <strong>grbit</strong> <a href="gg269186(v=exchg.10).md">de JET_INDEXCREATE</a>). Algunas causas comunes incluyen el <strong>miembro pidxunicode</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es NULL o el LCID especificado en la estructura <strong>pidxunicode</strong> no es válido.</p></li><li><p>Especificar una columna con varios valores para un índice principal.</p></li><li><p>Intentando indexar demasiadas columnas condicionales. El <strong>miembro cConditionalColumn</strong> de la <a href="gg269186(v=exchg.10).md">estructura JET_INDEXCREATE</a> no debe ser mayor que JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP y versiones posteriores. Se <a href="gg269207(v=exchg.10).md">especificó JET_TUPLELIMITS</a> estructura y no se admiten sus límites. Consulte la sección de comentarios de la <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> estructura.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP y versiones posteriores. Un índice de tupla no puede ser único (es decir, el miembro <em>grbit</em> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener JET_bitIndexPrimary y JET_bitIndexUnique establecido).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP y versiones posteriores. Un índice de tupla solo puede estar sobre una sola columna (es decir, si el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene un conjunto de JET_bitIndexTuples y el miembro <strong>szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especifica más de una columna).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP y versiones posteriores. Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener JET_bitIndexPrimary ni JET_bitIndexTuples establecidos).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP y versiones posteriores. Un índice de tupla solo puede estar en una columna de texto o Unicode. Un intento de indexar otras columnas (por ejemplo, columnas binarias) dará lugar a JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP y versiones posteriores. Un índice de tupla no permite establecer el <strong>miembro cbVarSegMac</strong> <a href="gg269186(v=exchg.10).md">de la JET_INDEXCREATE</a> estructura.</p> | 
| <p>JET_errInTransaction</p> | <p>Se intentó crear un índice sin información de versión mientras se encontraba en una transacción.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>El <strong>miembro cp</strong> de la <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> estructura no se estableció en una página de códigos válida. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de 0 significa que se usará el valor predeterminado (inglés, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>El <strong>miembro coltyp</strong> de la <a href="gg269252(v=exchg.10).md">estructura JET_COLUMNCREATE</a> no se estableció en un tipo de columna válido.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Algunas de las razones por las que se puede producir este error:</p><ul><li><p>El <strong>miembro rgindexcreate</strong> de la <a href="gg269203(v=exchg.10).md">estructura JET_TABLECREATE2</a> se estableció en NULL.</p></li><li><p>El <strong>miembro rgcolumncreate</strong> de la <a href="gg269203(v=exchg.10).md">estructura JET_TABLECREATE2</a> se estableció en NULL.</p></li><li><p>El <strong>miembro cbStruct</strong> de una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura no se estableció en un valor válido.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>Se especificó una combinación no válida de miembros <strong>grbit</strong> <a href="gg294146(v=exchg.10).md">en JET_TABLECREATE</a> o <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</p><p>La definición del índice no es válida porque el <strong>miembro grbit</strong> contiene valores incoherentes. Estos son algunos de los motivos posibles:</p><ul><li><p>Un índice principal tenía especificado un bit de ignore (es decir, JET_bitIndexPrimary se pasó con JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</p></li><li><p>Un índice vacío no omite ningún miembro NULL (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexEmpty establecido, pero no tiene JET_bitIndexIgnoreAnyNull establecido).</p></li><li><p>Pasar una estructura <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un <strong>miembro grbit no</strong> válido.</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Se pasó un identificador de configuración regional (LCID) no válido (ya sea a través del miembro <strong>lcid</strong> de la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX al</a> que apunta el <strong>miembro pidxunicode</strong> en la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> o a través del <strong>campo lcid</strong> de la <a href="gg269186(v=exchg.10).md">estructura JET_INDEXCREATE).</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>Se ha especificado un parámetro no válido. Estos son algunos de los motivos posibles:</p><ul><li><p>El <strong>miembro rgcolumncreate</strong> de la <a href="gg269203(v=exchg.10).md">estructura JET_TABLECREATE2</a> es NULL.</p></li><li><p>El <strong>miembro cbStruct</strong> de una de las <a href="gg269252(v=exchg.10).md">estructuras JET_COLUMNCREATE</a> dadas en el miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> no se estableció en sizeof( JET_COLUMNCREATE ).</p></li><li><p>El <strong>miembro cbKey</strong> de una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura está establecido en cero.</p></li><li><p>El <strong>miembro cbStruct</strong> de una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura no se establece en sizeof( JET_INDEXCREATE ).</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>El registro es demasiado grande. La suma del <strong>miembro cbMax</strong> de la <a href="gg269252(v=exchg.10).md">estructura JET_COLUMNCREATE</a> para todas las columnas fijas no debe superar un valor determinado.</p> | 
| <p>JET_errTableDuplicate</p> | <p>La tabla ya existe.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Se intentó agregar demasiadas columnas a la tabla. Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, no más de JET_ccolVarMost columnas de longitud variable y no más de JET_ccolTaggedMost columnas etiquetadas.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Error al intentar normalizar una columna Unicode. Esto puede deberse a que se están quedando sin recursos del sistema.</p> | 



#### <a name="remarks"></a>Observaciones

El nombre **JetCreateTableColumnIndex2** procede del orden de creación de los objetos: primero crea una tabla, columnas y, por último, índices. **JetCreateTableColumnIndex2** crea una tabla con un conjunto inicial de columnas e índices. Se pueden agregar y quitar columnas e índices adicionales dinámicamente con [JetAddColumn,](./jetaddcolumn-function.md) [JetDeleteColumn,](./jetdeletecolumn-function.md) [JetDeleteColumn2,](./jetdeletecolumn2-function.md) [JetCreateIndex,](./jetcreateindex-function.md) [JetCreateIndex2](./jetcreateindex2-function.md)y [JetDeleteIndex.](./jetdeleteindex-function.md)

Al [igual que JetOpenTable,](./jetopentable-function.md)cuando la aplicación se realiza con el *tableid* devuelto, normalmente se debe cerrar [con JetCloseTable.](./jetclosetable-function.md)

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetCreateTableColumnIndex2W</strong> (Unicode) y <strong>JetCreateTableColumnIndex2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_CBTYP](./jet-cbtyp.md)  
[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
