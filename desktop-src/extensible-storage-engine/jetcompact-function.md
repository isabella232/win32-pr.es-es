---
description: 'Más información acerca de: JetCompact (función)'
title: JetCompact función)
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebac7fe4f09a6c4456b5370af03ea24f2334cff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716168"
---
# <a name="jetcompact-function"></a><span data-ttu-id="5e2c9-103">JetCompact función)</span><span class="sxs-lookup"><span data-stu-id="5e2c9-103">JetCompact Function</span></span>


<span data-ttu-id="5e2c9-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5e2c9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcompact-function"></a><span data-ttu-id="5e2c9-105">JetCompact función)</span><span class="sxs-lookup"><span data-stu-id="5e2c9-105">JetCompact Function</span></span>

<span data-ttu-id="5e2c9-106">La función **JetCompact** realiza una copia de una base de datos existente.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-106">The **JetCompact** function makes a copy of an existing database.</span></span> <span data-ttu-id="5e2c9-107">La copia se compacta con un estado óptimo para su uso.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-107">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="5e2c9-108">Los datos de los datos copiados se empaquetarán de acuerdo con las medidas elegidas para los índices en la creación de índices.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-108">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="5e2c9-109">De esta manera, los datos comprimidos se pueden almacenar de la forma más densa posible.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-109">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="5e2c9-110">Como alternativa, los datos compactos pueden reservar espacio para las inserciones de índice o el crecimiento de registros posteriores.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-110">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="5e2c9-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e2c9-111">Parameters</span></span>

<span data-ttu-id="5e2c9-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5e2c9-112">*sesid*</span></span>

<span data-ttu-id="5e2c9-113">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-113">The session to use for this call.</span></span>

<span data-ttu-id="5e2c9-114">*szDatabaseSrc*</span><span class="sxs-lookup"><span data-stu-id="5e2c9-114">*szDatabaseSrc*</span></span>

<span data-ttu-id="5e2c9-115">La base de datos de origen que se compactará.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-115">The source database that will be compacted.</span></span>

<span data-ttu-id="5e2c9-116">*szDatabaseDest*</span><span class="sxs-lookup"><span data-stu-id="5e2c9-116">*szDatabaseDest*</span></span>

<span data-ttu-id="5e2c9-117">Nombre que se va a utilizar para la base de datos compactada.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-117">The name to use for the compacted database.</span></span>

<span data-ttu-id="5e2c9-118">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="5e2c9-118">*pfnStatus*</span></span>

<span data-ttu-id="5e2c9-119">Función de devolución de llamada a la que se puede llamar periódicamente a través de la operación de compactación de base de datos para informar del progreso.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-119">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<span data-ttu-id="5e2c9-120">*pconvert*</span><span class="sxs-lookup"><span data-stu-id="5e2c9-120">*pconvert*</span></span>

<span data-ttu-id="5e2c9-121">Puntero que se usa para designar un archivo DLL de ESE alternativo que se puede usar para leer la base de datos de origen y para proporcionar parámetros opcionales para una operación **JetCompact** que está convirtiendo una base de datos de un formato de versión anterior a posterior.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-121">A pointer used to designate an alternative ESE DLL that can be used to read the source database, and to provide optional parameters for a **JetCompact** operation that is converting a database from an earlier to a later version format.</span></span> <span data-ttu-id="5e2c9-122">Esta característica se ha suspendido en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-122">This feature was discontinued in Windows Server 2003.</span></span>

<span data-ttu-id="5e2c9-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5e2c9-123">*grbit*</span></span>

