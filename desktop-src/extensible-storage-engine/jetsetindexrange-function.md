---
description: 'Más información acerca de: JetSetIndexRange (función)'
title: Función JetSetIndexRange
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883085633bebf25180c82f0f8917f6fa31fe7304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275561"
---
# <a name="jetsetindexrange-function"></a>Función JetSetIndexRange


_**Se aplica a:** Windows | Windows Server_

## <a name="jetsetindexrange-function"></a>Función JetSetIndexRange

La función **JetSetIndexRange** limita temporalmente el conjunto de entradas de índice que el cursor puede recorrer con [JetMove](./jetmove-function.md) para que empiecen a partir de la entrada de índice actual y terminen en la entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y los criterios enlazados especificados. Una clave de búsqueda se debe haber construido previamente mediante [JetMakeKey](./jetmakekey-function.md).

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableidSrc*

Cursor que se va a usar para esta llamada.

*grbit*

Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitRangeInclusive</p></td>
<td><p>Esta opción o ausencia de esta opción indica los criterios de límite del intervalo de índices. Cuando está presente, esta opción indica que el límite del intervalo de índice es inclusivo. Cuando está ausente, esta opción indica que el límite del intervalo de índice es exclusivo. Cuando el límite del intervalo de índice es inclusivo, las entradas de índice que coinciden exactamente con los criterios de búsqueda se incluyen en el intervalo.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRangeInstantDuration</p></td>
<td><p>Esta opción solicita que se quite el intervalo de índice en cuanto se haya establecido. Todos los demás aspectos de la operación permanecen sin cambios. Esto resulta útil para probar la existencia de entradas de índice que coinciden con los criterios de búsqueda.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRangeRemove</p></td>
<td><p>Esta opción solicita que se cancele un intervalo de índice existente en el cursor. Una vez que se cancele el intervalo de índice, será posible moverse más allá del final del intervalo de índices mediante <a href="gg294117(v=exchg.10).md">JetMove</a>. Si un intervalo de índice no está ya en vigor, se producirá un error en <strong>JetSetIndexRange</strong> con JET_errInvalidOperation.</p>
<p>Cuando se especifica esta opción, se omiten todas las demás opciones.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRangeUpperLimit</p></td>
<td><p>Si se usa esta opción, la clave de búsqueda del cursor representa los criterios de búsqueda para la entrada de índice más cercana al final del índice que coincidirá con el intervalo de índice. El intervalo de índice se establecerá entre la posición actual del cursor y esta entrada de índice para que se puedan encontrar todas las coincidencias recorriendo en el índice mediante <a href="gg294117(v=exchg.10).md">JetMove</a> con JET_MoveNext o un desplazamiento positivo.</p>
<p>No es significativo usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín diseñada para buscar entradas de índice más cercanas al inicio del índice.</p>
<p>Si se omite esta opción, la clave de búsqueda del cursor representa los criterios de búsqueda para la entrada de índice más cercana al inicio del índice que coincidirá con el intervalo de índice. El intervalo de índice se establecerá entre la posición actual del cursor y esta entrada de índice para que se puedan encontrar todas las coincidencias recorriendo hacia atrás el índice mediante <a href="gg294117(v=exchg.10).md">JetMove</a> con JET_MovePrevious o un desplazamiento negativo.</p>
<p>No es significativo omitir esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín diseñada para buscar las entradas de índice más cercanas al final del índice.</p></td>
</tr>
</tbody>
</table>


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
<td><p>La operación se ha completado correctamente.</p>
<p>En el caso de <strong>JetSetIndexRange</strong>, esto significa que se ha cancelado un intervalo de índice existente o que hay al menos una entrada de índice dentro del intervalo de índices.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p>Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOperation</p></td>
<td><p><strong>JetSetIndexRange</strong> devolverá este error cuando se especificó JET_bitRangeRemove y no hay ningún intervalo de índice en vigor.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade</p></td>
<td><p>No hay ninguna clave de búsqueda actual para el cursor. <strong>JetSetIndexRange</strong> requiere que el cursor tenga una clave de búsqueda válida porque la usará para los criterios de búsqueda utilizados para buscar entradas de índice.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>No hay ningún índice actual para el cursor. Esto ocurrirá para <strong>JetSetIndexRange</strong> si el cursor está en el índice clúster de una tabla, no se ha definido un índice principal. No se admite la configuración de un intervalo de índice en este tipo de índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Este error lo devolverá <strong>JetSetIndexRange</strong> para indicar que no hay entradas de índice dentro del intervalo de índices.</p></td>
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
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p>Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se realiza correctamente, si se especifica JET_bitRangeRemove, se cancela el intervalo de índice que está actualmente en vigor. Si no se especifica JET_bitRangeRemove y se especifica JET_bitRangeInstantDuration, no habrá ningún intervalo de índice en vigor. Si no se especifica ni JET_bitRangeRemove ni JET_bitRangeInstantDuration, se aplica un nuevo intervalo de índices. Este intervalo de índice limitará temporalmente el conjunto de entradas de índice que el cursor puede recorrer con [JetMove](./jetmove-function.md) a los que empiezan en la entrada de índice actual y terminan en la entrada de índice que coincide con los criterios de búsqueda. La posición del cursor permanecerá sin cambios. Si se ha construido una clave de búsqueda para el cursor, esa clave de búsqueda se eliminará. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, si no se devuelve JET_errNoCurrentRecord, no habrá ningún intervalo de índice en vigor. Si se devuelve JET_errNoCurrentRecord, se aplica un nuevo intervalo de índices. Este intervalo de índice limitará temporalmente el conjunto de entradas de índice que el cursor puede recorrer con [JetMove](./jetmove-function.md) a los que empiezan en la entrada de índice actual y terminan en la entrada de índice que coincide con los criterios de búsqueda. La posición del cursor permanecerá sin cambios. Si se devolvió JET_errNoCurrentRecord y se ha creado una clave de búsqueda para el cursor, esa clave de búsqueda se eliminará. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Un intervalo de índice es volátil y se cancelará automáticamente si se realiza una navegación distinta de [JetMove](./jetmove-function.md) en el cursor.

Los intervalos de índice solo funcionan en una dirección. Si se establece un límite superior, solo se impedirá el movimiento hacia delante mediante [JetMove](./jetmove-function.md) con JET_MoveNext o un desplazamiento positivo una vez alcanzado el final del intervalo de índices. Todavía es posible dejar el intervalo de índice en este caso usando [JetMove](./jetmove-function.md) con JET_MovePrevious o un desplazamiento negativo. Una situación análoga se produce para un límite inferior.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetMove](./jetmove-function.md)  
[JetSetIndexRange]()  
[JetStopService](./jetstopservice-function.md)
