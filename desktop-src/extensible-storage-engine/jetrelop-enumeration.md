---
description: 'Más información sobre: Enumeración JetRestone'
title: Enumeración JetRestone (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: JetRelop enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JetRelop
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jetrelop(v=EXCHG.10)
ms:contentKeyID: 55104456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7839e0223eb9dd773ca9a5d10b5210b10b0a944a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126882673"
---
# <a name="jetrelop-enumeration"></a>Enumeración JetRestone

Operación de comparación para el filtro definido [como JET_INDEX_COLUMN](./jet-index-column-class.md).

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Enumeration JetRelop
'Usage
Dim instance As JetRelop
```

``` csharp
public enum JetRelop
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
<td>es igual a</td>
<td>Acepte solo las filas que tengan un valor de columna igual al valor especificado.</td>
</tr>
<tr class="even">
<td></td>
<td>PrefixEquals</td>
<td>Acepte solo las filas que tengan columnas cuyo prefijo coincida con el valor especificado.</td>
</tr>
<tr class="odd">
<td></td>
<td>NotEquals</td>
<td>Acepte solo las filas que tengan un valor de columna que no sea igual al valor especificado.</td>
</tr>
<tr class="even">
<td></td>
<td>LessThanOrEqual</td>
<td>Acepte solo las filas que tengan un valor de columna menor o igual que un valor determinado.</td>
</tr>
<tr class="odd">
<td></td>
<td>LessThan</td>
<td>Acepte solo las filas que tengan un valor de columna menor que un valor determinado.</td>
</tr>
<tr class="even">
<td></td>
<td>GreaterThanOrEqual</td>
<td>Acepte solo las filas que tengan un valor de columna mayor o igual que un valor determinado.</td>
</tr>
<tr class="odd">
<td></td>
<td>GreaterThan</td>
<td>Acepte solo las filas que tengan un valor de columna mayor que un valor determinado.</td>
</tr>
<tr class="even">
<td></td>
<td>Máscara de bitsEqualsZero</td>
<td>Acepte solo las filas que tengan el valor de columna ANDed con una máscara de bits determinada que produce cero.</td>
</tr>
<tr class="odd">
<td></td>
<td>BitmaskNotEqualsZero</td>
<td>Acepte solo las filas que tengan el valor de columna ANDed con una máscara de bits determinada que produce un valor distinto de cero.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
