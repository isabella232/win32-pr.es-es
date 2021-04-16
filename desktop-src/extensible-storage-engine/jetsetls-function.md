---
description: 'Más información acerca de: JetSetLS (función)'
title: Función JetSetLS
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540766"
---
# <a name="jetsetls-function"></a><span data-ttu-id="95714-103">Función JetSetLS</span><span class="sxs-lookup"><span data-stu-id="95714-103">JetSetLS Function</span></span>


<span data-ttu-id="95714-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="95714-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetls-function"></a><span data-ttu-id="95714-105">Función JetSetLS</span><span class="sxs-lookup"><span data-stu-id="95714-105">JetSetLS Function</span></span>

<span data-ttu-id="95714-106">La función **JetSetLS** permite a la aplicación asociar un identificador de contexto conocido como almacenamiento local con un cursor o la tabla asociada a ese cursor.</span><span class="sxs-lookup"><span data-stu-id="95714-106">The **JetSetLS** function enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="95714-107">La aplicación puede usar este identificador de contexto para almacenar datos auxiliares que están asociados a un cursor o una tabla.</span><span class="sxs-lookup"><span data-stu-id="95714-107">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="95714-108">Posteriormente, la aplicación recibe una notificación mediante una devolución de llamada en tiempo de ejecución cuando se debe liberar el identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="95714-108">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="95714-109">Esto hace posible asociar el estado asignado dinámicamente a un cursor o una tabla.</span><span class="sxs-lookup"><span data-stu-id="95714-109">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="95714-110">**Windows XP:**  **JetSetLS** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="95714-110">**Windows XP:**  **JetSetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="95714-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95714-111">Parameters</span></span>

<span data-ttu-id="95714-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="95714-112">*sesid*</span></span>

<span data-ttu-id="95714-113">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="95714-113">The session to use for this call.</span></span>

<span data-ttu-id="95714-114">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="95714-114">*tableid*</span></span>

<span data-ttu-id="95714-115">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="95714-115">The cursor to use for this call.</span></span>

<span data-ttu-id="95714-116">*ls*</span><span class="sxs-lookup"><span data-stu-id="95714-116">*ls*</span></span>

<span data-ttu-id="95714-117">Identificador de contexto que se va a asociar al cursor o a la tabla.</span><span class="sxs-lookup"><span data-stu-id="95714-117">The context handle to be associated with the cursor or table.</span></span>

<span data-ttu-id="95714-118">Cuando se especifica JET_bitLSReset, se omite el valor real de este parámetro y se usa JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="95714-118">When JET_bitLSReset is specified then the actual value of this parameter is ignored and JET_LSNil is used.</span></span>

<span data-ttu-id="95714-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="95714-119">*grbit*</span></span>

