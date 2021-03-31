---
description: 'Más información acerca de: JetGetDatabaseInfo (función)'
title: Función JetGetDatabaseInfo
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c414a1dd38f621ba86bf7b1c9ce87710801446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277102"
---
# <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="ae2b8-103">Función JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="ae2b8-103">JetGetDatabaseInfo Function</span></span>


<span data-ttu-id="ae2b8-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ae2b8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="ae2b8-105">Función JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="ae2b8-105">JetGetDatabaseInfo Function</span></span>

<span data-ttu-id="ae2b8-106">La función **JetGetDatabaseInfo** Recupera varios tipos de información sobre la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-106">The **JetGetDatabaseInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="ae2b8-107">Se puede llamar a esta API mientras una base de datos está conectada o en línea (con **JetGetDatabaseInfo**) o mientras la base de datos o el motor de base de datos está sin conexión (con [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).</span><span class="sxs-lookup"><span data-stu-id="ae2b8-107">This API can be called while a database is attached or online (with **JetGetDatabaseInfo**) or while the database or database engine is offline (with [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="ae2b8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae2b8-108">Parameters</span></span>

<span data-ttu-id="ae2b8-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ae2b8-109">*sesid*</span></span>

<span data-ttu-id="ae2b8-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-110">The session to use for this call.</span></span>

<span data-ttu-id="ae2b8-111">*DBID*</span><span class="sxs-lookup"><span data-stu-id="ae2b8-111">*dbid*</span></span>

<span data-ttu-id="ae2b8-112">[JET_DBID](./jet-dbid.md) de la base de datos de la que se va a recuperar la información.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-112">The [JET_DBID](./jet-dbid.md) for the database to retrieve the information from.</span></span>

<span data-ttu-id="ae2b8-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="ae2b8-113">*pvResult*</span></span>

<span data-ttu-id="ae2b8-114">Puntero a un búfer que recibirá la información especificada.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-114">Pointer to a buffer which will receive the specified information.</span></span> <span data-ttu-id="ae2b8-115">El tamaño del búfer, en bytes, se pasa en *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-115">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="ae2b8-116">En caso de error, el contenido de *pvResult* no está definido.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-116">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="ae2b8-117">La información almacenada en *pvResult* depende de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-117">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="ae2b8-118">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="ae2b8-118">*cbMax*</span></span>

<span data-ttu-id="ae2b8-119">Tamaño, en bytes, del búfer que se pasó en *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="ae2b8-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="ae2b8-120">*InfoLevel*</span></span>

<span data-ttu-id="ae2b8-121">*InfoLevel* especifica qué tipo de información se debe recuperar en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-121">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="ae2b8-122">Afecta al modo en que se interpreta *pvResult* .</span><span class="sxs-lookup"><span data-stu-id="ae2b8-122">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="ae2b8-123">Algunos *InfoLevel* solo están disponibles en la versión sin conexión ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) o en línea (**JetGetDatabaseInfo**) de la API.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-123">Some *InfoLevel* are available only in the offline ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) or online (**JetGetDatabaseInfo**) version of the API.</span></span>

