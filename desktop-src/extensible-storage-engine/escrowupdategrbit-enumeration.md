---
description: 'Más información sobre: EscrowUpdateGrbit (enumeración)'
title: EscrowUpdateGrbit (enumeración)
TOCTitle: EscrowUpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.escrowupdategrbit(v=EXCHG.10)
ms:contentKeyID: 39514160
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d301ef801a5685057a9e33beb794f3b6cf13e646
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359079"
---
# <a name="escrowupdategrbit-enumeration"></a>EscrowUpdateGrbit (enumeración)

Opciones de JetEscrowUpdate.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EscrowUpdateGrbit
'Usage
Dim instance As EscrowUpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum EscrowUpdateGrbit
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
<td>None</td>
<td>Opciones predeterminadas.</td>
</tr>
<tr class="even">
<td></td>
<td>NoRollback</td>
<td>Incluso si la sesión que realiza la actualización de custodia tiene su reversión de transacciones, esta actualización no se deshacerá. Como es posible que las entradas de registro no se vacían en el disco, las actualizaciones de custodia recientes realizadas con esta marca pueden perderse si se produce un bloqueo.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