<span data-ttu-id="5e2c9-124">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-124">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e2c9-125">Value</span><span class="sxs-lookup"><span data-stu-id="5e2c9-125">Value</span></span></p></th>
<th><p><span data-ttu-id="5e2c9-126">Significado</span><span class="sxs-lookup"><span data-stu-id="5e2c9-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e2c9-127">JET_bitCompactRepair</span><span class="sxs-lookup"><span data-stu-id="5e2c9-127">JET_bitCompactRepair</span></span></p></td>
<td><p><span data-ttu-id="5e2c9-128">Se usa cuando se sabe que la base de datos de origen está dañada.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-128">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="5e2c9-129">Habilita un conjunto completo de nuevos comportamientos para recuperar tantos datos como sea posible de la base de datos de origen.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-129">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="5e2c9-130"><strong>JetCompact</strong> con este conjunto de opciones puede devolver JET_errSuccess pero no copiar todos los datos creados en la base de datos de origen.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-130"><strong>JetCompact</strong> with this option set may return JET_errSuccess but not copy all of the data created in the source database.</span></span> <span data-ttu-id="5e2c9-131">Se omitirán los datos que se encontraban en partes dañadas de la base de datos de origen.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-131">Data that was in damaged portions of the source database will be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e2c9-132">JET_bitCompactStats</span><span class="sxs-lookup"><span data-stu-id="5e2c9-132">JET_bitCompactStats</span></span></p></td>
<td><p><span data-ttu-id="5e2c9-133">Hace que <strong>JetCompact</strong> vuelque las estadísticas de la base de datos de origen en un archivo denominado DFRGINFO.TXT.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-133">Causes <strong>JetCompact</strong> to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="5e2c9-134">Las estadísticas incluyen el nombre de cada tabla en la base de datos de origen, el número de filas de cada tabla, el tamaño total en bytes de todas las filas de cada tabla, el tamaño total en bytes de todas las columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> que eran lo suficientemente grandes como para almacenarse por separado del registro, el número de páginas hoja del índice clúster y el número de páginas</span><span class="sxs-lookup"><span data-stu-id="5e2c9-134">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="5e2c9-135">Además, también se vuelcan todas las estadísticas de Resumen, incluido el tamaño de la base de datos de origen, la base de datos de destino, el tiempo necesario para la compactación de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-135">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5e2c9-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e2c9-136">Return Value</span></span>

<span data-ttu-id="5e2c9-137">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-137">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5e2c9-138">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5e2c9-138">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e2c9-139">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5e2c9-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="5e2c9-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e2c9-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e2c9-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5e2c9-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5e2c9-142">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-142">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e2c9-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5e2c9-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5e2c9-144">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e2c9-145">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="5e2c9-145">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="5e2c9-146">Se ha proporcionado un puntero <em>pconvert</em> que no es null, pero la versión de ese que se está usando no admite la característica Convert.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-146">A non-NULL <em>pconvert</em> pointer has been supplied but the version of ESE being used does not support the convert feature.</span></span> <span data-ttu-id="5e2c9-147">Esta característica se ha quitado de la versión 2003 de Windows Server de ESE.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-147">This feature was removed in the Windows Server 2003 version of ESE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e2c9-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5e2c9-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5e2c9-149">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="5e2c9-150">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e2c9-151">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="5e2c9-151">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="5e2c9-152">La sesión que realiza la llamada se encuentra dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-152">The calling session is within a transaction.</span></span> <span data-ttu-id="5e2c9-153">Una sesión fuera de cualquier transacción debe llamar a <strong>JetCompact</strong> .</span><span class="sxs-lookup"><span data-stu-id="5e2c9-153"><strong>JetCompact</strong> must be called by a session outside of any transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e2c9-154">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5e2c9-154">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5e2c9-155">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-155">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e2c9-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5e2c9-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5e2c9-157">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e2c9-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="5e2c9-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="5e2c9-159">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="5e2c9-160">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e2c9-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5e2c9-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5e2c9-162">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5e2c9-163">Si se ejecuta correctamente, la base de datos de origen se copia en la base de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-163">On success, the source database is copied to the destination database.</span></span> <span data-ttu-id="5e2c9-164">La base de datos de destino está en un estado óptimo; por ejemplo, todos los índices de tabla se encuentran en un espacio de disco lógico adyacente.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-164">The destination database is in an optimal state, for example, all table indexes are located in adjacent logical disk space.</span></span> <span data-ttu-id="5e2c9-165">Cada página de índice se rellenará hasta la cantidad configurada cuando los índices se crearon originalmente en la base de datos de origen.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-165">Each index page is padded to the amount configured when the indexes were originally created in the source database.</span></span> <span data-ttu-id="5e2c9-166">Toda la configuración de datos y metadatos se copia con plena fidelidad, a menos que se haya especificado la opción de reparación.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-166">All data and metadata settings are copied with full fidelity, unless the repair option was specified.</span></span> <span data-ttu-id="5e2c9-167">Si se ha especificado la opción de reparación, es posible que no se hayan copiado algunos datos de la base de datos de origen.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-167">If the repair option was specified, some data from the source database may not have been copied.</span></span>

<span data-ttu-id="5e2c9-168">En caso de error, la base de datos de destino puede existir pero no es una copia completa de la base de datos de origen.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-168">On failure, the destination database may exist but is not a full copy of the source database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5e2c9-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e2c9-169">Remarks</span></span>

