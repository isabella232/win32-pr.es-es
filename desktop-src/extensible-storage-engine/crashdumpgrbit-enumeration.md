---
description: 'Más información sobre: enumeración CrashDumpGrbit'
title: Enumeración CrashDumpGrbit (Microsoft. ISAM. esent. Interop. Windows7)
TOCTitle: CrashDumpGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.crashdumpgrbit(v=EXCHG.10)
ms:contentKeyID: 39515535
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3108190143115b1e6be5b7e0981d49c4bd9d4afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360447"
---
# <a name="crashdumpgrbit-enumeration"></a>Enumeración CrashDumpGrbit

Opciones de JetConfigureProcessForCrashDump.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CrashDumpGrbit
'Usage
Dim instance As CrashDumpGrbit
```

``` csharp
[FlagsAttribute]
public enum CrashDumpGrbit
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
<td>Mínima</td>
<td>El mínimo de volcado incluye CacheMinimum.</td>
</tr>
<tr class="odd">
<td></td>
<td>Máxima</td>
<td>El máximo de volcado incluye CacheMaximum.</td>
</tr>
<tr class="even">
<td></td>
<td>CacheMinimum</td>
<td>CacheMinimum incluye páginas con bloqueo temporal. CacheMinimum incluye las páginas que se usan para la memoria. CacheMinimum incluye páginas marcadas con errores.</td>
</tr>
<tr class="odd">
<td></td>
<td>CacheMaximum</td>
<td>Caché máxima incluye caché mínima. La memoria caché máxima incluye toda la imagen de caché.</td>
</tr>
<tr class="even">
<td></td>
<td>CacheIncludeDirtyPages</td>
<td>El volcado de memoria incluye páginas modificadas.</td>
</tr>
<tr class="odd">
<td></td>
<td>CacheIncludeCachedPages</td>
<td>El volcado de memoria incluye páginas que contienen datos válidos.</td>
</tr>
<tr class="even">
<td></td>
<td>CacheIncludeCorruptedPages</td>
<td>El volcado de memoria incluye páginas que están dañadas (es caro de calcular).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)
