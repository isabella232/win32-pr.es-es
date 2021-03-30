---
description: 'Más información acerca de: JetEndSession (función)'
title: JetEndSession función)
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46bea6f5db745252a5e0ac6e8e03550dfead1b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360932"
---
# <a name="jetendsession-function"></a><span data-ttu-id="32f48-103">JetEndSession función)</span><span class="sxs-lookup"><span data-stu-id="32f48-103">JetEndSession Function</span></span>


<span data-ttu-id="32f48-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="32f48-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendsession-function"></a><span data-ttu-id="32f48-105">JetEndSession función)</span><span class="sxs-lookup"><span data-stu-id="32f48-105">JetEndSession Function</span></span>

<span data-ttu-id="32f48-106">La función **JetEndSession** finaliza la sesión y limpia y cancela la asignación de los recursos asociados a la sesión especificada.</span><span class="sxs-lookup"><span data-stu-id="32f48-106">The **JetEndSession** function ends the session, and cleans up and deallocates any resources associated with the specified session.</span></span>

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="32f48-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32f48-107">Parameters</span></span>

<span data-ttu-id="32f48-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="32f48-108">*sesid*</span></span>

<span data-ttu-id="32f48-109">La sesión que se va a finalizar.</span><span class="sxs-lookup"><span data-stu-id="32f48-109">The session to end.</span></span> <span data-ttu-id="32f48-110">Los recursos asociados se liberan cuando finaliza la sesión.</span><span class="sxs-lookup"><span data-stu-id="32f48-110">Associated resources are released when the session ends.</span></span>

<span data-ttu-id="32f48-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="32f48-111">*grbit*</span></span>

<span data-ttu-id="32f48-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="32f48-112">Reserved.</span></span> <span data-ttu-id="32f48-113">Este parámetro puede contener la marca JET_bitForceSessionClosed, pero esta marca está reservada y la configuración no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="32f48-113">This parameter can contain the JET_bitForceSessionClosed flag, but this flag is reserved and setting it has no effect.</span></span>

### <a name="return-value"></a><span data-ttu-id="32f48-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32f48-114">Return Value</span></span>

<span data-ttu-id="32f48-115">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="32f48-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="32f48-116">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="32f48-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32f48-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="32f48-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="32f48-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="32f48-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32f48-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="32f48-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="32f48-120">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="32f48-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32f48-121">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="32f48-121">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="32f48-122">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="32f48-122">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32f48-123">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="32f48-123">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="32f48-124">Uno de los parámetros que se proporcionó contenía un valor inesperado o la combinación de varios valores de parámetro produjo un resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="32f48-124">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32f48-125">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="32f48-125">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="32f48-126">La sesión no era una sesión válida de JET.</span><span class="sxs-lookup"><span data-stu-id="32f48-126">The session was not a valid JET session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32f48-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="32f48-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="32f48-128">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="32f48-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32f48-129">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="32f48-129">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="32f48-130">No se pudo realizar la operación porque no se pudo asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="32f48-130">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32f48-131">JET_errSessionInUse</span><span class="sxs-lookup"><span data-stu-id="32f48-131">JET_errSessionInUse</span></span></p></td>
<td><p><span data-ttu-id="32f48-132">Esto significa que la sesión estaba en uso en otro subproceso o que la sesión no se estableció o se restableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="32f48-132">This means the session was in use on another thread, or the session was not set or reset properly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32f48-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="32f48-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="32f48-134">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="32f48-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="32f48-135">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="32f48-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32f48-136">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="32f48-136">JET_errOutOfBuffers</span></span></p></td>
<td><p><span data-ttu-id="32f48-137">Error del sistema que indica que no hay más búferes.</span><span class="sxs-lookup"><span data-stu-id="32f48-137">System error that indicates that there are no more buffers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32f48-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="32f48-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="32f48-139">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="32f48-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32f48-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="32f48-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="32f48-141">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="32f48-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="32f48-142">Si se ejecuta correctamente, el identificador de sesión se cierra y no está disponible, y se limpian todos los recursos relacionados con esta sesión.</span><span class="sxs-lookup"><span data-stu-id="32f48-142">On success, the session handle is closed, and unavailable, and all resources related to this session are cleaned up.</span></span>

<span data-ttu-id="32f48-143">En caso de error, se pueden producir varios errores adicionales como parte del cierre de la tabla de ordenación, el cierre del cursor y la reversión de la transacción.</span><span class="sxs-lookup"><span data-stu-id="32f48-143">On failure, there are several additional errors that could occur as part of sort table close, cursor close, and transaction rollback.</span></span> <span data-ttu-id="32f48-144">Estos errores son bastante poco probables y muy poco probables si las sesiones no se utilizan completamente cuando se llama a **JetEndSession** .</span><span class="sxs-lookup"><span data-stu-id="32f48-144">These errors are fairly unlikely, and extremely unlikely if your sessions are completely not in use when **JetEndSession** is called.</span></span> <span data-ttu-id="32f48-145">Estos errores se devolverán si alguna parte de la sesión no se pudo limpiar correctamente.</span><span class="sxs-lookup"><span data-stu-id="32f48-145">These errors will be returned if some part of the session was unable to be cleaned up properly.</span></span>

#### <a name="remarks"></a><span data-ttu-id="32f48-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32f48-146">Remarks</span></span>

<span data-ttu-id="32f48-147">Esta API revierte todas las transacciones abiertas (no confirmadas en el nivel 0).</span><span class="sxs-lookup"><span data-stu-id="32f48-147">This API will rollback any open transactions (not committed to level 0).</span></span> <span data-ttu-id="32f48-148">También se limpiarán todos los cursores asociados a esta sesión y las tablas de ordenación que se hayan creado o abierto.</span><span class="sxs-lookup"><span data-stu-id="32f48-148">Also all cursors associated with this session, and any sort tables that have been created or opened will be cleaned up.</span></span>

#### <a name="requirements"></a><span data-ttu-id="32f48-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32f48-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32f48-150"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="32f48-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="32f48-151">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="32f48-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32f48-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="32f48-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="32f48-153">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="32f48-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32f48-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="32f48-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="32f48-155">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="32f48-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32f48-156"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="32f48-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="32f48-157">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="32f48-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32f48-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="32f48-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="32f48-159">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="32f48-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="32f48-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="32f48-160">See Also</span></span>

[<span data-ttu-id="32f48-161">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="32f48-161">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="32f48-162">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="32f48-162">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="32f48-163">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="32f48-163">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="32f48-164">JetRollback</span><span class="sxs-lookup"><span data-stu-id="32f48-164">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="32f48-165">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="32f48-165">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="32f48-166">JetStopService</span><span class="sxs-lookup"><span data-stu-id="32f48-166">JetStopService</span></span>](./jetstopservice-function.md)
