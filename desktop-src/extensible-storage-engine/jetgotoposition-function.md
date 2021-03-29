---
description: 'Más información acerca de: JetGotoPosition (función)'
title: JetGotoPosition función)
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae5148431ad46c5a75bbd804f2c0d777b279561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808438"
---
# <a name="jetgotoposition-function"></a>JetGotoPosition función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgotoposition-function"></a>JetGotoPosition función)

La función **JetGotoPosition** mueve un cursor a una nueva ubicación que es una fracción del camino a través del índice actual. La fracción es aproximadamente igual a la siguiente:

precpos- \> centriesLT/precpos- \> centriesTotal

Esta operación se realiza en respuesta a la entrada del cuadro de desplazamiento del usuario que se recibe cuando el usuario intenta mostrar los datos que se inician a la vez a través de un conjunto de datos.

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*precpos*

La descripción de la fracción que se va a usar para colocar el cursor en el índice actual.

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
<td><p>No se pudo completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No se pudo completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>El precpos especificado- &gt; cbStruct no es un tamaño válido para la estructura <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> , o precpos- &gt; centriesLT es mayor que precpos- &gt; centriesTotal.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNotFound</p></td>
<td><p>Se devolverá este error si el índice está vacío.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, el cursor se mueve a un registro actual que es una fracción del camino a través del índice donde la fracción es precpos- \> centriesLT dividida por precpos- \> centriesTotal.

Si se produce un error en esta función, la ubicación del cursor permanece sin cambios.

#### <a name="remarks"></a>Observaciones

Esta operación mueve el cursor por la tabla a una posición en el siguiente punto aproximado: precpos- \> centriesLT dividido por precpos- \> centriesTotal.

Cuando las actualizaciones se producen de forma continua en la tabla, las llamadas subsiguientes con el mismo [JET_RECPOS](./jet-recpos-structure.md) pueden mover el cursor a distintas posiciones del índice, tanto antes como después de la posición anterior. El aislamiento transaccional no se aplica a la colocación a través de [JET_RECPOS](./jet-recpos-structure.md) porque depende de las propiedades físicas del índice que no están aisladas de las transacciones.

[JET_RECPOS](./jet-recpos-structure.md) no se deben utilizar para describir un registro de una tabla o para cambiar la posición de un registro cerca de un registro existente. En su lugar, los marcadores de un registro existente deben recuperarse después de un **JetGotoPosition** inicial y, a continuación, usarse para cambiar la posición del mismo registro.

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
