---
description: 'Más información acerca de: JET_RECSIZE miembros'
title: Miembros de JET_RECSIZE (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_RECSIZE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_members(v=EXCHG.10)
ms:contentKeyID: 39510137
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 224d22b5dea0447297163fb6b5e1a70fe62a6396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566322"
---
# <a name="jet_recsize-members"></a><span data-ttu-id="f810b-103">Miembros de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="f810b-103">JET_RECSIZE members</span></span>

<span data-ttu-id="f810b-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="f810b-104">Include protected members</span></span>  
<span data-ttu-id="f810b-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="f810b-105">Include inherited members</span></span>  

<span data-ttu-id="f810b-106">Usado por [JetGetRecordSize (JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) para devolver información sobre los requisitos de uso de un registro en el espacio de datos del usuario, el número de columnas establecidas, el número de valores y el espacio de sobrecarga de la estructura de registro esent.</span><span class="sxs-lookup"><span data-stu-id="f810b-106">Used by [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESENT record structure overhead space.</span></span>

<span data-ttu-id="f810b-107">El tipo de [JET_RECSIZE](./jet-recsize-structure2.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="f810b-107">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="f810b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f810b-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f810b-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="f810b-109">Name</span></span></th>
<th><span data-ttu-id="f810b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f810b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f810b-112"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="f810b-112"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="f810b-113">Obtiene el conjunto de datos de usuario del registro.</span><span class="sxs-lookup"><span data-stu-id="f810b-113">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f810b-115"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="f810b-115"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="f810b-116">Obtiene el tamaño comprimido de los datos de usuario en el registro.</span><span class="sxs-lookup"><span data-stu-id="f810b-116">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="f810b-117">Es lo mismo que <a href="hh557581(v=exchg.10).md">cbData</a> si no se comprimen valores largos intrínsecos).</span><span class="sxs-lookup"><span data-stu-id="f810b-117">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f810b-119"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span><span class="sxs-lookup"><span data-stu-id="f810b-119"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="f810b-120">Obtiene el conjunto de datos de usuario del registro, pero almacenado en el árbol de valores largos.</span><span class="sxs-lookup"><span data-stu-id="f810b-120">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f810b-122"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="f810b-122"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="f810b-123">Obtiene el tamaño comprimido de los datos de usuario en el árbol de valores largos.</span><span class="sxs-lookup"><span data-stu-id="f810b-123">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="f810b-124">Es lo mismo que <a href="hh557913(v=exchg.10).md">cbLongValueData</a> si no se comprimen valores largos separados.</span><span class="sxs-lookup"><span data-stu-id="f810b-124">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f810b-126"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span><span class="sxs-lookup"><span data-stu-id="f810b-126"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="f810b-127">Obtiene la sobrecarga de los datos de valor largo.</span><span class="sxs-lookup"><span data-stu-id="f810b-127">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f810b-129"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span><span class="sxs-lookup"><span data-stu-id="f810b-129"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="f810b-130">Obtiene la sobrecarga de la estructura de registro ESENT para este registro.</span><span class="sxs-lookup"><span data-stu-id="f810b-130">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="f810b-131">Esto incluye el tamaño de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="f810b-131">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f810b-133"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span><span class="sxs-lookup"><span data-stu-id="f810b-133"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="f810b-134">Obtiene el número total de columnas del registro que se comprimen.</span><span class="sxs-lookup"><span data-stu-id="f810b-134">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f810b-136"><a href="hh596288(v=exchg.10).md">cLongValues</a></span><span class="sxs-lookup"><span data-stu-id="f810b-136"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="f810b-137">Obtiene el número total de valores Long almacenados en el árbol de valor largo para este registro.</span><span class="sxs-lookup"><span data-stu-id="f810b-137">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="f810b-138">No se incluyen los valores largos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="f810b-138">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f810b-140"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span><span class="sxs-lookup"><span data-stu-id="f810b-140"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="f810b-141">Obtiene la acumulación del número total de valores más allá de la primera para todas las columnas del registro.</span><span class="sxs-lookup"><span data-stu-id="f810b-141">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f810b-143"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="f810b-143"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="f810b-144">Obtiene el número total de columnas fijas y variables establecidas en este registro.</span><span class="sxs-lookup"><span data-stu-id="f810b-144">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f810b-146"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="f810b-146"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="f810b-147">Obtiene el número total de columnas etiquetadas establecidas en este registro.</span><span class="sxs-lookup"><span data-stu-id="f810b-147">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f810b-148">Superior</span><span class="sxs-lookup"><span data-stu-id="f810b-148">Top</span></span>

## <a name="methods"></a><span data-ttu-id="f810b-149">Métodos</span><span class="sxs-lookup"><span data-stu-id="f810b-149">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f810b-150">Nombre</span><span class="sxs-lookup"><span data-stu-id="f810b-150">Name</span></span></th>
<th><span data-ttu-id="f810b-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="f810b-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="f810b-154"><a href="hh538879(v=exchg.10).md">Add (Agregar)</a></span><span class="sxs-lookup"><span data-stu-id="f810b-154"><a href="hh538879(v=exchg.10).md">Add</a></span></span></td>
<td><span data-ttu-id="f810b-155">Agregue los tamaños en dos estructuras de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="f810b-155">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="f810b-157"><a href="hh558506(v=exchg.10).md">Equals (Object)</a></span><span class="sxs-lookup"><span data-stu-id="f810b-157"><a href="hh558506(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="f810b-158">Devuelve un valor que indica si esta instancia es igual a otra instancia de.</span><span class="sxs-lookup"><span data-stu-id="f810b-158">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="f810b-159">(Invalida <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (Object)</a>).</span><span class="sxs-lookup"><span data-stu-id="f810b-159">(Overrides <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="f810b-161"><a href="hh577992(v=exchg.10).md">Es igual a (JET_RECSIZE)</a></span><span class="sxs-lookup"><span data-stu-id="f810b-161"><a href="hh577992(v=exchg.10).md">Equals(JET_RECSIZE)</a></span></span></td>
<td><span data-ttu-id="f810b-162">Devuelve un valor que indica si esta instancia es igual a otra instancia de.</span><span class="sxs-lookup"><span data-stu-id="f810b-162">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="f810b-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="f810b-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="f810b-165">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="f810b-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="f810b-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="f810b-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="f810b-168">Devuelve el código hash de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="f810b-168">Returns the hash code for this instance.</span></span> <span data-ttu-id="f810b-169">(Invalida <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>).</span><span class="sxs-lookup"><span data-stu-id="f810b-169">(Overrides <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="f810b-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="f810b-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="f810b-172">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="f810b-172">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="f810b-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="f810b-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="f810b-175">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="f810b-175">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="f810b-178"><a href="hh579561(v=exchg.10).md">Restar</a></span><span class="sxs-lookup"><span data-stu-id="f810b-178"><a href="hh579561(v=exchg.10).md">Subtract</a></span></span></td>
<td><span data-ttu-id="f810b-179">Calcular la diferencia en tamaños entre dos estructuras JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="f810b-179">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="f810b-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span><span class="sxs-lookup"><span data-stu-id="f810b-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span></span></td>
<td><span data-ttu-id="f810b-182">(Se hereda de <a href="/dotnet/api/system.valuetype">ValueType</a>).</span><span class="sxs-lookup"><span data-stu-id="f810b-182">(Inherited from <a href="/dotnet/api/system.valuetype">ValueType</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f810b-183">Superior</span><span class="sxs-lookup"><span data-stu-id="f810b-183">Top</span></span>

## <a name="operators"></a><span data-ttu-id="f810b-184">Operadores</span><span class="sxs-lookup"><span data-stu-id="f810b-184">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f810b-185">Nombre</span><span class="sxs-lookup"><span data-stu-id="f810b-185">Name</span></span></th>
<th><span data-ttu-id="f810b-186">Descripción</span><span class="sxs-lookup"><span data-stu-id="f810b-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="f810b-189"><a href="hh578675(v=exchg.10).md">Agregado</a></span><span class="sxs-lookup"><span data-stu-id="f810b-189"><a href="hh578675(v=exchg.10).md">Addition</a></span></span></td>
<td><span data-ttu-id="f810b-190">Agregue los tamaños en dos estructuras de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="f810b-190">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="f810b-193"><a href="hh596362(v=exchg.10).md">Igualdad</a></span><span class="sxs-lookup"><span data-stu-id="f810b-193"><a href="hh596362(v=exchg.10).md">Equality</a></span></span></td>
<td><span data-ttu-id="f810b-194">Determina si dos instancias especificadas de JET_RECSIZE son iguales.</span><span class="sxs-lookup"><span data-stu-id="f810b-194">Determines whether two specified instances of JET_RECSIZE are equal.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="f810b-197"><a href="hh578809(v=exchg.10).md">Desigualdad</a></span><span class="sxs-lookup"><span data-stu-id="f810b-197"><a href="hh578809(v=exchg.10).md">Inequality</a></span></span></td>
<td><span data-ttu-id="f810b-198">Determina si dos instancias especificadas de JET_RECSIZE no son iguales.</span><span class="sxs-lookup"><span data-stu-id="f810b-198">Determines whether two specified instances of JET_RECSIZE are not equal.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="f810b-201"><a href="hh596696(v=exchg.10).md">Resta</a></span><span class="sxs-lookup"><span data-stu-id="f810b-201"><a href="hh596696(v=exchg.10).md">Subtraction</a></span></span></td>
<td><span data-ttu-id="f810b-202">Calcular la diferencia en tamaños entre dos estructuras JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="f810b-202">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f810b-203">Superior</span><span class="sxs-lookup"><span data-stu-id="f810b-203">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="f810b-204">Vea también</span><span class="sxs-lookup"><span data-stu-id="f810b-204">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f810b-205">Referencia</span><span class="sxs-lookup"><span data-stu-id="f810b-205">Reference</span></span>

[<span data-ttu-id="f810b-206">Estructura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="f810b-206">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="f810b-207">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="f810b-207">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
