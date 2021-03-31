---
description: 'Más información sobre: API. RetrieveColumn (método)'
title: Método API. RetrieveColumn
TOCTitle: 'RetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100835
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: 3bcb5effcfc59e155007fbd9e1733d95db058970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816995"
---
# <a name="apiretrievecolumn-method"></a><span data-ttu-id="cbc1f-103">Método API. RetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="cbc1f-103">Api.RetrieveColumn method</span></span>

<span data-ttu-id="cbc1f-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="cbc1f-104">Include protected members</span></span>  
<span data-ttu-id="cbc1f-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="cbc1f-105">Include inherited members</span></span>  

## <a name="overload-list"></a><span data-ttu-id="cbc1f-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="cbc1f-106">Overload list</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="cbc1f-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="cbc1f-107">Name</span></span></th>
<th><span data-ttu-id="cbc1f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbc1f-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="cbc1f-111"><a href="dn334041(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span><span class="sxs-lookup"><span data-stu-id="cbc1f-111"><a href="dn334041(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="cbc1f-112">Recupera un valor de una sola columna del registro actual.</span><span class="sxs-lookup"><span data-stu-id="cbc1f-112">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="cbc1f-113">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="cbc1f-113">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="cbc1f-116"><a href="dn334060(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="cbc1f-116"><a href="dn334060(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="cbc1f-117">Recupera un valor de una sola columna del registro actual.</span><span class="sxs-lookup"><span data-stu-id="cbc1f-117">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="cbc1f-118">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="cbc1f-118">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="cbc1f-119">Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor.</span><span class="sxs-lookup"><span data-stu-id="cbc1f-119">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="cbc1f-120">Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual.</span><span class="sxs-lookup"><span data-stu-id="cbc1f-120">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="cbc1f-121">Además de recuperar el valor de la columna real, JetRetrieveColumn también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de la columna para que se pueda ajustar el tamaño adecuado de los búferes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cbc1f-121">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cbc1f-122">Superior</span><span class="sxs-lookup"><span data-stu-id="cbc1f-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="cbc1f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbc1f-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cbc1f-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="cbc1f-124">Reference</span></span>

[<span data-ttu-id="cbc1f-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="cbc1f-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cbc1f-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="cbc1f-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cbc1f-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cbc1f-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
