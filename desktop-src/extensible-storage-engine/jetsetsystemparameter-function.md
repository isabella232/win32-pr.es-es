---
description: 'Más información acerca de: JetSetSystemParameter (función)'
title: JetSetSystemParameter función)
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbb57a1b50f3ad39525b894932f7111b56c3a076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275560"
---
# <a name="jetsetsystemparameter-function"></a><span data-ttu-id="a2b21-103">JetSetSystemParameter función)</span><span class="sxs-lookup"><span data-stu-id="a2b21-103">JetSetSystemParameter Function</span></span>


<span data-ttu-id="a2b21-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a2b21-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsystemparameter-function"></a><span data-ttu-id="a2b21-105">JetSetSystemParameter función)</span><span class="sxs-lookup"><span data-stu-id="a2b21-105">JetSetSystemParameter Function</span></span>

<span data-ttu-id="a2b21-106">La función **JetSetSystemParameter** se usa para establecer los numerosos valores de configuración del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="a2b21-106">The **JetSetSystemParameter** function is used to set the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a><span data-ttu-id="a2b21-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2b21-107">Parameters</span></span>

<span data-ttu-id="a2b21-108">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="a2b21-108">*pinstance*</span></span>

<span data-ttu-id="a2b21-109">Especifica la instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="a2b21-109">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="a2b21-110">**Windows 2000:**  En Windows 2000, este parámetro se omite y siempre debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a2b21-110">**Windows 2000:**  For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="a2b21-111">**Windows XP:**  En Windows XP y versiones posteriores, este parámetro está ligeramente sobrecargado.</span><span class="sxs-lookup"><span data-stu-id="a2b21-111">**Windows XP:**  For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="a2b21-112">Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, este parámetro puede ser **null** o contener la instancia real devuelta por [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="a2b21-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="a2b21-113">En cualquier caso, todos los parámetros del sistema se leen desde esa instancia.</span><span class="sxs-lookup"><span data-stu-id="a2b21-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="a2b21-114">Si el motor está funcionando en modo de varias instancias, este parámetro puede ser **null** o un puntero a una instancia creada mediante [JetInit](./jetinit-function.md) o [JetCreateIndex](./jetcreateindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="a2b21-114">If the engine is operating in multi-instance mode, then this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateIndex](./jetcreateindex-function.md).</span></span> <span data-ttu-id="a2b21-115">Cuando este parámetro es **null** , se lee la configuración global del parámetro del sistema (o el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="a2b21-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="a2b21-116">Cuando este parámetro es una instancia, se lee el valor del parámetro del sistema para esa instancia.</span><span class="sxs-lookup"><span data-stu-id="a2b21-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="a2b21-117">Aunque técnicamente es un parámetro de salida, esta API nunca modifica el contenido del búfer proporcionado.</span><span class="sxs-lookup"><span data-stu-id="a2b21-117">Even though this is technically an out parameter, this API never modifies the contents of the provided buffer.</span></span>

<span data-ttu-id="a2b21-118">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a2b21-118">*sesid*</span></span>

<span data-ttu-id="a2b21-119">Especifica la sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="a2b21-119">Specifies the session to use for this call.</span></span>

<span data-ttu-id="a2b21-120">Cuando se especifica, se omite la instancia especificada y se utilizará la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a2b21-120">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="a2b21-121">*paramid*</span><span class="sxs-lookup"><span data-stu-id="a2b21-121">*paramid*</span></span>

<span data-ttu-id="a2b21-122">IDENTIFICADOR del parámetro del sistema que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="a2b21-122">The ID of the system parameter that will be set.</span></span> <span data-ttu-id="a2b21-123">Vea [parámetros del sistema](./extensible-storage-engine-system-parameters.md) para obtener una lista completa de los parámetros del sistema y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="a2b21-123">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="a2b21-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2b21-124">*lParam*</span></span>

<span data-ttu-id="a2b21-125">Proporciona el valor que se va a establecer para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo entero.</span><span class="sxs-lookup"><span data-stu-id="a2b21-125">Provides the value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="a2b21-126">*szParam*</span><span class="sxs-lookup"><span data-stu-id="a2b21-126">*szParam*</span></span>

