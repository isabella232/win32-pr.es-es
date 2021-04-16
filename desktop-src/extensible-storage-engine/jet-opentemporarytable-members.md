---
description: 'Más información acerca de: JET_OPENTEMPORARYTABLE miembros'
title: Miembros de JET_OPENTEMPORARYTABLE (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_OPENTEMPORARYTABLE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_members(v=EXCHG.10)
ms:contentKeyID: 55104223
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af149ecba6858aca4b4877fc9446872386406838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562825"
---
# <a name="jet_opentemporarytable-members"></a><span data-ttu-id="e8f0e-103">Miembros de JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="e8f0e-103">JET_OPENTEMPORARYTABLE members</span></span>

<span data-ttu-id="e8f0e-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="e8f0e-104">Include protected members</span></span>  
<span data-ttu-id="e8f0e-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="e8f0e-105">Include inherited members</span></span>  

<span data-ttu-id="e8f0e-106">Colección de parámetros para el método JetOpenTemporaryTable.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-106">A collection of parameters for the JetOpenTemporaryTable method.</span></span>

<span data-ttu-id="e8f0e-107">El tipo de [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-107">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="e8f0e-108">Constructores</span><span class="sxs-lookup"><span data-stu-id="e8f0e-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e8f0e-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="e8f0e-109">Name</span></span></th>
<th><span data-ttu-id="e8f0e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8f0e-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e8f0e-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e8f0e-113">Superior</span><span class="sxs-lookup"><span data-stu-id="e8f0e-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="e8f0e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e8f0e-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e8f0e-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="e8f0e-115">Name</span></span></th>
<th><span data-ttu-id="e8f0e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8f0e-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e8f0e-118"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-118"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="e8f0e-119">Obtiene o establece el tamaño máximo para una clave que representa una fila determinada.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-119">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="e8f0e-120">Se puede establecer el tamaño máximo de la clave para controlar cómo se truncan las claves.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-120">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="e8f0e-121">El truncamiento de claves es importante porque puede afectar a la diferencia entre las filas.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-121">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="e8f0e-122">Si este parámetro se establece en 0 o 255, el tamaño de clave máximo y su semántica permanecerán idénticos al tamaño máximo de clave admitido por Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-122">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="e8f0e-123">Este parámetro también se puede establecer en un valor mayor como una función del tamaño de página de la base de datos para la instancia <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-123">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="e8f0e-124">Vea <a href="dn335292(v=exchg.10).md">KeyMost</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-124">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e8f0e-126"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-126"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="e8f0e-127">Obtiene o establece la cantidad máxima de datos que se usarán de cualquier variable lengthcolumn para construir una clave para una fila determinada.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-127">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="e8f0e-128">Este parámetro se puede utilizar para controlar la cantidad de espacio de clave consumida por una columna de clave determinada.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-128">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="e8f0e-129">Este límite se encuentra en bytes.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-129">This limit is in bytes.</span></span> <span data-ttu-id="e8f0e-130">Si este parámetro es cero o es igual que la propiedad <a href="dn335290(v=exchg.10).md">cbKeyMost</a> , no se aplica ningún límite.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-130">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e8f0e-132"><a href="dn335287(v=exchg.10).md">ccolumn</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-132"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="e8f0e-133">Obtiene o establece el número de columnas de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-133">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e8f0e-135"><a href="dn351232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-135"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="e8f0e-136">Obtiene o establece las opciones de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-136">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e8f0e-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="e8f0e-139">Obtiene o establece el identificador de configuración regional y las marcas de normalización que se van a utilizar para comparar los datos de columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-139">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="e8f0e-140">Cuando este parámetro es null, se utilizará el LCID predeterminado para comparar las columnas de clave Unicode de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-140">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="e8f0e-141">El LCID predeterminado es la configuración regional en Inglés de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-141">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="e8f0e-142">Cuando este parámetro es null, se usarán las marcas de normalización predeterminadas para comparar los datos de columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-142">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="e8f0e-143">Las marcas de normalización predeterminadas son: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-143">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e8f0e-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="e8f0e-146">Obtiene o establece las definiciones de columna para las columnas creadas en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-146">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e8f0e-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="e8f0e-149">Obtiene o establece el búfer de salida que recibe la matriz de identificadores de columna generados durante la creación de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-149">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="e8f0e-150">Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-150">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="e8f0e-151">Como resultado, el tamaño de este búfer debe corresponder al tamaño de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-151">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e8f0e-153"><a href="dn335293(v=exchg.10).md">TABLEID</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-153"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="e8f0e-154">Obtiene el identificador de tabla para la tabla temporal creada como resultado de una llamada correcta a JetOpenTemporaryTable.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-154">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e8f0e-155">Superior</span><span class="sxs-lookup"><span data-stu-id="e8f0e-155">Top</span></span>

## <a name="methods"></a><span data-ttu-id="e8f0e-156">Métodos</span><span class="sxs-lookup"><span data-stu-id="e8f0e-156">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e8f0e-157">Nombre</span><span class="sxs-lookup"><span data-stu-id="e8f0e-157">Name</span></span></th>
<th><span data-ttu-id="e8f0e-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8f0e-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e8f0e-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="e8f0e-161">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e8f0e-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="e8f0e-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="e8f0e-164">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e8f0e-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e8f0e-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="e8f0e-167">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e8f0e-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e8f0e-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="e8f0e-170">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e8f0e-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="e8f0e-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="e8f0e-173">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e8f0e-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e8f0e-175"><a href="dn335286(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="e8f0e-175"><a href="dn335286(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="e8f0e-176">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa el <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>actual.</span><span class="sxs-lookup"><span data-stu-id="e8f0e-176">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>.</span></span> <span data-ttu-id="e8f0e-177">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="e8f0e-177">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e8f0e-178">Superior</span><span class="sxs-lookup"><span data-stu-id="e8f0e-178">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="e8f0e-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8f0e-179">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e8f0e-180">Referencia</span><span class="sxs-lookup"><span data-stu-id="e8f0e-180">Reference</span></span>

[<span data-ttu-id="e8f0e-181">JET_OPENTEMPORARYTABLE (clase)</span><span class="sxs-lookup"><span data-stu-id="e8f0e-181">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="e8f0e-182">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="e8f0e-182">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
