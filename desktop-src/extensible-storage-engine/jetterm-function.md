---
description: 'Más información acerca de: JetTerm (función)'
title: Función JetTerm
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ce78ea12dfa61265a12b3858cc1e859adcae6e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696294"
---
# <a name="jetterm-function"></a><span data-ttu-id="84ac5-103">Función JetTerm</span><span class="sxs-lookup"><span data-stu-id="84ac5-103">JetTerm Function</span></span>


<span data-ttu-id="84ac5-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="84ac5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm-function"></a><span data-ttu-id="84ac5-105">Función JetTerm</span><span class="sxs-lookup"><span data-stu-id="84ac5-105">JetTerm Function</span></span>

<span data-ttu-id="84ac5-106">La función **JetTerm** inicia el cierre de una instancia de que [JetInit](./jetinit-function.md)ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="84ac5-106">The **JetTerm** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="84ac5-107">**JetTerm** también se puede usar para destruir una instancia no inicializada creada por [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="84ac5-107">**JetTerm** can also be used to destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="84ac5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84ac5-108">Parameters</span></span>

<span data-ttu-id="84ac5-109">*repetición*</span><span class="sxs-lookup"><span data-stu-id="84ac5-109">*instance*</span></span>

<span data-ttu-id="84ac5-110">Especifica la instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="84ac5-110">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="84ac5-111">**Windows 2000:**  Este parámetro se omite y siempre debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="84ac5-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="84ac5-112">**Windows XP y versiones posteriores:**  Este parámetro está sobrecargado.</span><span class="sxs-lookup"><span data-stu-id="84ac5-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="84ac5-113">Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, este parámetro puede ser **null** o contener la instancia real devuelta por [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="84ac5-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="84ac5-114">Si el motor está funcionando en modo de varias instancias, este parámetro debe ser un puntero a una instancia de creada mediante [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="84ac5-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="84ac5-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84ac5-115">Return Value</span></span>

<span data-ttu-id="84ac5-116">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="84ac5-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="84ac5-117">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="84ac5-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84ac5-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="84ac5-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="84ac5-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="84ac5-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84ac5-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="84ac5-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="84ac5-121">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="84ac5-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84ac5-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="84ac5-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="84ac5-123">Uno de los parámetros que se proporcionó contenía un valor inesperado o la combinación de varios parámetros produjo un resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="84ac5-123">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="84ac5-124"><strong>JetTerm</strong> devolverá este error cuando el motor está en modo de varias instancias y cuando <em>pinstance</em> hace referencia a una instancia no válida.</span><span class="sxs-lookup"><span data-stu-id="84ac5-124">This error will be returned by <strong>JetTerm</strong> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="84ac5-125"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="84ac5-125"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84ac5-126">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="84ac5-126">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="84ac5-127">No se puede completar la operación porque la instancia aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="84ac5-127">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84ac5-128">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="84ac5-128">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="84ac5-129">No se puede completar la operación porque la instancia se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="84ac5-129">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84ac5-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="84ac5-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="84ac5-131">No es posible completar la operación porque hay una operación de restauración en curso en la instancia.</span><span class="sxs-lookup"><span data-stu-id="84ac5-131">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84ac5-132">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="84ac5-132">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="84ac5-133">No se puede completar la operación porque hay una operación de copia de seguridad en curso en la instancia.</span><span class="sxs-lookup"><span data-stu-id="84ac5-133">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84ac5-134">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="84ac5-134">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="84ac5-135">No se puede cerrar la instancia porque actualmente hay sesiones con transacciones activas para la instancia especificada.</span><span class="sxs-lookup"><span data-stu-id="84ac5-135">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="84ac5-136">Este error solo se produce si se usa el JET_bitTermComplete.</span><span class="sxs-lookup"><span data-stu-id="84ac5-136">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84ac5-137">Si esta función se ejecuta correctamente, se cerrará la instancia especificada.</span><span class="sxs-lookup"><span data-stu-id="84ac5-137">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="84ac5-138">El identificador de instancia también se cerrará y no estará disponible para ninguna API que tome un identificador de instancia.</span><span class="sxs-lookup"><span data-stu-id="84ac5-138">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="84ac5-139">También se cerrarán todos los demás objetos asociados a la instancia de, como sesiones.</span><span class="sxs-lookup"><span data-stu-id="84ac5-139">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="84ac5-140">El estado del archivo de punto de comprobación, los archivos de registro de transacciones y los archivos de base de datos adjuntos a la instancia se modificarán durante el proceso de cierre.</span><span class="sxs-lookup"><span data-stu-id="84ac5-140">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="84ac5-141">Si se produce un error en esta función como resultado de un error de uso, la instancia permanece en un estado inicializado y no cambia nada.</span><span class="sxs-lookup"><span data-stu-id="84ac5-141">If this function fails as the result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="84ac5-142">De lo contrario, la instancia de se sigue cerrando según el caso de éxito.</span><span class="sxs-lookup"><span data-stu-id="84ac5-142">Otherwise, the instance is still shut down as per the success case.</span></span> <span data-ttu-id="84ac5-143">La diferencia es que la instancia de deberá pasar a través de la recuperación de bloqueos la próxima vez que se inicialice.</span><span class="sxs-lookup"><span data-stu-id="84ac5-143">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="84ac5-144">El motor intentará vaciar tantos datos como sea posible para minimizar la cantidad de recuperación necesaria.</span><span class="sxs-lookup"><span data-stu-id="84ac5-144">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="84ac5-145">Conceptualmente, un error de **JetTerm** no es diferente de un bloqueo del proceso.</span><span class="sxs-lookup"><span data-stu-id="84ac5-145">Conceptually, such a failure of **JetTerm** is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="84ac5-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84ac5-146">Remarks</span></span>

<span data-ttu-id="84ac5-147">Si el proceso de host de una instancia se cierra por cualquier motivo antes de que **JetTerm** se llame correctamente en esa instancia, se considera que la instancia está en un estado bloqueado.</span><span class="sxs-lookup"><span data-stu-id="84ac5-147">If the host process of an instance quits for any reason before **JetTerm** is successfully called on that instance then the instance is considered to be in a crashed state.</span></span> <span data-ttu-id="84ac5-148">La recuperación tras bloqueo se producirá en el siguiente intento de inicializar esa instancia.</span><span class="sxs-lookup"><span data-stu-id="84ac5-148">Crash recovery will occur on the next attempt to initialize that instance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="84ac5-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84ac5-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84ac5-150"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="84ac5-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="84ac5-151">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="84ac5-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84ac5-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="84ac5-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="84ac5-153">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="84ac5-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84ac5-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="84ac5-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="84ac5-155">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="84ac5-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84ac5-156"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="84ac5-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="84ac5-157">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="84ac5-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84ac5-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="84ac5-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="84ac5-159">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="84ac5-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="84ac5-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="84ac5-160">See Also</span></span>

[<span data-ttu-id="84ac5-161">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="84ac5-161">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="84ac5-162">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="84ac5-162">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="84ac5-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="84ac5-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="84ac5-164">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="84ac5-164">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="84ac5-165">JetInit</span><span class="sxs-lookup"><span data-stu-id="84ac5-165">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="84ac5-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="84ac5-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="84ac5-167">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="84ac5-167">JetTerm2</span></span>](./jetterm2-function.md)
