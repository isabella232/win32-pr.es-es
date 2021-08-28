---
description: 'Más información sobre: JetCreateTable (Función)'
title: Función JetCreateTable
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e06e4c2d0cfa55ff85279b634449fd313eb7570
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985028"
---
# <a name="jetcreatetable-function"></a>Función JetCreateTable


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcreatetable-function"></a>Función JetCreateTable

La **función JetCreateTable** crea una tabla vacía en una base de datos ese.

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará.

*Dbid*

Identificador de base de datos que se usará.

*szTableName*

Nombre del índice que se creará.

El nombre debe tener el formato según las reglas siguientes:

  - Ser menor que JET_cbNameMost, sin incluir el valor NULL final.

  - Debe tener el siguiente conjunto de caracteres: de 0 a 9, de A a Z, de a a z y de todos los demás signos de puntuación excepto " \! " (signo de exclamación), "," (coma), " " (corchete de apertura) y " " (corchete de cierre), es decir, caracteres \[ \] ASCII 0x20, 0x22 a través de 0x2d, 0x2f a través de 0x5a, 0x5c, 0x5d a 0x7f.

  - No comience con un espacio.

  - Estar hecho de al menos un carácter que no sea de espacio.

*lPages*

Número inicial de páginas de base de datos que se asignarán a la tabla. Especificar un número mayor que uno puede reducir la fragmentación si se insertan muchas filas en esta tabla.

*lDensity*

Densidad de tabla, en puntos porcentuales. El número debe ser 0 o estar entre 20 y 100. Pasar 0 significa que se debe usar el valor predeterminado. El valor predeterminado es 80.

*ptableid*

