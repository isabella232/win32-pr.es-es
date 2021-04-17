---
description: 'Más información sobre: enumeración EnumerateColumnsGrbit'
title: Enumeración EnumerateColumnsGrbit
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e27e6810b37b513d550bbafce509b2815ccea2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717097"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a>Enumeración EnumerateColumnsGrbit

Opciones de JetEnumerateColumns.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a>Miembros

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
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
<td>EnumerateCompressOutput</td>
<td>Al enumerar los valores de columna, todas las columnas para las que se recuperan todos los valores y que solo tienen un valor de columna que no es NULL pueden devolverse en un formato comprimido. El estado de estas columnas se establecerá en <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> y el tamaño del valor de la columna y la memoria que contiene el valor de la columna se devolverán directamente en la estructura <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> . No se garantiza que todas las columnas coincidentes se compriman de esta manera. Consulte <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> para obtener más información.</td>
</tr>
<tr class="odd">
<td></td>
<td>EnumerateCopy</td>
<td>Esta opción indica que los valores de columna modificados del registro se deben enumerar en lugar de los valores de columna originales. Si un valor de columna no se ha modificado, se enumera el valor de la columna original. De esta manera, se puede enumerar un valor de columna que todavía no se ha insertado o actualizado al insertar o actualizar un registro.
<p>Esta opción es idéntica a <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</p></td>
</tr>
<tr class="even">
<td></td>
<td>EnumerateIgnoreDefault</td>
<td>Si una columna determinada no está presente en el registro, no se devolverá ningún valor de columna. Normalmente, el valor predeterminado de la columna, si existe, se devolvería en este caso. Se garantiza que, si la columna se establece en un valor distinto del valor predeterminado, se devolverá un valor diferente (es decir, si una columna con un valor predeterminado se establece explícitamente en NULL, se devolverá un valor NULL como valor para esa columna). Aunque se solicite esta opción, sigue siendo posible ver un valor de columna que sea igual al valor predeterminado. No se realiza ningún esfuerzo para quitar los valores de columna que coincidan con sus valores predeterminados. Es importante recordar que esta opción afecta a la salida de <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> cuando se usa con EnumeratePresenceOnly o EnumerateTaggedOnly.</td>
</tr>
<tr class="odd">
<td></td>
<td>EnumeratePresenceOnly</td>
<td>Si existe un valor no NULL para el valor de columna o columna solicitado, no se devuelven los datos asociados. En su lugar, el estado asociado para ese valor de columna o columna se establecerá en <a href="hh557250(v=exchg.10).md">ColumnPresent</a>. Si el valor de la columna o columna es NULL, <a href="hh557250(v=exchg.10).md">ColumnNull</a> se devolverá como de costumbre.</td>
</tr>
<tr class="even">
<td></td>
<td>EnumerateTaggedOnly</td>
<td>Al enumerar todos los valores de columna del registro (por ejemplo, es cuando numColumnids es cero), solo se devolverán los valores de columna etiquetada. Esta opción no está permitida cuando se enumera una matriz de identificadores de columna específica.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

[EnumerateIgnoreUserDefinedDefault](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[EnumerateInRecordOnly](./windows7grbits.enumerateinrecordonly-field.md)
