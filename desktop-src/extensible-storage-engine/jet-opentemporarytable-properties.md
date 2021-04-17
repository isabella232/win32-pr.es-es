---
description: 'Más información acerca de: JET_OPENTEMPORARYTABLE propiedades'
title: Propiedades de JET_OPENTEMPORARYTABLE (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_OPENTEMPORARYTABLE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_properties(v=EXCHG.10)
ms:contentKeyID: 55104127
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e9c55afddd1128a517c27f6a86466b488e6924a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562082"
---
# <a name="jet_opentemporarytable-properties"></a><span data-ttu-id="cc0a6-103">Propiedades de JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="cc0a6-103">JET_OPENTEMPORARYTABLE properties</span></span>

<span data-ttu-id="cc0a6-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="cc0a6-104">Include protected members</span></span>  
<span data-ttu-id="cc0a6-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="cc0a6-105">Include inherited members</span></span>  

<span data-ttu-id="cc0a6-106">El tipo de [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-106">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="cc0a6-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc0a6-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="cc0a6-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="cc0a6-108">Name</span></span></th>
<th><span data-ttu-id="cc0a6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc0a6-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="cc0a6-111"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="cc0a6-111"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="cc0a6-112">Obtiene o establece el tamaño máximo para una clave que representa una fila determinada.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-112">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="cc0a6-113">Se puede establecer el tamaño máximo de la clave para controlar cómo se truncan las claves.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-113">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="cc0a6-114">El truncamiento de claves es importante porque puede afectar a la diferencia entre las filas.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-114">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="cc0a6-115">Si este parámetro se establece en 0 o 255, el tamaño de clave máximo y su semántica permanecerán idénticos al tamaño máximo de clave admitido por Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-115">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="cc0a6-116">Este parámetro también se puede establecer en un valor mayor como una función del tamaño de página de la base de datos para la instancia <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-116">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="cc0a6-117">Vea <a href="dn335292(v=exchg.10).md">KeyMost</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-117">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="cc0a6-119"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="cc0a6-119"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="cc0a6-120">Obtiene o establece la cantidad máxima de datos que se usarán de cualquier variable lengthcolumn para construir una clave para una fila determinada.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-120">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="cc0a6-121">Este parámetro se puede utilizar para controlar la cantidad de espacio de clave consumida por una columna de clave determinada.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-121">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="cc0a6-122">Este límite se encuentra en bytes.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-122">This limit is in bytes.</span></span> <span data-ttu-id="cc0a6-123">Si este parámetro es cero o es igual que la propiedad <a href="dn335290(v=exchg.10).md">cbKeyMost</a> , no se aplica ningún límite.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-123">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="cc0a6-125"><a href="dn335287(v=exchg.10).md">ccolumn</a></span><span class="sxs-lookup"><span data-stu-id="cc0a6-125"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="cc0a6-126">Obtiene o establece el número de columnas de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-126">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="cc0a6-128"><a href="dn351232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="cc0a6-128"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="cc0a6-129">Obtiene o establece las opciones de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-129">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="cc0a6-131"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="cc0a6-131"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="cc0a6-132">Obtiene o establece el identificador de configuración regional y las marcas de normalización que se van a utilizar para comparar los datos de columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-132">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="cc0a6-133">Cuando este parámetro es null, se utilizará el LCID predeterminado para comparar las columnas de clave Unicode de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-133">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="cc0a6-134">El LCID predeterminado es la configuración regional en Inglés de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-134">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="cc0a6-135">Cuando este parámetro es null, se usarán las marcas de normalización predeterminadas para comparar los datos de columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-135">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="cc0a6-136">Las marcas de normalización predeterminadas son: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-136">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="cc0a6-138"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span><span class="sxs-lookup"><span data-stu-id="cc0a6-138"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="cc0a6-139">Obtiene o establece las definiciones de columna para las columnas creadas en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-139">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="cc0a6-141"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="cc0a6-141"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="cc0a6-142">Obtiene o establece el búfer de salida que recibe la matriz de identificadores de columna generados durante la creación de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-142">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="cc0a6-143">Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-143">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="cc0a6-144">Como resultado, el tamaño de este búfer debe corresponder al tamaño de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-144">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="cc0a6-146"><a href="dn335293(v=exchg.10).md">TABLEID</a></span><span class="sxs-lookup"><span data-stu-id="cc0a6-146"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="cc0a6-147">Obtiene el identificador de tabla para la tabla temporal creada como resultado de una llamada correcta a JetOpenTemporaryTable.</span><span class="sxs-lookup"><span data-stu-id="cc0a6-147">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cc0a6-148">Superior</span><span class="sxs-lookup"><span data-stu-id="cc0a6-148">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="cc0a6-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc0a6-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cc0a6-150">Referencia</span><span class="sxs-lookup"><span data-stu-id="cc0a6-150">Reference</span></span>

[<span data-ttu-id="cc0a6-151">JET_OPENTEMPORARYTABLE (clase)</span><span class="sxs-lookup"><span data-stu-id="cc0a6-151">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="cc0a6-152">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="cc0a6-152">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