<span data-ttu-id="ae2b8-124">Si el búfer de *pvResult* proporcionado es demasiado pequeño, se devolverá JET_errInvalidBufferSize o JET_errBufferTooSmall en función de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-124">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae2b8-125">Value</span><span class="sxs-lookup"><span data-stu-id="ae2b8-125">Value</span></span></p></th>
<th><p><span data-ttu-id="ae2b8-126">Significado</span><span class="sxs-lookup"><span data-stu-id="ae2b8-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-127">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="ae2b8-127">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-128">Todavía no se admiten y devuelven valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-128">Not yet supported and return default values.</span></span> <span data-ttu-id="ae2b8-129">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-129">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2b8-130">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="ae2b8-130">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-131">Estos <em>InfoLevels</em> están desusados y no se admiten actualmente.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-131">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="ae2b8-132">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-132">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-133">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="ae2b8-133">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-134">Todavía no se admiten y devuelven valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-134">Not yet supported and return default values.</span></span> <span data-ttu-id="ae2b8-135">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-135">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2b8-136">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="ae2b8-136">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-137">Todavía no se admiten y devuelven valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-137">Not yet supported and return default values.</span></span> <span data-ttu-id="ae2b8-138">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-138">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-139">JET_DbInfoFilename</span><span class="sxs-lookup"><span data-stu-id="ae2b8-139">JET_DbInfoFilename</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-140"><em>pvResult</em> se interpretará como un búfer de cadena (Char \*).</span><span class="sxs-lookup"><span data-stu-id="ae2b8-140"><em>pvResult</em> will be interpreted as a string buffer (char \*).</span></span> <span data-ttu-id="ae2b8-141">No obstante, se sugiere un búfer de MAX_PATH.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-141">A MAX_PATH buffer is suggested, however not required.</span></span> <span data-ttu-id="ae2b8-142">Si el búfer no es suficientemente largo, se devolverá JET_errBufferTooSmall.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-142">If the buffer is not long enough, JET_errBufferTooSmall will be returned.</span></span> <span data-ttu-id="ae2b8-143">La cadena se rellenará con la ruta de acceso de la base de datos para este DBID.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-143">The string will be populated with the path of the database for this DBID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2b8-144">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="ae2b8-144">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-145"><em>pvResult</em> se interpretará como un valor DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="ae2b8-145"><em>pvResult</em> will be interpreted as a DWORD (4 bytes).</span></span> <span data-ttu-id="ae2b8-146">Devuelve el tamaño de la base de datos en páginas.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-146">Returns the size of the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-147">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="ae2b8-147">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-148">Estos <em>InfoLevels</em> están desusados y no se admiten actualmente.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-148">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="ae2b8-149">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-149">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2b8-150">JET_DbInfoLCID</span><span class="sxs-lookup"><span data-stu-id="ae2b8-150">JET_DbInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-151">(Windows XP y versiones posteriores) Este <em>InfoLevel</em> se especificó originalmente como: JET_DbInfoLangid (Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="ae2b8-151">(Windows XP and later) This <em>InfoLevel</em> was originally specified as: JET_DbInfoLangid (Windows 2000)</span></span></p>
<p><span data-ttu-id="ae2b8-152"><em>pvResult</em> se interpretará como un valor Long.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-152"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="ae2b8-153">Esto devuelve el identificador de configuración regional (LCID) asociado a esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-153">This returns the Locale identifier (LCID) associate with this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-154">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="ae2b8-154">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-155"><em>pvResult</em> se interpretará como un <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-155"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="ae2b8-156">La estructura de <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> se rellenará con información relativa a la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-156">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the database specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2b8-157">JET_DbInfoOptions</span><span class="sxs-lookup"><span data-stu-id="ae2b8-157">JET_DbInfoOptions</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-158"><em>pvResult</em> se interpretará como un <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD).</span><span class="sxs-lookup"><span data-stu-id="ae2b8-158"><em>pvResult</em> will be interpreted as a <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD).</span></span> <span data-ttu-id="ae2b8-159">Esto devuelve si la base de datos se abre en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-159">This returns whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="ae2b8-160">Si la base de datos está en modo exclusivo JET_bitDbExclusive se establecerá en el <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> proporcionado; de lo contrario, se establecerá cero.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-160">If the database is in exclusive mode JET_bitDbExclusive will be set in the <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> provided, otherwise zero is set.</span></span> <span data-ttu-id="ae2b8-161">Tenga en cuenta que no se devuelven otras opciones de <em>grbit</em> de base de datos para <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> y <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> .</span><span class="sxs-lookup"><span data-stu-id="ae2b8-161">Note other database <em>grbit</em> options for <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> and <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> are not returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-162">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="ae2b8-162">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-163">Solo disponible en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-163">Available only on Windows XP and later.</span></span> <span data-ttu-id="ae2b8-164"><em>pvResult</em> se interpretará como una longitud sin signo.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-164"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="ae2b8-165">Esto devolverá el tamaño de página de la base de datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-165">This will return the page size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2b8-166">JET_DbInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="ae2b8-166">JET_DbInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-167"><em>pvResult</em> se interpretará como un valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-167"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="ae2b8-168">Esto devuelve el espacio disponible para la base de datos en páginas.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-168">This returns the available space for the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-169">JET_DbInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="ae2b8-169">JET_DbInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-170"><em>pvResult</em> se interpretará como un valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-170"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="ae2b8-171">Esto devuelve el espacio de propiedad de la base de datos en páginas.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-171">This returns the owned space for the database in pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2b8-172">JET_DbInfoTransactions</span><span class="sxs-lookup"><span data-stu-id="ae2b8-172">JET_DbInfoTransactions</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-173"><em>pvResult</em> se interpretará como un valor Long.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-173"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="ae2b8-174">Esto devolverá un valor mayor que el nivel máximo en el que se pueden anidar las transacciones.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-174">This will return one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="ae2b8-175">Si se llama a <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> (en modo de anidamiento, es decir, en la misma sesión, sin commit o rollback) tantas veces como este valor, en la última llamada JET_errTransTooDeep se devolverá desde <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-175">If <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call JET_errTransTooDeep will be returned from <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>.</span></span> <span data-ttu-id="ae2b8-176">Tenga en cuenta que el valor de Windows 2000, Windows XP y Windows Server 2003 es 7.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-176">Note the value in Windows 2000, Windows XP, and Windows Server 2003 is 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-177">JET_DbInfoVersion</span><span class="sxs-lookup"><span data-stu-id="ae2b8-177">JET_DbInfoVersion</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-178"><em>pvResult</em> se interpretará como un valor Long.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-178"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="ae2b8-179">Esto devuelve la versión principal nativa del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-179">This returns the database engine's native major version.</span></span> <span data-ttu-id="ae2b8-180">Este valor es 0x620 para Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-180">This value is 0x620 for Windows 2000, Windows XP, and Windows Server 2003.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ae2b8-181">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae2b8-181">Return Value</span></span>

