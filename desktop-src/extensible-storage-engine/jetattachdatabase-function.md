---
description: 'Más información acerca de: JetAttachDatabase (función)'
title: Función JetAttachDatabase
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5968fe7906ace720dad3f94e278f37d992710d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275191"
---
# <a name="jetattachdatabase-function"></a><span data-ttu-id="30dba-103">Función JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="30dba-103">JetAttachDatabase Function</span></span>


<span data-ttu-id="30dba-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="30dba-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase-function"></a><span data-ttu-id="30dba-105">Función JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="30dba-105">JetAttachDatabase Function</span></span>

<span data-ttu-id="30dba-106">La función **JetAttachDatabase** adjunta un archivo de base de datos para su uso con una instancia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="30dba-106">The **JetAttachDatabase** function attaches a database file for use with a database instance.</span></span> <span data-ttu-id="30dba-107">Para poder usar la base de datos, deberá abrirse posteriormente con [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="30dba-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="30dba-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30dba-108">Parameters</span></span>

<span data-ttu-id="30dba-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="30dba-109">*sesid*</span></span>

<span data-ttu-id="30dba-110">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="30dba-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="30dba-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="30dba-111">*szFilename*</span></span>

<span data-ttu-id="30dba-112">Nombre de la base de datos que se va a adjuntar.</span><span class="sxs-lookup"><span data-stu-id="30dba-112">The name of the database to attach.</span></span>

<span data-ttu-id="30dba-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="30dba-113">*grbit*</span></span>

<span data-ttu-id="30dba-114">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="30dba-114">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30dba-115">Value</span><span class="sxs-lookup"><span data-stu-id="30dba-115">Value</span></span></p></th>
<th><p><span data-ttu-id="30dba-116">Significado</span><span class="sxs-lookup"><span data-stu-id="30dba-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30dba-117">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="30dba-117">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="30dba-118">Si se ha establecido <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> , se eliminarán todos los índices sobre los datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="30dba-118">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="30dba-119">Para obtener información más detallada, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="30dba-119">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dba-120">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="30dba-120">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="30dba-121">Se eliminarán todos los índices sobre datos Unicode, independientemente del valor de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span><span class="sxs-lookup"><span data-stu-id="30dba-121">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="30dba-122">Para obtener información más detallada, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="30dba-122">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30dba-123">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="30dba-123">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="30dba-124">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="30dba-124">Obsolete.</span></span> <span data-ttu-id="30dba-125">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="30dba-125">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dba-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="30dba-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="30dba-127">Impide las modificaciones en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="30dba-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="30dba-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30dba-128">Return Value</span></span>

<span data-ttu-id="30dba-129">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="30dba-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="30dba-130">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="30dba-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30dba-131">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="30dba-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="30dba-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="30dba-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30dba-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="30dba-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="30dba-134">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="30dba-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dba-135">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="30dba-135">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="30dba-136">No se permite adjuntar una base de datos durante una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="30dba-136">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30dba-137">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="30dba-137">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="30dba-138">El archivo de base de datos especificado por <em>szFilename</em> debe ser grabable.</span><span class="sxs-lookup"><span data-stu-id="30dba-138">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="30dba-139">No se debe establecer el atributo Read-Only y el proceso en ejecución debe tener privilegios suficientes para escribir en el archivo.</span><span class="sxs-lookup"><span data-stu-id="30dba-139">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dba-140">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="30dba-140">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="30dba-141">Otro proceso está abriendo el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="30dba-141">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30dba-142">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="30dba-142">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="30dba-143">Se proporcionó una ruta de acceso no válida en <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="30dba-143">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="30dba-144"><em>szFilename</em> debe ser distinto de NULL y hacer referencia a una ruta de acceso válida.</span><span class="sxs-lookup"><span data-stu-id="30dba-144"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dba-145">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="30dba-145">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="30dba-146">Una sesión diferente ya ha adjuntado el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="30dba-146">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30dba-147">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="30dba-147">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="30dba-148">El motor de base de datos no puede abrir el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="30dba-148">The database engine cannot open the database file.</span></span> <span data-ttu-id="30dba-149">Es posible que el archivo esté en uso por otro proceso o que el autor de la llamada no tenga privilegios suficientes para abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="30dba-149">The file may be in use by another process or the caller may not have sufficient privileges to open the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dba-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="30dba-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="30dba-151">El archivo proporcionado en <em>szFilename</em> no existe.</span><span class="sxs-lookup"><span data-stu-id="30dba-151">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30dba-152">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="30dba-152">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="30dba-153">Hay un error con el índice principal.</span><span class="sxs-lookup"><span data-stu-id="30dba-153">There is an error with the primary index.</span></span> <span data-ttu-id="30dba-154">Esto puede deberse a daños físicos (por ejemplo, daños en disco o memoria).</span><span class="sxs-lookup"><span data-stu-id="30dba-154">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="30dba-155">También se puede devolver al adjuntar una base de datos que se modificó por última vez en un sistema operativo anterior y el índice principal está sobre una columna con datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="30dba-155">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="30dba-156">Vea la sección Comentarios para obtener más información sobre los índices sobre datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="30dba-156">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dba-157">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="30dba-157">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="30dba-158">Hay un error con un índice secundario.</span><span class="sxs-lookup"><span data-stu-id="30dba-158">There is an error with a secondary index.</span></span> <span data-ttu-id="30dba-159">Esto puede deberse a daños físicos (por ejemplo, daños en disco o memoria).</span><span class="sxs-lookup"><span data-stu-id="30dba-159">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="30dba-160">También se puede devolver al adjuntar una base de datos que se modificó por última vez en un sistema operativo anterior y un índice secundario se encuentra sobre una columna con datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="30dba-160">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="30dba-161">Vea la sección Comentarios para obtener más información sobre los índices sobre datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="30dba-161">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="30dba-162">Los índices secundarios se recompilan completamente cuando una base de datos se desfragmenta con una utilidad sin conexión mediante el siguiente comando: <strong>esentutl-d</strong>.</span><span class="sxs-lookup"><span data-stu-id="30dba-162">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30dba-163">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="30dba-163">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="30dba-164">Solo se puede asociar un número finito de bases de datos por instancia.</span><span class="sxs-lookup"><span data-stu-id="30dba-164">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="30dba-165">Actualmente, el límite es de siete bases de datos por instancia.</span><span class="sxs-lookup"><span data-stu-id="30dba-165">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dba-166">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="30dba-166">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="30dba-167">Una advertencia no fatal que indica que el archivo de base de datos ya se ha adjuntado a esta sesión.</span><span class="sxs-lookup"><span data-stu-id="30dba-167">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="30dba-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30dba-168">Remarks</span></span>

<span data-ttu-id="30dba-169">Llamar a **JetAttachDatabase** es equivalente a llamar a [JetAttachDatabase2](./jetattachdatabase2-function.md) y pasar un valor de cero, lo que significa que no hay límite para el parámetro *cpgDatabaseSizeMax* .</span><span class="sxs-lookup"><span data-stu-id="30dba-169">Calling **JetAttachDatabase** is equivalent to calling [JetAttachDatabase2](./jetattachdatabase2-function.md) and passing a value of zero, meaning there is no limit, for the *cpgDatabaseSizeMax* parameter.</span></span>

<span data-ttu-id="30dba-170">Si se adjunta una base de datos de escritura (es decir, si no se especificó JET_bitDbReadOnly en el parámetro *grbit* ), el archivo se abrirá exclusivamente en el nivel de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="30dba-170">Attaching a writable database (that is, if JET_bitDbReadOnly was not specified in the *grbit* parameter) will open the file exclusively at the operating system level.</span></span> <span data-ttu-id="30dba-171">Ningún otro proceso podrá abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="30dba-171">No other process will be able open the file.</span></span> <span data-ttu-id="30dba-172">Es posible que varios procesos adjunten una sola base de datos abriéndola en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="30dba-172">It is possible for multiple processes to attach a single database by opening them in read-only mode.</span></span>

<span data-ttu-id="30dba-173">El archivo de base de datos se separa mediante [JetDetachDatabase](./jetdetachdatabase-function.md) o [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="30dba-173">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="30dba-174">Parámetros de comprobación de índices</span><span class="sxs-lookup"><span data-stu-id="30dba-174">Index-checking parameters</span></span>

<span data-ttu-id="30dba-175">Las distintas versiones de Windows normalizan el texto Unicode de maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="30dba-175">Different versions of Windows normalize Unicode text in different ways.</span></span> <span data-ttu-id="30dba-176">Esto significa que los índices compilados con una versión de Windows pueden no funcionar en otras versiones.</span><span class="sxs-lookup"><span data-stu-id="30dba-176">That means indexes built under one version of Windows may not work on other versions.</span></span>

<span data-ttu-id="30dba-177">Antes de Windows Server 2003, cuando la versión del sistema operativo cambió (incluida la instalación de un Service Pack), cada índice sobre datos Unicode estaba en un estado potencialmente dañado.</span><span class="sxs-lookup"><span data-stu-id="30dba-177">Prior to Windows Server 2003, when the operating system version changed (including installation of a Service Pack), every index over Unicode data was in a potentially corrupt state.</span></span>

<span data-ttu-id="30dba-178">Los índices creados en Windows Server 2003 y versiones posteriores se marcan con la versión de normalización Unicode con la que se compilaron.</span><span class="sxs-lookup"><span data-stu-id="30dba-178">Indexes created in Windows Server 2003 and later are flagged with the version of Unicode normalization with which they were built.</span></span> <span data-ttu-id="30dba-179">Los índices más antiguos no contienen información de versión.</span><span class="sxs-lookup"><span data-stu-id="30dba-179">Older indexes contain no version information.</span></span> <span data-ttu-id="30dba-180">La mayoría de los cambios de normalización Unicode consisten en agregar nuevos caracteres, los puntos de código que anteriormente no estaban definidos ahora se definen y normalizan de manera diferente.</span><span class="sxs-lookup"><span data-stu-id="30dba-180">Most Unicode normalization changes consist of adding new characters, code points which were previously undefined are now defined and normalize differently.</span></span> <span data-ttu-id="30dba-181">Por lo tanto, si los datos binarios se almacenan en una columna Unicode, se normalizarán de manera diferente a medida que se definen nuevos puntos de código.</span><span class="sxs-lookup"><span data-stu-id="30dba-181">Thus, if binary data is stored in a Unicode column, it will normalize differently as new code points are defined.</span></span>

<span data-ttu-id="30dba-182">A partir de Windows Server 2003, el motor de base de datos de ESE realiza un seguimiento de las entradas de índice Unicode que contienen puntos de código sin definir.</span><span class="sxs-lookup"><span data-stu-id="30dba-182">As of Windows Server 2003, the ESE database engine tracks Unicode index entries that contain undefined code points.</span></span> <span data-ttu-id="30dba-183">Se pueden usar para corregir un índice cuando cambia el conjunto de caracteres Unicode definidos.</span><span class="sxs-lookup"><span data-stu-id="30dba-183">These can be used to fix an index when the set of defined Unicode characters changes.</span></span>

<span data-ttu-id="30dba-184">Estos parámetros controlan lo que sucede cuando el motor de base de datos de ESE se adjunta a una base de datos que se usó por última vez en una compilación diferente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="30dba-184">These parameters control what happens when the ESE database engine attaches to a database that was last used under a different build of the operating system.</span></span> <span data-ttu-id="30dba-185">La versión del sistema operativo se marca en el encabezado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="30dba-185">The operating system version is stamped in the database header.</span></span>

<span data-ttu-id="30dba-186">Si [JET_paramEnableIndexChecking](./database-parameters.md) está establecido en **true** y la base de datos contiene índices potencialmente dañados:</span><span class="sxs-lookup"><span data-stu-id="30dba-186">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **TRUE**, and the database contains potentially corrupt indexes:</span></span>

  - <span data-ttu-id="30dba-187">**JetAttachDatabase** eliminará los índices potencialmente dañados si *grbit* contiene JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="30dba-187">**JetAttachDatabase** will delete the potentially corrupt indexes if *grbit* contains JET_bitDbDeleteCorruptIndexes</span></span>

  - <span data-ttu-id="30dba-188">**JetAttachDatabase** devolverá un error si *grbit* no contiene JET_bitDbDeleteCorruptIndexes y hay índices que deben eliminarse.</span><span class="sxs-lookup"><span data-stu-id="30dba-188">**JetAttachDatabase** will return an error if *grbit* does not contain JET_bitDbDeleteCorruptIndexes and there are indexes which need deletion.</span></span>

<span data-ttu-id="30dba-189">Si [JET_paramEnableIndexChecking](./database-parameters.md) está establecido en **false**:</span><span class="sxs-lookup"><span data-stu-id="30dba-189">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **FALSE**:</span></span>

  - <span data-ttu-id="30dba-190">**JetAttachDatabase** omitirá los índices potencialmente dañados y devolverá JET_errSuccess (suponiendo que no haya otros errores).</span><span class="sxs-lookup"><span data-stu-id="30dba-190">**JetAttachDatabase** will ignore potentially corrupt indexes, and return JET_errSuccess (assuming there were no other errors).</span></span>

<span data-ttu-id="30dba-191">Windows Server 2003 y versiones posteriores: Si no se ha restablecido [JET_paramEnableIndexChecking](./database-parameters.md) , se usará la tabla de correcciones internas para corregir las entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="30dba-191">Windows Server 2003 and later: If [JET_paramEnableIndexChecking](./database-parameters.md) has not been reset, the internal fixup table will be used to fixup index entries.</span></span> <span data-ttu-id="30dba-192">Es posible que esto no corrija todos los daños en el índice, pero que sea transparente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="30dba-192">This may not fix all index corruptions but will be transparent to the application.</span></span>

<span data-ttu-id="30dba-193">Si la base de datos se adjuntó como de solo lectura, el índice no se puede corregir ni eliminar.</span><span class="sxs-lookup"><span data-stu-id="30dba-193">If the database was attached as read-only the index cannot be fixed or deleted.</span></span> <span data-ttu-id="30dba-194">En este caso, la API devolverá en su lugar un error, como JET_errSecondaryIndexCorrupted o JET_errPrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="30dba-194">In this case, the API will instead return an error, such as JET_errSecondaryIndexCorrupted or JET_errPrimaryIndexCorrupted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="30dba-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30dba-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30dba-196"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="30dba-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="30dba-197">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="30dba-197">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dba-198"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="30dba-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="30dba-199">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="30dba-199">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30dba-200"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="30dba-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="30dba-201">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="30dba-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dba-202"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="30dba-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="30dba-203">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="30dba-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30dba-204"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="30dba-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="30dba-205">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="30dba-205">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30dba-206"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="30dba-206"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="30dba-207">Se implementa como <strong>JetAddColumnW</strong> (Unicode) y <strong>JetAddColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="30dba-207">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="30dba-208">Consulte también</span><span class="sxs-lookup"><span data-stu-id="30dba-208">See Also</span></span>

[<span data-ttu-id="30dba-209">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="30dba-209">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="30dba-210">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="30dba-210">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="30dba-211">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="30dba-211">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="30dba-212">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="30dba-212">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="30dba-213">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="30dba-213">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="30dba-214">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="30dba-214">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="30dba-215">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="30dba-215">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="30dba-216">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="30dba-216">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="30dba-217">JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="30dba-217">JetDetachDatabase2</span></span>](./jetdetachdatabase2-function.md)  
[<span data-ttu-id="30dba-218">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="30dba-218">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="30dba-219">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="30dba-219">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
