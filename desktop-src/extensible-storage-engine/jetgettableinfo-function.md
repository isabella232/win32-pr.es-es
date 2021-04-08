---
description: 'Más información acerca de: JetGetTableInfo (función)'
title: Función JetGetTableInfo
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002894"
---
# <a name="jetgettableinfo-function"></a><span data-ttu-id="9a742-103">Función JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="9a742-103">JetGetTableInfo Function</span></span>


<span data-ttu-id="9a742-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9a742-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableinfo-function"></a><span data-ttu-id="9a742-105">Función JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="9a742-105">JetGetTableInfo Function</span></span>

<span data-ttu-id="9a742-106">La función **JetGetTableInfo** Recupera varios fragmentos de información sobre una tabla de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="9a742-106">The **JetGetTableInfo** function retrieves various pieces of information about a table in a database.</span></span>

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="9a742-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a742-107">Parameters</span></span>

<span data-ttu-id="9a742-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9a742-108">*sesid*</span></span>

<span data-ttu-id="9a742-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="9a742-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="9a742-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="9a742-110">*tableid*</span></span>

<span data-ttu-id="9a742-111">Tabla a la que se aplica la información.</span><span class="sxs-lookup"><span data-stu-id="9a742-111">The table that the information applies to.</span></span>

<span data-ttu-id="9a742-112">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="9a742-112">*pvResult*</span></span>

<span data-ttu-id="9a742-113">Puntero a un búfer que recibirá la información.</span><span class="sxs-lookup"><span data-stu-id="9a742-113">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="9a742-114">El tipo de búfer depende de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="9a742-114">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="9a742-115">Es responsabilidad del autor de la llamada alinear el búfer adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="9a742-115">It is the responsibility of the caller to align the buffer appropriately.</span></span>

<span data-ttu-id="9a742-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="9a742-116">*cbMax*</span></span>

<span data-ttu-id="9a742-117">Tamaño, en bytes, del búfer que se pasó en *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="9a742-117">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="9a742-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="9a742-118">*InfoLevel*</span></span>

