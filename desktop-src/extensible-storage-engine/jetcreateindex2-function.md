---
description: 'Más información acerca de: JetCreateIndex2 (función)'
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
ms.openlocfilehash: 42c1eb8fa1bb7fa880cf7286a1ec472ddc7ba7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716606"
---
# <a name="jetcreateindex2-function"></a>Función JetCreateIndex2


_**Se aplica a:** Windows | Windows Server_

## <a name="jetcreateindex2-function"></a>Función JetCreateIndex2

La función **JetCreateIndex2** crea índices sobre los datos en una base de datos de ese, que se puede usar para buscar datos específicos rápidamente.

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

Contexto de sesión de base de datos que se va a usar para la llamada API.

*TABLEID*

Tabla en la que se creará el índice.

*pindexcreate*

Matriz de estructuras de [JET_INDEXCREATE](./jet-indexcreate-structure.md) , cada una de las cuales define un índice que se va a crear.

*cIndexCreate*

Número de elementos de la matriz *pindexcreate* .

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
<td><p>JET_errCannotIndex</p></td>
<td><p>Se intentó indexar sobre una columna de actualización de custodia o de SLV (tenga en cuenta que las columnas de SLV están desusadas).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Se intentó indizar una columna que no existe. El intento de indizar condicionalmente en una columna que no existe también puede generar este error.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Este error se devolverá si el miembro <strong>ulDensity</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> está establecido en un número inferior a 20 o superior a 100.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>Se ha intentado definir dos índices idénticos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>Se intentó especificar más de un índice principal para una tabla. Una tabla debe tener exactamente un índice principal. Si no se especifica ningún índice principal, el motor de base de datos creará uno de forma transparente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Se especificó una definición de índice no válida. Algunas de las posibles razones para recibir este error son:</p>
<ul>
<li><p>Un índice principal es condicional (el miembro<strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexPrimary establecido y el miembro <strong>cConditionalColumn</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> es mayor que cero).</p></li>
<li><p>Windows Server 2003 y versiones posteriores. Se ha intentado crear un índice de tupla con límites de tupla, pero sin pasar información en el miembro <strong>ptuplelimits</strong> en <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (es decir, <em>grbit</em> JET_bitIndexTupleLimits se ha establecido, pero el puntero <strong>ptuplelimits</strong> es null).</p></li>
<li><p>Pasando una definición de clave no válida en el miembro <strong>szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de las definiciones válidas.</p></li>
<li><p>Establecer el miembro <strong>cbVarSegMac</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para que sea mayor que JET_cbPrimaryKeyMost (para un índice principal) o mayor que JET_cbSecondaryKeyMost (para un índice secundario).</p></li>
<li><p>Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tiene el bit de JET_bitIndexUnicode establecido en el miembro <strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>). Algunas causas comunes pueden ser que el campo pidxunicode de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> sea NULL o que el LCID especificado en la estructura pidxunicode no sea válido.</p></li>
<li><p>Especificar una columna de varios valores para un índice principal.</p></li>
<li><p>Intentando indexar demasiadas columnas condicionales. El miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe ser mayor que JET_ccolKeyMost.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Windows XP y versiones posteriores. Se especificó una estructura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> y no se admiten sus límites. Vea la sección Comentarios de la estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Windows XP y versiones posteriores. Un índice de tupla no puede ser único (<em>grbit</em> no debe tener JET_bitIndexTuples y JET_bitIndexUnique establecer).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Windows XP y versiones posteriores. Un índice de tupla solo puede estar en una sola columna (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexTuples establecido y el miembro <strong>szKey</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especifica más de una columna).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Windows XP y versiones posteriores. Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no debe tener establecido JET_bitIndexPrimary y JET_bitIndexTuples).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP y versiones posteriores. Un índice de tupla solo puede estar en una columna de texto o Unicode. Un intento de indizar otras columnas (por ejemplo, columnas binarias) dará como resultado JET_errIndexTuplesTextColumnsOnly.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP y versiones posteriores. Un índice de tupla no permite establecer el miembro <strong>cbVarSegMac</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Se intentó crear un índice sin información de versión mientras estaba en una transacción.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>La definición del índice no es válida porque el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> contiene valores incoherentes. Algunas de las razones posibles son:</p>
<ul>
<li><p>Un índice principal tenía un bit omitido especificado (JET_bitIndexPrimary se pasó con uno de JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</p></li>
<li><p>Un índice vacío no omite los campos NULOs (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiene JET_bitIndexEmpty establecido, pero no tiene JET_bitIndexIgnoreAnyNull establecida).</p></li>
<li><p>Pasando una estructura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un miembro <strong>grbit</strong> no válido. Vea <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li>
</ul>
<p>Al crear varios índices a la vez (es decir, si el parámetro <em>cIndexCreate</em> es mayor que uno), ninguno de los índices puede contener ninguno de los bits siguientes:</p>
<ul>
<li><p>JET_bitIndexPrimary</p></li>
<li><p>JET_bitIndexUnversioned</p></li>
<li><p>JET_bitIndexEmpty</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Se pasó un ID. de configuración regional (LCID) no válido (ya sea a través del miembro <strong>LCID</strong> en la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que el miembro <strong>pidxunicode</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> contiene un puntero a o a través del miembro <strong>LCID</strong> de la estructura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Se especificó un nombre de índice no válido. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más detalles.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Se pasó un parámetro no válido a la API. Algunas de las razones por las que se puede devolver este error son:</p>
<ul>
<li><p>El campo <strong>cbKey</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> se establece en cero.</p></li>
<li><p>El miembro <strong>cbStruct</strong> de una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> no se establece en sizeof (<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Error al intentar normalizar una columna Unicode. Esto puede deberse a la falta de recursos del sistema.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

El valor devuelto es JET_errSuccess si se completan correctamente todos los índices especificados.

**JetCreateIndex2** recorre en iteración los índices proporcionados en **pindexcreate** y a veces se anulará en el primer error. Es posible que no se haya intentado ningún índice después del primer índice con un error, aunque el miembro **Err** de la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) contiene JET_errSuccess.

#### <a name="requirements"></a>Requisitos

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
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetCreateIndex2W</strong> (Unicode) y <strong>JetCreateIndex2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
