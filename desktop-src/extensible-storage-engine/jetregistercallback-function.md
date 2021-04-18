---
description: 'Más información acerca de: JetRegisterCallback (función)'
title: Función JetRegisterCallback
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ca7559488182f2d687d5c678639e108792f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715093"
---
# <a name="jetregistercallback-function"></a><span data-ttu-id="3f808-103">Función JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="3f808-103">JetRegisterCallback Function</span></span>


<span data-ttu-id="3f808-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3f808-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetregistercallback-function"></a><span data-ttu-id="3f808-105">Función JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="3f808-105">JetRegisterCallback Function</span></span>

<span data-ttu-id="3f808-106">La función **JetRegisterCallback** permite a la aplicación configurar el motor de base de datos para emitir notificaciones a la aplicación para eventos concretos.</span><span class="sxs-lookup"><span data-stu-id="3f808-106">The **JetRegisterCallback** function allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="3f808-107">Estas notificaciones están asociadas a una tabla específica y permanecen en vigor solo hasta que se cierre la instancia que contiene la tabla con [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="3f808-107">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="3f808-108">**Windows XP: JetRegisterCallback** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3f808-108">**Windows XP:  JetRegisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="3f808-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f808-109">Parameters</span></span>

<span data-ttu-id="3f808-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3f808-110">*sesid*</span></span>

<span data-ttu-id="3f808-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="3f808-111">The session to use for this call.</span></span>

<span data-ttu-id="3f808-112">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="3f808-112">*tableid*</span></span>

<span data-ttu-id="3f808-113">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="3f808-113">The cursor to use for this call.</span></span>

<span data-ttu-id="3f808-114">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="3f808-114">*cbtyp*</span></span>

<span data-ttu-id="3f808-115">Máscara de bits formada por las razones de devolución de llamada para las que la aplicación desea recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="3f808-115">A bit mask composed of the callback reasons for which the application wishes to receive notifications.</span></span>

<span data-ttu-id="3f808-116">Para crear esta máscara de bits, simplemente o juntos, los motivos de devolución de llamada válidos de la enumeración [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="3f808-116">To create this bit mask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="3f808-117">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="3f808-117">*pCallback*</span></span>

<span data-ttu-id="3f808-118">Puntero de función a la función de devolución de llamada para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f808-118">The function pointer to the callback function for the application.</span></span>

<span data-ttu-id="3f808-119">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="3f808-119">*pvContext*</span></span>

<span data-ttu-id="3f808-120">Especifica un puntero de contexto que se asignará a la función de devolución de llamada para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f808-120">Specifies a context pointer that will be given to the callback function for the application.</span></span>

<span data-ttu-id="3f808-121">*phCallbackId*</span><span class="sxs-lookup"><span data-stu-id="3f808-121">*phCallbackId*</span></span>

<span data-ttu-id="3f808-122">Devuelve un identificador que se puede usar más adelante para cancelar el registro de la función de devolución de llamada especificada mediante [JetUnregisterCallback](./jetunregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="3f808-122">Returns a handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback](./jetunregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="3f808-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f808-123">Return Value</span></span>

<span data-ttu-id="3f808-124">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="3f808-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3f808-125">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3f808-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f808-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3f808-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="3f808-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f808-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f808-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3f808-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3f808-129">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3f808-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f808-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="3f808-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="3f808-131">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="3f808-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f808-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="3f808-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="3f808-133">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="3f808-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="3f808-134">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3f808-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f808-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3f808-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3f808-136">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="3f808-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="3f808-137">Este error lo devolverá <strong>JetRegisterCallback</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="3f808-137">This error will be returned by <strong>JetRegisterCallback</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="3f808-138"><em>cbtyp</em> es cero,</span><span class="sxs-lookup"><span data-stu-id="3f808-138"><em>cbtyp</em> is zero,</span></span></p></li>
<li><p><span data-ttu-id="3f808-139"><em>pCallback</em> es NULL.</span><span class="sxs-lookup"><span data-stu-id="3f808-139"><em>pCallback</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="3f808-140"><em>phCallbackId</em> es NULL.</span><span class="sxs-lookup"><span data-stu-id="3f808-140"><em>phCallbackId</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f808-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3f808-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3f808-142">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="3f808-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f808-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3f808-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3f808-144">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="3f808-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f808-145">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="3f808-145">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="3f808-146">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="3f808-146">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="3f808-147">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3f808-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f808-148">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3f808-148">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3f808-149">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="3f808-149">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3f808-150">Si se ejecuta correctamente, la devolución de llamada especificada se registrará para los motivos de devolución de llamada especificados con la tabla asociada al cursor especificado.</span><span class="sxs-lookup"><span data-stu-id="3f808-150">On success, the specified callback will be registered for the given callback reasons with the table associated with the given cursor.</span></span> <span data-ttu-id="3f808-151">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3f808-151">No change to the database state will occur.</span></span>

<span data-ttu-id="3f808-152">En caso de error, la devolución de llamada no se registrará.</span><span class="sxs-lookup"><span data-stu-id="3f808-152">On failure, the callback will not be registered.</span></span> <span data-ttu-id="3f808-153">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3f808-153">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3f808-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f808-154">Remarks</span></span>

<span data-ttu-id="3f808-155">Este método proporciona un medio para que la aplicación asocie las devoluciones de llamada volátiles a una tabla en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="3f808-155">This method provides a means for the application to associate volatile callbacks with a table in a database.</span></span> <span data-ttu-id="3f808-156">Si la aplicación desea asociar devoluciones de llamada persistentes con una tabla en la base de datos, debe pasar la devolución de llamada a [JET_TABLECREATE](./jet-tablecreate-structure.md) mediante [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="3f808-156">If the application wishes to associate persisted callbacks with a table in the database then it should pass the callback to [JET_TABLECREATE](./jet-tablecreate-structure.md) using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="3f808-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f808-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f808-158"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3f808-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3f808-159">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3f808-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f808-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3f808-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3f808-161">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3f808-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f808-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3f808-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3f808-163">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="3f808-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f808-164"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="3f808-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3f808-165">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3f808-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f808-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3f808-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3f808-167">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3f808-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3f808-168">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3f808-168">See Also</span></span>

[<span data-ttu-id="3f808-169">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="3f808-169">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="3f808-170">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="3f808-170">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="3f808-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3f808-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3f808-172">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="3f808-172">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="3f808-173">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3f808-173">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3f808-174">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3f808-174">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3f808-175">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="3f808-175">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="3f808-176">JetTerm</span><span class="sxs-lookup"><span data-stu-id="3f808-176">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="3f808-177">JetUnregisterCallback</span><span class="sxs-lookup"><span data-stu-id="3f808-177">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)
