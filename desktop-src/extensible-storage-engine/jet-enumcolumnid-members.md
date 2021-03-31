---
description: 'Más información acerca de: JET_ENUMCOLUMNID miembros'
title: Miembros de JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_members(v=EXCHG.10)
ms:contentKeyID: 55103504
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f852541d8e16a1a9edfd87afe59a0a8a4c4c4af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104081990"
---
# <a name="jet_enumcolumnid-members"></a><span data-ttu-id="22706-103">Miembros de JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="22706-103">JET_ENUMCOLUMNID members</span></span>

<span data-ttu-id="22706-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="22706-104">Include protected members</span></span>  
<span data-ttu-id="22706-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="22706-105">Include inherited members</span></span>  

<span data-ttu-id="22706-106">Enumera un conjunto específico de columnas y, opcionalmente, un conjunto específico de varios valores para esas columnas cuando se usa la función JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="22706-106">Enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the JetEnumerateColumns function is used.</span></span> <span data-ttu-id="22706-107">JetEnumerateColumns opcionalmente toma una matriz de estructuras JET_ENUMCOLUMNID.</span><span class="sxs-lookup"><span data-stu-id="22706-107">JetEnumerateColumns optionally takes an array of JET_ENUMCOLUMNID structures.</span></span>

<span data-ttu-id="22706-108">El tipo de [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="22706-108">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="22706-109">Constructores</span><span class="sxs-lookup"><span data-stu-id="22706-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="22706-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="22706-110">Name</span></span></th>
<th><span data-ttu-id="22706-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="22706-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="22706-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span><span class="sxs-lookup"><span data-stu-id="22706-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="22706-114">Superior</span><span class="sxs-lookup"><span data-stu-id="22706-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="22706-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22706-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="22706-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="22706-116">Name</span></span></th>
<th><span data-ttu-id="22706-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="22706-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="22706-119"><a href="dn335141(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="22706-119"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="22706-120">Obtiene o establece el identificador de columnid que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="22706-120">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="22706-122"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span><span class="sxs-lookup"><span data-stu-id="22706-122"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="22706-123">Obtiene o establece el recuento de valores de columna (por índice basado en uno) que se va a enumerar para el identificador de columna especificado.</span><span class="sxs-lookup"><span data-stu-id="22706-123">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="22706-124">Si ctagSequence es 0 (cero), se omite rgtagSequence y se enumeran todos los valores de columna para el ID. de columna especificado.</span><span class="sxs-lookup"><span data-stu-id="22706-124">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="22706-126"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span><span class="sxs-lookup"><span data-stu-id="22706-126"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="22706-127">Obtiene o establece la matriz de índices basados en uno en la matriz de valores de columna de una columna determinada.</span><span class="sxs-lookup"><span data-stu-id="22706-127">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="22706-128">Un único elemento es un itagSequence que se define en JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="22706-128">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="22706-129">Un valor de itagSequence de 0 (cero) significa &quot; SKIP &quot; .</span><span class="sxs-lookup"><span data-stu-id="22706-129">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="22706-130">Un itagSequence de 1 significa devolver el valor de la primera columna de la columna, 2 significa el segundo, etc.</span><span class="sxs-lookup"><span data-stu-id="22706-130">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="22706-131">Superior</span><span class="sxs-lookup"><span data-stu-id="22706-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="22706-132">Métodos</span><span class="sxs-lookup"><span data-stu-id="22706-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="22706-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="22706-133">Name</span></span></th>
<th><span data-ttu-id="22706-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="22706-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="22706-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="22706-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="22706-137">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="22706-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="22706-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="22706-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="22706-140">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="22706-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="22706-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="22706-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="22706-143">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="22706-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="22706-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="22706-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="22706-146">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="22706-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="22706-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="22706-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="22706-149">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="22706-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="22706-151"><a href="dn335091(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="22706-151"><a href="dn335091(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="22706-152">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa el <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>actual.</span><span class="sxs-lookup"><span data-stu-id="22706-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>.</span></span> <span data-ttu-id="22706-153">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="22706-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="22706-154">Superior</span><span class="sxs-lookup"><span data-stu-id="22706-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="22706-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="22706-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="22706-156">Referencia</span><span class="sxs-lookup"><span data-stu-id="22706-156">Reference</span></span>

[<span data-ttu-id="22706-157">JET_ENUMCOLUMNID (clase)</span><span class="sxs-lookup"><span data-stu-id="22706-157">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="22706-158">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="22706-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
