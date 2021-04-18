---
description: 'Más información acerca de: JetOSSnapshotTruncateLog (función)'
title: JetOSSnapshotTruncateLog función)
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0a3cebd743a3c8cd9a3d86f1f637dcb5b2c9c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648587"
---
# <a name="jetossnapshottruncatelog-function"></a>JetOSSnapshotTruncateLog función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetossnapshottruncatelog-function"></a>JetOSSnapshotTruncateLog función)

La función **JetOSSnapshotTruncateLog** habilita el truncamiento del registro para todas las instancias que forman parte de la sesión de instantáneas.

**Windows Vista:**  **JetOSSnapshotTruncateLog** se presentó en Windows Vista.

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
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
<td><p>JET_bitAllDatabasesSnapshot</p></td>
<td><p>Todas las bases de datos están adjuntas para que el motor de almacenamiento pueda calcular y realizar el truncamiento del registro.</p></td>
</tr>
<tr class="even">
<td><p>0 (cero)</p></td>
<td><p>No se producirá ningún truncamiento.</p></td>
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
<td><p>El parámetro <em>grbit</em> no es válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>La sesión de instantáneas no está en el estado en el que puede producirse un truncamiento. Las posibles causas son:</p>
<ul>
<li><p>la llamada se realiza después de que se agote el tiempo de espera de la sesión de instantáneas</p></li>
<li><p>la sesión se especificó como instantánea de copia</p></li>
</ul></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se truncarán los archivos de registro de una o todas las instancias que formen parte de la sesión de instantáneas, si es posible.

#### <a name="remarks"></a>Observaciones

Solo se debe llamar a esta función si la instantánea se creó con la opción JET_bitContinueAfterThaw. De lo contrario, la sesión de instantánea habría finalizado después de la llamada a [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) .

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
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
