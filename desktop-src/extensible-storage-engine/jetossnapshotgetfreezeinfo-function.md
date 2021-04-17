---
description: 'Más información acerca de: JetOSSnapshotGetFreezeInfo (función)'
title: JetOSSnapshotGetFreezeInfo función)
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fbfd3fb31567ea73b8266b5aeba506d62be7714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716601"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a>JetOSSnapshotGetFreezeInfo función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetossnapshotgetfreezeinfo-function"></a>JetOSSnapshotGetFreezeInfo función)

La función **JetOSSnapshotGetFreezeInfo** recupera la lista de instancias y bases de datos que forman parte de la sesión de instantáneas en un momento dado.

**Windows Vista:**  **JetOSSnapshotGetFreezeInfo** se presentó en Windows Vista.

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*snapId*

Identificador de la sesión de instantáneas que se va a iniciar.

*pcInstanceInfo*

El número de instancias que se están ejecutando actualmente y que forman parte de la sesión de instantáneas.

*paInstanceInfo*

Una matriz de estructuras, una para cada instancia en ejecución, que describe la instancia y las bases de datos que forman parte de ella.

*grbit*

Opciones de esta llamada. Este parámetro se reserva para uso futuro. El único valor válido es 0 (cero).

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>Error de la función debido a una condición de memoria insuficiente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p><em>pcInstanceInfo</em> o <em>paInstanceInfo</em> es <strong>null</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>El identificador de la sesión de instantáneas no es válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Una sesión de instantáneas no está en curso.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, la información de la instancia se rellena correctamente y se debe liberar más adelante llamando a [JetFreeBuffer](./jetfreebuffer-function.md) con el puntero a la matriz de información de instancia que se devolvió.

Si se produce un error en esta función, no se produce ningún cambio en el estado del motor.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) y <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
