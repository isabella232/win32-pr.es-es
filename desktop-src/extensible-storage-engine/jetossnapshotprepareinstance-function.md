---
description: 'Más información acerca de: JetOSSnapshotPrepareInstance (función)'
title: JetOSSnapshotPrepareInstance función)
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc5179a55aabfa3324e3caab7005f4abe437a6d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104424551"
---
# <a name="jetossnapshotprepareinstance-function"></a>JetOSSnapshotPrepareInstance función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetossnapshotprepareinstance-function"></a>JetOSSnapshotPrepareInstance función)

La función **JetOSSnapshotPrepareInstance** selecciona una instancia específica para que forme parte de la sesión de instantáneas.

**Windows Vista:** **JetOSSnapshotPrepareInstance** se presentó en Windows Vista.

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parámetros

*snapId*

Identificador de la sesión de instantánea.

*repetición*

Instancia de que se utilizará para esta llamada.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>El puntero de identificador de instantánea es <strong>null</strong> o el parámetro <em>grbit</em> no es válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Ya hay una sesión de instantánea en curso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>El identificador de la sesión de instantáneas no es válido.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, la instancia especificada formará parte de la sesión de instantáneas.

Si se produce un error en esta función, no se produce ningún cambio en el estado del motor.

#### <a name="remarks"></a>Observaciones

La llamada de secuencia de API normal es: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), seguido, opcionalmente, de una o varias llamadas a **JetOSSnapshotPrepareInstance** y, después, por [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Una vez que se inicia la inmovilización, puede terminarse mediante [JetOSSnapshotThaw](./jetossnapshotthaw-function.md). En cualquier momento después de la preparación, la sesión de instantáneas puede terminar repentinamente con [JetOSSnapshotAbort](./jetossnapshotabort-function.md). Se generarán entradas del registro de eventos para los distintos pasos de la instantánea.

Si no se llama a **JetOSSnapshotPrepareInstance** entre el inicio de la sesión ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) y el momento de la inmovilización ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), todas las instancias en ejecución del motor se inmovilizarán y pasarán a formar parte de la sesión de instantáneas. Esto se produce por dos motivos:

  - Simplifica el código para los usuarios que deseen todas las instancias.

  - Permite la compatibilidad con versiones anteriores de las API de instantáneas.

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

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
