---
description: 'Más información acerca de: JetGetDatabaseFileInfo (función)'
title: JetGetDatabaseFileInfo función)
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ac94dd6f088a82c932aaca5b60ec16f49644f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659991"
---
# <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="27c67-103">JetGetDatabaseFileInfo función)</span><span class="sxs-lookup"><span data-stu-id="27c67-103">JetGetDatabaseFileInfo Function</span></span>


<span data-ttu-id="27c67-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="27c67-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="27c67-105">JetGetDatabaseFileInfo función)</span><span class="sxs-lookup"><span data-stu-id="27c67-105">JetGetDatabaseFileInfo Function</span></span>

<span data-ttu-id="27c67-106">La función **JetGetDatabaseFileInfo** Recupera varios tipos de información sobre la base de datos.</span><span class="sxs-lookup"><span data-stu-id="27c67-106">The **JetGetDatabaseFileInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="27c67-107">Se puede llamar a esta API mientras una base de datos está conectada o en línea (con [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) o mientras la base de datos o el motor de base de datos está sin conexión (con **JetGetDatabaseFileInfo**).</span><span class="sxs-lookup"><span data-stu-id="27c67-107">This API can be called while a database is attached or online (with [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) or while the database or database engine is offline (with **JetGetDatabaseFileInfo**).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="27c67-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27c67-108">Parameters</span></span>

<span data-ttu-id="27c67-109">*szDatabaseName*</span><span class="sxs-lookup"><span data-stu-id="27c67-109">*szDatabaseName*</span></span>

<span data-ttu-id="27c67-110">Ruta de acceso de la base de datos de la que se va a recuperar la información.</span><span class="sxs-lookup"><span data-stu-id="27c67-110">The path of the database from which to retrieve the information.</span></span>

<span data-ttu-id="27c67-111">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="27c67-111">*pvResult*</span></span>

<span data-ttu-id="27c67-112">Puntero a un búfer que recibirá la información especificada.</span><span class="sxs-lookup"><span data-stu-id="27c67-112">Pointer to a buffer that will receive the specified information.</span></span> <span data-ttu-id="27c67-113">El tamaño del búfer, en bytes, se pasa en *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="27c67-113">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="27c67-114">Si se produce un error en esta función, el contenido de *pvResult* no está definido.</span><span class="sxs-lookup"><span data-stu-id="27c67-114">If this function fails, the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="27c67-115">La información almacenada en *pvResult* depende de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="27c67-115">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="27c67-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="27c67-116">*cbMax*</span></span>

<span data-ttu-id="27c67-117">Tamaño, en bytes, del búfer pasado en *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="27c67-117">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="27c67-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="27c67-118">*InfoLevel*</span></span>

<span data-ttu-id="27c67-119">*InfoLevel* especifica qué tipo de información se debe recuperar en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="27c67-119">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="27c67-120">Afecta al modo en que se interpreta *pvResult* .</span><span class="sxs-lookup"><span data-stu-id="27c67-120">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="27c67-121">Algunos objetos *InfoLevel* solo están disponibles en la versión sin conexión (**JetGetDatabaseFileInfo**) o en línea ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) de la API.</span><span class="sxs-lookup"><span data-stu-id="27c67-121">Some *InfoLevel* objects are available only in the offline (**JetGetDatabaseFileInfo**) or online ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) version of the API.</span></span>

