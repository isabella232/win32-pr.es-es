---
description: 'Más información acerca de: JetResetTableSequential (función)'
title: JetResetTableSequential función)
TOCTitle: JetResetTableSequential Function
ms:assetid: 5fe9daf2-5ef1-46d6-b0c3-ef92fb57d8bb
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269261(v=EXCHG.10)
ms:contentKeyID: 32765563
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86de80ac935af81fd2b4e8fdfef8b20dbb8d27d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706443"
---
# <a name="jetresettablesequential-function"></a><span data-ttu-id="60ce6-103">JetResetTableSequential función)</span><span class="sxs-lookup"><span data-stu-id="60ce6-103">JetResetTableSequential Function</span></span>


<span data-ttu-id="60ce6-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="60ce6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresettablesequential-function"></a><span data-ttu-id="60ce6-105">JetResetTableSequential función)</span><span class="sxs-lookup"><span data-stu-id="60ce6-105">JetResetTableSequential Function</span></span>

<span data-ttu-id="60ce6-106">La función **JetResetTableSequential** notifica al motor de base de datos que la aplicación ya no examina todo el índice actual que contiene un cursor determinado.</span><span class="sxs-lookup"><span data-stu-id="60ce6-106">The **JetResetTableSequential** function notifies the database engine that the application is no longer scanning the entire current index containing a given cursor.</span></span> <span data-ttu-id="60ce6-107">Esta llamada invierte una notificación enviada por [JetSetTableSequential](./jetsettablesequential-function.md).</span><span class="sxs-lookup"><span data-stu-id="60ce6-107">This call reverses a notification sent by [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

<span data-ttu-id="60ce6-108">**Windows XP:**   **JetResetTableSequential** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="60ce6-108">**Windows XP:**   **JetResetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetResetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="60ce6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60ce6-109">Parameters</span></span>

<span data-ttu-id="60ce6-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="60ce6-110">*sesid*</span></span>

<span data-ttu-id="60ce6-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="60ce6-111">The session to use for this call.</span></span>

<span data-ttu-id="60ce6-112">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="60ce6-112">*tableid*</span></span>

<span data-ttu-id="60ce6-113">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="60ce6-113">The cursor to use for this call.</span></span>

<span data-ttu-id="60ce6-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="60ce6-114">*grbit*</span></span>

<span data-ttu-id="60ce6-115">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="60ce6-115">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="60ce6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60ce6-116">Return Value</span></span>

<span data-ttu-id="60ce6-117">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="60ce6-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="60ce6-118">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="60ce6-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60ce6-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="60ce6-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="60ce6-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="60ce6-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60ce6-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="60ce6-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="60ce6-122">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="60ce6-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ce6-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="60ce6-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="60ce6-124">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="60ce6-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ce6-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="60ce6-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="60ce6-126">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="60ce6-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="60ce6-127">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="60ce6-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ce6-128">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="60ce6-128">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="60ce6-129">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="60ce6-129">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ce6-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="60ce6-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="60ce6-131">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="60ce6-131">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ce6-132">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="60ce6-132">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="60ce6-133">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="60ce6-133">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="60ce6-134">Si se ejecuta correctamente, el índice actual del cursor ya no está optimizado para un examen secuencial de todo el índice.</span><span class="sxs-lookup"><span data-stu-id="60ce6-134">On success, the current index of the cursor is no longer optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="60ce6-135">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="60ce6-135">No change to the database state will occur.</span></span>

<span data-ttu-id="60ce6-136">En caso de error, no se producirá ningún cambio en la configuración del cursor.</span><span class="sxs-lookup"><span data-stu-id="60ce6-136">On failure, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="60ce6-137">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="60ce6-137">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="60ce6-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60ce6-138">Remarks</span></span>

<span data-ttu-id="60ce6-139">Es seguro realizar esta llamada en un cursor que no se haya configurado previamente mediante una llamada a [JetSetTableSequential](./jetsettablesequential-function.md).</span><span class="sxs-lookup"><span data-stu-id="60ce6-139">It is safe to make this call against a cursor that has not been previously configured by a call to [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="60ce6-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60ce6-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60ce6-141"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="60ce6-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="60ce6-142">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="60ce6-142">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ce6-143"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="60ce6-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="60ce6-144">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="60ce6-144">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ce6-145"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="60ce6-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="60ce6-146">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="60ce6-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ce6-147"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="60ce6-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="60ce6-148">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="60ce6-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ce6-149"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="60ce6-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="60ce6-150">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="60ce6-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="60ce6-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="60ce6-151">See Also</span></span>

[<span data-ttu-id="60ce6-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="60ce6-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="60ce6-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="60ce6-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="60ce6-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="60ce6-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="60ce6-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="60ce6-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="60ce6-156">JetSetTableSequential</span><span class="sxs-lookup"><span data-stu-id="60ce6-156">JetSetTableSequential</span></span>](./jetsettablesequential-function.md)  
[<span data-ttu-id="60ce6-157">JetStopService</span><span class="sxs-lookup"><span data-stu-id="60ce6-157">JetStopService</span></span>](./jetstopservice-function.md)
