---
description: 'Más información acerca de: JET_ENUMCOLUMN miembros'
title: Miembros de JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103614
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: a1281d7d81fc4e0db476c4ca0f9ac688a7a7b055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559712"
---
# <a name="jet_enumcolumn-members"></a><span data-ttu-id="2c9e5-103">Miembros de JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="2c9e5-103">JET_ENUMCOLUMN members</span></span>

<span data-ttu-id="2c9e5-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="2c9e5-104">Include protected members</span></span>  
<span data-ttu-id="2c9e5-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="2c9e5-105">Include inherited members</span></span>  

<span data-ttu-id="2c9e5-106">Enumera los valores de columna de un registro mediante la función JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="2c9e5-107">JetEnumerateColumns devuelve una matriz de estructuras JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-107">JetEnumerateColumns returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="2c9e5-108">La matriz se devuelve en memoria que se asignó mediante la devolución de llamada que se proporcionó a esa función.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="2c9e5-109">El tipo de [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-109">The [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="2c9e5-110">Constructores</span><span class="sxs-lookup"><span data-stu-id="2c9e5-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2c9e5-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c9e5-111">Name</span></span></th>
<th><span data-ttu-id="2c9e5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c9e5-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="2c9e5-114"><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-114"><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2c9e5-115">Superior</span><span class="sxs-lookup"><span data-stu-id="2c9e5-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="2c9e5-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c9e5-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2c9e5-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c9e5-117">Name</span></span></th>
<th><span data-ttu-id="2c9e5-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c9e5-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="2c9e5-120"><a href="dn335137(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-120"><a href="dn335137(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="2c9e5-121">Obtiene el tamaño del valor que se enumeró para la columna.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-121">Gets the size of the value that was enumerated for the column.</span></span> <span data-ttu-id="2c9e5-122">Este miembro solo se utiliza si el valor de <a href="dn335086(v=exchg.10).md">Err</a> es igual a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-122">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="2c9e5-124"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-124"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="2c9e5-125">Obtiene el número de valores de columna enumerados para la columna.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-125">Gets the number of column values enumerated for the column.</span></span> <span data-ttu-id="2c9e5-126">Este miembro solo se utiliza si <a href="dn335086(v=exchg.10).md">Err</a> no es <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-126">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="2c9e5-128"><a href="dn335135(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-128"><a href="dn335135(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="2c9e5-129">Obtiene el identificador de columnid que se enumeró.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-129">Gets the columnid ID that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="2c9e5-131"><a href="dn335086(v=exchg.10).md">ERR</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-131"><a href="dn335086(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="2c9e5-132">Obtiene el código de estado de la columna que es el resultado de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-132">Gets the column status code that results from the enumeration.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="2c9e5-134"><a href="dn335087(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-134"><a href="dn335087(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="2c9e5-135">Obtiene el valor que se enumeró para la columna.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-135">Gets the value that was enumerated for the column.</span></span> <span data-ttu-id="2c9e5-136">Este miembro solo se utiliza si el valor de <a href="dn335086(v=exchg.10).md">Err</a> es igual a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-136">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span> <span data-ttu-id="2c9e5-137">Esto apunta a la memoria asignada con la devolución de llamada de asignador <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> pasada a <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-137">This points to memory allocated with the <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> allocator callback passed to <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>.</span></span> <span data-ttu-id="2c9e5-138">Recuerde liberar la memoria cuando termine.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-138">Remember to release the memory when finished.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="2c9e5-140"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-140"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="2c9e5-141">Obtiene los valores de la columna enumerada para la columna.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-141">Gets the enumerated column values for the column.</span></span> <span data-ttu-id="2c9e5-142">Este miembro solo se utiliza si <a href="dn335086(v=exchg.10).md">Err</a> no es <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-142">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2c9e5-143">Superior</span><span class="sxs-lookup"><span data-stu-id="2c9e5-143">Top</span></span>

## <a name="methods"></a><span data-ttu-id="2c9e5-144">Métodos</span><span class="sxs-lookup"><span data-stu-id="2c9e5-144">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2c9e5-145">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c9e5-145">Name</span></span></th>
<th><span data-ttu-id="2c9e5-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c9e5-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="2c9e5-148"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-148"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="2c9e5-149">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="2c9e5-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="2c9e5-151"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-151"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="2c9e5-152">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="2c9e5-152">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="2c9e5-154"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-154"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="2c9e5-155">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="2c9e5-155">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="2c9e5-157"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-157"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="2c9e5-158">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="2c9e5-158">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="2c9e5-160"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-160"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="2c9e5-161">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="2c9e5-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="2c9e5-163"><a href="dn335132(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="2c9e5-163"><a href="dn335132(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="2c9e5-164">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa el <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>actual.</span><span class="sxs-lookup"><span data-stu-id="2c9e5-164">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>.</span></span> <span data-ttu-id="2c9e5-165">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="2c9e5-165">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2c9e5-166">Superior</span><span class="sxs-lookup"><span data-stu-id="2c9e5-166">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="2c9e5-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c9e5-167">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2c9e5-168">Referencia</span><span class="sxs-lookup"><span data-stu-id="2c9e5-168">Reference</span></span>

[<span data-ttu-id="2c9e5-169">JET_ENUMCOLUMN (clase)</span><span class="sxs-lookup"><span data-stu-id="2c9e5-169">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="2c9e5-170">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2c9e5-170">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
