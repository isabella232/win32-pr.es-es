---
description: 'Más información sobre: Enumeración SeekGrbit'
title: Enumeración SeekGrbit
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e59072055710676f5f7647130f42ad5acf50527
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887193"
---
# <a name="seekgrbit-enumeration"></a>Enumeración SeekGrbit

Opciones de JetSeek.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
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
<td>SeekEQ</td>
<td>El cursor se colocará en la entrada de índice más cercana al inicio del índice que coincida exactamente con la clave de búsqueda.</td>
</tr>
<tr class="even">
<td></td>
<td>SeekLT</td>
<td>El cursor se colocará en la entrada de índice más cercana al final del índice que sea menor que una entrada de índice que coincida exactamente con los criterios de búsqueda.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekLE</td>
<td>El cursor se colocará en la entrada de índice más cercana al final del índice que sea menor o igual que una entrada de índice que coincida exactamente con los criterios de búsqueda.</td>
</tr>
<tr class="even">
<td></td>
<td>SeekGE</td>
<td>El cursor se colocará en la entrada de índice más cercana al inicio del índice que sea mayor o igual que una entrada de índice que coincida exactamente con los criterios de búsqueda.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekGT</td>
<td>El cursor se colocará en la entrada de índice más cercana al inicio del índice que sea mayor que una entrada de índice que coincida exactamente con los criterios de búsqueda.</td>
</tr>
<tr class="even">
<td></td>
<td>SetIndexRange</td>
<td>Se configurará automáticamente un intervalo de índice para todas las claves que coincidan exactamente con la clave de búsqueda.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
