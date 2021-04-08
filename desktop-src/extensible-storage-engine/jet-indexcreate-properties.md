---
description: 'Más información acerca de: JET_INDEXCREATE propiedades'
title: Propiedades de JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 66b6ada105e6f6d12cb754f288478e85d75a07e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002809"
---
# <a name="jet_indexcreate-properties"></a><span data-ttu-id="f4a5b-103">Propiedades de JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="f4a5b-103">JET_INDEXCREATE properties</span></span>

<span data-ttu-id="f4a5b-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="f4a5b-104">Include protected members</span></span>  
<span data-ttu-id="f4a5b-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="f4a5b-105">Include inherited members</span></span>  

<span data-ttu-id="f4a5b-106">El tipo de [JET_INDEXCREATE](./jet-indexcreate-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-106">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="f4a5b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4a5b-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f4a5b-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4a5b-108">Name</span></span></th>
<th><span data-ttu-id="f4a5b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4a5b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f4a5b-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="f4a5b-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="f4a5b-112">Obtiene o establece la longitud, en caracteres, de szKey, incluidos los dos valores NULL de terminación.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-112">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f4a5b-114"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="f4a5b-114"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="f4a5b-115">Obtiene o establece el tamaño máximo permitido, en bytes, para las claves del índice.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-115">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="f4a5b-116">El tamaño máximo de clave compatible mínimo es JET_cbKeyMostMin (255), que es el tamaño de clave máximo heredado.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-116">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="f4a5b-117">El tamaño máximo de la clave depende del tamaño de página de la base de datos <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-117">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="f4a5b-118">El tamaño máximo de la clave se puede recuperar con <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-118">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="f4a5b-119">Este parámetro se omite en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-119">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="f4a5b-120">A diferencia de la API no administrada, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) no es necesario, sino que se agregará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-120">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f4a5b-122"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="f4a5b-122"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="f4a5b-123">Obtiene o establece la longitud máxima, en bytes, de cada columna que se va a almacenar en el índice.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-123">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f4a5b-125"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span><span class="sxs-lookup"><span data-stu-id="f4a5b-125"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="f4a5b-126">Obtiene o establece el número de columnas condicionales.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-126">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f4a5b-128"><a href="dn335157(v=exchg.10).md">ERR</a></span><span class="sxs-lookup"><span data-stu-id="f4a5b-128"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="f4a5b-129">Obtiene o establece el código de error de la creación de este índice.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-129">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f4a5b-131"><a href="dn335119(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="f4a5b-131"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="f4a5b-132">Obtiene o establece las opciones de creación de índices.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-132">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f4a5b-134"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span><span class="sxs-lookup"><span data-stu-id="f4a5b-134"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="f4a5b-135">Obtiene o establece las opciones de comparación Unicode opcionales.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-135">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f4a5b-137"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span><span class="sxs-lookup"><span data-stu-id="f4a5b-137"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="f4a5b-138">Obtiene o establece las sugerencias de asignación, mantenimiento y uso de espacio.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-138">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f4a5b-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="f4a5b-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="f4a5b-141">Obtiene o establece las columnas condicionales opcionales.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-141">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f4a5b-143"><a href="dn335121(v=exchg.10).md">szIndexName</a></span><span class="sxs-lookup"><span data-stu-id="f4a5b-143"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="f4a5b-144">Obtiene o establece el nombre del índice que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-144">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f4a5b-146"><a href="dn335161(v=exchg.10).md">szKey</a></span><span class="sxs-lookup"><span data-stu-id="f4a5b-146"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="f4a5b-147">Obtiene o establece la descripción de la clave de índice.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-147">Gets or sets the description of the index key.</span></span> <span data-ttu-id="f4a5b-148">Se trata de una cadena doble terminada en NULL de tokens delimitados por null.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-148">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="f4a5b-149">Cada token tiene la forma [Direction-Specifier] [column-Name], donde Direction-Specification es &quot; + &quot; o &quot; - &quot; .</span><span class="sxs-lookup"><span data-stu-id="f4a5b-149">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="f4a5b-150">por ejemplo, un szKey de &quot; + abc\0-def\0 + ghi\0 &quot; indexará las tres columnas &quot; ABC &quot; (en orden ascendente), &quot; Def &quot; (en orden descendente) y &quot; GHI &quot; (en orden ascendente).</span><span class="sxs-lookup"><span data-stu-id="f4a5b-150">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="f4a5b-152"><a href="dn335162(v=exchg.10).md">ulDensity</a></span><span class="sxs-lookup"><span data-stu-id="f4a5b-152"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="f4a5b-153">Obtiene o establece la densidad del índice.</span><span class="sxs-lookup"><span data-stu-id="f4a5b-153">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f4a5b-154">Superior</span><span class="sxs-lookup"><span data-stu-id="f4a5b-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="f4a5b-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4a5b-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f4a5b-156">Referencia</span><span class="sxs-lookup"><span data-stu-id="f4a5b-156">Reference</span></span>

[<span data-ttu-id="f4a5b-157">JET_INDEXCREATE (clase)</span><span class="sxs-lookup"><span data-stu-id="f4a5b-157">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="f4a5b-158">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f4a5b-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
