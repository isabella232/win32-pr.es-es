---
description: 'Más información acerca de: miembros de tabla'
title: 'Miembros de Table '
TOCTitle: Table members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Table
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table_members(v=EXCHG.10)
ms:contentKeyID: 55104054
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: b4e5bd09cf1c450197978e3126dc63fe96ec6425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567818"
---
# <a name="table-members"></a><span data-ttu-id="25f2d-103">Miembros de Table </span><span class="sxs-lookup"><span data-stu-id="25f2d-103">Table members</span></span>

<span data-ttu-id="25f2d-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="25f2d-104">Include protected members</span></span>  
<span data-ttu-id="25f2d-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="25f2d-105">Include inherited members</span></span>  

<span data-ttu-id="25f2d-106">Una clase que encapsula una JET_TABLEID en un objeto descartable.</span><span class="sxs-lookup"><span data-stu-id="25f2d-106">A class that encapsulates a JET_TABLEID in a disposable object.</span></span> <span data-ttu-id="25f2d-107">Se abrirá una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="25f2d-107">This opens an existing table.</span></span> <span data-ttu-id="25f2d-108">Para crear una tabla, use el método JetCreateTable.</span><span class="sxs-lookup"><span data-stu-id="25f2d-108">To create a table use the JetCreateTable method.</span></span>

