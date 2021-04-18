---
description: 'Más información acerca de: JetSetCurrentIndex (función)'
title: Función JetSetCurrentIndex
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7698a12f470fadd5c43dc2afe23f95f8e51bdf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715030"
---
# <a name="jetsetcurrentindex-function"></a>Función JetSetCurrentIndex


_**Se aplica a:** Windows | Windows Server_

## <a name="jetsetcurrentindex-function"></a>Función JetSetCurrentIndex

La función **JetSetCurrentIndex** se puede usar para establecer el índice actual de un cursor. El índice actual de un cursor define qué registros de una tabla son visibles para ese cursor y el orden en que aparecen seleccionando el conjunto de entradas de índice que se van a usar para exponer esos registros.

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*szIndexName*

Nombre del índice que se va a seleccionar para el cursor.

Si este parámetro es NULL o una cadena vacía, se seleccionará el índice clúster. Si se define un índice principal para la tabla, ese índice se seleccionará porque es el mismo que el índice clúster. Si no hay ningún índice principal definido para la tabla, se seleccionará el índice secuencial. El índice secuencial no tiene ninguna definición de índice. Vea [JetCreateIndex](./jetcreateindex-function.md) para obtener más información.

Si *pindexid* no es null, se omitirá el nombre del índice y el índice se seleccionará por su ID. de índice.

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
<td><p>JET_errBadItagSequence</p></td>
<td><p>Se selecciona un índice secundario con la opción JET_bitNoMove y no hay ningún valor para la primera columna de clave de varios valores en la definición del nuevo índice que corresponde al número de secuencia especificado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidIndexId</p></td>
<td><p>El contenido del ID. de índice no era válido o expiró y debe actualizarse. Esto puede ocurrir para <strong>JetSetCurrentIndex</strong> cuando:</p>
<ul>
<li><p>pindexid- &gt; cbStruct no tiene el tamaño esperado (Windows Server 2003 y versiones posteriores).</p></li>
<li><p>El motor se ha cerrado desde que se ha capturado el ID. de índice.</p></li>
<li><p>Todos los cursores que hacen referencia a la tabla que contiene el índice correspondiente al ID. de índice se han cerrado y el motor ha expulsado la definición de ese índice de la caché de esquema.</p></li>
<li><p>El ID. de índice se está usando con un cursor abierto en la tabla equivocada.</p></li>
<li><p>El índice se ha quitado o aún no está visible para la sesión.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p>Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Uno de los nombres de objeto especificados no era válido. Todos los nombres de objeto deben cumplir el mismo conjunto de reglas. Estas reglas son:</p>
<ul>
<li><p>Los nombres de objeto deben estar compuestos por caracteres ASCII.</p></li>
<li><p>Los nombres de objeto deben tener al menos un carácter de longitud.</p></li>
<li><p>Los nombres de objeto no pueden superar JET_cbNameMost (64) caracteres de longitud.</p></li>
<li><p>Los nombres de objeto no pueden comenzar con un espacio.</p></li>
<li><p>Los nombres de objeto no pueden contener caracteres de control ASCII (de 0x00 a 0x1F).</p></li>
<li><p>Los nombres de objeto no pueden contener un carácter de exclamación (!), punto (.), corchete de apertura ([) o corchete de cierre (]).</p></li>
<li><p>Una vez validada, solo se usará la parte de la cadena hasta el primer espacio (si existe) para el nombre del objeto. Esto significa que los nombres de objeto no pueden contener un espacio.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Esto puede ocurrir para <strong>JetSetCurrentIndex</strong> cuando <em>PINDEXID</em> no es NULL y pindexid- &gt; cbStruct no tiene el tamaño esperado (Windows XP y versiones anteriores).</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Se selecciona un índice secundario con la opción JET_bitNoMove y no hay ninguna entrada de índice en el nuevo índice que se corresponda con el registro asociado a la entrada de índice en la posición actual del cursor en el índice anterior.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>El motor ha agotado el grupo de recursos usado para abrir cursores. El número máximo de cursores que se pueden abrir en cualquier momento se controla mediante <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>. Vea <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para obtener más información. Esto puede ocurrir para <strong>JetSetCurrentIndex</strong> cuando se ha seleccionado un índice secundario y el motor no puede abrir un cursor interno para usar ese índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p>Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, el índice actual del cursor se establece en el índice solicitado. Ahora se pueden buscar entradas de índice mediante [JetSeek](./jetseek-function.md) según la definición de índice del índice solicitado. Las entradas de índice también se pueden enumerar mediante [JetMove](./jetmove-function.md) en el orden especificado por la definición del índice. La posición actual del cursor se establece en la primera entrada de índice del índice (JET_bitMoveFirst) o en una entrada de índice específica relacionada con la posición actual del cursor en el índice anterior (JET_bitNoMove). No se producirá ningún cambio en el estado de la base de datos.

En caso de error, el índice actual y la posición actual del cursor se encuentran en un estado indefinido. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Si la sugerencia de ID. de índice está obsoleta, la API simplemente produce un error. No hay ninguna reserva al nombre de texto del índice en este caso, ya que podría esperar. Esta reserva debe realizarse manualmente mediante el autor de la llamada de la API.

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
<td><p>Se implementa como <strong>JetSetCurrentIndexW</strong> (Unicode) y <strong>JetSetCurrentIndexA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetGetCurrentIndex](./jetgetcurrentindex-function.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetMove](./jetmove-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetCurrentIndex]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
