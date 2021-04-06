---
description: 'Más información acerca de: JetSetSessionParameter (función)'
title: JetSetSessionParameter función)
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001007"
---
# <a name="jetsetsessionparameter-function"></a><span data-ttu-id="71944-103">JetSetSessionParameter función)</span><span class="sxs-lookup"><span data-stu-id="71944-103">JetSetSessionParameter Function</span></span>


<span data-ttu-id="71944-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="71944-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="71944-105">La función **JetSetSessionParameter** configura el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="71944-105">The **JetSetSessionParameter** function configures the database engine.</span></span>

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a><span data-ttu-id="71944-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71944-106">Parameters</span></span>

<span data-ttu-id="71944-107">*sesid*</span><span class="sxs-lookup"><span data-stu-id="71944-107">*sesid*</span></span>

<span data-ttu-id="71944-108">Especifica la sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="71944-108">Specifies the session to use for this call.</span></span>

<span data-ttu-id="71944-109">Cuando se especifica, se omite la instancia especificada y se utilizará la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="71944-109">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="71944-110">*sesparamid*</span><span class="sxs-lookup"><span data-stu-id="71944-110">*sesparamid*</span></span>

<span data-ttu-id="71944-111">IDENTIFICADOR del parámetro de sesión que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="71944-111">The ID of the session parameter to set.</span></span>

<span data-ttu-id="71944-112">*pvParam*</span><span class="sxs-lookup"><span data-stu-id="71944-112">*pvParam*</span></span>

<span data-ttu-id="71944-113">Los datos que se van a establecer en este parámetro de sesión.</span><span class="sxs-lookup"><span data-stu-id="71944-113">The data to set in this session parameter.</span></span>

<span data-ttu-id="71944-114">*cbParam*</span><span class="sxs-lookup"><span data-stu-id="71944-114">*cbParam*</span></span>

<span data-ttu-id="71944-115">Tamaño de los datos proporcionados.</span><span class="sxs-lookup"><span data-stu-id="71944-115">The size of the data provided.</span></span>

### <a name="return-value"></a><span data-ttu-id="71944-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71944-116">Return value</span></span>

