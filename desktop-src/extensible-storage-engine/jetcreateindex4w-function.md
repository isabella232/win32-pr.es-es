---
description: 'Más información acerca de: JetCreateIndex4W (función)'
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
ms.openlocfilehash: 9a4c7671cbe361b6214552f4c611cd1706c0e48d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716605"
---
# <a name="jetcreateindex4w-function"></a>Función JetCreateIndex4W


_**Se aplica a:** Windows | Windows Server_

La función **JetCreateIndex4W** crea índices sobre los datos en una base de datos del motor de almacenamiento extensible (ese), que se puede usar para buscar datos específicos rápidamente.

La función **JetCreateIndex4W** se presentó en el sistema operativo Windows 8.

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

Contexto de sesión de base de datos que se va a usar para la llamada API.

*TABLEID*

Tabla en la que se creará el índice.

*pindexcreate*

Matriz de estructuras de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , cada una de las cuales define un índice que se va a crear.

*cIndexCreate*

Número de elementos de la matriz *pindexcreate* .

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

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
<td><p>Se intentó indizar una columna que no existe. Un intento de indexación condicional de una columna no existente también puede generar este error.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Este error se devolverá si el miembro <strong>ulDensity</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> está establecido en un número menor que 20 o mayor que 100.</p></td>
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
<td><p>Se especificó una definición de índice no válida. A continuación se indican algunas de las razones posibles de este error:</p>
<ul>
<li><p>Un índice principal es condicional (el miembro<strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene <strong>JET_bitIndexPrimary</strong> establecido y el miembro <strong>cConditionalColumn</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> es mayor que cero).</p></li>
<li><p>Se aplica a las versiones de Windows a partir de Windows Server 2003. Se intentó crear un índice de tupla con límites de tupla, pero sin pasar información en el miembro <strong>ptuplelimits</strong> en <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (es decir, <em>grbit</em> se ha establecido <strong>JET_bitIndexTupleLimits</strong> , pero el puntero <strong>ptuplelimits</strong> es null).</p></li>
<li><p>Pasando una definición de clave no válida en el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Para obtener información sobre las definiciones válidas, vea <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li>
<li><p>Establecer el miembro <strong>cbVarSegMac</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para que sea mayor que <strong>JET_cbPrimaryKeyMost</strong> (para un índice principal) o mayor que <strong>JET_cbSecondaryKeyMost</strong> (para un índice secundario).</p></li>
<li><p>Pasar una combinación no válida para un índice Unicode definido por el usuario (uno que tiene el bit de <strong>JET_bitIndexUnicode</strong> establecido en el miembro <strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>). Algunas causas comunes pueden ser que el campo pidxunicode de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> sea NULL o que el LCID especificado en la estructura pidxunicode no sea válido.</p></li>
<li><p>Especificar una columna multivalor para un índice principal.</p></li>
<li><p>Intentando indexar demasiadas columnas condicionales. El miembro <strong>cConditionalColumn</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe ser mayor que <strong>JET_ccolKeyMost</strong>.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Se aplica a las versiones de Windows a partir de Windows XP. Se especificó una estructura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> y no se admiten sus límites. Para obtener más información, vea la sección Comentarios de la estructura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla no puede ser único (<em>grbit</em> no debe tener <strong>JET_bitIndexTuples</strong> y <strong>JET_bitIndexUnique</strong> establecer).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla solo puede estar en una sola columna (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene <strong>JET_bitIndexTuples</strong> establecido y el miembro <strong>szKey</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica más de una columna).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla no puede ser un índice principal (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no debe tener establecido <strong>JET_bitIndexPrimary</strong> y <strong>JET_bitIndexTuples</strong> ).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla solo puede estar en una columna de texto o Unicode. Un intento de indizar otras columnas (por ejemplo, columnas binarias) dará como resultado <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Se aplica a las versiones de Windows a partir de Windows XP. Un índice de tupla no permite establecer el miembro <strong>cbVarSegMac</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Se intentó crear un índice sin información de versión mientras estaba en una transacción.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>La definición del índice no es válida porque el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene valores incoherentes. A continuación se indican algunas razones posibles:</p>
<ul>
<li><p>Un índice principal tenía un bit omitido especificado (JET_bitIndexPrimary se pasó con uno de <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>o <strong>JET_bitIndexIgnoreFirstNull</strong>).</p></li>
<li><p>Un índice vacío no omite los campos nulos (es decir, el miembro <strong>grbit</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiene <strong>JET_bitIndexEmpty</strong> establecido, pero no tiene <strong>JET_bitIndexIgnoreAnyNull</strong> establecida).</p></li>
<li><p>Pasando una estructura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un miembro <strong>grbit</strong> no válido. Vea <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li>
</ul>
<p>Al crear varios índices a la vez (es decir, si el parámetro <em>cIndexCreate</em> es mayor que uno), ninguno de los índices puede contener ninguno de los bits siguientes:</p>
<ul>
<li><p><strong>JET_bitIndexPrimary</strong></p></li>
<li><p><strong>JET_bitIndexUnversioned</strong></p></li>
<li><p><strong>JET_bitIndexEmpty</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Se pasó un ID. de configuración regional (LCID) no válido (ya sea a través del miembro <strong>LCID</strong> en la estructura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que el miembro <strong>pidxunicode</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene un puntero a o a través del miembro <strong>LCID</strong> de la estructura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Se especificó un nombre de índice no válido. Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obtener más detalles.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Se pasó un parámetro no válido a la API. A continuación se indican algunos de los motivos por los que se puede devolver este error:</p>
<ul>
<li><p>El campo <strong>cbKey</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> se establece en cero.</p></li>
<li><p>El miembro <strong>cbStruct</strong> de una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> no se establece en sizeof (JET_INDEXCREATE2).</p></li>
</ul></td>
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

La función **JetCreateIndex4W** recorre en iteración los índices especificados en el parámetro *pindexcreate* y a veces se anulará en el primer error. Es posible que no se haya intentado ningún índice después del primer índice con un error, aunque el miembro **Err** de la estructura [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contiene JET_errSuccess.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2012.</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>Vea también

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