<span data-ttu-id="25f2d-109">El tipo de [tabla](./table-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="25f2d-109">The [Table](./table-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="25f2d-110">Constructores</span><span class="sxs-lookup"><span data-stu-id="25f2d-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="25f2d-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="25f2d-111">Name</span></span></th>
<th><span data-ttu-id="25f2d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="25f2d-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="25f2d-114"><a href="dn351234(v=exchg.10).md">Table</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-114"><a href="dn351234(v=exchg.10).md">Table</a></span></span></td>
<td><span data-ttu-id="25f2d-115">Inicializa una nueva instancia de la clase Table.</span><span class="sxs-lookup"><span data-stu-id="25f2d-115">Initializes a new instance of the Table class.</span></span> <span data-ttu-id="25f2d-116">La tabla se abre desde la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="25f2d-116">The table is opened from the given database.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="25f2d-117">Superior</span><span class="sxs-lookup"><span data-stu-id="25f2d-117">Top</span></span>

## <a name="properties"></a><span data-ttu-id="25f2d-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25f2d-118">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="25f2d-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="25f2d-119">Name</span></span></th>
<th><span data-ttu-id="25f2d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="25f2d-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propiedad protegida" alt="Protected property" /></td>
<td><span data-ttu-id="25f2d-122"><a href="dn350578(v=exchg.10).md">HasResource</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-122"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="25f2d-123">Obtiene un valor que indica si el recurso subyacente está asignado actualmente.</span><span class="sxs-lookup"><span data-stu-id="25f2d-123">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="25f2d-124">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-124">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="25f2d-126"><a href="dn351171(v=exchg.10).md">JetTableid</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-126"><a href="dn351171(v=exchg.10).md">JetTableid</a></span></span></td>
<td><span data-ttu-id="25f2d-127">Obtiene el JET_TABLEID que esta tabla contiene.</span><span class="sxs-lookup"><span data-stu-id="25f2d-127">Gets the JET_TABLEID that this table contains.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="25f2d-129"><a href="dn351170(v=exchg.10).md">Nombre</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-129"><a href="dn351170(v=exchg.10).md">Name</a></span></span></td>
<td><span data-ttu-id="25f2d-130">Obtiene el nombre de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="25f2d-130">Gets the name of this table.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="25f2d-131">Superior</span><span class="sxs-lookup"><span data-stu-id="25f2d-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="25f2d-132">Métodos</span><span class="sxs-lookup"><span data-stu-id="25f2d-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="25f2d-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="25f2d-133">Name</span></span></th>
<th><span data-ttu-id="25f2d-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="25f2d-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="25f2d-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="25f2d-137">Produce una excepción si este objeto se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="25f2d-137">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="25f2d-138">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-138">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="25f2d-140"><a href="dn351235(v=exchg.10).md">Cerrar</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-140"><a href="dn351235(v=exchg.10).md">Close</a></span></span></td>
<td><span data-ttu-id="25f2d-141">Cierre la tabla.</span><span class="sxs-lookup"><span data-stu-id="25f2d-141">Close the table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="25f2d-143"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-143"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="25f2d-144">Desechar este objeto, liberando el recurso esent subyacente.</span><span class="sxs-lookup"><span data-stu-id="25f2d-144">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="25f2d-145">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-145">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="25f2d-147"><a href="dn350543(v=exchg.10).md">Dispose (booleano)</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-147"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="25f2d-148">Lo llama Dispose y el finalizador.</span><span class="sxs-lookup"><span data-stu-id="25f2d-148">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="25f2d-149">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-149">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="25f2d-151"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-151"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="25f2d-152">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-152">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="25f2d-154"><a href="dn350552(v=exchg.10).md">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-154"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="25f2d-155">Finaliza una instancia de la clase EsentResource.</span><span class="sxs-lookup"><span data-stu-id="25f2d-155">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="25f2d-156">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-156">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="25f2d-158"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-158"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="25f2d-159">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-159">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="25f2d-161"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-161"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="25f2d-162">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-162">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="25f2d-164"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-164"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="25f2d-165">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="25f2d-167"><a href="dn351168(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-167"><a href="dn351168(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="25f2d-168">Libere el JET_TABLEID subyacente.</span><span class="sxs-lookup"><span data-stu-id="25f2d-168">Free the underlying JET_TABLEID.</span></span> <span data-ttu-id="25f2d-169">(Invalida <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-169">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="25f2d-171"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-171"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="25f2d-172">Lo llama una subclase cuando se asigna un recurso.</span><span class="sxs-lookup"><span data-stu-id="25f2d-172">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="25f2d-173">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-173">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="25f2d-175"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-175"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="25f2d-176">Lo llama una subclase cuando se libera un recurso.</span><span class="sxs-lookup"><span data-stu-id="25f2d-176">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="25f2d-177">(Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-177">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="25f2d-179"><a href="dn351237(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-179"><a href="dn351237(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="25f2d-180">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa la <a href="dn351163(v=exchg.10).md">tabla</a>actual.</span><span class="sxs-lookup"><span data-stu-id="25f2d-180">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351163(v=exchg.10).md">Table</a>.</span></span> <span data-ttu-id="25f2d-181">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="25f2d-181">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="25f2d-182">Superior</span><span class="sxs-lookup"><span data-stu-id="25f2d-182">Top</span></span>

## <a name="operators"></a><span data-ttu-id="25f2d-183">Operadores</span><span class="sxs-lookup"><span data-stu-id="25f2d-183">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="25f2d-184">Nombre</span><span class="sxs-lookup"><span data-stu-id="25f2d-184">Name</span></span></th>
<th><span data-ttu-id="25f2d-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="25f2d-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="25f2d-188"><a href="dn351239(v=exchg.10).md">Implicit (tabla a JET_TABLEID)</a></span><span class="sxs-lookup"><span data-stu-id="25f2d-188"><a href="dn351239(v=exchg.10).md">Implicit(Table to JET_TABLEID)</a></span></span></td>
<td><span data-ttu-id="25f2d-189">Operador de conversión implícita de una tabla a una JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="25f2d-189">Implicit conversion operator from a Table to a JET_TABLEID.</span></span> <span data-ttu-id="25f2d-190">Esto permite usar una tabla con las API que esperan un JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="25f2d-190">This allows a Table to be used with APIs which expect a JET_TABLEID.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="25f2d-191">Superior</span><span class="sxs-lookup"><span data-stu-id="25f2d-191">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="25f2d-192">Vea también</span><span class="sxs-lookup"><span data-stu-id="25f2d-192">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25f2d-193">Referencia</span><span class="sxs-lookup"><span data-stu-id="25f2d-193">Reference</span></span>

[<span data-ttu-id="25f2d-194">Table (clase)</span><span class="sxs-lookup"><span data-stu-id="25f2d-194">Table class</span></span>](./table-class.md)

[<span data-ttu-id="25f2d-195">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="25f2d-195">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
