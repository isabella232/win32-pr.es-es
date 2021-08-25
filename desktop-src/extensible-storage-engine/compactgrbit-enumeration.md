---
description: 'Más información sobre: Enumeración CompactGrbit'
title: Enumeración CompactGrbit
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a85f3298e4127a35acd5a39839f788fc404269f80a07463bde1417dc04f7fe16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976545"
---
# <a name="compactgrbit-enumeration"></a>Enumeración CompactGrbit

Opciones de [JetCompact(JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit).](./api.jetcompact-method.md)

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
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
<td>Ninguno</td>
<td>Opciones predeterminadas.</td>
</tr>
<tr class="even">
<td></td>
<td>Estadísticas</td>
<td>Hace que JetCompact vuelque las estadísticas de la base de datos de origen en un archivo denominado DFRGINFO.TXT. Las estadísticas incluyen el nombre de cada tabla de la base de datos de origen, el número de filas de cada tabla, el tamaño total en bytes de todas las filas de cada tabla, el tamaño total en bytes de todas las columnas de tipo <a href="hh577895(v=exchg.10).md">LongText</a> o <a href="hh577895(v=exchg.10).md">LongBinary</a> que eran lo suficientemente grandes como para almacenarse independientes del registro, el número de páginas hoja de índice agrupado y el número de páginas hoja de valor largo. Además, también se vuelca el tamaño de la base de datos de origen, la base de datos de destino, el tiempo necesario para la compactación de la base de datos y el espacio temporal de la base de datos.</td>
</tr>
<tr class="odd">
<td></td>
<td>Reparación</td>
<td><strong>Obsoleto.</strong> Se usa cuando se sabe que la base de datos de origen está dañada. Permite un conjunto completo de comportamientos nuevos diseñados para recuperar tantos datos como sea posible de la base de datos de origen. JetCompact con este conjunto de opciones puede devolver <a href="hh564840(v=exchg.10).md">Success,</a> pero no copiar todos los datos creados en la base de datos de origen. Se omitirán los datos que se encontraban en partes dañadas de la base de datos de origen.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
