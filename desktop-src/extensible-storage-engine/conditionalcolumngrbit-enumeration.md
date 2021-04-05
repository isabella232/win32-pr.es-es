---
description: 'Más información sobre: enumeración ConditionalColumnGrbit'
title: Enumeración ConditionalColumnGrbit
TOCTitle: ConditionalColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conditionalcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39513009
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNonNull
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNull
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNonNull
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82828df5d5a25dac08a2a8ab560225456f075a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001367"
---
# <a name="conditionalcolumngrbit-enumeration"></a>Enumeración ConditionalColumnGrbit

Opciones de la estructura de JET_CONDITIONALCOLUMN.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ConditionalColumnGrbit
'Usage
Dim instance As ConditionalColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum ConditionalColumnGrbit
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
<td>ColumnMustBeNull</td>
<td>La columna debe ser null para que una entrada de índice aparezca en el índice.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnMustBeNonNull</td>
<td>La columna no debe ser null para que una entrada de índice aparezca en el índice.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
