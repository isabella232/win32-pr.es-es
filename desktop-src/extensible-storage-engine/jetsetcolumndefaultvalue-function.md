---
description: 'Más información acerca de: JetSetColumnDefaultValue (función)'
title: JetSetColumnDefaultValue función)
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f50d30b2edeca716895d8dd2339d659f0e1382f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907764"
---
# <a name="jetsetcolumndefaultvalue-function"></a>JetSetColumnDefaultValue función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetsetcolumndefaultvalue-function"></a>JetSetColumnDefaultValue función)

La función **JetSetColumnDefaultValue** se puede usar para cambiar el valor predeterminado de una columna existente.

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*DBID*

Base de datos que se va a usar para esta llamada.

*szTableName*

Nombre de la tabla que contiene la columna que se verá afectada.

*szColumnName*

Nombre de la columna cuyo valor predeterminado se cambiará.

*pvData*

Búfer de entrada que contiene el nuevo valor predeterminado.

*cbData*

Tamaño del búfer de entrada que contiene el nuevo valor predeterminado.

*grbit*

Reservado para uso futuro.

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
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Igual que JET_errNullInvalid.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnInUse</p></td>
<td><p>La columna especificada está siendo utilizada por un índice.</p>
<p><strong>JetSetColumnDefaultValue</strong> no puede cambiar el valor predeterminado de una columna a la que se hace referencia en la definición de un índice. Esto se debe a que, si lo hace, podría cambiar el contenido del índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Esta columna especificada no existe para esta tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>El identificador de base de datos especificado no era válido.</p></td>
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
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullInvalid</p></td>
<td><p>No se pudo establecer la columna en NULL. Esto sucede para <strong>JetSetColumnDefaultValue</strong> cuando:</p>
<ul>
<li><p><em>cbData</em> es cero.</p></li>
<li><p><strong>pvData</strong> es NULL.</p></li>
</ul>
<p>Por lo tanto, no es posible establecer el valor predeterminado de una columna (atrás) en NULL o en un valor de longitud cero.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>Esta tabla especificada no existe para esta base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Esta tabla especificada está en uso por otra sesión.</p>
<p><strong>JetSetColumnDefaultValue</strong> requiere acceso exclusivo a una tabla para cambiar el valor predeterminado de la columna en las versiones anteriores a Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>No es válido intentar una actualización cuando se encuentra dentro del ámbito de una transacción de solo lectura. Una transacción de solo lectura es una transacción que se ha iniciado mediante una llamada a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Otra sesión ha bloqueado previamente el registro para su actualización. Se producirá un error en la actualización intentada por esta sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, el valor predeterminado de la columna especificada en la tabla dada en la base de datos determinada se cambia permanentemente al nuevo valor predeterminado.

En caso de error, no se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

No es posible cambiar el valor predeterminado de una columna en una tabla de plantilla.

El motor de base de datos truncará silenciosamente el valor predeterminado de una columna en 255 bytes para las columnas de texto largo y binario largo.

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
<td><p>Se implementa como <strong>JetSetColumnDefaultValueW</strong> (Unicode) y <strong>JetSetColumnDefaultValueA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)  
[JetStopService](./jetstopservice-function.md)