<span data-ttu-id="95714-120">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="95714-120">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95714-121">Value</span><span class="sxs-lookup"><span data-stu-id="95714-121">Value</span></span></p></th>
<th><p><span data-ttu-id="95714-122">Significado</span><span class="sxs-lookup"><span data-stu-id="95714-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95714-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="95714-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="95714-124">Esta opción indica que el identificador de contexto debe estar asociado al cursor especificado.</span><span class="sxs-lookup"><span data-stu-id="95714-124">This option indicates that the context handle should be associated with the given cursor.</span></span></p>
<p><span data-ttu-id="95714-125">Si no se especifica ni JET_bitLSCursor ni JET_bitLSTable, se supone JET_bitLSCursor.</span><span class="sxs-lookup"><span data-stu-id="95714-125">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="95714-126">No se puede usar esta opción con JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="95714-126">It is illegal to use this option with JET_bitLSTable.</span></span> <span data-ttu-id="95714-127">Se producirá un error en la operación con JET_errInvalidgrbit si se intenta.</span><span class="sxs-lookup"><span data-stu-id="95714-127">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95714-128">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="95714-128">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="95714-129">Esta opción indica que se debe omitir el identificador de contexto especificado y que el identificador de contexto para el objeto elegido se debe restablecer en JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="95714-129">This option indicates that the specified context handle should be ignored and that the context handle for the chosen object should be reset to JET_LSNil.</span></span></p>
<p><span data-ttu-id="95714-130">Es importante tener en cuenta que esta acción no producirá una devolución de llamada para limpiar el valor anterior del identificador de contexto para el objeto elegido.</span><span class="sxs-lookup"><span data-stu-id="95714-130">It is important to note that this action will not result in a callback to cleanup the previous value of the context handle for the chosen object.</span></span> <span data-ttu-id="95714-131">La limpieza correcta del identificador de contexto anterior se puede lograr mediante <a href="gg269234(v=exchg.10).md">JetGetLS</a> con JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="95714-131">Proper cleanup of the previous context handle can be achieved using <a href="gg269234(v=exchg.10).md">JetGetLS</a> with JET_bitLSReset.</span></span> <span data-ttu-id="95714-132">Vea <a href="gg269234(v=exchg.10).md">JetGetLS</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="95714-132">See <a href="gg269234(v=exchg.10).md">JetGetLS</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95714-133">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="95714-133">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="95714-134">Esta opción indica que el identificador de contexto se debe asociar a la tabla asociada al cursor especificado.</span><span class="sxs-lookup"><span data-stu-id="95714-134">This option indicates that the context handle should be associated with the table associated with the given cursor.</span></span></p>
<p><span data-ttu-id="95714-135">No se puede usar esta opción con JET_bitLSCursor.</span><span class="sxs-lookup"><span data-stu-id="95714-135">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="95714-136">Se producirá un error en la operación con JET_errInvalidgrbit si se intenta.</span><span class="sxs-lookup"><span data-stu-id="95714-136">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="95714-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95714-137">Return Value</span></span>

<span data-ttu-id="95714-138">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="95714-138">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="95714-139">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="95714-139">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95714-140">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="95714-140">Return code</span></span></p></th>
<th><p><span data-ttu-id="95714-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="95714-141">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95714-142">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="95714-142">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="95714-143">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="95714-143">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95714-144">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="95714-144">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="95714-145">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="95714-145">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95714-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="95714-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="95714-147">Una de las opciones solicitadas no era válida, se usó de forma incorrecta o no se implementó.</span><span class="sxs-lookup"><span data-stu-id="95714-147">One of the options requested was invalid, used incorrectly, or not implemented.</span></span> <span data-ttu-id="95714-148">Esto puede ocurrir para <strong>JetSetLS</strong> cuando se especifican JET_bitLSCursor y JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="95714-148">This can happen for <strong>JetSetLS</strong> when JET_bitLSCursor and JET_bitLSTable are both specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95714-149">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="95714-149">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="95714-150">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="95714-150">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="95714-151">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="95714-151">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95714-152">JET_errLSAlreadySet</span><span class="sxs-lookup"><span data-stu-id="95714-152">JET_errLSAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="95714-153">No se pudo asociar el identificador de contexto dado al objeto solicitado porque ya tenía un identificador de contexto asociado a él.</span><span class="sxs-lookup"><span data-stu-id="95714-153">The given context handle could not be associated with the requested object because it already had a context handle associated with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95714-154">JET_errLSCallbackNotSpecified</span><span class="sxs-lookup"><span data-stu-id="95714-154">JET_errLSCallbackNotSpecified</span></span></p></td>
<td><p><span data-ttu-id="95714-155">No se pudo asociar el identificador de contexto dado al objeto solicitado porque la devolución de llamada en tiempo de ejecución no se ha configurado para la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="95714-155">The given context handle could not be associated with the requested object because the runtime callback has not been configured for the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95714-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="95714-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="95714-157">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="95714-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95714-158">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="95714-158">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="95714-159">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="95714-159">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95714-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="95714-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="95714-161">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="95714-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="95714-162">En caso de éxito, el identificador de contexto especificado se asoció correctamente al objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="95714-162">On success, the given context handle was successfully associated with the requested object.</span></span> <span data-ttu-id="95714-163">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="95714-163">No change to the database state will occur.</span></span>

<span data-ttu-id="95714-164">En caso de error, no se ha producido ningún cambio en el estado del objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="95714-164">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="95714-165">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="95714-165">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="95714-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95714-166">Remarks</span></span>

