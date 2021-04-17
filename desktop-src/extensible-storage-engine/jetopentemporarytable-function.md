---
description: 'Más información acerca de: JetOpenTemporaryTable (función)'
title: JetOpenTemporaryTable función)
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2335f6d6426b321d5db55b4ed005c6220484d509
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697443"
---
# <a name="jetopentemporarytable-function"></a><span data-ttu-id="b1f16-103">JetOpenTemporaryTable función)</span><span class="sxs-lookup"><span data-stu-id="b1f16-103">JetOpenTemporaryTable Function</span></span>


<span data-ttu-id="b1f16-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b1f16-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemporarytable-function"></a><span data-ttu-id="b1f16-105">JetOpenTemporaryTable función)</span><span class="sxs-lookup"><span data-stu-id="b1f16-105">JetOpenTemporaryTable Function</span></span>

<span data-ttu-id="b1f16-106">La función **JetOpenTemporaryTable** crea una tabla volátil con un índice único que se puede usar para almacenar y recuperar registros, al igual que una tabla normal que se crea a través de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="b1f16-106">The **JetOpenTemporaryTable** function creates a volatile table with a single index that can be used to store and retrieve records, just like an ordinary table that is created via [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

<span data-ttu-id="b1f16-107">**Windows Vista:**  **JetOpenTemporaryTable** se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b1f16-107">**Windows Vista:**  **JetOpenTemporaryTable** is introduced in Windows Vista.</span></span>

<span data-ttu-id="b1f16-108">Las tablas temporales son más rápidas que las normales debido a su naturaleza volátil.</span><span class="sxs-lookup"><span data-stu-id="b1f16-108">Temporary tables are faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="b1f16-109">Pueden ordenar y realizar rápidamente la eliminación de duplicados en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial.</span><span class="sxs-lookup"><span data-stu-id="b1f16-109">They can quickly sort and perform duplicate removal on record sets when they are accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a><span data-ttu-id="b1f16-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1f16-110">Parameters</span></span>

<span data-ttu-id="b1f16-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b1f16-111">*sesid*</span></span>

<span data-ttu-id="b1f16-112">La sesión que se utilizará para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="b1f16-112">The session that will be used for this call.</span></span>

<span data-ttu-id="b1f16-113">*popentemporarytable*</span><span class="sxs-lookup"><span data-stu-id="b1f16-113">*popentemporarytable*</span></span>

<span data-ttu-id="b1f16-114">Puntero a una estructura de [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) que contiene la descripción de la tabla temporal que se va a crear en la entrada.</span><span class="sxs-lookup"><span data-stu-id="b1f16-114">A pointer to a [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) structure that contains the description of the temporary table to create on input.</span></span> <span data-ttu-id="b1f16-115">Después de una llamada correcta, la estructura contiene el identificador de la tabla temporal y las identificaciones de las columnas.</span><span class="sxs-lookup"><span data-stu-id="b1f16-115">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span>

### <a name="return-value"></a><span data-ttu-id="b1f16-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1f16-116">Return Value</span></span>

<span data-ttu-id="b1f16-117">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="b1f16-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b1f16-118">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b1f16-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1f16-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b1f16-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="b1f16-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1f16-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b1f16-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b1f16-122">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b1f16-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f16-123">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="b1f16-123">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="b1f16-124">No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</span><span class="sxs-lookup"><span data-stu-id="b1f16-124">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="b1f16-125"><strong>JetOpenTemporaryTable</strong> puede devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host está demasiado fragmentado.</span><span class="sxs-lookup"><span data-stu-id="b1f16-125"><strong>JetOpenTemporaryTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="b1f16-126">El administrador de tablas temporales asignará un fragmento de espacio de direcciones de 1 MB para cada tabla temporal creada independientemente de la cantidad de datos que se almacenen.</span><span class="sxs-lookup"><span data-stu-id="b1f16-126">The temporary table manager will allocates a 1 MB chunk of address space for every temporary table created regardless of the amount of data is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b1f16-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b1f16-128">Uno de los parámetros proporcionados contenía un valor inesperado o la combinación de varios valores de parámetro produjo un resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="b1f16-128">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="b1f16-129">Este error lo devuelve <strong>JetOpenTemporaryTable</strong> en las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="b1f16-129">This error is returned by <strong>JetOpenTemporaryTable</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="b1f16-130">El miembro <strong>cbStruct</strong> de la estructura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> no se corresponde con una versión de esta estructura compatible con esa versión del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="b1f16-130">The <strong>cbStruct</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure does not correspond to a version of this structure that is supported by that version of the database engine</span></span></p></li>
<li><p><span data-ttu-id="b1f16-131">El miembro <strong>cbKeyMost</strong> de la estructura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> es menor que JET_cbKeyMostMin.</span><span class="sxs-lookup"><span data-stu-id="b1f16-131">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is less than JET_cbKeyMostMin.</span></span></p></li>
<li><p><span data-ttu-id="b1f16-132">El miembro <strong>cbKeyMost</strong> de la estructura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> es mayor que el mayor valor admitido para el tamaño de página de la base de datos de la instancia (JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="b1f16-132">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than the largest supported value for the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="b1f16-133">Vea el parámetro JET_paramKeyMost en la lista de <a href="gg269241(v=exchg.10).md">parámetros informativos</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b1f16-133">See the JET_paramKeyMost parameter in the list of <a href="gg269241(v=exchg.10).md">Informational Parameters</a> for more information.</span></span></p></li>
<li><p><span data-ttu-id="b1f16-134">El miembro cbVarSegMac de la estructura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> es mayor que el miembro <strong>cbKeyMost</strong> .</span><span class="sxs-lookup"><span data-stu-id="b1f16-134">The cbVarSegMac member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than The <strong>cbKeyMost</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f16-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b1f16-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b1f16-136">No se puede completar la operación porque la instancia que estaba asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="b1f16-136">The operation cannot complete because the instance that was associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b1f16-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b1f16-138">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b1f16-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f16-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b1f16-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b1f16-140">No se puede completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="b1f16-140">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="b1f16-141"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b1f16-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b1f16-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b1f16-143">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="b1f16-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f16-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b1f16-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b1f16-145">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="b1f16-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b1f16-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b1f16-147">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="b1f16-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="b1f16-148"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b1f16-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f16-149">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="b1f16-149">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="b1f16-150">El identificador de sesión no es válido o hace referencia a una sesión cerrada.</span><span class="sxs-lookup"><span data-stu-id="b1f16-150">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="b1f16-151"><strong>Nota:</strong>  Este error no se devuelve en todas las circunstancias.</span><span class="sxs-lookup"><span data-stu-id="b1f16-151"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="b1f16-152">Los identificadores se validan solo en función del mejor esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="b1f16-152">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-153">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="b1f16-153">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="b1f16-154">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para abrir un nuevo cursor.</span><span class="sxs-lookup"><span data-stu-id="b1f16-154">The operation failed because the engine cannot allocate the resources that are required to open a new cursor.</span></span> <span data-ttu-id="b1f16-155">Los recursos de cursor se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="b1f16-155">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f16-156">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="b1f16-156">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="b1f16-157">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para crear una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b1f16-157">The operation failed because the engine cannot allocate the resources that are required to create a temporary table.</span></span> <span data-ttu-id="b1f16-158">Los recursos de tabla temporal se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="b1f16-158">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-159">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="b1f16-159">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="b1f16-160">Error de <strong>JetOpenTemporaryTable</strong> porque se especificó JET_bitTTForwardOnly y no se pudo crear la tabla temporal que se especificó mediante la optimización de solo avance.</span><span class="sxs-lookup"><span data-stu-id="b1f16-160"><strong>JetOpenTemporaryTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table that was specified could not be created using the forward-only optimization.</span></span></p>
<p><span data-ttu-id="b1f16-161"><strong>Windows Server 2003:</strong>  Este error solo lo devolverán Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b1f16-161"><strong>Windows Server 2003:</strong>  This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f16-162">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="b1f16-162">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="b1f16-163">Se intentó agregar demasiadas columnas a la tabla.</span><span class="sxs-lookup"><span data-stu-id="b1f16-163">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="b1f16-164">Una tabla no puede tener más de JET_ccolFixedMost columnas fijas, ni más de JET_ccolVarMost columnas de longitud variable, ni más de JET_ccolTaggedMost columnas etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="b1f16-164">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-165">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="b1f16-165">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="b1f16-166">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para almacenar en caché el esquema de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b1f16-166">The operation failed because the engine cannot allocate the resources that are required to cache the schema of the table.</span></span> <span data-ttu-id="b1f16-167">Para configurar el número de tablas que tienen esquemas que se pueden almacenar en caché, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="b1f16-167">To configure the number of tables that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f16-168">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="b1f16-168">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="b1f16-169">El miembro <strong>CP</strong> de la estructura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se ha establecido en una página de códigos válida.</span><span class="sxs-lookup"><span data-stu-id="b1f16-169">The <strong>cp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="b1f16-170">Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="b1f16-170">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="b1f16-171">Un valor de 0 significa que se usará el valor predeterminado (Inglés, 1252).</span><span class="sxs-lookup"><span data-stu-id="b1f16-171">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-172">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="b1f16-172">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="b1f16-173">El miembro <strong>coltyp</strong> de la <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> no se ha establecido en un tipo de columna válido.</span><span class="sxs-lookup"><span data-stu-id="b1f16-173">The <strong>coltyp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f16-174">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="b1f16-174">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="b1f16-175">No se pudo crear el índice porque se intentó usar un ID. de configuración regional no válido.</span><span class="sxs-lookup"><span data-stu-id="b1f16-175">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="b1f16-176">Es posible que el ID. de configuración regional no sea válido o que el paquete de idioma asociado no esté instalado.</span><span class="sxs-lookup"><span data-stu-id="b1f16-176">The locale ID might be either completely invalid or the associated language pack might not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-177">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="b1f16-177">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="b1f16-178">No se pudo crear el índice porque se intentó usar un conjunto no válido de marcas de normalización.</span><span class="sxs-lookup"><span data-stu-id="b1f16-178">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span></p>
<p><span data-ttu-id="b1f16-179"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b1f16-179"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p>
<p><span data-ttu-id="b1f16-180"><strong>Windows 2000:</strong>  En Windows 2000, las marcas de normalización no válidas producirán JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="b1f16-180"><strong>Windows 2000:</strong>  On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f16-181">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="b1f16-181">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="b1f16-182">No se pudo crear el índice porque se especificó una definición de índice no válida.</span><span class="sxs-lookup"><span data-stu-id="b1f16-182">The index could not be created because an invalid index definition was specified.</span></span> <span data-ttu-id="b1f16-183"><strong>JetOpenTemporaryTable</strong> devolverá este error en las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="b1f16-183"><strong>JetOpenTemporaryTable</strong> will return this error under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="b1f16-184">Se especifica la configuración regional independiente del idioma.</span><span class="sxs-lookup"><span data-stu-id="b1f16-184">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="b1f16-185">Se especifica un conjunto no válido de marcas de normalización.</span><span class="sxs-lookup"><span data-stu-id="b1f16-185">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="b1f16-186"><strong>Windows 2000:</strong>  Este error solo lo devolverá Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b1f16-186"><strong>Windows 2000:</strong>  This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-187">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="b1f16-187">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="b1f16-188">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para almacenar en memoria caché los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b1f16-188">The operation failed because the engine cannot allocate the resources that are required to cache the indexes of the table.</span></span> <span data-ttu-id="b1f16-189">Para configurar el número de índices que tienen esquemas que se pueden almacenar en caché, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="b1f16-189">To configure the number of indexes that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1f16-190">Si se ejecuta correctamente, se devolverá un cursor abierto en la tabla temporal recién creada.</span><span class="sxs-lookup"><span data-stu-id="b1f16-190">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="b1f16-191">El estado de la base de datos temporal se preparará para contener la nueva tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b1f16-191">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="b1f16-192">El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="b1f16-192">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="b1f16-193">En caso de error, no se creará la tabla temporal y no se devolverá un cursor.</span><span class="sxs-lookup"><span data-stu-id="b1f16-193">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="b1f16-194">Se puede cambiar el estado de la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="b1f16-194">The state of the temporary database can be changed.</span></span> <span data-ttu-id="b1f16-195">El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="b1f16-195">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b1f16-196">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1f16-196">Remarks</span></span>

<span data-ttu-id="b1f16-197">Las tablas temporales no admiten el complemento completo de las opciones de definición de columna que normalmente admite el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="b1f16-197">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="b1f16-198">De hecho, solo se admiten JET_bitColumnFixed y JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="b1f16-198">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="b1f16-199">Esto significa que no es posible crear una columna de incremento automático, versión o multivalor en una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b1f16-199">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="b1f16-200">Por último, no se admiten las columnas de actualización de custodia porque solo se pueden usar en una sesión a la vez.</span><span class="sxs-lookup"><span data-stu-id="b1f16-200">Finally, escrow update columns are not supported because they can only be used by one session at a time.</span></span> <span data-ttu-id="b1f16-201">Si se solicita alguna de estas opciones, se omitirán.</span><span class="sxs-lookup"><span data-stu-id="b1f16-201">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="b1f16-202">Las tablas temporales no admiten valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="b1f16-202">Temporary tables do not support default values.</span></span> <span data-ttu-id="b1f16-203">Si se proporciona una definición de columna que contiene una especificación de valor predeterminado, se omitirá esa especificación.</span><span class="sxs-lookup"><span data-stu-id="b1f16-203">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="b1f16-204">Las tablas temporales se devuelven al autor de la llamada como resultado de muchas funciones de ESE diferentes.</span><span class="sxs-lookup"><span data-stu-id="b1f16-204">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="b1f16-205">Por ejemplo, [JetGetIndexInfo](./jetgetindexinfo-function.md) con el conjunto de opciones JET_IdxInfo devolverá una tabla temporal que contenga una lista de todas las columnas de clave de un índice determinado.</span><span class="sxs-lookup"><span data-stu-id="b1f16-205">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="b1f16-206">Las tablas temporales siguen las mismas reglas del ciclo de vida que las tablas temporales normales, como se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="b1f16-206">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="b1f16-207">El motor de base de datos también usa internamente las tablas temporales para muchas tareas.</span><span class="sxs-lookup"><span data-stu-id="b1f16-207">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="b1f16-208">Lo más importante de estas tareas es la creación de un índice en una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="b1f16-208">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="b1f16-209">Se utilizará una tabla temporal para ordenar las claves de índice que se usan para construir ese índice.</span><span class="sxs-lookup"><span data-stu-id="b1f16-209">A temporary table will be used to sort the index keys that are used to construct that index.</span></span>

<span data-ttu-id="b1f16-210">Todas las tablas temporales se almacenan en la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="b1f16-210">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="b1f16-211">La base de datos temporal es un archivo de base de datos Especial que se mantiene durante la vigencia de una instancia de ESE y se elimina cuando se cierra o se reinicia la instancia.</span><span class="sxs-lookup"><span data-stu-id="b1f16-211">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="b1f16-212">La ubicación de la base de datos temporal se puede configurar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b1f16-212">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="b1f16-213">La selección de ubicación de la base de datos temporal en el disco en relación con los archivos de registro de transacciones y los archivos de base de datos puede ser importante si la aplicación hace un uso intensivo de tablas temporales o crea índices con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="b1f16-213">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="b1f16-214">El ciclo de vida de una tabla temporal está asociado a los cursores que hacen referencia a él.</span><span class="sxs-lookup"><span data-stu-id="b1f16-214">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="b1f16-215">Si se cierran todos los cursores que hacen referencia a una tabla temporal, ya sea implícita o explícitamente, se eliminará la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b1f16-215">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="b1f16-216">Si una tabla temporal se crea dentro de una transacción y esa transacción se revierte posteriormente, se eliminará la tabla temporal, ya que todos los cursores que hagan referencia a ella en este momento se cerrarán implícitamente.</span><span class="sxs-lookup"><span data-stu-id="b1f16-216">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="b1f16-217">Los nuevos cursores solo pueden hacer referencia a una tabla temporal mediante el uso de [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="b1f16-217">New cursors can reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="b1f16-218">En este caso, los nuevos cursores se colocarán en la primera entrada de índice de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b1f16-218">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="b1f16-219">[JetDupCursor](./jetdupcursor-function.md) solo funcionará durante ciertas fases de uso de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b1f16-219">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="b1f16-220">Para obtener más información, consulte las notas sobre las funcionalidades de cursor de tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b1f16-220">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="b1f16-221">No es posible hacer referencia a una tabla temporal de más de una sesión a la vez.</span><span class="sxs-lookup"><span data-stu-id="b1f16-221">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="b1f16-222">**PRECAUCIÓN**  Hay un problema importante en [JetDupCursor](./jetdupcursor-function.md) que afecta a las tablas temporales.</span><span class="sxs-lookup"><span data-stu-id="b1f16-222">**Caution**  There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="b1f16-223">Si se realiza un intento de duplicar una tabla temporal que está en modo de solo avance, el cursor resultante no se creará correctamente y dejará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="b1f16-223">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="b1f16-224">Todavía es seguro duplicar un cursor sobre una tabla temporal materializada.</span><span class="sxs-lookup"><span data-stu-id="b1f16-224">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="b1f16-225">El administrador de tablas temporales puede implementar una tabla temporal de tres maneras.</span><span class="sxs-lookup"><span data-stu-id="b1f16-225">The temporary table manager can implement a temporary table in three ways.</span></span> <span data-ttu-id="b1f16-226">El primer método consiste en mantener una tabla en memoria.</span><span class="sxs-lookup"><span data-stu-id="b1f16-226">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="b1f16-227">Esta estrategia es la más rápida, pero solo se puede usar para tablas pequeñas, simples y temporales.</span><span class="sxs-lookup"><span data-stu-id="b1f16-227">This strategy is the fastest but can only be used for small, simple, temporary tables.</span></span> <span data-ttu-id="b1f16-228">El segundo método consiste en crear una ordenación basada en disco que se puede controlar mediante un iterador de solo avance.</span><span class="sxs-lookup"><span data-stu-id="b1f16-228">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="b1f16-229">Esta estrategia solo se puede usar en determinadas circunstancias y es la manera más rápida de ordenar y quitar duplicados de un conjunto de datos muy grande.</span><span class="sxs-lookup"><span data-stu-id="b1f16-229">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="b1f16-230">El tercer método consiste en crear un árbol B + en la base de datos temporal para almacenar la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b1f16-230">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="b1f16-231">Esta estrategia es la más lenta, pero la más versátil, y se conoce como una tabla temporal materializada.</span><span class="sxs-lookup"><span data-stu-id="b1f16-231">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="b1f16-232">Estas estrategias se pueden usar en combinación para lograr en última instancia la funcionalidad solicitada de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b1f16-232">These strategies can be used in combination to ultimately achieve the functionality that is requested of the temporary table.</span></span>

<span data-ttu-id="b1f16-233">Cuando la tabla temporal no se materializa, se usa principalmente en dos fases principales.</span><span class="sxs-lookup"><span data-stu-id="b1f16-233">When the temporary table is not materialized then it is used primarily in two major phases.</span></span> <span data-ttu-id="b1f16-234">La primera fase es la fase de inserción en la que la tabla se rellena con su conjunto de datos inicial.</span><span class="sxs-lookup"><span data-stu-id="b1f16-234">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="b1f16-235">Durante esta fase, solo se permite la inserción de datos.</span><span class="sxs-lookup"><span data-stu-id="b1f16-235">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="b1f16-236">Esta fase finaliza cuando se realiza un intento de trasladar el cursor mediante [JetMove](./jetmove-function.md) o [JetSeek](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="b1f16-236">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="b1f16-237">La segunda fase es la fase de extracción de datos.</span><span class="sxs-lookup"><span data-stu-id="b1f16-237">The second phase is the data extraction phase.</span></span> <span data-ttu-id="b1f16-238">Durante esta fase, los datos que se almacenan en la tabla temporal se pueden extraer según las capacidades que se solicitaron cuando se creó la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b1f16-238">During this phase, the data that is stored in the temporary table can be extracted according to the capabilities that were requested when the temporary table was created.</span></span>

<span data-ttu-id="b1f16-239">**Funciones de cursor de tabla temporal**</span><span class="sxs-lookup"><span data-stu-id="b1f16-239">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="b1f16-240">Cuando se materializa la tabla temporal, el cursor tiene las siguientes capacidades, pero puede estar más limitado por las opciones que se solicitan:</span><span class="sxs-lookup"><span data-stu-id="b1f16-240">When the temporary table is materialized, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="b1f16-241">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b1f16-241">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="b1f16-242">JetDelete</span><span class="sxs-lookup"><span data-stu-id="b1f16-242">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="b1f16-243">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="b1f16-243">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="b1f16-244">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="b1f16-244">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="b1f16-245">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="b1f16-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="b1f16-246">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="b1f16-246">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="b1f16-247">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="b1f16-247">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="b1f16-248">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="b1f16-248">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="b1f16-249">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="b1f16-249">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="b1f16-250">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="b1f16-250">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="b1f16-251">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="b1f16-251">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="b1f16-252">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="b1f16-252">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="b1f16-253">JetMove</span><span class="sxs-lookup"><span data-stu-id="b1f16-253">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="b1f16-254">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="b1f16-254">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="b1f16-255">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="b1f16-255">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="b1f16-256">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="b1f16-256">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="b1f16-257">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="b1f16-257">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="b1f16-258">JetSeek</span><span class="sxs-lookup"><span data-stu-id="b1f16-258">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="b1f16-259">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="b1f16-259">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="b1f16-260">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="b1f16-260">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="b1f16-261">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="b1f16-261">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="b1f16-262">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="b1f16-262">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="b1f16-263">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="b1f16-263">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="b1f16-264">Cuando la tabla temporal no se materializa y se encuentra en la fase de inserción, el cursor tiene las siguientes capacidades, pero puede estar más limitado por las opciones que se solicitan:</span><span class="sxs-lookup"><span data-stu-id="b1f16-264">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="b1f16-265">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b1f16-265">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="b1f16-266">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="b1f16-266">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="b1f16-267">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="b1f16-267">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="b1f16-268">JetMove</span><span class="sxs-lookup"><span data-stu-id="b1f16-268">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="b1f16-269">**Nota:**  Provoca la transición a la fase de extracción.</span><span class="sxs-lookup"><span data-stu-id="b1f16-269">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="b1f16-270">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="b1f16-270">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="b1f16-271">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="b1f16-271">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="b1f16-272">JetSeek</span><span class="sxs-lookup"><span data-stu-id="b1f16-272">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="b1f16-273">**Nota:**  Provoca la transición a la fase de extracción.</span><span class="sxs-lookup"><span data-stu-id="b1f16-273">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="b1f16-274">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="b1f16-274">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="b1f16-275">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="b1f16-275">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="b1f16-276">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="b1f16-276">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="b1f16-277">Cuando la tabla temporal no se materializa y se encuentra en la fase de extracción, el cursor tiene las siguientes capacidades, pero puede estar más limitado por las opciones que se solicitan:</span><span class="sxs-lookup"><span data-stu-id="b1f16-277">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="b1f16-278">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b1f16-278">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="b1f16-279">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="b1f16-279">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="b1f16-280">**Nota:**  Si se realiza un intento de duplicar una tabla temporal que está en modo de solo avance, el cursor resultante no se creará correctamente y dejará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="b1f16-280">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="b1f16-281">Todavía es seguro duplicar un cursor sobre una tabla temporal materializada.</span><span class="sxs-lookup"><span data-stu-id="b1f16-281">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="b1f16-282">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="b1f16-282">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="b1f16-283">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="b1f16-283">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="b1f16-284">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="b1f16-284">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="b1f16-285">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="b1f16-285">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="b1f16-286">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="b1f16-286">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="b1f16-287">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="b1f16-287">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="b1f16-288">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="b1f16-288">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="b1f16-289">JetMove</span><span class="sxs-lookup"><span data-stu-id="b1f16-289">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="b1f16-290">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="b1f16-290">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="b1f16-291">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="b1f16-291">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="b1f16-292">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="b1f16-292">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="b1f16-293">JetSeek</span><span class="sxs-lookup"><span data-stu-id="b1f16-293">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="b1f16-294">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="b1f16-294">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="b1f16-295">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="b1f16-295">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="b1f16-296">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1f16-296">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-297"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b1f16-297"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b1f16-298">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b1f16-298">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f16-299"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b1f16-299"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b1f16-300">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b1f16-300">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-301"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b1f16-301"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b1f16-302">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="b1f16-302">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f16-303"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="b1f16-303"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b1f16-304">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b1f16-304">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f16-305"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b1f16-305"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b1f16-306">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b1f16-306">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b1f16-307">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b1f16-307">See Also</span></span>

[<span data-ttu-id="b1f16-308">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b1f16-308">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b1f16-309">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b1f16-309">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b1f16-310">JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="b1f16-310">JET_OPENTEMPORARYTABLE</span></span>](./jet-opentemporarytable-structure.md)  
[<span data-ttu-id="b1f16-311">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b1f16-311">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="b1f16-312">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="b1f16-312">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="b1f16-313">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="b1f16-313">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="b1f16-314">JetMove</span><span class="sxs-lookup"><span data-stu-id="b1f16-314">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="b1f16-315">JetRollback</span><span class="sxs-lookup"><span data-stu-id="b1f16-315">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="b1f16-316">JetSeek</span><span class="sxs-lookup"><span data-stu-id="b1f16-316">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="b1f16-317">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="b1f16-317">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="b1f16-318">Parámetros informativos</span><span class="sxs-lookup"><span data-stu-id="b1f16-318">Informational Parameters</span></span>](./informational-parameters.md)  
[<span data-ttu-id="b1f16-319">Parámetros temporales de base de datos</span><span class="sxs-lookup"><span data-stu-id="b1f16-319">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)
