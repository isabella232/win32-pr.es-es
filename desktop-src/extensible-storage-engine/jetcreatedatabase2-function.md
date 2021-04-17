---
description: 'Más información acerca de: JetCreateDatabase2 (función)'
title: Función JetCreateDatabase2
TOCTitle: JetCreateDatabase2 Function
ms:assetid: 267ac69f-49d3-4741-b324-d8510d7a36d3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269208(v=EXCHG.10)
ms:contentKeyID: 32765511
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase2A
- JetCreateDatabase2W
- JetCreateDatabase2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370f88f95a2eb8217dc06124b50c9ed165eb679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716675"
---
# <a name="jetcreatedatabase2-function"></a><span data-ttu-id="6ce2a-103">Función JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="6ce2a-103">JetCreateDatabase2 Function</span></span>


<span data-ttu-id="6ce2a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6ce2a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase2-function"></a><span data-ttu-id="6ce2a-105">Función JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="6ce2a-105">JetCreateDatabase2 Function</span></span>

<span data-ttu-id="6ce2a-106">La función **JetCreateDatabase2** crea y adjunta un archivo de base de datos que se utilizará con el motor de base de datos ese con un tamaño máximo de base de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-106">The **JetCreateDatabase2** function creates and attaches a database file to be used with the ESE database engine with a maximum database size specified.</span></span> <span data-ttu-id="6ce2a-107">Llamar a **JetCreateDatabase2** con *cpgDatabaseSizeMax* establecido en cero es idéntico a llamar a [JETCREATEDATABASE](./jetcreatedatabase-function.md) con *szConnect* establecido en NULL.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-107">Calling **JetCreateDatabase2** with *cpgDatabaseSizeMax* set to zero is identical to calling [JetCreateDatabase](./jetcreatedatabase-function.md) with *szConnect* set to NULL.</span></span> <span data-ttu-id="6ce2a-108">Actualmente, se pueden crear hasta siete bases de datos por instancia.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-108">Currently up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="6ce2a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ce2a-109">Parameters</span></span>

<span data-ttu-id="6ce2a-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6ce2a-110">*sesid*</span></span>

<span data-ttu-id="6ce2a-111">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="6ce2a-112">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="6ce2a-112">*szFilename*</span></span>

<span data-ttu-id="6ce2a-113">Nombre de la base de datos que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-113">The name of the database to be created.</span></span>

<span data-ttu-id="6ce2a-114">*cpgDatabaseSizeMax*</span><span class="sxs-lookup"><span data-stu-id="6ce2a-114">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="6ce2a-115">Tamaño máximo, en páginas de base de datos, de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-115">The maximum size, in database pages, for the database.</span></span> <span data-ttu-id="6ce2a-116">El tamaño de página predeterminado de la base de datos es de 4 kilobytes y se puede cambiar con [JetSetSystemParameter](./jetsetsystemparameter-function.md) antes de crear una base de datos.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-116">The default database page size is 4 kilobytes, and can be changed with [JetSetSystemParameter](./jetsetsystemparameter-function.md) prior to creating a database.</span></span>

<span data-ttu-id="6ce2a-117">Pasar cero significa que no hay ningún máximo aplicado por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-117">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="6ce2a-118">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="6ce2a-118">*pdbid*</span></span>

<span data-ttu-id="6ce2a-119">Puntero a un búfer que, en una llamada correcta, contiene el identificador de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-119">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="6ce2a-120">En caso de error, el valor es indefinido.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-120">On failure, the value is undefined.</span></span>

<span data-ttu-id="6ce2a-121">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6ce2a-121">*grbit*</span></span>

<span data-ttu-id="6ce2a-122">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-122">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ce2a-123">Value</span><span class="sxs-lookup"><span data-stu-id="6ce2a-123">Value</span></span></p></th>
<th><p><span data-ttu-id="6ce2a-124">Significado</span><span class="sxs-lookup"><span data-stu-id="6ce2a-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-125">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="6ce2a-125">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-126">De forma predeterminada, si se llama a <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> o <strong>JetCreateDatabase2</strong> y la base de datos ya existe, se producirá un error en la llamada a la API y no se sobrescribirá la base de datos original.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-126">By default, if <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> or <strong>JetCreateDatabase2</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="6ce2a-127">JET_bitDbOverwriteExisting cambia este comportamiento y la antigua base de datos se sobrescribirá con otra nueva.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-127">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="6ce2a-128">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-128">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ce2a-129">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="6ce2a-129">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-130">JET_bitDbRecoveryOff desactiva el registro.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-130">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="6ce2a-131">La configuración de este bit pierde la capacidad de reproducir los archivos de registro y de recuperar la base de datos a un estado utilizable coherente después de un evento catastrófico.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-131">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-132">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="6ce2a-132">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-133">Al establecer JET_bitDbShadowingOff se deshabilitará la duplicación de algunas estructuras de base de datos internas (sombreado).</span><span class="sxs-lookup"><span data-stu-id="6ce2a-133">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="6ce2a-134">La duplicación de estas estructuras se realiza para lograr resistencia, por lo que la configuración de JET_bitDbShadowingOff quitará esa resistencia.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-134">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6ce2a-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ce2a-135">Return Value</span></span>

