---
description: 'Más información acerca de: JetRenameColumn (función)'
title: JetRenameColumn función)
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ab2dee1895e4148bb2ea0600464d7e9c4a6a358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707020"
---
# <a name="jetrenamecolumn-function"></a>JetRenameColumn función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetrenamecolumn-function"></a>JetRenameColumn función)

La función **JetRenameColumn** se puede usar para cambiar el nombre de una columna existente en una tabla.

**Windows XP:**  **JetRenameColumn** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*szName*

Nombre actual de la columna cuyo nombre se va a cambiar.

*szNameNew*

Nombre nuevo de la columna a la que se va a cambiar el nombre.

*grbit*

Este parámetro debe ser 0.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Esta columna especificada no existe para esta tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Uno de los nombres de objeto especificados no era válido. Todos los nombres de objeto deben cumplir el mismo conjunto de reglas. Estas reglas son:</p>
<ul>
<li><p>Los nombres de objeto deben estar compuestos por caracteres ASCII.</p></li>
<li><p>Los nombres de objeto deben tener al menos un carácter de longitud.</p></li>
<li><p>Los nombres de objeto no pueden superar JET_cbNameMost (64) caracteres de longitud.</p></li>
<li><p>Los nombres de objeto no pueden comenzar con un espacio: los nombres de objeto no pueden contener caracteres de control ASCII (de 0x00 a 0x1F).</p></li>
<li><p>Los nombres de objeto no pueden contener un carácter de exclamación (!), punto (.), corchete de apertura ([) o corchete de cierre (]).</p></li>
<li><p>Una vez validada, solo se usará la parte de la cadena hasta el primer espacio (si existe) para el nombre del objeto. Esto significa que los nombres de objeto no pueden contener un espacio.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Esto puede ocurrir para <strong>JetRenameColumn</strong> cuando:</p>
<ul>
<li><p><em>szName</em> es NULL.</p></li>
<li><p><em>szNameNew</em> es NULL.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Esta operación solo se puede realizar cuando la sesión no está dentro de una transacción.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>No se puede realizar una actualización mientras esté dentro del ámbito de una transacción de solo lectura. Una transacción de solo lectura es una transacción que se ha iniciado mediante una llamada a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, el nombre de la columna especificada en la tabla asociada al cursor se cambia de forma permanente al nuevo nombre. También se actualizarán los índices que hagan referencia a esa columna.

En caso de error, no se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

La operación de cambio de nombre de columna es poco habitual porque, a diferencia de otras operaciones de esquema, no se lleva a cabo como una transacción. Cuando se cambia el nombre de una columna de una tabla determinada en una sesión, cualquier otra sesión que use esa tabla verá el cambio inmediatamente, incluso si se encuentran en una transacción que impediría que esa sesión pudiera ver cualquier otro cambio realizado por la sesión que realiza la operación de cambio de nombre.

El ID. de columna de una columna no se ve afectado por la operación de cambio de nombre.

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
<td><p>Se implementa como <strong>JetRenameColumnW</strong> (Unicode) y <strong>JetRenameColumnA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
