---
description: 'Más información acerca de: JetGetTableColumnInfo (función)'
title: JetGetTableColumnInfo función)
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8c7b073ca9be90e89a1c6b99c010707e6405323
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104280545"
---
# <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="1329a-103">JetGetTableColumnInfo función)</span><span class="sxs-lookup"><span data-stu-id="1329a-103">JetGetTableColumnInfo Function</span></span>


<span data-ttu-id="1329a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1329a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="1329a-105">JetGetTableColumnInfo función)</span><span class="sxs-lookup"><span data-stu-id="1329a-105">JetGetTableColumnInfo Function</span></span>

<span data-ttu-id="1329a-106">La función **JetGetTableColumnInfo** recupera información sobre una columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="1329a-106">The **JetGetTableColumnInfo** function retrieves information about a table column.</span></span>

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a><span data-ttu-id="1329a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1329a-107">Parameters</span></span>

<span data-ttu-id="1329a-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1329a-108">*sesid*</span></span>

<span data-ttu-id="1329a-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="1329a-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="1329a-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="1329a-110">*tableid*</span></span>

<span data-ttu-id="1329a-111">Tabla que contiene la columna para la que se va a obtener información.</span><span class="sxs-lookup"><span data-stu-id="1329a-111">The table that contains the column to fetch information for.</span></span>

<span data-ttu-id="1329a-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="1329a-112">*szColumnName*</span></span>

<span data-ttu-id="1329a-113">Nombre de la columna para la que se va a obtener información.</span><span class="sxs-lookup"><span data-stu-id="1329a-113">The name of the column to fetch information for.</span></span>

<span data-ttu-id="1329a-114">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="1329a-114">*pvResult*</span></span>

<span data-ttu-id="1329a-115">Puntero a un búfer que recibirá la información.</span><span class="sxs-lookup"><span data-stu-id="1329a-115">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="1329a-116">El tipo de búfer depende de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="1329a-116">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="1329a-117">El autor de la llamada debe estar configurado para alinear el búfer adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="1329a-117">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="1329a-118">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="1329a-118">*cbMax*</span></span>

<span data-ttu-id="1329a-119">Tamaño, en bytes, del búfer que se pasó en *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="1329a-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="1329a-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="1329a-120">*InfoLevel*</span></span>

