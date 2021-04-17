---
description: 'Más información acerca de: métodos de transacción'
title: 'Métodos de Transaction '
TOCTitle: Transaction methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_methods(v=EXCHG.10)
ms:contentKeyID: 55104163
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c926d00f785aab3a63cd8ebc7eebaf74ea5f0e23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551430"
---
# <a name="transaction-methods"></a><span data-ttu-id="b2f55-103">Métodos de Transaction </span><span class="sxs-lookup"><span data-stu-id="b2f55-103">Transaction methods</span></span>

<span data-ttu-id="b2f55-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="b2f55-104">Include protected members</span></span>  
<span data-ttu-id="b2f55-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="b2f55-105">Include inherited members</span></span>  

<span data-ttu-id="b2f55-106">El tipo de [transacción](./transaction-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="b2f55-106">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="b2f55-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="b2f55-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b2f55-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="b2f55-108">Name</span></span></th>
<th><span data-ttu-id="b2f55-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2f55-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b2f55-111"><a href="dn351172(v=exchg.10).md">Comenzar</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-111"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="b2f55-112">Inicia una transacción.</span><span class="sxs-lookup"><span data-stu-id="b2f55-112">Begin a transaction.</span></span> <span data-ttu-id="b2f55-113">Este objeto no debe estar actualmente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="b2f55-113">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="b2f55-115"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-115"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="b2f55-116">Produce una excepción si este objeto se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="b2f55-116">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="b2f55-117">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="b2f55-117">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b2f55-119"><a href="dn351179(v=exchg.10).md">Confirmar (CommitTransactionGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-119"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="b2f55-120">Confirme una transacción.</span><span class="sxs-lookup"><span data-stu-id="b2f55-120">Commit a transaction.</span></span> <span data-ttu-id="b2f55-121">Este objeto debe estar en una transacción.</span><span class="sxs-lookup"><span data-stu-id="b2f55-121">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b2f55-123"><a href="dn351243(v=exchg.10).md">Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-123"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="b2f55-124">Confirme una transacción.</span><span class="sxs-lookup"><span data-stu-id="b2f55-124">Commit a transaction.</span></span> <span data-ttu-id="b2f55-125">Este objeto debe estar en una transacción.</span><span class="sxs-lookup"><span data-stu-id="b2f55-125">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b2f55-127"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-127"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="b2f55-128">Desechar este objeto, liberando el recurso esent subyacente.</span><span class="sxs-lookup"><span data-stu-id="b2f55-128">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="b2f55-129">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="b2f55-129">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="b2f55-131"><a href="dn350543(v=exchg.10).md">Dispose (booleano)</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-131"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="b2f55-132">Lo llama Dispose y el finalizador.</span><span class="sxs-lookup"><span data-stu-id="b2f55-132">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="b2f55-133">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="b2f55-133">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b2f55-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="b2f55-136">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="b2f55-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="b2f55-138"><a href="dn350552(v=exchg.10).md">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-138"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="b2f55-139">Finaliza una instancia de la clase EsentResource.</span><span class="sxs-lookup"><span data-stu-id="b2f55-139">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="b2f55-140">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="b2f55-140">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b2f55-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="b2f55-143">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="b2f55-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b2f55-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="b2f55-146">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="b2f55-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="b2f55-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="b2f55-149">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="b2f55-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="b2f55-151"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-151"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="b2f55-152">Se llama cuando la transacción se desecha mientras está activa.</span><span class="sxs-lookup"><span data-stu-id="b2f55-152">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="b2f55-153">Esto debería revertir la transacción.</span><span class="sxs-lookup"><span data-stu-id="b2f55-153">This should rollback the transaction.</span></span> <span data-ttu-id="b2f55-154">(Invalida <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>).</span><span class="sxs-lookup"><span data-stu-id="b2f55-154">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="b2f55-156"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-156"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="b2f55-157">Lo llama una subclase cuando se asigna un recurso.</span><span class="sxs-lookup"><span data-stu-id="b2f55-157">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="b2f55-158">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="b2f55-158">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="b2f55-160"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-160"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="b2f55-161">Lo llama una subclase cuando se libera un recurso.</span><span class="sxs-lookup"><span data-stu-id="b2f55-161">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="b2f55-162">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="b2f55-162">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b2f55-164"><a href="dn351244(v=exchg.10).md">Reversión</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-164"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="b2f55-165">Revertir una transacción.</span><span class="sxs-lookup"><span data-stu-id="b2f55-165">Rollback a transaction.</span></span> <span data-ttu-id="b2f55-166">Este objeto debe estar en una transacción.</span><span class="sxs-lookup"><span data-stu-id="b2f55-166">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b2f55-168"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="b2f55-168"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="b2f55-169">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa la <a href="dn351174(v=exchg.10).md">transacción</a>actual.</span><span class="sxs-lookup"><span data-stu-id="b2f55-169">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="b2f55-170">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="b2f55-170">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b2f55-171">Superior</span><span class="sxs-lookup"><span data-stu-id="b2f55-171">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="b2f55-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2f55-172">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b2f55-173">Referencia</span><span class="sxs-lookup"><span data-stu-id="b2f55-173">Reference</span></span>

[<span data-ttu-id="b2f55-174">Transaction, clase</span><span class="sxs-lookup"><span data-stu-id="b2f55-174">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="b2f55-175">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b2f55-175">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
