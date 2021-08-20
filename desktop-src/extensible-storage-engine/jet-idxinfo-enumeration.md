---
description: 'Más información sobre: enumeración JET_IdxInfo datos'
title: JET_IdxInfo enumeración
TOCTitle: JET_IdxInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_IdxInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_idxinfo(v=EXCHG.10)
ms:contentKeyID: 39512789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4447e5e1d7a839b27246121145e820a016eba19f4a4e7c88e487c26782bfc607
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118075210"
---
# <a name="jet_idxinfo-enumeration"></a>JET_IdxInfo enumeración

Niveles de información para recuperar información de índice con JetGetIndexInfo. y JetGetTableIndexInfo.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Enumeration JET_IdxInfo
'Usage
Dim instance As JET_IdxInfo
```

``` csharp
public enum JET_IdxInfo
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
<td>Valor predeterminado</td>
<td>Devuelve una <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> estructura con información sobre el índice.</td>
</tr>
<tr class="even">
<td></td>
<td>List</td>
<td>Devuelve una <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> estructura con información sobre el índice.</td>
</tr>
<tr class="odd">
<td></td>
<td>SysTabCursor</td>
<td><strong>Obsoleto.</strong> SysTabCursor está obsoleto.</td>
</tr>
<tr class="even">
<td></td>
<td>Olc</td>
<td><strong>Obsoleto.</strong> OLC está obsoleto.</td>
</tr>
<tr class="odd">
<td></td>
<td>ResetOLC</td>
<td><strong>Obsoleto.</strong> Restablecer OLC está obsoleto.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceAlloc</td>
<td>Devuelve un entero con el uso de espacio del índice.</td>
</tr>
<tr class="odd">
<td></td>
<td>LCID</td>
<td>Devuelve un entero con el LCID del índice.</td>
</tr>
<tr class="even">
<td></td>
<td>Langid</td>
<td><strong>Obsoleto.</strong> Langid está obsoleto. En su lugar, use LCID.</td>
</tr>
<tr class="odd">
<td></td>
<td>Count</td>
<td>Devuelve un entero con el recuento de índices de la tabla.</td>
</tr>
<tr class="even">
<td></td>
<td>VarSegMac</td>
<td>Devuelve un ushort con el valor de cbVarSegMac con el que se creó el índice.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexId</td>
<td>Devuelve un <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> que identifica el índice.</td>
</tr>
<tr class="even">
<td></td>
<td>KeyMost</td>
<td>Introducido en Windows Vista. Devuelve un ushort con el valor de cbKeyMost con el que se creó el índice.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
