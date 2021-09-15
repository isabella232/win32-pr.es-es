---
description: 'Más información sobre: Enumeración GetLockGrbit'
title: GetLockGrbit (enumeración)
TOCTitle: GetLockGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetLockGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getlockgrbit(v=EXCHG.10)
ms:contentKeyID: 39512424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cfcad088fa93d73910a0333d3aca9a700e97996
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575073"
---
# <a name="getlockgrbit-enumeration"></a>GetLockGrbit (enumeración)

Opciones de JetGetLock.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetLockGrbit
'Usage
Dim instance As GetLockGrbit
```

``` csharp
[FlagsAttribute]
public enum GetLockGrbit
```

## <a name="members"></a>Members

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
<td>Lectura</td>
<td>Adquiera un bloqueo de lectura en el registro actual. Los bloqueos de lectura no son compatibles con los bloqueos de escritura que ya mantienen otras sesiones, pero son compatibles con los bloqueos de lectura que mantienen otras sesiones.</td>
</tr>
<tr class="even">
<td></td>
<td>Escritura</td>
<td>Adquiera un bloqueo de escritura en el registro actual. Los bloqueos de escritura no son compatibles con los bloqueos de escritura o lectura que mantienen otras sesiones, pero son compatibles con los bloqueos de lectura mantenidos por la misma sesión.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
