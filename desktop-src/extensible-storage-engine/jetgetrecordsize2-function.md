---
description: 'Más información acerca de: JetGetRecordSize2 (función)'
title: JetGetRecordSize2 función)
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c68eafaaa53b5b88e6b003bdbafce287035cbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717233"
---
# <a name="jetgetrecordsize2-function"></a>JetGetRecordSize2 función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetrecordsize2-function"></a>JetGetRecordSize2 función)

La función **JetGetRecordSize2** recupera información de tamaño del registro de la ubicación deseada.

**Windows 7: JetGetRecordSize2** se incluye en el sistema operativo Windows 7.

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Identifica el contexto de la sesión de base de datos que se utilizará para la llamada API.

*TABLEID*

Identifica la tabla o el cursor que se utilizará para la llamada API. El cursor debe estar colocado en un registro o tener una actualización preparada.

*precsize*

Puntero a un búfer de salida para la estructura de [JET_RECSIZE2](./jet-recsize2-structure.md) .

*grbit*

Se trata de uno o varios de los valores siguientes.

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
<td><p>JET_bitRecordSizeInCopyBuffer</p></td>
<td><p>Recupera el tamaño del registro que se encuentra en el búfer de copia preparado para la actualización. De lo contrario <em>, el ID. de</em> reactivación o el cursor deben estar colocados en un registro y se utilizará ese registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordSizeRunningTotal</p></td>
<td><p>Cuando se especifica este bit, el <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> no se pone a cero antes de rellenar el contenido, lo que actúa de forma eficaz como acumulación de las estadísticas para varios registros visitados o actualizados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRecordSizeLocal</p></td>
<td><p>Esto hace que la API omita los valores largos no intrínsecos. Por ejemplo, solo se utilizará el registro local de la página.</p></td>
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
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Una de las opciones solicitadas no era válida o no se implementó. Este error lo devolverá la función <strong>JetGetRecordSize2</strong> cuando se especifica un <em>grbit</em> no válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:  </strong> JET_errInstanceUnavailable solo lo devolverá el sistema operativo Windows XP y versiones posteriores de Windows.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No es válido utilizar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:  </strong> JET_errInstanceUnavailable solo se devolverán en Windows XP y versiones posteriores de Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Esto puede ocurrir si el cursor se colocó incorrectamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Si el cursor no se colocó en una transacción, esto puede ocurrir si otro subproceso elimina el registro de esta sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Se puede devolver si se ha pasado un valor de<em>Precsize</em> <strong>nulo</strong>.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

El tamaño de la clave acumulada en el campo **cbOverhead** de [JET_RECSIZE2](./jet-recsize2-structure.md), se ve afectado por JET_bitRecordSizeInCopyBuffer. Si se especifica este bit, el tamaño de clave acumulado en el campo **cbOverhead** es el tamaño de clave completo. Si no se usa este bit, el tamaño de clave acumulado no incluirá ningún tamaño guardado debido a la compresión de prefijo de clave.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
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
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)
