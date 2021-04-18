---
description: 'Más información acerca de: JetSetSessionContext (función)'
title: JetSetSessionContext función)
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4aafafa17499b76282599586f7477ac1ef6f878d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715296"
---
# <a name="jetsetsessioncontext-function"></a><span data-ttu-id="310ad-103">JetSetSessionContext función)</span><span class="sxs-lookup"><span data-stu-id="310ad-103">JetSetSessionContext Function</span></span>


<span data-ttu-id="310ad-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="310ad-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsessioncontext-function"></a><span data-ttu-id="310ad-105">JetSetSessionContext función)</span><span class="sxs-lookup"><span data-stu-id="310ad-105">JetSetSessionContext Function</span></span>

<span data-ttu-id="310ad-106">La función **JetSetSessionContext** asocia una sesión con el subproceso actual utilizando el identificador de contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="310ad-106">The **JetSetSessionContext** function associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="310ad-107">Esta asociación invalida el requisito de motor predeterminado que una transacción para una sesión determinada debe aparecer completamente en el mismo subproceso.</span><span class="sxs-lookup"><span data-stu-id="310ad-107">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span>

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a><span data-ttu-id="310ad-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="310ad-108">Parameters</span></span>

<span data-ttu-id="310ad-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="310ad-109">*sesid*</span></span>

<span data-ttu-id="310ad-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="310ad-110">The session to use for this call.</span></span>

<span data-ttu-id="310ad-111">*ulContext*</span><span class="sxs-lookup"><span data-stu-id="310ad-111">*ulContext*</span></span>

<span data-ttu-id="310ad-112">Identificador único al que se asociará esta sesión.</span><span class="sxs-lookup"><span data-stu-id="310ad-112">A unique identifier to which this session will be associated.</span></span>

### <a name="return-value"></a><span data-ttu-id="310ad-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="310ad-113">Return Value</span></span>

<span data-ttu-id="310ad-114">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="310ad-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="310ad-115">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="310ad-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="310ad-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="310ad-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="310ad-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="310ad-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="310ad-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="310ad-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="310ad-119">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="310ad-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="310ad-120">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="310ad-120">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="310ad-121">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="310ad-121">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="310ad-122">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="310ad-122">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="310ad-123">No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="310ad-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="310ad-124"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="310ad-124"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="310ad-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="310ad-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="310ad-126">Uno de los parámetros que se proporcionó contenía un valor inesperado o la combinación de varios valores de parámetro produjo un resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="310ad-126">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="310ad-127">Este error lo devolverá <strong>JetSetSessionContext</strong> en las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="310ad-127">This error will be returned by <strong>JetSetSessionContext</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="310ad-128"><em>ulContext</em> es null</span><span class="sxs-lookup"><span data-stu-id="310ad-128"><em>ulContext</em> is NULL</span></span></p></li>
<li><p><span data-ttu-id="310ad-129"><em>ulContext</em> es-1</span><span class="sxs-lookup"><span data-stu-id="310ad-129"><em>ulContext</em> is -1</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="310ad-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="310ad-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="310ad-131">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="310ad-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="310ad-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="310ad-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="310ad-133">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="310ad-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="310ad-134">JET_errSessionContextAlreadySet</span><span class="sxs-lookup"><span data-stu-id="310ad-134">JET_errSessionContextAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="310ad-135">No se pudo asociar la sesión con el subproceso actual porque ya se ha asociado a un subproceso.</span><span class="sxs-lookup"><span data-stu-id="310ad-135">The session could not be associated with the current thread because it has already been associated with a thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="310ad-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="310ad-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="310ad-137">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="310ad-137">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="310ad-138">Si esta función se ejecuta correctamente, la sesión se asociará al subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="310ad-138">If this function succeeds, the session will be associated with the current thread.</span></span> <span data-ttu-id="310ad-139">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="310ad-139">No change to the database state will occur.</span></span>

<span data-ttu-id="310ad-140">Si se produce un error en esta función, el estado de la sesión permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="310ad-140">If this function fails, the session state will remain unchanged.</span></span> <span data-ttu-id="310ad-141">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="310ad-141">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="310ad-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="310ad-142">Remarks</span></span>

