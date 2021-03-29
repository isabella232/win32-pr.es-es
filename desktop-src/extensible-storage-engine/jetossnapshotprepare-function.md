---
description: 'Más información acerca de: JetOSSnapshotPrepare (función)'
title: Función JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ccf9a5b21ccb9a4f94ba5aa4f995e4bb9017bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648535"
---
# <a name="jetossnapshotprepare-function"></a>Función JetOSSnapshotPrepare


_**Se aplica a:** Windows | Windows Server_

## <a name="jetossnapshotprepare-function"></a>Función JetOSSnapshotPrepare

La función **JetOSSnapshotPrepare** inicia los preparativos para una sesión de instantánea. Una sesión de instantáneas es un breve intervalo de tiempo en el que el motor no emite ninguna e/s de escritura en el disco, de modo que el motor puede participar en una sesión de instantáneas de volumen (cuando está controlada por un escritor de instantáneas).

**Windows XP:**  **JetOSSnapshotPrepare** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*psnapId*

Identificador de la sesión de instantáneas que se va a iniciar.

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
<td><p>Instantánea normal.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIncrementalSnapshot</p></td>
<td><p>Solo se tomarán los archivos de registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitCopySnapshot</p></td>
<td><p>Una instantánea de copia (normal o incremental) sin truncamiento del registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitContinueAfterThaw</p></td>
<td><p>La sesión de instantáneas se produce después de <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> y requerirá una llamada a la función <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitExplicitPrepare</p></td>
<td><p>No se preparará ninguna instancia de forma predeterminada.</p>
<p><strong>Windows 7:</strong>  JET_bitExplicitPrepare se presenta en Windows 7.</p></td>
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
<td><p>JET_errInvalidParameter</p></td>
<td><p>El puntero de identificador de instantánea es NULL o el parámetro <em>grbit</em> no es válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Ya hay una sesión de instantánea en curso y la operación no puede tener más de una sesión de instantáneas en un momento dado.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, una sesión de instantáneas podrá iniciarse en cualquier momento con la fase de inmovilización de e/s. Se devolverá el identificador de la sesión y se debe usar en las llamadas subsiguientes para la sesión de instantáneas.

Las instancias en ejecución del motor se considerarán parte de la sesión de instantáneas.

**Windows Vista:**  Para especificar un subconjunto diferente de instancias, se puede llamar a [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) .

La llamada de secuencia de API normal es: **JetOSSnapshotPrepare**, seguido, opcionalmente, de una o varias llamadas a [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)y, después, por [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Una vez que se inicia la inmovilización, puede terminarse mediante [JetOSSnapshotThaw](./jetossnapshotthaw-function.md). En cualquier momento después de la preparación, la sesión de instantáneas puede terminar repentinamente con [JetOSSnapshotAbort](./jetossnapshotabort-function.md).

Si se especifica JET_bitContinueAfterThaw después de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), se conservará la sesión de instantáneas (aunque se reanudará la e/s). Esto habilitará una comprobación de la instantánea y, si es necesario, habilitará el truncamiento del registro mediante [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) y requerirá una llamada a [JetOSSnapshotEnd](./jetossnapshotend-function.md).

Si se produce un error en esta función, no se produce ningún cambio en el estado del motor.

#### <a name="remarks"></a>Observaciones

Se generarán entradas del registro de eventos para los distintos pasos de la instantánea.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
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
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)  
[JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md)
