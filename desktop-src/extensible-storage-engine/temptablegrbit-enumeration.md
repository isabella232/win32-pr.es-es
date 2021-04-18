---
description: 'Más información sobre: enumeración TempTableGrbit'
title: Enumeración TempTableGrbit
TOCTitle: TempTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TempTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.temptablegrbit(v=EXCHG.10)
ms:contentKeyID: 39515065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79247bac6e8d3bda9d1aeac4d19b7af894201a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686760"
---
# <a name="temptablegrbit-enumeration"></a><span data-ttu-id="0808a-103">Enumeración TempTableGrbit</span><span class="sxs-lookup"><span data-stu-id="0808a-103">TempTableGrbit enumeration</span></span>

<span data-ttu-id="0808a-104">Opciones para la creación de una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="0808a-104">Options for temporary table creation.</span></span>

<span data-ttu-id="0808a-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="0808a-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="0808a-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0808a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0808a-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0808a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0808a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0808a-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TempTableGrbit
'Usage
Dim instance As TempTableGrbit
```

``` csharp
[FlagsAttribute]
public enum TempTableGrbit
```

## <a name="members"></a><span data-ttu-id="0808a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0808a-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0808a-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="0808a-110">Member name</span></span></th>
<th><span data-ttu-id="0808a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0808a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0808a-112">None</span><span class="sxs-lookup"><span data-stu-id="0808a-112">None</span></span></td>
<td><span data-ttu-id="0808a-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="0808a-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0808a-114">Indizó</span><span class="sxs-lookup"><span data-stu-id="0808a-114">Indexed</span></span></td>
<td><span data-ttu-id="0808a-115">Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir el uso de JetSeek para buscar registros por clave de índice.</span><span class="sxs-lookup"><span data-stu-id="0808a-115">This option requests that the temporary table be flexible enough to permit the use of JetSeek to lookup records by index key.</span></span> <span data-ttu-id="0808a-116">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="0808a-116">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="0808a-117">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="0808a-117">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0808a-118">Único</span><span class="sxs-lookup"><span data-stu-id="0808a-118">Unique</span></span></td>
<td><span data-ttu-id="0808a-119">Esta opción solicita que los registros con claves de índice duplicadas se quiten del conjunto final de registros de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="0808a-119">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span> <span data-ttu-id="0808a-120">Antes de Windows Server 2003, el motor de base de datos siempre asumió que esta opción está en vigor debido al hecho de que todos los índices clúster también deben ser una clave principal y, por tanto, deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="0808a-120">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="0808a-121">A partir de Windows Server 2003, ahora es posible crear una tabla temporal que no quita los duplicados cuando también se especifica la opción <a href="dn351284(v=exchg.10).md">ForwardOnly</a> .</span><span class="sxs-lookup"><span data-stu-id="0808a-121">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the <a href="dn351284(v=exchg.10).md">ForwardOnly</a> option is also specified.</span></span> <span data-ttu-id="0808a-122">No es posible saber qué duplicado ganará y qué duplicados se descartarán en general.</span><span class="sxs-lookup"><span data-stu-id="0808a-122">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="0808a-123">Sin embargo, cuando se solicita la opción ErrorOnDuplicateInsertion, el primer registro con una clave de índice determinada que se va a insertar en la tabla temporal siempre ganará.</span><span class="sxs-lookup"><span data-stu-id="0808a-123">However, when the ErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0808a-124">Actualizable</span><span class="sxs-lookup"><span data-stu-id="0808a-124">Updatable</span></span></td>
<td><span data-ttu-id="0808a-125">Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir que se modifiquen posteriormente los registros que se han insertado previamente.</span><span class="sxs-lookup"><span data-stu-id="0808a-125">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="0808a-126">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="0808a-126">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="0808a-127">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="0808a-127">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0808a-128">De desplazamiento</span><span class="sxs-lookup"><span data-stu-id="0808a-128">Scrollable</span></span></td>
<td><span data-ttu-id="0808a-129">Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros se examinen en orden y dirección arbitrarios mediante <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span><span class="sxs-lookup"><span data-stu-id="0808a-129">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span> <span data-ttu-id="0808a-130">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="0808a-130">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="0808a-131">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="0808a-131">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0808a-132">SortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="0808a-132">SortNullsHigh</span></span></td>
<td><span data-ttu-id="0808a-133">Esta opción solicita que los valores de columna de clave NULL se ordenen más cerca del final del índice que los valores de columna de clave no NULL.</span><span class="sxs-lookup"><span data-stu-id="0808a-133">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0808a-134">ForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="0808a-134">ForceMaterialization</span></span></td>
<td><span data-ttu-id="0808a-135">Esta opción obliga al administrador de tablas temporales a abandonar cualquier intento de elegir una estrategia de Clever para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="0808a-135">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0808a-136">ErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="0808a-136">ErrorOnDuplicateInsertion</span></span></td>
<td><span data-ttu-id="0808a-137">Esta opción solicita que se produzca inmediatamente un error al intentar insertar un registro con la misma clave de índice que un registro insertado previamente con <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>.</span><span class="sxs-lookup"><span data-stu-id="0808a-137">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>.</span></span> <span data-ttu-id="0808a-138">Si no se solicita esta opción, un duplicado puede detectarse inmediatamente y producir un error, o bien se puede quitar de forma silenciosa más adelante según la estrategia elegida por el motor de base de datos para implementar la tabla temporal en función de la funcionalidad solicitada.</span><span class="sxs-lookup"><span data-stu-id="0808a-138">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span> <span data-ttu-id="0808a-139">Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</span><span class="sxs-lookup"><span data-stu-id="0808a-139">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="0808a-140">Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="0808a-140">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0808a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="0808a-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0808a-142">Referencia</span><span class="sxs-lookup"><span data-stu-id="0808a-142">Reference</span></span>

[<span data-ttu-id="0808a-143">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0808a-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="0808a-144">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="0808a-144">ForwardOnly</span></span>](./server2003grbits.forwardonly-field.md)

[<span data-ttu-id="0808a-145">IntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="0808a-145">IntrinsicLVsOnly</span></span>](./windows7grbits.intrinsiclvsonly-field.md)
