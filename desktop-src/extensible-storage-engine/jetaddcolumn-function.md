---
description: 'Más información acerca de: JetAddColumn (función)'
title: Función JetAddColumn
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b8c3eac113daeae43ec4a8e62b7fcda9ddbf9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720670"
---
# <a name="jetaddcolumn-function"></a>Función JetAddColumn


_**Se aplica a:** Windows | Windows Server_

## <a name="jetaddcolumn-function"></a>Función JetAddColumn

La función **JetAddColumn** agrega una nueva columna a una tabla existente en una base de datos ese.

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se va a usar para la llamada API.

*TABLEID*

Tabla a la que se va a agregar la columna.

*szColumnName*

Nombre de la columna que se va a agregar. El nombre debe cumplir los siguientes criterios:

  - Debe tener menos de JET_cbNameMost caracteres de longitud, sin incluir el carácter **null** de terminación.

  - Solo debe contener caracteres de los siguientes conjuntos: de 0 a 9, de la a a la Z, de la a a la z y de todos los demás signos de puntuación, excepto el signo de exclamación ( \! ), la coma (,), el corchete de apertura () y el \[ corchete de cierre ( \] ), es decir, los caracteres ASCII 0x20, 0x22 a

  - No puede comenzar con un espacio.

  - Debe contener al menos un carácter que no sea un espacio.

*pcolumndef*

Puntero a una estructura de [JET_COLUMNDEF](./jet-columndef-structure.md) , que define los datos que se pueden almacenar en una columna.

*pvDefault*

Un puntero a un búfer que contiene el valor predeterminado de la columna. La longitud del búfer es **cbDefault**. Si no hay ningún valor predeterminado, establezca **pvDefault** en **null** y **cbDefault** en cero. Los valores predeterminados no pueden ser mayores que JET_cbColumnMost bytes para las columnas fijas o JET_cbLVDefaultValueMost bytes para valores largos. Si un valor predeterminado es mayor que, se truncará en modo silencioso.

Si *grbit* ha establecido JET_bitColumnUserDefinedDefault, **pvDefault** se interpretará como un puntero a una estructura de [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) .

*cbDefault*

Tamaño, en bytes, del búfer que se especifica en **pvDefault**.

*pcolumnid*

