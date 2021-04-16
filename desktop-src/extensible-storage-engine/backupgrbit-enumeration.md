---
description: 'Más información sobre: enumeración BackupGrbit'
title: Enumeración BackupGrbit
TOCTitle: BackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.backupgrbit(v=EXCHG.10)
ms:contentKeyID: 39512196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bda9754efcae8ebe353b8272ba57c5640ecdf946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678417"
---
# <a name="backupgrbit-enumeration"></a>Enumeración BackupGrbit

Opciones para [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BackupGrbit
'Usage
Dim instance As BackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BackupGrbit
```

## <a name="members"></a>Miembros

<table>
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
<td>None</td>
<td>Opciones predeterminadas.</td>
</tr>
<tr class="even">
<td></td>
<td>Incremental</td>
<td>Crea una copia de seguridad incremental en lugar de una copia de seguridad completa. Esto significa que solo se realizará una copia de seguridad de los archivos de registro creados desde la última copia de seguridad completa o incremental.</td>
</tr>
<tr class="odd">
<td></td>
<td>Atómico</td>
<td>Crea una copia de seguridad completa de la base de datos. Esto permite conservar una copia de seguridad existente en el mismo directorio si se produce un error en la nueva copia de seguridad.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