<span data-ttu-id="ae2b8-182">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ae2b8-183">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ae2b8-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae2b8-184">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ae2b8-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="ae2b8-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae2b8-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ae2b8-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-187">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2b8-188">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="ae2b8-188">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-189">El tamaño del búfer proporcionado en <em>cbMax</em> era demasiado pequeño (o no correcto) para contener la información deseada.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-189">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-190">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="ae2b8-190">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-191">La <em>InfoLevel</em> solicitada se JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-191">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="ae2b8-192">Esto no se admite.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-192">This is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2b8-193">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="ae2b8-193">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-194">El tamaño del búfer proporcionado en <em>cbMax</em> era demasiado pequeño (o no correcto) para contener la información deseada.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-194">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-195">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ae2b8-195">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ae2b8-196">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-196">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="ae2b8-197"><strong>JetGetDatabaseInfo</strong> devolverá este error cuando el <a href="gg269248(v=exchg.10).md">JET_DBID</a> proporcionado no sea una base de datos válida (adjunta).</span><span class="sxs-lookup"><span data-stu-id="ae2b8-197">This error will be returned by <strong>JetGetDatabaseInfo</strong> when the <a href="gg269248(v=exchg.10).md">JET_DBID</a> provided is not a valid (attached) database.</span></span> <span data-ttu-id="ae2b8-198">Este error lo devolverá <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> y <strong>JetGetDatabaseInfo</strong> cuando una <em>InfoLevel</em> solicitada no sea compatible con esa versión de la función.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-198">This error will be returned by <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> and <strong>JetGetDatabaseInfo</strong> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ae2b8-199">Si se ejecuta correctamente, los datos solicitados se devolverán en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-199">On success, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="ae2b8-200">En caso de error, el búfer de salida estará en un estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-200">On failure, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ae2b8-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae2b8-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-202"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ae2b8-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ae2b8-203">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2b8-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ae2b8-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ae2b8-205">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ae2b8-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ae2b8-207">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2b8-208"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="ae2b8-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ae2b8-209">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae2b8-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ae2b8-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ae2b8-211">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ae2b8-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2b8-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ae2b8-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ae2b8-213">Se implementa como <strong>JetGetDatabaseInfoW</strong> (Unicode) y <strong>JetGetDatabaseInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ae2b8-213">Implemented as <strong>JetGetDatabaseInfoW</strong> (Unicode) and <strong>JetGetDatabaseInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ae2b8-214">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ae2b8-214">See Also</span></span>

[<span data-ttu-id="ae2b8-215">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="ae2b8-215">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="ae2b8-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ae2b8-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ae2b8-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ae2b8-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ae2b8-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ae2b8-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ae2b8-219">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="ae2b8-219">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="ae2b8-220">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="ae2b8-220">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="ae2b8-221">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="ae2b8-221">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
