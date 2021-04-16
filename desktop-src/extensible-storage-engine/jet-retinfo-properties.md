---
description: 'Más información acerca de: JET_RETINFO propiedades'
title: Propiedades de JET_RETINFO
TOCTitle: JET_RETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103867
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4724651b0184bae0b4acca049a8a16653282ce85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554406"
---
# <a name="jet_retinfo-properties"></a><span data-ttu-id="f5060-103">Propiedades de JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="f5060-103">JET_RETINFO properties</span></span>

<span data-ttu-id="f5060-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="f5060-104">Include protected members</span></span>  
<span data-ttu-id="f5060-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="f5060-105">Include inherited members</span></span>  

<span data-ttu-id="f5060-106">El tipo de [JET_RETINFO](./jet-retinfo-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="f5060-106">The [JET_RETINFO](./jet-retinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="f5060-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5060-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f5060-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="f5060-108">Name</span></span></th>
<th><span data-ttu-id="f5060-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5060-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f5060-111"><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="f5060-111"><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="f5060-112">Obtiene el columnid de la columna etiquetada, multivalor o dispersa recuperada cuando se recuperan todas las columnas etiquetadas pasando 0 como columnid a JetRetrieveColumn.</span><span class="sxs-lookup"><span data-stu-id="f5060-112">Gets the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to JetRetrieveColumn.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f5060-114"><a href="dn335220(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="f5060-114"><a href="dn335220(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="f5060-115">Obtiene o establece el desplazamiento del primer byte que se va a recuperar de una columna de tipo <a href="hh577895(v=exchg.10).md">LongBinary</a>o <a href="hh577895(v=exchg.10).md">LongText</a>.</span><span class="sxs-lookup"><span data-stu-id="f5060-115">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a>, or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f5060-117"><a href="dn351035(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="f5060-117"><a href="dn351035(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="f5060-118">Obtiene o establece el número de secuencia de un valor en una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="f5060-118">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="f5060-119">La matriz de valores se basa en uno.</span><span class="sxs-lookup"><span data-stu-id="f5060-119">The array of values is one-based.</span></span> <span data-ttu-id="f5060-120">El primer valor es Sequence 1, no 0.</span><span class="sxs-lookup"><span data-stu-id="f5060-120">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="f5060-121">Si la columna de registro solo tiene un valor, se debe pasar 1 como itagSequence.</span><span class="sxs-lookup"><span data-stu-id="f5060-121">If the record column has only one value then 1 should be passed as the itagSequence.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f5060-122">Superior</span><span class="sxs-lookup"><span data-stu-id="f5060-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="f5060-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5060-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f5060-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="f5060-124">Reference</span></span>

[<span data-ttu-id="f5060-125">JET_RETINFO (clase)</span><span class="sxs-lookup"><span data-stu-id="f5060-125">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="f5060-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f5060-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
