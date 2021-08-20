---
description: 'Más información sobre: JetOSSnapshotPrepareInstance (Función)'
title: JetOSSnapshotPrepareInstance (Función)
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
ms.openlocfilehash: bfd4fc15f3ea7d4f6275f0d4dd31ed96729715b6089397fff7ee73fc7d0c6e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614944"
---
# <a name="jetossnapshotprepareinstance-function"></a>JetOSSnapshotPrepareInstance (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetossnapshotprepareinstance-function"></a>JetOSSnapshotPrepareInstance (Función)

La **función JetOSSnapshotPrepareInstance** selecciona una instancia específica para formar parte de la sesión de instantáneas.

**Windows Vista:** **JetOSSnapshotPrepareInstance** se introdujo en Windows Vista.

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

*Ejemplo*

Instancia de que se usará para esta llamada.

*grbit*

Opciones para esta llamada. Este parámetro se reserva para uso futuro. El único valor válido es 0 (cero).

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

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
<td><p>El puntero de identificador de instantánea <strong>es NULL</strong> o el <em>parámetro grbit</em> no es válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Ya hay una sesión de instantánea en curso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>El identificador de la sesión de instantánea no es válido.</p></td>
</tr>
</tbody>
</table>


Si esta función se realiza correctamente, la instancia especificada formará parte de la sesión de instantáneas.

Si se produce un error en esta función, no se produce ningún cambio en el estado del motor.

#### <a name="remarks"></a>Comentarios

La llamada de secuencia de API normal es: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), seguida opcionalmente de una o varias llamadas a **JetOSSnapshotPrepareInstance** y, a continuación, seguida de [JetOSSnapshotFreeze.](./jetossnapshotfreeze-function.md) Una vez iniciada la inmovilización, se puede finalizar [con JetOSSnapshotThaw](./jetossnapshotthaw-function.md). En cualquier momento después de la preparación, la sesión de instantánea se puede finalizar repentinamente [con JetOSSnapshotAbort.](./jetossnapshotabort-function.md) Las entradas del registro de eventos se generarán para los distintos pasos de la instantánea.

Si no se llama a **JetOSSnapshotPrepareInstance** entre el inicio de la sesión [(JetOSSnapshotPrepare)](./jetossnapshotprepare-function.md)y el momento de inmovilización [(JetOSSnapshotFreeze),](./jetossnapshotfreeze-function.md)todas las instancias en ejecución del motor se inmovilizarán y pasarán a formar parte de la sesión de instantáneas. Esto se produce por dos motivos:

  - Simplifica el código para los usuarios que desean todas las instancias.

  - Permite la compatibilidad con versiones anteriores para los autores de llamadas de las API de instantáneas.

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores extensibles Storage motor de ejecución](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
