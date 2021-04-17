---
description: 'Más información acerca de: JetCreateDatabase (función)'
title: Función JetCreateDatabase
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8fbec76e3b38f9b42c36156b2312a8e77a6b43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716167"
---
# <a name="jetcreatedatabase-function"></a><span data-ttu-id="bc684-103">Función JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="bc684-103">JetCreateDatabase Function</span></span>


<span data-ttu-id="bc684-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bc684-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase-function"></a><span data-ttu-id="bc684-105">Función JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="bc684-105">JetCreateDatabase Function</span></span>

<span data-ttu-id="bc684-106">La función **JetCreateDatabase** crea y adjunta un archivo de base de datos que se utilizará con el motor de base de datos ese.</span><span class="sxs-lookup"><span data-stu-id="bc684-106">The **JetCreateDatabase** function creates and attaches a database file to be used with the ESE database engine.</span></span> <span data-ttu-id="bc684-107">Llamar a [JetCreateDatabase2](./jetcreatedatabase2-function.md) con *cpgDatabaseSizeMax* establecido en cero es idéntico a llamar a **JETCREATEDATABASE** con *szConnect* establecido en NULL.</span><span class="sxs-lookup"><span data-stu-id="bc684-107">Calling [JetCreateDatabase2](./jetcreatedatabase2-function.md) with *cpgDatabaseSizeMax* set to zero is identical to calling **JetCreateDatabase** with *szConnect* set to NULL.</span></span> <span data-ttu-id="bc684-108">Actualmente, se pueden crear hasta siete bases de datos por instancia.</span><span class="sxs-lookup"><span data-stu-id="bc684-108">Currently, up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="bc684-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc684-109">Parameters</span></span>

<span data-ttu-id="bc684-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="bc684-110">*sesid*</span></span>

<span data-ttu-id="bc684-111">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="bc684-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="bc684-112">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="bc684-112">*szFilename*</span></span>

<span data-ttu-id="bc684-113">Nombre de la base de datos que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="bc684-113">The name of the database to be created.</span></span>

<span data-ttu-id="bc684-114">*szConnect*</span><span class="sxs-lookup"><span data-stu-id="bc684-114">*szConnect*</span></span>

<span data-ttu-id="bc684-115">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="bc684-115">Reserved for future use.</span></span> <span data-ttu-id="bc684-116">Definición en NULL</span><span class="sxs-lookup"><span data-stu-id="bc684-116">Set to NULL.</span></span>

<span data-ttu-id="bc684-117">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="bc684-117">*pdbid*</span></span>

<span data-ttu-id="bc684-118">Puntero a un búfer que, en una llamada correcta, contiene el identificador de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="bc684-118">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="bc684-119">En caso de error, el valor es indefinido.</span><span class="sxs-lookup"><span data-stu-id="bc684-119">On failure, the value is undefined.</span></span>

<span data-ttu-id="bc684-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="bc684-120">*grbit*</span></span>

<span data-ttu-id="bc684-121">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="bc684-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc684-122">Value</span><span class="sxs-lookup"><span data-stu-id="bc684-122">Value</span></span></p></th>
<th><p><span data-ttu-id="bc684-123">Significado</span><span class="sxs-lookup"><span data-stu-id="bc684-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc684-124">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="bc684-124">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="bc684-125">De forma predeterminada, si se llama a <strong>JetCreateDatabase</strong> y la base de datos ya existe, se producirá un error en la llamada a la API y no se sobrescribirá la base de datos original.</span><span class="sxs-lookup"><span data-stu-id="bc684-125">By default, if <strong>JetCreateDatabase</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="bc684-126">JET_bitDbOverwriteExisting cambia este comportamiento y la antigua base de datos se sobrescribirá con otra nueva.</span><span class="sxs-lookup"><span data-stu-id="bc684-126">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="bc684-127">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bc684-127">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc684-128">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="bc684-128">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="bc684-129">JET_bitDbRecoveryOff desactiva el registro.</span><span class="sxs-lookup"><span data-stu-id="bc684-129">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="bc684-130">La configuración de este bit pierde la capacidad de reproducir los archivos de registro y de recuperar la base de datos a un estado utilizable coherente después de un evento catastrófico.</span><span class="sxs-lookup"><span data-stu-id="bc684-130">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc684-131">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="bc684-131">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="bc684-132">Al establecer JET_bitDbShadowingOff se deshabilitará la duplicación de algunas estructuras de base de datos internas (sombreado).</span><span class="sxs-lookup"><span data-stu-id="bc684-132">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="bc684-133">La duplicación de estas estructuras se realiza para lograr resistencia, por lo que la configuración de JET_bitDbShadowingOff quitará esa resistencia.</span><span class="sxs-lookup"><span data-stu-id="bc684-133">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="bc684-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc684-134">Return Value</span></span>

