---
description: 'Más información acerca de: JET_INDEXCREATE miembros'
title: Miembros de JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_members(v=EXCHG.10)
ms:contentKeyID: 55103641
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbe9ce962221db30c8cdae90461fa55fc0baea19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278667"
---
# <a name="jet_indexcreate-members"></a><span data-ttu-id="ff8de-103">Miembros de JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="ff8de-103">JET_INDEXCREATE members</span></span>

<span data-ttu-id="ff8de-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="ff8de-104">Include protected members</span></span>  
<span data-ttu-id="ff8de-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="ff8de-105">Include inherited members</span></span>  

<span data-ttu-id="ff8de-106">Contiene la información necesaria para crear un índice sobre los datos en una base de datos ESE.</span><span class="sxs-lookup"><span data-stu-id="ff8de-106">Contains the information needed to create an index over data in an ESE database.</span></span> <span data-ttu-id="ff8de-107">Contiene la información necesaria para crear un índice sobre los datos en una base de datos ESE.</span><span class="sxs-lookup"><span data-stu-id="ff8de-107">Contains the information needed to create an index over data in an ESE database.</span></span>

<span data-ttu-id="ff8de-108">El tipo de [JET_INDEXCREATE](./jet-indexcreate-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="ff8de-108">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="ff8de-109">Constructores</span><span class="sxs-lookup"><span data-stu-id="ff8de-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ff8de-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="ff8de-110">Name</span></span></th>
<th><span data-ttu-id="ff8de-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff8de-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ff8de-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ff8de-114">Superior</span><span class="sxs-lookup"><span data-stu-id="ff8de-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="ff8de-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff8de-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ff8de-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="ff8de-116">Name</span></span></th>
<th><span data-ttu-id="ff8de-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff8de-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ff8de-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="ff8de-120">Obtiene o establece la longitud, en caracteres, de szKey, incluidos los dos valores NULL de terminación.</span><span class="sxs-lookup"><span data-stu-id="ff8de-120">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ff8de-122"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-122"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="ff8de-123">Obtiene o establece el tamaño máximo permitido, en bytes, para las claves del índice.</span><span class="sxs-lookup"><span data-stu-id="ff8de-123">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="ff8de-124">El tamaño máximo de clave compatible mínimo es JET_cbKeyMostMin (255), que es el tamaño de clave máximo heredado.</span><span class="sxs-lookup"><span data-stu-id="ff8de-124">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="ff8de-125">El tamaño máximo de la clave depende del tamaño de página de la base de datos <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="ff8de-125">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="ff8de-126">El tamaño máximo de la clave se puede recuperar con <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span><span class="sxs-lookup"><span data-stu-id="ff8de-126">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="ff8de-127">Este parámetro se omite en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ff8de-127">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="ff8de-128">A diferencia de la API no administrada, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) no es necesario, sino que se agregará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ff8de-128">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ff8de-130"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-130"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="ff8de-131">Obtiene o establece la longitud máxima, en bytes, de cada columna que se va a almacenar en el índice.</span><span class="sxs-lookup"><span data-stu-id="ff8de-131">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ff8de-133"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-133"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="ff8de-134">Obtiene o establece el número de columnas condicionales.</span><span class="sxs-lookup"><span data-stu-id="ff8de-134">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ff8de-136"><a href="dn335157(v=exchg.10).md">ERR</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-136"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="ff8de-137">Obtiene o establece el código de error de la creación de este índice.</span><span class="sxs-lookup"><span data-stu-id="ff8de-137">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ff8de-139"><a href="dn335119(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-139"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="ff8de-140">Obtiene o establece las opciones de creación de índices.</span><span class="sxs-lookup"><span data-stu-id="ff8de-140">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ff8de-142"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-142"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="ff8de-143">Obtiene o establece las opciones de comparación Unicode opcionales.</span><span class="sxs-lookup"><span data-stu-id="ff8de-143">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ff8de-145"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-145"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="ff8de-146">Obtiene o establece las sugerencias de asignación, mantenimiento y uso de espacio.</span><span class="sxs-lookup"><span data-stu-id="ff8de-146">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ff8de-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="ff8de-149">Obtiene o establece las columnas condicionales opcionales.</span><span class="sxs-lookup"><span data-stu-id="ff8de-149">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ff8de-151"><a href="dn335121(v=exchg.10).md">szIndexName</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-151"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="ff8de-152">Obtiene o establece el nombre del índice que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="ff8de-152">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ff8de-154"><a href="dn335161(v=exchg.10).md">szKey</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-154"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="ff8de-155">Obtiene o establece la descripción de la clave de índice.</span><span class="sxs-lookup"><span data-stu-id="ff8de-155">Gets or sets the description of the index key.</span></span> <span data-ttu-id="ff8de-156">Se trata de una cadena doble terminada en NULL de tokens delimitados por null.</span><span class="sxs-lookup"><span data-stu-id="ff8de-156">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="ff8de-157">Cada token tiene la forma [Direction-Specifier] [column-Name], donde Direction-Specification es &quot; + &quot; o &quot; - &quot; .</span><span class="sxs-lookup"><span data-stu-id="ff8de-157">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="ff8de-158">por ejemplo, un szKey de &quot; + abc\0-def\0 + ghi\0 &quot; indexará las tres columnas &quot; ABC &quot; (en orden ascendente), &quot; Def &quot; (en orden descendente) y &quot; GHI &quot; (en orden ascendente).</span><span class="sxs-lookup"><span data-stu-id="ff8de-158">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="ff8de-160"><a href="dn335162(v=exchg.10).md">ulDensity</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-160"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="ff8de-161">Obtiene o establece la densidad del índice.</span><span class="sxs-lookup"><span data-stu-id="ff8de-161">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ff8de-162">Superior</span><span class="sxs-lookup"><span data-stu-id="ff8de-162">Top</span></span>