<span data-ttu-id="27c67-122">Si el búfer de *pvResult* proporcionado es demasiado pequeño, se devolverá JET_errInvalidBufferSize o JET_errBufferTooSmall, en función de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="27c67-122">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned, depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27c67-123">Value</span><span class="sxs-lookup"><span data-stu-id="27c67-123">Value</span></span></p></th>
<th><p><span data-ttu-id="27c67-124">Significado</span><span class="sxs-lookup"><span data-stu-id="27c67-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27c67-125">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="27c67-125">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="27c67-126"><em>pvResult</em> se interpretará como QWord (8 bytes).</span><span class="sxs-lookup"><span data-stu-id="27c67-126"><em>pvResult</em> will be interpreted as a QWORD (8 bytes).</span></span> <span data-ttu-id="27c67-127">Devuelve el tamaño de la base de datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="27c67-127">Returns the size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c67-128">JET_DbInfoUpgrade</span><span class="sxs-lookup"><span data-stu-id="27c67-128">JET_DbInfoUpgrade</span></span></p></td>
<td><p><span data-ttu-id="27c67-129"><em>pvResult</em> se interpretará como un <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>.</span><span class="sxs-lookup"><span data-stu-id="27c67-129"><em>pvResult</em> will be interpreted as a <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>.</span></span> <span data-ttu-id="27c67-130">La estructura de <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> se rellenará con información relativa a la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="27c67-130">The <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27c67-131">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="27c67-131">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="27c67-132"><em>pvResult</em> se interpretará como un <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span><span class="sxs-lookup"><span data-stu-id="27c67-132"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="27c67-133">La estructura de <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> se rellenará con información relativa a la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="27c67-133">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c67-134">JET_DbInfoDBInUse</span><span class="sxs-lookup"><span data-stu-id="27c67-134">JET_DbInfoDBInUse</span></span></p></td>
<td><p><span data-ttu-id="27c67-135"><em>pvResult</em> se interpretará como un booleano (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="27c67-135"><em>pvResult</em> will be interpreted as a BOOL (4 bytes).</span></span> <span data-ttu-id="27c67-136">Esto devolverá si el motor de base de datos tiene actualmente cualquier base de datos abierta o adjunta.</span><span class="sxs-lookup"><span data-stu-id="27c67-136">This will return whether the database engine currently has any open or attached databases.</span></span></p>
<p><span data-ttu-id="27c67-137"><strong>Windows XP:  </strong> Este valor se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="27c67-137"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27c67-138">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="27c67-138">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="27c67-139"><em>pvResult</em> se interpretará como una longitud sin signo.</span><span class="sxs-lookup"><span data-stu-id="27c67-139"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="27c67-140">Esto devolverá el tamaño de página de la base de datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="27c67-140">This will return the page size of the database in bytes.</span></span></p>
<p><span data-ttu-id="27c67-141"><strong>Windows XP:  </strong> Este valor se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="27c67-141"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c67-142">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="27c67-142">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="27c67-143">Estos <em>InfoLevels</em> aún no se admiten y devuelven valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="27c67-143">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="27c67-144">No use estos <em>InfoLevels</em>.</span><span class="sxs-lookup"><span data-stu-id="27c67-144">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27c67-145">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="27c67-145">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="27c67-146">Estos <em>InfoLevels</em> aún no se admiten y devuelven valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="27c67-146">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="27c67-147">No use estos <em>InfoLevels</em>.</span><span class="sxs-lookup"><span data-stu-id="27c67-147">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c67-148">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="27c67-148">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="27c67-149">Igual que JET_DbInfoCp.</span><span class="sxs-lookup"><span data-stu-id="27c67-149">Same as JET_DbInfoCp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27c67-150">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="27c67-150">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="27c67-151">Estos <em>InfoLevels</em> están desusados y no se admiten actualmente.</span><span class="sxs-lookup"><span data-stu-id="27c67-151">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="27c67-152">No use estos <em>InfoLevels</em>.</span><span class="sxs-lookup"><span data-stu-id="27c67-152">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c67-153">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="27c67-153">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="27c67-154">Igual que JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="27c67-154">Same as JET_DbInfoIsam.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27c67-155">JET_DbInfoFileType</span><span class="sxs-lookup"><span data-stu-id="27c67-155">JET_DbInfoFileType</span></span></p></td>
<td><p><span data-ttu-id="27c67-156"><strong>Windows Vista:  </strong> Este valor de <em>InfoLevel</em> se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="27c67-156"><strong>Windows Vista:  </strong>This <em>InfoLevel</em> value is introduced in Windows Vista.</span></span></p>
<p><span data-ttu-id="27c67-157"><em>pvResult</em> se tratará como un puntero a un valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="27c67-157"><em>pvResult</em> will be treated as a pointer to a DWORD.</span></span> <span data-ttu-id="27c67-158">Devuelve un valor de enumeración, que indica el tipo de archivo que el motor considera que es.</span><span class="sxs-lookup"><span data-stu-id="27c67-158">Returns an enumeration value, indicating what kind of file the engine considers this to be.</span></span> <span data-ttu-id="27c67-159">Los tipos de archivo se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="27c67-159">File types are listed in the following table.</span></span> <span data-ttu-id="27c67-160">Para obtener más información sobre estos tipos de archivos y su uso en el motor de, consulte <a href="gg294069(v=exchg.10).md">archivos del motor de almacenamiento extensible</a>.</span><span class="sxs-lookup"><span data-stu-id="27c67-160">For more information about these types of files and their usage to the engine, see <a href="gg294069(v=exchg.10).md">Extensible Storage Engine Files</a>.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27c67-161">Value</span><span class="sxs-lookup"><span data-stu-id="27c67-161">Value</span></span></p></th>
<th><p><span data-ttu-id="27c67-162">Significado</span><span class="sxs-lookup"><span data-stu-id="27c67-162">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27c67-163">JET_filetypeUnknown</span><span class="sxs-lookup"><span data-stu-id="27c67-163">JET_filetypeUnknown</span></span></p></td>
<td><p><span data-ttu-id="27c67-164">El tipo de archivo es desconocido o no es un tipo de archivo ESE.</span><span class="sxs-lookup"><span data-stu-id="27c67-164">The type of file is unknown, or not an ESE file type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c67-165">JET_filetypeDatabase</span><span class="sxs-lookup"><span data-stu-id="27c67-165">JET_filetypeDatabase</span></span></p></td>
<td><p><span data-ttu-id="27c67-166">El archivo es un archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="27c67-166">The file is a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27c67-167">JET_filetypeLog</span><span class="sxs-lookup"><span data-stu-id="27c67-167">JET_filetypeLog</span></span></p></td>
<td><p><span data-ttu-id="27c67-168">El archivo es un archivo de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="27c67-168">The file is a transaction log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c67-169">JET_filetypeCheckpoint</span><span class="sxs-lookup"><span data-stu-id="27c67-169">JET_filetypeCheckpoint</span></span></p></td>
<td><p><span data-ttu-id="27c67-170">El archivo es un archivo de punto de comprobación.</span><span class="sxs-lookup"><span data-stu-id="27c67-170">The file is a checkpoint file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27c67-171">JET_filetypeTempDatabase</span><span class="sxs-lookup"><span data-stu-id="27c67-171">JET_filetypeTempDatabase</span></span></p></td>
<td><p><span data-ttu-id="27c67-172">El archivo es un archivo de base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="27c67-172">The file is a temporary database file.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="27c67-173">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27c67-173">Return Value</span></span>

<span data-ttu-id="27c67-174">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="27c67-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="27c67-175">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="27c67-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27c67-176">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="27c67-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="27c67-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="27c67-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27c67-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="27c67-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="27c67-179">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="27c67-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c67-180">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="27c67-180">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="27c67-181">La <em>InfoLevel</em> solicitada se JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="27c67-181">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="27c67-182">Esto no se admite.</span><span class="sxs-lookup"><span data-stu-id="27c67-182">This is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27c67-183">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="27c67-183">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="27c67-184">El búfer que se proporciona en <em>cbMax</em> es demasiado pequeño para la información deseada.</span><span class="sxs-lookup"><span data-stu-id="27c67-184">The buffer that is given in <em>cbMax</em> is too small for the desired information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c67-185">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="27c67-185">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="27c67-186">El búfer que se proporciona en <em>cbMax</em> no es el tamaño correcto para la información deseada.</span><span class="sxs-lookup"><span data-stu-id="27c67-186">The buffer that is given in <em>cbMax</em> is not the correct size for the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27c67-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="27c67-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="27c67-188">Uno de los parámetros que se proporcionó contenía un valor inesperado o la combinación de varios valores de parámetro produjo un resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="27c67-188">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="27c67-189"><a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> devolverá este error cuando el DBID proporcionado no sea una base de datos válida (adjunta).</span><span class="sxs-lookup"><span data-stu-id="27c67-189">This error will be returned by <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when the DBID provided is not a valid (attached) database.</span></span> <span data-ttu-id="27c67-190">Este error lo devolverá <strong>JetGetDatabaseFileInfo</strong> y <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> cuando una <em>InfoLevel</em> solicitada no sea compatible con esa versión de la función.</span><span class="sxs-lookup"><span data-stu-id="27c67-190">This error will be returned by <strong>JetGetDatabaseFileInfo</strong> and <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="27c67-191">Si esta función se ejecuta correctamente, los datos solicitados se devolverán en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="27c67-191">If this function succeeds, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="27c67-192">Si se produce un error en esta función, el búfer de salida estará en un estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="27c67-192">If this function fails, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="27c67-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27c67-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27c67-194"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="27c67-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="27c67-195">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="27c67-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c67-196"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="27c67-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="27c67-197">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="27c67-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27c67-198"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="27c67-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="27c67-199">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="27c67-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c67-200"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="27c67-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="27c67-201">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="27c67-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27c67-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="27c67-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="27c67-203">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="27c67-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27c67-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="27c67-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="27c67-205">Se implementa como <strong>JetGetDatabaseFileInfoW</strong> (Unicode) y <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="27c67-205">Implemented as <strong>JetGetDatabaseFileInfoW</strong> (Unicode) and <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="27c67-206">Consulte también</span><span class="sxs-lookup"><span data-stu-id="27c67-206">See Also</span></span>

[<span data-ttu-id="27c67-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="27c67-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="27c67-208">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="27c67-208">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="27c67-209">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="27c67-209">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="27c67-210">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="27c67-210">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)
