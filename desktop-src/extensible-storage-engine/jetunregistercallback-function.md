---
description: 'Más información acerca de: JetUnregisterCallback (función)'
title: JetUnregisterCallback función)
TOCTitle: JetUnregisterCallback Function
ms:assetid: de5c7afa-07e1-4687-989b-b56125a9712e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294116(v=EXCHG.10)
ms:contentKeyID: 32765730
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUnregisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b342bab655e3cf1e3c1a5967410edb1c971af87b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423739"
---
# <a name="jetunregistercallback-function"></a><span data-ttu-id="8f96b-103">JetUnregisterCallback función)</span><span class="sxs-lookup"><span data-stu-id="8f96b-103">JetUnregisterCallback Function</span></span>


<span data-ttu-id="8f96b-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8f96b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetunregistercallback-function"></a><span data-ttu-id="8f96b-105">JetUnregisterCallback función)</span><span class="sxs-lookup"><span data-stu-id="8f96b-105">JetUnregisterCallback Function</span></span>

<span data-ttu-id="8f96b-106">La función **JetUnregisterCallback** permite a la aplicación configurar el motor de base de datos para detener la emisión de notificaciones a la aplicación como se solicitó previamente a través de [JetRegisterCallback](./jetregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="8f96b-106">The **JetUnregisterCallback** function enables the application to configure the database engine to stop issuing notifications to the application as previously requested through [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

<span data-ttu-id="8f96b-107">**Windows XP:**  **JetUnregisterCallback** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f96b-107">**Windows XP:**  **JetUnregisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetUnregisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_HANDLE hCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="8f96b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f96b-108">Parameters</span></span>

<span data-ttu-id="8f96b-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8f96b-109">*sesid*</span></span>

<span data-ttu-id="8f96b-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="8f96b-110">The session to use for this call.</span></span>

<span data-ttu-id="8f96b-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="8f96b-111">*tableid*</span></span>

<span data-ttu-id="8f96b-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="8f96b-112">The cursor to use for this call.</span></span>

<span data-ttu-id="8f96b-113">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="8f96b-113">*cbtyp*</span></span>

<span data-ttu-id="8f96b-114">Máscara de máscara que se compone de los motivos por los que la aplicación ya no quiere recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="8f96b-114">A bitmask composed of the callback reasons that the application no longer wishes to receive notifications.</span></span>

<span data-ttu-id="8f96b-115">Para crear esta máscara de cadena, simplemente o juntos, los motivos válidos de devolución de llamada de la enumeración [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="8f96b-115">To create this bitmask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="8f96b-116">*hCallbackId*</span><span class="sxs-lookup"><span data-stu-id="8f96b-116">*hCallbackId*</span></span>

<span data-ttu-id="8f96b-117">Identificador de la devolución de llamada registrada devuelta por [JetRegisterCallback](./jetregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="8f96b-117">The handle of the registered callback that was returned by [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="8f96b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f96b-118">Return Value</span></span>

<span data-ttu-id="8f96b-119">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="8f96b-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8f96b-120">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8f96b-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f96b-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8f96b-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="8f96b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f96b-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f96b-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8f96b-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8f96b-124">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8f96b-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f96b-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8f96b-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8f96b-126">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="8f96b-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f96b-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8f96b-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8f96b-128">No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="8f96b-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="8f96b-129"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f96b-129"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f96b-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8f96b-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8f96b-131">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="8f96b-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f96b-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8f96b-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8f96b-133">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="8f96b-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f96b-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="8f96b-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="8f96b-135">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="8f96b-135">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="8f96b-136"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f96b-136"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f96b-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8f96b-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8f96b-138">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="8f96b-138">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8f96b-139">Si esta función se ejecuta correctamente, se anulará el registro de la devolución de llamada especificada para los motivos de devolución de llamada dados con la tabla asociada al cursor especificado.</span><span class="sxs-lookup"><span data-stu-id="8f96b-139">If this function succeeds, the specified callback will be unregistered for the given callback reasons with the table that is associated with the given cursor.</span></span> <span data-ttu-id="8f96b-140">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8f96b-140">No change to the database state will occur.</span></span>

<span data-ttu-id="8f96b-141">Si se produce un error en esta función, no se anulará el registro de la devolución de llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="8f96b-141">If this function fails, the specified callback will not be unregistered.</span></span> <span data-ttu-id="8f96b-142">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8f96b-142">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8f96b-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f96b-143">Remarks</span></span>

<span data-ttu-id="8f96b-144">La máscara de la función debe coincidir exactamente con la máscara de la que se especifica al registrar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8f96b-144">The given bitmask should exactly match the bitmask that is specified when registering the callback.</span></span> <span data-ttu-id="8f96b-145">El motor de base de datos no admite actualmente la eliminación de un subconjunto de estas notificaciones y no devuelve un error cuando se intenta.</span><span class="sxs-lookup"><span data-stu-id="8f96b-145">The database engine does not currently support removing a subset of these notifications and it does not return an error when this is attempted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8f96b-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f96b-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f96b-147"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8f96b-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8f96b-148">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f96b-148">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f96b-149"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8f96b-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8f96b-150">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8f96b-150">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f96b-151"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8f96b-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8f96b-152">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="8f96b-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f96b-153"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="8f96b-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8f96b-154">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8f96b-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f96b-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8f96b-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8f96b-156">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8f96b-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8f96b-157">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8f96b-157">See Also</span></span>

[<span data-ttu-id="8f96b-158">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="8f96b-158">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="8f96b-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8f96b-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8f96b-160">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="8f96b-160">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="8f96b-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8f96b-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8f96b-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8f96b-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8f96b-163">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="8f96b-163">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="8f96b-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="8f96b-164">JetStopService</span></span>](./jetstopservice-function.md)
