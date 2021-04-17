---
description: 'Más información acerca de: JetGetColumnInfo (función)'
title: Función JetGetColumnInfo
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d96d5860f4b10f9294ab210e4e41d78cede202f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716512"
---
# <a name="jetgetcolumninfo-function"></a><span data-ttu-id="60785-103">Función JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="60785-103">JetGetColumnInfo Function</span></span>


<span data-ttu-id="60785-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="60785-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcolumninfo-function"></a><span data-ttu-id="60785-105">Función JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="60785-105">JetGetColumnInfo Function</span></span>

<span data-ttu-id="60785-106">La función **JetGetColumnInfo** recupera información acerca de una columna.</span><span class="sxs-lookup"><span data-stu-id="60785-106">The **JetGetColumnInfo** function retrieves information about a column.</span></span>

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="60785-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60785-107">Parameters</span></span>

<span data-ttu-id="60785-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="60785-108">*sesid*</span></span>

<span data-ttu-id="60785-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="60785-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="60785-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="60785-110">*dbid*</span></span>

<span data-ttu-id="60785-111">Identifica, junto con *szTableName*, la tabla que contiene la columna de la que se recupera la información.</span><span class="sxs-lookup"><span data-stu-id="60785-111">Identifies, along with *szTableName*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="60785-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="60785-112">*szTableName*</span></span>

<span data-ttu-id="60785-113">Identifica, junto con *DBID*, la tabla que contiene la columna de la que se recupera la información.</span><span class="sxs-lookup"><span data-stu-id="60785-113">Identifies, along with *dbid*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="60785-114">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="60785-114">*szColumnName*</span></span>

<span data-ttu-id="60785-115">Nombre de la columna para la que se captura la información.</span><span class="sxs-lookup"><span data-stu-id="60785-115">The name of the column that information is fetched for.</span></span>

<span data-ttu-id="60785-116">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="60785-116">*pvResult*</span></span>

<span data-ttu-id="60785-117">Puntero a un búfer que recibirá la información.</span><span class="sxs-lookup"><span data-stu-id="60785-117">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="60785-118">El tipo de búfer depende de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="60785-118">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="60785-119">El autor de la llamada debe estar configurado para alinear el búfer adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="60785-119">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="60785-120">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="60785-120">*cbMax*</span></span>

<span data-ttu-id="60785-121">Tamaño, en bytes, del búfer que se pasa en *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="60785-121">The size, in bytes, of the buffer that is passed in *pvResult*.</span></span>

<span data-ttu-id="60785-122">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="60785-122">*InfoLevel*</span></span>

