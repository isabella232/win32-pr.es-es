---
description: 'Más información acerca de: JetIndexRecordCount (función)'
title: JetIndexRecordCount función)
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539979"
---
# <a name="jetindexrecordcount-function"></a>JetIndexRecordCount función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetindexrecordcount-function"></a>JetIndexRecordCount función)

La función **JetIndexRecordCount** cuenta el número de entradas en el índice actual desde la posición actual hacia delante. La posición actual se incluye en el recuento. El recuento puede ser mayor que el número total de registros de la tabla si el índice actual está sobre una columna de varios valores y las instancias de la columna tienen varios valores. Si la tabla está vacía, se devolverá 0 para el recuento.

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*pcrec*

El puntero a un valor Long sin signo para recibir el recuento.

*crecMax*

Número máximo de registros que se van a contar. Un valor de *crecMax* de 0 indica que el recuento es ilimitado.

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
<td><p>No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor no está actualmente en un registro y la tabla no está vacía.</p>
<p><strong>Windows XP, Windows server 2003, windows 2000 Server y windows 2000 Professional:</strong>  Si el cursor está situado en un índice vacío o en un intervalo de índices, <strong>JetIndexRecordCount</strong> devuelve erróneamente JET_errNoCurrentRecord.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, el número exacto de entradas de índice, incluida la posición actual y hasta *crecMax* (si no es 0), se devuelve en la unsigned Long a la que apunta *pcrec*.

Si se produce un error en esta función, no se realiza ningún cambio en la memoria asignada en *precpos*.

#### <a name="remarks"></a>Observaciones

Si la tabla no está vacía, el cursor se debe colocar en el registro desde el que se va a iniciar el recuento. El recuento incluirá este registro y recuento hasta el límite especificado en *crecMax*. Si *crecMax* es 0, la operación seguirá contando hasta el final del índice.

Los intervalos de índice se pueden usar para construir limitaciones de final de índice artificiales para el recuento. De esta manera, los subintervalos de un índice se pueden contar exactamente. El cursor debe colocarse en la primera fila del intervalo. Se debe crear el final de la clave de intervalo y, a continuación, se debe usar [JetSetIndexRange](./jetsetindexrange-function.md) para establecer el intervalo superior, ya sea de forma inclusiva o exclusiva. Por último, se debe llamar a **JetIndexRecordCount** para contar exactamente el intervalo.

**JetIndexRecordCount** obedece la semántica de las transacciones y devuelve un recuento exacto para esta sesión en particular en su estado transaccional actual.

**JetIndexRecordCount** obtiene acceso a las páginas hoja del índice con el fin de contar exactamente las entradas. Por lo tanto, puede realizar una gran cantidad de e/s y puede ser lenta. La limitación de *crecMax* debe usarse para evitar una carga excesiva. Si un intervalo es grande, es posible que se pueda contar el intervalo de manera aproximada mediante [JetGetRecordPosition](./jetgetrecordposition-function.md).

**Windows XP, Windows server 2003, windows 2000 Server y windows 2000 Professional:**  Si el cursor está situado en un índice vacío o en un intervalo de índices, **JetIndexRecordCount** devuelve erróneamente JET_errNoCurrentRecord en lugar de devolver un recuento de registros de cero. La aplicación debe comprobar si el índice o el intervalo de índices está vacío en este caso.

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
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