<span data-ttu-id="bc684-135">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="bc684-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bc684-136">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bc684-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc684-137">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bc684-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="bc684-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc684-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc684-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bc684-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bc684-140">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bc684-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc684-141">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="bc684-141">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="bc684-142">La base de datos denominada en <em>szFilename</em> ya existe.</span><span class="sxs-lookup"><span data-stu-id="bc684-142">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="bc684-143">Cuando se devuelve este error, la base de datos no se adjunta.</span><span class="sxs-lookup"><span data-stu-id="bc684-143">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc684-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="bc684-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="bc684-145">Se puede devolver si se solicitó acceso exclusivo, pero no se pudo conceder o si otra sesión ya ha abierto la base de datos de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="bc684-145">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc684-146">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="bc684-146">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="bc684-147">Se devuelve cuando <em>cpgDatabaseSizeMax</em> es mayor que el número máximo de páginas permitidas en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="bc684-147">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="bc684-148">El máximo actual es 2147483646 (0x7ffffffe).</span><span class="sxs-lookup"><span data-stu-id="bc684-148">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc684-149">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="bc684-149">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="bc684-150">Se proporcionó una ruta de acceso no válida en <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="bc684-150">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="bc684-151"><em>szFilename</em> debe ser distinto de NULL.</span><span class="sxs-lookup"><span data-stu-id="bc684-151"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="bc684-152">De forma predeterminada, <em>szFilename</em> debe apuntar a un directorio que exista.</span><span class="sxs-lookup"><span data-stu-id="bc684-152">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="bc684-153">La ruta de acceso se creará si se establece <em>JET_paramCreatePathIfNotExist</em> (vea <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span><span class="sxs-lookup"><span data-stu-id="bc684-153">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc684-154">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="bc684-154">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="bc684-155">Indica que otra sesión ya ha abierto la base de datos de forma exclusiva (mediante JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="bc684-155">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc684-156">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="bc684-156">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="bc684-157">La base de datos no se adjuntó previamente (vea <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="bc684-157">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc684-158">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="bc684-158">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="bc684-159">Una sesión diferente ya ha adjuntado el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="bc684-159">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc684-160">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="bc684-160">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="bc684-161">Se intentó crear una base de datos mientras estaba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="bc684-161">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc684-162">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="bc684-162">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="bc684-163">Se intentó abrir un archivo que no es un archivo de base de datos válido.</span><span class="sxs-lookup"><span data-stu-id="bc684-163">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc684-164">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="bc684-164">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="bc684-165">Se intentó abrir más de una base de datos y se estableció JET_paramOneDatabasePerSession.</span><span class="sxs-lookup"><span data-stu-id="bc684-165">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="bc684-166">Vea <a href="gg269337(v=exchg.10).md">parámetros de base de datos</a>.</span><span class="sxs-lookup"><span data-stu-id="bc684-166">See <a href="gg269337(v=exchg.10).md">Database Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc684-167">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="bc684-167">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="bc684-168">No se pudo realizar la operación porque no se pudo asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="bc684-168">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc684-169">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="bc684-169">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="bc684-170">Solo se puede asociar un número finito de bases de datos por instancia.</span><span class="sxs-lookup"><span data-stu-id="bc684-170">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="bc684-171">Actualmente, el límite es de siete bases de datos por instancia.</span><span class="sxs-lookup"><span data-stu-id="bc684-171">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc684-172">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="bc684-172">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="bc684-173">Una advertencia no fatal que indica que el archivo de base de datos ya se ha adjuntado a esta sesión.</span><span class="sxs-lookup"><span data-stu-id="bc684-173">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc684-174">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="bc684-174">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="bc684-175">JET_wrnFileOpenReadOnly indica que el archivo estaba asociado de solo lectura, pero <strong>JetCreateDatabase</strong> no pasó JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="bc684-175">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <strong>JetCreateDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="bc684-176">La base de datos todavía está abierta con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bc684-176">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="bc684-177">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc684-177">Remarks</span></span>

<span data-ttu-id="bc684-178">Si la base de datos especificada en *szFilename* existe y no se ha pasado JET_bitDbOverwriteExisting, se producirá un error en la llamada a la API.</span><span class="sxs-lookup"><span data-stu-id="bc684-178">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="bc684-179">Si se pasó JET_bitDbOverwriteExisting, primero se eliminará el archivo de base de datos anterior.</span><span class="sxs-lookup"><span data-stu-id="bc684-179">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="bc684-180">Si la API crea un archivo de base de datos y, a continuación, llega a otro error, se limpiará y se eliminará el archivo.</span><span class="sxs-lookup"><span data-stu-id="bc684-180">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="bc684-181">**JetCreateDatabase** abrirá implícitamente la base de datos.</span><span class="sxs-lookup"><span data-stu-id="bc684-181">**JetCreateDatabase** will implicitly open the database.</span></span> <span data-ttu-id="bc684-182">No es necesario llamar posteriormente a [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="bc684-182">It is not necessarily to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="bc684-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc684-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc684-184"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="bc684-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bc684-185">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bc684-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc684-186"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bc684-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bc684-187">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bc684-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc684-188"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bc684-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bc684-189">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="bc684-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc684-190"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="bc684-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bc684-191">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bc684-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc684-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bc684-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bc684-193">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bc684-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc684-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="bc684-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="bc684-195">Se implementa como <strong>JetCreateDatabaseW</strong> (Unicode) y <strong>JetCreateDatabaseA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="bc684-195">Implemented as <strong>JetCreateDatabaseW</strong> (Unicode) and <strong>JetCreateDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bc684-196">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bc684-196">See Also</span></span>

[<span data-ttu-id="bc684-197">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="bc684-197">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="bc684-198">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bc684-198">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bc684-199">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="bc684-199">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="bc684-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="bc684-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="bc684-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bc684-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bc684-202">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="bc684-202">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="bc684-203">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="bc684-203">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="bc684-204">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="bc684-204">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="bc684-205">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="bc684-205">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="bc684-206">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="bc684-206">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="bc684-207">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="bc684-207">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