Puntero a una estructura de [JET_COLUMNID](./jet-columnid.md) , que, si se ejecuta correctamente, recibirá el identificador de la columna recién creada. En caso de error, el valor es indefinido.

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
<td><p>La operación se realizó correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedDDL</p></td>
<td><p>Se intentó modificar la definición de datos de una tabla de DDL fija. Un ejemplo de una tabla con DDL fijos es una tabla de plantillas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Se pasó un parámetro no válido a la API. Algunos ejemplos de parámetros no válidos son:</p>
<ul>
<li><p>Se pasa el tamaño incorrecto de la estructura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> en su miembro <em>cbStruct</em> .</p></li>
<li><p>Pasar JET_bitColumnUserDefinedDefault, pero no establecer <strong>cbDefault</strong> en sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Se intentó agregar una columna con el conjunto de JET_bitColumnUnversioned bits, pero la sesión se encuentra actualmente en una transacción.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Ya existe una columna. Se intentó agregar una columna sin información de versión y esa columna ya existe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableNotEmpty</p></td>
<td><p>La tabla contiene datos. Una columna de actualización de custodia solo puede agregarse a una tabla vacía.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>El registro es demasiado grande. La suma del parámetro <strong>cbMax</strong> para las columnas fijas no debe superar un valor determinado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Se intentó agregar demasiadas columnas a la tabla. Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Se intentó agregar una columna redundante. No debe haber más de una columna de incremento automático y no más de una columna de versión por tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>No se pudo resolver la función de devolución de llamada. Es posible que no se haya encontrado el archivo DLL o que no se haya encontrado la función del archivo DLL. El registro de eventos proporcionará más detalles si está habilitado el registro suficiente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>ADVERTENCIA que indica que la longitud máxima (<strong>cbMax</strong>) de una columna fija o de variable era mayor que JET_cbColumnMost. Este límite no se aplica a los valores largos (es decir <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> y <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Se pasó un nombre no válido como <strong>szColumnName</strong>. Para obtener más información sobre las restricciones, vea los criterios de <strong>szColumnName</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>El campo <strong>coltyp</strong> no se estableció en un tipo de columna válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>El parámetro <strong>CP</strong> de la estructura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se estableció en una página de códigos válida. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaggedNotNULL</p></td>
<td><p>No se puede usar JET_bitColumnNotNULL con columnas etiquetadas, de valor Long o de SLV.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Se especificó una combinación no válida de <em>grbits</em> . Algunos de los motivos de este error son:</p>
<ul>
<li><p>JET_bitColumnFixed se usó en una columna etiquetada, un valor largo o SLV.</p></li>
<li><p>JET_bitColumnEscrowUpdate se usó en una columna que no era de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li>
<li><p>JET_bitColumnEscrowUpdate se usó en una columna de versión (JET_bitColumnVersion).</p></li>
<li><p>JET_bitColumnEscrowUpdate se usó en una columna AutoIncrememnt (JET_bitColumnAutoincrement).</p></li>
<li><p>JET_bitColumnEscrowUpdate se usó en una columna que no tenía un valor predeterminado (<strong>cbDefault</strong> era igual a cero).</p></li>
<li><p>JET_bitColumnFinalize se usó en una columna que no era una columna de actualización de custodia (no se estableció JET_bitColumnEscrowUpdate).</p></li>
<li><p>JET_bitColumnDeleteOnZero se usó en una columna que no era una columna de actualización de custodia (no se estableció JET_bitColumnEscrowUpdate).</p></li>
<li><p>JET_bitColumnAutoincrement se usó en una columna que no se <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p>
<p><strong>Windows 2000:  </strong> Este motivo del código de error solo se utiliza en Windows 2000.</p>
<p>JET_bitColumnAutoincrement se usó en una columna que no era <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> ni <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</p>
<p><strong>Windows XP:  </strong> Este motivo del código de error se utiliza en Windows XP y en los sistemas operativos posteriores.</p></li>
<li><p>JET_bitColumnVersion se usó en una columna que no se <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li>
<li><p>JET_bitColumnVersion se usó en una columna de incremento automático.</p></li>
<li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnFixed.</p></li>
<li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnNotNULL.</p></li>
<li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnVersion.</p></li>
<li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnAutoincrement.</p></li>
<li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnUpdatable.</p></li>
<li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnEscrowUpdate.</p></li>
<li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnFinalize.</p></li>
<li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnDeleteOnZero.</p></li>
<li><p>JET_bitColumnUserDefinedDefault se usó junto con JET_bitColumnMaybeNull.</p></li>
<li><p>JET_bitColumnUserDefinedDefault se usó en una columna no etiquetada (que es fija o variable).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged</p></td>
<td><p>Una columna con varios valores (JET_bitColumnMultiValued) solo se puede usar en una columna de valor largo o etiquetado (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged</p></td>
<td><p>Se intentó utilizar una columna etiquetada cuando es posible que la columna no esté etiquetada. Algunas de las restricciones para impedir las columnas etiquetadas son:</p>
<ul>
<li><p>No se puede usar una columna de actualización de custodia (JET_bitColumnEscrowUpdate) en una columna de valor largo o etiquetado (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></li>
<li><p>Es posible que una columna de incremento automático no esté etiquetada.</p></li>
<li><p>Es posible que una columna de versión no esté etiquetada.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired</p></td>
<td><p>Se requiere un bloqueo exclusivo en la tabla para esta operación.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>ADVERTENCIA que indica que la longitud máxima (<em>cbMax</em>) de una columna fija o de variable era mayor que JET_cbColumnMost. Este límite no se aplica a los valores largos (es decir <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> y <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
</tbody>
</table>


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
<td><p>Se implementa como <strong>JetAddColumnW</strong> (Unicode) y <strong>JetAddColumnA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
