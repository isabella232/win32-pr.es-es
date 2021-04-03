---
description: 'Más información acerca de: JetGetRecordPosition (función)'
title: Función JetGetRecordPosition
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4301b25ca111228b742ce7b35ab9ae28e170526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082746"
---
# <a name="jetgetrecordposition-function"></a>Función JetGetRecordPosition


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetrecordposition-function"></a>Función JetGetRecordPosition

La función **JetGetRecordPosition** devuelve la posición fraccionaria del registro actual en el índice actual en forma de estructura de [JET_RECPOS](./jet-recpos-structure.md) . Esta estructura describe las posiciones fraccionarias en términos de un número aproximado de entradas de índice antes del registro actual y un número total aproximado de entradas en el índice.

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*precpos*

La descripción de la fracción que se va a usar para obtener la posición del registro actual en el índice actual.

*cbRecpos*

Tamaño de la memoria asignada en *precpos*.

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
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No se puede completar esta operación porque la instancia, asociada a la sesión, encontró un error irrecuperable. Es necesario revocar el acceso a todos los datos con el fin de proteger la integridad de los datos.</p>
<p><strong>Windows 2000:</strong>  Este error no lo devolverá el sistema operativo Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>El tamaño de la memoria asignada en <em>precpos</em> no es suficiente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor no está actualmente en un registro y no puede devolver una posición.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows 2000:</strong>  Este error no lo devolverá el sistema operativo Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se devuelve el número aproximado de entradas de índice que preceden al registro actual del índice en precpos- \> centriesLT. se devuelve 1 en precpos- \> centriesInRange. El número aproximado de entradas en el índice se devuelve en precpos- \> centriesTotal.

En caso de error, no se realiza ningún cambio en la memoria asignada en *precpos*.

#### <a name="remarks"></a>Observaciones

Esta operación devuelve datos variables cuando las actualizaciones se producen de forma continua en la tabla. Los cambios en los valores no siempre coincidirán con las expectativas basadas en el conocimiento de las actualizaciones, ya que los valores son aproximaciones basadas en las propiedades físicas del índice. El aislamiento transaccional no se aplica a las posiciones de **JetGetRecordPosition** , ya que los valores dependen de las propiedades físicas del índice que no están aisladas de las transacciones.

[JET_RECPOS](./jet-recpos-structure.md) no se deben utilizar para describir un registro de una tabla o para cambiar la posición de un registro cerca de un registro existente. En su lugar, se deben recuperar los marcadores de un registro existente y, a continuación, usar para cambiar la posición del mismo registro.

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
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetGotoPosition](./jetgotoposition-function.md)  
[JetStopService](./jetstopservice-function.md)