<span data-ttu-id="95714-167">El almacenamiento local de un cursor o una tabla debe verse como una caché volátil.</span><span class="sxs-lookup"><span data-stu-id="95714-167">The Local Storage for a cursor or table should be viewed as a volatile cache.</span></span> <span data-ttu-id="95714-168">En primer lugar, la aplicación debe intentar recuperar el identificador de contexto mediante [JetGetLS](./jetgetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="95714-168">The application should first try to retrieve the context handle using [JetGetLS](./jetgetls-function.md).</span></span> <span data-ttu-id="95714-169">Si no se establece el valor (es decir, es JET_LSNil), la aplicación debe crear un nuevo contexto y cargarlo en la memoria caché mediante **JetSetLS**.</span><span class="sxs-lookup"><span data-stu-id="95714-169">If the value is not set (that is it is JET_LSNil) then the application should create a new context and load it into the cache using **JetSetLS**.</span></span> <span data-ttu-id="95714-170">La aplicación puede purgar la memoria caché mediante una llamada a [JetGetLS](./jetgetls-function.md) con JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="95714-170">The application can purge the cache using a call to [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="95714-171">Si el motor de base de datos purga la memoria caché, se generará una devolución de llamada en tiempo de ejecución para dar a la aplicación la oportunidad de limpiar ese contexto.</span><span class="sxs-lookup"><span data-stu-id="95714-171">If the database engine purges the cache then a runtime callback will be generated to give the application a chance to cleanup that context.</span></span> <span data-ttu-id="95714-172">El tipo de devolución de llamada se JET_cbtypFreeCursorLS para un identificador de contexto asociado a un cursor y JET_cbtypFreeTableLS para un identificador de contexto asociado a una tabla.</span><span class="sxs-lookup"><span data-stu-id="95714-172">The callback type will be JET_cbtypFreeCursorLS for a context handle associated with a cursor and JET_cbtypFreeTableLS for a context handle associated with a table.</span></span> <span data-ttu-id="95714-173">En cualquier caso, el identificador de contexto se pasará como pvArg1.</span><span class="sxs-lookup"><span data-stu-id="95714-173">In either case, the context handle will be passed as pvArg1.</span></span> <span data-ttu-id="95714-174">Consulte [JET_CALLBACK](./jet-callback-callback-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="95714-174">See [JET_CALLBACK](./jet-callback-callback-function.md) for more information.</span></span>

<span data-ttu-id="95714-175">La devolución de llamada en tiempo de ejecución debe estar configurada correctamente para la instancia asociada a la sesión determinada antes de poder usar el almacenamiento local.</span><span class="sxs-lookup"><span data-stu-id="95714-175">The runtime callback must be properly configured for the instance associated with the given session before Local Storage can be used.</span></span> <span data-ttu-id="95714-176">Esta devolución de llamada se puede establecer mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramRuntimeCallback](./callback-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="95714-176">This callback can be set using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramRuntimeCallback](./callback-parameters.md).</span></span> <span data-ttu-id="95714-177">Consulte [JetSetSystemParameter](./jetsetsystemparameter-function.md) y [JET_paramRuntimeCallback](./callback-parameters.md) en parámetros del sistema para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="95714-177">See [JetSetSystemParameter](./jetsetsystemparameter-function.md) and [JET_paramRuntimeCallback](./callback-parameters.md) in System Parameters for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="95714-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95714-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95714-179"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="95714-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="95714-180">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="95714-180">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95714-181"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="95714-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="95714-182">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="95714-182">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95714-183"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="95714-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="95714-184">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="95714-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95714-185"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="95714-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="95714-186">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="95714-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95714-187"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="95714-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="95714-188">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="95714-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="95714-189">Consulte también</span><span class="sxs-lookup"><span data-stu-id="95714-189">See Also</span></span>

[<span data-ttu-id="95714-190">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="95714-190">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="95714-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="95714-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="95714-192">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="95714-192">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="95714-193">JET_LS</span><span class="sxs-lookup"><span data-stu-id="95714-193">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="95714-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="95714-194">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="95714-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="95714-195">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="95714-196">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="95714-196">JetGetLS</span></span>](./jetgetls-function.md)  
[<span data-ttu-id="95714-197">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="95714-197">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="95714-198">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="95714-198">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
