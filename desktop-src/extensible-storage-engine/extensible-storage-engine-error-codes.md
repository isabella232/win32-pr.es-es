---
description: 'Más información sobre: códigos de error del motor de almacenamiento extensible'
title: Códigos de error del motor de almacenamiento extensible
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716833"
---
# <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="431a5-103">Códigos de error del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="431a5-103">Extensible Storage Engine Error Codes</span></span>


<span data-ttu-id="431a5-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="431a5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="431a5-105">Códigos de error del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="431a5-105">Extensible Storage Engine Error Codes</span></span>

<span data-ttu-id="431a5-106">Las funciones de la API del motor de almacenamiento extensible usan los siguientes códigos de error (marcas).</span><span class="sxs-lookup"><span data-stu-id="431a5-106">The following error codes (flags) are used by functions in the Extensible Storage Engine API.</span></span>

<span data-ttu-id="431a5-107">Un valor [JET_ERR](./jet-err.md) de cero debe interpretarse como correcto.</span><span class="sxs-lookup"><span data-stu-id="431a5-107">A [JET_ERR](./jet-err.md) value of zero should be interpreted as success.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="431a5-108">Correcto</span><span class="sxs-lookup"><span data-stu-id="431a5-108">Success</span></span></p></th>
<th><p><span data-ttu-id="431a5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="431a5-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="431a5-110">JET_errSuccess 0</span><span class="sxs-lookup"><span data-stu-id="431a5-110">JET_errSuccess 0</span></span></p></td>
<td><p><span data-ttu-id="431a5-111">La función se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="431a5-111">The function succeeded.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="431a5-112">Un valor [JET_ERR](./jet-err.md) mayor que cero debe interpretarse como una advertencia.</span><span class="sxs-lookup"><span data-stu-id="431a5-112">A [JET_ERR](./jet-err.md) value that is greater than zero should be interpreted as a warning.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="431a5-113">Advertencias</span><span class="sxs-lookup"><span data-stu-id="431a5-113">Warnings</span></span></p></th>
<th><p><span data-ttu-id="431a5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="431a5-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="431a5-115">JET_wrnRemainingVersions</span><span class="sxs-lookup"><span data-stu-id="431a5-115">JET_wrnRemainingVersions</span></span><br />
<span data-ttu-id="431a5-116">321</span><span class="sxs-lookup"><span data-stu-id="431a5-116">321</span></span></p></td>
<td><p><span data-ttu-id="431a5-117">El almacén de versiones todavía está activo.</span><span class="sxs-lookup"><span data-stu-id="431a5-117">The version store is still active.</span></span> <span data-ttu-id="431a5-118">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-118">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-119">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="431a5-119">JET_wrnUniqueKey</span></span><br />
<span data-ttu-id="431a5-120">345</span><span class="sxs-lookup"><span data-stu-id="431a5-120">345</span></span></p></td>
<td><p><span data-ttu-id="431a5-121">Una búsqueda en un índice no único produjo una clave única.</span><span class="sxs-lookup"><span data-stu-id="431a5-121">A seek on a non-unique index yielded a unique key.</span></span> <span data-ttu-id="431a5-122">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-122">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-123">JET_wrnSeparateLongValue</span><span class="sxs-lookup"><span data-stu-id="431a5-123">JET_wrnSeparateLongValue</span></span><br />
<span data-ttu-id="431a5-124">406</span><span class="sxs-lookup"><span data-stu-id="431a5-124">406</span></span></p></td>
<td><p><span data-ttu-id="431a5-125">Una columna de base de datos es un valor largo separado.</span><span class="sxs-lookup"><span data-stu-id="431a5-125">A database column is a separated long value.</span></span> <span data-ttu-id="431a5-126">Este error lo devuelve el administrador de registros.</span><span class="sxs-lookup"><span data-stu-id="431a5-126">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-127">JET_wrnExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="431a5-127">JET_wrnExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="431a5-128">558</span><span class="sxs-lookup"><span data-stu-id="431a5-128">558</span></span></p></td>
<td><p><span data-ttu-id="431a5-129">El archivo de registro existente tiene una firma incorrecta.</span><span class="sxs-lookup"><span data-stu-id="431a5-129">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-130">JET_wrnExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="431a5-130">JET_wrnExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="431a5-131">559</span><span class="sxs-lookup"><span data-stu-id="431a5-131">559</span></span></p></td>
<td><p><span data-ttu-id="431a5-132">El archivo de registro existente no es contiguo.</span><span class="sxs-lookup"><span data-stu-id="431a5-132">The existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-133">JET_wrnSkipThisRecord</span><span class="sxs-lookup"><span data-stu-id="431a5-133">JET_wrnSkipThisRecord</span></span><br />
<span data-ttu-id="431a5-134">564</span><span class="sxs-lookup"><span data-stu-id="431a5-134">564</span></span></p></td>
<td><p><span data-ttu-id="431a5-135">Este error solo es para uso interno.</span><span class="sxs-lookup"><span data-stu-id="431a5-135">This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-136">JET_wrnTargetInstanceRunning</span><span class="sxs-lookup"><span data-stu-id="431a5-136">JET_wrnTargetInstanceRunning</span></span><br />
<span data-ttu-id="431a5-137">578</span><span class="sxs-lookup"><span data-stu-id="431a5-137">578</span></span></p></td>
<td><p><span data-ttu-id="431a5-138">Se está ejecutando el TargetInstance especificado para la restauración.</span><span class="sxs-lookup"><span data-stu-id="431a5-138">The TargetInstance specified for the restore is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-139">JET_wrnDatabaseRepaired</span><span class="sxs-lookup"><span data-stu-id="431a5-139">JET_wrnDatabaseRepaired</span></span><br />
<span data-ttu-id="431a5-140">595</span><span class="sxs-lookup"><span data-stu-id="431a5-140">595</span></span></p></td>
<td><p><span data-ttu-id="431a5-141">Se han reparado los daños en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-141">The database corruption has been repaired.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-142">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="431a5-142">JET_wrnColumnNull</span></span><br />
<span data-ttu-id="431a5-143">1004</span><span class="sxs-lookup"><span data-stu-id="431a5-143">1004</span></span></p></td>
<td><p><span data-ttu-id="431a5-144">La columna tiene un valor <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="431a5-144">The column has a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-145">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="431a5-145">JET_wrnBufferTruncated</span></span><br />
<span data-ttu-id="431a5-146">1006</span><span class="sxs-lookup"><span data-stu-id="431a5-146">1006</span></span></p></td>
<td><p><span data-ttu-id="431a5-147">El búfer es demasiado pequeño para los datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-147">The buffer is too small for the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-148">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="431a5-148">JET_wrnDatabaseAttached</span></span><br />
<span data-ttu-id="431a5-149">1007</span><span class="sxs-lookup"><span data-stu-id="431a5-149">1007</span></span></p></td>
<td><p><span data-ttu-id="431a5-150">La base de datos ya está adjunta.</span><span class="sxs-lookup"><span data-stu-id="431a5-150">The database is already attached.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-151">JET_wrnSortOverflow</span><span class="sxs-lookup"><span data-stu-id="431a5-151">JET_wrnSortOverflow</span></span><br />
<span data-ttu-id="431a5-152">1009</span><span class="sxs-lookup"><span data-stu-id="431a5-152">1009</span></span></p></td>
<td><p><span data-ttu-id="431a5-153">La ordenación que se está intentando no tiene suficiente memoria para completarse.</span><span class="sxs-lookup"><span data-stu-id="431a5-153">The sort that is being attempted does not have enough memory to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-154">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="431a5-154">JET_wrnSeekNotEqual</span></span><br />
<span data-ttu-id="431a5-155">1039</span><span class="sxs-lookup"><span data-stu-id="431a5-155">1039</span></span></p></td>
<td><p><span data-ttu-id="431a5-156">No se encontró una coincidencia exacta durante una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="431a5-156">An exact match was not found during a seek.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-157">JET_wrnRecordFoundGreater</span><span class="sxs-lookup"><span data-stu-id="431a5-157">JET_wrnRecordFoundGreater</span></span><br />
<span data-ttu-id="431a5-158">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="431a5-158">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="431a5-159">No se encontró una coincidencia exacta durante una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="431a5-159">An exact match was not found during a seek.</span></span> <span data-ttu-id="431a5-160">Este error lo devuelve el administrador de registros.</span><span class="sxs-lookup"><span data-stu-id="431a5-160">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-161">JET_wrnRecordFoundLess</span><span class="sxs-lookup"><span data-stu-id="431a5-161">JET_wrnRecordFoundLess</span></span><br />
<span data-ttu-id="431a5-162">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="431a5-162">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="431a5-163">No se encontró una coincidencia exacta durante una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="431a5-163">An exact match was not found during a seek.</span></span> <span data-ttu-id="431a5-164">Este error lo devuelve el administrador de registros.</span><span class="sxs-lookup"><span data-stu-id="431a5-164">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-165">JET_wrnNoErrorInfo</span><span class="sxs-lookup"><span data-stu-id="431a5-165">JET_wrnNoErrorInfo</span></span><br />
<span data-ttu-id="431a5-166">1055</span><span class="sxs-lookup"><span data-stu-id="431a5-166">1055</span></span></p></td>
<td><p><span data-ttu-id="431a5-167">No hay información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="431a5-167">There is no extended error information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-168">JET_wrnNoIdleActivity</span><span class="sxs-lookup"><span data-stu-id="431a5-168">JET_wrnNoIdleActivity</span></span><br />
<span data-ttu-id="431a5-169">1058</span><span class="sxs-lookup"><span data-stu-id="431a5-169">1058</span></span></p></td>
<td><p><span data-ttu-id="431a5-170">No se ha producido ninguna actividad inactiva.</span><span class="sxs-lookup"><span data-stu-id="431a5-170">No idle activity occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-171">JET_wrnNoWriteLock</span><span class="sxs-lookup"><span data-stu-id="431a5-171">JET_wrnNoWriteLock</span></span><br />
<span data-ttu-id="431a5-172">1067</span><span class="sxs-lookup"><span data-stu-id="431a5-172">1067</span></span></p></td>
<td><p><span data-ttu-id="431a5-173">No hay ningún bloqueo de escritura en el nivel de transacción 0.</span><span class="sxs-lookup"><span data-stu-id="431a5-173">There is a no write lock at transaction level 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-174">JET_wrnColumnSetNull</span><span class="sxs-lookup"><span data-stu-id="431a5-174">JET_wrnColumnSetNull</span></span><br />
<span data-ttu-id="431a5-175">1068</span><span class="sxs-lookup"><span data-stu-id="431a5-175">1068</span></span></p></td>
<td><p><span data-ttu-id="431a5-176">La columna se establece en un valor <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="431a5-176">The column is set to a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-177">JET_wrnTableEmpty</span><span class="sxs-lookup"><span data-stu-id="431a5-177">JET_wrnTableEmpty</span></span><br />
<span data-ttu-id="431a5-178">1301</span><span class="sxs-lookup"><span data-stu-id="431a5-178">1301</span></span></p></td>
<td><p><span data-ttu-id="431a5-179">Se abrió una tabla vacía.</span><span class="sxs-lookup"><span data-stu-id="431a5-179">An empty table was opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-180">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="431a5-180">JET_wrnTableInUseBySystem</span></span><br />
<span data-ttu-id="431a5-181">1327</span><span class="sxs-lookup"><span data-stu-id="431a5-181">1327</span></span></p></td>
<td><p><span data-ttu-id="431a5-182">La limpieza del sistema tiene un cursor abierto en la tabla.</span><span class="sxs-lookup"><span data-stu-id="431a5-182">The system cleanup has a cursor open on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-183">JET_wrnCorruptIndexDeleted</span><span class="sxs-lookup"><span data-stu-id="431a5-183">JET_wrnCorruptIndexDeleted</span></span><br />
<span data-ttu-id="431a5-184">1415</span><span class="sxs-lookup"><span data-stu-id="431a5-184">1415</span></span></p></td>
<td><p><span data-ttu-id="431a5-185">Se debe quitar el índice no actualizado.</span><span class="sxs-lookup"><span data-stu-id="431a5-185">The out-of-date index must be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-186">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="431a5-186">JET_wrnColumnMaxTruncated</span></span><br />
<span data-ttu-id="431a5-187">1512</span><span class="sxs-lookup"><span data-stu-id="431a5-187">1512</span></span></p></td>
<td><p><span data-ttu-id="431a5-188">La longitud máxima es demasiado grande y se ha truncado.</span><span class="sxs-lookup"><span data-stu-id="431a5-188">The Max length is too large and has been truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-189">JET_wrnCopyLongValue</span><span class="sxs-lookup"><span data-stu-id="431a5-189">JET_wrnCopyLongValue</span></span><br />
<span data-ttu-id="431a5-190">1520</span><span class="sxs-lookup"><span data-stu-id="431a5-190">1520</span></span></p></td>
<td><p><span data-ttu-id="431a5-191">Un valor de BLOB se ha pasado del registro a un almacenamiento independiente de blobs grandes.</span><span class="sxs-lookup"><span data-stu-id="431a5-191">A BLOB value has been moved from the record into a separate storage of large BLOBs.</span></span></p>
<p><span data-ttu-id="431a5-192"><strong>Nota:</strong> Este error solo es para uso interno.</span><span class="sxs-lookup"><span data-stu-id="431a5-192"><strong>Note</strong> This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-193">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="431a5-193">JET_wrnColumnSkipped</span></span><br />
<span data-ttu-id="431a5-194">1531</span><span class="sxs-lookup"><span data-stu-id="431a5-194">1531</span></span></p></td>
<td><p><span data-ttu-id="431a5-195">No se devolvieron los valores de columna porque el ID. de columna correspondiente o el miembro <em>itagSequence</em> de la estructura <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> que se solicitó para la enumeración era null.</span><span class="sxs-lookup"><span data-stu-id="431a5-195">The column values were not returned because the corresponding column ID or <em>itagSequence</em> member from the <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> structure that was requested for enumeration was null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-196">JET_wrnColumnNotLocal</span><span class="sxs-lookup"><span data-stu-id="431a5-196">JET_wrnColumnNotLocal</span></span><br />
<span data-ttu-id="431a5-197">1532</span><span class="sxs-lookup"><span data-stu-id="431a5-197">1532</span></span></p></td>
<td><p><span data-ttu-id="431a5-198">No se devolvieron los valores de columna porque no se pudieron reconstruir a partir de los datos existentes.</span><span class="sxs-lookup"><span data-stu-id="431a5-198">The column values were not returned because they could not be reconstructed from the existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-199">JET_wrnColumnMoreTags</span><span class="sxs-lookup"><span data-stu-id="431a5-199">JET_wrnColumnMoreTags</span></span><br />
<span data-ttu-id="431a5-200">1533</span><span class="sxs-lookup"><span data-stu-id="431a5-200">1533</span></span></p></td>
<td><p><span data-ttu-id="431a5-201">No se solicitaron los valores de columna existentes para la enumeración.</span><span class="sxs-lookup"><span data-stu-id="431a5-201">The existing column values were not requested for enumeration.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-202">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="431a5-202">JET_wrnColumnTruncated</span></span><br />
<span data-ttu-id="431a5-203">1534</span><span class="sxs-lookup"><span data-stu-id="431a5-203">1534</span></span></p></td>
<td><p><span data-ttu-id="431a5-204">El valor de la columna se truncó en el límite de tamaño solicitado durante la enumeración.</span><span class="sxs-lookup"><span data-stu-id="431a5-204">The column value was truncated at the requested size limit during enumeration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-205">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="431a5-205">JET_wrnColumnPresent</span></span><br />
<span data-ttu-id="431a5-206">1535</span><span class="sxs-lookup"><span data-stu-id="431a5-206">1535</span></span></p></td>
<td><p><span data-ttu-id="431a5-207">Los valores de columna existen pero no fueron devueltos por la solicitud.</span><span class="sxs-lookup"><span data-stu-id="431a5-207">The column values exist but were not returned by the request.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-208">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="431a5-208">JET_wrnColumnSingleValue</span></span><br />
<span data-ttu-id="431a5-209">1536</span><span class="sxs-lookup"><span data-stu-id="431a5-209">1536</span></span></p></td>
<td><p><span data-ttu-id="431a5-210">El valor de la columna se devolvió en JET_COLUMNENUM como resultado de la JET_bitEnumerateCompressOutput que se establece.</span><span class="sxs-lookup"><span data-stu-id="431a5-210">The column value was returned in JET_COLUMNENUM as a result of the JET_bitEnumerateCompressOutput being set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-211">JET_wrnColumnDefault</span><span class="sxs-lookup"><span data-stu-id="431a5-211">JET_wrnColumnDefault</span></span><br />
<span data-ttu-id="431a5-212">1537</span><span class="sxs-lookup"><span data-stu-id="431a5-212">1537</span></span></p></td>
<td><p><span data-ttu-id="431a5-213">El valor de la columna se establece en el valor predeterminado de la columna.</span><span class="sxs-lookup"><span data-stu-id="431a5-213">The column value is set to the default value of the column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-214">JET_wrnDataHasChanged</span><span class="sxs-lookup"><span data-stu-id="431a5-214">JET_wrnDataHasChanged</span></span><br />
<span data-ttu-id="431a5-215">1610</span><span class="sxs-lookup"><span data-stu-id="431a5-215">1610</span></span></p></td>
<td><p><span data-ttu-id="431a5-216">Los datos han cambiado.</span><span class="sxs-lookup"><span data-stu-id="431a5-216">The data has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-217">JET_wrnKeyChanged</span><span class="sxs-lookup"><span data-stu-id="431a5-217">JET_wrnKeyChanged</span></span><br />
<span data-ttu-id="431a5-218">1618</span><span class="sxs-lookup"><span data-stu-id="431a5-218">1618</span></span></p></td>
<td><p><span data-ttu-id="431a5-219">Se está usando una nueva clave.</span><span class="sxs-lookup"><span data-stu-id="431a5-219">A new key is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-220">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="431a5-220">JET_wrnFileOpenReadOnly</span></span><br />
<span data-ttu-id="431a5-221">1813</span><span class="sxs-lookup"><span data-stu-id="431a5-221">1813</span></span></p></td>
<td><p><span data-ttu-id="431a5-222">El archivo de base de datos es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="431a5-222">The database file is read only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-223">JET_wrnIdleFull</span><span class="sxs-lookup"><span data-stu-id="431a5-223">JET_wrnIdleFull</span></span><br />
<span data-ttu-id="431a5-224">1908</span><span class="sxs-lookup"><span data-stu-id="431a5-224">1908</span></span></p></td>
<td><p><span data-ttu-id="431a5-225">El registro inactivo está lleno.</span><span class="sxs-lookup"><span data-stu-id="431a5-225">The idle registry is full.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-226">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="431a5-226">JET_wrnDefragAlreadyRunning</span></span><br />
<span data-ttu-id="431a5-227">2000</span><span class="sxs-lookup"><span data-stu-id="431a5-227">2000</span></span></p></td>
<td><p><span data-ttu-id="431a5-228">Había una desfragmentación con conexión que ya se estaba ejecutando en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="431a5-228">There was an online defragmentation already running on the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-229">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="431a5-229">JET_wrnDefragNotRunning</span></span><br />
<span data-ttu-id="431a5-230">2001</span><span class="sxs-lookup"><span data-stu-id="431a5-230">2001</span></span></p></td>
<td><p><span data-ttu-id="431a5-231">No se está ejecutando una desfragmentación con conexión en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="431a5-231">An online defragmentation is not running on the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-232">JET_wrnCallbackNotRegistered</span><span class="sxs-lookup"><span data-stu-id="431a5-232">JET_wrnCallbackNotRegistered</span></span><br />
<span data-ttu-id="431a5-233">2100</span><span class="sxs-lookup"><span data-stu-id="431a5-233">2100</span></span></p></td>
<td><p><span data-ttu-id="431a5-234">Se anuló el registro de una función de devolución de llamada que no existe.</span><span class="sxs-lookup"><span data-stu-id="431a5-234">A non-existent callback function was unregistered.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="431a5-235">Un valor de [JET_ERR](./jet-err.md) que sea menor que cero debe interpretarse como un error.</span><span class="sxs-lookup"><span data-stu-id="431a5-235">A [JET_ERR](./jet-err.md) value that is less than zero should be interpreted as an error.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="431a5-236">Errors</span><span class="sxs-lookup"><span data-stu-id="431a5-236">Errors</span></span></p></th>
<th><p><span data-ttu-id="431a5-237">Descripción</span><span class="sxs-lookup"><span data-stu-id="431a5-237">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="431a5-238">JET_wrnNyi</span><span class="sxs-lookup"><span data-stu-id="431a5-238">JET_wrnNyi</span></span><br />
<span data-ttu-id="431a5-239">-1</span><span class="sxs-lookup"><span data-stu-id="431a5-239">-1</span></span></p></td>
<td><p><span data-ttu-id="431a5-240">La función aún no está implementada.</span><span class="sxs-lookup"><span data-stu-id="431a5-240">The function is not yet implemented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-241">JET_errRfsFailure</span><span class="sxs-lookup"><span data-stu-id="431a5-241">JET_errRfsFailure</span></span><br />
<span data-ttu-id="431a5-242">-100</span><span class="sxs-lookup"><span data-stu-id="431a5-242">-100</span></span></p></td>
<td><p><span data-ttu-id="431a5-243">Error del simulador de errores de recursos.</span><span class="sxs-lookup"><span data-stu-id="431a5-243">The Resource Failure Simulator failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-244">JET_errRfsNotArmed</span><span class="sxs-lookup"><span data-stu-id="431a5-244">JET_errRfsNotArmed</span></span><br />
<span data-ttu-id="431a5-245">-101</span><span class="sxs-lookup"><span data-stu-id="431a5-245">-101</span></span></p></td>
<td><p><span data-ttu-id="431a5-246">No se ha inicializado el simulador de errores de recursos.</span><span class="sxs-lookup"><span data-stu-id="431a5-246">The Resource Failure Simulator has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-247">JET_errFileClose</span><span class="sxs-lookup"><span data-stu-id="431a5-247">JET_errFileClose</span></span><br />
<span data-ttu-id="431a5-248">-102</span><span class="sxs-lookup"><span data-stu-id="431a5-248">-102</span></span></p></td>
<td><p><span data-ttu-id="431a5-249">No se pudo cerrar el archivo.</span><span class="sxs-lookup"><span data-stu-id="431a5-249">The file could not be closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-250">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="431a5-250">JET_errOutOfThreads</span></span><br />
<span data-ttu-id="431a5-251">-103</span><span class="sxs-lookup"><span data-stu-id="431a5-251">-103</span></span></p></td>
<td><p><span data-ttu-id="431a5-252">No se pudo iniciar el subproceso.</span><span class="sxs-lookup"><span data-stu-id="431a5-252">The thread could not be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-253">JET_errTooManyIO</span><span class="sxs-lookup"><span data-stu-id="431a5-253">JET_errTooManyIO</span></span><br />
<span data-ttu-id="431a5-254">-105</span><span class="sxs-lookup"><span data-stu-id="431a5-254">-105</span></span></p></td>
<td><p><span data-ttu-id="431a5-255">El sistema está ocupado debido a que hay demasiadas e/s.</span><span class="sxs-lookup"><span data-stu-id="431a5-255">The system is busy due to too many IOs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-256">JET_errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="431a5-256">JET_errTaskDropped</span></span><br />
<span data-ttu-id="431a5-257">-106</span><span class="sxs-lookup"><span data-stu-id="431a5-257">-106</span></span></p></td>
<td><p><span data-ttu-id="431a5-258">No se pudo ejecutar la tarea asincrónica solicitada.</span><span class="sxs-lookup"><span data-stu-id="431a5-258">The requested asynchronous task could not be executed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-259">JET_errInternalError</span><span class="sxs-lookup"><span data-stu-id="431a5-259">JET_errInternalError</span></span><br />
<span data-ttu-id="431a5-260">-107</span><span class="sxs-lookup"><span data-stu-id="431a5-260">-107</span></span></p></td>
<td><p><span data-ttu-id="431a5-261">Se produjo un error interno grave.</span><span class="sxs-lookup"><span data-stu-id="431a5-261">There was a fatal internal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-262">JET_errDatabaseBufferDependenciesCorrupted</span><span class="sxs-lookup"><span data-stu-id="431a5-262">JET_errDatabaseBufferDependenciesCorrupted</span></span><br />
<span data-ttu-id="431a5-263">-255</span><span class="sxs-lookup"><span data-stu-id="431a5-263">-255</span></span></p></td>
<td><p><span data-ttu-id="431a5-264">Las dependencias del búfer se establecieron incorrectamente y se produjo un error de recuperación.</span><span class="sxs-lookup"><span data-stu-id="431a5-264">The buffer dependencies were set improperly and there was a recovery failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-265">JET_errPreviousVersion</span><span class="sxs-lookup"><span data-stu-id="431a5-265">JET_errPreviousVersion</span></span><br />
<span data-ttu-id="431a5-266">-322</span><span class="sxs-lookup"><span data-stu-id="431a5-266">-322</span></span></p></td>
<td><p><span data-ttu-id="431a5-267">La versión ya existía y se produjo un error de recuperación.</span><span class="sxs-lookup"><span data-stu-id="431a5-267">The version already existed and there was a recovery failure.</span></span> <span data-ttu-id="431a5-268">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-268">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-269">JET_errPageBoundary</span><span class="sxs-lookup"><span data-stu-id="431a5-269">JET_errPageBoundary</span></span><br />
<span data-ttu-id="431a5-270">-323</span><span class="sxs-lookup"><span data-stu-id="431a5-270">-323</span></span></p></td>
<td><p><span data-ttu-id="431a5-271">Se ha alcanzado el límite de la página.</span><span class="sxs-lookup"><span data-stu-id="431a5-271">The page boundary has been reached.</span></span> <span data-ttu-id="431a5-272">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-272">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-273">JET_errKeyBoundary</span><span class="sxs-lookup"><span data-stu-id="431a5-273">JET_errKeyBoundary</span></span><br />
<span data-ttu-id="431a5-274">-324</span><span class="sxs-lookup"><span data-stu-id="431a5-274">-324</span></span></p></td>
<td><p><span data-ttu-id="431a5-275">Se ha alcanzado el límite de la clave.</span><span class="sxs-lookup"><span data-stu-id="431a5-275">The key boundary has been reached.</span></span> <span data-ttu-id="431a5-276">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-276">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-277">JET_errBadPageLink</span><span class="sxs-lookup"><span data-stu-id="431a5-277">JET_errBadPageLink</span></span><br />
<span data-ttu-id="431a5-278">-327</span><span class="sxs-lookup"><span data-stu-id="431a5-278">-327</span></span></p></td>
<td><p><span data-ttu-id="431a5-279">La base de datos está dañada.</span><span class="sxs-lookup"><span data-stu-id="431a5-279">The database is corrupt.</span></span> <span data-ttu-id="431a5-280">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-280">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-281">JET_errBadBookmark</span><span class="sxs-lookup"><span data-stu-id="431a5-281">JET_errBadBookmark</span></span><br />
<span data-ttu-id="431a5-282">-328</span><span class="sxs-lookup"><span data-stu-id="431a5-282">-328</span></span></p></td>
<td><p><span data-ttu-id="431a5-283">El marcador no tiene ninguna dirección correspondiente en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-283">The bookmark has no corresponding address in the database.</span></span> <span data-ttu-id="431a5-284">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-284">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-285">JET_errNTSystemCallFailed</span><span class="sxs-lookup"><span data-stu-id="431a5-285">JET_errNTSystemCallFailed</span></span><br />
<span data-ttu-id="431a5-286">-334</span><span class="sxs-lookup"><span data-stu-id="431a5-286">-334</span></span></p></td>
<td><p><span data-ttu-id="431a5-287">Error en la llamada al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="431a5-287">The call to the operating system failed.</span></span> <span data-ttu-id="431a5-288">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-288">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-289">JET_errBadParentPageLink</span><span class="sxs-lookup"><span data-stu-id="431a5-289">JET_errBadParentPageLink</span></span><br />
<span data-ttu-id="431a5-290">-338</span><span class="sxs-lookup"><span data-stu-id="431a5-290">-338</span></span></p></td>
<td><p><span data-ttu-id="431a5-291">Una base de datos primaria está dañada.</span><span class="sxs-lookup"><span data-stu-id="431a5-291">A parent database is corrupt.</span></span> <span data-ttu-id="431a5-292">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-292">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-293">JET_errSPAvailExtCacheOutOfSync</span><span class="sxs-lookup"><span data-stu-id="431a5-293">JET_errSPAvailExtCacheOutOfSync</span></span><br />
<span data-ttu-id="431a5-294">-340</span><span class="sxs-lookup"><span data-stu-id="431a5-294">-340</span></span></p></td>
<td><p><span data-ttu-id="431a5-295">La memoria caché de AvailExt no coincide con el árbol B +.</span><span class="sxs-lookup"><span data-stu-id="431a5-295">The AvailExt cache does not match the B+ tree.</span></span> <span data-ttu-id="431a5-296">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-296">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-297">JET_errSPAvailExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="431a5-297">JET_errSPAvailExtCorrupted</span></span><br />
<span data-ttu-id="431a5-298">-341</span><span class="sxs-lookup"><span data-stu-id="431a5-298">-341</span></span></p></td>
<td><p><span data-ttu-id="431a5-299">El árbol de espacio AllAvailExt está dañado.</span><span class="sxs-lookup"><span data-stu-id="431a5-299">The AllAvailExt space tree is corrupt.</span></span> <span data-ttu-id="431a5-300">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-300">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-301">JET_errSPAvailExtCacheOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="431a5-301">JET_errSPAvailExtCacheOutOfMemory</span></span><br />
<span data-ttu-id="431a5-302">-342</span><span class="sxs-lookup"><span data-stu-id="431a5-302">-342</span></span></p></td>
<td><p><span data-ttu-id="431a5-303">Se produjo un error de memoria insuficiente al asignar un nodo de caché de AvailExt.</span><span class="sxs-lookup"><span data-stu-id="431a5-303">An out of memory error occurred while allocating an AvailExt cache node.</span></span> <span data-ttu-id="431a5-304">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-304">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-305">JET_errSPOwnExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="431a5-305">JET_errSPOwnExtCorrupted</span></span><br />
<span data-ttu-id="431a5-306">-343</span><span class="sxs-lookup"><span data-stu-id="431a5-306">-343</span></span></p></td>
<td><p><span data-ttu-id="431a5-307">El árbol de espacio OwnExt está dañado.</span><span class="sxs-lookup"><span data-stu-id="431a5-307">The OwnExt space tree is corrupt.</span></span> <span data-ttu-id="431a5-308">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-308">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-309">JET_errDbTimeCorrupted</span><span class="sxs-lookup"><span data-stu-id="431a5-309">JET_errDbTimeCorrupted</span></span><br />
<span data-ttu-id="431a5-310">-344</span><span class="sxs-lookup"><span data-stu-id="431a5-310">-344</span></span></p></td>
<td><p><span data-ttu-id="431a5-311">El dbTime de la página actual es mayor que el de la base de datos global dbTime.</span><span class="sxs-lookup"><span data-stu-id="431a5-311">The Dbtime on the current page is greater than the global database dbtime.</span></span> <span data-ttu-id="431a5-312">Este error lo devuelve el administrador de directorios.</span><span class="sxs-lookup"><span data-stu-id="431a5-312">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-313">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="431a5-313">JET_errKeyTruncated</span></span><br />
<span data-ttu-id="431a5-314">-346</span><span class="sxs-lookup"><span data-stu-id="431a5-314">-346</span></span></p></td>
<td><p><span data-ttu-id="431a5-315">Error al tratar de crear una clave para una entrada de índice porque la clave se habría truncado y la definición del índice no permite el truncamiento de claves.</span><span class="sxs-lookup"><span data-stu-id="431a5-315">An attempt to create a key for an index entry failed because the key would have been truncated and the index definition disallows key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-316">JET_errKeyTooBig</span><span class="sxs-lookup"><span data-stu-id="431a5-316">JET_errKeyTooBig</span></span><br />
<span data-ttu-id="431a5-317">-408</span><span class="sxs-lookup"><span data-stu-id="431a5-317">-408</span></span></p></td>
<td><p><span data-ttu-id="431a5-318">La clave es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="431a5-318">The key is too large.</span></span> <span data-ttu-id="431a5-319">Este error lo devuelve el administrador de registros.</span><span class="sxs-lookup"><span data-stu-id="431a5-319">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-320">JET_errInvalidLoggedOperation</span><span class="sxs-lookup"><span data-stu-id="431a5-320">JET_errInvalidLoggedOperation</span></span><br />
<span data-ttu-id="431a5-321">-500</span><span class="sxs-lookup"><span data-stu-id="431a5-321">-500</span></span></p></td>
<td><p><span data-ttu-id="431a5-322">No se puede rehacer la operación registrada.</span><span class="sxs-lookup"><span data-stu-id="431a5-322">The logged operation cannot be redone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-323">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="431a5-323">JET_errLogFileCorrupt</span></span><br />
<span data-ttu-id="431a5-324">-501</span><span class="sxs-lookup"><span data-stu-id="431a5-324">-501</span></span></p></td>
<td><p><span data-ttu-id="431a5-325">El archivo de registro está dañado.</span><span class="sxs-lookup"><span data-stu-id="431a5-325">The log file is corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-326">JET_errNoBackupDirectory</span><span class="sxs-lookup"><span data-stu-id="431a5-326">JET_errNoBackupDirectory</span></span><br />
<span data-ttu-id="431a5-327">-503</span><span class="sxs-lookup"><span data-stu-id="431a5-327">-503</span></span></p></td>
<td><p><span data-ttu-id="431a5-328">No se proporcionó un directorio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="431a5-328">A backup directory was not given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-329">JET_errBackupDirectoryNotEmpty</span><span class="sxs-lookup"><span data-stu-id="431a5-329">JET_errBackupDirectoryNotEmpty</span></span><br />
<span data-ttu-id="431a5-330">-504</span><span class="sxs-lookup"><span data-stu-id="431a5-330">-504</span></span></p></td>
<td><p><span data-ttu-id="431a5-331">El directorio de copia de seguridad no está vacío.</span><span class="sxs-lookup"><span data-stu-id="431a5-331">The backup directory is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-332">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="431a5-332">JET_errBackupInProgress</span></span><br />
<span data-ttu-id="431a5-333">-505</span><span class="sxs-lookup"><span data-stu-id="431a5-333">-505</span></span></p></td>
<td><p><span data-ttu-id="431a5-334">La copia de seguridad ya está activa.</span><span class="sxs-lookup"><span data-stu-id="431a5-334">The backup is active already.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-335">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="431a5-335">JET_errRestoreInProgress</span></span><br />
<span data-ttu-id="431a5-336">-506</span><span class="sxs-lookup"><span data-stu-id="431a5-336">-506</span></span></p></td>
<td><p><span data-ttu-id="431a5-337">Una restauración está en curso.</span><span class="sxs-lookup"><span data-stu-id="431a5-337">A restore is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-338">JET_errMissingPreviousLogFile</span><span class="sxs-lookup"><span data-stu-id="431a5-338">JET_errMissingPreviousLogFile</span></span><br />
<span data-ttu-id="431a5-339">-509</span><span class="sxs-lookup"><span data-stu-id="431a5-339">-509</span></span></p></td>
<td><p><span data-ttu-id="431a5-340">Falta el archivo de registro para el punto de comprobación.</span><span class="sxs-lookup"><span data-stu-id="431a5-340">The log file is missing for the check point.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-341">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="431a5-341">JET_errLogWriteFail</span></span><br />
<span data-ttu-id="431a5-342">-510</span><span class="sxs-lookup"><span data-stu-id="431a5-342">-510</span></span></p></td>
<td><p><span data-ttu-id="431a5-343">Error al escribir en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="431a5-343">There was a failure writing to the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-344">JET_errLogDisabledDueToRecoveryFailure</span><span class="sxs-lookup"><span data-stu-id="431a5-344">JET_errLogDisabledDueToRecoveryFailure</span></span><br />
<span data-ttu-id="431a5-345">-511</span><span class="sxs-lookup"><span data-stu-id="431a5-345">-511</span></span></p></td>
<td><p><span data-ttu-id="431a5-346">Error al intentar escribir en el registro después de la recuperación.</span><span class="sxs-lookup"><span data-stu-id="431a5-346">The attempt to write to the log after recovery failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-347">JET_errCannotLogDuringRecoveryRedo</span><span class="sxs-lookup"><span data-stu-id="431a5-347">JET_errCannotLogDuringRecoveryRedo</span></span><br />
<span data-ttu-id="431a5-348">-512</span><span class="sxs-lookup"><span data-stu-id="431a5-348">-512</span></span></p></td>
<td><p><span data-ttu-id="431a5-349">Error al intentar escribir en el registro durante la repuesta de recuperación.</span><span class="sxs-lookup"><span data-stu-id="431a5-349">The attempt to write to the log during the recovery redo failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-350">JET_errLogGenerationMismatch</span><span class="sxs-lookup"><span data-stu-id="431a5-350">JET_errLogGenerationMismatch</span></span><br />
<span data-ttu-id="431a5-351">-513</span><span class="sxs-lookup"><span data-stu-id="431a5-351">-513</span></span></p></td>
<td><p><span data-ttu-id="431a5-352">El nombre del archivo de registro no coincide con el número de generación interno.</span><span class="sxs-lookup"><span data-stu-id="431a5-352">The name of of the log file does not match the internal generation number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-353">JET_errBadLogVersion</span><span class="sxs-lookup"><span data-stu-id="431a5-353">JET_errBadLogVersion</span></span><br />
<span data-ttu-id="431a5-354">-514</span><span class="sxs-lookup"><span data-stu-id="431a5-354">-514</span></span></p></td>
<td><p><span data-ttu-id="431a5-355">La versión del archivo de registro no es compatible con la versión de ESE.</span><span class="sxs-lookup"><span data-stu-id="431a5-355">The version of the log file is not compatible with the ESE version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-356">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="431a5-356">JET_errInvalidLogSequence</span></span><br />
<span data-ttu-id="431a5-357">-515</span><span class="sxs-lookup"><span data-stu-id="431a5-357">-515</span></span></p></td>
<td><p><span data-ttu-id="431a5-358">La marca de tiempo del Registro siguiente no coincide con la marca de tiempo esperada.</span><span class="sxs-lookup"><span data-stu-id="431a5-358">The timestamp in the next log does not match the expected timestamp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-359">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="431a5-359">JET_errLoggingDisabled</span></span><br />
<span data-ttu-id="431a5-360">-516</span><span class="sxs-lookup"><span data-stu-id="431a5-360">-516</span></span></p></td>
<td><p><span data-ttu-id="431a5-361">El registro no está activo.</span><span class="sxs-lookup"><span data-stu-id="431a5-361">The log is not active.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-362">JET_errLogBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="431a5-362">JET_errLogBufferTooSmall</span></span><br />
<span data-ttu-id="431a5-363">-517</span><span class="sxs-lookup"><span data-stu-id="431a5-363">-517</span></span></p></td>
<td><p><span data-ttu-id="431a5-364">El búfer de registro es demasiado pequeño para la recuperación.</span><span class="sxs-lookup"><span data-stu-id="431a5-364">The log buffer is too small for recovery.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-365">JET_errLogSequenceEnd</span><span class="sxs-lookup"><span data-stu-id="431a5-365">JET_errLogSequenceEnd</span></span><br />
<span data-ttu-id="431a5-366">-519</span><span class="sxs-lookup"><span data-stu-id="431a5-366">-519</span></span></p></td>
<td><p><span data-ttu-id="431a5-367">Se ha superado el número máximo de archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="431a5-367">The maximum log file number has been exceeded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-368">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="431a5-368">JET_errNoBackup</span></span><br />
<span data-ttu-id="431a5-369">-520</span><span class="sxs-lookup"><span data-stu-id="431a5-369">-520</span></span></p></td>
<td><p><span data-ttu-id="431a5-370">No hay ninguna copia de seguridad en curso.</span><span class="sxs-lookup"><span data-stu-id="431a5-370">There is no backup in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-371">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="431a5-371">JET_errInvalidBackupSequence</span></span><br />
<span data-ttu-id="431a5-372">-521</span><span class="sxs-lookup"><span data-stu-id="431a5-372">-521</span></span></p></td>
<td><p><span data-ttu-id="431a5-373">La llamada de copia de seguridad está fuera de secuencia.</span><span class="sxs-lookup"><span data-stu-id="431a5-373">The backup call is out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-374">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="431a5-374">JET_errBackupNotAllowedYet</span></span><br />
<span data-ttu-id="431a5-375">-523</span><span class="sxs-lookup"><span data-stu-id="431a5-375">-523</span></span></p></td>
<td><p><span data-ttu-id="431a5-376">No se puede realizar una copia de seguridad en este momento.</span><span class="sxs-lookup"><span data-stu-id="431a5-376">A backup cannot be done at this time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-377">JET_errDeleteBackupFileFail</span><span class="sxs-lookup"><span data-stu-id="431a5-377">JET_errDeleteBackupFileFail</span></span><br />
<span data-ttu-id="431a5-378">-524</span><span class="sxs-lookup"><span data-stu-id="431a5-378">-524</span></span></p></td>
<td><p><span data-ttu-id="431a5-379">No se pudo eliminar un archivo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="431a5-379">A backup file could not be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-380">JET_errMakeBackupDirectoryFail</span><span class="sxs-lookup"><span data-stu-id="431a5-380">JET_errMakeBackupDirectoryFail</span></span><br />
<span data-ttu-id="431a5-381">-525</span><span class="sxs-lookup"><span data-stu-id="431a5-381">-525</span></span></p></td>
<td><p><span data-ttu-id="431a5-382">No se pudo crear el directorio temporal de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="431a5-382">The backup temporary directory could not be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-383">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="431a5-383">JET_errInvalidBackup</span></span><br />
<span data-ttu-id="431a5-384">-526</span><span class="sxs-lookup"><span data-stu-id="431a5-384">-526</span></span></p></td>
<td><p><span data-ttu-id="431a5-385">El registro circular está habilitado; no se puede realizar una copia de seguridad incremental.</span><span class="sxs-lookup"><span data-stu-id="431a5-385">Circular logging is enabled; an incremental backup cannot be performed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-386">JET_errRecoveredWithErrors</span><span class="sxs-lookup"><span data-stu-id="431a5-386">JET_errRecoveredWithErrors</span></span><br />
<span data-ttu-id="431a5-387">-527</span><span class="sxs-lookup"><span data-stu-id="431a5-387">-527</span></span></p></td>
<td><p><span data-ttu-id="431a5-388">Los datos se restauraron con errores.</span><span class="sxs-lookup"><span data-stu-id="431a5-388">The data was restored with errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-389">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="431a5-389">JET_errMissingLogFile</span></span><br />
<span data-ttu-id="431a5-390">-528</span><span class="sxs-lookup"><span data-stu-id="431a5-390">-528</span></span></p></td>
<td><p><span data-ttu-id="431a5-391">Falta el archivo de registro actual.</span><span class="sxs-lookup"><span data-stu-id="431a5-391">The current log file is missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-392">JET_errLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="431a5-392">JET_errLogDiskFull</span></span><br />
<span data-ttu-id="431a5-393">-529</span><span class="sxs-lookup"><span data-stu-id="431a5-393">-529</span></span></p></td>
<td><p><span data-ttu-id="431a5-394">El disco de registro está lleno.</span><span class="sxs-lookup"><span data-stu-id="431a5-394">The log disk is full.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-395">JET_errBadLogSignature</span><span class="sxs-lookup"><span data-stu-id="431a5-395">JET_errBadLogSignature</span></span><br />
<span data-ttu-id="431a5-396">-530</span><span class="sxs-lookup"><span data-stu-id="431a5-396">-530</span></span></p></td>
<td><p><span data-ttu-id="431a5-397">Hay una firma incorrecta para un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="431a5-397">There is a bad signature for a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-398">JET_errBadDbSignature</span><span class="sxs-lookup"><span data-stu-id="431a5-398">JET_errBadDbSignature</span></span><br />
<span data-ttu-id="431a5-399">-531</span><span class="sxs-lookup"><span data-stu-id="431a5-399">-531</span></span></p></td>
<td><p><span data-ttu-id="431a5-400">Hay una firma incorrecta para un archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-400">There is a bad signature for a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-401">JET_errBadCheckpointSignature</span><span class="sxs-lookup"><span data-stu-id="431a5-401">JET_errBadCheckpointSignature</span></span><br />
<span data-ttu-id="431a5-402">-532</span><span class="sxs-lookup"><span data-stu-id="431a5-402">-532</span></span></p></td>
<td><p><span data-ttu-id="431a5-403">Hay una firma incorrecta para un archivo de punto de comprobación.</span><span class="sxs-lookup"><span data-stu-id="431a5-403">There is a bad signature for a checkpoint file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-404">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="431a5-404">JET_errCheckpointCorrupt</span></span><br />
<span data-ttu-id="431a5-405">-533</span><span class="sxs-lookup"><span data-stu-id="431a5-405">-533</span></span></p></td>
<td><p><span data-ttu-id="431a5-406">No se encontró el archivo de punto de comprobación o estaba dañado.</span><span class="sxs-lookup"><span data-stu-id="431a5-406">The checkpoint file was not found or was corrupt.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-407">JET_errMissingPatchPage</span><span class="sxs-lookup"><span data-stu-id="431a5-407">JET_errMissingPatchPage</span></span><br />
<span data-ttu-id="431a5-408">-534</span><span class="sxs-lookup"><span data-stu-id="431a5-408">-534</span></span></p></td>
<td><p><span data-ttu-id="431a5-409">No se encontró la página del archivo de revisión de la base de datos durante la recuperación.</span><span class="sxs-lookup"><span data-stu-id="431a5-409">The database patch file page was not found during recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-410">JET_errBadPatchPage</span><span class="sxs-lookup"><span data-stu-id="431a5-410">JET_errBadPatchPage</span></span><br />
<span data-ttu-id="431a5-411">-535</span><span class="sxs-lookup"><span data-stu-id="431a5-411">-535</span></span></p></td>
<td><p><span data-ttu-id="431a5-412">La página del archivo de revisión de la base de datos no es válida.</span><span class="sxs-lookup"><span data-stu-id="431a5-412">The database patch file page is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-413">JET_errRedoAbruptEnded</span><span class="sxs-lookup"><span data-stu-id="431a5-413">JET_errRedoAbruptEnded</span></span><br />
<span data-ttu-id="431a5-414">-536</span><span class="sxs-lookup"><span data-stu-id="431a5-414">-536</span></span></p></td>
<td><p><span data-ttu-id="431a5-415">La repuesta finalizó repentinamente debido a un error repentino al leer los registros del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="431a5-415">The redo abruptly ended due to a sudden failure while reading logs from the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-416">JET_errBadSLVSignature</span><span class="sxs-lookup"><span data-stu-id="431a5-416">JET_errBadSLVSignature</span></span><br />
<span data-ttu-id="431a5-417">-537</span><span class="sxs-lookup"><span data-stu-id="431a5-417">-537</span></span></p></td>
<td><p><span data-ttu-id="431a5-418">Esta marca está reservada.</span><span class="sxs-lookup"><span data-stu-id="431a5-418">This flag is reserved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-419">JET_errPatchFileMissing</span><span class="sxs-lookup"><span data-stu-id="431a5-419">JET_errPatchFileMissing</span></span><br />
<span data-ttu-id="431a5-420">-538</span><span class="sxs-lookup"><span data-stu-id="431a5-420">-538</span></span></p></td>
<td><p><span data-ttu-id="431a5-421">La restauración de hardware detectó que falta un archivo de revisión de base de datos en el conjunto de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="431a5-421">The hard restore detected that a database patch file is missing from the backup set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-422">JET_errDatabaseLogSetMismatch</span><span class="sxs-lookup"><span data-stu-id="431a5-422">JET_errDatabaseLogSetMismatch</span></span><br />
<span data-ttu-id="431a5-423">-539</span><span class="sxs-lookup"><span data-stu-id="431a5-423">-539</span></span></p></td>
<td><p><span data-ttu-id="431a5-424">La base de datos no pertenece al conjunto actual de archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="431a5-424">The database does not belong with the current set of log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-425">JET_errDatabaseStreamingFileMismatch</span><span class="sxs-lookup"><span data-stu-id="431a5-425">JET_errDatabaseStreamingFileMismatch</span></span><br />
<span data-ttu-id="431a5-426">-540</span><span class="sxs-lookup"><span data-stu-id="431a5-426">-540</span></span></p></td>
<td><p><span data-ttu-id="431a5-427">Esta marca está reservada.</span><span class="sxs-lookup"><span data-stu-id="431a5-427">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-428">JET_errLogFileSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="431a5-428">JET_errLogFileSizeMismatch</span></span><br />
<span data-ttu-id="431a5-429">-541</span><span class="sxs-lookup"><span data-stu-id="431a5-429">-541</span></span></p></td>
<td><p><span data-ttu-id="431a5-430">El tamaño real del archivo de registro no coincide con <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span><span class="sxs-lookup"><span data-stu-id="431a5-430">The actual log file size does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-431">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="431a5-431">JET_errCheckpointFileNotFound</span></span><br />
<span data-ttu-id="431a5-432">-542</span><span class="sxs-lookup"><span data-stu-id="431a5-432">-542</span></span></p></td>
<td><p><span data-ttu-id="431a5-433">No se pudo encontrar el archivo de punto de comprobación.</span><span class="sxs-lookup"><span data-stu-id="431a5-433">The checkpoint file could not be located.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-434">JET_errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="431a5-434">JET_errRequiredLogFilesMissing</span></span><br />
<span data-ttu-id="431a5-435">-543</span><span class="sxs-lookup"><span data-stu-id="431a5-435">-543</span></span></p></td>
<td><p><span data-ttu-id="431a5-436">Faltan los archivos de registro necesarios para la recuperación.</span><span class="sxs-lookup"><span data-stu-id="431a5-436">The required log files for recovery are missing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-437">JET_errSoftRecoveryOnBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="431a5-437">JET_errSoftRecoveryOnBackupDatabase</span></span><br />
<span data-ttu-id="431a5-438">-544</span><span class="sxs-lookup"><span data-stu-id="431a5-438">-544</span></span></p></td>
<td><p><span data-ttu-id="431a5-439">Una recuperación de software está a punto de usarse en una base de datos de copia de seguridad cuando se debe utilizar en su lugar una restauración.</span><span class="sxs-lookup"><span data-stu-id="431a5-439">A soft recovery is about to be used on a backup database when a restore should be used instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-440">JET_errLogFileSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="431a5-440">JET_errLogFileSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="431a5-441">-545</span><span class="sxs-lookup"><span data-stu-id="431a5-441">-545</span></span></p></td>
<td><p><span data-ttu-id="431a5-442">Se han recuperado las bases de datos, pero el tamaño del archivo de registro usado durante la recuperación no coincide con <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span><span class="sxs-lookup"><span data-stu-id="431a5-442">The databases have been recovered, but the log file size used during recovery does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-443">JET_errLogSectorSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="431a5-443">JET_errLogSectorSizeMismatch</span></span><br />
<span data-ttu-id="431a5-444">-546</span><span class="sxs-lookup"><span data-stu-id="431a5-444">-546</span></span></p></td>
<td><p><span data-ttu-id="431a5-445">El tamaño del sector del archivo de registro no coincide con el tamaño del sector del volumen actual.</span><span class="sxs-lookup"><span data-stu-id="431a5-445">The log file sector size does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="431a5-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="431a5-447">-547</span><span class="sxs-lookup"><span data-stu-id="431a5-447">-547</span></span></p></td>
<td><p><span data-ttu-id="431a5-448">Se han recuperado las bases de datos, pero el tamaño del sector del archivo de registro (usado durante la recuperación) no coincide con el tamaño del sector del volumen actual.</span><span class="sxs-lookup"><span data-stu-id="431a5-448">The databases have been recovered, but the log file sector size (used during recovery) does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-449">JET_errLogSequenceEndDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="431a5-449">JET_errLogSequenceEndDatabasesConsistent</span></span><br />
<span data-ttu-id="431a5-450">-548</span><span class="sxs-lookup"><span data-stu-id="431a5-450">-548</span></span></p></td>
<td><p><span data-ttu-id="431a5-451">Se han recuperado las bases de datos, pero se han utilizado todas las generaciones de registro posibles en la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="431a5-451">The databases have been recovered, but all possible log generations in the current sequence have been used.</span></span> <span data-ttu-id="431a5-452">Deben eliminarse todos los archivos de registro y el archivo de punto de comprobación y se deben realizar copias de seguridad de las bases de datos antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="431a5-452">All log files and the checkpoint file must be deleted and databases must be backed up before continuing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-453">JET_errStreamingDataNotLogged</span><span class="sxs-lookup"><span data-stu-id="431a5-453">JET_errStreamingDataNotLogged</span></span><br />
<span data-ttu-id="431a5-454">-549</span><span class="sxs-lookup"><span data-stu-id="431a5-454">-549</span></span></p></td>
<td><p><span data-ttu-id="431a5-455">Se produjo un intento no válido de reproducir una operación de transmisión de archivos en la que los datos no se registraron.</span><span class="sxs-lookup"><span data-stu-id="431a5-455">There was an illegal attempt to replay a streaming file operation where the data was not logged.</span></span> <span data-ttu-id="431a5-456">Esto probablemente se debe a un intento de puesta al día con el registro circular habilitado.</span><span class="sxs-lookup"><span data-stu-id="431a5-456">This is probably caused by an attempt to rollforward with circular logging enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-457">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="431a5-457">JET_errDatabaseDirtyShutdown</span></span><br />
<span data-ttu-id="431a5-458">-550</span><span class="sxs-lookup"><span data-stu-id="431a5-458">-550</span></span></p></td>
<td><p><span data-ttu-id="431a5-459">La base de datos no se ha cerrado correctamente.</span><span class="sxs-lookup"><span data-stu-id="431a5-459">The database was not shutdown cleanly.</span></span> <span data-ttu-id="431a5-460">Primero se debe ejecutar una recuperación para completar correctamente las operaciones de base de datos para el cierre anterior.</span><span class="sxs-lookup"><span data-stu-id="431a5-460">A recovery must first be run to properly complete database operations for the previous shutdown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-461">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="431a5-461">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="431a5-462">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="431a5-462">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="431a5-463">Este error está obsoleto y se ha reemplazado por JET_errDatabaseDirtyShutdown.</span><span class="sxs-lookup"><span data-stu-id="431a5-463">This error is obsolete and has been replaced by JET_errDatabaseDirtyShutdown.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-464">JET_errConsistentTimeMismatch</span><span class="sxs-lookup"><span data-stu-id="431a5-464">JET_errConsistentTimeMismatch</span></span><br />
<span data-ttu-id="431a5-465">-551</span><span class="sxs-lookup"><span data-stu-id="431a5-465">-551</span></span></p></td>
<td><p><span data-ttu-id="431a5-466">No se ha encontrado la última hora coherente para la base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-466">The last consistent time for the database has not been matched.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-467">JET_errDatabasePatchFileMismatch</span><span class="sxs-lookup"><span data-stu-id="431a5-467">JET_errDatabasePatchFileMismatch</span></span><br />
<span data-ttu-id="431a5-468">-552</span><span class="sxs-lookup"><span data-stu-id="431a5-468">-552</span></span></p></td>
<td><p><span data-ttu-id="431a5-469">El archivo de revisión de la base de datos no se genera a partir de esta copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="431a5-469">The database patch file is not generated from this backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-470">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="431a5-470">JET_errEndingRestoreLogTooLow</span></span><br />
<span data-ttu-id="431a5-471">-553</span><span class="sxs-lookup"><span data-stu-id="431a5-471">-553</span></span></p></td>
<td><p><span data-ttu-id="431a5-472">El número de registro de inicio es demasiado bajo para la restauración.</span><span class="sxs-lookup"><span data-stu-id="431a5-472">The starting log number is too low for the restore.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-473">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="431a5-473">JET_errStartingRestoreLogTooHigh</span></span><br />
<span data-ttu-id="431a5-474">-554</span><span class="sxs-lookup"><span data-stu-id="431a5-474">-554</span></span></p></td>
<td><p><span data-ttu-id="431a5-475">El número de registro de inicio es demasiado alto para la restauración.</span><span class="sxs-lookup"><span data-stu-id="431a5-475">The starting log number is too high for the restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-476">JET_errGivenLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="431a5-476">JET_errGivenLogFileHasBadSignature</span></span><br />
<span data-ttu-id="431a5-477">-555</span><span class="sxs-lookup"><span data-stu-id="431a5-477">-555</span></span></p></td>
<td><p><span data-ttu-id="431a5-478">El archivo de registro de restauración tiene una firma incorrecta.</span><span class="sxs-lookup"><span data-stu-id="431a5-478">The restore log file has a bad signature.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-479">JET_errGivenLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="431a5-479">JET_errGivenLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="431a5-480">-556</span><span class="sxs-lookup"><span data-stu-id="431a5-480">-556</span></span></p></td>
<td><p><span data-ttu-id="431a5-481">El archivo de registro de restauración no es contiguo.</span><span class="sxs-lookup"><span data-stu-id="431a5-481">The restore log file is not contiguous.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-482">JET_errMissingRestoreLogFiles</span><span class="sxs-lookup"><span data-stu-id="431a5-482">JET_errMissingRestoreLogFiles</span></span><br />
<span data-ttu-id="431a5-483">-557</span><span class="sxs-lookup"><span data-stu-id="431a5-483">-557</span></span></p></td>
<td><p><span data-ttu-id="431a5-484">Faltan algunos archivos de registro de restauración.</span><span class="sxs-lookup"><span data-stu-id="431a5-484">Some restore log files are missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-485">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="431a5-485">JET_errMissingFullBackup</span></span><br />
<span data-ttu-id="431a5-486">-560</span><span class="sxs-lookup"><span data-stu-id="431a5-486">-560</span></span></p></td>
<td><p><span data-ttu-id="431a5-487">La base de datos perdió una copia de seguridad completa anterior antes de intentar realizar una copia de seguridad incremental.</span><span class="sxs-lookup"><span data-stu-id="431a5-487">The database missed a previous full backup before attempting to perform an incremental backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-488">JET_errBadBackupDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="431a5-488">JET_errBadBackupDatabaseSize</span></span><br />
<span data-ttu-id="431a5-489">-561</span><span class="sxs-lookup"><span data-stu-id="431a5-489">-561</span></span></p></td>
<td><p><span data-ttu-id="431a5-490">El tamaño de la base de datos de copia de seguridad no es múltiplo del tamaño de página de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-490">The backup database size is not a multiple of the database page size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-491">JET_errDatabaseAlreadyUpgraded</span><span class="sxs-lookup"><span data-stu-id="431a5-491">JET_errDatabaseAlreadyUpgraded</span></span><br />
<span data-ttu-id="431a5-492">-562</span><span class="sxs-lookup"><span data-stu-id="431a5-492">-562</span></span></p></td>
<td><p><span data-ttu-id="431a5-493">Se ha detenido el intento actual de actualizar una base de datos porque la base de datos ya está actualizada.</span><span class="sxs-lookup"><span data-stu-id="431a5-493">The current attempt to upgrade a database has been stopped because the database is already current.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-494">JET_errDatabaseIncompleteUpgrade</span><span class="sxs-lookup"><span data-stu-id="431a5-494">JET_errDatabaseIncompleteUpgrade</span></span><br />
<span data-ttu-id="431a5-495">-563</span><span class="sxs-lookup"><span data-stu-id="431a5-495">-563</span></span></p></td>
<td><p><span data-ttu-id="431a5-496">La base de datos se convirtió solo parcialmente en el formato actual.</span><span class="sxs-lookup"><span data-stu-id="431a5-496">The database was only partially converted to the current format.</span></span> <span data-ttu-id="431a5-497">La base de datos debe restaurarse a partir de una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="431a5-497">The database must be restored from backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-498">JET_errMissingCurrentLogFiles</span><span class="sxs-lookup"><span data-stu-id="431a5-498">JET_errMissingCurrentLogFiles</span></span><br />
<span data-ttu-id="431a5-499">-565</span><span class="sxs-lookup"><span data-stu-id="431a5-499">-565</span></span></p></td>
<td><p><span data-ttu-id="431a5-500">Faltan algunos archivos de registro actuales para la restauración continua.</span><span class="sxs-lookup"><span data-stu-id="431a5-500">Some current log files are missing for continuous restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-501">JET_errDbTimeTooOld</span><span class="sxs-lookup"><span data-stu-id="431a5-501">JET_errDbTimeTooOld</span></span><br />
<span data-ttu-id="431a5-502">-566</span><span class="sxs-lookup"><span data-stu-id="431a5-502">-566</span></span></p></td>
<td><p><span data-ttu-id="431a5-503">El dbTime de una página es menor que el dbtimeBefore que se encuentra en el registro.</span><span class="sxs-lookup"><span data-stu-id="431a5-503">The dbtime on a page is smaller than the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-504">JET_errDbTimeTooNew</span><span class="sxs-lookup"><span data-stu-id="431a5-504">JET_errDbTimeTooNew</span></span><br />
<span data-ttu-id="431a5-505">-567</span><span class="sxs-lookup"><span data-stu-id="431a5-505">-567</span></span></p></td>
<td><p><span data-ttu-id="431a5-506">El dbTime de una página es anterior al dbtimeBefore que se encuentra en el registro.</span><span class="sxs-lookup"><span data-stu-id="431a5-506">The dbtime on a page is in advance of the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-507">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="431a5-507">JET_errMissingFileToBackup</span></span><br />
<span data-ttu-id="431a5-508">-569</span><span class="sxs-lookup"><span data-stu-id="431a5-508">-569</span></span></p></td>
<td><p><span data-ttu-id="431a5-509">Faltan algunos archivos de revisión de registro o de base de datos durante la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="431a5-509">Some log or database patch files were missing during the backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-510">JET_errLogTornWriteDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="431a5-510">JET_errLogTornWriteDuringHardRestore</span></span><br />
<span data-ttu-id="431a5-511">-570</span><span class="sxs-lookup"><span data-stu-id="431a5-511">-570</span></span></p></td>
<td><p><span data-ttu-id="431a5-512">Se detectó una escritura rasgada en una copia de seguridad que se estableció durante una restauración de hardware.</span><span class="sxs-lookup"><span data-stu-id="431a5-512">A torn write was detected in a backup that was set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-513">JET_errLogTornWriteDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="431a5-513">JET_errLogTornWriteDuringHardRecovery</span></span><br />
<span data-ttu-id="431a5-514">-571</span><span class="sxs-lookup"><span data-stu-id="431a5-514">-571</span></span></p></td>
<td><p><span data-ttu-id="431a5-515">Se detectó una escritura incompleta durante una recuperación de hardware (el registro no formaba parte de un conjunto de copia de seguridad).</span><span class="sxs-lookup"><span data-stu-id="431a5-515">A torn write was detected during a hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-516">JET_errLogCorruptDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="431a5-516">JET_errLogCorruptDuringHardRestore</span></span><br />
<span data-ttu-id="431a5-517">-573</span><span class="sxs-lookup"><span data-stu-id="431a5-517">-573</span></span></p></td>
<td><p><span data-ttu-id="431a5-518">Se detectaron daños en un conjunto de copia de seguridad durante una restauración de hardware.</span><span class="sxs-lookup"><span data-stu-id="431a5-518">Corruption was detected in a backup set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-519">JET_errLogCorruptDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="431a5-519">JET_errLogCorruptDuringHardRecovery</span></span><br />
<span data-ttu-id="431a5-520">-574</span><span class="sxs-lookup"><span data-stu-id="431a5-520">-574</span></span></p></td>
<td><p><span data-ttu-id="431a5-521">Se detectaron daños durante la recuperación de hardware (el registro no formaba parte de un conjunto de copia de seguridad).</span><span class="sxs-lookup"><span data-stu-id="431a5-521">Corruption was detected during hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-522">JET_errMustDisableLoggingForDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="431a5-522">JET_errMustDisableLoggingForDbUpgrade</span></span><br />
<span data-ttu-id="431a5-523">-575</span><span class="sxs-lookup"><span data-stu-id="431a5-523">-575</span></span></p></td>
<td><p><span data-ttu-id="431a5-524">No se puede habilitar el registro al intentar actualizar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-524">Logging cannot be enabled while attempting to upgrade a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-525">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="431a5-525">JET_errBadRestoreTargetInstance</span></span><br />
<span data-ttu-id="431a5-526">-577</span><span class="sxs-lookup"><span data-stu-id="431a5-526">-577</span></span></p></td>
<td><p><span data-ttu-id="431a5-527">No se ha encontrado el TargetInstance que se especificó para la restauración o los archivos de registro no coinciden.</span><span class="sxs-lookup"><span data-stu-id="431a5-527">Either the TargetInstance that was specified for restore has not been found or the log files do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-528">JET_errRecoveredWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="431a5-528">JET_errRecoveredWithoutUndo</span></span><br />
<span data-ttu-id="431a5-529">-579</span><span class="sxs-lookup"><span data-stu-id="431a5-529">-579</span></span></p></td>
<td><p><span data-ttu-id="431a5-530">El motor de base de datos ha reproducido correctamente todas las operaciones en el registro de transacciones para realizar una recuperación tras bloqueo, pero el autor de la llamada decidió detener la recuperación sin revertir las actualizaciones no confirmadas.</span><span class="sxs-lookup"><span data-stu-id="431a5-530">The database engine successfully replayed all operations in the transaction log to perform a crash recovery but the caller elected to stop recovery without rolling back uncommitted updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-531">JET_errDatabasesNotFromSameSnapshot</span><span class="sxs-lookup"><span data-stu-id="431a5-531">JET_errDatabasesNotFromSameSnapshot</span></span><br />
<span data-ttu-id="431a5-532">-580</span><span class="sxs-lookup"><span data-stu-id="431a5-532">-580</span></span></p></td>
<td><p><span data-ttu-id="431a5-533">Las bases de datos que se van a restaurar no son de la misma copia de seguridad de instantánea.</span><span class="sxs-lookup"><span data-stu-id="431a5-533">The databases to be restored are not from the same shadow copy backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-534">JET_errSoftRecoveryOnSnapshot</span><span class="sxs-lookup"><span data-stu-id="431a5-534">JET_errSoftRecoveryOnSnapshot</span></span><br />
<span data-ttu-id="431a5-535">-581</span><span class="sxs-lookup"><span data-stu-id="431a5-535">-581</span></span></p></td>
<td><p><span data-ttu-id="431a5-536">Hay una recuperación de software en una base de datos de un conjunto de copia de seguridad de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="431a5-536">There is a soft recovery on a database from a shadow copy backup set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-537">JET_errUnicodeTranslationBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="431a5-537">JET_errUnicodeTranslationBufferTooSmall</span></span><br />
<span data-ttu-id="431a5-538">-601</span><span class="sxs-lookup"><span data-stu-id="431a5-538">-601</span></span></p></td>
<td><p><span data-ttu-id="431a5-539">El búfer de conversión Unicode es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="431a5-539">The Unicode translation buffer is too small.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-540">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="431a5-540">JET_errUnicodeTranslationFail</span></span><br />
<span data-ttu-id="431a5-541">-602</span><span class="sxs-lookup"><span data-stu-id="431a5-541">-602</span></span></p></td>
<td><p><span data-ttu-id="431a5-542">Error de normalización Unicode.</span><span class="sxs-lookup"><span data-stu-id="431a5-542">The Unicode normalization failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-543">JET_errUnicodeNormalizationNotSupported</span><span class="sxs-lookup"><span data-stu-id="431a5-543">JET_errUnicodeNormalizationNotSupported</span></span><br />
<span data-ttu-id="431a5-544">-603</span><span class="sxs-lookup"><span data-stu-id="431a5-544">-603</span></span></p></td>
<td><p><span data-ttu-id="431a5-545">El sistema operativo no proporciona compatibilidad con la normalización Unicode y no se especificó una devolución de llamada de normalización.</span><span class="sxs-lookup"><span data-stu-id="431a5-545">The operating system does not provide support for Unicode normalization and a normalization callback was not specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-546">JET_errExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="431a5-546">JET_errExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="431a5-547">-610</span><span class="sxs-lookup"><span data-stu-id="431a5-547">-610</span></span></p></td>
<td><p><span data-ttu-id="431a5-548">El archivo de registro existente tiene una firma incorrecta.</span><span class="sxs-lookup"><span data-stu-id="431a5-548">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-549">JET_errExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="431a5-549">JET_errExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="431a5-550">-611</span><span class="sxs-lookup"><span data-stu-id="431a5-550">-611</span></span></p></td>
<td><p><span data-ttu-id="431a5-551">Un archivo de registro existente no es contiguo.</span><span class="sxs-lookup"><span data-stu-id="431a5-551">An existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-552">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="431a5-552">JET_errLogReadVerifyFailure</span></span><br />
<span data-ttu-id="431a5-553">-612</span><span class="sxs-lookup"><span data-stu-id="431a5-553">-612</span></span></p></td>
<td><p><span data-ttu-id="431a5-554">Se encontró un error de suma de comprobación en el archivo de registro durante la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="431a5-554">A checksum error was found in the log file during backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-555">JET_errSLVReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="431a5-555">JET_errSLVReadVerifyFailure</span></span><br />
<span data-ttu-id="431a5-556">-613</span><span class="sxs-lookup"><span data-stu-id="431a5-556">-613</span></span></p></td>
<td><p><span data-ttu-id="431a5-557">Esta marca está reservada.</span><span class="sxs-lookup"><span data-stu-id="431a5-557">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-558">JET_errCheckpointDepthTooDeep</span><span class="sxs-lookup"><span data-stu-id="431a5-558">JET_errCheckpointDepthTooDeep</span></span><br />
<span data-ttu-id="431a5-559">-614</span><span class="sxs-lookup"><span data-stu-id="431a5-559">-614</span></span></p></td>
<td><p><span data-ttu-id="431a5-560">Hay demasiadas generaciones pendientes entre el punto de control y la generación actual.</span><span class="sxs-lookup"><span data-stu-id="431a5-560">There are too many outstanding generations between the checkpoint and the current generation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-561">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="431a5-561">JET_errRestoreOfNonBackupDatabase</span></span><br />
<span data-ttu-id="431a5-562">-615</span><span class="sxs-lookup"><span data-stu-id="431a5-562">-615</span></span></p></td>
<td><p><span data-ttu-id="431a5-563">Se intentó realizar una recuperación de hardware en una base de datos que no era una base de datos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="431a5-563">A hard recovery was attempted on a database that was not a backup database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-564">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="431a5-564">JET_errInvalidGrbit</span></span><br />
<span data-ttu-id="431a5-565">-900</span><span class="sxs-lookup"><span data-stu-id="431a5-565">-900</span></span></p></td>
<td><p><span data-ttu-id="431a5-566">Hay un parámetro grbit no válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-566">There is an invalid grbit parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-567">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="431a5-567">JET_errTermInProgress</span></span><br />
<span data-ttu-id="431a5-568">-1000</span><span class="sxs-lookup"><span data-stu-id="431a5-568">-1000</span></span></p></td>
<td><p><span data-ttu-id="431a5-569">La terminación está en curso.</span><span class="sxs-lookup"><span data-stu-id="431a5-569">Termination is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-570">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="431a5-570">JET_errFeatureNotAvailable</span></span><br />
<span data-ttu-id="431a5-571">-1001</span><span class="sxs-lookup"><span data-stu-id="431a5-571">-1001</span></span></p></td>
<td><p><span data-ttu-id="431a5-572">Este elemento de API no se admite.</span><span class="sxs-lookup"><span data-stu-id="431a5-572">This API element is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-573">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="431a5-573">JET_errInvalidName</span></span><br />
<span data-ttu-id="431a5-574">-1002</span><span class="sxs-lookup"><span data-stu-id="431a5-574">-1002</span></span></p></td>
<td><p><span data-ttu-id="431a5-575">Se está utilizando un nombre no válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-575">An invalid name is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-576">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="431a5-576">JET_errInvalidParameter</span></span><br />
<span data-ttu-id="431a5-577">-1003</span><span class="sxs-lookup"><span data-stu-id="431a5-577">-1003</span></span></p></td>
<td><p><span data-ttu-id="431a5-578">Se está utilizando un parámetro de API no válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-578">An invalid API parameter is being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-579">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="431a5-579">JET_errDatabaseFileReadOnly</span></span><br />
<span data-ttu-id="431a5-580">-1008</span><span class="sxs-lookup"><span data-stu-id="431a5-580">-1008</span></span></p></td>
<td><p><span data-ttu-id="431a5-581">Se intentó asociar a un archivo de base de datos de solo lectura para las operaciones de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="431a5-581">There was an attempt to attach to a read-only database file for read/write operations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-582">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="431a5-582">JET_errInvalidDatabaseId</span></span><br />
<span data-ttu-id="431a5-583">-1010</span><span class="sxs-lookup"><span data-stu-id="431a5-583">-1010</span></span></p></td>
<td><p><span data-ttu-id="431a5-584">Hay un identificador de base de datos no válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-584">There is an invalid database ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-585">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="431a5-585">JET_errOutOfMemory</span></span><br />
<span data-ttu-id="431a5-586">-1011</span><span class="sxs-lookup"><span data-stu-id="431a5-586">-1011</span></span></p></td>
<td><p><span data-ttu-id="431a5-587">El sistema no tiene memoria suficiente.</span><span class="sxs-lookup"><span data-stu-id="431a5-587">The system is out of memory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-588">JET_errOutOfDatabaseSpace</span><span class="sxs-lookup"><span data-stu-id="431a5-588">JET_errOutOfDatabaseSpace</span></span><br />
<span data-ttu-id="431a5-589">-1012</span><span class="sxs-lookup"><span data-stu-id="431a5-589">-1012</span></span></p></td>
<td><p><span data-ttu-id="431a5-590">Se ha alcanzado el tamaño máximo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-590">The maximum database size has been reached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-591">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="431a5-591">JET_errOutOfCursors</span></span><br />
<span data-ttu-id="431a5-592">-1013</span><span class="sxs-lookup"><span data-stu-id="431a5-592">-1013</span></span></p></td>
<td><p><span data-ttu-id="431a5-593">La tabla está fuera de cursores.</span><span class="sxs-lookup"><span data-stu-id="431a5-593">The table is out of cursors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-594">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="431a5-594">JET_errOutOfBuffers</span></span><br />
<span data-ttu-id="431a5-595">-1014</span><span class="sxs-lookup"><span data-stu-id="431a5-595">-1014</span></span></p></td>
<td><p><span data-ttu-id="431a5-596">La base de datos no tiene búferes de página.</span><span class="sxs-lookup"><span data-stu-id="431a5-596">The database is out of page buffers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-597">JET_errTooManyIndexes</span><span class="sxs-lookup"><span data-stu-id="431a5-597">JET_errTooManyIndexes</span></span><br />
<span data-ttu-id="431a5-598">-1015</span><span class="sxs-lookup"><span data-stu-id="431a5-598">-1015</span></span></p></td>
<td><p><span data-ttu-id="431a5-599">Hay demasiados índices.</span><span class="sxs-lookup"><span data-stu-id="431a5-599">There are too many indexes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-600">JET_errTooManyKeys</span><span class="sxs-lookup"><span data-stu-id="431a5-600">JET_errTooManyKeys</span></span><br />
<span data-ttu-id="431a5-601">-1016</span><span class="sxs-lookup"><span data-stu-id="431a5-601">-1016</span></span></p></td>
<td><p><span data-ttu-id="431a5-602">Hay demasiadas columnas en un índice.</span><span class="sxs-lookup"><span data-stu-id="431a5-602">There are too many columns in an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-603">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="431a5-603">JET_errRecordDeleted</span></span><br />
<span data-ttu-id="431a5-604">-1017</span><span class="sxs-lookup"><span data-stu-id="431a5-604">-1017</span></span></p></td>
<td><p><span data-ttu-id="431a5-605">El registro se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="431a5-605">The record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-606">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="431a5-606">JET_errReadVerifyFailure</span></span><br />
<span data-ttu-id="431a5-607">-1018</span><span class="sxs-lookup"><span data-stu-id="431a5-607">-1018</span></span></p></td>
<td><p><span data-ttu-id="431a5-608">Hay un error de suma de comprobación en una página de base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-608">There is a checksum error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-609">JET_errPageNotInitialized</span><span class="sxs-lookup"><span data-stu-id="431a5-609">JET_errPageNotInitialized</span></span><br />
<span data-ttu-id="431a5-610">-1019</span><span class="sxs-lookup"><span data-stu-id="431a5-610">-1019</span></span></p></td>
<td><p><span data-ttu-id="431a5-611">Hay una página de base de datos en blanco.</span><span class="sxs-lookup"><span data-stu-id="431a5-611">There is a blank database page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-612">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="431a5-612">JET_errOutOfFileHandles</span></span><br />
<span data-ttu-id="431a5-613">-1020</span><span class="sxs-lookup"><span data-stu-id="431a5-613">-1020</span></span></p></td>
<td><p><span data-ttu-id="431a5-614">No hay identificadores de archivo.</span><span class="sxs-lookup"><span data-stu-id="431a5-614">There are no file handles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-615">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="431a5-615">JET_errDiskIO</span></span><br />
<span data-ttu-id="431a5-616">-1022</span><span class="sxs-lookup"><span data-stu-id="431a5-616">-1022</span></span></p></td>
<td><p><span data-ttu-id="431a5-617">Hay un error de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="431a5-617">There is a disk IO error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-618">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="431a5-618">JET_errInvalidPath</span></span><br />
<span data-ttu-id="431a5-619">-1023</span><span class="sxs-lookup"><span data-stu-id="431a5-619">-1023</span></span></p></td>
<td><p><span data-ttu-id="431a5-620">Hay una ruta de acceso de archivo no válida.</span><span class="sxs-lookup"><span data-stu-id="431a5-620">There is an invalid file path.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-621">JET_errInvalidSystemPath</span><span class="sxs-lookup"><span data-stu-id="431a5-621">JET_errInvalidSystemPath</span></span><br />
<span data-ttu-id="431a5-622">-1024</span><span class="sxs-lookup"><span data-stu-id="431a5-622">-1024</span></span></p></td>
<td><p><span data-ttu-id="431a5-623">Hay una ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="431a5-623">There is an invalid system path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-624">JET_errInvalidLogDirectory</span><span class="sxs-lookup"><span data-stu-id="431a5-624">JET_errInvalidLogDirectory</span></span><br />
<span data-ttu-id="431a5-625">-1025</span><span class="sxs-lookup"><span data-stu-id="431a5-625">-1025</span></span></p></td>
<td><p><span data-ttu-id="431a5-626">Hay un directorio de registro no válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-626">There is an invalid log directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-627">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="431a5-627">JET_errRecordTooBig</span></span><br />
<span data-ttu-id="431a5-628">-1026</span><span class="sxs-lookup"><span data-stu-id="431a5-628">-1026</span></span></p></td>
<td><p><span data-ttu-id="431a5-629">El registro es mayor que el tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="431a5-629">The record is larger than maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-630">JET_errTooManyOpenDatabases</span><span class="sxs-lookup"><span data-stu-id="431a5-630">JET_errTooManyOpenDatabases</span></span><br />
<span data-ttu-id="431a5-631">-1027</span><span class="sxs-lookup"><span data-stu-id="431a5-631">-1027</span></span></p></td>
<td><p><span data-ttu-id="431a5-632">Hay demasiadas bases de datos abiertas.</span><span class="sxs-lookup"><span data-stu-id="431a5-632">There are too many open databases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-633">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="431a5-633">JET_errInvalidDatabase</span></span><br />
<span data-ttu-id="431a5-634">-1028</span><span class="sxs-lookup"><span data-stu-id="431a5-634">-1028</span></span></p></td>
<td><p><span data-ttu-id="431a5-635">No es un archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-635">This is not a database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-636">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="431a5-636">JET_errNotInitialized</span></span><br />
<span data-ttu-id="431a5-637">-1029</span><span class="sxs-lookup"><span data-stu-id="431a5-637">-1029</span></span></p></td>
<td><p><span data-ttu-id="431a5-638">El motor de base de datos no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="431a5-638">The database engine has not been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-639">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="431a5-639">JET_errAlreadyInitialized</span></span><br />
<span data-ttu-id="431a5-640">-1030</span><span class="sxs-lookup"><span data-stu-id="431a5-640">-1030</span></span></p></td>
<td><p><span data-ttu-id="431a5-641">El motor de base de datos ya está inicializado.</span><span class="sxs-lookup"><span data-stu-id="431a5-641">The database engine is already initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-642">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="431a5-642">JET_errInitInProgress</span></span><br />
<span data-ttu-id="431a5-643">-1031</span><span class="sxs-lookup"><span data-stu-id="431a5-643">-1031</span></span></p></td>
<td><p><span data-ttu-id="431a5-644">El motor de base de datos se está inicializando.</span><span class="sxs-lookup"><span data-stu-id="431a5-644">The database engine is being initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-645">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="431a5-645">JET_errFileAccessDenied</span></span><br />
<span data-ttu-id="431a5-646">-1032</span><span class="sxs-lookup"><span data-stu-id="431a5-646">-1032</span></span></p></td>
<td><p><span data-ttu-id="431a5-647">No se puede tener acceso al archivo porque el archivo está bloqueado o en uso.</span><span class="sxs-lookup"><span data-stu-id="431a5-647">The file cannot be accessed because the file is locked or in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-648">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="431a5-648">JET_errBufferTooSmall</span></span><br />
<span data-ttu-id="431a5-649">-1038</span><span class="sxs-lookup"><span data-stu-id="431a5-649">-1038</span></span></p></td>
<td><p><span data-ttu-id="431a5-650">El búfer es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="431a5-650">The buffer is too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-651">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="431a5-651">JET_errTooManyColumns</span></span><br />
<span data-ttu-id="431a5-652">-1040</span><span class="sxs-lookup"><span data-stu-id="431a5-652">-1040</span></span></p></td>
<td><p><span data-ttu-id="431a5-653">Hay demasiadas columnas definidas.</span><span class="sxs-lookup"><span data-stu-id="431a5-653">Too many columns are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-654">JET_errContainerNotEmpty</span><span class="sxs-lookup"><span data-stu-id="431a5-654">JET_errContainerNotEmpty</span></span><br />
<span data-ttu-id="431a5-655">-1043</span><span class="sxs-lookup"><span data-stu-id="431a5-655">-1043</span></span></p></td>
<td><p><span data-ttu-id="431a5-656">El contenedor no está vacío.</span><span class="sxs-lookup"><span data-stu-id="431a5-656">The container is not empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-657">JET_errInvalidFilename</span><span class="sxs-lookup"><span data-stu-id="431a5-657">JET_errInvalidFilename</span></span><br />
<span data-ttu-id="431a5-658">-1044</span><span class="sxs-lookup"><span data-stu-id="431a5-658">-1044</span></span></p></td>
<td><p><span data-ttu-id="431a5-659">El nombre de archivo no es válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-659">The filename is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-660">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="431a5-660">JET_errInvalidBookmark</span></span><br />
<span data-ttu-id="431a5-661">-1045</span><span class="sxs-lookup"><span data-stu-id="431a5-661">-1045</span></span></p></td>
<td><p><span data-ttu-id="431a5-662">Hay un marcador no válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-662">There is an invalid bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-663">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="431a5-663">JET_errColumnInUse</span></span><br />
<span data-ttu-id="431a5-664">-1046</span><span class="sxs-lookup"><span data-stu-id="431a5-664">-1046</span></span></p></td>
<td><p><span data-ttu-id="431a5-665">La columna utilizada se encuentra en un índice.</span><span class="sxs-lookup"><span data-stu-id="431a5-665">The column used is in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-666">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="431a5-666">JET_errInvalidBufferSize</span></span><br />
<span data-ttu-id="431a5-667">-1047</span><span class="sxs-lookup"><span data-stu-id="431a5-667">-1047</span></span></p></td>
<td><p><span data-ttu-id="431a5-668">El búfer de datos no coincide con el tamaño de la columna.</span><span class="sxs-lookup"><span data-stu-id="431a5-668">The data buffer does not match the column size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-669">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="431a5-669">JET_errColumnNotUpdatable</span></span><br />
<span data-ttu-id="431a5-670">-1048</span><span class="sxs-lookup"><span data-stu-id="431a5-670">-1048</span></span></p></td>
<td><p><span data-ttu-id="431a5-671">No se puede establecer el valor de la columna.</span><span class="sxs-lookup"><span data-stu-id="431a5-671">The column value cannot be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-672">JET_errIndexInUse</span><span class="sxs-lookup"><span data-stu-id="431a5-672">JET_errIndexInUse</span></span><br />
<span data-ttu-id="431a5-673">-1051</span><span class="sxs-lookup"><span data-stu-id="431a5-673">-1051</span></span></p></td>
<td><p><span data-ttu-id="431a5-674">El índice está en uso.</span><span class="sxs-lookup"><span data-stu-id="431a5-674">The index is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-675">JET_errLinkNotSupported</span><span class="sxs-lookup"><span data-stu-id="431a5-675">JET_errLinkNotSupported</span></span><br />
<span data-ttu-id="431a5-676">-1052</span><span class="sxs-lookup"><span data-stu-id="431a5-676">-1052</span></span></p></td>
<td><p><span data-ttu-id="431a5-677">La compatibilidad con vínculos no está disponible.</span><span class="sxs-lookup"><span data-stu-id="431a5-677">The link support is unavailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-678">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="431a5-678">JET_errNullKeyDisallowed</span></span><br />
<span data-ttu-id="431a5-679">-1053</span><span class="sxs-lookup"><span data-stu-id="431a5-679">-1053</span></span></p></td>
<td><p><span data-ttu-id="431a5-680">No se permiten claves null en un índice.</span><span class="sxs-lookup"><span data-stu-id="431a5-680">Null keys are not allowed on an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-681">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="431a5-681">JET_errNotInTransaction</span></span><br />
<span data-ttu-id="431a5-682">-1054</span><span class="sxs-lookup"><span data-stu-id="431a5-682">-1054</span></span></p></td>
<td><p><span data-ttu-id="431a5-683">La operación debe realizarse dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="431a5-683">The operation must occur within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-684">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="431a5-684">JET_errTooManyActiveUsers</span></span><br />
<span data-ttu-id="431a5-685">-1059</span><span class="sxs-lookup"><span data-stu-id="431a5-685">-1059</span></span></p></td>
<td><p><span data-ttu-id="431a5-686">Hay demasiados usuarios de base de datos activos</span><span class="sxs-lookup"><span data-stu-id="431a5-686">There are too many active database users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-687">JET_errInvalidCountry</span><span class="sxs-lookup"><span data-stu-id="431a5-687">JET_errInvalidCountry</span></span><br />
<span data-ttu-id="431a5-688">-1061</span><span class="sxs-lookup"><span data-stu-id="431a5-688">-1061</span></span></p></td>
<td><p><span data-ttu-id="431a5-689">Hay un código de país no válido o desconocido.</span><span class="sxs-lookup"><span data-stu-id="431a5-689">There is an invalid or unknown country code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-690">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="431a5-690">JET_errInvalidLanguageId</span></span><br />
<span data-ttu-id="431a5-691">-1062</span><span class="sxs-lookup"><span data-stu-id="431a5-691">-1062</span></span></p></td>
<td><p><span data-ttu-id="431a5-692">Hay un ID. de idioma no válido o desconocido.</span><span class="sxs-lookup"><span data-stu-id="431a5-692">There is an invalid or unknown language ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-693">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="431a5-693">JET_errInvalidCodePage</span></span><br />
<span data-ttu-id="431a5-694">-1063</span><span class="sxs-lookup"><span data-stu-id="431a5-694">-1063</span></span></p></td>
<td><p><span data-ttu-id="431a5-695">Hay una página de códigos no válida o desconocida.</span><span class="sxs-lookup"><span data-stu-id="431a5-695">There is an invalid or unknown code page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-696">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="431a5-696">JET_errInvalidLCMapStringFlags</span></span><br />
<span data-ttu-id="431a5-697">-1064</span><span class="sxs-lookup"><span data-stu-id="431a5-697">-1064</span></span></p></td>
<td><p><span data-ttu-id="431a5-698">Hay marcas no válidas que se usan para <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</span><span class="sxs-lookup"><span data-stu-id="431a5-698">There are invalid flags being used for <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-699">JET_errVersionStoreEntryTooBig</span><span class="sxs-lookup"><span data-stu-id="431a5-699">JET_errVersionStoreEntryTooBig</span></span><br />
<span data-ttu-id="431a5-700">-1065</span><span class="sxs-lookup"><span data-stu-id="431a5-700">-1065</span></span></p></td>
<td><p><span data-ttu-id="431a5-701">Se produjo un intento de crear una entrada de almacén de versiones (RCE) más grande que un depósito de versión.</span><span class="sxs-lookup"><span data-stu-id="431a5-701">There was an attempt to create a version store entry (RCE) that was larger than a version bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="431a5-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span></span><br />
<span data-ttu-id="431a5-703">-1066</span><span class="sxs-lookup"><span data-stu-id="431a5-703">-1066</span></span></p></td>
<td><p><span data-ttu-id="431a5-704">El almacén de versiones no tiene memoria y no se pudo completar el intento de limpieza.</span><span class="sxs-lookup"><span data-stu-id="431a5-704">The version store is out of memory and the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-705">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="431a5-705">JET_errVersionStoreOutOfMemory</span></span><br />
<span data-ttu-id="431a5-706">-1069</span><span class="sxs-lookup"><span data-stu-id="431a5-706">-1069</span></span></p></td>
<td><p><span data-ttu-id="431a5-707">El almacén de versiones no tiene memoria y ya se intentó realizar una limpieza).</span><span class="sxs-lookup"><span data-stu-id="431a5-707">The version store is out of memory and a cleanup was already attempted).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-708">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="431a5-708">JET_errCannotIndex</span></span><br />
<span data-ttu-id="431a5-709">-1071</span><span class="sxs-lookup"><span data-stu-id="431a5-709">-1071</span></span></p></td>
<td><p><span data-ttu-id="431a5-710">Las columnas custodia y SLV no se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="431a5-710">The escrow and SLV columns cannot be indexed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-711">JET_errRecordNotDeleted</span><span class="sxs-lookup"><span data-stu-id="431a5-711">JET_errRecordNotDeleted</span></span><br />
<span data-ttu-id="431a5-712">-1072</span><span class="sxs-lookup"><span data-stu-id="431a5-712">-1072</span></span></p></td>
<td><p><span data-ttu-id="431a5-713">El registro no se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="431a5-713">The record has not been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-714">JET_errTooManyMempoolEntries</span><span class="sxs-lookup"><span data-stu-id="431a5-714">JET_errTooManyMempoolEntries</span></span><br />
<span data-ttu-id="431a5-715">-1073</span><span class="sxs-lookup"><span data-stu-id="431a5-715">-1073</span></span></p></td>
<td><p><span data-ttu-id="431a5-716">Se han solicitado demasiadas entradas de mempool.</span><span class="sxs-lookup"><span data-stu-id="431a5-716">Too many mempool entries have been requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-717">JET_errOutOfObjectIDs</span><span class="sxs-lookup"><span data-stu-id="431a5-717">JET_errOutOfObjectIDs</span></span><br />
<span data-ttu-id="431a5-718">-1074</span><span class="sxs-lookup"><span data-stu-id="431a5-718">-1074</span></span></p></td>
<td><p><span data-ttu-id="431a5-719">La base de datos está fuera del árbol de objectId B +, por lo que se debe realizar una desfragmentación sin conexión para reclamar el objectId liberado o no utilizado.</span><span class="sxs-lookup"><span data-stu-id="431a5-719">The database is out of B+ tree ObjectIDs so an offline defragmentation must be performed to reclaim freed or unused ObjectIds.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-720">JET_errOutOfLongValueIDs</span><span class="sxs-lookup"><span data-stu-id="431a5-720">JET_errOutOfLongValueIDs</span></span><br />
<span data-ttu-id="431a5-721">-1075</span><span class="sxs-lookup"><span data-stu-id="431a5-721">-1075</span></span></p></td>
<td><p><span data-ttu-id="431a5-722">El contador de identificador de valor largo ha alcanzado el valor máximo.</span><span class="sxs-lookup"><span data-stu-id="431a5-722">The Long-value ID counter has reached the maximum value.</span></span> <span data-ttu-id="431a5-723">Se debe realizar una desfragmentación sin conexión para reclamar LongValueIDs libres o sin usar.</span><span class="sxs-lookup"><span data-stu-id="431a5-723">An offline defragmentation must be performed to reclaim free or unused LongValueIDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-724">JET_errOutOfAutoincrementValues</span><span class="sxs-lookup"><span data-stu-id="431a5-724">JET_errOutOfAutoincrementValues</span></span><br />
<span data-ttu-id="431a5-725">-1076</span><span class="sxs-lookup"><span data-stu-id="431a5-725">-1076</span></span></p></td>
<td><p><span data-ttu-id="431a5-726">El contador de incremento automático ha alcanzado el valor máximo.</span><span class="sxs-lookup"><span data-stu-id="431a5-726">The auto-increment counter has reached the maximum value.</span></span> <span data-ttu-id="431a5-727">Una desfragmentación sin conexión no podrá recuperar valores de incremento automático gratuitos o no usados).</span><span class="sxs-lookup"><span data-stu-id="431a5-727">An offline defragmentation will not be able to reclaim free or unused auto-increment values).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-728">JET_errOutOfDbtimeValues</span><span class="sxs-lookup"><span data-stu-id="431a5-728">JET_errOutOfDbtimeValues</span></span><br />
<span data-ttu-id="431a5-729">-1077</span><span class="sxs-lookup"><span data-stu-id="431a5-729">-1077</span></span></p></td>
<td><p><span data-ttu-id="431a5-730">El contador dbTime ha alcanzado el valor máximo.</span><span class="sxs-lookup"><span data-stu-id="431a5-730">The Dbtime counter has reached the maximum value.</span></span> <span data-ttu-id="431a5-731">Se debe realizar una desfragmentación sin conexión para recuperar los valores de dbTime libres o no usados.</span><span class="sxs-lookup"><span data-stu-id="431a5-731">An offline defragmentation must be performed to reclaim free or unused Dbtime values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-732">JET_errOutOfSequentialIndexValues</span><span class="sxs-lookup"><span data-stu-id="431a5-732">JET_errOutOfSequentialIndexValues</span></span><br />
<span data-ttu-id="431a5-733">-1078</span><span class="sxs-lookup"><span data-stu-id="431a5-733">-1078</span></span></p></td>
<td><p><span data-ttu-id="431a5-734">Un contador de índice secuencial ha alcanzado el valor máximo.</span><span class="sxs-lookup"><span data-stu-id="431a5-734">A sequential index counter has reached the maximum value.</span></span> <span data-ttu-id="431a5-735">Se debe realizar una desfragmentación sin conexión para recuperar los valores de SequentialIndex libres o no usados.</span><span class="sxs-lookup"><span data-stu-id="431a5-735">An offline defragmentation must be performed to reclaim free or unused SequentialIndex values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-736">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="431a5-736">JET_errRunningInOneInstanceMode</span></span><br />
<span data-ttu-id="431a5-737">-1080</span><span class="sxs-lookup"><span data-stu-id="431a5-737">-1080</span></span></p></td>
<td><p><span data-ttu-id="431a5-738">Esta llamada de varias instancias tiene habilitado el modo de instancia única.</span><span class="sxs-lookup"><span data-stu-id="431a5-738">This multi-instance call has the single-instance mode enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-739">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="431a5-739">JET_errRunningInMultiInstanceMode</span></span><br />
<span data-ttu-id="431a5-740">-1081</span><span class="sxs-lookup"><span data-stu-id="431a5-740">-1081</span></span></p></td>
<td><p><span data-ttu-id="431a5-741">Esta llamada de instancia única tiene el modo de varias instancias habilitado.</span><span class="sxs-lookup"><span data-stu-id="431a5-741">This single-instance call has the multi-instance mode enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-742">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="431a5-742">JET_errSystemParamsAlreadySet</span></span><br />
<span data-ttu-id="431a5-743">-1082</span><span class="sxs-lookup"><span data-stu-id="431a5-743">-1082</span></span></p></td>
<td><p><span data-ttu-id="431a5-744">Ya se han establecido los parámetros globales del sistema.</span><span class="sxs-lookup"><span data-stu-id="431a5-744">The global system parameters have already been set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-745">JET_errSystemPathInUse</span><span class="sxs-lookup"><span data-stu-id="431a5-745">JET_errSystemPathInUse</span></span><br />
<span data-ttu-id="431a5-746">-1083</span><span class="sxs-lookup"><span data-stu-id="431a5-746">-1083</span></span></p></td>
<td><p><span data-ttu-id="431a5-747">La ruta de acceso del sistema ya está siendo utilizada por otra instancia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-747">The system path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-748">JET_errLogFilePathInUse</span><span class="sxs-lookup"><span data-stu-id="431a5-748">JET_errLogFilePathInUse</span></span><br />
<span data-ttu-id="431a5-749">-1084</span><span class="sxs-lookup"><span data-stu-id="431a5-749">-1084</span></span></p></td>
<td><p><span data-ttu-id="431a5-750">Otra instancia de base de datos ya está usando la ruta de acceso al archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="431a5-750">The log file path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-751">JET_errTempPathInUse</span><span class="sxs-lookup"><span data-stu-id="431a5-751">JET_errTempPathInUse</span></span><br />
<span data-ttu-id="431a5-752">-1085</span><span class="sxs-lookup"><span data-stu-id="431a5-752">-1085</span></span></p></td>
<td><p><span data-ttu-id="431a5-753">La ruta de acceso a la base de datos temporal ya está siendo utilizada por otra instancia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-753">The path to the temporary database is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-754">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="431a5-754">JET_errInstanceNameInUse</span></span><br />
<span data-ttu-id="431a5-755">-1086</span><span class="sxs-lookup"><span data-stu-id="431a5-755">-1086</span></span></p></td>
<td><p><span data-ttu-id="431a5-756">El nombre de instancia ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="431a5-756">The instance name is already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-757">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="431a5-757">JET_errInstanceUnavailable</span></span><br />
<span data-ttu-id="431a5-758">-1090</span><span class="sxs-lookup"><span data-stu-id="431a5-758">-1090</span></span></p></td>
<td><p><span data-ttu-id="431a5-759">Esta instancia no se puede usar porque encontró un error irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="431a5-759">This instance cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-760">JET_errDatabaseUnavailable</span><span class="sxs-lookup"><span data-stu-id="431a5-760">JET_errDatabaseUnavailable</span></span><br />
<span data-ttu-id="431a5-761">-1091</span><span class="sxs-lookup"><span data-stu-id="431a5-761">-1091</span></span></p></td>
<td><p><span data-ttu-id="431a5-762">No se puede usar esta base de datos porque se ha producido un error irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="431a5-762">This database cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="431a5-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span></span><br />
<span data-ttu-id="431a5-764">-1092</span><span class="sxs-lookup"><span data-stu-id="431a5-764">-1092</span></span></p></td>
<td><p><span data-ttu-id="431a5-765">Esta instancia no se puede usar porque encontró un error de registro de disco completo al realizar una operación (por ejemplo, una reversión de la transacción) que no pudo tolerar el error.</span><span class="sxs-lookup"><span data-stu-id="431a5-765">This instance cannot be used because it encountered a log-disk-full error while performing an operation (such as a transaction rollback) that could not tolerate failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-766">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="431a5-766">JET_errOutOfSessions</span></span><br />
<span data-ttu-id="431a5-767">-1101</span><span class="sxs-lookup"><span data-stu-id="431a5-767">-1101</span></span></p></td>
<td><p><span data-ttu-id="431a5-768">La base de datos no tiene sesiones.</span><span class="sxs-lookup"><span data-stu-id="431a5-768">The database is out of sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-769">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="431a5-769">JET_errWriteConflict</span></span><br />
<span data-ttu-id="431a5-770">-1102</span><span class="sxs-lookup"><span data-stu-id="431a5-770">-1102</span></span></p></td>
<td><p><span data-ttu-id="431a5-771">Error en el bloqueo de escritura debido a la existencia de un bloqueo de escritura pendiente.</span><span class="sxs-lookup"><span data-stu-id="431a5-771">The write lock failed due to the existence of an outstanding write lock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-772">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="431a5-772">JET_errTransTooDeep</span></span><br />
<span data-ttu-id="431a5-773">-1103</span><span class="sxs-lookup"><span data-stu-id="431a5-773">-1103</span></span></p></td>
<td><p><span data-ttu-id="431a5-774">Las transacciones están demasiado anidadas.</span><span class="sxs-lookup"><span data-stu-id="431a5-774">The transactions are nested too deeply.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-775">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="431a5-775">JET_errInvalidSesid</span></span><br />
<span data-ttu-id="431a5-776">-1104</span><span class="sxs-lookup"><span data-stu-id="431a5-776">-1104</span></span></p></td>
<td><p><span data-ttu-id="431a5-777">Hay un identificador de sesión no válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-777">There is an invalid session handle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-778">JET_errWriteConflictPrimaryIndex</span><span class="sxs-lookup"><span data-stu-id="431a5-778">JET_errWriteConflictPrimaryIndex</span></span><br />
<span data-ttu-id="431a5-779">-1105</span><span class="sxs-lookup"><span data-stu-id="431a5-779">-1105</span></span></p></td>
<td><p><span data-ttu-id="431a5-780">Se intentó realizar una actualización en un índice principal no confirmado.</span><span class="sxs-lookup"><span data-stu-id="431a5-780">An update was attempted on an uncommitted primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-781">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="431a5-781">JET_errInTransaction</span></span><br />
<span data-ttu-id="431a5-782">-1108</span><span class="sxs-lookup"><span data-stu-id="431a5-782">-1108</span></span></p></td>
<td><p><span data-ttu-id="431a5-783">No se permite la operación dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="431a5-783">The operation is not allowed within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-784">JET_errRollbackRequired</span><span class="sxs-lookup"><span data-stu-id="431a5-784">JET_errRollbackRequired</span></span><br />
<span data-ttu-id="431a5-785">-1109</span><span class="sxs-lookup"><span data-stu-id="431a5-785">-1109</span></span></p></td>
<td><p><span data-ttu-id="431a5-786">Se debe revertir la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="431a5-786">The current transaction must be rolled back.</span></span> <span data-ttu-id="431a5-787">No se puede confirmar y no se puede iniciar una nueva.</span><span class="sxs-lookup"><span data-stu-id="431a5-787">It cannot be committed and a new one cannot be started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-788">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="431a5-788">JET_errTransReadOnly</span></span><br />
<span data-ttu-id="431a5-789">-1110</span><span class="sxs-lookup"><span data-stu-id="431a5-789">-1110</span></span></p></td>
<td><p><span data-ttu-id="431a5-790">Una transacción de solo lectura intentó modificar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-790">A read-only transaction tried to modify the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-791">JET_errSessionWriteConflict</span><span class="sxs-lookup"><span data-stu-id="431a5-791">JET_errSessionWriteConflict</span></span><br />
<span data-ttu-id="431a5-792">-1111</span><span class="sxs-lookup"><span data-stu-id="431a5-792">-1111</span></span></p></td>
<td><p><span data-ttu-id="431a5-793">Se intentó reemplazar el mismo registro por dos cursores diferentes en la misma sesión.</span><span class="sxs-lookup"><span data-stu-id="431a5-793">There was an attempt to replace the same record by two different cursors in the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-794">JET_errRecordTooBigForBackwardCompatibility</span><span class="sxs-lookup"><span data-stu-id="431a5-794">JET_errRecordTooBigForBackwardCompatibility</span></span><br />
<span data-ttu-id="431a5-795">-1112</span><span class="sxs-lookup"><span data-stu-id="431a5-795">-1112</span></span></p></td>
<td><p><span data-ttu-id="431a5-796">El registro sería demasiado grande si se representa en un formato de base de datos de una versión anterior de jet.</span><span class="sxs-lookup"><span data-stu-id="431a5-796">The record would be too big if represented in a database format from a previous version of Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-797">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="431a5-797">JET_errCannotMaterializeForwardOnlySort</span></span><br />
<span data-ttu-id="431a5-798">-1113</span><span class="sxs-lookup"><span data-stu-id="431a5-798">-1113</span></span></p></td>
<td><p><span data-ttu-id="431a5-799">No se pudo crear la tabla temporal debido a los parámetros que entran en conflicto con JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="431a5-799">The temporary table could not be created due to parameters that conflict with JET_bitTTForwardOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-800">JET_errSesidTableIdMismatch</span><span class="sxs-lookup"><span data-stu-id="431a5-800">JET_errSesidTableIdMismatch</span></span><br />
<span data-ttu-id="431a5-801">-1114</span><span class="sxs-lookup"><span data-stu-id="431a5-801">-1114</span></span></p></td>
<td><p><span data-ttu-id="431a5-802">No se puede usar el identificador de sesión con el ID. de tabla porque no se usó para crearlo.</span><span class="sxs-lookup"><span data-stu-id="431a5-802">The session handle cannot be used with the table id because it was not used to create it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-803">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="431a5-803">JET_errInvalidInstance</span></span><br />
<span data-ttu-id="431a5-804">-1115</span><span class="sxs-lookup"><span data-stu-id="431a5-804">-1115</span></span></p></td>
<td><p><span data-ttu-id="431a5-805">El identificador de instancia no es válido o hace referencia a una instancia de que se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="431a5-805">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-806">JET_errReadLostFlushVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="431a5-806">JET_errReadLostFlushVerifyFailure</span></span><br />
<span data-ttu-id="431a5-807">-1119</span><span class="sxs-lookup"><span data-stu-id="431a5-807">-1119</span></span></p></td>
<td><p><span data-ttu-id="431a5-808">La página de la base de datos leída del disco tenía una escritura anterior no representada en la página.</span><span class="sxs-lookup"><span data-stu-id="431a5-808">The database page read from disk had a previous write not represented on the page.</span></span> <span data-ttu-id="431a5-809">Disponible en Windows 8 y versiones posteriores para el cliente de, y Windows Server 2012 y versiones posteriores para el servidor de.</span><span class="sxs-lookup"><span data-stu-id="431a5-809">Available on Windows 8 and later for client, and Windows Server 2012 and later for server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-810">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="431a5-810">JET_errDatabaseDuplicate</span></span><br />
<span data-ttu-id="431a5-811">-1201</span><span class="sxs-lookup"><span data-stu-id="431a5-811">-1201</span></span></p></td>
<td><p><span data-ttu-id="431a5-812">La base de datos ya existe.</span><span class="sxs-lookup"><span data-stu-id="431a5-812">The database already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-813">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="431a5-813">JET_errDatabaseInUse</span></span><br />
<span data-ttu-id="431a5-814">-1202</span><span class="sxs-lookup"><span data-stu-id="431a5-814">-1202</span></span></p></td>
<td><p><span data-ttu-id="431a5-815">La base de datos en uso.</span><span class="sxs-lookup"><span data-stu-id="431a5-815">The database in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-816">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="431a5-816">JET_errDatabaseNotFound</span></span><br />
<span data-ttu-id="431a5-817">-1203</span><span class="sxs-lookup"><span data-stu-id="431a5-817">-1203</span></span></p></td>
<td><p><span data-ttu-id="431a5-818">No existe dicha base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-818">There is no such database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-819">JET_errDatabaseInvalidName</span><span class="sxs-lookup"><span data-stu-id="431a5-819">JET_errDatabaseInvalidName</span></span><br />
<span data-ttu-id="431a5-820">-1204</span><span class="sxs-lookup"><span data-stu-id="431a5-820">-1204</span></span></p></td>
<td><p><span data-ttu-id="431a5-821">El nombre de la base de datos no es válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-821">The database name is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-822">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="431a5-822">JET_errDatabaseInvalidPages</span></span><br />
<span data-ttu-id="431a5-823">-1205</span><span class="sxs-lookup"><span data-stu-id="431a5-823">-1205</span></span></p></td>
<td><p><span data-ttu-id="431a5-824">Hay un número no válido de páginas.</span><span class="sxs-lookup"><span data-stu-id="431a5-824">There are an invalid number of pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-825">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="431a5-825">JET_errDatabaseCorrupted</span></span><br />
<span data-ttu-id="431a5-826">-1206</span><span class="sxs-lookup"><span data-stu-id="431a5-826">-1206</span></span></p></td>
<td><p><span data-ttu-id="431a5-827">Hay un archivo que no es de base de datos o una base de datos dañada.</span><span class="sxs-lookup"><span data-stu-id="431a5-827">There is a non-database file or corrupt database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-828">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="431a5-828">JET_errDatabaseLocked</span></span><br />
<span data-ttu-id="431a5-829">-1207</span><span class="sxs-lookup"><span data-stu-id="431a5-829">-1207</span></span></p></td>
<td><p><span data-ttu-id="431a5-830">La base de datos está bloqueada de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="431a5-830">The database is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-831">JET_errCannotDisableVersioning</span><span class="sxs-lookup"><span data-stu-id="431a5-831">JET_errCannotDisableVersioning</span></span><br />
<span data-ttu-id="431a5-832">-1208</span><span class="sxs-lookup"><span data-stu-id="431a5-832">-1208</span></span></p></td>
<td><p><span data-ttu-id="431a5-833">No se puede deshabilitar el control de versiones de esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-833">The versioning for this database cannot be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-834">JET_errInvalidDatabaseVersion</span><span class="sxs-lookup"><span data-stu-id="431a5-834">JET_errInvalidDatabaseVersion</span></span><br />
<span data-ttu-id="431a5-835">-1209</span><span class="sxs-lookup"><span data-stu-id="431a5-835">-1209</span></span></p></td>
<td><p><span data-ttu-id="431a5-836">El motor de base de datos no es compatible con la base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-836">The database engine is incompatible with the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-837">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="431a5-837">JET_errDatabase200Format</span></span><br />
<span data-ttu-id="431a5-838">-1210</span><span class="sxs-lookup"><span data-stu-id="431a5-838">-1210</span></span></p></td>
<td><p><span data-ttu-id="431a5-839">La base de datos tiene un formato anterior (200).</span><span class="sxs-lookup"><span data-stu-id="431a5-839">The database is in an older (200) format.</span></span> <span data-ttu-id="431a5-840"><a href="gg294068(v=exchg.10).md">JetInit</a> devuelve este error si se establece <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> .</span><span class="sxs-lookup"><span data-stu-id="431a5-840">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="431a5-841">Solo cliente de Windows NT.</span><span class="sxs-lookup"><span data-stu-id="431a5-841">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-842">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="431a5-842">JET_errDatabase400Format</span></span><br />
<span data-ttu-id="431a5-843">-1211</span><span class="sxs-lookup"><span data-stu-id="431a5-843">-1211</span></span></p></td>
<td><p><span data-ttu-id="431a5-844">La base de datos tiene un formato anterior (400).</span><span class="sxs-lookup"><span data-stu-id="431a5-844">The database is in an older (400) format.</span></span> <span data-ttu-id="431a5-845"><a href="gg294068(v=exchg.10).md">JetInit</a> devuelve este error si se establece <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> .</span><span class="sxs-lookup"><span data-stu-id="431a5-845">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="431a5-846">Solo cliente de Windows NT.</span><span class="sxs-lookup"><span data-stu-id="431a5-846">Windows NT client only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-847">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="431a5-847">JET_errDatabase500Format</span></span><br />
<span data-ttu-id="431a5-848">-1212</span><span class="sxs-lookup"><span data-stu-id="431a5-848">-1212</span></span></p></td>
<td><p><span data-ttu-id="431a5-849">La base de datos tiene un formato anterior (500).</span><span class="sxs-lookup"><span data-stu-id="431a5-849">The database is in an older (500) format.</span></span> <span data-ttu-id="431a5-850"><a href="gg294068(v=exchg.10).md">JetInit</a> devuelve este error si se establece <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> .</span><span class="sxs-lookup"><span data-stu-id="431a5-850">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="431a5-851">Solo cliente de Windows NT.</span><span class="sxs-lookup"><span data-stu-id="431a5-851">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-852">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="431a5-852">JET_errPageSizeMismatch</span></span><br />
<span data-ttu-id="431a5-853">-1213</span><span class="sxs-lookup"><span data-stu-id="431a5-853">-1213</span></span></p></td>
<td><p><span data-ttu-id="431a5-854">El tamaño de página de la base de datos no coincide con el motor.</span><span class="sxs-lookup"><span data-stu-id="431a5-854">The database page size does not match the engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-855">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="431a5-855">JET_errTooManyInstances</span></span><br />
<span data-ttu-id="431a5-856">-1214</span><span class="sxs-lookup"><span data-stu-id="431a5-856">-1214</span></span></p></td>
<td><p><span data-ttu-id="431a5-857">No se pueden iniciar más instancias de base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-857">No more database instances can be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-858">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="431a5-858">JET_errDatabaseSharingViolation</span></span><br />
<span data-ttu-id="431a5-859">-1215</span><span class="sxs-lookup"><span data-stu-id="431a5-859">-1215</span></span></p></td>
<td><p><span data-ttu-id="431a5-860">Una instancia de base de datos diferente utiliza esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-860">A different database instance is using this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-861">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="431a5-861">JET_errAttachedDatabaseMismatch</span></span><br />
<span data-ttu-id="431a5-862">-1216</span><span class="sxs-lookup"><span data-stu-id="431a5-862">-1216</span></span></p></td>
<td><p><span data-ttu-id="431a5-863">Se detectaron datos adjuntos de base de datos pendientes al principio o al final de la recuperación, pero falta la base de datos o no coincide con la información de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="431a5-863">An outstanding database attachment has been detected at the start or end of the recovery, but the database is missing or does not match attachment info.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-864">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="431a5-864">JET_errDatabaseInvalidPath</span></span><br />
<span data-ttu-id="431a5-865">-1217</span><span class="sxs-lookup"><span data-stu-id="431a5-865">-1217</span></span></p></td>
<td><p><span data-ttu-id="431a5-866">La ruta de acceso especificada al archivo de base de datos no es válida.</span><span class="sxs-lookup"><span data-stu-id="431a5-866">The specified path to the database file is illegal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-867">JET_errDatabaseIdInUse</span><span class="sxs-lookup"><span data-stu-id="431a5-867">JET_errDatabaseIdInUse</span></span><br />
<span data-ttu-id="431a5-868">-1218</span><span class="sxs-lookup"><span data-stu-id="431a5-868">-1218</span></span></p></td>
<td><p><span data-ttu-id="431a5-869">A una base de datos se le asigna un identificador que ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="431a5-869">A database is being assigned an ID that is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-870">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="431a5-870">JET_errForceDetachNotAllowed</span></span><br />
<span data-ttu-id="431a5-871">-1219</span><span class="sxs-lookup"><span data-stu-id="431a5-871">-1219</span></span></p></td>
<td><p><span data-ttu-id="431a5-872">Se permite la desasociación forzada solo después de que se detuviera la desasociación normal debido a un error.</span><span class="sxs-lookup"><span data-stu-id="431a5-872">The force detach is allowed only after the normal detach was stopped due to an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-873">JET_errCatalogCorrupted</span><span class="sxs-lookup"><span data-stu-id="431a5-873">JET_errCatalogCorrupted</span></span><br />
<span data-ttu-id="431a5-874">-1220</span><span class="sxs-lookup"><span data-stu-id="431a5-874">-1220</span></span></p></td>
<td><p><span data-ttu-id="431a5-875">Se detectaron daños en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="431a5-875">Corruption was detected in the catalog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-876">JET_errPartiallyAttachedDB</span><span class="sxs-lookup"><span data-stu-id="431a5-876">JET_errPartiallyAttachedDB</span></span><br />
<span data-ttu-id="431a5-877">-1221</span><span class="sxs-lookup"><span data-stu-id="431a5-877">-1221</span></span></p></td>
<td><p><span data-ttu-id="431a5-878">La base de datos solo está parcialmente adjunta y no se puede completar la operación de adjuntar.</span><span class="sxs-lookup"><span data-stu-id="431a5-878">The database is only partially attached and the attach operation cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-879">JET_errDatabaseSignInUse</span><span class="sxs-lookup"><span data-stu-id="431a5-879">JET_errDatabaseSignInUse</span></span><br />
<span data-ttu-id="431a5-880">-1222</span><span class="sxs-lookup"><span data-stu-id="431a5-880">-1222</span></span></p></td>
<td><p><span data-ttu-id="431a5-881">La base de datos con la misma firma ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="431a5-881">The database with the same signature is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-882">JET_errDatabaseCorruptedNoRepair</span><span class="sxs-lookup"><span data-stu-id="431a5-882">JET_errDatabaseCorruptedNoRepair</span></span><br />
<span data-ttu-id="431a5-883">-1224</span><span class="sxs-lookup"><span data-stu-id="431a5-883">-1224</span></span></p></td>
<td><p><span data-ttu-id="431a5-884">La base de datos está dañada, pero no se permite una reparación.</span><span class="sxs-lookup"><span data-stu-id="431a5-884">The database is corrupted but a repair is not allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-885">JET_errInvalidCreateDbVersion</span><span class="sxs-lookup"><span data-stu-id="431a5-885">JET_errInvalidCreateDbVersion</span></span><br />
<span data-ttu-id="431a5-886">-1225</span><span class="sxs-lookup"><span data-stu-id="431a5-886">-1225</span></span></p></td>
<td><p><span data-ttu-id="431a5-887">El motor de base de datos intentó reproducir una operación de creación de base de datos desde el registro de transacciones, pero se produjo un error debido a una versión incompatible de esa operación.</span><span class="sxs-lookup"><span data-stu-id="431a5-887">The database engine attempted to replay a Create Database operation from the transaction log but failed due to an incompatible version of that operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-888">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="431a5-888">JET_errTableLocked</span></span><br />
<span data-ttu-id="431a5-889">-1302</span><span class="sxs-lookup"><span data-stu-id="431a5-889">-1302</span></span></p></td>
<td><p><span data-ttu-id="431a5-890">La tabla está bloqueada de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="431a5-890">The table is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-891">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="431a5-891">JET_errTableDuplicate</span></span><br />
<span data-ttu-id="431a5-892">-1303</span><span class="sxs-lookup"><span data-stu-id="431a5-892">-1303</span></span></p></td>
<td><p><span data-ttu-id="431a5-893">La tabla ya existe.</span><span class="sxs-lookup"><span data-stu-id="431a5-893">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-894">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="431a5-894">JET_errTableInUse</span></span><br />
<span data-ttu-id="431a5-895">-1304</span><span class="sxs-lookup"><span data-stu-id="431a5-895">-1304</span></span></p></td>
<td><p><span data-ttu-id="431a5-896">La tabla está en uso y no se puede bloquear.</span><span class="sxs-lookup"><span data-stu-id="431a5-896">The table is in use and cannot be locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-897">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="431a5-897">JET_errObjectNotFound</span></span><br />
<span data-ttu-id="431a5-898">-1305</span><span class="sxs-lookup"><span data-stu-id="431a5-898">-1305</span></span></p></td>
<td><p><span data-ttu-id="431a5-899">No hay ninguna tabla u objeto.</span><span class="sxs-lookup"><span data-stu-id="431a5-899">There is no such table or object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-900">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="431a5-900">JET_errDensityInvalid</span></span><br />
<span data-ttu-id="431a5-901">-1307</span><span class="sxs-lookup"><span data-stu-id="431a5-901">-1307</span></span></p></td>
<td><p><span data-ttu-id="431a5-902">Hay una densidad de índice o archivo incorrecta.</span><span class="sxs-lookup"><span data-stu-id="431a5-902">There is a bad file or index density.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-903">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="431a5-903">JET_errTableNotEmpty</span></span><br />
<span data-ttu-id="431a5-904">-1308</span><span class="sxs-lookup"><span data-stu-id="431a5-904">-1308</span></span></p></td>
<td><p><span data-ttu-id="431a5-905">La tabla no está vacía.</span><span class="sxs-lookup"><span data-stu-id="431a5-905">The table is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-906">JET_errInvalidTableId</span><span class="sxs-lookup"><span data-stu-id="431a5-906">JET_errInvalidTableId</span></span><br />
<span data-ttu-id="431a5-907">-1310</span><span class="sxs-lookup"><span data-stu-id="431a5-907">-1310</span></span></p></td>
<td><p><span data-ttu-id="431a5-908">El ID. de tabla no es válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-908">The table ID is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-909">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="431a5-909">JET_errTooManyOpenTables</span></span><br />
<span data-ttu-id="431a5-910">-1311</span><span class="sxs-lookup"><span data-stu-id="431a5-910">-1311</span></span></p></td>
<td><p><span data-ttu-id="431a5-911">No se pueden abrir más tablas, incluso después de que se ejecute la tarea de limpieza interna.</span><span class="sxs-lookup"><span data-stu-id="431a5-911">No more tables can be opened, even after the internal cleanup task has run.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-912">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="431a5-912">JET_errIllegalOperation</span></span><br />
<span data-ttu-id="431a5-913">-1312</span><span class="sxs-lookup"><span data-stu-id="431a5-913">-1312</span></span></p></td>
<td><p><span data-ttu-id="431a5-914">La operación no se admite en la tabla.</span><span class="sxs-lookup"><span data-stu-id="431a5-914">The operation is not supported on the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="431a5-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span></span><br />
<span data-ttu-id="431a5-916">-1313</span><span class="sxs-lookup"><span data-stu-id="431a5-916">-1313</span></span></p></td>
<td><p><span data-ttu-id="431a5-917">No se pueden abrir más tablas porque no se pudo completar el intento de limpieza.</span><span class="sxs-lookup"><span data-stu-id="431a5-917">No more tables can be opened because the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-918">JET_errObjectDuplicate</span><span class="sxs-lookup"><span data-stu-id="431a5-918">JET_errObjectDuplicate</span></span><br />
<span data-ttu-id="431a5-919">-1314</span><span class="sxs-lookup"><span data-stu-id="431a5-919">-1314</span></span></p></td>
<td><p><span data-ttu-id="431a5-920">El nombre de la tabla o del objeto está en uso.</span><span class="sxs-lookup"><span data-stu-id="431a5-920">The table or object name is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-921">JET_errInvalidObject</span><span class="sxs-lookup"><span data-stu-id="431a5-921">JET_errInvalidObject</span></span><br />
<span data-ttu-id="431a5-922">-1316</span><span class="sxs-lookup"><span data-stu-id="431a5-922">-1316</span></span></p></td>
<td><p><span data-ttu-id="431a5-923">El objeto no es válido para la operación.</span><span class="sxs-lookup"><span data-stu-id="431a5-923">The object is invalid for operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-924">JET_errCannotDeleteTempTable</span><span class="sxs-lookup"><span data-stu-id="431a5-924">JET_errCannotDeleteTempTable</span></span><br />
<span data-ttu-id="431a5-925">-1317</span><span class="sxs-lookup"><span data-stu-id="431a5-925">-1317</span></span></p></td>
<td><p><span data-ttu-id="431a5-926">Se debe utilizar <a href="gg294087(v=exchg.10).md">JetCloseTable</a> en lugar de <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> para eliminar una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="431a5-926"><a href="gg294087(v=exchg.10).md">JetCloseTable</a> must be used instead of <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> to delete a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-927">JET_errCannotDeleteSystemTable</span><span class="sxs-lookup"><span data-stu-id="431a5-927">JET_errCannotDeleteSystemTable</span></span><br />
<span data-ttu-id="431a5-928">-1318</span><span class="sxs-lookup"><span data-stu-id="431a5-928">-1318</span></span></p></td>
<td><p><span data-ttu-id="431a5-929">Se produjo un intento no válido de eliminar una tabla del sistema.</span><span class="sxs-lookup"><span data-stu-id="431a5-929">There was an illegal attempt to delete a system table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-930">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="431a5-930">JET_errCannotDeleteTemplateTable</span></span><br />
<span data-ttu-id="431a5-931">-1319</span><span class="sxs-lookup"><span data-stu-id="431a5-931">-1319</span></span></p></td>
<td><p><span data-ttu-id="431a5-932">Se produjo un intento no válido de eliminar una tabla de plantilla.</span><span class="sxs-lookup"><span data-stu-id="431a5-932">There was an illegal attempt to delete a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-933">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="431a5-933">JET_errExclusiveTableLockRequired</span></span><br />
<span data-ttu-id="431a5-934">-1322</span><span class="sxs-lookup"><span data-stu-id="431a5-934">-1322</span></span></p></td>
<td><p><span data-ttu-id="431a5-935">Debe haber un bloqueo exclusivo en la tabla.</span><span class="sxs-lookup"><span data-stu-id="431a5-935">There must be an exclusive lock on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-936">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="431a5-936">JET_errFixedDDL</span></span><br />
<span data-ttu-id="431a5-937">-1323</span><span class="sxs-lookup"><span data-stu-id="431a5-937">-1323</span></span></p></td>
<td><p><span data-ttu-id="431a5-938">Las operaciones DDL están prohibidas en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="431a5-938">DDL operations are prohibited on this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-939">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="431a5-939">JET_errFixedInheritedDDL</span></span><br />
<span data-ttu-id="431a5-940">-1324</span><span class="sxs-lookup"><span data-stu-id="431a5-940">-1324</span></span></p></td>
<td><p><span data-ttu-id="431a5-941">En una tabla derivada, las operaciones DDL están prohibidas en la parte heredada del DDL.</span><span class="sxs-lookup"><span data-stu-id="431a5-941">On a derived table, DDL operations are prohibited on the inherited portion of the DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-942">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="431a5-942">JET_errCannotNestDDL</span></span><br />
<span data-ttu-id="431a5-943">-1325</span><span class="sxs-lookup"><span data-stu-id="431a5-943">-1325</span></span></p></td>
<td><p><span data-ttu-id="431a5-944">Actualmente no se admite el anidamiento de la DDL jerárquica.</span><span class="sxs-lookup"><span data-stu-id="431a5-944">Nesting the hierarchical DDL is not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-945">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="431a5-945">JET_errDDLNotInheritable</span></span><br />
<span data-ttu-id="431a5-946">-1326</span><span class="sxs-lookup"><span data-stu-id="431a5-946">-1326</span></span></p></td>
<td><p><span data-ttu-id="431a5-947">Se produjo un intento de heredar un DDL de una tabla que no está marcada como tabla de plantillas.</span><span class="sxs-lookup"><span data-stu-id="431a5-947">There was an attempt to inherit a DDL from a table that is not marked as a template table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-948">JET_errInvalidSettings</span><span class="sxs-lookup"><span data-stu-id="431a5-948">JET_errInvalidSettings</span></span><br />
<span data-ttu-id="431a5-949">-1328</span><span class="sxs-lookup"><span data-stu-id="431a5-949">-1328</span></span></p></td>
<td><p><span data-ttu-id="431a5-950">Los parámetros del sistema se establecieron incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="431a5-950">The system parameters were set improperly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-951">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="431a5-951">JET_errClientRequestToStopJetService</span></span><br />
<span data-ttu-id="431a5-952">-1329</span><span class="sxs-lookup"><span data-stu-id="431a5-952">-1329</span></span></p></td>
<td><p><span data-ttu-id="431a5-953">El cliente ha solicitado que se detenga el servicio.</span><span class="sxs-lookup"><span data-stu-id="431a5-953">The client has requested that the service be stopped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-954">JET_errCannotAddFixedVarColumnToDerivedTable</span><span class="sxs-lookup"><span data-stu-id="431a5-954">JET_errCannotAddFixedVarColumnToDerivedTable</span></span><br />
<span data-ttu-id="431a5-955">-1330</span><span class="sxs-lookup"><span data-stu-id="431a5-955">-1330</span></span></p></td>
<td><p><span data-ttu-id="431a5-956">La tabla de plantilla se creó con la marca NoFixedVarColumnsInDerivedTables establecida.</span><span class="sxs-lookup"><span data-stu-id="431a5-956">The Template table was created with the NoFixedVarColumnsInDerivedTables flag set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-957">JET_errIndexCantBuild</span><span class="sxs-lookup"><span data-stu-id="431a5-957">JET_errIndexCantBuild</span></span><br />
<span data-ttu-id="431a5-958">-1401</span><span class="sxs-lookup"><span data-stu-id="431a5-958">-1401</span></span></p></td>
<td><p><span data-ttu-id="431a5-959">No se pudo generar el índice.</span><span class="sxs-lookup"><span data-stu-id="431a5-959">The index build failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-960">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="431a5-960">JET_errIndexHasPrimary</span></span><br />
<span data-ttu-id="431a5-961">-1402</span><span class="sxs-lookup"><span data-stu-id="431a5-961">-1402</span></span></p></td>
<td><p><span data-ttu-id="431a5-962">El índice principal ya está definido.</span><span class="sxs-lookup"><span data-stu-id="431a5-962">The primary index is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-963">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="431a5-963">JET_errIndexDuplicate</span></span><br />
<span data-ttu-id="431a5-964">-1403</span><span class="sxs-lookup"><span data-stu-id="431a5-964">-1403</span></span></p></td>
<td><p><span data-ttu-id="431a5-965">El índice ya está definido.</span><span class="sxs-lookup"><span data-stu-id="431a5-965">The index is already defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-966">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="431a5-966">JET_errIndexNotFound</span></span><br />
<span data-ttu-id="431a5-967">-1404</span><span class="sxs-lookup"><span data-stu-id="431a5-967">-1404</span></span></p></td>
<td><p><span data-ttu-id="431a5-968">No existe este tipo de índice.</span><span class="sxs-lookup"><span data-stu-id="431a5-968">There is no such index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-969">JET_errIndexMustStay</span><span class="sxs-lookup"><span data-stu-id="431a5-969">JET_errIndexMustStay</span></span><br />
<span data-ttu-id="431a5-970">-1405</span><span class="sxs-lookup"><span data-stu-id="431a5-970">-1405</span></span></p></td>
<td><p><span data-ttu-id="431a5-971">No se puede eliminar el índice clúster.</span><span class="sxs-lookup"><span data-stu-id="431a5-971">The clustered index cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-972">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="431a5-972">JET_errIndexInvalidDef</span></span><br />
<span data-ttu-id="431a5-973">-1406</span><span class="sxs-lookup"><span data-stu-id="431a5-973">-1406</span></span></p></td>
<td><p><span data-ttu-id="431a5-974">La definición del índice no es válida.</span><span class="sxs-lookup"><span data-stu-id="431a5-974">The index definition is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-975">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="431a5-975">JET_errInvalidCreateIndex</span></span><br />
<span data-ttu-id="431a5-976">-1409</span><span class="sxs-lookup"><span data-stu-id="431a5-976">-1409</span></span></p></td>
<td><p><span data-ttu-id="431a5-977">La creación de la descripción del índice no era válida.</span><span class="sxs-lookup"><span data-stu-id="431a5-977">The creation of the index description was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-978">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="431a5-978">JET_errTooManyOpenIndexes</span></span><br />
<span data-ttu-id="431a5-979">-1410</span><span class="sxs-lookup"><span data-stu-id="431a5-979">-1410</span></span></p></td>
<td><p><span data-ttu-id="431a5-980">La base de datos está fuera de los bloques de Descripción del índice.</span><span class="sxs-lookup"><span data-stu-id="431a5-980">The database is out of index description blocks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-981">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="431a5-981">JET_errMultiValuedIndexViolation</span></span><br />
<span data-ttu-id="431a5-982">-1411</span><span class="sxs-lookup"><span data-stu-id="431a5-982">-1411</span></span></p></td>
<td><p><span data-ttu-id="431a5-983">Se han generado claves de índice entre registros no únicas para un índice con varios valores.</span><span class="sxs-lookup"><span data-stu-id="431a5-983">Non-unique inter-record index keys have been generated for a multi-valued index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-984">JET_errIndexBuildCorrupted</span><span class="sxs-lookup"><span data-stu-id="431a5-984">JET_errIndexBuildCorrupted</span></span><br />
<span data-ttu-id="431a5-985">-1412</span><span class="sxs-lookup"><span data-stu-id="431a5-985">-1412</span></span></p></td>
<td><p><span data-ttu-id="431a5-986">Un índice secundario que refleja correctamente el índice principal no se pudo compilar.</span><span class="sxs-lookup"><span data-stu-id="431a5-986">A secondary index that properly reflects the primary index failed to build.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-987">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="431a5-987">JET_errPrimaryIndexCorrupted</span></span><br />
<span data-ttu-id="431a5-988">-1413</span><span class="sxs-lookup"><span data-stu-id="431a5-988">-1413</span></span></p></td>
<td><p><span data-ttu-id="431a5-989">El índice principal está dañado y se debe desfragmentar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-989">The primary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-990">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="431a5-990">JET_errSecondaryIndexCorrupted</span></span><br />
<span data-ttu-id="431a5-991">-1414</span><span class="sxs-lookup"><span data-stu-id="431a5-991">-1414</span></span></p></td>
<td><p><span data-ttu-id="431a5-992">El índice secundario está dañado y se debe desfragmentar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="431a5-992">The secondary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-993">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="431a5-993">JET_errInvalidIndexId</span></span><br />
<span data-ttu-id="431a5-994">-1416</span><span class="sxs-lookup"><span data-stu-id="431a5-994">-1416</span></span></p></td>
<td><p><span data-ttu-id="431a5-995">El ID. de índice no es válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-995">The index ID is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-996">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="431a5-996">JET_errIndexTuplesSecondaryIndexOnly</span></span><br />
<span data-ttu-id="431a5-997">-1430</span><span class="sxs-lookup"><span data-stu-id="431a5-997">-1430</span></span></p></td>
<td><p><span data-ttu-id="431a5-998">El índice de tupla solo se puede establecer en un índice secundario.</span><span class="sxs-lookup"><span data-stu-id="431a5-998">The tuple index can only be set on a secondary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-999">JET_errIndexTuplesTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="431a5-999">JET_errIndexTuplesTooManyColumns</span></span><br />
<span data-ttu-id="431a5-1000">-1431</span><span class="sxs-lookup"><span data-stu-id="431a5-1000">-1431</span></span></p></td>
<td><p><span data-ttu-id="431a5-1001">La definición de índice para el índice de tupla contiene más columnas de clave que el motor de base de datos puede admitir.</span><span class="sxs-lookup"><span data-stu-id="431a5-1001">The index definition for the tuple index contains more key columns that the database engine can support.</span></span></p>
<p><span data-ttu-id="431a5-1002"><strong>Nota:  </strong> El error de JET_errIndexTuplesOneColumnOnly está obsoleto y se ha reemplazado por JET_errIndexTuplesTooManyColumns.</span><span class="sxs-lookup"><span data-stu-id="431a5-1002"><strong>Note  </strong>The JET_errIndexTuplesOneColumnOnly error is obsolete and has been replaced by JET_errIndexTuplesTooManyColumns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1003">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="431a5-1003">JET_errIndexTuplesNonUniqueOnly</span></span><br />
<span data-ttu-id="431a5-1004">-1432</span><span class="sxs-lookup"><span data-stu-id="431a5-1004">-1432</span></span></p></td>
<td><p><span data-ttu-id="431a5-1005">El índice de tupla debe ser un índice no único.</span><span class="sxs-lookup"><span data-stu-id="431a5-1005">The tuple index must be a non-unique index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="431a5-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span></span><br />
<span data-ttu-id="431a5-1007">-1433</span><span class="sxs-lookup"><span data-stu-id="431a5-1007">-1433</span></span></p></td>
<td><p><span data-ttu-id="431a5-1008">Una definición de índice de tupla solo puede contener columnas de clave que tengan tipos de columna de texto o binarios.</span><span class="sxs-lookup"><span data-stu-id="431a5-1008">A tuple index definition can only contain key columns that have text or binary column types.</span></span></p>
<p><span data-ttu-id="431a5-1009"><strong>Nota:  </strong> El error de JET_errIndexTuplesTextColumnsOnly está obsoleto y se ha reemplazado por JET_errIndexTuplesTextBinaryColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="431a5-1009"><strong>Note  </strong>The JET_errIndexTuplesTextColumnsOnly error is obsolete and has been replaced by JET_errIndexTuplesTextBinaryColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1010">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="431a5-1010">JET_errIndexTuplesVarSegMacNotAllowed</span></span><br />
<span data-ttu-id="431a5-1011">-1434</span><span class="sxs-lookup"><span data-stu-id="431a5-1011">-1434</span></span></p></td>
<td><p><span data-ttu-id="431a5-1012">El índice de tupla no permite establecer cbVarSegMac.</span><span class="sxs-lookup"><span data-stu-id="431a5-1012">The tuple index does not allow setting cbVarSegMac.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1013">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="431a5-1013">JET_errIndexTuplesInvalidLimits</span></span><br />
<span data-ttu-id="431a5-1014">-1435</span><span class="sxs-lookup"><span data-stu-id="431a5-1014">-1435</span></span></p></td>
<td><p><span data-ttu-id="431a5-1015">La longitud de tupla mínima/máxima o el número máximo de caracteres que se especifican para un índice no son válidos.</span><span class="sxs-lookup"><span data-stu-id="431a5-1015">The minimum/maximum tuple length or the maximum number of characters that are specified for an index are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="431a5-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span></span><br />
<span data-ttu-id="431a5-1017">-1436</span><span class="sxs-lookup"><span data-stu-id="431a5-1017">-1436</span></span></p></td>
<td><p><span data-ttu-id="431a5-1018">No se puede llamar a <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> con la marca JET_bitRetrieveFromIndex establecida al recuperar una columna en un índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="431a5-1018"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> cannot be called with the JET_bitRetrieveFromIndex flag set while retrieving a column on a tuple index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1019">JET_errIndexTuplesKeyTooSmall</span><span class="sxs-lookup"><span data-stu-id="431a5-1019">JET_errIndexTuplesKeyTooSmall</span></span><br />
<span data-ttu-id="431a5-1020">-1437</span><span class="sxs-lookup"><span data-stu-id="431a5-1020">-1437</span></span></p></td>
<td><p><span data-ttu-id="431a5-1021">La clave especificada no cumple la longitud mínima de la tupla.</span><span class="sxs-lookup"><span data-stu-id="431a5-1021">The specified key does not meet the minimum tuple length.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1022">JET_errColumnLong</span><span class="sxs-lookup"><span data-stu-id="431a5-1022">JET_errColumnLong</span></span><br />
<span data-ttu-id="431a5-1023">-1501</span><span class="sxs-lookup"><span data-stu-id="431a5-1023">-1501</span></span></p></td>
<td><p><span data-ttu-id="431a5-1024">El valor de la columna es Long.</span><span class="sxs-lookup"><span data-stu-id="431a5-1024">The column value is long.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1025">JET_errColumnNoChunk</span><span class="sxs-lookup"><span data-stu-id="431a5-1025">JET_errColumnNoChunk</span></span><br />
<span data-ttu-id="431a5-1026">-1502</span><span class="sxs-lookup"><span data-stu-id="431a5-1026">-1502</span></span></p></td>
<td><p><span data-ttu-id="431a5-1027">No existe este fragmento en un valor largo.</span><span class="sxs-lookup"><span data-stu-id="431a5-1027">There is no such chunk in a long value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1028">JET_errColumnDoesNotFit</span><span class="sxs-lookup"><span data-stu-id="431a5-1028">JET_errColumnDoesNotFit</span></span><br />
<span data-ttu-id="431a5-1029">-1503</span><span class="sxs-lookup"><span data-stu-id="431a5-1029">-1503</span></span></p></td>
<td><p><span data-ttu-id="431a5-1030">El campo no cabe en el registro.</span><span class="sxs-lookup"><span data-stu-id="431a5-1030">The field will not fit in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1031">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="431a5-1031">JET_errNullInvalid</span></span><br />
<span data-ttu-id="431a5-1032">-1504</span><span class="sxs-lookup"><span data-stu-id="431a5-1032">-1504</span></span></p></td>
<td><p><span data-ttu-id="431a5-1033">NULL no es válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-1033">Null is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1034">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="431a5-1034">JET_errColumnIllegalNull</span></span><br />
<span data-ttu-id="431a5-1035">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="431a5-1035">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="431a5-1036">NULL no es válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-1036">Null is not valid.</span></span> <span data-ttu-id="431a5-1037">Este error lo devuelve el administrador de registros.</span><span class="sxs-lookup"><span data-stu-id="431a5-1037">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1038">JET_errColumnIndexed-1505</span><span class="sxs-lookup"><span data-stu-id="431a5-1038">JET_errColumnIndexed -1505</span></span></p></td>
<td><p><span data-ttu-id="431a5-1039">La columna está indizada y no se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="431a5-1039">The column is indexed and cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1040">JET_errColumnTooBig-1506</span><span class="sxs-lookup"><span data-stu-id="431a5-1040">JET_errColumnTooBig -1506</span></span></p></td>
<td><p><span data-ttu-id="431a5-1041">La longitud del campo es mayor que la longitud máxima permitida.</span><span class="sxs-lookup"><span data-stu-id="431a5-1041">The field length is greater than maximum allowed length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1042">JET_errColumnNotFound-1507</span><span class="sxs-lookup"><span data-stu-id="431a5-1042">JET_errColumnNotFound -1507</span></span></p></td>
<td><p><span data-ttu-id="431a5-1043">No existe esa columna.</span><span class="sxs-lookup"><span data-stu-id="431a5-1043">There is no such column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1044">JET_errColumnDuplicate-1508</span><span class="sxs-lookup"><span data-stu-id="431a5-1044">JET_errColumnDuplicate -1508</span></span></p></td>
<td><p><span data-ttu-id="431a5-1045">Este campo ya está definido.</span><span class="sxs-lookup"><span data-stu-id="431a5-1045">This field is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1046">JET_errMultiValuedColumnMustBeTagged-1509</span><span class="sxs-lookup"><span data-stu-id="431a5-1046">JET_errMultiValuedColumnMustBeTagged -1509</span></span></p></td>
<td><p><span data-ttu-id="431a5-1047">Se intentó crear una columna con varios valores, pero no se etiquetó la columna.</span><span class="sxs-lookup"><span data-stu-id="431a5-1047">An attempt was made to create a multi-valued column, but the column was not tagged.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1048">JET_errColumnRedundant-1510</span><span class="sxs-lookup"><span data-stu-id="431a5-1048">JET_errColumnRedundant -1510</span></span></p></td>
<td><p><span data-ttu-id="431a5-1049">Se produjo una segunda columna de incremento automático o de versión.</span><span class="sxs-lookup"><span data-stu-id="431a5-1049">There was a second auto-increment or version column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1050">JET_errInvalidColumnType-1511</span><span class="sxs-lookup"><span data-stu-id="431a5-1050">JET_errInvalidColumnType -1511</span></span></p></td>
<td><p><span data-ttu-id="431a5-1051">El tipo de datos de la columna no es válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-1051">The column data type is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1052">JET_errTaggedNotNULL-1514</span><span class="sxs-lookup"><span data-stu-id="431a5-1052">JET_errTaggedNotNULL -1514</span></span></p></td>
<td><p><span data-ttu-id="431a5-1053">No hay ninguna columna etiquetada que no sea NULL.</span><span class="sxs-lookup"><span data-stu-id="431a5-1053">There are no non-NULL tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1054">JET_errNoCurrentIndex-1515</span><span class="sxs-lookup"><span data-stu-id="431a5-1054">JET_errNoCurrentIndex -1515</span></span></p></td>
<td><p><span data-ttu-id="431a5-1055">La base de datos no es válida porque no contiene un índice actual.</span><span class="sxs-lookup"><span data-stu-id="431a5-1055">The database is invalid because it does not contain a current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1056">JET_errKeyIsMade-1516</span><span class="sxs-lookup"><span data-stu-id="431a5-1056">JET_errKeyIsMade -1516</span></span></p></td>
<td><p><span data-ttu-id="431a5-1057">La clave se realiza por completo.</span><span class="sxs-lookup"><span data-stu-id="431a5-1057">The key is completely made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1058">JET_errBadColumnId-1517</span><span class="sxs-lookup"><span data-stu-id="431a5-1058">JET_errBadColumnId -1517</span></span></p></td>
<td><p><span data-ttu-id="431a5-1059">El ID. de columna no es correcto.</span><span class="sxs-lookup"><span data-stu-id="431a5-1059">The column ID is incorrect.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1060">JET_errBadItagSequence-1518</span><span class="sxs-lookup"><span data-stu-id="431a5-1060">JET_errBadItagSequence -1518</span></span></p></td>
<td><p><span data-ttu-id="431a5-1061">Hay un itagSequence incorrecto para la columna etiquetada.</span><span class="sxs-lookup"><span data-stu-id="431a5-1061">There is a bad itagSequence for the tagged column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1062">JET_errColumnInRelationship-1519</span><span class="sxs-lookup"><span data-stu-id="431a5-1062">JET_errColumnInRelationship -1519</span></span></p></td>
<td><p><span data-ttu-id="431a5-1063">No se puede eliminar una columna porque forma parte de una relación.</span><span class="sxs-lookup"><span data-stu-id="431a5-1063">A column cannot be deleted because it is part of a relationship.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1064">JET_errCannotBeTagged-1521</span><span class="sxs-lookup"><span data-stu-id="431a5-1064">JET_errCannotBeTagged -1521</span></span></p></td>
<td><p><span data-ttu-id="431a5-1065">El incremento automático y la versión no se pueden etiquetar.</span><span class="sxs-lookup"><span data-stu-id="431a5-1065">The auto increment and version cannot be tagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1066">JET_errDefaultValueTooBig-1524</span><span class="sxs-lookup"><span data-stu-id="431a5-1066">JET_errDefaultValueTooBig -1524</span></span></p></td>
<td><p><span data-ttu-id="431a5-1067">El valor predeterminado es mayor que el tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="431a5-1067">The default value exceeds the maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1068">JET_errMultiValuedDuplicate-1525</span><span class="sxs-lookup"><span data-stu-id="431a5-1068">JET_errMultiValuedDuplicate -1525</span></span></p></td>
<td><p><span data-ttu-id="431a5-1069">Se detectó un valor duplicado en una columna con varios valores única.</span><span class="sxs-lookup"><span data-stu-id="431a5-1069">A duplicate value was detected on a unique multi-valued column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1070">JET_errLVCorrupted-1526</span><span class="sxs-lookup"><span data-stu-id="431a5-1070">JET_errLVCorrupted -1526</span></span></p></td>
<td><p><span data-ttu-id="431a5-1071">Se encontraron daños en un árbol de valores largos.</span><span class="sxs-lookup"><span data-stu-id="431a5-1071">Corruption was encountered in a long-value tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1072">JET_errMultiValuedDuplicateAfterTruncation-1528</span><span class="sxs-lookup"><span data-stu-id="431a5-1072">JET_errMultiValuedDuplicateAfterTruncation -1528</span></span></p></td>
<td><p><span data-ttu-id="431a5-1073">Se detectó un valor duplicado en una columna con varios valores única después de que se normalizaran los datos y se normalizó el truncamiento de los datos antes de la comparación.</span><span class="sxs-lookup"><span data-stu-id="431a5-1073">A duplicate value was detected on a unique multi-valued column after the data was normalized, and it is normalizing truncated the data before comparison.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1074">JET_errDerivedColumnCorruption-1529</span><span class="sxs-lookup"><span data-stu-id="431a5-1074">JET_errDerivedColumnCorruption -1529</span></span></p></td>
<td><p><span data-ttu-id="431a5-1075">Hay una columna no válida en la tabla derivada.</span><span class="sxs-lookup"><span data-stu-id="431a5-1075">There is an invalid column in derived table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1076">JET_errInvalidPlaceholderColumn-1530</span><span class="sxs-lookup"><span data-stu-id="431a5-1076">JET_errInvalidPlaceholderColumn -1530</span></span></p></td>
<td><p><span data-ttu-id="431a5-1077">Se intentó convertir una columna en un marcador de posición de índice principal, pero la columna no cumple los criterios necesarios.</span><span class="sxs-lookup"><span data-stu-id="431a5-1077">An attempt was made to convert a column to a primary index placeholder, but the column does not meet the necessary criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1078">JET_errRecordNotFound-1601</span><span class="sxs-lookup"><span data-stu-id="431a5-1078">JET_errRecordNotFound -1601</span></span></p></td>
<td><p><span data-ttu-id="431a5-1079">No se encontró la clave.</span><span class="sxs-lookup"><span data-stu-id="431a5-1079">The key was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1080">JET_errRecordNoCopy-1602</span><span class="sxs-lookup"><span data-stu-id="431a5-1080">JET_errRecordNoCopy -1602</span></span></p></td>
<td><p><span data-ttu-id="431a5-1081">No hay ningún búfer de trabajo.</span><span class="sxs-lookup"><span data-stu-id="431a5-1081">There is no working buffer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1082">JET_errNoCurrentRecord-1603</span><span class="sxs-lookup"><span data-stu-id="431a5-1082">JET_errNoCurrentRecord -1603</span></span></p></td>
<td><p><span data-ttu-id="431a5-1083">No hay ningún registro actual.</span><span class="sxs-lookup"><span data-stu-id="431a5-1083">There is no current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1084">JET_errRecordPrimaryChanged-1604</span><span class="sxs-lookup"><span data-stu-id="431a5-1084">JET_errRecordPrimaryChanged -1604</span></span></p></td>
<td><p><span data-ttu-id="431a5-1085">Es posible que la clave principal no cambie.</span><span class="sxs-lookup"><span data-stu-id="431a5-1085">The primary key might not change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1086">JET_errKeyDuplicate-1605</span><span class="sxs-lookup"><span data-stu-id="431a5-1086">JET_errKeyDuplicate -1605</span></span></p></td>
<td><p><span data-ttu-id="431a5-1087">Hay una clave duplicada no válida.</span><span class="sxs-lookup"><span data-stu-id="431a5-1087">There is an illegal duplicate key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1088">JET_errAlreadyPrepared-1607</span><span class="sxs-lookup"><span data-stu-id="431a5-1088">JET_errAlreadyPrepared -1607</span></span></p></td>
<td><p><span data-ttu-id="431a5-1089">Se intentó actualizar un registro mientras una actualización de registro ya estaba en curso.</span><span class="sxs-lookup"><span data-stu-id="431a5-1089">An attempt was made to update a record while a record update was already in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1090">JET_errKeyNotMade-1608</span><span class="sxs-lookup"><span data-stu-id="431a5-1090">JET_errKeyNotMade -1608</span></span></p></td>
<td><p><span data-ttu-id="431a5-1091">No se realizó una llamada a <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span><span class="sxs-lookup"><span data-stu-id="431a5-1091">A call was not made to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1092">JET_errUpdateNotPrepared-1609</span><span class="sxs-lookup"><span data-stu-id="431a5-1092">JET_errUpdateNotPrepared -1609</span></span></p></td>
<td><p><span data-ttu-id="431a5-1093">No se realizó una llamada a <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="431a5-1093">A call was not made to <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1094">JET_errDataHasChanged-1611</span><span class="sxs-lookup"><span data-stu-id="431a5-1094">JET_errDataHasChanged -1611</span></span></p></td>
<td><p><span data-ttu-id="431a5-1095">Los datos han cambiado y se anuló la operación.</span><span class="sxs-lookup"><span data-stu-id="431a5-1095">The data has changed and the operation was aborted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1096">JET_errLanguageNotSupported-1619</span><span class="sxs-lookup"><span data-stu-id="431a5-1096">JET_errLanguageNotSupported -1619</span></span></p></td>
<td><p><span data-ttu-id="431a5-1097">Esta instalación de Windows no admite el idioma seleccionado.</span><span class="sxs-lookup"><span data-stu-id="431a5-1097">This Windows installation does not support the selected language.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1098">JET_errTooManySorts-1701</span><span class="sxs-lookup"><span data-stu-id="431a5-1098">JET_errTooManySorts -1701</span></span></p></td>
<td><p><span data-ttu-id="431a5-1099">Hay demasiados procesos de ordenación.</span><span class="sxs-lookup"><span data-stu-id="431a5-1099">There are too many sort processes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1100">JET_errInvalidOnSort-1702</span><span class="sxs-lookup"><span data-stu-id="431a5-1100">JET_errInvalidOnSort -1702</span></span></p></td>
<td><p><span data-ttu-id="431a5-1101">Se produjo una operación no válida durante una ordenación.</span><span class="sxs-lookup"><span data-stu-id="431a5-1101">An invalid operation occurred during a sort.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1102">JET_errTempFileOpenError-1803</span><span class="sxs-lookup"><span data-stu-id="431a5-1102">JET_errTempFileOpenError -1803</span></span></p></td>
<td><p><span data-ttu-id="431a5-1103">No se pudo abrir el archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="431a5-1103">The temporary file could not be opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1104">JET_errTooManyAttachedDatabases-1805</span><span class="sxs-lookup"><span data-stu-id="431a5-1104">JET_errTooManyAttachedDatabases -1805</span></span></p></td>
<td><p><span data-ttu-id="431a5-1105">Hay demasiadas bases de datos abiertas.</span><span class="sxs-lookup"><span data-stu-id="431a5-1105">Too many databases are open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1106">JET_errDiskFull-1808</span><span class="sxs-lookup"><span data-stu-id="431a5-1106">JET_errDiskFull -1808</span></span></p></td>
<td><p><span data-ttu-id="431a5-1107">No queda espacio en el disco.</span><span class="sxs-lookup"><span data-stu-id="431a5-1107">There is no space left on disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1108">JET_errPermissionDenied-1809</span><span class="sxs-lookup"><span data-stu-id="431a5-1108">JET_errPermissionDenied -1809</span></span></p></td>
<td><p><span data-ttu-id="431a5-1109">Se denegó el permiso.</span><span class="sxs-lookup"><span data-stu-id="431a5-1109">Permission is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1110">JET_errFileNotFound-1811</span><span class="sxs-lookup"><span data-stu-id="431a5-1110">JET_errFileNotFound -1811</span></span></p></td>
<td><p><span data-ttu-id="431a5-1111">No se encontró el archivo.</span><span class="sxs-lookup"><span data-stu-id="431a5-1111">The file was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1112">JET_errFileInvalidType-1812</span><span class="sxs-lookup"><span data-stu-id="431a5-1112">JET_errFileInvalidType -1812</span></span></p></td>
<td><p><span data-ttu-id="431a5-1113">El tipo de archivo no es válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-1113">The file type is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1114">JET_errAfterInitialization-1850</span><span class="sxs-lookup"><span data-stu-id="431a5-1114">JET_errAfterInitialization -1850</span></span></p></td>
<td><p><span data-ttu-id="431a5-1115">No se puede iniciar una restauración después de la inicialización.</span><span class="sxs-lookup"><span data-stu-id="431a5-1115">A restore cannot be started after initialization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1116">JET_errLogCorrupted-1852</span><span class="sxs-lookup"><span data-stu-id="431a5-1116">JET_errLogCorrupted -1852</span></span></p></td>
<td><p><span data-ttu-id="431a5-1117">No se pudieron interpretar los registros.</span><span class="sxs-lookup"><span data-stu-id="431a5-1117">The logs could not be interpreted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1118">JET_errInvalidOperation-1906</span><span class="sxs-lookup"><span data-stu-id="431a5-1118">JET_errInvalidOperation -1906</span></span></p></td>
<td><p><span data-ttu-id="431a5-1119">La operación no es válida.</span><span class="sxs-lookup"><span data-stu-id="431a5-1119">The operation is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1120">JET_errAccessDenied-1907</span><span class="sxs-lookup"><span data-stu-id="431a5-1120">JET_errAccessDenied -1907</span></span></p></td>
<td><p><span data-ttu-id="431a5-1121">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="431a5-1121">Access is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1122">JET_errTooManySplits-1909</span><span class="sxs-lookup"><span data-stu-id="431a5-1122">JET_errTooManySplits -1909</span></span></p></td>
<td><p><span data-ttu-id="431a5-1123">División infinita.</span><span class="sxs-lookup"><span data-stu-id="431a5-1123">An infinite split.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1124">JET_errSessionSharingViolation-1910</span><span class="sxs-lookup"><span data-stu-id="431a5-1124">JET_errSessionSharingViolation -1910</span></span></p></td>
<td><p><span data-ttu-id="431a5-1125">Varios subprocesos están usando la misma sesión.</span><span class="sxs-lookup"><span data-stu-id="431a5-1125">Multiple threads are using the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1126">JET_errEntryPointNotFound-1911</span><span class="sxs-lookup"><span data-stu-id="431a5-1126">JET_errEntryPointNotFound -1911</span></span></p></td>
<td><p><span data-ttu-id="431a5-1127">No se pudo encontrar un punto de entrada en un archivo DLL necesario.</span><span class="sxs-lookup"><span data-stu-id="431a5-1127">An entry point in a required DLL could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1128">JET_errSessionContextAlreadySet-1912</span><span class="sxs-lookup"><span data-stu-id="431a5-1128">JET_errSessionContextAlreadySet -1912</span></span></p></td>
<td><p><span data-ttu-id="431a5-1129">La sesión especificada ya tiene un conjunto de contextos de sesión.</span><span class="sxs-lookup"><span data-stu-id="431a5-1129">The specified session already has a session context set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1130">JET_errSessionContextNotSetByThisThread-1913</span><span class="sxs-lookup"><span data-stu-id="431a5-1130">JET_errSessionContextNotSetByThisThread -1913</span></span></p></td>
<td><p><span data-ttu-id="431a5-1131">Se intentó restablecer el contexto de la sesión, pero el subproceso actual no era el original que estableció el contexto de la sesión.</span><span class="sxs-lookup"><span data-stu-id="431a5-1131">An attempt was made to reset the session context, but the current thread was not the original one that set the session context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1132">JET_errSessionInUse-1914</span><span class="sxs-lookup"><span data-stu-id="431a5-1132">JET_errSessionInUse -1914</span></span></p></td>
<td><p><span data-ttu-id="431a5-1133">Se ha intentado finalizar la sesión actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="431a5-1133">An attempt was made to terminate the session currently in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1134">JET_errRecordFormatConversionFailed-1915</span><span class="sxs-lookup"><span data-stu-id="431a5-1134">JET_errRecordFormatConversionFailed -1915</span></span></p></td>
<td><p><span data-ttu-id="431a5-1135">Se produjo un error interno durante la conversión del formato de registro dinámico.</span><span class="sxs-lookup"><span data-stu-id="431a5-1135">An internal error occurred during a dynamic record format conversion.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1136">JET_errOneDatabasePerSession-1916</span><span class="sxs-lookup"><span data-stu-id="431a5-1136">JET_errOneDatabasePerSession -1916</span></span></p></td>
<td><p><span data-ttu-id="431a5-1137">Solo se permite una base de datos de usuario abierta por sesión (como se indica al establecer la marca de <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> durante la creación de la base de datos).</span><span class="sxs-lookup"><span data-stu-id="431a5-1137">Only one open user database per session is allowed (as indicated by setting the <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> flag during database creation).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1138">JET_errRollbackError-1917</span><span class="sxs-lookup"><span data-stu-id="431a5-1138">JET_errRollbackError -1917</span></span></p></td>
<td><p><span data-ttu-id="431a5-1139">Error durante la reversión.</span><span class="sxs-lookup"><span data-stu-id="431a5-1139">There was an error during rollback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1140">JET_errCallbackFailed-2101</span><span class="sxs-lookup"><span data-stu-id="431a5-1140">JET_errCallbackFailed -2101</span></span></p></td>
<td><p><span data-ttu-id="431a5-1141">Error en una llamada de función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="431a5-1141">A callback function call failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1142">JET_errCallbackNotResolved-2102</span><span class="sxs-lookup"><span data-stu-id="431a5-1142">JET_errCallbackNotResolved -2102</span></span></p></td>
<td><p><span data-ttu-id="431a5-1143">No se pudo encontrar una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="431a5-1143">A callback function could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1144">JET_errOSSnapshotInvalidSequence-2401</span><span class="sxs-lookup"><span data-stu-id="431a5-1144">JET_errOSSnapshotInvalidSequence -2401</span></span></p></td>
<td><p><span data-ttu-id="431a5-1145">La API de instantáneas de sistema operativo se usó en una secuencia no válida.</span><span class="sxs-lookup"><span data-stu-id="431a5-1145">The operating system shadow copy API was used in an invalid sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1146">JET_errOSSnapshotTimeOut-2402</span><span class="sxs-lookup"><span data-stu-id="431a5-1146">JET_errOSSnapshotTimeOut -2402</span></span></p></td>
<td><p><span data-ttu-id="431a5-1147">La instantánea del sistema operativo finalizó con un tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="431a5-1147">The operating system shadow copy ended with a time-out.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1148">JET_errOSSnapshotNotAllowed-2403</span><span class="sxs-lookup"><span data-stu-id="431a5-1148">JET_errOSSnapshotNotAllowed -2403</span></span></p></td>
<td><p><span data-ttu-id="431a5-1149">La instantánea del sistema operativo no está permitida porque una copia de seguridad o una recuperación en está en curso.</span><span class="sxs-lookup"><span data-stu-id="431a5-1149">The operating system shadow copy is not allowed because a backup or recovery in is progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1150">JET_errOSSnapshotInvalidSnapId-2404</span><span class="sxs-lookup"><span data-stu-id="431a5-1150">JET_errOSSnapshotInvalidSnapId -2404</span></span></p></td>
<td><p><span data-ttu-id="431a5-1151">No se pudo realizar la operación porque el controlador de instantáneas del sistema operativo especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="431a5-1151">The operation failed because the specified operating system shadow copy handle was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1152">JET_errLSCallbackNotSpecified-3000</span><span class="sxs-lookup"><span data-stu-id="431a5-1152">JET_errLSCallbackNotSpecified -3000</span></span></p></td>
<td><p><span data-ttu-id="431a5-1153">Se intentó usar el almacenamiento local sin especificar una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="431a5-1153">An attempt was made to use local storage without a callback function being specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1154">JET_errLSAlreadySet-3001</span><span class="sxs-lookup"><span data-stu-id="431a5-1154">JET_errLSAlreadySet -3001</span></span></p></td>
<td><p><span data-ttu-id="431a5-1155">Se intentó establecer el almacenamiento local de un objeto que ya lo tenía establecido.</span><span class="sxs-lookup"><span data-stu-id="431a5-1155">An attempt was made to set the local storage for an object which already had it set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1156">JET_errLSNotSet-3002</span><span class="sxs-lookup"><span data-stu-id="431a5-1156">JET_errLSNotSet -3002</span></span></p></td>
<td><p><span data-ttu-id="431a5-1157">Se intentó recuperar el almacenamiento local de un objeto que no lo tenía establecido.</span><span class="sxs-lookup"><span data-stu-id="431a5-1157">An attempt was made to retrieve local storage from an object which did not have it set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1158">JET_errFileIOSparse-4000</span><span class="sxs-lookup"><span data-stu-id="431a5-1158">JET_errFileIOSparse -4000</span></span></p></td>
<td><p><span data-ttu-id="431a5-1159">No se pudo realizar una operación de e/s porque se intentó en una región sin asignar de un archivo.</span><span class="sxs-lookup"><span data-stu-id="431a5-1159">An I/O operation failed because it was attempted against an unallocated region of a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1160">JET_errFileIOBeyondEOF-4001</span><span class="sxs-lookup"><span data-stu-id="431a5-1160">JET_errFileIOBeyondEOF -4001</span></span></p></td>
<td><p><span data-ttu-id="431a5-1161">Se emitió una lectura a una ubicación más allá de EOF (las escrituras expandirán el archivo).</span><span class="sxs-lookup"><span data-stu-id="431a5-1161">A read was issued to a location beyond the EOF (writes will expand the file).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1162">JET_errFileIOAbort-4002</span><span class="sxs-lookup"><span data-stu-id="431a5-1162">JET_errFileIOAbort -4002</span></span></p></td>
<td><p><span data-ttu-id="431a5-1163">Esta marca indica al JET_ABORTRETRYFAILCALLBACK que llama para anular la e/s especificada.</span><span class="sxs-lookup"><span data-stu-id="431a5-1163">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to abort the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1164">JET_errFileIORetry-4003</span><span class="sxs-lookup"><span data-stu-id="431a5-1164">JET_errFileIORetry -4003</span></span></p></td>
<td><p><span data-ttu-id="431a5-1165">Esta marca indica al llamador JET_ABORTRETRYFAILCALLBACK que vuelva a intentar la e/s especificada.</span><span class="sxs-lookup"><span data-stu-id="431a5-1165">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to retry the specified I/O.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1166">JET_errFileIOFail-4004</span><span class="sxs-lookup"><span data-stu-id="431a5-1166">JET_errFileIOFail -4004</span></span></p></td>
<td><p><span data-ttu-id="431a5-1167">Esta marca indica al JET_ABORTRETRYFAILCALLBACK llamador que produzca un error en la e/s especificada.</span><span class="sxs-lookup"><span data-stu-id="431a5-1167">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to fail the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1168">JET_errFileCompressed-4005</span><span class="sxs-lookup"><span data-stu-id="431a5-1168">JET_errFileCompressed -4005</span></span></p></td>
<td><p><span data-ttu-id="431a5-1169">No se admite el acceso de lectura y escritura en archivos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="431a5-1169">Read/write access is not supported on compressed files.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="431a5-1170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="431a5-1170">Remarks</span></span>

<span data-ttu-id="431a5-1171">En general, un valor mayor que cero debe interpretarse como una advertencia, el valor cero debe interpretarse como correcto y un valor menor que cero debe interpretarse como un error.</span><span class="sxs-lookup"><span data-stu-id="431a5-1171">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="431a5-1172">Ningún otro patrón de estos valores, como los intervalos de valores, debe basarse en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="431a5-1172">No other patterns in these values, such as ranges of values, should be relied upon by an application.</span></span>

### <a name="requirements"></a><span data-ttu-id="431a5-1173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="431a5-1173">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1174"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="431a5-1174"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="431a5-1175">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="431a5-1175">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a5-1176"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="431a5-1176"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="431a5-1177">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="431a5-1177">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a5-1178"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="431a5-1178"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="431a5-1179">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="431a5-1179">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="431a5-1180">Consulte también</span><span class="sxs-lookup"><span data-stu-id="431a5-1180">See Also</span></span>

[<span data-ttu-id="431a5-1181">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="431a5-1181">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="431a5-1182">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="431a5-1182">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="431a5-1183">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="431a5-1183">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)
