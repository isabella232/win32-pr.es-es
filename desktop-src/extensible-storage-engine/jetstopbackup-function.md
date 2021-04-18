---
description: 'Más información acerca de: JetStopBackup (función)'
title: JetStopBackup función)
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c47a1454e5846fae510a7b91c197d4b180fd14a7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105718583"
---
# <a name="jetstopbackup-function"></a>JetStopBackup función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetstopbackup-function"></a>JetStopBackup función)

La función **JetStopBackup** evita que cualquier actividad relacionada con la copia de seguridad de secuencias continúe en una instancia en ejecución específica, con lo que finaliza la copia de seguridad de streaming de forma predecible.

**Windows XP:**  Esta función se ha introducido en Windows XP.

[JetStopService](./jetstopservice-function.md) es la llamada heredada cuando solo se permite una instancia. En este caso, la única instancia activa es aquella en la que se está preparando la terminación.

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

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
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>No está claro qué instancia se debe preparar para la finalización cuando se usa <a href="gg269240(v=exchg.10).md">JetStopService</a> con el modo de varias instancias.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, la instancia de iniciará la conmutación por error de las nuevas API de copia de seguridad de streaming.

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

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
