---
description: 'Más información sobre: JetStopBackup (Función)'
title: JetStopBackup (Función)
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
ms.openlocfilehash: 36b62df437cc7e7b81b699308c1b1d28d9a8ebdb09a352769ea44eb3b836d73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614785"
---
# <a name="jetstopbackup-function"></a>JetStopBackup (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetstopbackup-function"></a>JetStopBackup (Función)

La **función JetStopBackup** impide que cualquier actividad relacionada con la copia de seguridad de streaming continúe en una instancia en ejecución específica, finalizando así la copia de seguridad de streaming de una manera predecible.

**Windows XP:**  Esta función se introduce en Windows XP.

[JetStopService es](./jetstopservice-function.md) la llamada heredada cuando solo se permite una instancia. En este caso, la única instancia activa es la que se está preparando para la terminación.

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

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
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>No está claro qué instancia preparar para la terminación cuando se <a href="gg269240(v=exchg.10).md">usa JetStopService</a> con el modo de varias instancias.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
</tbody>
</table>


Si esta función se realiza correctamente, la instancia comenzará a dar error a las nuevas API de copia de seguridad de streaming.

Si se produce un error en esta función, no se realizará ningún paso para preparar la finalización de la copia de seguridad en la instancia y no se producirá ningún cambio en el estado de la instancia.

#### <a name="remarks"></a>Comentarios

Normalmente, la copia de seguridad se desencadena mediante un evento fuera del mecanismo de proceso y, mediante esta API, la propia aplicación ESENT realizará cualquier otra llamada a las API de copia de seguridad de streaming para producir un error. La mayoría de las API de copia de seguridad de streaming comenzarán a dar error con JET_errBackupAbortByServer. Por lo tanto, cualquier progreso de la copia de seguridad de streaming [(como JetReadFileInstance)](./jetreadfileinstance-function.md)devolverá un error. Todavía se permitirán las operaciones de copia de seguridad que forman parte de la terminación de copia de seguridad (por [ejemplo, JetEndExternalBackupInstance).](./jetendexternalbackupinstance-function.md)

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
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

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