## <a name="methods"></a><span data-ttu-id="ff8de-163">Métodos</span><span class="sxs-lookup"><span data-stu-id="ff8de-163">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ff8de-164">Nombre</span><span class="sxs-lookup"><span data-stu-id="ff8de-164">Name</span></span></th>
<th><span data-ttu-id="ff8de-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff8de-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ff8de-167"><a href="dn335116(v=exchg.10).md">ContentEquals</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-167"><a href="dn335116(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="ff8de-168">Devuelve un valor que indica si esta instancia es igual a otra instancia de.</span><span class="sxs-lookup"><span data-stu-id="ff8de-168">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ff8de-170"><a href="dn335153(v=exchg.10).md">DeepClone</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-170"><a href="dn335153(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="ff8de-171">Devuelve una copia en profundidad del objeto.</span><span class="sxs-lookup"><span data-stu-id="ff8de-171">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ff8de-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="ff8de-174">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="ff8de-174">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="ff8de-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="ff8de-177">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="ff8de-177">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ff8de-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="ff8de-180">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="ff8de-180">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ff8de-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="ff8de-183">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="ff8de-183">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="ff8de-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="ff8de-186">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="ff8de-186">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="ff8de-188"><a href="dn335154(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="ff8de-188"><a href="dn335154(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="ff8de-189">Generar una representación de cadena de la instancia.</span><span class="sxs-lookup"><span data-stu-id="ff8de-189">Generate a string representation of the instance.</span></span> <span data-ttu-id="ff8de-190">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="ff8de-190">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ff8de-191">Superior</span><span class="sxs-lookup"><span data-stu-id="ff8de-191">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ff8de-192">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff8de-192">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ff8de-193">Referencia</span><span class="sxs-lookup"><span data-stu-id="ff8de-193">Reference</span></span>

[<span data-ttu-id="ff8de-194">JET_INDEXCREATE (clase)</span><span class="sxs-lookup"><span data-stu-id="ff8de-194">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="ff8de-195">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ff8de-195">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
