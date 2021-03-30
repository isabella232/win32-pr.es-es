---
description: 'Más información acerca de: JET_RETRIEVECOLUMN propiedades'
title: Propiedades de JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2a42337e361fc7cbef60db70662ab7388c678903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816366"
---
# <a name="jet_retrievecolumn-properties"></a><span data-ttu-id="1868f-103">Propiedades de JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="1868f-103">JET_RETRIEVECOLUMN properties</span></span>

<span data-ttu-id="1868f-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="1868f-104">Include protected members</span></span>  
<span data-ttu-id="1868f-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="1868f-105">Include inherited members</span></span>  

<span data-ttu-id="1868f-106">El tipo de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="1868f-106">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="1868f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1868f-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1868f-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="1868f-108">Name</span></span></th>
<th><span data-ttu-id="1868f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1868f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1868f-111"><a href="dn335226(v=exchg.10).md">cbActual</a></span><span class="sxs-lookup"><span data-stu-id="1868f-111"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="1868f-112">Obtiene el tamaño, en bytes, de los datos recuperados por una operación de recuperación de columna.</span><span class="sxs-lookup"><span data-stu-id="1868f-112">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1868f-114"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="1868f-114"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="1868f-115">Obtiene o establece el tamaño del búfer de <a href="dn351040(v=exchg.10).md">pvData</a> , en bytes.</span><span class="sxs-lookup"><span data-stu-id="1868f-115">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="1868f-116">La operación de recuperación de columna no almacenará más datos en pvData que cbData.</span><span class="sxs-lookup"><span data-stu-id="1868f-116">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1868f-118"><a href="dn335230(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="1868f-118"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="1868f-119">Obtiene o establece el identificador de columna para la columna que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="1868f-119">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1868f-121"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="1868f-121"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="1868f-122">Obtiene el columnid de la columna etiquetada, con varios valores o dispersas cuando se recuperan todas las columnas etiquetadas pasando 0 como columnid.</span><span class="sxs-lookup"><span data-stu-id="1868f-122">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1868f-124"><a href="dn335231(v=exchg.10).md">ERR</a></span><span class="sxs-lookup"><span data-stu-id="1868f-124"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="1868f-125">Obtiene la advertencia devuelta por la recuperación de la columna.</span><span class="sxs-lookup"><span data-stu-id="1868f-125">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1868f-127"><a href="dn335232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="1868f-127"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="1868f-128">Obtiene o establece las opciones para la recuperación de columnas.</span><span class="sxs-lookup"><span data-stu-id="1868f-128">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1868f-130"><a href="dn335233(v=exchg.10).md">ibData</a></span><span class="sxs-lookup"><span data-stu-id="1868f-130"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="1868f-131">Obtiene o establece el desplazamiento en el búfer en el que se almacenarán los datos.</span><span class="sxs-lookup"><span data-stu-id="1868f-131">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1868f-133"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="1868f-133"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="1868f-134">Obtiene o establece el desplazamiento del primer byte que se va a recuperar de una columna de tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> o <a href="hh577895(v=exchg.10).md">LongText</a>.</span><span class="sxs-lookup"><span data-stu-id="1868f-134">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1868f-136"><a href="dn351039(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="1868f-136"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="1868f-137">Obtiene o establece el número de secuencia de los valores contenidos en una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="1868f-137">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="1868f-138">Si el valor de itagSequence es 0, se devuelve el número de instancias de una columna con varios valores en lugar de datos de columna.</span><span class="sxs-lookup"><span data-stu-id="1868f-138">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="1868f-140"><a href="dn351040(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="1868f-140"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="1868f-141">Obtiene o establece el búfer que almacenará los datos recuperados de la columna.</span><span class="sxs-lookup"><span data-stu-id="1868f-141">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1868f-142">Superior</span><span class="sxs-lookup"><span data-stu-id="1868f-142">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="1868f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="1868f-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1868f-144">Referencia</span><span class="sxs-lookup"><span data-stu-id="1868f-144">Reference</span></span>

[<span data-ttu-id="1868f-145">JET_RETRIEVECOLUMN (clase)</span><span class="sxs-lookup"><span data-stu-id="1868f-145">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="1868f-146">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1868f-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
