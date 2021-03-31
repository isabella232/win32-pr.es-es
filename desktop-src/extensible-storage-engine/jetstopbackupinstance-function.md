---
description: 'Más información acerca de: JetStopBackupInstance (función)'
title: JetStopBackupInstance función)
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1813658ed1fb569795bdfa65ccada3ef8ee629c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154003"
---
# <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance función)

La función **JetStopBackupInstance** evita que la actividad relacionada con la copia de seguridad continúe en una instancia en ejecución específica, con lo que finaliza la copia de seguridad de streaming de una manera predecible.

**Windows XP:**  **JetStopBackupInstance** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parámetros

*repetición*

Identifica la instancia en ejecución que se va a usar para la llamada API.

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
<td><p>El parámetro de instancia especificado tiene un valor no válido (no una instancia que se está ejecutando actualmente).</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, la instancia que se especificó comenzará con errores en las nuevas API de copia de seguridad de streaming.

Si se produce un error en esta función, no se realizará ningún paso para preparar la finalización de la copia de seguridad en la instancia de y no se producirá ningún cambio en el estado de la instancia.

#### <a name="remarks"></a>Observaciones

La copia de seguridad se desencadena normalmente mediante un evento fuera del mecanismo de proceso y mediante esta API, la propia aplicación ESENT realizará cualquier llamada posterior a las API de copia de seguridad de streaming para producir un error. La mayoría de las API de copia de seguridad de streaming comenzarán a generar errores con JET_errBackupAbortByServer. Como tal, cualquier progreso de la copia de seguridad de streaming (como [JetReadFileInstance](./jetreadfileinstance-function.md)) devolverá un error. Todavía se permitirán las operaciones de copia de seguridad que forman parte de la finalización de la copia de seguridad (como [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)).

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
[JET_INSTANCE](./jet-instance.md)  
[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
