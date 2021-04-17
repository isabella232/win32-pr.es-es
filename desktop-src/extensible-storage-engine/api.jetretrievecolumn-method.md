---
description: 'Más información sobre: API. JetRetrieveColumn (método)'
title: Método API. JetRetrieveColumn
TOCTitle: 'JetRetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100791
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: e4e43d57f4393d6b0d4ce2f1cdbe4ecd8338ec54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279275"
---
# <a name="apijetretrievecolumn-method"></a><span data-ttu-id="7ceb2-103">Método API. JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="7ceb2-103">Api.JetRetrieveColumn method</span></span>

<span data-ttu-id="7ceb2-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="7ceb2-104">Include protected members</span></span>  
<span data-ttu-id="7ceb2-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="7ceb2-105">Include inherited members</span></span>  

## <a name="overload-list"></a><span data-ttu-id="7ceb2-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="7ceb2-106">Overload list</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="7ceb2-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="7ceb2-107">Name</span></span></th>
<th><span data-ttu-id="7ceb2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ceb2-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="7ceb2-111"><a href="dn332995(v=exchg.10).md">JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="7ceb2-111"><a href="dn332995(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="7ceb2-112">Recupera un valor de una sola columna del registro actual.</span><span class="sxs-lookup"><span data-stu-id="7ceb2-112">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="7ceb2-113">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="7ceb2-113">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="7ceb2-114">Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor.</span><span class="sxs-lookup"><span data-stu-id="7ceb2-114">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="7ceb2-115">Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual.</span><span class="sxs-lookup"><span data-stu-id="7ceb2-115">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="7ceb2-116">Además de recuperar el valor de la columna real, JetRetrieveColumn también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de la columna para que se pueda ajustar el tamaño adecuado de los búferes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7ceb2-116">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="7ceb2-119"><a href="dn332997(v=exchg.10).md">JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="7ceb2-119"><a href="dn332997(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="7ceb2-120">Recupera un valor de una sola columna del registro actual.</span><span class="sxs-lookup"><span data-stu-id="7ceb2-120">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="7ceb2-121">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="7ceb2-121">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="7ceb2-122">Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor.</span><span class="sxs-lookup"><span data-stu-id="7ceb2-122">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="7ceb2-123">Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual.</span><span class="sxs-lookup"><span data-stu-id="7ceb2-123">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="7ceb2-124">Además de recuperar el valor de la columna real, JetRetrieveColumn también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de la columna para que se pueda ajustar el tamaño adecuado de los búferes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7ceb2-124">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7ceb2-125">Superior</span><span class="sxs-lookup"><span data-stu-id="7ceb2-125">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="7ceb2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ceb2-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7ceb2-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="7ceb2-127">Reference</span></span>

[<span data-ttu-id="7ceb2-128">Clase de API</span><span class="sxs-lookup"><span data-stu-id="7ceb2-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7ceb2-129">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="7ceb2-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7ceb2-130">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7ceb2-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