<span data-ttu-id="a2b21-127">Proporciona el valor para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo de cadena.</span><span class="sxs-lookup"><span data-stu-id="a2b21-127">Provides the value for the selected system parameter if that system parameter is of a string type.</span></span>

### <a name="return-value"></a><span data-ttu-id="a2b21-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2b21-128">Return Value</span></span>

<span data-ttu-id="a2b21-129">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="a2b21-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a2b21-130">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a2b21-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2b21-131">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a2b21-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="a2b21-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2b21-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2b21-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a2b21-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a2b21-134">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a2b21-134">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="a2b21-135"><strong>Windows Vista:</strong>  En Windows Vista y versiones posteriores, se puede devolver Success sin un cambio en el valor del parámetro System.</span><span class="sxs-lookup"><span data-stu-id="a2b21-135"><strong>Windows Vista:</strong>  On Windows Vista and later releases, success can be returned without a change to the system parameter's value.</span></span> <span data-ttu-id="a2b21-136">Para obtener más información, vea el JET_paramEnableAdvanced parámetro System en el tema <a href="gg269346(v=exchg.10).md">meta Parameters</a> .</span><span class="sxs-lookup"><span data-stu-id="a2b21-136">See the JET_paramEnableAdvanced system parameter in the <a href="gg269346(v=exchg.10).md">Meta Parameters</a> topic for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b21-137">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="a2b21-137">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="a2b21-138">La instancia se ha inicializado mediante una llamada a <a href="gg294068(v=exchg.10).md">JetInit</a> y esta operación no se puede realizar como resultado.</span><span class="sxs-lookup"><span data-stu-id="a2b21-138">The instance has been initialized using a call to <a href="gg294068(v=exchg.10).md">JetInit</a> and this operation cannot be performed as a result.</span></span> <span data-ttu-id="a2b21-139">Esto puede ocurrir para <strong>JetSetSystemParameter</strong> cuando se realiza un intento de configurar un parámetro del sistema después de que un cambio en su valor no pueda afectar al estado del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="a2b21-139">This can happen for <strong>JetSetSystemParameter</strong> when an attempt is made to configure a system parameter after a change in its value cannot affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b21-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a2b21-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a2b21-141">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a2b21-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b21-142">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="a2b21-142">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="a2b21-143">Los parámetros de índice de tupla especificados no son válidos.</span><span class="sxs-lookup"><span data-stu-id="a2b21-143">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="a2b21-144">Este error puede ser devuelto por <strong>JetSetSystemParameter</strong> solo cuando se establece <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>o <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> en un valor no válido.</span><span class="sxs-lookup"><span data-stu-id="a2b21-144">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="a2b21-145"><strong>Windows XP y Windows Server 2003:</strong>  Esto solo puede ocurrir en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a2b21-145"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b21-146">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="a2b21-146">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="a2b21-147">No es posible completar la operación porque se está inicializando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a2b21-147">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b21-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a2b21-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a2b21-149">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="a2b21-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a2b21-150"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a2b21-150"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b21-151">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a2b21-151">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a2b21-152">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="a2b21-152">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="a2b21-153">Esto puede ocurrir para <strong>JetSetSystemParameter</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="a2b21-153">This can happen for <strong>JetSetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2b21-154">El ID. de parámetro del sistema especificado no es válido o no es compatible.</span><span class="sxs-lookup"><span data-stu-id="a2b21-154">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="a2b21-155">Se intentó establecer un parámetro del sistema con valores de cadena con una cadena cuya longitud estaba fuera del intervalo permitido para el parámetro.</span><span class="sxs-lookup"><span data-stu-id="a2b21-155">An attempt was made to set a string-valued system parameter with a string whose length was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="a2b21-156">Se intentó establecer un parámetro del sistema con valores de cadena con una ruta de acceso de archivo donde la longitud de la representación de la ruta de acceso absoluta estaba fuera del intervalo permitido para ese parámetro.</span><span class="sxs-lookup"><span data-stu-id="a2b21-156">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p>
<p><span data-ttu-id="a2b21-157"><strong>Windows Vista:</strong>  Esto solo puede ocurrir en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a2b21-157"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="a2b21-158">Se intentó establecer un parámetro del sistema con valores enteros con un entero que estaba fuera del intervalo válido para el parámetro.</span><span class="sxs-lookup"><span data-stu-id="a2b21-158">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="a2b21-159">Se intentó establecer JET_paramUnicodeIndexDefault con un puntero JET_UNICODEINDEX <strong>null</strong> <a href="gg294097(v=exchg.10).md"></a> , un LCID no válido o un conjunto no admitido de marcas de LCMapString.</span><span class="sxs-lookup"><span data-stu-id="a2b21-159">An attempt was made to set JET_paramUnicodeIndexDefault with a <strong>NULL</strong> <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of LCMapString flags.</span></span></p>
<p><span data-ttu-id="a2b21-160"><strong>Windows Vista:</strong>  Esto solo puede ocurrir en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a2b21-160"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="a2b21-161">No se puede establecer el parámetro del sistema especificado porque es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a2b21-161">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="a2b21-162">Se ha intentado establecer un parámetro del sistema después de llamar a <a href="gg294068(v=exchg.10).md">JetInit</a> , el motor de base de datos está en modo de instancia única y no se ha especificado una sesión.</span><span class="sxs-lookup"><span data-stu-id="a2b21-162">An attempt was made to set a system parameter after <a href="gg294068(v=exchg.10).md">JetInit</a> was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p>
<p><span data-ttu-id="a2b21-163"><strong>Windows XP y Windows Server 2003:</strong>  Esto solo puede ocurrir en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a2b21-163"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="a2b21-164">El parámetro del sistema especificado solo es global y se ha intentado establecer un valor específico de la instancia para ese parámetro del sistema.</span><span class="sxs-lookup"><span data-stu-id="a2b21-164">The specified system parameter is global only and an attempt was made to set an instance specific value for that system parameter.</span></span></p>
<p><span data-ttu-id="a2b21-165"><strong>Windows XP y Windows Server 2003:</strong>  Esto solo puede ocurrir en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a2b21-165"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="a2b21-166">El parámetro del sistema especificado solo es por instancia y se intentó establecer el valor global para ese parámetro del sistema.</span><span class="sxs-lookup"><span data-stu-id="a2b21-166">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p>
<p><span data-ttu-id="a2b21-167"><strong>Windows XP y Windows Server 2003:</strong>  Esto solo puede ocurrir en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a2b21-167"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b21-168">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="a2b21-168">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="a2b21-169">La ruta de acceso del sistema de archivos especificada no era válida.</span><span class="sxs-lookup"><span data-stu-id="a2b21-169">The specified file system path was invalid.</span></span> <span data-ttu-id="a2b21-170">Este error puede ser devuelto por <strong>JetSetSystemParameter</strong> solo cuando se establecen parámetros del sistema que representan rutas de acceso del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="a2b21-170">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="a2b21-171">Por ejemplo, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> puede devolver este error.</span><span class="sxs-lookup"><span data-stu-id="a2b21-171">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> may return this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b21-172">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a2b21-172">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a2b21-173">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a2b21-173">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b21-174">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a2b21-174">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a2b21-175">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a2b21-175">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b21-176">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a2b21-176">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a2b21-177">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a2b21-177">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b21-178">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="a2b21-178">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="a2b21-179">El identificador de sesión no es válido o hace referencia a una sesión cerrada.</span><span class="sxs-lookup"><span data-stu-id="a2b21-179">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="a2b21-180">Este error no se devuelve en todas las circunstancias.</span><span class="sxs-lookup"><span data-stu-id="a2b21-180">This error is not returned under all circumstances.</span></span> <span data-ttu-id="a2b21-181">Los identificadores se validan solo en función del mejor esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="a2b21-181">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b21-182">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="a2b21-182">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="a2b21-183">El identificador de instancia no es válido o hace referencia a una instancia de que se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="a2b21-183">The instance handle is invalid or refers to an instance that has been shutdown.</span></span></p>
<p><span data-ttu-id="a2b21-184">Este error no se devuelve en todas las circunstancias.</span><span class="sxs-lookup"><span data-stu-id="a2b21-184">This error is not returned under all circumstances.</span></span> <span data-ttu-id="a2b21-185">Los identificadores se validan solo en función del mejor esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="a2b21-185">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="a2b21-186"><strong>Windows Vista:</strong>  Este error solo lo devolverán Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a2b21-186"><strong>Windows Vista:</strong>  This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a2b21-187">Si se ejecuta correctamente, la configuración del parámetro System se establecerá en el valor proporcionado.</span><span class="sxs-lookup"><span data-stu-id="a2b21-187">On success, the setting for the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="a2b21-188">En caso de error, la configuración del parámetro System no se modificará.</span><span class="sxs-lookup"><span data-stu-id="a2b21-188">On failure, the setting for the system parameter will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a2b21-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2b21-189">Remarks</span></span>

