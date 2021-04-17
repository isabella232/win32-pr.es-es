---
description: 'Más información acerca de: JET_RETRIEVECOLUMN miembros'
title: Miembros de JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103877
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9a5eda1d671cfe6225a8419314b2f53558294754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562068"
---
# <a name="jet_retrievecolumn-members"></a><span data-ttu-id="e517d-103">Miembros de JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="e517d-103">JET_RETRIEVECOLUMN members</span></span>

<span data-ttu-id="e517d-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="e517d-104">Include protected members</span></span>  
<span data-ttu-id="e517d-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="e517d-105">Include inherited members</span></span>  

<span data-ttu-id="e517d-106">Contiene parámetros de entrada y salida para [JetRetrieveColumns (JET_SESID, JET_TABLEID, \[ \] , Int32)](./api.jetretrievecolumns-method.md).</span><span class="sxs-lookup"><span data-stu-id="e517d-106">Contains input and output parameters for [JetRetrieveColumns(JET_SESID, JET_TABLEID, \[\], Int32)](./api.jetretrievecolumns-method.md).</span></span> <span data-ttu-id="e517d-107">Los campos de la estructura describen qué valor de columna se va a recuperar, cómo se recupera y dónde se guardan los resultados.</span><span class="sxs-lookup"><span data-stu-id="e517d-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

<span data-ttu-id="e517d-108">El tipo de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="e517d-108">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="e517d-109">Constructores</span><span class="sxs-lookup"><span data-stu-id="e517d-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e517d-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="e517d-110">Name</span></span></th>
<th><span data-ttu-id="e517d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e517d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e517d-113"><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="e517d-113"><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e517d-114">Superior</span><span class="sxs-lookup"><span data-stu-id="e517d-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="e517d-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e517d-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e517d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="e517d-116">Name</span></span></th>
<th><span data-ttu-id="e517d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e517d-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e517d-119"><a href="dn335226(v=exchg.10).md">cbActual</a></span><span class="sxs-lookup"><span data-stu-id="e517d-119"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="e517d-120">Obtiene el tamaño, en bytes, de los datos recuperados por una operación de recuperación de columna.</span><span class="sxs-lookup"><span data-stu-id="e517d-120">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e517d-122"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="e517d-122"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="e517d-123">Obtiene o establece el tamaño del búfer de <a href="dn351040(v=exchg.10).md">pvData</a> , en bytes.</span><span class="sxs-lookup"><span data-stu-id="e517d-123">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="e517d-124">La operación de recuperación de columna no almacenará más datos en pvData que cbData.</span><span class="sxs-lookup"><span data-stu-id="e517d-124">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e517d-126"><a href="dn335230(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="e517d-126"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="e517d-127">Obtiene o establece el identificador de columna para la columna que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="e517d-127">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e517d-129"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="e517d-129"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="e517d-130">Obtiene el columnid de la columna etiquetada, con varios valores o dispersas cuando se recuperan todas las columnas etiquetadas pasando 0 como columnid.</span><span class="sxs-lookup"><span data-stu-id="e517d-130">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e517d-132"><a href="dn335231(v=exchg.10).md">ERR</a></span><span class="sxs-lookup"><span data-stu-id="e517d-132"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="e517d-133">Obtiene la advertencia devuelta por la recuperación de la columna.</span><span class="sxs-lookup"><span data-stu-id="e517d-133">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e517d-135"><a href="dn335232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="e517d-135"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="e517d-136">Obtiene o establece las opciones para la recuperación de columnas.</span><span class="sxs-lookup"><span data-stu-id="e517d-136">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e517d-138"><a href="dn335233(v=exchg.10).md">ibData</a></span><span class="sxs-lookup"><span data-stu-id="e517d-138"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="e517d-139">Obtiene o establece el desplazamiento en el búfer en el que se almacenarán los datos.</span><span class="sxs-lookup"><span data-stu-id="e517d-139">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e517d-141"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="e517d-141"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="e517d-142">Obtiene o establece el desplazamiento del primer byte que se va a recuperar de una columna de tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> o <a href="hh577895(v=exchg.10).md">LongText</a>.</span><span class="sxs-lookup"><span data-stu-id="e517d-142">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e517d-144"><a href="dn351039(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="e517d-144"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="e517d-145">Obtiene o establece el número de secuencia de los valores contenidos en una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="e517d-145">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="e517d-146">Si el valor de itagSequence es 0, se devuelve el número de instancias de una columna con varios valores en lugar de datos de columna.</span><span class="sxs-lookup"><span data-stu-id="e517d-146">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="e517d-148"><a href="dn351040(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="e517d-148"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="e517d-149">Obtiene o establece el búfer que almacenará los datos recuperados de la columna.</span><span class="sxs-lookup"><span data-stu-id="e517d-149">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e517d-150">Superior</span><span class="sxs-lookup"><span data-stu-id="e517d-150">Top</span></span>

## <a name="methods"></a><span data-ttu-id="e517d-151">Métodos</span><span class="sxs-lookup"><span data-stu-id="e517d-151">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e517d-152">Nombre</span><span class="sxs-lookup"><span data-stu-id="e517d-152">Name</span></span></th>
<th><span data-ttu-id="e517d-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="e517d-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e517d-155"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="e517d-155"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="e517d-156">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e517d-156">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="e517d-158"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="e517d-158"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="e517d-159">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e517d-159">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e517d-161"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="e517d-161"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="e517d-162">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e517d-162">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e517d-164"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="e517d-164"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="e517d-165">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e517d-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="e517d-167"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="e517d-167"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="e517d-168">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="e517d-168">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e517d-170"><a href="dn335224(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="e517d-170"><a href="dn335224(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="e517d-171">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa el <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>actual.</span><span class="sxs-lookup"><span data-stu-id="e517d-171">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>.</span></span> <span data-ttu-id="e517d-172">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="e517d-172">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e517d-173">Superior</span><span class="sxs-lookup"><span data-stu-id="e517d-173">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="e517d-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="e517d-174">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e517d-175">Referencia</span><span class="sxs-lookup"><span data-stu-id="e517d-175">Reference</span></span>

[<span data-ttu-id="e517d-176">JET_RETRIEVECOLUMN (clase)</span><span class="sxs-lookup"><span data-stu-id="e517d-176">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="e517d-177">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e517d-177">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
