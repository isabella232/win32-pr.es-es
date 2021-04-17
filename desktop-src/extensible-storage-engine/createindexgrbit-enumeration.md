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
# <a name="createindexgrbit-enumeration"></a><span data-ttu-id="56780-103">Enumeración CreateIndexGrbit</span><span class="sxs-lookup"><span data-stu-id="56780-103">CreateIndexGrbit enumeration</span></span>

<span data-ttu-id="56780-104">Opciones de JetCreateIndex.</span><span class="sxs-lookup"><span data-stu-id="56780-104">Options for JetCreateIndex.</span></span>

<span data-ttu-id="56780-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="56780-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="56780-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="56780-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="56780-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="56780-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="56780-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56780-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="56780-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="56780-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="56780-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="56780-110">Member name</span></span></th>
<th><span data-ttu-id="56780-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="56780-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="56780-112">None</span><span class="sxs-lookup"><span data-stu-id="56780-112">None</span></span></td>
<td><span data-ttu-id="56780-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="56780-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="56780-114">IndexUnique</span><span class="sxs-lookup"><span data-stu-id="56780-114">IndexUnique</span></span></td>
<td><span data-ttu-id="56780-115">No se permiten entradas de índice duplicadas (claves).</span><span class="sxs-lookup"><span data-stu-id="56780-115">Duplicate index entries (keys) are disallowed.</span></span> <span data-ttu-id="56780-116">Esto se aplica cuando se llama a JetUpdate, no cuando se llama a JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="56780-116">This is enforced when JetUpdate is called, not when JetSetColumn is called.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="56780-117">IndexPrimary</span><span class="sxs-lookup"><span data-stu-id="56780-117">IndexPrimary</span></span></td>
<td><span data-ttu-id="56780-118">El índice es un índice principal (clúster).</span><span class="sxs-lookup"><span data-stu-id="56780-118">The index is a primary (clustered) index.</span></span> <span data-ttu-id="56780-119">Cada tabla debe tener exactamente un índice principal.</span><span class="sxs-lookup"><span data-stu-id="56780-119">Every table must have exactly one primary index.</span></span> <span data-ttu-id="56780-120">Si no se define un índice principal explícitamente en una tabla, el motor de base de datos creará su propio índice principal.</span><span class="sxs-lookup"><span data-stu-id="56780-120">If no primary index is explicitly defined over a table, then the database engine will create its own primary index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="56780-121">IndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="56780-121">IndexDisallowNull</span></span></td>
<td><span data-ttu-id="56780-122">Ninguna de las columnas en las que se crea el índice puede contener un valor NULL.</span><span class="sxs-lookup"><span data-stu-id="56780-122">None of the columns over which the index is created may contain a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="56780-123">IndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="56780-123">IndexIgnoreNull</span></span></td>
<td><span data-ttu-id="56780-124">No agregue una entrada de índice para una fila si todas las columnas que se van a indizar son NULL.</span><span class="sxs-lookup"><span data-stu-id="56780-124">Do not add an index entry for a row if all of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="56780-125">IndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="56780-125">IndexIgnoreAnyNull</span></span></td>
<td><span data-ttu-id="56780-126">No agregue una entrada de índice para una fila si alguna de las columnas que se van a indizar es NULL.</span><span class="sxs-lookup"><span data-stu-id="56780-126">Do not add an index entry for a row if any of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="56780-127">IndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="56780-127">IndexIgnoreFirstNull</span></span></td>
<td><span data-ttu-id="56780-128">No agregue una entrada de índice para una fila si la primera columna que se va a indizar es NULL.</span><span class="sxs-lookup"><span data-stu-id="56780-128">Do not add an index entry for a row if the first column being indexed is NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="56780-129">IndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="56780-129">IndexLazyFlush</span></span></td>
<td><span data-ttu-id="56780-130">Especifica que las operaciones de índice se registrarán de forma diferida.</span><span class="sxs-lookup"><span data-stu-id="56780-130">Specifies that the index operations will be logged lazily.</span></span> <span data-ttu-id="56780-131">JET_bitIndexLazyFlush no afecta a la Laziness de las actualizaciones de datos.</span><span class="sxs-lookup"><span data-stu-id="56780-131">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="56780-132">Si la terminación del proceso interrumpe las operaciones de indexación, la recuperación de software seguirá pudiendo ser capaz de obtener la base de datos en un estado coherente, pero es posible que el índice no esté presente.</span><span class="sxs-lookup"><span data-stu-id="56780-132">If the indexing operations is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index may not be present.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="56780-133">IndexEmpty</span><span class="sxs-lookup"><span data-stu-id="56780-133">IndexEmpty</span></span></td>
<td><span data-ttu-id="56780-134">No intente compilar el índice, ya que todas las entradas se evaluarían como NULL.</span><span class="sxs-lookup"><span data-stu-id="56780-134">Do not attempt to build the index, because all entries would evaluate to NULL.</span></span> <span data-ttu-id="56780-135">grbit también debe especificar JET_bitIgnoreAnyNull cuando se pasa JET_bitIndexEmpty.</span><span class="sxs-lookup"><span data-stu-id="56780-135">grbit MUST also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="56780-136">Se trata de una mejora del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="56780-136">This is a performance enhancement.</span></span> <span data-ttu-id="56780-137">Por ejemplo, si se agrega una nueva columna a una tabla, se crea un índice sobre esta columna recién agregada, todos los registros de la tabla se examinarán aunque nunca se agreguen al índice de todos modos.</span><span class="sxs-lookup"><span data-stu-id="56780-137">For example if a new column is added to a table, then an index is created over this newly added column, all of the records in the table would be scanned even though they would never get added to the index anyway.</span></span> <span data-ttu-id="56780-138">Al especificar JET_bitIndexEmpty se omite el examen de la tabla, lo que podría tardar mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="56780-138">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="56780-139">IndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="56780-139">IndexUnversioned</span></span></td>
<td><span data-ttu-id="56780-140">Hace que la creación de índices sea visible para otras transacciones.</span><span class="sxs-lookup"><span data-stu-id="56780-140">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="56780-141">Normalmente, una sesión de una transacción no podrá ver una operación de creación de índices en otra sesión.</span><span class="sxs-lookup"><span data-stu-id="56780-141">Normally a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="56780-142">Esta marca puede ser útil si es probable que otra transacción cree el mismo índice, de modo que el segundo índice-Create simplemente producirá un error en lugar de producir potencialmente muchas operaciones de base de datos innecesarias.</span><span class="sxs-lookup"><span data-stu-id="56780-142">This flag can be useful if another transaction is likely to create the same index, so that the second index-create will simply fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="56780-143">Es posible que la segunda transacción no pueda usar el índice inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="56780-143">The second transaction may not be able to use the index immediately.</span></span> <span data-ttu-id="56780-144">La operación de creación de índices debe completarse antes de poderse usar.</span><span class="sxs-lookup"><span data-stu-id="56780-144">The index creation operation needs to complete before it is usable.</span></span> <span data-ttu-id="56780-145">La sesión no debe estar actualmente en una transacción para crear un índice sin información de versión.</span><span class="sxs-lookup"><span data-stu-id="56780-145">The session must not currently be in a transaction to create an index without version information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="56780-146">IndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="56780-146">IndexSortNullsHigh</span></span></td>
<td><span data-ttu-id="56780-147">Si se especifica esta marca, se ordenarán los valores NULL después de los datos de todas las columnas del índice.</span><span class="sxs-lookup"><span data-stu-id="56780-147">Specifying this flag causes NULL values to be sorted after data for all columns in the index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="56780-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="56780-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="56780-149">Referencia</span><span class="sxs-lookup"><span data-stu-id="56780-149">Reference</span></span>

[<span data-ttu-id="56780-150">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="56780-150">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
