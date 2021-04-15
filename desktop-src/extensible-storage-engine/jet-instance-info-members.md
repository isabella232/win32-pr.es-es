---
description: 'Más información acerca de: JET_INSTANCE_INFO miembros'
title: Miembros de JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info_members(v=EXCHG.10)
ms:contentKeyID: 55103693
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 42d9bcd2c078766875fc8230eaf83dc07fdb4b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550145"
---
# <a name="jet_instance_info-members"></a><span data-ttu-id="e4219-103">Miembros de JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="e4219-103">JET_INSTANCE_INFO members</span></span>

<span data-ttu-id="e4219-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="e4219-104">Include protected members</span></span>  
<span data-ttu-id="e4219-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="e4219-105">Include inherited members</span></span>  

<span data-ttu-id="e4219-106">Recibe información sobre la ejecución de instancias de base de datos cuando se usa con las funciones JetGetInstanceInfo y JetOSSnapshotFreeze.</span><span class="sxs-lookup"><span data-stu-id="e4219-106">Receives information about running database instances when used with the JetGetInstanceInfo and JetOSSnapshotFreeze functions.</span></span>

<span data-ttu-id="e4219-107">El tipo de [JET_INSTANCE_INFO](./jet-instance-info-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="e4219-107">The [JET_INSTANCE_INFO](./jet-instance-info-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="e4219-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4219-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e4219-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="e4219-109">Name</span></span></th>
<th><span data-ttu-id="e4219-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4219-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e4219-112"><a href="dn335189(v=exchg.10).md">cDatabases</a></span><span class="sxs-lookup"><span data-stu-id="e4219-112"><a href="dn335189(v=exchg.10).md">cDatabases</a></span></span></td>
<td><span data-ttu-id="e4219-113">Obtiene el número de bases de datos que se adjuntan a la instancia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4219-113">Gets the number of databases that are attached to the database instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e4219-115"><a href="dn335190(v=exchg.10).md">hInstanceId</a></span><span class="sxs-lookup"><span data-stu-id="e4219-115"><a href="dn335190(v=exchg.10).md">hInstanceId</a></span></span></td>
<td><span data-ttu-id="e4219-116">Obtiene el JET_INSTANCE de la instancia de especificada.</span><span class="sxs-lookup"><span data-stu-id="e4219-116">Gets the JET_INSTANCE of the given instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e4219-118"><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></span><span class="sxs-lookup"><span data-stu-id="e4219-118"><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></span></span></td>
<td><span data-ttu-id="e4219-119">Obtiene una colección de cadenas, cada una de las cuales contiene el nombre de archivo de una base de datos que se adjunta a la instancia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4219-119">Gets a collection of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="e4219-120">La matriz tiene elementos cDatabases.</span><span class="sxs-lookup"><span data-stu-id="e4219-120">The array has cDatabases elements.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e4219-122"><a href="dn335194(v=exchg.10).md">szInstanceName</a></span><span class="sxs-lookup"><span data-stu-id="e4219-122"><a href="dn335194(v=exchg.10).md">szInstanceName</a></span></span></td>
<td><span data-ttu-id="e4219-123">Obtiene el nombre de la instancia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4219-123">Gets the name of the database instance.</span></span> <span data-ttu-id="e4219-124">Este valor puede ser null si la instancia de no tiene un nombre.</span><span class="sxs-lookup"><span data-stu-id="e4219-124">This value can be null if the instance does not have a name.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e4219-125">Superior</span><span class="sxs-lookup"><span data-stu-id="e4219-125">Top</span></span>

## <a name="methods"></a><span data-ttu-id="e4219-126">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4219-126">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e4219-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="e4219-127">Name</span></span></th>
<th><span data-ttu-id="e4219-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4219-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e4219-130"><a href="dn335184(v=exchg.10).md">Equals (Object)</a></span><span class="sxs-lookup"><span data-stu-id="e4219-130"><a href="dn335184(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="e4219-131">Devuelve un valor que indica si esta instancia es igual a otra instancia de.</span><span class="sxs-lookup"><span data-stu-id="e4219-131">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="e4219-132">(Invalida <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object. Equals (Object)</a>).</span><span class="sxs-lookup"><span data-stu-id="e4219-132">(Overrides <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e4219-134"><a href="dn335187(v=exchg.10).md">Es igual a (JET_INSTANCE_INFO)</a></span><span class="sxs-lookup"><span data-stu-id="e4219-134"><a href="dn335187(v=exchg.10).md">Equals(JET_INSTANCE_INFO)</a></span></span></td>
<td><span data-ttu-id="e4219-135">Devuelve un valor que indica si esta instancia es igual a otra instancia de.</span><span class="sxs-lookup"><span data-stu-id="e4219-135">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="e4219-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="e4219-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="e4219-138">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e4219-138">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e4219-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="e4219-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="e4219-141">Devuelve el código hash de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="e4219-141">Returns the hash code for this instance.</span></span> <span data-ttu-id="e4219-142">(Invalida <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object. GetHashCode ()</a>).</span><span class="sxs-lookup"><span data-stu-id="e4219-142">(Overrides <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e4219-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="e4219-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="e4219-145">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e4219-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="e4219-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="e4219-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="e4219-148">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e4219-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e4219-150"><a href="dn335192(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="e4219-150"><a href="dn335192(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="e4219-151">Generar una representación de cadena de la instancia.</span><span class="sxs-lookup"><span data-stu-id="e4219-151">Generate a string representation of the instance.</span></span> <span data-ttu-id="e4219-152">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="e4219-152">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e4219-153">Superior</span><span class="sxs-lookup"><span data-stu-id="e4219-153">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="e4219-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4219-154">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e4219-155">Referencia</span><span class="sxs-lookup"><span data-stu-id="e4219-155">Reference</span></span>

[<span data-ttu-id="e4219-156">JET_INSTANCE_INFO (clase)</span><span class="sxs-lookup"><span data-stu-id="e4219-156">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="e4219-157">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e4219-157">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
