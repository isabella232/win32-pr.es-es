---
description: 'Más información acerca de: JetIdle (función)'
title: JetIdle función)
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0adf2845997b97eb93b39b779da4ad19bb9ee066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911438"
---
# <a name="jetidle-function"></a>JetIdle función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetidle-function"></a>JetIdle función)

La función **JetIdle** está inactiva y solo debe usarse con fines de prueba. **JetIdle** se puede usar para realizar tareas de limpieza inactiva o comprobar el estado del almacén de versiones en ese.

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

La sesión que se utilizará para esta llamada.

*grbit*

Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los bits siguientes:

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
<td><p>JET_bitIdleCompact</p></td>
<td><p>Desencadena la limpieza del almacén de versiones.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIdleFlushBuffers</p></td>
<td><p>Reservado para uso futuro. Si se especifica esta marca, la API devolverá JET_errInvalidgrbit.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIdleStatus</p></td>
<td><p>Devuelve JET_wrnIdleFull si el almacén de versiones es más de la mitad de llenado.</p></td>
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
<td><p>Un parámetro <em>grbit</em> que se proporcionó a la API no era válido.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, se desencadenará la operación adecuada o un código de error que indique el grado de llenado del almacén de versiones según el valor de *grbit* proporcionado.

Si se produce un error en esta función, la operación solicitada no se completará correctamente.

#### <a name="remarks"></a>Observaciones

El almacén de versiones mantiene el mecanismo de aislamiento de instantáneas de ESE. Si el almacén de versiones es más de la mitad, el programa podría cerrar las transacciones de ejecución prolongada. Si una transacción de ejecución prolongada agota el almacén de versiones, ESE dejará de permitir operaciones de escritura en la base de datos.

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
[JetCommitTransaction](./jetcommittransaction-function.md)
