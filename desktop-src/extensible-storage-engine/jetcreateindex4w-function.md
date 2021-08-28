---
description: 'Más información sobre: JetCreateIndex4W (Función)'
title: Función JetCreateIndex4W
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c79f1638645f0dcd7e4306f543a9ee15b9668843
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987448"
---
# <a name="jetcreateindex4w-function"></a>Función JetCreateIndex4W


_**Se aplica a:** Windows | Windows Servidor_

La **función JetCreateIndex4W** crea índices sobre datos en una base de datos extensible Storage Engine (ESE), que se puede usar para buscar datos específicos rápidamente.

La **función JetCreateIndex4W** se introdujo en el Windows 8 operativo.

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Tabla en la que se creará el índice.

*pindexcreate*

Matriz de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) estructura, cada una de las cuales define un índice que se va a crear.

*cIndexCreate*

Número de elementos de la matriz *pindexcreate.*

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los códigos de retorno enumerados en la tabla siguiente. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errCannotIndex</p> | <p>Se intentó indexar sobre una columna SLV o de actualización de custodia (tenga en cuenta que las columnas SLV están en desuso).</p> | 
| <p>JET_errColumnNotFound</p> | <p>Se intentó indexar sobre una columna inexistente. Un intento de indexar condicionalmente sobre una columna inexistente también puede producir este error.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Este error se devolverá si el <strong>miembro ulDensity</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> está establecido en un número menor que 20 o mayor que 100.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Se intentó definir dos índices idénticos.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Se intentó especificar más de un índice principal para una tabla. Una tabla debe tener exactamente un índice principal. Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Se especificó una definición de índice no válida. Estas son algunas de las posibles razones de este error:</p><ul><li><p>Un índice principal es condicional (el miembro<strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene JET_bitIndexPrimary <strong>establecido</strong> y el miembro <strong>cConditionalColumn</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> es mayor que cero).</p></li><li><p>Se aplica a las versiones de Windows a partir de Windows Server 2003. Se intentó crear un índice de tupla con límites de tupla, pero sin pasar información en el miembro <strong></strong> <strong>ptuplelimits</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (es decir, <em>grbit</em> tiene un conjunto de JET_bitIndexTupleLimits, pero el <strong>puntero ptuplelimits</strong> es null).</p></li><li><p>Pasar una definición de clave no válida en el <strong>miembro szKey</strong> de la <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> estructura. Para obtener información sobre las definiciones válidas, <a href="gg294082(v=exchg.10).md">vea JET_INDEXCREATE2</a>.</p></li><li><p>Establecer el <strong>miembro cbVarSegMac</strong> en <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> sea mayor que <strong>JET_cbPrimaryKeyMost</strong> (para un índice principal) o mayor que <strong>JET_cbSecondaryKeyMost</strong> (para un índice secundario).</p></li><li><p>Pasar una combinación no válida para un índice Unicode <strong></strong> definido por el usuario (que tiene el bit JET_bitIndexUnicode establecido en el <strong>miembro grbit</strong> <a href="gg294082(v=exchg.10).md">de JET_INDEXCREATE2</a>). Algunas causas comunes pueden ser que el campo pidxunicode de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> sea NULL o que el LCID especificado en la estructura pidxunicode no sea válido.</p></li><li><p>Especificar una columna de varios valores para un índice principal.</p></li><li><p>Intentando indexar demasiadas columnas condicionales. El <strong>miembro cConditionalColumn</strong> de la <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> estructura no debe ser mayor <strong>que JET_ccolKeyMost</strong>.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Se aplica a las versiones de Windows a partir de Windows XP. Se <a href="gg269207(v=exchg.10).md">especificó JET_TUPLELIMITS</a> estructura y no se admiten sus límites. Para obtener más información, vea la sección comentarios de la <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> estructura.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla no puede ser único<em>(grbit</em> no debe tener <strong>JET_bitIndexTuples</strong> ni <strong>JET_bitIndexUnique</strong> establecido).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla solo puede estar <strong>sobre</strong> una sola columna (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene un conjunto de JET_bitIndexTuples y el <strong>miembro szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica más de una columna).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla no puede ser un índice principal (es decir, el <strong></strong> miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe tener tanto JET_bitIndexPrimary como <strong>JET_bitIndexTuples</strong> establecido).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla solo puede estar en una columna de texto o Unicode. Un intento de indexar otras columnas (por ejemplo, columnas binarias) dará lugar a <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla no permite establecer el <strong>miembro cbVarSegMac</strong> de <a href="gg294082(v=exchg.10).md">la JET_INDEXCREATE2</a> estructura.</p> | 
| <p>JET_errInTransaction</p> | <p>Se intentó crear un índice sin información de versión mientras estaba en una transacción.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>La definición del índice no es válida porque el <strong>miembro grbit</strong> de la <a href="gg294082(v=exchg.10).md">estructura JET_INDEXCREATE2</a> contiene valores incoherentes. Estas son algunas de las posibles razones:</p><ul><li><p>Un índice principal tenía especificado un bit de ignore (JET_bitIndexPrimary se pasó con uno de JET_bitIndexIgnoreNull <strong>,</strong> <strong>JET_bitIndexIgnoreAnyNull</strong>o <strong>JET_bitIndexIgnoreFirstNull</strong>).</p></li><li><p>Un índice vacío no omite los campos null (es decir, el <strong></strong> miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene un JET_bitIndexEmpty establecido, pero no <strong>tiene JET_bitIndexIgnoreAnyNull</strong> establecido).</p></li><li><p>Pasar una estructura <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un <strong>miembro grbit no</strong> válido. Vea <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>Al crear varios índices a la vez (es decir, si el parámetro <em>cIndexCreate</em> es mayor que uno), ninguno de los índices puede contener ninguno de los siguientes bits:</p><ul><li><p><strong>JET_bitIndexPrimary</strong></p></li><li><p><strong>JET_bitIndexUnversioned</strong></p></li><li><p><strong>JET_bitIndexEmpty</strong></p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Se pasó un identificador de configuración regional (LCID) no válido (ya sea a través del miembro <strong>lcid</strong> de la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX,</a> al que el miembro <strong>pidxunicode</strong> de la estructura JET_INDEXCREATE2 contiene un puntero <a href="gg294082(v=exchg.10).md">o</a> a través del <strong>miembro lcid</strong> de la <a href="gg294082(v=exchg.10).md">estructura JET_INDEXCREATE2).</a></p> | 
| <p>JET_errInvalidName</p> | <p>Se especificó un nombre de índice no válido. Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obtener más detalles.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Se pasó un parámetro no válido a la API. Estas son algunas de las razones por las que se puede devolver este error:</p><ul><li><p>El <strong>campo cbKey</strong> de una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> estructura está establecido en cero.</p></li><li><p>El <strong>miembro cbStruct</strong> de una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> estructura no se establece en sizeof(JET_INDEXCREATE2).</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Error al intentar normalizar una columna Unicode. Esto puede deberse a que se están quedando sin recursos del sistema.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Un elemento de la estructura de sugerencias de espacio JET no era correcto o utilizable.</p> | 



#### <a name="remarks"></a>Observaciones

La **función JetCreateIndex4W** recorre en iteración los índices especificados en el *parámetro pindexcreate* y, a veces, se anula en el primer error. Es posible que no se haya intentado ningún índice después del primer índice con un error, aunque el miembro **err** de la estructura [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contiene JET_errSuccess.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JET_SPACEHINTS](./jet-spacehints-structure.md)
