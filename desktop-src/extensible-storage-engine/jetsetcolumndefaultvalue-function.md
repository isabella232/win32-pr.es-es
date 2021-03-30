---
description: 'Más información acerca de: JetSetColumnDefaultValue (función)'
title: JetSetColumnDefaultValue función)
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f50d30b2edeca716895d8dd2339d659f0e1382f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907764"
---
# <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="721ee-103">JetSetColumnDefaultValue función)</span><span class="sxs-lookup"><span data-stu-id="721ee-103">JetSetColumnDefaultValue Function</span></span>


<span data-ttu-id="721ee-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="721ee-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="721ee-105">JetSetColumnDefaultValue función)</span><span class="sxs-lookup"><span data-stu-id="721ee-105">JetSetColumnDefaultValue Function</span></span>

<span data-ttu-id="721ee-106">La función **JetSetColumnDefaultValue** se puede usar para cambiar el valor predeterminado de una columna existente.</span><span class="sxs-lookup"><span data-stu-id="721ee-106">The **JetSetColumnDefaultValue** function can be used to change the default value of an existing column.</span></span>

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="721ee-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="721ee-107">Parameters</span></span>

<span data-ttu-id="721ee-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="721ee-108">*sesid*</span></span>

<span data-ttu-id="721ee-109">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="721ee-109">The session to use for this call.</span></span>

<span data-ttu-id="721ee-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="721ee-110">*dbid*</span></span>

<span data-ttu-id="721ee-111">Base de datos que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="721ee-111">The database to use for this call.</span></span>

<span data-ttu-id="721ee-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="721ee-112">*szTableName*</span></span>

<span data-ttu-id="721ee-113">Nombre de la tabla que contiene la columna que se verá afectada.</span><span class="sxs-lookup"><span data-stu-id="721ee-113">The name of the table containing the column that will be affected.</span></span>

<span data-ttu-id="721ee-114">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="721ee-114">*szColumnName*</span></span>

<span data-ttu-id="721ee-115">Nombre de la columna cuyo valor predeterminado se cambiará.</span><span class="sxs-lookup"><span data-stu-id="721ee-115">The name of the column whose default value will be changed.</span></span>

<span data-ttu-id="721ee-116">*pvData*</span><span class="sxs-lookup"><span data-stu-id="721ee-116">*pvData*</span></span>

<span data-ttu-id="721ee-117">Búfer de entrada que contiene el nuevo valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="721ee-117">The input buffer containing the new default value.</span></span>

<span data-ttu-id="721ee-118">*cbData*</span><span class="sxs-lookup"><span data-stu-id="721ee-118">*cbData*</span></span>

<span data-ttu-id="721ee-119">Tamaño del búfer de entrada que contiene el nuevo valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="721ee-119">The size of the input buffer containing the new default value.</span></span>

<span data-ttu-id="721ee-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="721ee-120">*grbit*</span></span>

<span data-ttu-id="721ee-121">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="721ee-121">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="721ee-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="721ee-122">Return Value</span></span>

