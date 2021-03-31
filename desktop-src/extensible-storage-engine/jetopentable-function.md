---
description: 'Más información acerca de: JetOpenTable (función)'
title: Función JetOpenTable
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808431"
---
# <a name="jetopentable-function"></a><span data-ttu-id="fcfd4-103">Función JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="fcfd4-103">JetOpenTable Function</span></span>


<span data-ttu-id="fcfd4-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fcfd4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentable-function"></a><span data-ttu-id="fcfd4-105">Función JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="fcfd4-105">JetOpenTable Function</span></span>

<span data-ttu-id="fcfd4-106">La función **JetOpenTable** abre un cursor en una tabla creada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-106">The **JetOpenTable** function opens a cursor on a previously created table.</span></span>

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="fcfd4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcfd4-107">Parameters</span></span>

<span data-ttu-id="fcfd4-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="fcfd4-108">*sesid*</span></span>

<span data-ttu-id="fcfd4-109">Contexto de sesión de base de datos que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-109">The database session context to use.</span></span>

<span data-ttu-id="fcfd4-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="fcfd4-110">*dbid*</span></span>

<span data-ttu-id="fcfd4-111">Identificador de base de datos que se va a usar para buscar la tabla.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-111">The database identifier to use to find the table.</span></span>

<span data-ttu-id="fcfd4-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="fcfd4-112">*szTableName*</span></span>

<span data-ttu-id="fcfd4-113">Nombre de la tabla que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-113">The name of the table to open.</span></span>

<span data-ttu-id="fcfd4-114">*pvParameters*</span><span class="sxs-lookup"><span data-stu-id="fcfd4-114">*pvParameters*</span></span>

<span data-ttu-id="fcfd4-115">En desuso.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-115">Deprecated.</span></span> <span data-ttu-id="fcfd4-116">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-116">Set to **NULL**.</span></span>

<span data-ttu-id="fcfd4-117">*cbParameters*</span><span class="sxs-lookup"><span data-stu-id="fcfd4-117">*cbParameters*</span></span>

<span data-ttu-id="fcfd4-118">En desuso.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-118">Deprecated.</span></span> <span data-ttu-id="fcfd4-119">Se establece en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="fcfd4-119">Set to 0 (zero).</span></span>

<span data-ttu-id="fcfd4-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="fcfd4-120">*grbit*</span></span>

<span data-ttu-id="fcfd4-121">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fcfd4-122">Value</span><span class="sxs-lookup"><span data-stu-id="fcfd4-122">Value</span></span></p></th>
<th><p><span data-ttu-id="fcfd4-123">Significado</span><span class="sxs-lookup"><span data-stu-id="fcfd4-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcfd4-124">JET_bitTableDenyRead</span><span class="sxs-lookup"><span data-stu-id="fcfd4-124">JET_bitTableDenyRead</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-125">Otra sesión de base de datos no puede abrir la tabla para acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-125">The table cannot be opened for read-access by another database session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfd4-126">JET_bitTableDenyWrite</span><span class="sxs-lookup"><span data-stu-id="fcfd4-126">JET_bitTableDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-127">No se puede abrir la tabla para acceso de escritura en otra sesión de base de datos.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-127">The table cannot be opened for write-access by another database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfd4-128">JET_bitTableNoCache</span><span class="sxs-lookup"><span data-stu-id="fcfd4-128">JET_bitTableNoCache</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-129">No almacene en caché las páginas de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-129">Do not cache the pages for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfd4-130">JET_bitTablePermitDDL</span><span class="sxs-lookup"><span data-stu-id="fcfd4-130">JET_bitTablePermitDDL</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-131">Permite la modificación de DDL en las tablas marcadas como FixedDDL.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-131">Allows DDL modification on tables flagged as FixedDDL.</span></span> <span data-ttu-id="fcfd4-132">Esta opción debe usarse con la opción JET_bitTableDenyRead.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-132">This option must be used with the JET_bitTableDenyRead option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfd4-133">JET_bitTablePreread</span><span class="sxs-lookup"><span data-stu-id="fcfd4-133">JET_bitTablePreread</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-134">Proporciona una sugerencia que indica que la tabla probablemente no está en la caché del búfer y que la lectura previa puede ser beneficiosa para el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-134">Provides a hint that the table is probably not in the buffer cache, and that pre-reading may be beneficial to performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfd4-135">JET_bitTableReadOnly</span><span class="sxs-lookup"><span data-stu-id="fcfd4-135">JET_bitTableReadOnly</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-136">Solicita acceso de solo lectura a la tabla.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-136">Requests read-only access to the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfd4-137">JET_bitTableSequential</span><span class="sxs-lookup"><span data-stu-id="fcfd4-137">JET_bitTableSequential</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-138">La tabla se debe capturar de forma muy agresiva desde el disco, ya que la aplicación la examinará secuencialmente.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-138">The table should be very aggressively prefetched from disk because the application will be scanning it sequentially.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfd4-139">JET_bitTableUpdatable</span><span class="sxs-lookup"><span data-stu-id="fcfd4-139">JET_bitTableUpdatable</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-140">Solicita acceso de escritura a la tabla.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-140">Requests write-access to the table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fcfd4-141">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="fcfd4-141">*ptableid*</span></span>

<span data-ttu-id="fcfd4-142">Si se ejecuta correctamente, apunta al identificador de la tabla.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-142">On success, points to the identifier of the table.</span></span> <span data-ttu-id="fcfd4-143">En caso de error, el contenido de *ptableid* no está definido.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-143">On failure, the contents for *ptableid* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="fcfd4-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcfd4-144">Return Value</span></span>