<span data-ttu-id="9a742-119">El tipo de información que se recuperará para la tabla especificada por *TABLEID*.</span><span class="sxs-lookup"><span data-stu-id="9a742-119">The type of information that will be retrieved for the table that is specified by *tableid*.</span></span> <span data-ttu-id="9a742-120">El formato de los datos que se almacenan en *pvResult* depende de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="9a742-120">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="9a742-121">Se pueden establecer las siguientes opciones para este parámetro:</span><span class="sxs-lookup"><span data-stu-id="9a742-121">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a742-122">Value</span><span class="sxs-lookup"><span data-stu-id="9a742-122">Value</span></span></p></th>
<th><p><span data-ttu-id="9a742-123">Significado</span><span class="sxs-lookup"><span data-stu-id="9a742-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a742-124">JET_TblInfo</span><span class="sxs-lookup"><span data-stu-id="9a742-124">JET_TblInfo</span></span></p></td>
<td><p><span data-ttu-id="9a742-125"><em>pvResult</em> se interpreta como una estructura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="9a742-125"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span> <span data-ttu-id="9a742-126">Si el método se ejecuta correctamente, la estructura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> se rellena con los datos adecuados.</span><span class="sxs-lookup"><span data-stu-id="9a742-126">If the method succeeds, the <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is filled in with the appropriate data.</span></span> <span data-ttu-id="9a742-127">Si se produce un error, el contenido es indefinido.</span><span class="sxs-lookup"><span data-stu-id="9a742-127">If it fails, the contents are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-128">JET_TblInfoDbid</span><span class="sxs-lookup"><span data-stu-id="9a742-128">JET_TblInfoDbid</span></span></p></td>
<td><p><span data-ttu-id="9a742-129"><em>pvResult</em> se trata como una matriz de dos objetos <a href="gg269248(v=exchg.10).md">JET_DBID</a> .</span><span class="sxs-lookup"><span data-stu-id="9a742-129"><em>pvResult</em> is treated as an array of two <a href="gg269248(v=exchg.10).md">JET_DBID</a> objects.</span></span> <span data-ttu-id="9a742-130">El identificador de la base de datos que posee la tabla se almacena dos veces en esta matriz.</span><span class="sxs-lookup"><span data-stu-id="9a742-130">The database identifier of the database that owns the table is stored in this array twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a742-131">JET_TblInfoDumpTable</span><span class="sxs-lookup"><span data-stu-id="9a742-131">JET_TblInfoDumpTable</span></span></p></td>
<td><p><span data-ttu-id="9a742-132">JET_TblInfoDumpTable está en desuso.</span><span class="sxs-lookup"><span data-stu-id="9a742-132">JET_TblInfoDumpTable is deprecated.</span></span> <span data-ttu-id="9a742-133">La API devolverá JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="9a742-133">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-134">JET_TblInfoName</span><span class="sxs-lookup"><span data-stu-id="9a742-134">JET_TblInfoName</span></span></p></td>
<td><p><span data-ttu-id="9a742-135">JET_TblInfoName recupera el nombre de la tabla y la almacena en <em>pvResult</em>.</span><span class="sxs-lookup"><span data-stu-id="9a742-135">JET_TblInfoName retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="9a742-136">Si el búfer es demasiado pequeño, el comportamiento es indefinido.</span><span class="sxs-lookup"><span data-stu-id="9a742-136">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a742-137">JET_TblInfoMostMany</span><span class="sxs-lookup"><span data-stu-id="9a742-137">JET_TblInfoMostMany</span></span></p></td>
<td><p><span data-ttu-id="9a742-138">JET_TblInfoMostMany recupera el nombre de la tabla y la almacena en <em>pvResult</em>.</span><span class="sxs-lookup"><span data-stu-id="9a742-138">JET_TblInfoMostMany retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="9a742-139">Si el búfer es demasiado pequeño, el comportamiento es indefinido.</span><span class="sxs-lookup"><span data-stu-id="9a742-139">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-140">JET_TblInfoOLC</span><span class="sxs-lookup"><span data-stu-id="9a742-140">JET_TblInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="9a742-141">JET_TblInfoOLC está en desuso.</span><span class="sxs-lookup"><span data-stu-id="9a742-141">JET_TblInfoOLC is deprecated.</span></span> <span data-ttu-id="9a742-142">La API devolverá JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="9a742-142">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a742-143">JET_TblInfoRvt</span><span class="sxs-lookup"><span data-stu-id="9a742-143">JET_TblInfoRvt</span></span></p></td>
<td><p><span data-ttu-id="9a742-144">JET_TblInfoRvt está en desuso.</span><span class="sxs-lookup"><span data-stu-id="9a742-144">JET_TblInfoRvt is deprecated.</span></span> <span data-ttu-id="9a742-145">La API devolverá JET_errQueryNotSupported.</span><span class="sxs-lookup"><span data-stu-id="9a742-145">The API will return JET_errQueryNotSupported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-146">JET_TblInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="9a742-146">JET_TblInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="9a742-147">JET_TblInfoResetOLC está en desuso.</span><span class="sxs-lookup"><span data-stu-id="9a742-147">JET_TblInfoResetOLC is deprecated.</span></span> <span data-ttu-id="9a742-148">La API devolverá JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="9a742-148">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a742-149">JET_TblInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="9a742-149">JET_TblInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="9a742-150"><em>pvResult</em> se interpreta como una matriz de dos ULONGs:</span><span class="sxs-lookup"><span data-stu-id="9a742-150"><em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="9a742-151">El primer <strong>ULong</strong> es el número de páginas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9a742-151">The first <strong>ULONG</strong> is the number of pages in the table.</span></span></p></li>
<li><p><span data-ttu-id="9a742-152">El segundo <strong>ULong</strong> es la densidad de destino de las páginas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9a742-152">The second <strong>ULONG</strong> is the target density of pages for the table.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-153">JET_TblInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="9a742-153">JET_TblInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="9a742-154"><em>pvResult</em> se interpreta como <strong>ULong</strong>.</span><span class="sxs-lookup"><span data-stu-id="9a742-154"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="9a742-155"><strong>ULong</strong> es la suma del número de páginas que están disponibles en la tabla, sus índices y el árbol de valores largos.</span><span class="sxs-lookup"><span data-stu-id="9a742-155">The <strong>ULONG</strong> is the sum of the number of pages that are available in the table, its indexes, and the long value tree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a742-156">JET_TblInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="9a742-156">JET_TblInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="9a742-157"><em>pvResult</em> se interpreta como <strong>ULong</strong>.</span><span class="sxs-lookup"><span data-stu-id="9a742-157"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="9a742-158"><strong>ULong</strong> es la suma del número de páginas que pertenecen a la tabla (incluidos sus índices y el árbol de valores largos y las páginas disponibles).</span><span class="sxs-lookup"><span data-stu-id="9a742-158">The <strong>ULONG</strong> is the sum of the number of pages that are owned by the table (including its indexes, and the long value tree and any available pages therein).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-159">JET_TblInfoSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="9a742-159">JET_TblInfoSpaceUsage</span></span></p></td>
<td><p><span data-ttu-id="9a742-160">El comportamiento de la API depende del tamaño del búfer que se pasa a la API.</span><span class="sxs-lookup"><span data-stu-id="9a742-160">The behavior of the API depends on how large the buffer that is passed to the API is.</span></span> <span data-ttu-id="9a742-161">Dos valores de <em>cbMax</em> deben ser al menos (2 \* SIZEOF (ulong)).</span><span class="sxs-lookup"><span data-stu-id="9a742-161">Two <em>cbMax</em> values must be at least ( 2 \* sizeof( ULONG ) ).</span></span></p>
<ul>
<li><p><span data-ttu-id="9a742-162">Si <em>cbMax</em> es (2 \* SIZEOF (ulong)), <em>pvResult</em> se interpreta como una matriz de dos ULONGs:</span><span class="sxs-lookup"><span data-stu-id="9a742-162">If <em>cbMax</em> is ( 2 \* sizeof( ULONG ) ), <em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="9a742-163">El primer <strong>ULong</strong> es el número de extensiones de propiedad de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9a742-163">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="9a742-164">El segundo <strong>ULong</strong> es el número de extensiones disponibles de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9a742-164">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="9a742-165"><em>pvResult</em> se interpreta como una matriz de:</span><span class="sxs-lookup"><span data-stu-id="9a742-165"><em>pvResult</em> is interpreted as an array of:</span></span></p>
<ul>
<li><p><span data-ttu-id="9a742-166">El primer <strong>ULong</strong> es el número de extensiones de propiedad de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9a742-166">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="9a742-167">El segundo <strong>ULong</strong> es el número de extensiones disponibles de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9a742-167">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a742-168">JET_TblInfoTemplateTableName</span><span class="sxs-lookup"><span data-stu-id="9a742-168">JET_TblInfoTemplateTableName</span></span></p></td>
<td><p><span data-ttu-id="9a742-169"><em>pvResult</em> se interpreta como un búfer de cadena.</span><span class="sxs-lookup"><span data-stu-id="9a742-169"><em>pvResult</em> is interpreted as a string buffer.</span></span> <span data-ttu-id="9a742-170">El búfer debe ser al menos JET_cbNameMost + 1, incluido el carácter <strong>nulo</strong>final.</span><span class="sxs-lookup"><span data-stu-id="9a742-170">The buffer must be at least JET_cbNameMost + 1, including the terminating <strong>NULL</strong>.</span></span> <span data-ttu-id="9a742-171">Si la tabla es una tabla derivada, el búfer se rellenará con el nombre de la tabla de la que la tabla derivada heredó su DDL.</span><span class="sxs-lookup"><span data-stu-id="9a742-171">If the table is a derived table, the buffer will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="9a742-172">Si la tabla no es una tabla derivada, el búfer será una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="9a742-172">If the table is not a derived table, the buffer will an empty string.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9a742-173">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a742-173">Return Value</span></span>