<span data-ttu-id="721ee-123">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="721ee-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="721ee-124">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="721ee-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="721ee-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="721ee-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="721ee-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="721ee-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="721ee-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="721ee-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="721ee-128">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="721ee-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ee-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="721ee-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="721ee-130">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="721ee-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="721ee-131">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="721ee-131">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="721ee-132">Igual que JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="721ee-132">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ee-133">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="721ee-133">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="721ee-134">La columna especificada está siendo utilizada por un índice.</span><span class="sxs-lookup"><span data-stu-id="721ee-134">This specified column is currently in use by an index.</span></span></p>
<p><span data-ttu-id="721ee-135"><strong>JetSetColumnDefaultValue</strong> no puede cambiar el valor predeterminado de una columna a la que se hace referencia en la definición de un índice.</span><span class="sxs-lookup"><span data-stu-id="721ee-135"><strong>JetSetColumnDefaultValue</strong> cannot change the default value of a column that is referenced in the definition of an index.</span></span> <span data-ttu-id="721ee-136">Esto se debe a que, si lo hace, podría cambiar el contenido del índice.</span><span class="sxs-lookup"><span data-stu-id="721ee-136">This is because doing so could change the contents of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="721ee-137">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="721ee-137">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="721ee-138">Esta columna especificada no existe para esta tabla.</span><span class="sxs-lookup"><span data-stu-id="721ee-138">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ee-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="721ee-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="721ee-140">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="721ee-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="721ee-141">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="721ee-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="721ee-142">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="721ee-142">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="721ee-143">El identificador de base de datos especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="721ee-143">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ee-144">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="721ee-144">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="721ee-145">Uno de los nombres de objeto especificados no era válido.</span><span class="sxs-lookup"><span data-stu-id="721ee-145">One of the specified object names was invalid.</span></span> <span data-ttu-id="721ee-146">Todos los nombres de objeto deben cumplir el mismo conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="721ee-146">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="721ee-147">Estas reglas son:</span><span class="sxs-lookup"><span data-stu-id="721ee-147">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="721ee-148">Los nombres de objeto deben estar compuestos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="721ee-148">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="721ee-149">Los nombres de objeto deben tener al menos un carácter de longitud.</span><span class="sxs-lookup"><span data-stu-id="721ee-149">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="721ee-150">Los nombres de objeto no pueden superar JET_cbNameMost (64) caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="721ee-150">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="721ee-151">Los nombres de objeto no pueden comenzar con un espacio.</span><span class="sxs-lookup"><span data-stu-id="721ee-151">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="721ee-152">Los nombres de objeto no pueden contener caracteres de control ASCII (de 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="721ee-152">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="721ee-153">Los nombres de objeto no pueden contener un carácter de exclamación (!), punto (.), corchete de apertura ([) o corchete de cierre (]).</span><span class="sxs-lookup"><span data-stu-id="721ee-153">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="721ee-154">Una vez validada, solo se usará la parte de la cadena hasta el primer espacio (si existe) para el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="721ee-154">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="721ee-155">Esto significa que los nombres de objeto no pueden contener un espacio.</span><span class="sxs-lookup"><span data-stu-id="721ee-155">This means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="721ee-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="721ee-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="721ee-157">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="721ee-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ee-158">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="721ee-158">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="721ee-159">No se pudo establecer la columna en NULL.</span><span class="sxs-lookup"><span data-stu-id="721ee-159">The column could not be set to NULL.</span></span> <span data-ttu-id="721ee-160">Esto sucede para <strong>JetSetColumnDefaultValue</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="721ee-160">This happens for <strong>JetSetColumnDefaultValue</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="721ee-161"><em>cbData</em> es cero.</span><span class="sxs-lookup"><span data-stu-id="721ee-161"><em>cbData</em> is zero.</span></span></p></li>
<li><p><span data-ttu-id="721ee-162"><strong>pvData</strong> es NULL.</span><span class="sxs-lookup"><span data-stu-id="721ee-162"><strong>pvData</strong> is NULL.</span></span></p></li>
</ul>
<p><span data-ttu-id="721ee-163">Por lo tanto, no es posible establecer el valor predeterminado de una columna (atrás) en NULL o en un valor de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="721ee-163">Therefore, it is not possible to set the default value of a column (back) to NULL or to a zero length value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="721ee-164">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="721ee-164">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="721ee-165">Esta tabla especificada no existe para esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="721ee-165">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ee-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="721ee-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="721ee-167">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="721ee-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="721ee-168">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="721ee-168">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="721ee-169">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="721ee-169">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="721ee-170">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="721ee-170">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ee-171">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="721ee-171">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="721ee-172">Esta tabla especificada está en uso por otra sesión.</span><span class="sxs-lookup"><span data-stu-id="721ee-172">This specified table is in use by another session.</span></span></p>
<p><span data-ttu-id="721ee-173"><strong>JetSetColumnDefaultValue</strong> requiere acceso exclusivo a una tabla para cambiar el valor predeterminado de la columna en las versiones anteriores a Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="721ee-173"><strong>JetSetColumnDefaultValue</strong> requires exclusive access to a table in order to change the default value of the column for releases prior to Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="721ee-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="721ee-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="721ee-175">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="721ee-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ee-176">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="721ee-176">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="721ee-177">No es válido intentar una actualización cuando se encuentra dentro del ámbito de una transacción de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="721ee-177">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="721ee-178">Una transacción de solo lectura es una transacción que se ha iniciado mediante una llamada a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="721ee-178">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="721ee-179">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="721ee-179">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="721ee-180">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="721ee-180">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="721ee-181">Otra sesión ha bloqueado previamente el registro para su actualización.</span><span class="sxs-lookup"><span data-stu-id="721ee-181">Another session has previously locked the record for update.</span></span> <span data-ttu-id="721ee-182">Se producirá un error en la actualización intentada por esta sesión.</span><span class="sxs-lookup"><span data-stu-id="721ee-182">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="721ee-183">Si se ejecuta correctamente, el valor predeterminado de la columna especificada en la tabla dada en la base de datos determinada se cambia permanentemente al nuevo valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="721ee-183">On success, the default value of the specified column in the given table in the given database is permanently changed to the new default value.</span></span>

<span data-ttu-id="721ee-184">En caso de error, no se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="721ee-184">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="721ee-185">Observaciones</span><span class="sxs-lookup"><span data-stu-id="721ee-185">Remarks</span></span>

<span data-ttu-id="721ee-186">No es posible cambiar el valor predeterminado de una columna en una tabla de plantilla.</span><span class="sxs-lookup"><span data-stu-id="721ee-186">It is not possible to change the default value of a column in a template table.</span></span>

<span data-ttu-id="721ee-187">El motor de base de datos truncará silenciosamente el valor predeterminado de una columna en 255 bytes para las columnas de texto largo y binario largo.</span><span class="sxs-lookup"><span data-stu-id="721ee-187">The database engine will silently truncate the default value of a column to 255 bytes for long text and long binary columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="721ee-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="721ee-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="721ee-189"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="721ee-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="721ee-190">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="721ee-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ee-191"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="721ee-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="721ee-192">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="721ee-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="721ee-193"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="721ee-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="721ee-194">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="721ee-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ee-195"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="721ee-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="721ee-196">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="721ee-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="721ee-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="721ee-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="721ee-198">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="721ee-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ee-199"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="721ee-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="721ee-200">Se implementa como <strong>JetSetColumnDefaultValueW</strong> (Unicode) y <strong>JetSetColumnDefaultValueA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="721ee-200">Implemented as <strong>JetSetColumnDefaultValueW</strong> (Unicode) and <strong>JetSetColumnDefaultValueA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="721ee-201">Consulte también</span><span class="sxs-lookup"><span data-stu-id="721ee-201">See Also</span></span>

[<span data-ttu-id="721ee-202">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="721ee-202">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="721ee-203">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="721ee-203">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="721ee-204">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="721ee-204">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="721ee-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="721ee-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="721ee-206">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="721ee-206">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)  
[<span data-ttu-id="721ee-207">JetStopService</span><span class="sxs-lookup"><span data-stu-id="721ee-207">JetStopService</span></span>](./jetstopservice-function.md)
