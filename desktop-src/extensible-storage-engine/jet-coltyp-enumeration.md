---
description: 'Más información acerca de: enumeración JET_coltyp'
title: Enumeración JET_coltyp
TOCTitle: JET_coltyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_coltyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_coltyp(v=EXCHG.10)
ms:contentKeyID: 39511169
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_coltyp.Nil
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEEDouble
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongBinary
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongText
- Microsoft.Isam.Esent.Interop.JET_coltyp.Text
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEESingle
- Microsoft.Isam.Esent.Interop.JET_coltyp.DateTime
- Microsoft.Isam.Esent.Interop.JET_coltyp.Binary
- Microsoft.Isam.Esent.Interop.JET_coltyp.UnsignedByte
- Microsoft.Isam.Esent.Interop.JET_coltyp.Currency
- Microsoft.Isam.Esent.Interop.JET_coltyp.Bit
- Microsoft.Isam.Esent.Interop.JET_coltyp.Long
- Microsoft.Isam.Esent.Interop.JET_coltyp
- Microsoft.Isam.Esent.Interop.JET_coltyp.Short
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_coltyp.Binary
- Microsoft.Isam.Esent.Interop.JET_coltyp.Short
- Microsoft.Isam.Esent.Interop.JET_coltyp.Bit
- Microsoft.Isam.Esent.Interop.JET_coltyp.UnsignedByte
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEEDouble
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEESingle
- Microsoft.Isam.Esent.Interop.JET_coltyp
- Microsoft.Isam.Esent.Interop.JET_coltyp.Currency
- Microsoft.Isam.Esent.Interop.JET_coltyp.Nil
- Microsoft.Isam.Esent.Interop.JET_coltyp.DateTime
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongBinary
- Microsoft.Isam.Esent.Interop.JET_coltyp.Long
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongText
- Microsoft.Isam.Esent.Interop.JET_coltyp.Text
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 616dc80d835e22502b6781355a2eff35a6375e05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678325"
---
# <a name="jet_coltyp-enumeration"></a>Enumeración JET_coltyp

Tipos de columna ESENT.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Enumeration JET_coltyp
'Usage
Dim instance As JET_coltyp
```

``` csharp
public enum JET_coltyp
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
<td>Nulo</td>
<td>Tipo de columna null. No es válido para la creación de columnas.</td>
</tr>
<tr class="even">
<td></td>
<td>bit</td>
<td>True, false o NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>UnsignedByte</td>
<td>entero de 1 byte, sin signo.</td>
</tr>
<tr class="even">
<td></td>
<td>Short</td>
<td>entero de 2 bytes, con signo.</td>
</tr>
<tr class="odd">
<td></td>
<td>long</td>
<td>entero de 4 bytes, con signo.</td>
</tr>
<tr class="even">
<td></td>
<td>Moneda</td>
<td>entero de 8 bytes, con signo.</td>
</tr>
<tr class="odd">
<td></td>
<td>IEEESingle</td>
<td>una sola precisión IEEE de 4 bytes.</td>
</tr>
<tr class="even">
<td></td>
<td>IEEEDouble</td>
<td>IEEE de doble precisión de 8 bytes.</td>
</tr>
<tr class="odd">
<td></td>
<td>DateTime</td>
<td>Fecha entera, hora fraccionaria.</td>
</tr>
<tr class="even">
<td></td>
<td>Binary</td>
<td>Datos binarios, hasta 255 bytes.</td>
</tr>
<tr class="odd">
<td></td>
<td>Texto</td>
<td>Datos de texto, hasta 255 bytes.</td>
</tr>
<tr class="even">
<td></td>
<td>LongBinary</td>
<td>Datos binarios, hasta 2 GB.</td>
</tr>
<tr class="odd">
<td></td>
<td>LongText</td>
<td>Datos de texto, hasta 2 GB.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