<span data-ttu-id="310ad-143">Normalmente, una sesión está enlazada a un subproceso concreto para la duración de una transacción.</span><span class="sxs-lookup"><span data-stu-id="310ad-143">A session is usually bound to a specific thread for the duration of a transaction.</span></span> <span data-ttu-id="310ad-144">Este comportamiento está diseñado para ayudar a las aplicaciones a detectar y evitar el uso compartido conceptualmente inadvertido de una sola sesión entre varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="310ad-144">This behavior is designed to help applications detect and prevent the conceptually ill-advised sharing of a single session amongst multiple threads.</span></span> <span data-ttu-id="310ad-145">A veces, esta simple comprobación no funciona con la arquitectura de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="310ad-145">Sometimes, this simple check does not work with the application's architecture.</span></span> <span data-ttu-id="310ad-146">Por ejemplo, si la aplicación hospeda objetos del servidor mediante un grupo de subprocesos y las transacciones abarcan varias llamadas de servidor a un objeto determinado, esta protección puede hacer que algunas de esas llamadas produzcan un error con JET_errSessionSharingViolation aunque el patrón de uso sea correcto.</span><span class="sxs-lookup"><span data-stu-id="310ad-146">For example, if the application is hosting server-side objects using a thread pool and transactions span multiple server calls to a given object then this protection may cause some of those calls to fail with JET_errSessionSharingViolation even though the usage pattern is correct.</span></span> <span data-ttu-id="310ad-147">Esta situación es común para los servidores de objetos COM.</span><span class="sxs-lookup"><span data-stu-id="310ad-147">This situation is common for COM object servers.</span></span>

<span data-ttu-id="310ad-148">**JetSetSessionContext** y [JetResetSessionContext](./jetresetsessioncontext-function.md) solucionan este problema haciendo que la comprobación de uso compartido de la sesión sea un poco más flexible.</span><span class="sxs-lookup"><span data-stu-id="310ad-148">**JetSetSessionContext** and [JetResetSessionContext](./jetresetsessioncontext-function.md) solve this problem by making this session sharing check a little more flexible.</span></span> <span data-ttu-id="310ad-149">Cuando la aplicación empieza a realizar una serie de llamadas de la API de ESE mediante una sesión determinada, primero establece el contexto de la sesión en un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="310ad-149">When the application starts to make a series of ESE API calls using a particular session, it first sets the session context to a given value.</span></span> <span data-ttu-id="310ad-150">Esta acción asocia la sesión al subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="310ad-150">This action associates the session to the calling thread.</span></span> <span data-ttu-id="310ad-151">En el ejemplo dado, este contexto podría ser la dirección del objeto que contiene el identificador de sesión JET.</span><span class="sxs-lookup"><span data-stu-id="310ad-151">In the given example, this context could be the address of the object that contains the JET session handle.</span></span> <span data-ttu-id="310ad-152">Una vez realizadas las llamadas a la API de ESE, la aplicación restablece el contexto de la sesión.</span><span class="sxs-lookup"><span data-stu-id="310ad-152">Once the ESE API calls have been made, the application resets the session context.</span></span> <span data-ttu-id="310ad-153">Esta acción desasocia la sesión del subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="310ad-153">This action disassociates the session from the calling thread.</span></span> <span data-ttu-id="310ad-154">Otro subproceso puede utilizar el objeto y su sesión, incluso si la sesión tiene una transacción activa.</span><span class="sxs-lookup"><span data-stu-id="310ad-154">The object and its session can then be used by another thread even if the session has an active transaction.</span></span>

<span data-ttu-id="310ad-155">Es importante tener en cuenta que se debe llamar a **JetSetSessionContext** antes de abrir una transacción en esa sesión, o bien la asociación no funcionará.</span><span class="sxs-lookup"><span data-stu-id="310ad-155">It is important to note that **JetSetSessionContext** must be called prior to opening a transaction on that session or the association will not work.</span></span>

<span data-ttu-id="310ad-156">**JetSetSessionContext** es seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="310ad-156">**JetSetSessionContext** is thread safe.</span></span> <span data-ttu-id="310ad-157">Varios subprocesos pueden intentar establecer un contexto de subproceso en la misma sesión al mismo tiempo y solo se ganará uno.</span><span class="sxs-lookup"><span data-stu-id="310ad-157">Multiple threads can try to set a thread context on the same session at the same time and only one will win.</span></span> <span data-ttu-id="310ad-158">Este hecho puede ser utilizado por la aplicación como un medio para asignar una sesión de un grupo sin almacenar el estado externo sobre su asignación.</span><span class="sxs-lookup"><span data-stu-id="310ad-158">This fact can be used by the application as a means to allocate a session from a pool without storing external state about its allocation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="310ad-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="310ad-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="310ad-160"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="310ad-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="310ad-161">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="310ad-161">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="310ad-162"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="310ad-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="310ad-163">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="310ad-163">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="310ad-164"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="310ad-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="310ad-165">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="310ad-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="310ad-166"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="310ad-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="310ad-167">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="310ad-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="310ad-168"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="310ad-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="310ad-169">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="310ad-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="310ad-170">Consulte también</span><span class="sxs-lookup"><span data-stu-id="310ad-170">See Also</span></span>

[<span data-ttu-id="310ad-171">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="310ad-171">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="310ad-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="310ad-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="310ad-173">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="310ad-173">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="310ad-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="310ad-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="310ad-175">JetStopService</span><span class="sxs-lookup"><span data-stu-id="310ad-175">JetStopService</span></span>](./jetstopservice-function.md)
