---
description: 'Más información sobre: JetCreateIndex2 (Función)'
title: Función JetCreateIndex2
TOCTitle: JetCreateIndex2 Function
ms:assetid: 8810eaed-40cb-4561-aafc-9a9bbdb0d05b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269324(v=EXCHG.10)
ms:contentKeyID: 32765614
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex2W
- JetCreateIndex2A
- JetCreateIndex2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 849caa4e52d2c07f06bded436ff22628fd427784
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475861"
---
# <a name="jetcreateindex2-function"></a>Función JetCreateIndex2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcreateindex2-function"></a>Función JetCreateIndex2

La **función JetCreateIndex2** crea índices sobre los datos de una base de datos ESE, que se pueden usar para buscar datos específicos rápidamente.

```cpp
    JET_ERR JET_API JetCreateIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Tabla en la que se creará el índice.

*pindexcreate*

Matriz de [JET_INDEXCREATE](./jet-indexcreate-structure.md) estructura, cada una de las cuales define un índice que se va a crear.

*cIndexCreate*

Número de elementos de la matriz *pindexcreate.*

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errCannotIndex</p> | <p>Se intentó indexar sobre una columna SLV o de actualización de custodia (tenga en cuenta que las columnas SLV están en desuso).</p> | 
| <p>JET_errColumnNotFound</p> | <p>Se intentó indexar sobre una columna inexistente. El intento de indexar condicionalmente una columna inexistente también puede producir este error.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Este error se devolverá si el <strong>miembro ulDensity</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> está establecido en un número menor que 20 o más de 100.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Se intentó definir dos índices idénticos.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Se intentó especificar más de un índice principal para una tabla. Una tabla debe tener exactamente un índice principal. Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Se especificó una definición de índice no válida. Algunos de los posibles motivos para recibir este error son:</p><ul><li><p>Un índice principal es condicional (el miembro<strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexPrimary establecido y el <strong>miembro cConditionalColumn</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es mayor que cero).</p></li><li><p>Windows Server 2003 y versiones posteriores. Intentando crear un índice de tupla con límites de tupla, pero sin pasar información en el miembro <strong>ptuplelimits</strong> en <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (es decir, <em>grbit</em> tiene JET_bitIndexTupleLimits establecido, pero el <strong>puntero ptuplelimits</strong> es NULL).</p></li><li><p>Pasar una definición de clave no válida en <strong>el miembro szKey</strong> de la <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una explicación de las definiciones válidas.</p></li><li><p>Establecer el <strong>miembro cbVarSegMac</strong> en <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> sea mayor que JET_cbPrimaryKeyMost (para un índice principal) o mayor que JET_cbSecondaryKeyMost (para un índice secundario).</p></li><li><p>Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tenga el bit JET_bitIndexUnicode establecido en el <strong>miembro grbit</strong> <a href="gg269186(v=exchg.10).md">de JET_INDEXCREATE</a>). Algunas causas comunes pueden ser que el campo pidxunicode de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es NULL o que el LCID especificado en la estructura pidxunicode no es válido.</p></li><li><p>Especificar una columna con varios valores para un índice principal.</p></li><li><p>Intentando indexar demasiadas columnas condicionales. El <strong>miembro cConditionalColumn</strong> de la <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura no debe ser mayor que JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP y versiones posteriores. Se <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> estructura de la base de datos y no se admiten sus límites. Consulte la sección comentarios de la <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> estructura.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP y versiones posteriores. Un índice de tupla no puede ser único<em>(grbit</em> no debe tener JET_bitIndexTuples y JET_bitIndexUnique establecido).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP y versiones posteriores. Un índice de tupla solo puede estar sobre una sola columna (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene un conjunto de JET_bitIndexTuples y el <strong>miembro szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especifica más de una columna).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP y versiones posteriores. Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener tanto JET_bitIndexPrimary como JET_bitIndexTuples establecido).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP y versiones posteriores. Un índice de tupla solo puede estar en una columna de texto o Unicode. Un intento de indexar otras columnas (por ejemplo, columnas binarias) dará lugar a JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP y versiones posteriores. Un índice de tupla no permite establecer el <strong>miembro cbVarSegMac</strong> de <a href="gg269186(v=exchg.10).md">la JET_INDEXCREATE</a> estructura.</p> | 
| <p>JET_errInTransaction</p> | <p>Se intentó crear un índice sin información de versión mientras estaba en una transacción.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>La definición del índice no es válida porque el <strong>miembro grbit</strong> de la <a href="gg269186(v=exchg.10).md">estructura JET_INDEXCREATE</a> contiene valores incoherentes. Algunos posibles motivos son:</p><ul><li><p>Se especificó un bit de ignore en un índice principal (JET_bitIndexPrimary se pasó con uno de JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</p></li><li><p>Un índice vacío no omite ningún campo NULL (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexEmpty establecido, pero no tiene JET_bitIndexIgnoreAnyNull establecido).</p></li><li><p>Pasar una estructura <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un <strong>miembro grbit no</strong> válido. Vea <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>Al crear varios índices a la vez (es decir, si el parámetro <em>cIndexCreate</em> es mayor que uno), ninguno de los índices puede contener ninguno de los siguientes bits:</p><ul><li><p>JET_bitIndexPrimary</p></li><li><p>JET_bitIndexUnversioned</p></li><li><p>JET_bitIndexEmpty</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Se pasó un identificador de configuración regional (LCID) no válido (ya sea a través del miembro <strong>lcid</strong> de la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX,</a> que el <strong>miembro pidxunicode</strong> de la estructura JET_INDEXCREATE contiene un puntero <a href="gg269186(v=exchg.10).md">a</a> o a través del <strong>miembro lcid</strong> de la <a href="gg269186(v=exchg.10).md">estructura JET_INDEXCREATE).</a></p> | 
| <p>JET_errInvalidName</p> | <p>Se especificó un nombre de índice no válido. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más detalles.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Se pasó un parámetro no válido a la API. Algunas de las razones por las que se puede devolver este error son:</p><ul><li><p>El <strong>campo cbKey</strong> de una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura está establecido en cero.</p></li><li><p>El <strong>miembro cbStruct</strong> de una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura no se establece en sizeof(<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Error al intentar normalizar una columna Unicode. Esto puede deberse a que se están quedando sin recursos del sistema.</p> | 



#### <a name="remarks"></a>Comentarios

El valor devuelto se JET_errSuccess la finalización correcta de todos los índices especificados.

**JetCreateIndex2** recorre en iteración los índices dados en **pindexcreate** y, a veces, se anula en el primer error. Es posible que no se hayan intentado los índices después del primer índice con un error, aunque el miembro **err** de la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) contiene JET_errSuccess.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetCreateIndex2W</strong> (Unicode) y <strong>JetCreateIndex2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