<span data-ttu-id="fcfd4-145">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-145">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fcfd4-146">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fcfd4-146">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fcfd4-147">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fcfd4-147">Return code</span></span></p></th>
<th><p><span data-ttu-id="fcfd4-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="fcfd4-148">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcfd4-149">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fcfd4-149">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-150">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-150">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfd4-151">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="fcfd4-151">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-152"><em>DBID</em> no es un identificador de base de datos válido.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-152"><em>dbid</em> is not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfd4-153">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="fcfd4-153">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-154">Se pasó una combinación incorrecta de <em>grbit</em> .</span><span class="sxs-lookup"><span data-stu-id="fcfd4-154">A bad combination of <em>grbit</em> was passed in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfd4-155">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="fcfd4-155">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-156">El nombre proporcionado en <em>szTableName</em> no es válido.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-156">The name given in <em>szTableName</em> is invalid.</span></span></p>
<p><span data-ttu-id="fcfd4-157">Para obtener más información sobre los nombres de tabla válidos, vea el parámetro <em>szTableName</em> en <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-157">For more information about valid table names, see the <em>szTableName</em> parameter in <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfd4-158">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="fcfd4-158">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-159">Se intentó abrir una tabla que no existe en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-159">An attempt was made to open a table that does not exist in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfd4-160">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="fcfd4-160">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-161">No se pudo realizar la operación porque el motor no puede asignar los recursos necesarios para abrir un nuevo cursor.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-161">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="fcfd4-162">Consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-162">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfd4-163">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="fcfd4-163">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-164">Otra operación de base de datos está utilizando la tabla.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-164">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfd4-165">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="fcfd4-165">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-166">Una advertencia no grave que indica que el sistema está usando la tabla.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-166">A nonfatal warning indicating that the table is being used by the system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfd4-167">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="fcfd4-167">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-168">La tabla está bloqueada por otra operación de base de datos.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-168">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfd4-169">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="fcfd4-169">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="fcfd4-170">Se intentó abrir demasiadas tablas únicas a la vez.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-170">An attempt was made to open too many unique tables at once.</span></span> <span data-ttu-id="fcfd4-171">Consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-171">See the Remarks section.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="fcfd4-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcfd4-172">Remarks</span></span>

<span data-ttu-id="fcfd4-173">Las tablas abiertas con **JetOpenTable** normalmente se deben cerrar con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="fcfd4-173">Tables opened with **JetOpenTable** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="fcfd4-174">La excepción a esta regla se produce cuando se llama a **JetOpenTable** en una transacción y se revierte la transacción (con [JetRollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="fcfd4-174">The exception to this rule happens when **JetOpenTable** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="fcfd4-175">Cuando se revierte una transacción, la tabla se cierra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-175">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="fcfd4-176">En este caso, es un error cerrar la tabla con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="fcfd4-176">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="fcfd4-177">Es válido abrir tablas del sistema con **JetOpenTable** (por ejemplo, MSysObjects, MSysUnicodeFixup).</span><span class="sxs-lookup"><span data-stu-id="fcfd4-177">It is legal to open system tables with **JetOpenTable** (for example, MSysObjects, MSysUnicodeFixup).</span></span> <span data-ttu-id="fcfd4-178">El esquema de las tablas del sistema puede cambiar, por lo que no se recomienda el acceso a las tablas del sistema.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-178">The schema of the system tables may change, so accessing system tables is discouraged.</span></span> <span data-ttu-id="fcfd4-179">El número de tablas únicas que se pueden abrir simultáneamente se ve afectado directamente por *JET_paramMaxOpenTables*.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-179">The number of unique tables that can be opened simultaneously is affected directly by *JET_paramMaxOpenTables*.</span></span> <span data-ttu-id="fcfd4-180">Si la tabla está abierta actualmente, se creará un nuevo cursor en la tabla.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-180">If the table is currently open then a new cursor will be created on the table.</span></span> <span data-ttu-id="fcfd4-181">Los recursos de cursor se configuran mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con *JET_paramMaxCursors*.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-181">Cursor resources are configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxCursors*.</span></span> <span data-ttu-id="fcfd4-182">Consulte también [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="fcfd4-182">Also see [JetDupCursor](./jetdupcursor-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="fcfd4-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcfd4-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcfd4-184"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="fcfd4-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fcfd4-185">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfd4-186"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fcfd4-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fcfd4-187">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfd4-188"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="fcfd4-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fcfd4-189">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfd4-190"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="fcfd4-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fcfd4-191">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcfd4-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fcfd4-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fcfd4-193">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fcfd4-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcfd4-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="fcfd4-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="fcfd4-195">Se implementa como <strong>JetOpenTableW</strong> (Unicode) y <strong>JetOpenTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="fcfd4-195">Implemented as <strong>JetOpenTableW</strong> (Unicode) and <strong>JetOpenTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fcfd4-196">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fcfd4-196">See Also</span></span>

[<span data-ttu-id="fcfd4-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fcfd4-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fcfd4-198">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fcfd4-198">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fcfd4-199">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fcfd4-199">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fcfd4-200">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fcfd4-200">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fcfd4-201">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="fcfd4-201">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="fcfd4-202">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="fcfd4-202">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="fcfd4-203">JetRollback</span><span class="sxs-lookup"><span data-stu-id="fcfd4-203">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="fcfd4-204">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="fcfd4-204">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="fcfd4-205">Parámetros de recursos</span><span class="sxs-lookup"><span data-stu-id="fcfd4-205">Resource Parameters</span></span>](./resource-parameters.md)
