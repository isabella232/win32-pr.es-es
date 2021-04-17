---
description: 'Más información sobre: enumeración CompactGrbit'
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
ms.openlocfilehash: c7bbe6c88a0a52ab852e3cde9af8871833948949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652487"
---
# <a name="compactgrbit-enumeration"></a>Enumeración CompactGrbit

Opciones para [JetCompact (JET_SESID, cadena, cadena, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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
<td>None</td>
<td>Opciones predeterminadas.</td>
</tr>
<tr class="even">
<td></td>
<td>Estadísticas</td>
<td>Hace que JetCompact vuelque las estadísticas de la base de datos de origen en un archivo denominado DFRGINFO.TXT. Las estadísticas incluyen el nombre de cada tabla en la base de datos de origen, el número de filas de cada tabla, el tamaño total en bytes de todas las filas de cada tabla, el tamaño total en bytes de todas las columnas de tipo <a href="hh577895(v=exchg.10).md">LongText</a> o <a href="hh577895(v=exchg.10).md">LongBinary</a> que eran lo suficientemente grandes como para almacenarse por separado del registro, el número de páginas hoja del índice clúster y el número de páginas Además, también se vuelcan todas las estadísticas de Resumen, incluido el tamaño de la base de datos de origen, la base de datos de destino, el tiempo necesario para la compactación de bases de datos.</td>
</tr>
<tr class="odd">
<td></td>
<td>Reparación</td>
<td><strong>Obsoleto.</strong> Se usa cuando se sabe que la base de datos de origen está dañada. Habilita un conjunto completo de nuevos comportamientos para recuperar tantos datos como sea posible de la base de datos de origen. JetCompact con este conjunto de opciones puede devolver <a href="hh564840(v=exchg.10).md">Success</a> pero no copiar todos los datos creados en la base de datos de origen. Se omitirán los datos que se encontraban en partes dañadas de la base de datos de origen.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
