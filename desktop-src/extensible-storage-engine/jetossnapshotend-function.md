---
description: 'Más información acerca de: JetOSSnapshotEnd (función)'
title: JetOSSnapshotEnd función)
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1237de9af0b1b75f645346fc30a128a1b8e907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153772"
---
# <a name="jetossnapshotend-function"></a>JetOSSnapshotEnd función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetossnapshotend-function"></a>JetOSSnapshotEnd función)

La función **JetOSSnapshotEnd** notifica al motor que la sesión de instantáneas ha finalizado.

**Windows Vista:**  **JetOSSnapshotEnd** se presentó en Windows Vista:.

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*snapId*

Identificador de la sesión de instantánea.

*grbit*

Opciones de esta llamada. Este parámetro puede tener una combinación de los siguientes valores.

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
<td><p>0</p></td>
<td><p>Finalización correcta de la sesión de instantáneas.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitAbortSnapshot</p></td>
<td><p>Se anuló la sesión de instantáneas.</p></td>
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
<td><p>Una de las opciones solicitadas no es válida, se usa incorrectamente o no se ha implementado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Ya hay una sesión de instantánea en curso. Esto no está permitido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>El identificador de la sesión de instantáneas no es válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut</p></td>
<td><p>La sesión de instantáneas tenía un tiempo de espera interno antes de que se produjera esta llamada. Como resultado, las operaciones de e/s devueltas a la normalidad antes de que se realizara esta llamada.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, se completará una sesión de instantáneas y se reanudará el comportamiento normal del motor. Se puede iniciar una nueva sesión de instantáneas más adelante.

Si se produce un error en esta función, el código devuelto JET_errOSSnapshotTimeOut devuelve y la sesión de instantáneas actual finaliza pero no se respeta internamente la inmovilización de IOs durante el período de la instantánea. En el caso de todos los demás errores, no se cambiará el estado de la sesión de instantáneas.

#### <a name="remarks"></a>Observaciones

Solo se llama a esta función si se llamó a [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) con JET_bitContinueAfterThaw.

La sesión de instantánea debe completarse para que tenga lugar la comprobación de la instantánea y el truncamiento del registro. Se generarán entradas del registro de eventos para los distintos pasos de la instantánea.

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
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