<span data-ttu-id="60785-123">Tipo de información que se va a recuperar para la columna especificada por *szColumnName*.</span><span class="sxs-lookup"><span data-stu-id="60785-123">The type of information to retrieve for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="60785-124">El formato de los datos almacenados en *pvResult* depende de este parámetro.</span><span class="sxs-lookup"><span data-stu-id="60785-124">The format of the data stored in *pvResult* is dependent on this parameter.</span></span> <span data-ttu-id="60785-125">Para obtener el esquema de la tabla temporal, vea [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="60785-125">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="60785-126">Estos *InfoLevels* se diferencian en lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="60785-126">These *InfoLevels* are differentiated by:</span></span>

  - <span data-ttu-id="60785-127">JET_ColInfoListSortColumnid ordenará la tabla temporal por *columnid*.</span><span class="sxs-lookup"><span data-stu-id="60785-127">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="60785-128">JET_ColInfoListCompact compactará la salida.</span><span class="sxs-lookup"><span data-stu-id="60785-128">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="60785-129">Para obtener más información sobre la salida de Compact, consulte [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="60785-129">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="60785-130">Las siguientes opciones están disponibles para su uso con este parámetro.</span><span class="sxs-lookup"><span data-stu-id="60785-130">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60785-131">Value</span><span class="sxs-lookup"><span data-stu-id="60785-131">Value</span></span></p></th>
<th><p><span data-ttu-id="60785-132">Significado</span><span class="sxs-lookup"><span data-stu-id="60785-132">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60785-133">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="60785-133">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="60785-134">JET_ColInfo y JET_ColInfoByColid recuperan la misma información.</span><span class="sxs-lookup"><span data-stu-id="60785-134">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span> <span data-ttu-id="60785-135"><em>pvResult</em> se interpreta como un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>y los campos de la estructura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> se rellenan de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="60785-135"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60785-136">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="60785-136">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="60785-137"><em>pvResult</em> se interpreta como una estructura de <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> .</span><span class="sxs-lookup"><span data-stu-id="60785-137"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="60785-138">Esto es similar a una estructura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> .</span><span class="sxs-lookup"><span data-stu-id="60785-138">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="60785-139">Si esta función se ejecuta correctamente, la estructura se rellena con los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="60785-139">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="60785-140">Si se produce un error en esta función, la estructura contiene datos sin definir.</span><span class="sxs-lookup"><span data-stu-id="60785-140">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60785-141">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="60785-141">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="60785-142">Como JET_ColInfo, <em>pvResult</em> se interpreta como un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, con la excepción de que <em>InfoLevel</em> indica que la columna solicitada (<em>szColumName</em>) no es el nombre de la columna de cadena, sino un puntero a una <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="60785-142">Like JET_ColInfo, <em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60785-143">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="60785-143">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="60785-144"><em>pvResult</em> se interpreta como una estructura de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="60785-144"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="60785-145">Si esta función se ejecuta correctamente, la estructura se rellena con los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="60785-145">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="60785-146">Se abre una tabla temporal que se identifica mediante el miembro <strong>TABLEID</strong> de la estructura <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="60785-146">A temporary table is opened and is identified by the <strong>tableid</strong> member of the <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="60785-147">La tabla debe cerrarse con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="60785-147">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="60785-148">Si se produce un error en esta función, la estructura contiene datos sin definir.</span><span class="sxs-lookup"><span data-stu-id="60785-148">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60785-149">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="60785-149">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="60785-150">Igual que JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="60785-150">Same as JET_ColInfoList.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60785-151">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="60785-151">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="60785-152">Igual que JET_ColInfoList; sin embargo, la tabla resultante se ordena por columnid, en lugar de por nombre de columna.</span><span class="sxs-lookup"><span data-stu-id="60785-152">Same as JET_ColInfoList; however the resulting table is sorted by columnid, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60785-153">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="60785-153">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="60785-154">JET_ColInfoSysTabCursor está en desuso y el uso de él devolverá JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="60785-154">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60785-155">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="60785-155">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="60785-156">Como JET_ColInfoBase, <em>pvResult</em> se interpreta como un <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, con la excepción de que <em>InfoLevel</em> indica que la columna solicitada (<em>szColumName</em>) no es el nombre de la columna de cadena, sino un puntero a una <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="60785-156">Like JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="60785-157"><strong>Windows Vista:  </strong> Este valor se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="60785-157"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60785-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="60785-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="60785-159">Devolver solo columnas no derivadas (si la tabla se deriva de una plantilla).</span><span class="sxs-lookup"><span data-stu-id="60785-159">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="60785-160">Este valor puede ser lógicamente o debe encontrarse en el <em>InfoLevel</em>, cuando el <em>InfoLevel</em> base está JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="60785-160">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="60785-161"><strong>Windows Vista:  </strong> Este valor se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="60785-161"><strong>Windows Vista:  </strong>This value is introduced Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60785-162">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="60785-162">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="60785-163">Devuelva solo el nombre de columna y el columnid de cada columna.</span><span class="sxs-lookup"><span data-stu-id="60785-163">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="60785-164">Este valor puede ser lógicamente o debe encontrarse en el <em>InfoLevel</em>, cuando el <em>InfoLevel</em> base está JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="60785-164">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="60785-165"><strong>Windows Vista:  </strong> Este valor se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="60785-165"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60785-166">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="60785-166">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="60785-167">Orden devuelto de la lista de columnas por columnid (el valor predeterminado es ordenar la lista por nombre de columna).</span><span class="sxs-lookup"><span data-stu-id="60785-167">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="60785-168">Este valor puede ser lógicamente o debe encontrarse en el <em>InfoLevel</em>, cuando el <em>InfoLevel</em> base está JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="60785-168">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="60785-169"><strong>Windows Vista:  </strong> Este valor se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="60785-169"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="60785-170">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60785-170">Return Value</span></span>

<span data-ttu-id="60785-171">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="60785-171">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="60785-172">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="60785-172">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60785-173">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="60785-173">Return code</span></span></p></th>
<th><p><span data-ttu-id="60785-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="60785-174">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60785-175">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="60785-175">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="60785-176">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="60785-176">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60785-177">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="60785-177">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="60785-178">No se encontró la columna denominada <em>szColumnName</em> en la tabla.</span><span class="sxs-lookup"><span data-stu-id="60785-178">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60785-179">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="60785-179">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="60785-180">Se ha especificado un <em>InfoLevel</em> incorrecto.</span><span class="sxs-lookup"><span data-stu-id="60785-180">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60785-181">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="60785-181">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="60785-182">Este error se puede devolver si:</span><span class="sxs-lookup"><span data-stu-id="60785-182">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="60785-183">Se proporcionó un nombre incorrecto para <em>szTableName</em> .</span><span class="sxs-lookup"><span data-stu-id="60785-183">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="60785-184">Se proporcionó un nombre incorrecto para <em>szColumnName</em> .</span><span class="sxs-lookup"><span data-stu-id="60785-184">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60785-185">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="60785-185">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="60785-186">Este error se puede devolver si:</span><span class="sxs-lookup"><span data-stu-id="60785-186">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="60785-187">Se ha especificado un <em>InfoLevel</em> incorrecto.</span><span class="sxs-lookup"><span data-stu-id="60785-187">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="60785-188">Se pasó un valor de <em>szTableName</em> nulo.</span><span class="sxs-lookup"><span data-stu-id="60785-188">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="60785-189">El búfer es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="60785-189">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="60785-190">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60785-190">Remarks</span></span>

<span data-ttu-id="60785-191">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) y **JetGetColumnInfo** recuperan información sobre una columna.</span><span class="sxs-lookup"><span data-stu-id="60785-191">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) and **JetGetColumnInfo** both retrieve information about a column.</span></span> <span data-ttu-id="60785-192">La diferencia entre ellos es cómo se identifica la tabla:</span><span class="sxs-lookup"><span data-stu-id="60785-192">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="60785-193">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifica una tabla mediante *TABLEID*.</span><span class="sxs-lookup"><span data-stu-id="60785-193">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="60785-194">**JetGetColumnInfo** identifica una tabla por la combinación de *DBID* y *szTableName* .</span><span class="sxs-lookup"><span data-stu-id="60785-194">**JetGetColumnInfo** identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="60785-195">Al recuperar datos con JET_ColInfoList, JET_ColInfoListSortColumnid o JET_ColInfoListCompact, se abrirá una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="60785-195">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="60785-196">La tabla temporal contiene datos y la estructura [JET_COLUMNLIST](./jet-columnlist-structure.md) contiene información suficiente para atravesar la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="60785-196">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="60785-197">La tabla temporal debe cerrarse con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="60785-197">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="60785-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60785-198">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60785-199"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="60785-199"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="60785-200">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="60785-200">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60785-201"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="60785-201"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="60785-202">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="60785-202">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60785-203"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="60785-203"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="60785-204">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="60785-204">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60785-205"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="60785-205"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="60785-206">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="60785-206">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60785-207"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="60785-207"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="60785-208">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="60785-208">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60785-209"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="60785-209"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="60785-210">Se implementa como <strong>JetGetColumnInfoW</strong> (Unicode) y <strong>JetGetColumnInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="60785-210">Implemented as <strong>JetGetColumnInfoW</strong> (Unicode) and <strong>JetGetColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="60785-211">Consulte también</span><span class="sxs-lookup"><span data-stu-id="60785-211">See Also</span></span>

[<span data-ttu-id="60785-212">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="60785-212">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="60785-213">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="60785-213">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="60785-214">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="60785-214">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="60785-215">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="60785-215">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="60785-216">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="60785-216">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="60785-217">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="60785-217">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="60785-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="60785-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="60785-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="60785-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="60785-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="60785-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="60785-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="60785-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="60785-222">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="60785-222">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="60785-223">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="60785-223">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
