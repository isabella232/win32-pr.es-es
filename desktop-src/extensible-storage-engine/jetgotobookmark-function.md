---
description: 'Más información acerca de: JetGotoBookmark (función)'
title: JetGotoBookmark función)
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 89dde261648b396bcfc9532911c0d4acd3c88828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707185"
---
# <a name="jetgotobookmark-function"></a>JetGotoBookmark función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgotobookmark-function"></a>JetGotoBookmark función)

La función **JetGotoBookmark** coloca un cursor en una entrada de índice para el registro que está asociado al marcador especificado. El marcador se puede usar con cualquier índice definido en una tabla. El marcador de un registro se puede recuperar mediante [JetGetBookmark](./jetgetbookmark-function.md).

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*pvBookmark*

Búfer que contiene el marcador que se va a usar para colocar el cursor.

*cbBookmark*

Tamaño del marcador en el búfer.

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
<td><p>No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No se puede completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>   Este valor devuelto se presentó en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>El marcador proporcionado no es válido. Esto puede deberse a que el tamaño del marcador es cero o el puntero del búfer del marcador es <strong>nulo</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor está en un índice secundario y no se encontró ninguna entrada de índice para el registro que está asociado con el marcador.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>No se pudo encontrar el registro asociado al marcador.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>   Este valor devuelto se presentó en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, el cursor se colocará en una entrada de índice para el registro asociado al marcador especificado. Si se ha preparado un registro para la actualización, la actualización se cancelará. Si hay un intervalo de índice en vigor, se cancelará ese intervalo de índices. Si se ha construido una clave de búsqueda para el cursor, se eliminará la clave de búsqueda. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, la posición del cursor permanecerá sin cambios. Si se ha preparado un registro para la actualización, la actualización se cancelará. Si hay un intervalo de índice en vigor, se cancelará ese intervalo de índices. Si se ha construido una clave de búsqueda para el cursor, se eliminará la clave de búsqueda. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Hay dos maneras de usar un marcador para colocar un cursor en un índice. El primero es usar el marcador para colocarlo directamente en el registro. Esto sucede si el índice actual del cursor es el índice principal. Esta técnica funciona porque un marcador ESENT es el mismo que el de la clave principal del registro asociado.

La segunda manera de usar un marcador es colocarlo en una entrada de un índice secundario que se corresponda con el registro asociado a dicho marcador. Durante este proceso, el motor busca el registro real mediante el marcador en el índice principal. A continuación, utiliza los datos de registro y la definición de índice secundario para calcular una clave en el índice secundario que apunta al registro. A continuación, coloca el cursor en la entrada de índice de esa clave. Si el cursor se encuentra actualmente en un índice secundario de una o varias columnas de clave de varios valores, el cursor se colocará en la entrada de índice correspondiente al primer valor múltiple de cada una de esas columnas de clave.

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

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)
