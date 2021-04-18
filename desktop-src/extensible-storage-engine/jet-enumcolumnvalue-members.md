---
description: 'Más información acerca de: JET_ENUMCOLUMNVALUE miembros'
title: Miembros de JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55103510
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2950caf527af07312f4f27c9464ee4088830fe1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563715"
---
# <a name="jet_enumcolumnvalue-members"></a><span data-ttu-id="715ae-103">Miembros de JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="715ae-103">JET_ENUMCOLUMNVALUE members</span></span>

<span data-ttu-id="715ae-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="715ae-104">Include protected members</span></span>  
<span data-ttu-id="715ae-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="715ae-105">Include inherited members</span></span>  

<span data-ttu-id="715ae-106">Enumera los valores de columna de un registro mediante la función JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="715ae-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="715ae-107">[JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, \[ \] , Int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) devuelve una matriz de estructuras de JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="715ae-107">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="715ae-108">La matriz se devuelve en memoria que se asignó mediante la devolución de llamada que se proporcionó a esa función.</span><span class="sxs-lookup"><span data-stu-id="715ae-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="715ae-109">El tipo de [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="715ae-109">The [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="715ae-110">Constructores</span><span class="sxs-lookup"><span data-stu-id="715ae-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="715ae-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="715ae-111">Name</span></span></th>
<th><span data-ttu-id="715ae-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="715ae-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="715ae-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span><span class="sxs-lookup"><span data-stu-id="715ae-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="715ae-115">Superior</span><span class="sxs-lookup"><span data-stu-id="715ae-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="715ae-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="715ae-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="715ae-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="715ae-117">Name</span></span></th>
<th><span data-ttu-id="715ae-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="715ae-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="715ae-120"><a href="dn335097(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="715ae-120"><a href="dn335097(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="715ae-121">Obtiene el tamaño del valor de columna para la columna.</span><span class="sxs-lookup"><span data-stu-id="715ae-121">Gets the size of the column value for the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="715ae-123"><a href="dn335144(v=exchg.10).md">ERR</a></span><span class="sxs-lookup"><span data-stu-id="715ae-123"><a href="dn335144(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="715ae-124">Obtiene el código de estado de la columna resultante de la enumeración del valor de la columna.</span><span class="sxs-lookup"><span data-stu-id="715ae-124">Gets the column status code resulting from the enumeration of the column value.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="715ae-126"><a href="dn335102(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="715ae-126"><a href="dn335102(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="715ae-127">Obtiene el valor de columna (por índice basado en uno) que se enumeró.</span><span class="sxs-lookup"><span data-stu-id="715ae-127">Gets the column value (by one-based index) that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="715ae-129"><a href="dn335149(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="715ae-129"><a href="dn335149(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="715ae-130">Obtiene el valor que se enumeró para la columna.</span><span class="sxs-lookup"><span data-stu-id="715ae-130">Gets the value that was enumerated for the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="715ae-131">Superior</span><span class="sxs-lookup"><span data-stu-id="715ae-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="715ae-132">Métodos</span><span class="sxs-lookup"><span data-stu-id="715ae-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="715ae-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="715ae-133">Name</span></span></th>
<th><span data-ttu-id="715ae-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="715ae-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="715ae-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="715ae-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="715ae-137">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="715ae-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="715ae-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="715ae-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="715ae-140">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="715ae-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="715ae-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="715ae-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="715ae-143">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="715ae-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="715ae-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="715ae-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="715ae-146">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="715ae-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="715ae-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="715ae-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="715ae-149">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="715ae-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="715ae-151"><a href="dn335096(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="715ae-151"><a href="dn335096(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="715ae-152">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa el <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>actual.</span><span class="sxs-lookup"><span data-stu-id="715ae-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="715ae-153">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="715ae-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="715ae-154">Superior</span><span class="sxs-lookup"><span data-stu-id="715ae-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="715ae-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="715ae-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="715ae-156">Referencia</span><span class="sxs-lookup"><span data-stu-id="715ae-156">Reference</span></span>

[<span data-ttu-id="715ae-157">JET_ENUMCOLUMNVALUE (clase)</span><span class="sxs-lookup"><span data-stu-id="715ae-157">JET_ENUMCOLUMNVALUE class</span></span>](./jet-enumcolumnvalue-class.md)

[<span data-ttu-id="715ae-158">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="715ae-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