<span data-ttu-id="9a742-174">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="9a742-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9a742-175">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9a742-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a742-176">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9a742-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="9a742-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a742-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a742-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9a742-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9a742-179">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9a742-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-180">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="9a742-180">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="9a742-181">El búfer era demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="9a742-181">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a742-182">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="9a742-182">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="9a742-183">Se ha especificado un <em>InfoLevel</em> en desuso.</span><span class="sxs-lookup"><span data-stu-id="9a742-183">A deprecated <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-184">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="9a742-184">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="9a742-185">El tamaño del búfer no era el correcto.</span><span class="sxs-lookup"><span data-stu-id="9a742-185">The buffer was not the right size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a742-186">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="9a742-186">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="9a742-187">La tabla que se pasó era una tabla temporal y el <em>InfoLevel</em> solicitado no se puede recuperar para una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9a742-187">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-188">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="9a742-188">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="9a742-189">La tabla que se pasó era una tabla temporal y el <em>InfoLevel</em> solicitado no se puede recuperar para una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="9a742-189">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a742-190">JET_errQueryNotSupported</span><span class="sxs-lookup"><span data-stu-id="9a742-190">JET_errQueryNotSupported</span></span></p></td>
<td><p><span data-ttu-id="9a742-191">No se admite <em>InfoLevel</em> .</span><span class="sxs-lookup"><span data-stu-id="9a742-191">The <em>InfoLevel</em> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-192">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="9a742-192">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="9a742-193">Otra operación de base de datos está utilizando la tabla.</span><span class="sxs-lookup"><span data-stu-id="9a742-193">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a742-194">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="9a742-194">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="9a742-195">La tabla está bloqueada por otra operación de base de datos.</span><span class="sxs-lookup"><span data-stu-id="9a742-195">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-196">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="9a742-196">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="9a742-197">El sistema utiliza la tabla.</span><span class="sxs-lookup"><span data-stu-id="9a742-197">The table is being used by the system.</span></span> <span data-ttu-id="9a742-198">Esta advertencia no es grave.</span><span class="sxs-lookup"><span data-stu-id="9a742-198">This warning is nonfatal.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="9a742-199">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a742-199">Remarks</span></span>

