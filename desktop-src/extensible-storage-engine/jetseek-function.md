---
description: 'Más información acerca de: JetSeek (función)'
title: JetSeek función)
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c386ae3af5353b95d9d1d3c67df4d680c52bff68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707177"
---
# <a name="jetseek-function"></a>JetSeek función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetseek-function"></a>JetSeek función)

La función **JetSeek** coloca de forma eficaz un cursor en una entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y la desigualdad especificada. Una clave de búsqueda se debe haber construido previamente mediante [JetMakeKey](./jetmakekey-function.md).

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*grbit*

Grupo de bits que contiene las opciones que se van a utilizar para esta llamada. *Grbit* debe ser distinto de cero y debe incluir uno o varios de los valores enumerados en la tabla siguiente.

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
<td><p>JET_bitCheckUniqueness</p></td>
<td><p>Se devolverá un código de error especial, JET_wrnUniqueKey, si se puede determinar de forma económica que hay exactamente una entrada de índice que coincide con la clave de búsqueda.</p>
<p>Esta opción se omite a menos que también se especifique JET_bitSeekEQ.</p>
<p>Esta opción solo está disponible en Windows Server 2003 y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekEQ</p></td>
<td><p>El cursor se colocará en la entrada de índice más cercana al inicio del índice que coincida exactamente con la clave de búsqueda. El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de dicho índice. El inicio del índice no es el mismo que el extremo inferior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p>
<p>No es significativo usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSeekGE</p></td>
<td><p>El cursor se colocará en la entrada de índice más cercana al inicio del índice que sea mayor o igual que una entrada de índice que coincida exactamente con los criterios de búsqueda. El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de dicho índice. El inicio del índice no es el mismo que el extremo inferior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p>
<p>No es significativo usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín diseñada para buscar las entradas de índice más cercanas al final del índice.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekGT</p></td>
<td><p>El cursor se colocará en la entrada de índice más cercana al inicio del índice que sea mayor que una entrada de índice que coincida exactamente con los criterios de búsqueda. El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de dicho índice. El inicio del índice no es el mismo que el extremo inferior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p>
<p>No es significativo usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín diseñada para buscar entradas de índice más cercanas al inicio del índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSeekLE</p></td>
<td><p>El cursor se colocará en la entrada de índice más cercana al final del índice que sea menor o igual que una entrada de índice que coincida exactamente con los criterios de búsqueda. El final del índice es la entrada de índice que se encuentra al pasar al último registro de dicho índice. El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p>
<p>No es significativo usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín diseñada para buscar entradas de índice más cercanas al inicio del índice.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekLT</p></td>
<td><p>El cursor se colocará en la entrada de índice más cercana al final del índice que sea menor que una entrada de índice que coincida exactamente con los criterios de búsqueda. El final del índice es la entrada de índice que se encuentra al pasar al último registro de dicho índice. El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p>
<p>No es significativo usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín diseñada para buscar las entradas de índice más cercanas al final del índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIndexRange</p></td>
<td><p>Se configurará automáticamente un intervalo de índice para todas las claves que coincidan exactamente con la clave de búsqueda. El intervalo de índice resultante es idéntico al que se habría creado mediante una llamada a <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> con las opciones JET_bitRangeInclusive y JET_bitRangeUpperLimit. Vea <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> para obtener más información.</p>
<p>Este es un método práctico para detectar todas las entradas de índice que coinciden con los mismos criterios de búsqueda.</p>
<p>Esta opción se omite a menos que también se especifique JET_bitSeekEQ.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función permite que se devuelvan los [JET_ERRs](./jet-err.md) definidos en esta API. Para obtener más información acerca de los errores de jet, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

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
<p>En el caso de <strong>JetSeek</strong>, esto significa que se ha encontrado una entrada de índice que coincide exactamente con los criterios de búsqueda.</p></td>
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
<td><p>JET_errKeyNotMade</p></td>
<td><p>No hay ninguna clave de búsqueda actual para el cursor. <strong>JetSeek</strong> requiere que el cursor tenga una clave de búsqueda válida porque la usará para los criterios de búsqueda utilizados para buscar entradas de índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNotFound</p></td>
<td><p>No se encontró ninguna entrada de índice que coincida con los criterios de búsqueda.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSeekNotEqual</p></td>
<td><p>Se encontró una entrada de índice que coincidía con los criterios de búsqueda. Sin embargo, esa entrada de índice no era una coincidencia exacta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p>Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnUniqueKey</p></td>
<td><p>Se encontró exactamente una entrada de índice que coincide exactamente con los criterios de búsqueda. Este error solo se devolverá si se especificó JET_bitSeekCheckUniqueness y era barato determinar que la entrada de índice coincidente era la única entrada de índice que coincide exactamente con los criterios de búsqueda.</p>
<p>Este error solo lo devolverán Windows Server 2003 y versiones posteriores.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, el cursor se colocará en una entrada de índice que coincida con los criterios de búsqueda. Si se ha preparado un registro para la actualización, la actualización se cancelará. Si hay un intervalo de índice en vigor, se cancelará ese intervalo de índices. Si se ha construido una clave de búsqueda para el cursor, esa clave de búsqueda se eliminará. No se producirá ningún cambio en el estado de la base de datos. Cuando varias entradas de índice tienen el mismo valor, siempre se selecciona la entrada más cercana al inicio del índice.

En caso de error, la posición del cursor permanecerá sin cambios a menos que se devuelva JET_errRecordNotFound. En ese caso, el cursor se colocará donde la entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y la desigualdad especificada habría sido. El cursor se puede mover en relación con esa posición, pero aún no se encuentra en una entrada de índice válida. Si se ha preparado un registro para la actualización, la actualización se cancelará. Si hay un intervalo de índice en vigor, se cancelará ese intervalo de índices. Si se ha construido una clave de búsqueda para el cursor, esa clave de búsqueda se eliminará. No se producirá ningún cambio en el estado de la base de datos.

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
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
