---
description: 'Más información acerca de: JET_INDEXLIST miembros'
title: Miembros de JET_INDEXLIST
TOCTitle: JET_INDEXLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_members(v=EXCHG.10)
ms:contentKeyID: 55103660
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7800ef911366bad40b2d02ee60e23b5d138d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083206"
---
# <a name="jet_indexlist-members"></a><span data-ttu-id="3ccd0-103">Miembros de JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="3ccd0-103">JET_INDEXLIST members</span></span>

<span data-ttu-id="3ccd0-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="3ccd0-104">Include protected members</span></span>  
<span data-ttu-id="3ccd0-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="3ccd0-105">Include inherited members</span></span>  

<span data-ttu-id="3ccd0-106">Información sobre una tabla temporal que contiene información sobre todos los índices de una tabla determinada.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-106">Information about a temporary table containing information about all indexes for a given table.</span></span>

<span data-ttu-id="3ccd0-107">El tipo de [JET_INDEXLIST](./jet-indexlist-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-107">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="3ccd0-108">Constructores</span><span class="sxs-lookup"><span data-stu-id="3ccd0-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3ccd0-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="3ccd0-109">Name</span></span></th>
<th><span data-ttu-id="3ccd0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ccd0-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3ccd0-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3ccd0-113">Superior</span><span class="sxs-lookup"><span data-stu-id="3ccd0-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="3ccd0-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ccd0-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3ccd0-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="3ccd0-115">Name</span></span></th>
<th><span data-ttu-id="3ccd0-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ccd0-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-118"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-118"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="3ccd0-119">Obtiene el columnid de la columna de la tabla temporal que almacena el número de columnas de la clave de índice.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-119">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="3ccd0-120">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-120">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-122"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-122"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="3ccd0-123">Obtiene el columnid de la columna de la tabla temporal que almacena el número de entradas en el índice.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-123">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="3ccd0-124">Este valor no es actual y solo se actualiza mediante &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ccd0-124">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="3ccd0-125">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-125">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-127"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-127"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="3ccd0-128">Obtiene el columnid de la columna de la tabla temporal que almacena el número de claves únicas en el índice.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-128">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="3ccd0-129">Este valor no es actual y solo se actualiza mediante &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ccd0-129">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="3ccd0-130">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-130">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-132"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-132"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="3ccd0-133">Obtiene el columnid de la columna de la tabla temporal que almacena el tipo de columna de la columna que se está indizando.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-133">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="3ccd0-134">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-134">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="3ccd0-137">Obtiene el columnid de la columna de la tabla temporal que almacena el columnid de la columna que se está indizando.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-137">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="3ccd0-138">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-138">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="3ccd0-141">Obtiene el columnid de la columna de la tabla temporal que almacena el grbit que se aplica a la columna indizada.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-141">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="3ccd0-142">Vea <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-142">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="3ccd0-143">La columna es de tipo <a href="hh577895(v=exchg.10).md">Text</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-143">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-145"><a href="dn335168(v=exchg.10).md">columnidCp</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-145"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="3ccd0-146">Obtiene el columnid de la columna de la tabla temporal que almacena la página de códigos de la columna indizada.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-146">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="3ccd0-147">La columna es de tipo <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-147">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-149"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-149"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="3ccd0-150">Obtiene el columnid de la columna de la tabla temporal que almacena el número de páginas del índice.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-150">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="3ccd0-151">Este valor no es actual y solo se actualiza mediante &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="3ccd0-151">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="3ccd0-152">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-152">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-154"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-154"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="3ccd0-155">Obtiene el columnid de la columna de la tabla temporal que almacena el grbit que se aplica a la columna indizada.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-155">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="3ccd0-156">Vea <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-156">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="3ccd0-157">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-157">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-159"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-159"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="3ccd0-160">Obtiene el columnid de la columna de la tabla temporal que almacena el grbits que se usa en el índice.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-160">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="3ccd0-161">Vea <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-161">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="3ccd0-162">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-162">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-164"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-164"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="3ccd0-165">Obtiene el columnid de la columna de la tabla temporal que almacena el índice de de esta columna en la clave de índice.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-165">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="3ccd0-166">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-166">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="3ccd0-169">Obtiene el columnid de la columna de la tabla temporal que almacena el nombre del índice.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-169">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="3ccd0-170">La columna es de tipo <a href="hh577895(v=exchg.10).md">Text</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-170">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-172"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-172"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="3ccd0-173">Obtiene el columnid de la columna de la tabla temporal que almacena el identificador de idioma (LCID) del índice.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-173">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="3ccd0-174">La columna es de tipo <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-174">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-176"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-176"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="3ccd0-177">Obtiene el columnid de la columna de la tabla temporal que almacena las marcas de normalización Unicode para el índice.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-177">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="3ccd0-178">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-178">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-180"><a href="dn335173(v=exchg.10).md">cRecord</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-180"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="3ccd0-181">Obtiene el número de registros de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-181">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="3ccd0-183"><a href="dn335174(v=exchg.10).md">TABLEID</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-183"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="3ccd0-184">Obtiene TABLEID de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-184">Gets tableid of the temporary table.</span></span> <span data-ttu-id="3ccd0-185">Debe cerrarse cuando la tabla ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-185">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3ccd0-186">Superior</span><span class="sxs-lookup"><span data-stu-id="3ccd0-186">Top</span></span>

## <a name="methods"></a><span data-ttu-id="3ccd0-187">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ccd0-187">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3ccd0-188">Nombre</span><span class="sxs-lookup"><span data-stu-id="3ccd0-188">Name</span></span></th>
<th><span data-ttu-id="3ccd0-189">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ccd0-189">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3ccd0-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="3ccd0-192">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="3ccd0-192">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="3ccd0-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="3ccd0-195">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="3ccd0-195">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3ccd0-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="3ccd0-198">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="3ccd0-198">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3ccd0-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="3ccd0-201">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="3ccd0-201">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="3ccd0-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="3ccd0-204">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="3ccd0-204">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3ccd0-206"><a href="dn335165(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="3ccd0-206"><a href="dn335165(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="3ccd0-207">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa el <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>actual.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-207">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>.</span></span> <span data-ttu-id="3ccd0-208">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="3ccd0-208">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3ccd0-209">Superior</span><span class="sxs-lookup"><span data-stu-id="3ccd0-209">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="3ccd0-210">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ccd0-210">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3ccd0-211">Referencia</span><span class="sxs-lookup"><span data-stu-id="3ccd0-211">Reference</span></span>

[<span data-ttu-id="3ccd0-212">JET_INDEXLIST (clase)</span><span class="sxs-lookup"><span data-stu-id="3ccd0-212">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="3ccd0-213">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3ccd0-213">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
