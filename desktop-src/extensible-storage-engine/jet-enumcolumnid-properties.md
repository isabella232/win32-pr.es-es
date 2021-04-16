---
description: 'Más información acerca de: JET_ENUMCOLUMNID propiedades'
title: Propiedades de JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540062"
---
# <a name="jet_enumcolumnid-properties"></a><span data-ttu-id="b78cc-103">Propiedades de JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="b78cc-103">JET_ENUMCOLUMNID properties</span></span>

<span data-ttu-id="b78cc-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="b78cc-104">Include protected members</span></span>  
<span data-ttu-id="b78cc-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="b78cc-105">Include inherited members</span></span>  

<span data-ttu-id="b78cc-106">El tipo de [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="b78cc-106">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="b78cc-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b78cc-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b78cc-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="b78cc-108">Name</span></span></th>
<th><span data-ttu-id="b78cc-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b78cc-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="b78cc-111"><a href="dn335141(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="b78cc-111"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="b78cc-112">Obtiene o establece el identificador de columnid que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="b78cc-112">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="b78cc-114"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span><span class="sxs-lookup"><span data-stu-id="b78cc-114"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="b78cc-115">Obtiene o establece el recuento de valores de columna (por índice basado en uno) que se va a enumerar para el identificador de columna especificado.</span><span class="sxs-lookup"><span data-stu-id="b78cc-115">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="b78cc-116">Si ctagSequence es 0 (cero), se omite rgtagSequence y se enumeran todos los valores de columna para el ID. de columna especificado.</span><span class="sxs-lookup"><span data-stu-id="b78cc-116">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="b78cc-118"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span><span class="sxs-lookup"><span data-stu-id="b78cc-118"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="b78cc-119">Obtiene o establece la matriz de índices basados en uno en la matriz de valores de columna de una columna determinada.</span><span class="sxs-lookup"><span data-stu-id="b78cc-119">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="b78cc-120">Un único elemento es un itagSequence que se define en JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="b78cc-120">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="b78cc-121">Un valor de itagSequence de 0 (cero) significa &quot; SKIP &quot; .</span><span class="sxs-lookup"><span data-stu-id="b78cc-121">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="b78cc-122">Un itagSequence de 1 significa devolver el valor de la primera columna de la columna, 2 significa el segundo, etc.</span><span class="sxs-lookup"><span data-stu-id="b78cc-122">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b78cc-123">Superior</span><span class="sxs-lookup"><span data-stu-id="b78cc-123">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="b78cc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b78cc-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b78cc-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="b78cc-125">Reference</span></span>

[<span data-ttu-id="b78cc-126">JET_ENUMCOLUMNID (clase)</span><span class="sxs-lookup"><span data-stu-id="b78cc-126">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="b78cc-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b78cc-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
