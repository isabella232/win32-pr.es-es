---
description: 'Más información sobre: JetGotoBookmark (Función)'
title: JetGotoBookmark (Función)
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
ms.openlocfilehash: 56e94339a49cc80e8b7b416e89efc5c85079981e0430f325e29f1dd711eef63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979005"
---
# <a name="jetgotobookmark-function"></a>JetGotoBookmark (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgotobookmark-function"></a>JetGotoBookmark (Función)

La **función JetGotoBookmark** coloca un cursor en una entrada de índice para el registro asociado al marcador especificado. El marcador se puede usar con cualquier índice definido en una tabla. El marcador de un registro se puede recuperar mediante [JetGetBookmark](./jetgetbookmark-function.md).

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

*tableid*

Cursor que se va a usar para esta llamada.

*pvBookmark*

Búfer que contiene el marcador que se usará para colocar el cursor.

*cbBookmark*

Tamaño del marcador en el búfer.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

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
<td><p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>La operación no se puede completar porque la instancia de asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>   Este valor devuelto se introdujo en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>El marcador proporcionado no es válido. Esto puede haber ocurrido porque el tamaño del marcador es cero o el puntero de búfer del marcador es <strong>NULL.</strong></p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor está en un índice secundario y no se pudo encontrar ninguna entrada de índice para el registro asociado al marcador.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>No se encontró el registro asociado al marcador.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>   Este valor devuelto se introdujo en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si esta función se realiza correctamente, el cursor se colocará en una entrada de índice para el registro asociado al marcador especificado. Si se ha preparado un registro para la actualización, esa actualización se cancelará. Si hay un intervalo de índice en vigor, ese intervalo de índice se cancelará. Si se ha construido una clave de búsqueda para el cursor, se eliminará esa clave de búsqueda. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, la posición del cursor permanecerá sin cambios. Si se ha preparado un registro para la actualización, esa actualización se cancelará. Si hay un intervalo de índice en vigor, ese intervalo de índice se cancelará. Si se ha construido una clave de búsqueda para el cursor, se eliminará esa clave de búsqueda. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Comentarios

Hay dos maneras de usar un marcador para colocar un cursor en un índice. La primera es usar el marcador para colocar en el registro directamente. Esto sucede cuando el índice actual del cursor es el índice principal. Esta técnica funciona porque un marcador DE ESENT es el mismo que la clave principal del registro asociado.

La segunda manera de usar un marcador es colocarlo en una entrada de un índice secundario que se corresponda con el registro asociado a ese marcador. Durante este proceso, el motor busca el registro real mediante el marcador en el índice principal. A continuación, usa los datos de registro y la definición del índice secundario para calcular una clave en el índice secundario que apunta al registro. A continuación, coloca el cursor en la entrada de índice de esa clave. Si el cursor se encuentra actualmente en un índice secundario sobre una o varias columnas de clave con varios valores, el cursor se colocará en la entrada de índice correspondiente al primer valor múltiple de cada una de esas columnas de clave.

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)
