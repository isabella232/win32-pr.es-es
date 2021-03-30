---
description: 'Más información acerca de: JetMove (función)'
title: Función JetMove
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e42cb2258d373f8c4edb96309c6db0853eab4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275189"
---
# <a name="jetmove-function"></a>Función JetMove


_**Se aplica a:** Windows | Windows Server_

## <a name="jetmove-function"></a>Función JetMove

La función **JetMove** coloca un cursor al principio o al final de un índice y recorre las entradas de ese índice hacia delante o hacia atrás. También es posible desplazar el cursor hacia delante o hacia atrás en el índice actual en un número especificado de entradas de índice. Otro enfoque es limitar artificialmente las entradas de índice que se pueden enumerar mediante **JetMove** mediante la configuración de un intervalo de índice en el cursor mediante [JetSetIndexRange](./jetsetindexrange-function.md).

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*Gallo*

Desplazamiento arbitrario que indica el movimiento deseado del cursor en el índice actual.

Además de los desplazamientos estándar, este parámetro también se puede establecer con una de las siguientes opciones.

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
<td><p>JET_MoveFirst</p></td>
<td><p>Mueve el cursor a la primera entrada del índice en el índice (si existe).</p>
<p><strong>Nota:</strong>   El valor literal de-2147483648 se utiliza para denotar esta opción. No utilice este valor como un desplazamiento normal o se puede producir un comportamiento imprevisto.</p></td>
</tr>
<tr class="even">
<td><p>JET_MoveLast</p></td>
<td><p>Mueve el cursor a la última entrada del índice en el índice (si existe).</p>
<p><strong>Nota:</strong>   El valor literal de 2147483647 se utiliza para denotar esta opción. No utilice este valor como un desplazamiento normal o se puede producir un comportamiento imprevisto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_MoveNext</p></td>
<td><p>Mueve el cursor a la entrada de índice siguiente en el índice (si existe). Este valor es exactamente igual a un desplazamiento normal de + 1.</p></td>
</tr>
<tr class="even">
<td><p>JET_MovePrevious</p></td>
<td><p>Mueve el cursor a la entrada de índice anterior en el índice (si existe).</p>
<p>Este valor es exactamente igual a un desplazamiento normal de-1, o 0 (cero).</p>
<p>El cursor permanece en la posición lógica actual y se probará la existencia de la entrada de índice correspondiente a esa posición lógica.</p></td>
</tr>
</tbody>
</table>


*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.

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
<td><p>JET_bitMoveKeyNE</p></td>
<td><p>Mueve el cursor hacia delante o hacia atrás por el número de entradas de índice necesarias para omitir el número solicitado de valores de clave de índice encontrados en el índice. Esto tiene el efecto de contraer las entradas de índice con valores de clave duplicados en una sola entrada de índice. Normalmente, un desplazamiento moverá el cursor por el número especificado de entradas de índice, independientemente de sus valores de clave.</p></td>
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
<td><p>La operación se ha completado correctamente. En el caso de <strong>JetMove</strong>, esto significa que se encontró una entrada de índice en la ubicación o el desplazamiento solicitado en el índice actual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor no está actualmente situado en una entrada de índice. En el caso de <strong>JetMove</strong>, esto significa que no se encontró una entrada de índice en la ubicación o el desplazamiento solicitado en el índice actual.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>El cursor está actualmente colocado lógicamente en una entrada de índice que corresponde a un registro que se ha eliminado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No se puede completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
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


