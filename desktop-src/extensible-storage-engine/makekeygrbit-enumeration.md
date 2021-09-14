---
description: 'Más información sobre: Enumeración MakeKeyGrbit'
title: MakeKeyGrbit (enumeración)
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269636"
---
# <a name="makekeygrbit-enumeration"></a>MakeKeyGrbit (enumeración)

Opciones de JetMakeKey.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
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
<td>NewKey</td>
<td>Se debe construir una nueva clave de búsqueda. Se descarta cualquier clave de búsqueda existente anteriormente.</td>
</tr>
<tr class="odd">
<td></td>
<td>NormalizedKey</td>
<td>Cuando se especifica esta opción, se omiten todas las demás opciones, se descarta cualquier clave de búsqueda existente anteriormente y el contenido del búfer de entrada se carga como la nueva clave de búsqueda.</td>
</tr>
<tr class="even">
<td></td>
<td>KeyDataZeroLength</td>
<td>Si el tamaño del búfer de entrada es cero y la columna de clave actual es una columna de longitud variable, esta opción indica que el búfer de entrada contiene un valor de longitud cero. De lo contrario, un tamaño de búfer de entrada de cero indicaría un valor NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>StrLimit</td>
<td>Esta opción indica que la clave de búsqueda debe construirse de forma que todas las columnas de clave que vienen después de la columna de clave actual se consideren caracteres comodín.</td>
</tr>
<tr class="even">
<td></td>
<td>SubStrLimit</td>
<td>Esta opción indica que la clave de búsqueda debe construirse de forma que la columna de clave actual se considere un carácter comodín de prefijo y que las columnas de clave que vienen después de la columna de clave actual se consideren como caracteres comodín.</td>
</tr>
<tr class="odd">
<td></td>
<td>FullColumnStartLimit</td>
<td>La clave de búsqueda debe construirse de forma que todas las columnas de clave que vienen después de la columna de clave actual se consideren caracteres comodín.</td>
</tr>
<tr class="even">
<td></td>
<td>FullColumnEndLimit</td>
<td>La clave de búsqueda debe construirse de forma que las columnas de clave que vienen después de la columna de clave actual se consideren caracteres comodín.</td>
</tr>
<tr class="odd">
<td></td>
<td>PartialColumnStartLimit</td>
<td>La clave de búsqueda debe construirse de forma que la columna de clave actual se considere un carácter comodín de prefijo y que las columnas de clave que vienen después de la columna de clave actual se consideren caracteres comodín.</td>
</tr>
<tr class="even">
<td></td>
<td>PartialColumnEndLimit</td>
<td>La clave de búsqueda debe construirse de forma que la columna de clave actual se considere un carácter comodín de prefijo y que las columnas de clave que vienen después de la columna de clave actual se consideren caracteres comodín.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