<span data-ttu-id="5e2c9-170">La compactación de una base de datos también se usa para actualizar una base de datos de un formato de versión anterior a una versión más moderna.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-170">Compacting a database is also used to upgrade a database from an earlier version format to a more modern version.</span></span> <span data-ttu-id="5e2c9-171">Un parámetro opcional es *pconvert*, que contiene una estructura que puede contener una descripción para un archivo dll de una versión anterior que se utilizará para leer el formato de la base de datos de origen.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-171">An optional parameter is *pconvert*, which contains a structure that can hold a description for an earlier version DLL to use for reading the source database format.</span></span> <span data-ttu-id="5e2c9-172">Esta característica se ha suspendido en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-172">This feature was discontinued in Windows Server 2003.</span></span> <span data-ttu-id="5e2c9-173">Después de Windows Server 2003, las nuevas versiones de ESE siempre pueden leer versiones anteriores del formato de la base de datos y, por lo tanto, esta característica no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-173">Subsequent to Windows Server 2003, new versions of ESE are always able to read older versions of the database format and hence this feature is not needed.</span></span>

<span data-ttu-id="5e2c9-174">La densidad deseada de datos después de una operación de compactación se especifica cuando se crean tablas e índices.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-174">The desired density of data after a compact operation is specified when tables and indexes are created.</span></span> <span data-ttu-id="5e2c9-175">La densidad debe estar comprendida entre el 20% y el 100%.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-175">The density must be between 20% and 100%.</span></span> <span data-ttu-id="5e2c9-176">Si una base de datos se lee principalmente y no se actualiza, las aplicaciones establecerán la densidad en 100% para reducir el número de operaciones de e/s durante el procesamiento de la consulta.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-176">If a database is primarily read and not updated, applications will set the density to 100% to reduce the number of I/O operations during query processing.</span></span> <span data-ttu-id="5e2c9-177">Sin embargo, si los datos se actualizan con frecuencia con operaciones que aumentan el tamaño de los datos almacenados junto con el registro, o cuando se insertan nuevos datos con frecuencia, la aplicación elegirá una densidad inferior para que las actualizaciones encuentren con mayor frecuencia los recursos necesarios disponibles.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-177">However, if the data is updated frequently with operations that increase the size of data stored together with the record, or new data is frequently inserted, the application will choose a lower density so that updates will more often find needed resources available.</span></span> <span data-ttu-id="5e2c9-178">La operación de compactar la base de datos hace que la base de datos se disponga idealmente según el relleno elegido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-178">The operation of compacting the database causes the database to be ideally laid out according to the fill chosen by the application.</span></span>

<span data-ttu-id="5e2c9-179">La compactación de base de datos es una operación sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-179">Database compaction is an off-line operation.</span></span> <span data-ttu-id="5e2c9-180">No se puede realizar mientras la base de datos está en uso.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-180">It cannot be performed while the database is in use.</span></span> <span data-ttu-id="5e2c9-181">Como resultado, normalmente se hace como parte de un proceso de compilación para desarrollar una aplicación que entrega un conjunto de datos como parte de sí mismo.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-181">As a result, it is typically done as part of a build process of developing an application which delivers a data set as part of itself.</span></span>

<span data-ttu-id="5e2c9-182">La compactación de base de datos sin conexión toca cada bit de datos de una base de datos y se puede usar como un medio para comprobar la coherencia de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-182">Offline database compaction touches every bit of data in a database and can be used as a means of checking the consistency of a database.</span></span> <span data-ttu-id="5e2c9-183">Si una base de datos es sospechosa, se puede compactar.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-183">If a database is suspect then it can be compacted.</span></span> <span data-ttu-id="5e2c9-184">Si no se encuentra ningún error en la compactación, se sabe que la base de datos está en un estado válido para ESE.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-184">If no error is found from compaction then it will be known that the database is in a valid state for ESE.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5e2c9-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e2c9-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e2c9-186"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5e2c9-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5e2c9-187">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e2c9-188"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5e2c9-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5e2c9-189">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e2c9-190"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5e2c9-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5e2c9-191">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e2c9-192"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="5e2c9-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5e2c9-193">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e2c9-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5e2c9-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5e2c9-195">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5e2c9-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e2c9-196"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5e2c9-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5e2c9-197">Se implementa como <strong>JetCompactW</strong> (Unicode) y <strong>JetCompactA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5e2c9-197">Implemented as <strong>JetCompactW</strong> (Unicode) and <strong>JetCompactA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5e2c9-198">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5e2c9-198">See Also</span></span>

[<span data-ttu-id="5e2c9-199">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="5e2c9-199">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="5e2c9-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5e2c9-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5e2c9-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5e2c9-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5e2c9-202">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="5e2c9-202">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="5e2c9-203">JetStopService</span><span class="sxs-lookup"><span data-stu-id="5e2c9-203">JetStopService</span></span>](./jetstopservice-function.md)