Si se ejecuta correctamente, el identificador de tabla se devuelve en este campo. El valor no está definido si la API no devuelve JET_errSuccess.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>No se pudo resolver la función de devolución de llamada. Es posible que no se haya encontrado el archivo DLL o que la función del archivo DLL no se haya encontrado. Con el registro suficiente habilitado, el registro de eventos proporcionará más detalles.</p> | 
| <p>JET_errCannotIndex</p> | <p>Se intentó indexar sobre una columna de actualización de custodia o SLV (tenga en cuenta que las columnas SLV están en desuso).</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Si ptablecreate- &gt; grbit especifica JET_bitTableCreateTemplateTable, pero ptablecreate- &gt; szTemplateTableName se establece en NULL.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Ya existe una columna.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Se intentó indexar sobre una columna inexistente. El intento de indexar condicionalmente una columna inexistente también puede producir este error.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Se intentó agregar una columna redundante. No debería haber más de una columna de autoincremento y no más de una columna de versión por tabla.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Se pasó una densidad no válida en el <em>miembro ulDensity</em> en la <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> estructura.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Significa que la tabla denominada en el miembro <strong>szTemplateTableName</strong> de la estructura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> no estaba marcada como una tabla de plantilla (es decir, esa tabla no tenía JET_bitTableCreateTemplateTable establecido).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Se intentó definir dos índices idénticos.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Se intentó especificar más de un índice principal para una tabla. Una tabla debe tener exactamente un índice principal. Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Se especificó una definición de índice no válida. Algunas de las posibles razones para recibir este error son:</p><ul><li><p>Un índice principal es condicional (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene un conjunto JET_bitIndexPrimary y el miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es mayor que cero).</p></li><li><p>Windows Server 2003 y versiones posteriores. Intentando crear un índice de tupla con límites de tupla, pero sin pasar el miembro <strong>ptuplelimits</strong> en la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexTupleLimits establecido, pero el <strong>puntero ptuplelimits</strong> es NULL).</p></li><li><p>Pasar una definición de clave no válida en el <strong>miembro szKey</strong> de <a href="gg269186(v=exchg.10).md">la JET_INDEXCREATE</a> estructura. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una explicación de las definiciones válidas.</p></li><li><p>Establecer el <strong>miembro cbVarSegMac</strong> en <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> sea mayor que JET_cbPrimaryKeyMost (para un índice principal) o mayor que JET_cbSecondaryKeyMost (para un índice secundario).</p></li><li><p>Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tenga el bit JET_bitIndexUnicode establecido en el miembro <strong>grbit</strong> <a href="gg269186(v=exchg.10).md">de JET_INDEXCREATE</a>). Algunas causas comunes incluyen el <strong>miembro pidxunicode</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es NULL o el LCID especificado en la estructura <strong>pidxunicode</strong> no es válido.</p></li><li><p>Especificar una columna con varios valores para un índice principal.</p></li><li><p>Intentando indexar demasiadas columnas condicionales. El <strong>miembro cConditionalColumn</strong> de la <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura no debe ser mayor que JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP y versiones posteriores. Se <a href="gg269207(v=exchg.10).md">especificó JET_TUPLELIMITS</a> estructura y no se admiten sus límites. Consulte la sección de comentarios de la <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> estructura.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP y versiones posteriores. Un índice de tupla no puede ser único (es decir, el miembro <em>grbit</em> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener JET_bitIndexPrimary y JET_bitIndexUnique conjunto).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP y versiones posteriores. Un índice de tupla solo puede estar sobre una sola columna (es decir, si el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene un conjunto de JET_bitIndexTuples y el miembro <strong>szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especifica más de una columna).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP y versiones posteriores. Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener tanto JET_bitIndexPrimary como JET_bitIndexTuples conjunto).</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP y versiones posteriores. Un índice de tupla no permite establecer el <strong>miembro cbVarSegMac</strong> de <a href="gg269186(v=exchg.10).md">la JET_INDEXCREATE</a> estructura.</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP y versiones posteriores. Un índice de tupla solo puede estar en una columna de texto o Unicode. Un intento de indexar otras columnas (por ejemplo, columnas binarias) dará lugar a JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errInTransaction</p> | <p>Se intentó crear un índice sin información de versión mientras se encontraba en una transacción.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>El <strong>miembro cp</strong> de la <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> estructura no se estableció en una página de códigos válida. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de 0 significa que se usará el valor predeterminado (inglés, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>El <strong>miembro coltyp</strong> de la <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> estructura no se estableció en un tipo de columna válido.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Algunas de las razones por las que se puede producir este error:</p><ul><li><p>El <strong>miembro rgindexcreate</strong> de la <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> estructura se estableció en NULL.</p></li><li><p>El <strong>miembro rgcolumncreate</strong> de la <a href="gg269203(v=exchg.10).md">estructura JET_TABLECREATE2</a> se estableció en NULL.</p></li><li><p>El <strong>miembro cbStruct</strong> de una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura no se estableció en un valor válido.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>Se especificó una combinación no válida de miembros <strong>grbit</strong> <a href="gg294146(v=exchg.10).md">en JET_TABLECREATE</a> o <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</p><p>La definición del índice no es válida porque el <strong>miembro grbit</strong> contiene valores incoherentes. Estos son algunos de los motivos posibles:</p><ul><li><p>Un índice principal tenía especificado un bit de ignore (es decir, JET_bitIndexPrimary se pasó con JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</p></li><li><p>Un índice vacío no omite ningún miembro NULL (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexEmpty establecido, pero no tiene JET_bitIndexIgnoreAnyNull establecido).</p></li><li><p>Pasar una estructura <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un <strong>miembro grbit no</strong> válido.</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Se pasó un identificador de configuración regional (LCID) no válido (ya sea a través del miembro <strong>lcid</strong> de la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX al</a> que apunta el <strong>miembro pidxunicode</strong> en la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> o a través del <strong>campo lcid</strong> de la <a href="gg269186(v=exchg.10).md">estructura JET_INDEXCREATE).</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>Se ha especificado un parámetro no válido. Estos son algunos de los motivos posibles:</p><ul><li><p>El <strong>miembro rgcolumncreate</strong> de la <a href="gg269203(v=exchg.10).md">estructura JET_TABLECREATE2</a> es NULL.</p></li><li><p>El <strong>miembro cbStruct</strong> de una de las <a href="gg269252(v=exchg.10).md">estructuras JET_COLUMNCREATE</a> dadas en el miembro <strong>rgcolumncreate</strong> de la estructura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> no se estableció en sizeof( JET_COLUMNCREATE ).</p></li><li><p>El <strong>miembro cbKey</strong> de una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura está establecido en cero.</p></li><li><p>El <strong>miembro cbStruct</strong> de <a href="gg269186(v=exchg.10).md">una JET_INDEXCREATE</a> estructura no se establece en sizeof( JET_INDEXCREATE ).</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>El registro es demasiado grande. La suma del <strong>miembro cbMax</strong> de la <a href="gg269252(v=exchg.10).md">estructura JET_COLUMNCREATE</a> para todas las columnas fijas no debe superar un valor determinado.</p> | 
| <p>JET_errTableDuplicate</p> | <p>La tabla ya existe.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Se intentó agregar demasiadas columnas a la tabla. Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, no más de JET_ccolVarMost columnas de longitud variable y no más de JET_ccolTaggedMost columnas etiquetadas.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Error al intentar normalizar una columna Unicode. Esto puede deberse a que se están quedando sin recursos del sistema.</p> | 



#### <a name="remarks"></a>Observaciones

**JetCreateTable** crea una tabla que no contiene ninguna columna. Para agregar columnas, consulte [JetAddColumn](./jetaddcolumn-function.md).

Internamente, **JetCreateTable** llama a [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), rellenando [una JET_TABLECREATE2](./jet-tablecreate2-structure.md) estructura con:

  - JET_TABLECREATE2.cbStruct = sizeof( JET_TABLECREATE2 )

  - JET_TABLECREATE2.szTableName = szTableName

  - JET_TABLECREATE2.ulPages = lPage

  - JET_TABLECREATE2.ulDensity = lDensity

  - JET_TABLECREATE2.tableid = JET_tableidNil

Todos los demás campos de la estructura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) interno se establecen en cero o NULL. En la salida, *ptableid* se establecerá en JET_TABLECREATE2.tableid.

Consulte [JetCreateTableColumnIndex2 para](./jetcreatetablecolumnindex2-function.md) obtener más detalles.

Al [igual que JetOpenTable,](./jetopentable-function.md)cuando la aplicación se realiza mediante el miembro **tableid** devuelto de la [estructura JET_TABLECREATE2,](./jet-tablecreate2-structure.md) normalmente se debe cerrar con [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetCreateTableW</strong> (Unicode) y <strong>JetCreateTableA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
