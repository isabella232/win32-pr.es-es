---
description: 'Más información acerca de: JetGetCurrentIndex (función)'
title: JetGetCurrentIndex función)
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3337ddaefbea803a137ad8366d2e3df665bacd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716511"
---
# <a name="jetgetcurrentindex-function"></a>JetGetCurrentIndex función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetcurrentindex-function"></a>JetGetCurrentIndex función)

La función **JetGetCurrentIndex** determina el nombre del índice actual de un cursor determinado. Este nombre también se usa para volver a seleccionar más adelante dicho índice como el índice actual mediante [JetSetCurrentIndex](./jetsetcurrentindex-function.md). También se puede usar para detectar las propiedades de ese índice mediante [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*szIndexName*

Búfer de salida que recibe el nombre del índice actual del cursor.

*cchIndexName*

Tamaño máximo en caracteres del búfer de salida.

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
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
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
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>La operación se completó correctamente, pero el búfer de salida era demasiado pequeño para recibir el nombre de índice completo.</p>
<p>El búfer de salida se ha rellenado con tantos nombres de índice como quepan. Si el búfer de salida tiene al menos un carácter de longitud, la cadena en el búfer de salida se terminará en NULL.</p>
<p><strong>Nota:  </strong> Este error no se devolverá si cchIndexName es cero. Vea la sección Comentarios para obtener más información.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se devolverá el nombre del índice actual del cursor especificado en el búfer de salida. Si se devuelve JET_wrnBufferTruncated, el búfer de salida contendrá tantos el nombre del índice como quepan en el espacio proporcionado. Si el búfer de salida tiene al menos un carácter de longitud, la cadena devuelta en el búfer terminará en NULL. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, el estado del búfer de salida será undefined. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Si no hay ningún índice actual para el cursor, se devolverá una cadena vacía. Esto puede ocurrir cuando el cursor está en el índice clúster de la tabla y no se ha definido ningún índice principal. Este índice se conoce como el índice secuencial de la tabla y no tiene ninguna definición. En cualquier caso, si se establece el índice actual en una cadena vacía mediante [JetSetCurrentIndex](./jetsetcurrentindex-function.md) , se seleccionará el índice clúster independientemente de la presencia de una definición de índice principal.

Hay un error importante en esta función que está presente en todas las versiones. Si el búfer de salida es demasiado pequeño para recibir el nombre de índice completo y el búfer de salida tiene al menos un carácter de longitud, JET_wrnBufferTruncated no se devolverá. Se devolverá JET_errSuccess en su lugar. Para evitar este problema, el búfer de salida debe tener siempre al menos JET_cbNameMost + 1 (65) caracteres de longitud.

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
<td><p>Se implementa como <strong>JetGetCurrentIndexW</strong> (Unicode) y <strong>JetGetCurrentIndexA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
