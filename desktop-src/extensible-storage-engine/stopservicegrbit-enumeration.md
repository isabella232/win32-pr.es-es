---
description: 'Más información sobre: enumeración StopServiceGrbit'
title: Enumeración StopServiceGrbit (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54e54576dfb1023ec4e3bc55ddd198a77f0ddf25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696608"
---
# <a name="stopservicegrbit-enumeration"></a>Enumeración StopServiceGrbit

Opciones de [JetStopServiceInstance2 (JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a>Miembros

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Nombre del miembro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Todo</td>
<td>Detiene todos los servicios de ESE para la instancia especificada.</td>
</tr>
<tr class="even">
<td></td>
<td>BackgroundUserTasks</td>
<td>Detiene las tareas de mantenimiento de fondo específico del cliente reiniciables (B + desfragmentación de árbol).</td>
</tr>
<tr class="odd">
<td></td>
<td>QuiesceCaches</td>
<td>Quiesces todas las cachés desfasadas en el disco. Asincrónica La inactividad se cancela si se llama al bit de reanudación posteriormente.</td>
</tr>
<tr class="even">
<td></td>
<td>Reanudar</td>
<td>Reanuda las operaciones de StopService emitidas previamente, es decir, &quot; reinicia el servicio &quot; . Se puede combinar con los grbits anteriores para reanudar servicios específicos o con 0X0 reanuda todos los servicios detenidos anteriores.
<p>ADVERTENCIA: este bit solo se puede usar para reanudar JET_bitStopServiceBackground y JET_bitStopServiceQuiesceCaches, si ha realizado una JET_bitStopServiceAll o JET_bitStopServiceAPI, se producirá un error al intentar usar JET_bitStopServiceResume.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
