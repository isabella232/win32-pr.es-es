---
description: 'Más información acerca de: JetDupSession (función)'
title: JetDupSession función)
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aa320c329032f5867f5f762351277cc4567baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912170"
---
# <a name="jetdupsession-function"></a><span data-ttu-id="80441-103">JetDupSession función)</span><span class="sxs-lookup"><span data-stu-id="80441-103">JetDupSession Function</span></span>


<span data-ttu-id="80441-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="80441-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupsession-function"></a><span data-ttu-id="80441-105">JetDupSession función)</span><span class="sxs-lookup"><span data-stu-id="80441-105">JetDupSession Function</span></span>

<span data-ttu-id="80441-106">La función **JetDupSession** inicia una sesión e inicializa y devuelve un identificador de sesión de ESE ([JET_SESID](./jet-sesid.md)).</span><span class="sxs-lookup"><span data-stu-id="80441-106">The **JetDupSession** function starts a session, and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="80441-107">Las sesiones controlan todo el acceso a la base de datos y se usan para controlar el ámbito de las transacciones.</span><span class="sxs-lookup"><span data-stu-id="80441-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="80441-108">La sesión se puede usar para iniciar, confirmar o anular transacciones.</span><span class="sxs-lookup"><span data-stu-id="80441-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="80441-109">La sesión también se utiliza para adjuntar, crear o abrir una base de datos.</span><span class="sxs-lookup"><span data-stu-id="80441-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="80441-110">La sesión se utiliza como contexto para todas las operaciones DDL y DML.</span><span class="sxs-lookup"><span data-stu-id="80441-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="80441-111">Para aumentar la simultaneidad y el acceso en paralelo a la base de datos, se pueden iniciar varias sesiones.</span><span class="sxs-lookup"><span data-stu-id="80441-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

<span data-ttu-id="80441-112">**Nota:** Esta API actuará de todas formas como [JetBeginSession](./jetbeginsession-function.md) llamada en la instancia de la sesión pasada.</span><span class="sxs-lookup"><span data-stu-id="80441-112">**Note** This API will act in all ways as a [JetBeginSession](./jetbeginsession-function.md) called on the instance of the session passed in.</span></span> <span data-ttu-id="80441-113">No se recomienda esta función, se prefiere [JetBeginSession](./jetbeginsession-function.md) .</span><span class="sxs-lookup"><span data-stu-id="80441-113">This function is not recommended, [JetBeginSession](./jetbeginsession-function.md) is preferred.</span></span>

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a><span data-ttu-id="80441-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80441-114">Parameters</span></span>

<span data-ttu-id="80441-115">*sesid*</span><span class="sxs-lookup"><span data-stu-id="80441-115">*sesid*</span></span>

<span data-ttu-id="80441-116">La sesión que se va a usar como origen para duplicar o iniciar la sesión.</span><span class="sxs-lookup"><span data-stu-id="80441-116">The session to use as the source for duplicating or beginning the session.</span></span>

<span data-ttu-id="80441-117">*psesid*</span><span class="sxs-lookup"><span data-stu-id="80441-117">*psesid*</span></span>

<span data-ttu-id="80441-118">Un puntero a la variable que el identificador de la sesión inicializa si la devolución es correcta.</span><span class="sxs-lookup"><span data-stu-id="80441-118">A pointer to the variable that the session handle initializes on successful return.</span></span>

### <a name="return-value"></a><span data-ttu-id="80441-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80441-119">Return Value</span></span>

<span data-ttu-id="80441-120">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="80441-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="80441-121">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="80441-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80441-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="80441-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="80441-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="80441-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80441-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="80441-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="80441-125">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="80441-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80441-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="80441-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="80441-127">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="80441-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80441-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="80441-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="80441-129">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="80441-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="80441-130">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="80441-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80441-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="80441-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="80441-132">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="80441-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80441-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="80441-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="80441-134">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="80441-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80441-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="80441-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="80441-136">No se pudo realizar la operación porque no se pudo asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="80441-136">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80441-137">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="80441-137">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="80441-138">El número de sesiones que el motor permitirá que se inicie el cliente es limitado.</span><span class="sxs-lookup"><span data-stu-id="80441-138">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="80441-139">Este valor se puede cambiar mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con la constante <em>JET_paramMaxSessions</em> .</span><span class="sxs-lookup"><span data-stu-id="80441-139">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the <em>JET_paramMaxSessions</em> constant.</span></span> <span data-ttu-id="80441-140">El número predeterminado de sesiones es 16.</span><span class="sxs-lookup"><span data-stu-id="80441-140">The default number of sessions is 16.</span></span> <span data-ttu-id="80441-141">Consulte <a href="gg294139(v=exchg.10).md">parámetros del sistema</a> para obtener más información sobre <em>JET_paramMaxSessions</em>.</span><span class="sxs-lookup"><span data-stu-id="80441-141">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about <em>JET_paramMaxSessions</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80441-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="80441-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="80441-143">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="80441-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80441-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="80441-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="80441-145">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="80441-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80441-146">Si se ejecuta correctamente, el identificador de sesión se inicializa y se puede usar para las operaciones de base de datos.</span><span class="sxs-lookup"><span data-stu-id="80441-146">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="80441-147">En caso de error, no hay sesiones disponibles o no se pudo inicializar una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="80441-147">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="requirements"></a><span data-ttu-id="80441-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80441-148">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80441-149"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="80441-149"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="80441-150">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="80441-150">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80441-151"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="80441-151"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="80441-152">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="80441-152">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80441-153"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="80441-153"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="80441-154">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="80441-154">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80441-155"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="80441-155"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="80441-156">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="80441-156">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80441-157"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="80441-157"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="80441-158">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="80441-158">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="80441-159">Consulte también</span><span class="sxs-lookup"><span data-stu-id="80441-159">See Also</span></span>

[<span data-ttu-id="80441-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="80441-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="80441-161">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="80441-161">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="80441-162">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="80441-162">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="80441-163">JetStopService</span><span class="sxs-lookup"><span data-stu-id="80441-163">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="80441-164">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="80441-164">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
