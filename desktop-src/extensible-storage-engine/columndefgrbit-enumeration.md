---
description: 'Más información sobre: ColumndefGrbit (enumeración)'
title: ColumndefGrbit (enumeración)
TOCTitle: ColumndefGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumndefGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columndefgrbit(v=EXCHG.10)
ms:contentKeyID: 39513005
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c94dcf7d454c5f0ea11fcee0bd46655099dfd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580605"
---
# <a name="columndefgrbit-enumeration"></a>ColumndefGrbit (enumeración)

Opciones para la JET_COLUMNDEF estructura.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ColumndefGrbit
'Usage
Dim instance As ColumndefGrbit
```

``` csharp
[FlagsAttribute]
public enum ColumndefGrbit
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
<td>ColumnFixed</td>
<td>La columna se fijará. Siempre usará la misma cantidad de espacio en una fila, independientemente de la cantidad de datos que se almacenen en la columna. ColumnFixed no se puede usar con ColumnTagged. Este bit no se puede usar con valores long (es decir, JET_coltyp. LongText y JET_coltyp. LongBinary).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnTagged</td>
<td>La columna se etiquetará. Las columnas etiquetadas no ocupa ningún espacio en la base de datos si no contienen datos. Este bit no se puede usar con ColumnFixed.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnNotNULL</td>
<td>La columna nunca debe establecerse en un valor NULL. En Windows XP, esto solo se puede aplicar a columnas fijas (bit, byte, entero, etc.).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnVersion</td>
<td>La columna es una columna de versión que especifica la versión de la fila. El valor de esta columna comienza en cero y se incrementará automáticamente para cada actualización de la fila. Esta opción solo se puede aplicar a JET_coltyp. Columnas largas. Esta opción no se puede usar con ColumnAutoincrement, ColumnEscrowUpdate o ColumnTagged.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnAutoincrement</td>
<td>La columna se incrementará automáticamente. El número es un número creciente y se garantiza que es único dentro de una tabla. Sin embargo, es posible que los números no sean continuos. Por ejemplo, si se insertan cinco filas en una tabla, la columna de creación automática podría contener los valores &quot; &quot; { 1, 2, 6, 7, 8 }. Este bit solo se puede usar en columnas de tipo JET_coltyp. Largo o JET_coltyp. Moneda.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnMultiValued</td>
<td>La columna puede tener varios valores. Una columna con varios valores puede tener cero, uno o varios valores asociados. Los distintos valores de una columna con varios valores se identifican mediante un número denominado miembro itagSequence, que pertenece a varias estructuras, entre las que se incluyen: JET_RETINFO, JET_SETINFO, JET_SETCOLUMN, JET_RETRIEVECOLUMN y JET_ENUMCOLUMNVALUE. Las columnas con varios valores deben ser columnas etiquetadas; es decir, no pueden ser columnas de longitud fija o de longitud variable.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnEscrowUpdate</td>
<td>Especifica que una columna es una columna de actualización de custodia. Diferentes sesiones pueden actualizar simultáneamente una columna de actualización de custodia con JetEscrowUpdate y mantendrá la coherencia transaccional. Una columna de actualización de custodia también debe cumplir las condiciones siguientes: solo se puede crear una columna de actualización de custodia cuando la tabla está vacía. Una columna de actualización de custodia debe ser de tipo JET_coltypLong. Una columna de actualización de custodia debe tener un valor predeterminado. JET_bitColumnEscrowUpdate se puede usar junto con ColumnTagged, ColumnVersion o ColumnAutoincrement.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUnversioned</td>
<td>La columna se creará en sin información de versión. Esto significa que se producirá un error en otras transacciones que intenten agregar una columna con el mismo nombre. Este bit solo es útil con JetAddColumn. No se puede usar dentro de una transacción.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnMaybeNull</td>
<td>Al realizar una combinación externa, es posible que la operación de recuperación de columna no tenga una coincidencia de la tabla interna.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUserDefinedDefault</td>
<td>El valor predeterminado de una columna lo proporciona una función de devolución de llamada. Una columna que tenga un valor predeterminado definido por el usuario debe ser una columna etiquetada. Especificar JET_bitColumnUserDefinedDefault significa que pvDefault debe apuntar a una estructura JET_USERDEFINEDDEFAULT y cbDefault debe establecerse en sizeof( JET_USERDEFINEDDEFAULT ).</td>
</tr>
<tr class="even">
<td></td>
<td>TTKey</td>
<td>La columna será una columna de clave para la tabla temporal. El orden de las definiciones de columna con esta opción especificada en la matriz de entrada determinará la prioridad de cada columna de clave para la tabla temporal. La primera definición de columna de la matriz que tiene esta opción establecida será la columna de clave más importante, y así sucesivamente. Si se solicitan más columnas de clave de las que puede ser compatibles con el motor de base de datos, esta opción se omite para las columnas de clave no admitidas.</td>
</tr>
<tr class="odd">
<td></td>
<td>TTDescending</td>
<td>El criterio de ordenación de la columna de clave de la tabla temporal debe ser descendente en lugar de ascendente. Si esta opción se especifica sin TTKey, se omite esta opción.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

[ColumnCompressed](./windows7grbits.columncompressed-field.md)
