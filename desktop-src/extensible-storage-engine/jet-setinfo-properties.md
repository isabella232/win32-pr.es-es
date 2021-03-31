---
description: 'Más información acerca de: JET_SETINFO propiedades'
title: Propiedades de JET_SETINFO
TOCTitle: JET_SETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103917
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af54ddfc09cce0a9c9498dea2060fb83baa0d6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154011"
---
# <a name="jet_setinfo-properties"></a><span data-ttu-id="022af-103">Propiedades de JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="022af-103">JET_SETINFO properties</span></span>

<span data-ttu-id="022af-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="022af-104">Include protected members</span></span>  
<span data-ttu-id="022af-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="022af-105">Include inherited members</span></span>  

<span data-ttu-id="022af-106">El tipo de [JET_SETINFO](./jet-setinfo-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="022af-106">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="022af-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="022af-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="022af-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="022af-108">Name</span></span></th>
<th><span data-ttu-id="022af-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="022af-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="022af-111"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="022af-111"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="022af-112">Obtiene o establece el desplazamiento del primer byte que se va a establecer en una columna de tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> o <a href="hh577895(v=exchg.10).md">LongText</a>.</span><span class="sxs-lookup"><span data-stu-id="022af-112">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="022af-114"><a href="dn351037(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="022af-114"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="022af-115">Obtiene o establece el número de secuencia del valor de una columna con varios valores que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="022af-115">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="022af-116">La matriz de valores se basa en uno.</span><span class="sxs-lookup"><span data-stu-id="022af-116">The array of values is one-based.</span></span> <span data-ttu-id="022af-117">El primer valor es Sequence 1, no 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="022af-117">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="022af-118">Si la columna de registro solo tiene un valor, se debe pasar 1 como itagSequence si ese valor se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="022af-118">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="022af-119">Un valor de 0 (cero) significa agregar una nueva instancia de valor de columna al final de la secuencia de valores de columna.</span><span class="sxs-lookup"><span data-stu-id="022af-119">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="022af-120">Superior</span><span class="sxs-lookup"><span data-stu-id="022af-120">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="022af-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="022af-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="022af-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="022af-122">Reference</span></span>

[<span data-ttu-id="022af-123">JET_SETINFO (clase)</span><span class="sxs-lookup"><span data-stu-id="022af-123">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="022af-124">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="022af-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