<span data-ttu-id="6ce2a-136">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6ce2a-137">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6ce2a-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ce2a-138">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6ce2a-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="6ce2a-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ce2a-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6ce2a-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-141">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ce2a-142">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="6ce2a-142">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-143">La base de datos denominada en <em>szFilename</em> ya existe.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-143">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="6ce2a-144">Cuando se devuelve este error, la base de datos no se adjunta.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-144">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-145">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="6ce2a-145">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-146">Se puede devolver si se solicitó acceso exclusivo, pero no se pudo conceder o si otra sesión ya ha abierto la base de datos de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-146">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ce2a-147">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="6ce2a-147">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-148">Se devuelve cuando <em>cpgDatabaseSizeMax</em> es mayor que el número máximo de páginas permitidas en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-148">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="6ce2a-149">El máximo actual es 2147483646 (0x7ffffffe).</span><span class="sxs-lookup"><span data-stu-id="6ce2a-149">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-150">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="6ce2a-150">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-151">Se proporcionó una ruta de acceso no válida en <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-151">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="6ce2a-152"><em>szFilename</em> debe ser distinto de NULL.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-152"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="6ce2a-153">De forma predeterminada, <em>szFilename</em> debe apuntar a un directorio que exista.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-153">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="6ce2a-154">La ruta de acceso se creará si se establece <em>JET_paramCreatePathIfNotExist</em> (vea <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span><span class="sxs-lookup"><span data-stu-id="6ce2a-154">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ce2a-155">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="6ce2a-155">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-156">Indica que otra sesión ya ha abierto la base de datos de forma exclusiva (mediante JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="6ce2a-156">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-157">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="6ce2a-157">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-158">La base de datos no se adjuntó previamente (vea <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="6ce2a-158">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ce2a-159">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6ce2a-159">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-160">Una sesión diferente ya ha adjuntado el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-160">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-161">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="6ce2a-161">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-162">Se intentó crear una base de datos mientras estaba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-162">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ce2a-163">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="6ce2a-163">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-164">Se intentó abrir un archivo que no es un archivo de base de datos válido.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-164">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-165">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="6ce2a-165">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-166">Se intentó abrir más de una base de datos y se estableció JET_paramOneDatabasePerSession.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-166">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="6ce2a-167">Consulte <a href="gg294139(v=exchg.10).md">parámetros del sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-167">See <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ce2a-168">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="6ce2a-168">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-169">El sistema se quedó sin recursos.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-169">The system ran low on resources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-170">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="6ce2a-170">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-171">Solo se puede asociar un número finito de bases de datos por instancia.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-171">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="6ce2a-172">Actualmente, el límite es de siete bases de datos por instancia.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-172">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ce2a-173">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="6ce2a-173">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-174">Una advertencia no fatal que indica que el archivo de base de datos ya se ha adjuntado a esta sesión.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-174">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-175">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="6ce2a-175">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6ce2a-176">JET_wrnFileOpenReadOnly indica que el archivo estaba asociado de solo lectura, pero <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> no pasó JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-176">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="6ce2a-177">La base de datos todavía está abierta con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-177">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="6ce2a-178">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ce2a-178">Remarks</span></span>

<span data-ttu-id="6ce2a-179">Si la base de datos especificada en *szFilename* existe y no se ha pasado JET_bitDbOverwriteExisting, se producirá un error en la llamada a la API.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-179">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="6ce2a-180">Si se pasó JET_bitDbOverwriteExisting, primero se eliminará el archivo de base de datos anterior.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-180">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="6ce2a-181">Si la API crea un archivo de base de datos y, a continuación, llega a otro error, se limpiará y se eliminará el archivo.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-181">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="6ce2a-182">**JetCreateDatabase2** abrirá implícitamente la base de datos.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-182">**JetCreateDatabase2** will implicitly open the database.</span></span> <span data-ttu-id="6ce2a-183">Posteriormente, no es necesario llamar a [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="6ce2a-183">It is not necessary to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="6ce2a-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ce2a-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-185"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6ce2a-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6ce2a-186">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-186">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ce2a-187"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6ce2a-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6ce2a-188">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-188">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-189"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6ce2a-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6ce2a-190">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-190">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ce2a-191"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="6ce2a-191"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6ce2a-192">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-192">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ce2a-193"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6ce2a-193"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6ce2a-194">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6ce2a-194">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ce2a-195"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6ce2a-195"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6ce2a-196">Se implementa como <strong>JetCreateDatabase2W</strong> (Unicode) y <strong>JetCreateDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6ce2a-196">Implemented as <strong>JetCreateDatabase2W</strong> (Unicode) and <strong>JetCreateDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6ce2a-197">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6ce2a-197">See Also</span></span>

[<span data-ttu-id="6ce2a-198">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="6ce2a-198">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="6ce2a-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6ce2a-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6ce2a-200">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="6ce2a-200">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="6ce2a-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6ce2a-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6ce2a-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6ce2a-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6ce2a-203">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="6ce2a-203">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="6ce2a-204">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="6ce2a-204">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="6ce2a-205">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="6ce2a-205">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="6ce2a-206">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="6ce2a-206">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="6ce2a-207">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="6ce2a-207">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="6ce2a-208">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="6ce2a-208">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