<span data-ttu-id="9a742-200">Algunas partes de la información no son válidas para las tablas temporales (vea [JetOpenTempTable](./jetopentemptable-function.md)).</span><span class="sxs-lookup"><span data-stu-id="9a742-200">Some pieces of information are not valid for temporary tables (See [JetOpenTempTable](./jetopentemptable-function.md)).</span></span>

<span data-ttu-id="9a742-201">Las estadísticas de tabla incluyen el número de registros y el número de páginas del índice clúster (es decir, el índice que contiene los datos del registro).</span><span class="sxs-lookup"><span data-stu-id="9a742-201">The table statistics include the number of records and the number of pages in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="9a742-202">Se tiene acceso a las estadísticas de índice por separado por nombre, mediante [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="9a742-202">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="9a742-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a742-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a742-204"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9a742-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9a742-205">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9a742-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-206"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9a742-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9a742-207">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9a742-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a742-208"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9a742-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9a742-209">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="9a742-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-210"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="9a742-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9a742-211">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9a742-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a742-212"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9a742-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9a742-213">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9a742-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a742-214"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9a742-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9a742-215">Se implementa como <strong>JetGetTableInfoW</strong> (Unicode) y <strong>JetGetTableInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9a742-215">Implemented as <strong>JetGetTableInfoW</strong> (Unicode) and <strong>JetGetTableInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9a742-216">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9a742-216">See Also</span></span>

[<span data-ttu-id="9a742-217">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9a742-217">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9a742-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9a742-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9a742-219">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9a742-219">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9a742-220">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9a742-220">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9a742-221">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="9a742-221">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="9a742-222">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="9a742-222">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="9a742-223">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="9a742-223">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="9a742-224">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="9a742-224">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="9a742-225">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="9a742-225">JetOpenTempTable</span></span>](./jetopentemptable-function.md)