<span data-ttu-id="1329a-121">El tipo de información que se recuperará para la columna especificada por *szColumnName*.</span><span class="sxs-lookup"><span data-stu-id="1329a-121">The type of information that will be retrieved for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="1329a-122">El formato de los datos que se almacenan en *pvResult* depende de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="1329a-122">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span> <span data-ttu-id="1329a-123">Para obtener el esquema de la tabla temporal, vea [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="1329a-123">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

  - <span data-ttu-id="1329a-124">JET_ColInfoListSortColumnid ordenará la tabla temporal por *columnid*.</span><span class="sxs-lookup"><span data-stu-id="1329a-124">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="1329a-125">JET_ColInfoListCompact compactará la salida.</span><span class="sxs-lookup"><span data-stu-id="1329a-125">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="1329a-126">Para obtener más información sobre la salida de Compact, consulte [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="1329a-126">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="1329a-127">Se pueden establecer las siguientes opciones para este parámetro:</span><span class="sxs-lookup"><span data-stu-id="1329a-127">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1329a-128">Value</span><span class="sxs-lookup"><span data-stu-id="1329a-128">Value</span></span></p></th>
<th><p><span data-ttu-id="1329a-129">Significado</span><span class="sxs-lookup"><span data-stu-id="1329a-129">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1329a-130">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="1329a-130">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="1329a-131"><em>pvResult</em> se interpreta como un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>y los campos de la estructura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> se rellenan de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="1329a-131"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span> <span data-ttu-id="1329a-132">JET_ColInfo y JET_ColInfoByColid recuperan la misma información.</span><span class="sxs-lookup"><span data-stu-id="1329a-132">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1329a-133">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="1329a-133">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="1329a-134"><em>pvResult</em> se interpreta como una estructura de <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> .</span><span class="sxs-lookup"><span data-stu-id="1329a-134"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="1329a-135">Esto es similar a una estructura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> .</span><span class="sxs-lookup"><span data-stu-id="1329a-135">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="1329a-136">Si esta función se ejecuta correctamente, la estructura se rellena con los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="1329a-136">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="1329a-137">Si se produce un error en esta función, la estructura contiene datos sin definir.</span><span class="sxs-lookup"><span data-stu-id="1329a-137">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1329a-138">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="1329a-138">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="1329a-139"><em>pvResult</em> se interpreta como <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, excepto en que <em>InfoLevel</em> indica que la columna solicitada (<em>szColumName</em>) no es el nombre de la columna de cadena, sino un puntero a una <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="1329a-139"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span> <span data-ttu-id="1329a-140">JET_ColInfo y JET_ColInfoByColid recuperan la misma información.</span><span class="sxs-lookup"><span data-stu-id="1329a-140">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1329a-141">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="1329a-141">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="1329a-142"><em>pvResult</em> se interpreta como una estructura de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="1329a-142"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="1329a-143">Si esta función se ejecuta correctamente, la estructura se rellena con los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="1329a-143">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="1329a-144">Se abre una tabla temporal que se identifica mediante el miembro <em>TABLEID</em> de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="1329a-144">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="1329a-145">La tabla debe cerrarse con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="1329a-145">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="1329a-146">Si se produce un error en esta función, la estructura contiene datos sin definir.</span><span class="sxs-lookup"><span data-stu-id="1329a-146">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1329a-147">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="1329a-147">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="1329a-148"><em>pvResult</em> se interpreta como una estructura de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="1329a-148"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="1329a-149">Si esta función se ejecuta correctamente, la estructura se rellena con los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="1329a-149">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="1329a-150">Se abre una tabla temporal que se identifica mediante el miembro <em>TABLEID</em> de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="1329a-150">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="1329a-151">La tabla debe cerrarse con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="1329a-151">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="1329a-152">Si se produce un error en esta función, la estructura contiene datos sin definir.</span><span class="sxs-lookup"><span data-stu-id="1329a-152">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1329a-153">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="1329a-153">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="1329a-154">Igual que JET_ColInfoList, sin embargo, la tabla resultante se ordena por <em>columnid</em>, en lugar de por nombre de columna.</span><span class="sxs-lookup"><span data-stu-id="1329a-154">Same as JET_ColInfoList, however the resulting table is sorted by <em>columnid</em>, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1329a-155">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="1329a-155">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="1329a-156">JET_ColInfoSysTabCursor está en desuso y el uso de él devolverá JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="1329a-156">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1329a-157">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="1329a-157">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="1329a-158">Igual que JET_ColInfoBase, <em>pvResult</em> se interpreta como un <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, con la excepción de que <em>InfoLevel</em> indica que la columna solicitada (<em>szColumName</em>) no es el nombre de la columna de cadena, sino un puntero a una <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="1329a-158">Same as JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="1329a-159"><strong>Windows Vista:  </strong> Está disponible en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1329a-159"><strong>Windows Vista:  </strong>This is available in Windows Vista and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1329a-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="1329a-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="1329a-161">Devolver solo columnas no derivadas (si la tabla se deriva de una plantilla).</span><span class="sxs-lookup"><span data-stu-id="1329a-161">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="1329a-162">Este valor puede ser lógicamente o debe encontrarse en el <em>InfoLevel</em>, cuando el <em>InfoLevel</em> base está JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="1329a-162">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="1329a-163"><strong>Windows Vista:  </strong> Este valor se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1329a-163"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1329a-164">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="1329a-164">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="1329a-165">Devuelva solo el nombre de columna y el columnid de cada columna.</span><span class="sxs-lookup"><span data-stu-id="1329a-165">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="1329a-166">Este valor puede ser lógicamente o debe encontrarse en el <em>InfoLevel</em>, cuando el <em>InfoLevel</em> base está JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="1329a-166">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="1329a-167"><strong>Windows Vista:  </strong> Este valor se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1329a-167"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1329a-168">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="1329a-168">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="1329a-169">Orden devuelto de la lista de columnas por columnid (el valor predeterminado es ordenar la lista por nombre de columna).</span><span class="sxs-lookup"><span data-stu-id="1329a-169">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="1329a-170">Este valor puede ser lógicamente o debe encontrarse en el <em>InfoLevel</em>, cuando el <em>InfoLevel</em> base está JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="1329a-170">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="1329a-171"><strong>Windows Vista:  </strong> Este valor se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1329a-171"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="1329a-172">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1329a-172">Return Value</span></span>

<span data-ttu-id="1329a-173">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="1329a-173">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1329a-174">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1329a-174">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1329a-175">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1329a-175">Return code</span></span></p></th>
<th><p><span data-ttu-id="1329a-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="1329a-176">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1329a-177">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1329a-177">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1329a-178">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1329a-178">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1329a-179">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="1329a-179">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="1329a-180">No se encontró la columna denominada <em>szColumnName</em> en la tabla.</span><span class="sxs-lookup"><span data-stu-id="1329a-180">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1329a-181">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="1329a-181">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="1329a-182">Se ha especificado un <em>InfoLevel</em> incorrecto.</span><span class="sxs-lookup"><span data-stu-id="1329a-182">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1329a-183">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="1329a-183">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="1329a-184">Este error se puede devolver si:</span><span class="sxs-lookup"><span data-stu-id="1329a-184">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="1329a-185">Se proporcionó un nombre incorrecto para <em>szTableName</em> .</span><span class="sxs-lookup"><span data-stu-id="1329a-185">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="1329a-186">Se proporcionó un nombre incorrecto para <em>szColumnName</em> .</span><span class="sxs-lookup"><span data-stu-id="1329a-186">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1329a-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1329a-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1329a-188">Este error se puede devolver si:</span><span class="sxs-lookup"><span data-stu-id="1329a-188">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="1329a-189">Se ha especificado un <em>InfoLevel</em> incorrecto.</span><span class="sxs-lookup"><span data-stu-id="1329a-189">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="1329a-190">Se pasó un valor de <em>szTableName</em> nulo.</span><span class="sxs-lookup"><span data-stu-id="1329a-190">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="1329a-191">El búfer es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="1329a-191">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="1329a-192">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1329a-192">Remarks</span></span>

<span data-ttu-id="1329a-193">**JetGetTableColumnInfo** y [JetGetColumnInfo](./jetgetcolumninfo-function.md) recuperan información sobre una columna.</span><span class="sxs-lookup"><span data-stu-id="1329a-193">**JetGetTableColumnInfo** and [JetGetColumnInfo](./jetgetcolumninfo-function.md) both retrieve information about a column.</span></span> <span data-ttu-id="1329a-194">La diferencia entre ellos es cómo se identifica la tabla:</span><span class="sxs-lookup"><span data-stu-id="1329a-194">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="1329a-195">**JetGetTableColumnInfo** identifica una tabla mediante *TABLEID*.</span><span class="sxs-lookup"><span data-stu-id="1329a-195">**JetGetTableColumnInfo** identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="1329a-196">[JetGetColumnInfo](./jetgetcolumninfo-function.md) identifica una tabla por la combinación de *DBID* y *szTableName* .</span><span class="sxs-lookup"><span data-stu-id="1329a-196">[JetGetColumnInfo](./jetgetcolumninfo-function.md) identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="1329a-197">Al recuperar datos con JET_ColInfoList, JET_ColInfoListSortColumnid o JET_ColInfoListCompact, se abrirá una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="1329a-197">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="1329a-198">La tabla temporal contiene datos y la estructura [JET_COLUMNLIST](./jet-columnlist-structure.md) contiene información suficiente para atravesar la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="1329a-198">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="1329a-199">La tabla temporal debe cerrarse con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="1329a-199">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="1329a-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1329a-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1329a-201"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="1329a-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1329a-202">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1329a-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1329a-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1329a-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1329a-204">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1329a-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1329a-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1329a-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1329a-206">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="1329a-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1329a-207"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="1329a-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1329a-208">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1329a-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1329a-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1329a-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1329a-210">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1329a-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1329a-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1329a-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1329a-212">Se implementa como <strong>JetGetTableColumnInfoW</strong> (Unicode) y <strong>JetGetTableColumnInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1329a-212">Implemented as <strong>JetGetTableColumnInfoW</strong> (Unicode) and <strong>JetGetTableColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1329a-213">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1329a-213">See Also</span></span>

[<span data-ttu-id="1329a-214">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="1329a-214">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="1329a-215">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="1329a-215">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="1329a-216">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="1329a-216">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="1329a-217">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="1329a-217">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="1329a-218">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="1329a-218">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="1329a-219">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="1329a-219">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="1329a-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1329a-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1329a-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1329a-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1329a-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1329a-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1329a-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1329a-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1329a-224">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="1329a-224">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="1329a-225">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="1329a-225">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="1329a-226">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="1329a-226">JetGetTableColumnInfo</span></span>]()