<span data-ttu-id="a2b21-190">**JetSetSystemParameter** realiza un trabajo pobre al validar el valor elegido para cada parámetro del sistema.</span><span class="sxs-lookup"><span data-stu-id="a2b21-190">**JetSetSystemParameter** does a poor job of validating the chosen setting for each system parameter.</span></span> <span data-ttu-id="a2b21-191">Se debe tener cuidado de no confiar en esta validación para aplicar una configuración correcta.</span><span class="sxs-lookup"><span data-stu-id="a2b21-191">Care must be taken to not rely on this validation to enforce good settings.</span></span> <span data-ttu-id="a2b21-192">Preste mucha atención a la descripción de cada parámetro del sistema y siga estas instrucciones para obtener una buena configuración de parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="a2b21-192">Please pay close attention to the description of each system parameter and follow those guidelines for a good system parameter setting.</span></span>

<span data-ttu-id="a2b21-193">Hay un conjunto de parámetros del sistema que siempre se debe establecer para garantizar que el motor de base de datos funciona según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="a2b21-193">There are a set of system parameters that should always be set to guarantee that the database engine works as intended.</span></span> <span data-ttu-id="a2b21-194">En concreto, siempre debe establecerse cualquier parámetro del sistema que afecte al diseño físico de los archivos utilizados por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="a2b21-194">Specifically, any system parameters that affect the physical layout of the files used by the database engine should always be set.</span></span> <span data-ttu-id="a2b21-195">Para obtener más información, vea [parámetros del sistema](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a2b21-195">For more information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="a2b21-196">Cada parámetro del sistema tiene un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a2b21-196">Every system parameter has a default value.</span></span> <span data-ttu-id="a2b21-197">Estos valores predeterminados han evolucionado a lo largo del tiempo y son bastante arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="a2b21-197">These default values have evolved over time and are quite arbitrary.</span></span> <span data-ttu-id="a2b21-198">Se recomienda encarecidamente que una aplicación evalúe todos los valores predeterminados para asegurarse de que son adecuados.</span><span class="sxs-lookup"><span data-stu-id="a2b21-198">It is highly recommended that an application evaluate all the default values to ensure that they are appropriate.</span></span> <span data-ttu-id="a2b21-199">Si no son adecuados, la aplicación debe configurarlos.</span><span class="sxs-lookup"><span data-stu-id="a2b21-199">If they are not appropriate, then they should be configured by the application.</span></span> <span data-ttu-id="a2b21-200">Esto es importante, ya que muchos de estos parámetros pueden afectar en gran medida a la confiabilidad, el rendimiento y el uso de recursos del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="a2b21-200">This is important as many of these parameters can greatly impact the reliability, performance, and resource utilization of the database engine.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a2b21-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2b21-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2b21-202"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a2b21-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b21-203">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a2b21-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b21-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a2b21-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b21-205">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a2b21-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b21-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a2b21-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b21-207">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="a2b21-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b21-208"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="a2b21-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b21-209">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a2b21-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b21-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a2b21-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b21-211">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a2b21-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b21-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a2b21-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b21-213">Se implementa como <strong>JetSetSystemParameterW</strong> (Unicode) y <strong>JetSetSystemParameterA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a2b21-213">Implemented as <strong>JetSetSystemParameterW</strong> (Unicode) and <strong>JetSetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a2b21-214">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a2b21-214">See Also</span></span>

[<span data-ttu-id="a2b21-215">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="a2b21-215">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="a2b21-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a2b21-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a2b21-217">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a2b21-217">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a2b21-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a2b21-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a2b21-219">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="a2b21-219">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="a2b21-220">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a2b21-220">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="a2b21-221">JetInit</span><span class="sxs-lookup"><span data-stu-id="a2b21-221">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="a2b21-222">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="a2b21-222">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
