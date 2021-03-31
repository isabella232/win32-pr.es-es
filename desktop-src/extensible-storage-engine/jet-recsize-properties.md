---
description: 'Más información acerca de: JET_RECSIZE propiedades'
title: Propiedades de JET_RECSIZE (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_RECSIZE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_properties(v=EXCHG.10)
ms:contentKeyID: 39513545
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4733e1d666bdf3f938c91f437c1764811fb10f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913562"
---
# <a name="jet_recsize-properties"></a><span data-ttu-id="5231f-103">Propiedades de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="5231f-103">JET_RECSIZE properties</span></span>

<span data-ttu-id="5231f-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="5231f-104">Include protected members</span></span>  
<span data-ttu-id="5231f-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="5231f-105">Include inherited members</span></span>  

<span data-ttu-id="5231f-106">El tipo de [JET_RECSIZE](./jet-recsize-structure2.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="5231f-106">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="5231f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5231f-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5231f-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="5231f-108">Name</span></span></th>
<th><span data-ttu-id="5231f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5231f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="5231f-111"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="5231f-111"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="5231f-112">Obtiene el conjunto de datos de usuario del registro.</span><span class="sxs-lookup"><span data-stu-id="5231f-112">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="5231f-114"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="5231f-114"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="5231f-115">Obtiene el tamaño comprimido de los datos de usuario en el registro.</span><span class="sxs-lookup"><span data-stu-id="5231f-115">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="5231f-116">Es lo mismo que <a href="hh557581(v=exchg.10).md">cbData</a> si no se comprimen valores largos intrínsecos).</span><span class="sxs-lookup"><span data-stu-id="5231f-116">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="5231f-118"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span><span class="sxs-lookup"><span data-stu-id="5231f-118"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="5231f-119">Obtiene el conjunto de datos de usuario del registro, pero almacenado en el árbol de valores largos.</span><span class="sxs-lookup"><span data-stu-id="5231f-119">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="5231f-121"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="5231f-121"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="5231f-122">Obtiene el tamaño comprimido de los datos de usuario en el árbol de valores largos.</span><span class="sxs-lookup"><span data-stu-id="5231f-122">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="5231f-123">Es lo mismo que <a href="hh557913(v=exchg.10).md">cbLongValueData</a> si no se comprimen valores largos separados.</span><span class="sxs-lookup"><span data-stu-id="5231f-123">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="5231f-125"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span><span class="sxs-lookup"><span data-stu-id="5231f-125"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="5231f-126">Obtiene la sobrecarga de los datos de valor largo.</span><span class="sxs-lookup"><span data-stu-id="5231f-126">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="5231f-128"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span><span class="sxs-lookup"><span data-stu-id="5231f-128"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="5231f-129">Obtiene la sobrecarga de la estructura de registro ESENT para este registro.</span><span class="sxs-lookup"><span data-stu-id="5231f-129">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="5231f-130">Esto incluye el tamaño de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="5231f-130">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="5231f-132"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span><span class="sxs-lookup"><span data-stu-id="5231f-132"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="5231f-133">Obtiene el número total de columnas del registro que se comprimen.</span><span class="sxs-lookup"><span data-stu-id="5231f-133">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="5231f-135"><a href="hh596288(v=exchg.10).md">cLongValues</a></span><span class="sxs-lookup"><span data-stu-id="5231f-135"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="5231f-136">Obtiene el número total de valores Long almacenados en el árbol de valor largo para este registro.</span><span class="sxs-lookup"><span data-stu-id="5231f-136">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="5231f-137">No se incluyen los valores largos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="5231f-137">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="5231f-139"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span><span class="sxs-lookup"><span data-stu-id="5231f-139"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="5231f-140">Obtiene la acumulación del número total de valores más allá de la primera para todas las columnas del registro.</span><span class="sxs-lookup"><span data-stu-id="5231f-140">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="5231f-142"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="5231f-142"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="5231f-143">Obtiene el número total de columnas fijas y variables establecidas en este registro.</span><span class="sxs-lookup"><span data-stu-id="5231f-143">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="5231f-145"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="5231f-145"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="5231f-146">Obtiene el número total de columnas etiquetadas establecidas en este registro.</span><span class="sxs-lookup"><span data-stu-id="5231f-146">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5231f-147">Superior</span><span class="sxs-lookup"><span data-stu-id="5231f-147">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="5231f-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="5231f-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5231f-149">Referencia</span><span class="sxs-lookup"><span data-stu-id="5231f-149">Reference</span></span>

[<span data-ttu-id="5231f-150">Estructura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="5231f-150">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="5231f-151">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="5231f-151">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
