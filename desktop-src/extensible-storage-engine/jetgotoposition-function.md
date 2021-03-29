---
description: 'Más información acerca de: JetGotoPosition (función)'
title: JetGotoPosition función)
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae5148431ad46c5a75bbd804f2c0d777b279561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808438"
---
# <a name="jetgotoposition-function"></a><span data-ttu-id="29826-103">JetGotoPosition función)</span><span class="sxs-lookup"><span data-stu-id="29826-103">JetGotoPosition Function</span></span>


<span data-ttu-id="29826-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="29826-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotoposition-function"></a><span data-ttu-id="29826-105">JetGotoPosition función)</span><span class="sxs-lookup"><span data-stu-id="29826-105">JetGotoPosition Function</span></span>

<span data-ttu-id="29826-106">La función **JetGotoPosition** mueve un cursor a una nueva ubicación que es una fracción del camino a través del índice actual.</span><span class="sxs-lookup"><span data-stu-id="29826-106">The **JetGotoPosition** function moves a cursor to a new location that is a fraction of the way through the current index.</span></span> <span data-ttu-id="29826-107">La fracción es aproximadamente igual a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="29826-107">The fraction is approximately equal to the following:</span></span>

<span data-ttu-id="29826-108">precpos- \> centriesLT/precpos- \> centriesTotal</span><span class="sxs-lookup"><span data-stu-id="29826-108">precpos-\>centriesLT/precpos-\>centriesTotal</span></span>

<span data-ttu-id="29826-109">Esta operación se realiza en respuesta a la entrada del cuadro de desplazamiento del usuario que se recibe cuando el usuario intenta mostrar los datos que se inician a la vez a través de un conjunto de datos.</span><span class="sxs-lookup"><span data-stu-id="29826-109">This operation is performed in response to user scroll box input that is received when the user attempts to show data that starts part way through a data set.</span></span>

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a><span data-ttu-id="29826-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29826-110">Parameters</span></span>

<span data-ttu-id="29826-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="29826-111">*sesid*</span></span>

<span data-ttu-id="29826-112">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="29826-112">The session to use for this call.</span></span>

<span data-ttu-id="29826-113">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="29826-113">*tableid*</span></span>

<span data-ttu-id="29826-114">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="29826-114">The cursor to use for this call.</span></span>

<span data-ttu-id="29826-115">*precpos*</span><span class="sxs-lookup"><span data-stu-id="29826-115">*precpos*</span></span>

<span data-ttu-id="29826-116">La descripción de la fracción que se va a usar para colocar el cursor en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="29826-116">The description of the fraction to use in positioning the cursor in the current index.</span></span>

### <a name="return-value"></a><span data-ttu-id="29826-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29826-117">Return Value</span></span>

<span data-ttu-id="29826-118">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="29826-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="29826-119">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="29826-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="29826-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="29826-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="29826-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="29826-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29826-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="29826-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="29826-123">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="29826-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29826-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="29826-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="29826-125">No se pudo completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="29826-125">The operation could not complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29826-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="29826-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="29826-127">No se pudo completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="29826-127">The operation could not complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="29826-128"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29826-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29826-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="29826-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="29826-130">El precpos especificado- &gt; cbStruct no es un tamaño válido para la estructura <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> , o precpos- &gt; centriesLT es mayor que precpos- &gt; centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="29826-130">The given precpos-&gt;cbStruct is not a valid size for the <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> structure, or precpos-&gt;centriesLT is greater than precpos-&gt;centriesTotal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29826-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="29826-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="29826-132">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="29826-132">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29826-133">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="29826-133">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="29826-134">Se devolverá este error si el índice está vacío.</span><span class="sxs-lookup"><span data-stu-id="29826-134">This error will be returned if the index is empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29826-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="29826-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="29826-136">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="29826-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29826-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="29826-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="29826-138">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="29826-138">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="29826-139"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29826-139"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29826-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="29826-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="29826-141">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="29826-141">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="29826-142">Si esta función se ejecuta correctamente, el cursor se mueve a un registro actual que es una fracción del camino a través del índice donde la fracción es precpos- \> centriesLT dividida por precpos- \> centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="29826-142">If this function succeeds, the cursor is moved to a current record that is a fraction of the way through the index where the fraction is precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="29826-143">Si se produce un error en esta función, la ubicación del cursor permanece sin cambios.</span><span class="sxs-lookup"><span data-stu-id="29826-143">If this function fails, the cursor location is left unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="29826-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29826-144">Remarks</span></span>

<span data-ttu-id="29826-145">Esta operación mueve el cursor por la tabla a una posición en el siguiente punto aproximado: precpos- \> centriesLT dividido por precpos- \> centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="29826-145">This operation moves the cursor through the table to a position at the following approximate point: precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="29826-146">Cuando las actualizaciones se producen de forma continua en la tabla, las llamadas subsiguientes con el mismo [JET_RECPOS](./jet-recpos-structure.md) pueden mover el cursor a distintas posiciones del índice, tanto antes como después de la posición anterior.</span><span class="sxs-lookup"><span data-stu-id="29826-146">When updates are occurring continuously on the table, subsequent calls with the same [JET_RECPOS](./jet-recpos-structure.md) can move the cursor to different positions in the index, both before and after the previous position.</span></span> <span data-ttu-id="29826-147">El aislamiento transaccional no se aplica a la colocación a través de [JET_RECPOS](./jet-recpos-structure.md) porque depende de las propiedades físicas del índice que no están aisladas de las transacciones.</span><span class="sxs-lookup"><span data-stu-id="29826-147">Transactional isolation does not apply to positioning through [JET_RECPOS](./jet-recpos-structure.md) since it depends on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="29826-148">[JET_RECPOS](./jet-recpos-structure.md) no se deben utilizar para describir un registro de una tabla o para cambiar la posición de un registro cerca de un registro existente.</span><span class="sxs-lookup"><span data-stu-id="29826-148">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="29826-149">En su lugar, los marcadores de un registro existente deben recuperarse después de un **JetGotoPosition** inicial y, a continuación, usarse para cambiar la posición del mismo registro.</span><span class="sxs-lookup"><span data-stu-id="29826-149">Instead, bookmarks for an existing record should be retrieved after an initial **JetGotoPosition** and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="29826-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29826-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29826-151"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="29826-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="29826-152">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="29826-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29826-153"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="29826-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="29826-154">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="29826-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29826-155"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="29826-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="29826-156">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="29826-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29826-157"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="29826-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="29826-158">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="29826-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29826-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="29826-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="29826-160">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="29826-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="29826-161">Consulte también</span><span class="sxs-lookup"><span data-stu-id="29826-161">See Also</span></span>

[<span data-ttu-id="29826-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="29826-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="29826-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="29826-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="29826-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="29826-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="29826-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="29826-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="29826-166">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="29826-166">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="29826-167">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="29826-167">JET_SETINFO</span></span>](./jet-setinfo-structure.md)
