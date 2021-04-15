---
description: 'Más información sobre: enumeración SetColumnGrbit'
title: Enumeración SetColumnGrbit
TOCTitle: SetColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39509934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893f8e79b910a305bf6caccacd2d928e947be693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497674"
---
# <a name="setcolumngrbit-enumeration"></a>Enumeración SetColumnGrbit

Opciones de JetSetColumn.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetColumnGrbit
'Usage
Dim instance As SetColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum SetColumnGrbit
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
<td>AppendLV</td>
<td>Esta opción se utiliza para anexar datos a una columna de tipo JET_coltypLongText o JET_coltypLongBinary. Se puede lograr el mismo comportamiento determinando el tamaño del valor Long existente y especificando ibLongValue en psetinfo. Sin embargo, es más sencillo usar esta grbit, ya que no es necesario conocer el tamaño del valor de la columna existente.</td>
</tr>
<tr class="odd">
<td></td>
<td>OverwriteLV</td>
<td>Esta opción se usa para reemplazar el valor Long existente con los datos proporcionados recientemente. Cuando se usa esta opción, es como si el valor Long existente se hubiera establecido en la longitud 0 (cero) antes de establecer los datos nuevos.</td>
</tr>
<tr class="even">
<td></td>
<td>RevertToDefaultValue</td>
<td>Esta opción solo es aplicable para columnas etiquetadas, dispersas o con varios valores. Hace que la columna devuelva el valor de columna predeterminado en operaciones de recuperación de columna posteriores. Se quitan todos los valores de columna existentes.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeparateLV</td>
<td>Esta opción se usa para forzar un valor largo, las columnas de tipo JET_coltyp. LongText o JET_coltyp. LongBinary, que se almacenará de forma independiente del resto de datos de registro. Esto ocurre normalmente cuando el tamaño del valor Long impide que se almacene con los datos de registro restantes. Sin embargo, esta opción se puede usar para forzar el almacenamiento del valor largo por separado. Tenga en cuenta que no se puede forzar la separación de los valores Long de cuatro bytes de menor tamaño. En estos casos, se omite la opción.</td>
</tr>
<tr class="even">
<td></td>
<td>SizeLV</td>
<td>Esta opción se usa para interpretar el búfer de entrada como un número entero de bytes que se establecerá como la longitud del valor largo descrito por el columnid determinado y, si se proporciona, el número de secuencia en psetinfo- &gt; itagSequence. Si el tamaño dado es mayor que el valor de columna existente, la columna se extenderá con 0s. Si el tamaño es menor que el valor de la columna existente, el valor se truncará.</td>
</tr>
<tr class="odd">
<td></td>
<td>UniqueMultiValues</td>
<td>Esta opción se utiliza para exigir que todos los valores de una columna con varios valores sean distintos. Esta opción compara los datos de la columna de origen, sin ninguna transformación, con otros valores de columna existentes y se devuelve un error si se encuentra un duplicado. Si se proporciona esta opción, AppendLV, OverwriteLV y SizeLV también no se pueden proporcionar.</td>
</tr>
<tr class="even">
<td></td>
<td>UniqueNormalizedMultiValues</td>
<td>Esta opción se utiliza para exigir que todos los valores de una columna con varios valores sean distintos. Esta opción compara la transformación normalizada clave de datos de columna con otros valores de columna existentes transformados de forma similar y se devuelve un error si se encuentra un duplicado. Si se proporciona esta opción, AppendLV, OverwriteLV y SizeLV también no se pueden proporcionar.</td>
</tr>
<tr class="odd">
<td></td>
<td>ZeroLength</td>
<td>Esta opción se usa para establecer un valor de longitud cero. Normalmente, un valor de columna se establece en NULL pasando un cbMax de 0 (cero). Sin embargo, para algunos tipos, como JET_coltyp. Text, un valor de columna puede tener una longitud de 0 (cero) en lugar de NULL, y esta opción se utiliza para diferenciar entre la longitud NULL y 0 (cero).</td>
</tr>
<tr class="even">
<td></td>
<td>IntrinsicLV</td>
<td>Intente almacenar columnas de valores largos en el registro, incluso si superan el tamaño de la separación predeterminada.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

[Compressed](./windows7grbits.compressed-field.md)

[Sin comprimir](./windows7grbits.uncompressed-field.md)
