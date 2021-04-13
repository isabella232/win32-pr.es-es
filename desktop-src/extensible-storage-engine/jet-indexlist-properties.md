---
description: 'Más información acerca de: JET_INDEXLIST propiedades'
title: Propiedades de JET_INDEXLIST
TOCTitle: JET_INDEXLIST properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_properties(v=EXCHG.10)
ms:contentKeyID: 55103599
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 7a1f500f5d51c0487ea490d2051bfc5e4639afbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561214"
---
# <a name="jet_indexlist-properties"></a><span data-ttu-id="93c3a-103">Propiedades de JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="93c3a-103">JET_INDEXLIST properties</span></span>

<span data-ttu-id="93c3a-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="93c3a-104">Include protected members</span></span>  
<span data-ttu-id="93c3a-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="93c3a-105">Include inherited members</span></span>  

<span data-ttu-id="93c3a-106">El tipo de [JET_INDEXLIST](./jet-indexlist-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="93c3a-106">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="93c3a-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="93c3a-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="93c3a-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="93c3a-108">Name</span></span></th>
<th><span data-ttu-id="93c3a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="93c3a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-111"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-111"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="93c3a-112">Obtiene el columnid de la columna de la tabla temporal que almacena el número de columnas de la clave de índice.</span><span class="sxs-lookup"><span data-stu-id="93c3a-112">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="93c3a-113">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-113">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-115"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-115"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="93c3a-116">Obtiene el columnid de la columna de la tabla temporal que almacena el número de entradas en el índice.</span><span class="sxs-lookup"><span data-stu-id="93c3a-116">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="93c3a-117">Este valor no es actual y solo se actualiza mediante &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="93c3a-117">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="93c3a-118">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-118">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-120"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-120"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="93c3a-121">Obtiene el columnid de la columna de la tabla temporal que almacena el número de claves únicas en el índice.</span><span class="sxs-lookup"><span data-stu-id="93c3a-121">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="93c3a-122">Este valor no es actual y solo se actualiza mediante &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="93c3a-122">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="93c3a-123">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-123">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-125"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-125"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="93c3a-126">Obtiene el columnid de la columna de la tabla temporal que almacena el tipo de columna de la columna que se está indizando.</span><span class="sxs-lookup"><span data-stu-id="93c3a-126">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="93c3a-127">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-127">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="93c3a-130">Obtiene el columnid de la columna de la tabla temporal que almacena el columnid de la columna que se está indizando.</span><span class="sxs-lookup"><span data-stu-id="93c3a-130">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="93c3a-131">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-131">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="93c3a-134">Obtiene el columnid de la columna de la tabla temporal que almacena el grbit que se aplica a la columna indizada.</span><span class="sxs-lookup"><span data-stu-id="93c3a-134">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="93c3a-135">Vea <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-135">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="93c3a-136">La columna es de tipo <a href="hh577895(v=exchg.10).md">Text</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-136">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-138"><a href="dn335168(v=exchg.10).md">columnidCp</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-138"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="93c3a-139">Obtiene el columnid de la columna de la tabla temporal que almacena la página de códigos de la columna indizada.</span><span class="sxs-lookup"><span data-stu-id="93c3a-139">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="93c3a-140">La columna es de tipo <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-140">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-142"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-142"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="93c3a-143">Obtiene el columnid de la columna de la tabla temporal que almacena el número de páginas del índice.</span><span class="sxs-lookup"><span data-stu-id="93c3a-143">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="93c3a-144">Este valor no es actual y solo se actualiza mediante &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="93c3a-144">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="93c3a-145">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-145">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-147"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-147"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="93c3a-148">Obtiene el columnid de la columna de la tabla temporal que almacena el grbit que se aplica a la columna indizada.</span><span class="sxs-lookup"><span data-stu-id="93c3a-148">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="93c3a-149">Vea <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-149">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="93c3a-150">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-150">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-152"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-152"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="93c3a-153">Obtiene el columnid de la columna de la tabla temporal que almacena el grbits que se usa en el índice.</span><span class="sxs-lookup"><span data-stu-id="93c3a-153">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="93c3a-154">Vea <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-154">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="93c3a-155">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-155">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-157"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-157"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="93c3a-158">Obtiene el columnid de la columna de la tabla temporal que almacena el índice de de esta columna en la clave de índice.</span><span class="sxs-lookup"><span data-stu-id="93c3a-158">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="93c3a-159">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-159">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="93c3a-162">Obtiene el columnid de la columna de la tabla temporal que almacena el nombre del índice.</span><span class="sxs-lookup"><span data-stu-id="93c3a-162">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="93c3a-163">La columna es de tipo <a href="hh577895(v=exchg.10).md">Text</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-163">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-165"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-165"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="93c3a-166">Obtiene el columnid de la columna de la tabla temporal que almacena el identificador de idioma (LCID) del índice.</span><span class="sxs-lookup"><span data-stu-id="93c3a-166">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="93c3a-167">La columna es de tipo <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-167">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-169"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-169"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="93c3a-170">Obtiene el columnid de la columna de la tabla temporal que almacena las marcas de normalización Unicode para el índice.</span><span class="sxs-lookup"><span data-stu-id="93c3a-170">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="93c3a-171">La columna es de tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="93c3a-171">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-173"><a href="dn335173(v=exchg.10).md">cRecord</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-173"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="93c3a-174">Obtiene el número de registros de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="93c3a-174">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="93c3a-176"><a href="dn335174(v=exchg.10).md">TABLEID</a></span><span class="sxs-lookup"><span data-stu-id="93c3a-176"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="93c3a-177">Obtiene TABLEID de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="93c3a-177">Gets tableid of the temporary table.</span></span> <span data-ttu-id="93c3a-178">Debe cerrarse cuando la tabla ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="93c3a-178">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93c3a-179">Superior</span><span class="sxs-lookup"><span data-stu-id="93c3a-179">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="93c3a-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="93c3a-180">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="93c3a-181">Referencia</span><span class="sxs-lookup"><span data-stu-id="93c3a-181">Reference</span></span>

[<span data-ttu-id="93c3a-182">JET_INDEXLIST (clase)</span><span class="sxs-lookup"><span data-stu-id="93c3a-182">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="93c3a-183">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="93c3a-183">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
