---
description: 'Más información acerca de: JET_SETINFO miembros'
title: Miembros de JET_SETINFO
TOCTitle: JET_SETINFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_members(v=EXCHG.10)
ms:contentKeyID: 55103871
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c782eace916b3871ade67870b08e1766faeafd28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809019"
---
# <a name="jet_setinfo-members"></a><span data-ttu-id="1e246-103">Miembros de JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="1e246-103">JET_SETINFO members</span></span>

<span data-ttu-id="1e246-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="1e246-104">Include protected members</span></span>  
<span data-ttu-id="1e246-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="1e246-105">Include inherited members</span></span>  

<span data-ttu-id="1e246-106">Configuración de JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="1e246-106">Settings for JetSetColumn.</span></span>

<span data-ttu-id="1e246-107">El tipo de [JET_SETINFO](./jet-setinfo-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="1e246-107">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="1e246-108">Constructores</span><span class="sxs-lookup"><span data-stu-id="1e246-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1e246-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="1e246-109">Name</span></span></th>
<th><span data-ttu-id="1e246-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e246-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1e246-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span><span class="sxs-lookup"><span data-stu-id="1e246-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1e246-113">Superior</span><span class="sxs-lookup"><span data-stu-id="1e246-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="1e246-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e246-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1e246-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="1e246-115">Name</span></span></th>
<th><span data-ttu-id="1e246-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e246-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1e246-118"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="1e246-118"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="1e246-119">Obtiene o establece el desplazamiento del primer byte que se va a establecer en una columna de tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> o <a href="hh577895(v=exchg.10).md">LongText</a>.</span><span class="sxs-lookup"><span data-stu-id="1e246-119">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1e246-121"><a href="dn351037(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="1e246-121"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="1e246-122">Obtiene o establece el número de secuencia del valor de una columna con varios valores que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="1e246-122">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="1e246-123">La matriz de valores se basa en uno.</span><span class="sxs-lookup"><span data-stu-id="1e246-123">The array of values is one-based.</span></span> <span data-ttu-id="1e246-124">El primer valor es Sequence 1, no 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="1e246-124">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="1e246-125">Si la columna de registro solo tiene un valor, se debe pasar 1 como itagSequence si ese valor se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="1e246-125">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="1e246-126">Un valor de 0 (cero) significa agregar una nueva instancia de valor de columna al final de la secuencia de valores de columna.</span><span class="sxs-lookup"><span data-stu-id="1e246-126">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1e246-127">Superior</span><span class="sxs-lookup"><span data-stu-id="1e246-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="1e246-128">Métodos</span><span class="sxs-lookup"><span data-stu-id="1e246-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1e246-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="1e246-129">Name</span></span></th>
<th><span data-ttu-id="1e246-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e246-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1e246-132"><a href="dn351060(v=exchg.10).md">ContentEquals</a></span><span class="sxs-lookup"><span data-stu-id="1e246-132"><a href="dn351060(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="1e246-133">Devuelve un valor que indica si esta instancia es igual a otra instancia de.</span><span class="sxs-lookup"><span data-stu-id="1e246-133">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1e246-135"><a href="dn351032(v=exchg.10).md">DeepClone</a></span><span class="sxs-lookup"><span data-stu-id="1e246-135"><a href="dn351032(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="1e246-136">Devuelve una copia en profundidad del objeto.</span><span class="sxs-lookup"><span data-stu-id="1e246-136">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1e246-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="1e246-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="1e246-139">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="1e246-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="1e246-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="1e246-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="1e246-142">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="1e246-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1e246-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="1e246-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="1e246-145">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="1e246-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1e246-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="1e246-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="1e246-148">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="1e246-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="1e246-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="1e246-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="1e246-151">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="1e246-151">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1e246-153"><a href="dn351062(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="1e246-153"><a href="dn351062(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="1e246-154">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa el <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>actual.</span><span class="sxs-lookup"><span data-stu-id="1e246-154">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>.</span></span> <span data-ttu-id="1e246-155">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="1e246-155">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1e246-156">Superior</span><span class="sxs-lookup"><span data-stu-id="1e246-156">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="1e246-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e246-157">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1e246-158">Referencia</span><span class="sxs-lookup"><span data-stu-id="1e246-158">Reference</span></span>

[<span data-ttu-id="1e246-159">JET_SETINFO (clase)</span><span class="sxs-lookup"><span data-stu-id="1e246-159">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="1e246-160">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1e246-160">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