<span data-ttu-id="71944-117">Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="71944-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="71944-118">Para obtener más información sobre los posibles errores del motor de almacenamiento extensible (ESE), vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="71944-118">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71944-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="71944-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="71944-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="71944-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71944-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="71944-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="71944-122">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="71944-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71944-123">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="71944-123">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="71944-124">La instancia se ha inicializado mediante una llamada a la función <a href="gg294068(v=exchg.10).md">JetInit</a> y esta operación no se puede realizar como resultado.</span><span class="sxs-lookup"><span data-stu-id="71944-124">The instance has been initialized by using a call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function and this operation cannot be performed as a result.</span></span> <span data-ttu-id="71944-125">Esto puede ocurrir cuando se intenta configurar un parámetro del sistema después de que un cambio en el valor del parámetro ya no afecte al estado del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="71944-125">This can happen when an attempt is made to configure a system parameter after a change in the parameter value can no longer affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71944-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="71944-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="71944-127">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a la función <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="71944-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71944-128">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="71944-128">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="71944-129">Los parámetros de índice de tupla especificados no son válidos.</span><span class="sxs-lookup"><span data-stu-id="71944-129">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="71944-130">Este error solo se devuelve cuando el parámetro <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>o <em>JET_paramIndexTuplesToIndexMax</em> está establecido en un valor no válido.</span><span class="sxs-lookup"><span data-stu-id="71944-130">This error is returned only when the <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>, or <em>JET_paramIndexTuplesToIndexMax</em> parameter is set to an illegal value.</span></span> <span data-ttu-id="71944-131">Para obtener información sobre estos parámetros, vea <a href="gg294119(v=exchg.10).md">parámetros de índice</a>.</span><span class="sxs-lookup"><span data-stu-id="71944-131">For information about these parameters, see <a href="gg294119(v=exchg.10).md">Index Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71944-132">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="71944-132">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="71944-133">No es posible completar la operación porque se está inicializando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="71944-133">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71944-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="71944-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="71944-135">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="71944-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71944-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="71944-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="71944-137">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="71944-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="71944-138">Esto puede ocurrir cuando se produce lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="71944-138">This can happen when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="71944-139">El ID. de parámetro del sistema especificado no es válido o no es compatible.</span><span class="sxs-lookup"><span data-stu-id="71944-139">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="71944-140">Se intentó establecer un parámetro del sistema con valores de cadena con una cadena cuya longitud estaba fuera del intervalo permitido para el parámetro.</span><span class="sxs-lookup"><span data-stu-id="71944-140">An attempt was made to set a string-valued system parameter with a string the length of which was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="71944-141">Se intentó establecer un parámetro del sistema con valores de cadena con una ruta de acceso de archivo donde la longitud de la representación de la ruta de acceso absoluta estaba fuera del intervalo permitido para ese parámetro.</span><span class="sxs-lookup"><span data-stu-id="71944-141">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p></li>
<li><p><span data-ttu-id="71944-142">Se intentó establecer un parámetro del sistema con valores enteros con un entero que estaba fuera del intervalo válido para el parámetro.</span><span class="sxs-lookup"><span data-stu-id="71944-142">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="71944-143">Se intentó establecer JET_paramUnicodeIndexDefault con un puntero <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> null, un LCID no válido o un conjunto no admitido de marcas de <strong>LCMapString</strong> .</span><span class="sxs-lookup"><span data-stu-id="71944-143">An attempt was made to set JET_paramUnicodeIndexDefault with a null <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of <strong>LCMapString</strong> flags.</span></span></p></li>
<li><p><span data-ttu-id="71944-144">No se puede establecer el parámetro del sistema especificado porque es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71944-144">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="71944-145">Se ha intentado establecer un parámetro del sistema después de llamar a la función <a href="gg294068(v=exchg.10).md">JetInit</a> , el motor de base de datos está en modo de instancia única y no se ha especificado una sesión.</span><span class="sxs-lookup"><span data-stu-id="71944-145">An attempt was made to set a system parameter after the <a href="gg294068(v=exchg.10).md">JetInit</a> function was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p></li>
<li><p><span data-ttu-id="71944-146">El parámetro del sistema especificado solo es global y se ha intentado establecer un valor específico de la instancia para ese parámetro del sistema.</span><span class="sxs-lookup"><span data-stu-id="71944-146">The specified system parameter is global only and an attempt was made to set an instance-specific value for that system parameter.</span></span></p></li>
<li><p><span data-ttu-id="71944-147">El parámetro del sistema especificado solo es por instancia y se intentó establecer el valor global para ese parámetro del sistema.</span><span class="sxs-lookup"><span data-stu-id="71944-147">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71944-148">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="71944-148">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="71944-149">La ruta de acceso del sistema de archivos especificada no era válida.</span><span class="sxs-lookup"><span data-stu-id="71944-149">The specified file system path was invalid.</span></span> <span data-ttu-id="71944-150">Este error puede ser devuelto por <strong>JetSetSessionParameter</strong> solo cuando se establecen parámetros del sistema que representan rutas de acceso del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="71944-150">This error may be returned by <strong>JetSetSessionParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="71944-151">Por ejemplo, el parámetro <em>JET_paramSystemPath</em> puede devolver este error.</span><span class="sxs-lookup"><span data-stu-id="71944-151">For example, the <em>JET_paramSystemPath</em> parameter may return this error.</span></span> <span data-ttu-id="71944-152">Para obtener información acerca de este parámetro, consulte <a href="gg269235(v=exchg.10).md">parámetros del registro de transacciones</a>.</span><span class="sxs-lookup"><span data-stu-id="71944-152">For information about this parameter, see <a href="gg269235(v=exchg.10).md">Transaction Log Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71944-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="71944-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="71944-154">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="71944-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71944-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="71944-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="71944-156">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="71944-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71944-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="71944-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="71944-158">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="71944-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71944-159">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="71944-159">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="71944-160">El identificador de sesión no es válido o hace referencia a una sesión cerrada.</span><span class="sxs-lookup"><span data-stu-id="71944-160">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="71944-161">Este error no se devuelve en todas las circunstancias.</span><span class="sxs-lookup"><span data-stu-id="71944-161">This error is not returned under all circumstances.</span></span> <span data-ttu-id="71944-162">Los identificadores se validan solo en función del mejor esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="71944-162">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71944-163">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="71944-163">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="71944-164">El identificador de instancia no es válido o hace referencia a una instancia de que se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="71944-164">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p>
<p><span data-ttu-id="71944-165">Este error no se devuelve en todas las circunstancias.</span><span class="sxs-lookup"><span data-stu-id="71944-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="71944-166">Los identificadores se validan solo en función del mejor esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="71944-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71944-167">Si se ejecuta correctamente, el parámetro del sistema se establecerá en el valor proporcionado.</span><span class="sxs-lookup"><span data-stu-id="71944-167">On success, the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="71944-168">En caso de error, el valor del parámetro del sistema permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="71944-168">On failure, the system parameter value will remain unchanged.</span></span>

#### <a name="requirements"></a><span data-ttu-id="71944-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71944-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71944-170"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="71944-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="71944-171">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="71944-171">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71944-172"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="71944-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="71944-173">Requiere Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="71944-173">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71944-174"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="71944-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="71944-175">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="71944-175">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71944-176"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="71944-176"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="71944-177">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="71944-177">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71944-178"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="71944-178"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="71944-179">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="71944-179">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="71944-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="71944-180">See also</span></span>

[<span data-ttu-id="71944-181">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="71944-181">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="71944-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="71944-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="71944-183">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="71944-183">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="71944-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="71944-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="71944-185">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="71944-185">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="71944-186">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="71944-186">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="71944-187">JetInit</span><span class="sxs-lookup"><span data-stu-id="71944-187">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="71944-188">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="71944-188">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
