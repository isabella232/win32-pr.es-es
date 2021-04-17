---
description: 'Más información sobre: enumeración CreateIndexGrbit'
title: Enumeración CreateIndexGrbit
TOCTitle: CreateIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39511957
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e7a03a077262485533e29690215be1468987e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717103"
---
# <a name="createindexgrbit-enumeration"></a>Enumeración CreateIndexGrbit

Opciones de JetCreateIndex.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateIndexGrbit
'Usage
Dim instance As CreateIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateIndexGrbit
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
<td>IndexUnique</td>
<td>No se permiten entradas de índice duplicadas (claves). Esto se aplica cuando se llama a JetUpdate, no cuando se llama a JetSetColumn.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexPrimary</td>
<td>El índice es un índice principal (clúster). Cada tabla debe tener exactamente un índice principal. Si no se define un índice principal explícitamente en una tabla, el motor de base de datos creará su propio índice principal.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexDisallowNull</td>
<td>Ninguna de las columnas en las que se crea el índice puede contener un valor NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexIgnoreNull</td>
<td>No agregue una entrada de índice para una fila si todas las columnas que se van a indizar son NULL.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexIgnoreAnyNull</td>
<td>No agregue una entrada de índice para una fila si alguna de las columnas que se van a indizar es NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexIgnoreFirstNull</td>
<td>No agregue una entrada de índice para una fila si la primera columna que se va a indizar es NULL.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexLazyFlush</td>
<td>Especifica que las operaciones de índice se registrarán de forma diferida. JET_bitIndexLazyFlush no afecta a la Laziness de las actualizaciones de datos. Si la terminación del proceso interrumpe las operaciones de indexación, la recuperación de software seguirá pudiendo ser capaz de obtener la base de datos en un estado coherente, pero es posible que el índice no esté presente.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexEmpty</td>
<td>No intente compilar el índice, ya que todas las entradas se evaluarían como NULL. grbit también debe especificar JET_bitIgnoreAnyNull cuando se pasa JET_bitIndexEmpty. Se trata de una mejora del rendimiento. Por ejemplo, si se agrega una nueva columna a una tabla, se crea un índice sobre esta columna recién agregada, todos los registros de la tabla se examinarán aunque nunca se agreguen al índice de todos modos. Al especificar JET_bitIndexEmpty se omite el examen de la tabla, lo que podría tardar mucho tiempo.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexUnversioned</td>
<td>Hace que la creación de índices sea visible para otras transacciones. Normalmente, una sesión de una transacción no podrá ver una operación de creación de índices en otra sesión. Esta marca puede ser útil si es probable que otra transacción cree el mismo índice, de modo que el segundo índice-Create simplemente producirá un error en lugar de producir potencialmente muchas operaciones de base de datos innecesarias. Es posible que la segunda transacción no pueda usar el índice inmediatamente. La operación de creación de índices debe completarse antes de poderse usar. La sesión no debe estar actualmente en una transacción para crear un índice sin información de versión.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexSortNullsHigh</td>
<td>Si se especifica esta marca, se ordenarán los valores NULL después de los datos de todas las columnas del índice.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
