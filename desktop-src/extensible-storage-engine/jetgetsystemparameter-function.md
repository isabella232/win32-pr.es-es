---
description: 'Más información acerca de: JetGetSystemParameter (función)'
title: JetGetSystemParameter función)
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80005be47037bade1f22e8125d4633c5dac45f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278658"
---
# <a name="jetgetsystemparameter-function"></a><span data-ttu-id="21763-103">JetGetSystemParameter función)</span><span class="sxs-lookup"><span data-stu-id="21763-103">JetGetSystemParameter Function</span></span>


<span data-ttu-id="21763-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="21763-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsystemparameter-function"></a><span data-ttu-id="21763-105">JetGetSystemParameter función)</span><span class="sxs-lookup"><span data-stu-id="21763-105">JetGetSystemParameter Function</span></span>

<span data-ttu-id="21763-106">La función **JetGetSystemParameter** Lee los numerosos valores de configuración del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="21763-106">The **JetGetSystemParameter** function reads the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="21763-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21763-107">Parameters</span></span>

<span data-ttu-id="21763-108">*repetición*</span><span class="sxs-lookup"><span data-stu-id="21763-108">*instance*</span></span>

<span data-ttu-id="21763-109">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="21763-109">The instance to use for this call.</span></span>

<span data-ttu-id="21763-110">En Windows 2000, este parámetro se omite y siempre debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="21763-110">For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="21763-111">En Windows XP y versiones posteriores, este parámetro está ligeramente sobrecargado.</span><span class="sxs-lookup"><span data-stu-id="21763-111">For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="21763-112">Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, este parámetro puede ser **null** o contener la instancia real devuelta por [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="21763-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="21763-113">En cualquier caso, todos los parámetros del sistema se leen desde esa instancia.</span><span class="sxs-lookup"><span data-stu-id="21763-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="21763-114">Si el motor está funcionando en modo de varias instancias, este parámetro puede ser **null** o un puntero a una instancia creada mediante [JetInit](./jetinit-function.md) o [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="21763-114">If the engine is operating in multi-instance mode, this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateInstance](./jetcreateinstance-function.md).</span></span> <span data-ttu-id="21763-115">Cuando este parámetro es **null** , se lee la configuración global del parámetro del sistema (o el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="21763-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="21763-116">Cuando este parámetro es una instancia, se lee el valor del parámetro del sistema para esa instancia.</span><span class="sxs-lookup"><span data-stu-id="21763-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="21763-117">*sesid*</span><span class="sxs-lookup"><span data-stu-id="21763-117">*sesid*</span></span>

<span data-ttu-id="21763-118">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="21763-118">The session to use for this call.</span></span>

<span data-ttu-id="21763-119">Cuando se especifica, se omite la instancia especificada y se utilizará la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="21763-119">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="21763-120">*paramid*</span><span class="sxs-lookup"><span data-stu-id="21763-120">*paramid*</span></span>

<span data-ttu-id="21763-121">IDENTIFICADOR del parámetro del sistema que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="21763-121">The ID of the system parameter that will be read.</span></span>

<span data-ttu-id="21763-122">Vea [parámetros del sistema](./extensible-storage-engine-system-parameters.md) para obtener una lista completa de los parámetros del sistema y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="21763-122">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="21763-123">*plParam*</span><span class="sxs-lookup"><span data-stu-id="21763-123">*plParam*</span></span>

<span data-ttu-id="21763-124">Búfer de salida que recibe el valor del parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo entero.</span><span class="sxs-lookup"><span data-stu-id="21763-124">The output buffer that receives the value of the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="21763-125">*szParam*</span><span class="sxs-lookup"><span data-stu-id="21763-125">*szParam*</span></span>

<span data-ttu-id="21763-126">Búfer de salida que recibe el valor del parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo de cadena.</span><span class="sxs-lookup"><span data-stu-id="21763-126">The output buffer that receives the value of the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="21763-127">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="21763-127">*cbMax*</span></span>

<span data-ttu-id="21763-128">Tamaño máximo en bytes del búfer de salida de la cadena.</span><span class="sxs-lookup"><span data-stu-id="21763-128">The maximum size in bytes of the string output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="21763-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21763-129">Return Value</span></span>

<span data-ttu-id="21763-130">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="21763-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="21763-131">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="21763-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21763-132">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="21763-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="21763-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="21763-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21763-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="21763-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="21763-135">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="21763-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21763-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="21763-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="21763-137">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="21763-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21763-138">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="21763-138">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="21763-139">No es posible completar la operación porque se está inicializando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="21763-139">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21763-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="21763-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="21763-141">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="21763-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="21763-142">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="21763-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21763-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="21763-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="21763-144">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="21763-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="21763-145">Esto puede ocurrir para <strong>JetGetSystemParameter</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="21763-145">This can happen for <strong>JetGetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="21763-146">El ID. de parámetro del sistema especificado no es válido o no es compatible.</span><span class="sxs-lookup"><span data-stu-id="21763-146">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="21763-147">El parámetro del sistema especificado requiere que se proporcione el búfer de salida entero y que el puntero del búfer de salida sea <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="21763-147">The specified system parameter requires the integer output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="21763-148">El parámetro del sistema especificado requiere que se proporcione un búfer de salida de cadena y que el puntero del búfer de salida sea <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="21763-148">The specified system parameter requires a string output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p>
<p><span data-ttu-id="21763-149"><strong>Windows Vista:  </strong> Esto solo puede ocurrir en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="21763-149"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="21763-150">El parámetro del sistema especificado requiere que se proporcione un búfer de salida de cadena y el tamaño del búfer de salida es demasiado pequeño para aceptar una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="21763-150">The specified system parameter requires a string output buffer to be provided and the size of that output buffer is too small to accept a null terminated string.</span></span></p>
<p><span data-ttu-id="21763-151"><strong>Windows Vista:  </strong> Esto solo puede ocurrir en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="21763-151"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="21763-152">No se puede leer el parámetro del sistema especificado porque es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="21763-152">The specified system parameter cannot be read because it is write-only.</span></span></p></li>
<li><p><span data-ttu-id="21763-153">El parámetro del sistema especificado solo es global y se intentó leer un valor específico de la instancia para ese parámetro del sistema.</span><span class="sxs-lookup"><span data-stu-id="21763-153">The specified system parameter is global only and an attempt was made to read an instance specific value for that system parameter.</span></span> <span data-ttu-id="21763-154">Esto solo puede ocurrir en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="21763-154">This can only happen on Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="21763-155">El parámetro del sistema especificado solo es por instancia y se intentó leer el valor global de ese parámetro del sistema.</span><span class="sxs-lookup"><span data-stu-id="21763-155">The specified system parameter is per-instance only and an attempt was made to read the global value for that system parameter.</span></span> <span data-ttu-id="21763-156">Esto solo puede ocurrir en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="21763-156">This can only happen on Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21763-157">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="21763-157">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="21763-158">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="21763-158">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21763-159">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="21763-159">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="21763-160">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="21763-160">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21763-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="21763-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="21763-162">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="21763-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21763-163">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="21763-163">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="21763-164">El identificador de sesión no es válido o hace referencia a una sesión cerrada.</span><span class="sxs-lookup"><span data-stu-id="21763-164">The session handle is invalid or refers to a closed session.</span></span> <span data-ttu-id="21763-165">Este error no se devuelve en todas las circunstancias.</span><span class="sxs-lookup"><span data-stu-id="21763-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="21763-166">Los identificadores se validan solo en función del mejor esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="21763-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21763-167">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="21763-167">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="21763-168">El identificador de instancia no es válido o hace referencia a una instancia de que se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="21763-168">The instance handle is invalid or refers to an instance that has been shutdown.</span></span> <span data-ttu-id="21763-169">Este error no se devuelve en todas las circunstancias.</span><span class="sxs-lookup"><span data-stu-id="21763-169">This error is not returned under all circumstances.</span></span> <span data-ttu-id="21763-170">Los identificadores se validan solo en función del mejor esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="21763-170">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="21763-171"><strong>Windows Vista:  </strong> Este error solo lo devolverán Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="21763-171"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21763-172">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="21763-172">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="21763-173">La operación se completó correctamente, pero el búfer de salida era demasiado pequeño para recibir el valor de parámetro del sistema completo.</span><span class="sxs-lookup"><span data-stu-id="21763-173">The operation completed successfully, but the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="21763-174">El búfer de salida se ha rellenado con tantos valores del parámetro del sistema como quepan.</span><span class="sxs-lookup"><span data-stu-id="21763-174">The output buffer has been filled with as much of the system parameter setting as would fit.</span></span> <span data-ttu-id="21763-175">Si el búfer de salida tiene al menos un carácter de longitud, la cadena en el búfer de salida se terminará en NULL.</span><span class="sxs-lookup"><span data-stu-id="21763-175">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="21763-176"><strong>Nota:  </strong> Este error no se devuelve en todas las versiones.</span><span class="sxs-lookup"><span data-stu-id="21763-176"><strong>Note  </strong>This error is not returned by all releases.</span></span> <span data-ttu-id="21763-177">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="21763-177">Please see the Remarks section for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21763-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="21763-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="21763-179">No se pudo realizar la operación porque el búfer de salida era demasiado pequeño para recibir toda la configuración del parámetro del sistema.</span><span class="sxs-lookup"><span data-stu-id="21763-179">The operation failed because the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="21763-180"><strong>Nota:  </strong> Este error no se devuelve en algunos casos para preservar la compatibilidad de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="21763-180"><strong>Note  </strong>This error is not returned in some cases to preserve application compatibility.</span></span> <span data-ttu-id="21763-181">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="21763-181">Please see the Remarks section for more information.</span></span></p>
<p><span data-ttu-id="21763-182"><strong>Windows Vista:  </strong> Este error solo lo devolverán Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="21763-182"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="21763-183">Si se ejecuta correctamente, el búfer de salida adecuado para el parámetro del sistema solicitado se establecerá en el valor de ese parámetro del sistema.</span><span class="sxs-lookup"><span data-stu-id="21763-183">On success, the output buffer appropriate for the requested system parameter will be set to the value of that system parameter.</span></span>

<span data-ttu-id="21763-184">En caso de error, el estado de los búferes de salida será undefined.</span><span class="sxs-lookup"><span data-stu-id="21763-184">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="21763-185">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21763-185">Remarks</span></span>

<span data-ttu-id="21763-186">Hay un problema importante en esta API que está presente en todas las versiones.</span><span class="sxs-lookup"><span data-stu-id="21763-186">There is an important problem in this API that is present in all releases.</span></span> <span data-ttu-id="21763-187">Si se solicita un parámetro del sistema con un valor de cadena y el búfer de salida es demasiado pequeño para recibir la configuración del parámetro del sistema completo, no se devolverá JET_wrnBufferTruncated.</span><span class="sxs-lookup"><span data-stu-id="21763-187">If a system parameter with a string value is requested and the output buffer is too small to receive the entire system parameter setting, JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="21763-188">En su lugar, se devuelve JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="21763-188">JET_errSuccess is returned instead.</span></span> <span data-ttu-id="21763-189">Si la longitud de la cadena devuelta es igual al tamaño del búfer de salida menos el terminador **nulo** , el llamador debe reaccionar como si se devolviera JET_wrnBufferTruncated.</span><span class="sxs-lookup"><span data-stu-id="21763-189">If the length of the returned string is equal to the size of the output buffer less the **NULL** terminator, the caller should react as if JET_wrnBufferTruncated were returned.</span></span> <span data-ttu-id="21763-190">Si se especifica un búfer de salida de cadena de tamaño cero, el llamador debe reaccionar como si se devolvieran JET_errInvalidParameter.</span><span class="sxs-lookup"><span data-stu-id="21763-190">If a zero-sized string output buffer is specified, the caller should react as if JET_errInvalidParameter were returned.</span></span>

#### <a name="requirements"></a><span data-ttu-id="21763-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21763-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21763-192"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="21763-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="21763-193">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="21763-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21763-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="21763-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="21763-195">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="21763-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21763-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="21763-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="21763-197">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="21763-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21763-198"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="21763-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="21763-199">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="21763-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21763-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="21763-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="21763-201">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="21763-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21763-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="21763-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="21763-203">Se implementa como <strong>JetGetSystemParameterW</strong> (Unicode) y <strong>JetGetSystemParameterA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="21763-203">Implemented as <strong>JetGetSystemParameterW</strong> (Unicode) and <strong>JetGetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="21763-204">Consulte también</span><span class="sxs-lookup"><span data-stu-id="21763-204">See Also</span></span>

[<span data-ttu-id="21763-205">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="21763-205">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="21763-206">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="21763-206">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="21763-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="21763-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="21763-208">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="21763-208">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="21763-209">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="21763-209">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="21763-210">JetInit</span><span class="sxs-lookup"><span data-stu-id="21763-210">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="21763-211">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="21763-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="21763-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="21763-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="21763-213">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="21763-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
