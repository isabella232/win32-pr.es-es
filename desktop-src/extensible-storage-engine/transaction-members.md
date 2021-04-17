---
description: 'Más información acerca de: miembros de transacción'
title: 'Miembros de Transaction '
TOCTitle: Transaction members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_members(v=EXCHG.10)
ms:contentKeyID: 55104159
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4a11aba5d3ffdc8a0e02bd166aa0a433d4860af5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567317"
---
# <a name="transaction-members"></a><span data-ttu-id="51885-103">Miembros de Transaction </span><span class="sxs-lookup"><span data-stu-id="51885-103">Transaction members</span></span>

<span data-ttu-id="51885-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="51885-104">Include protected members</span></span>  
<span data-ttu-id="51885-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="51885-105">Include inherited members</span></span>  

<span data-ttu-id="51885-106">Una clase que encapsula una transacción en un JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="51885-106">A class that encapsulates a transaction on a JET_SESID.</span></span>

<span data-ttu-id="51885-107">El tipo de [transacción](./transaction-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="51885-107">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="51885-108">Constructores</span><span class="sxs-lookup"><span data-stu-id="51885-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="51885-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="51885-109">Name</span></span></th>
<th><span data-ttu-id="51885-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="51885-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="51885-112"><a href="dn351177(v=exchg.10).md">Transacción</a></span><span class="sxs-lookup"><span data-stu-id="51885-112"><a href="dn351177(v=exchg.10).md">Transaction</a></span></span></td>
<td><span data-ttu-id="51885-113">Inicializa una nueva instancia de la clase de transacción.</span><span class="sxs-lookup"><span data-stu-id="51885-113">Initializes a new instance of the Transaction class.</span></span> <span data-ttu-id="51885-114">Esto inicia automáticamente una transacción.</span><span class="sxs-lookup"><span data-stu-id="51885-114">This automatically begins a transaction.</span></span> <span data-ttu-id="51885-115">La transacción se revertirá si no se confirma explícitamente.</span><span class="sxs-lookup"><span data-stu-id="51885-115">The transaction will be rolled back if not explicitly committed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="51885-116">Superior</span><span class="sxs-lookup"><span data-stu-id="51885-116">Top</span></span>

## <a name="properties"></a><span data-ttu-id="51885-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51885-117">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="51885-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="51885-118">Name</span></span></th>
<th><span data-ttu-id="51885-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="51885-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propiedad protegida" alt="Protected property" /></td>
<td><span data-ttu-id="51885-121"><a href="dn350578(v=exchg.10).md">HasResource</a></span><span class="sxs-lookup"><span data-stu-id="51885-121"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="51885-122">Obtiene un valor que indica si el recurso subyacente está asignado actualmente.</span><span class="sxs-lookup"><span data-stu-id="51885-122">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="51885-123">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-123">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="51885-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span><span class="sxs-lookup"><span data-stu-id="51885-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span></span></td>
<td><span data-ttu-id="51885-126">Obtiene un valor que indica si este objeto se encuentra actualmente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="51885-126">Gets a value indicating whether this object is currently in a transaction.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="51885-127">Superior</span><span class="sxs-lookup"><span data-stu-id="51885-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="51885-128">Métodos</span><span class="sxs-lookup"><span data-stu-id="51885-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="51885-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="51885-129">Name</span></span></th>
<th><span data-ttu-id="51885-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="51885-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="51885-132"><a href="dn351172(v=exchg.10).md">Comenzar</a></span><span class="sxs-lookup"><span data-stu-id="51885-132"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="51885-133">Inicia una transacción.</span><span class="sxs-lookup"><span data-stu-id="51885-133">Begin a transaction.</span></span> <span data-ttu-id="51885-134">Este objeto no debe estar actualmente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="51885-134">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="51885-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="51885-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="51885-137">Produce una excepción si este objeto se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="51885-137">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="51885-138">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-138">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="51885-140"><a href="dn351179(v=exchg.10).md">Confirmar (CommitTransactionGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="51885-140"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="51885-141">Confirme una transacción.</span><span class="sxs-lookup"><span data-stu-id="51885-141">Commit a transaction.</span></span> <span data-ttu-id="51885-142">Este objeto debe estar en una transacción.</span><span class="sxs-lookup"><span data-stu-id="51885-142">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="51885-144"><a href="dn351243(v=exchg.10).md">Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span><span class="sxs-lookup"><span data-stu-id="51885-144"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="51885-145">Confirme una transacción.</span><span class="sxs-lookup"><span data-stu-id="51885-145">Commit a transaction.</span></span> <span data-ttu-id="51885-146">Este objeto debe estar en una transacción.</span><span class="sxs-lookup"><span data-stu-id="51885-146">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="51885-148"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="51885-148"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="51885-149">Desechar este objeto, liberando el recurso esent subyacente.</span><span class="sxs-lookup"><span data-stu-id="51885-149">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="51885-150">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-150">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="51885-152"><a href="dn350543(v=exchg.10).md">Dispose (booleano)</a></span><span class="sxs-lookup"><span data-stu-id="51885-152"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="51885-153">Lo llama Dispose y el finalizador.</span><span class="sxs-lookup"><span data-stu-id="51885-153">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="51885-154">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-154">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="51885-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="51885-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="51885-157">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-157">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="51885-159"><a href="dn350552(v=exchg.10).md">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="51885-159"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="51885-160">Finaliza una instancia de la clase EsentResource.</span><span class="sxs-lookup"><span data-stu-id="51885-160">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="51885-161">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-161">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="51885-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="51885-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="51885-164">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="51885-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="51885-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="51885-167">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="51885-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="51885-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="51885-170">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="51885-172"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="51885-172"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="51885-173">Se llama cuando la transacción se desecha mientras está activa.</span><span class="sxs-lookup"><span data-stu-id="51885-173">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="51885-174">Esto debería revertir la transacción.</span><span class="sxs-lookup"><span data-stu-id="51885-174">This should rollback the transaction.</span></span> <span data-ttu-id="51885-175">(Invalida <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-175">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="51885-177"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="51885-177"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="51885-178">Lo llama una subclase cuando se asigna un recurso.</span><span class="sxs-lookup"><span data-stu-id="51885-178">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="51885-179">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-179">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="51885-181"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="51885-181"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="51885-182">Lo llama una subclase cuando se libera un recurso.</span><span class="sxs-lookup"><span data-stu-id="51885-182">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="51885-183">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-183">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="51885-185"><a href="dn351244(v=exchg.10).md">Reversión</a></span><span class="sxs-lookup"><span data-stu-id="51885-185"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="51885-186">Revertir una transacción.</span><span class="sxs-lookup"><span data-stu-id="51885-186">Rollback a transaction.</span></span> <span data-ttu-id="51885-187">Este objeto debe estar en una transacción.</span><span class="sxs-lookup"><span data-stu-id="51885-187">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="51885-189"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="51885-189"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="51885-190">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa la <a href="dn351174(v=exchg.10).md">transacción</a>actual.</span><span class="sxs-lookup"><span data-stu-id="51885-190">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="51885-191">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="51885-191">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="51885-192">Superior</span><span class="sxs-lookup"><span data-stu-id="51885-192">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="51885-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="51885-193">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="51885-194">Referencia</span><span class="sxs-lookup"><span data-stu-id="51885-194">Reference</span></span>

[<span data-ttu-id="51885-195">Transaction, clase</span><span class="sxs-lookup"><span data-stu-id="51885-195">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="51885-196">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="51885-196">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
