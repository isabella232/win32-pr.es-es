---
description: 'Más información sobre: enumeración BeginExternalBackupGrbit'
title: Enumeración BeginExternalBackupGrbit
TOCTitle: BeginExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.beginexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39509773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b68cbfc75d0a71eacedb4bbd462fcd8a93d43690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678415"
---
# <a name="beginexternalbackupgrbit-enumeration"></a>Enumeración BeginExternalBackupGrbit

Opciones de [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md).

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginExternalBackupGrbit
'Usage
Dim instance As BeginExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginExternalBackupGrbit
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
<td>Crea una copia de seguridad incremental en lugar de una copia de seguridad completa. Esto significa que solo se realizará una copia de seguridad de los archivos de registro desde la última copia de seguridad completa o incremental.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