Si esta función se ejecuta correctamente, el cursor se colocará en una entrada de índice que coincida con la ubicación o el desplazamiento solicitados. Si se ha preparado un registro para la actualización, la actualización se cancelará. Si hay un intervalo de índice en vigor y se ha especificado JET_MoveFirst o JET_MoveLast, se cancelará dicho intervalo de índices. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, la posición del cursor permanecerá sin cambios a menos que se devuelva JET_errNoCurrentRecord. En ese caso, el cursor se colocará donde habría sido la entrada de índice que coincide con la ubicación o el desplazamiento solicitado. El cursor se puede mover en relación con esa posición, pero aún no se encuentra en una entrada de índice válida. Si se ha preparado un registro para la actualización, la actualización se cancelará. Si hay un intervalo de índice en vigor y se ha especificado JET_MoveFirst o JET_MoveLast, se cancelará dicho intervalo de índices. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Un cursor puede moverse a dos posiciones especiales mediante **JetMove**, antes y después de la última. Si el cursor está en la primera entrada de índice de la tabla y se llama a **JetMove** con JET_MovePrevious, se producirá un error en la llamada con JET_errNoCurrentRecord y el cursor se colocará lógicamente antes de la primera entrada del índice. Esta posición lógica se mantiene aunque se inserte otra entrada de índice antes de la primera entrada en el índice. Una situación análoga se produce después de la última relativa al final del índice. Antes de que la primera y la última vez sean más útiles al configurar un intervalo de entradas de índice que se van a recorrer en iteración con **JetMove**, con un modelo de iterador que espera que siempre se mueva al siguiente elemento (o anterior) antes de usar ese elemento.

El conjunto de entradas de índice que **JetMove** puede visitar puede verse limitado mediante la configuración de un intervalo de índice en el cursor. Esto resulta útil para las aplicaciones que enumeran un conjunto de entradas de índice que coinciden con criterios simples que se pueden expresar a través de un par de claves de búsqueda compiladas para ese índice. Para obtener más información, vea [JetSetIndexRange](./jetsetindexrange-function.md).

En las versiones anteriores a Windows Server 2003 SP1, hay un problema en **JetMove** que se produce en algunos casos específicos, que afecta a la aplicación correcta de un intervalo de índice configurado por la función [JetSetIndexRange](./jetsetindexrange-function.md) . Si el cursor se encuentra actualmente antes de la primera entrada de índice y se establece un intervalo de índice con un límite superior que es menor que la primera entrada de índice, la siguiente llamada a **JetMove** irá erróneamente a esa entrada de índice en lugar de a que se produzcan errores con JET_errNoCurrentRecord, según lo esperado. Se producirá el mismo error en la situación análoga a partir del final del índice. Esta situación puede producirse en una aplicación que configura un intervalo de índices y navega por él mediante un iterador que espera iniciarse antes de la primera entrada de índice que es miembro del conjunto de entradas que se va a enumerar, en lugar de comenzar en la primera entrada de índice de ese conjunto. Esta situación también se produce en el caso análogo a partir del final del índice. La solución alternativa es que la aplicación Compruebe manualmente que la entrada de índice adquirida se encuentra dentro del intervalo de índices comparando la clave de la entrada de índice actual (recuperada mediante [JetRetrieveKey](./jetretrievekey-function.md)) con la clave que representa el final del intervalo de índice actual (recuperada mediante [JetRetrieveKey](./jetretrievekey-function.md) con JET_bitRetrieveCopy).

Es importante tener cuidado al pasar desplazamientos calculados a **JetMove**. Si el desplazamiento calculado es menor o igual que JET_MoveFirst, dicho desplazamiento se debe dividir en varias partes, cada una de las cuales se pasa a **JetMove** por separado, pero dentro de una única transacción para obtener el efecto deseado. Lo mismo se aplica a los desplazamientos mayores o iguales que JET_MoveNext. No es probable que una aplicación se someta a esto en el mundo real, pero es conveniente tener una defensa en este caso dada la semántica muy diferente de JET_MoveFirst y JET_MoveLast a partir de un desplazamiento normal.

Cuando se llama a **JetMove** con un desplazamiento muy grande, como cuando el parámetro cRow está establecido en 1000, **JetMove** recorre todas las entradas de índice de 1000 para llegar a la posición final. Actualmente, la API de ESE no proporciona una manera eficaz de desplazarse directamente a una entrada de índice determinada por el desplazamiento sin atravesar cada entrada de índice.

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
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
