---
description: 'Más información acerca de: JetGetLS (función)'
title: JetGetLS función)
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716963"
---
# <a name="jetgetls-function"></a><span data-ttu-id="fe6ec-103">JetGetLS función)</span><span class="sxs-lookup"><span data-stu-id="fe6ec-103">JetGetLS Function</span></span>


<span data-ttu-id="fe6ec-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fe6ec-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetls-function"></a><span data-ttu-id="fe6ec-105">JetGetLS función)</span><span class="sxs-lookup"><span data-stu-id="fe6ec-105">JetGetLS Function</span></span>

<span data-ttu-id="fe6ec-106">La función **JetGetLS** permite que la aplicación recupere el identificador de contexto conocido como almacenamiento local que está asociado a un cursor o la tabla asociada a ese cursor.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-106">The **JetGetLS** function enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="fe6ec-107">Este identificador de contexto se debe haber establecido previamente mediante [JetSetLS](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="fe6ec-107">This context handle must have been previously set using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="fe6ec-108">**JetGetLS** también se puede usar para capturar simultáneamente el identificador de contexto actual para un cursor o una tabla y restablecer ese identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-108">**JetGetLS** can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="fe6ec-109">**Windows XP: JetGetLS** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-109">**Windows XP:  JetGetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="fe6ec-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe6ec-110">Parameters</span></span>

<span data-ttu-id="fe6ec-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="fe6ec-111">*sesid*</span></span>

<span data-ttu-id="fe6ec-112">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-112">The session to use for this call.</span></span>

<span data-ttu-id="fe6ec-113">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="fe6ec-113">*tableid*</span></span>

<span data-ttu-id="fe6ec-114">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-114">The cursor to use for this call.</span></span>

<span data-ttu-id="fe6ec-115">*pls*</span><span class="sxs-lookup"><span data-stu-id="fe6ec-115">*pls*</span></span>

<span data-ttu-id="fe6ec-116">Búfer de salida que recibe el identificador de contexto asociado actualmente al cursor o a la tabla.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-116">The output buffer that receives the context handle currently associated with the cursor or table.</span></span>

<span data-ttu-id="fe6ec-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="fe6ec-117">*grbit*</span></span>

<span data-ttu-id="fe6ec-118">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-118">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe6ec-119">Value</span><span class="sxs-lookup"><span data-stu-id="fe6ec-119">Value</span></span></p></th>
<th><p><span data-ttu-id="fe6ec-120">Significado</span><span class="sxs-lookup"><span data-stu-id="fe6ec-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe6ec-121">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="fe6ec-121">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="fe6ec-122">Indica que se debe recuperar el identificador de contexto asociado al cursor especificado.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-122">Indicates that the context handle associated with the given cursor should be retrieved.</span></span></p>
<p><span data-ttu-id="fe6ec-123">Si no se especifica ni JET_bitLSCursor ni JET_bitLSTable, se supone JET_bitLSCursor.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-123">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="fe6ec-124">Esta opción no se puede utilizar con JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-124">This option cannot be used with JET_bitLSTable.</span></span> <span data-ttu-id="fe6ec-125">Se producirá un error en la operación con JET_errInvalidgrbit si se intenta.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-125">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6ec-126">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="fe6ec-126">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="fe6ec-127">Indica que se debe recuperar el identificador de contexto asociado a la tabla que contiene el cursor especificado.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-127">Indicates that the context handle associated to the table that contains the given cursor should be retrieved.</span></span> <span data-ttu-id="fe6ec-128">No se puede usar esta opción con JET_bitLSCursor.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-128">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="fe6ec-129">Se producirá un error en la operación con JET_errInvalidgrbit si se intenta.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-129">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6ec-130">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="fe6ec-130">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="fe6ec-131">Indica que el identificador de contexto para el objeto elegido debe restablecerse a JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-131">Indicates that the context handle for the chosen object should be reset to JET_LSNil.</span></span> <span data-ttu-id="fe6ec-132">El valor actual del identificador de contexto se devuelve en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-132">The current value of the context handle is returned in the output buffer.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="fe6ec-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe6ec-133">Return Value</span></span>

<span data-ttu-id="fe6ec-134">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fe6ec-135">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fe6ec-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe6ec-136">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fe6ec-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="fe6ec-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe6ec-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe6ec-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fe6ec-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fe6ec-139">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6ec-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="fe6ec-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="fe6ec-141">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6ec-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="fe6ec-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="fe6ec-143">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="fe6ec-144">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-144">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6ec-145">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="fe6ec-145">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="fe6ec-146">Una de las opciones solicitadas no era válida, se usó de forma ilegal o no se implementó.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-146">One of the options requested was invalid, used in an illegal manner, or not implemented.</span></span></p>
<p><span data-ttu-id="fe6ec-147">Esto puede ocurrir para <strong>JetGetLS</strong> cuando se establecen tanto JET_bitLSCursor como JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-147">This can happen for <strong>JetGetLS</strong> when both JET_bitLSCursor and JET_bitLSTable are set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6ec-148">JET_errLSNotSet</span><span class="sxs-lookup"><span data-stu-id="fe6ec-148">JET_errLSNotSet</span></span></p></td>
<td><p><span data-ttu-id="fe6ec-149">No se pudo devolver el identificador de contexto porque actualmente no hay ningún identificador de contexto asociado al objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-149">The context handle could not be returned because no context handle is currently associated with the requested object.</span></span></p>
<p><span data-ttu-id="fe6ec-150"><strong>Nota:  </strong> Este error no se devuelve si se especifica JET_bitLSReset pero no se ha asociado ningún identificador de contexto al objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-150"><strong>Note  </strong> This error is not returned if JET_bitLSReset is specified yet no context handle was associated with the requested object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6ec-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="fe6ec-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="fe6ec-152">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6ec-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="fe6ec-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="fe6ec-154">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6ec-155">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="fe6ec-155">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="fe6ec-156">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-156">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fe6ec-157">En caso de éxito, el identificador de contexto se recuperó correctamente del objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-157">On success, the context handle was successfully retrieved from the requested object.</span></span> <span data-ttu-id="fe6ec-158">Si se especificó JET_bitLSReset, ese identificador de contexto también se quitó correctamente del objeto.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-158">If JET_bitLSReset was specified then that context handle was also successfully removed from the object.</span></span> <span data-ttu-id="fe6ec-159">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-159">No change to the database state will occur.</span></span>

<span data-ttu-id="fe6ec-160">En caso de error, no se ha producido ningún cambio en el estado del objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-160">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="fe6ec-161">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-161">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fe6ec-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe6ec-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe6ec-163"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="fe6ec-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6ec-164">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6ec-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fe6ec-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6ec-166">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6ec-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="fe6ec-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6ec-168">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6ec-169"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="fe6ec-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6ec-170">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6ec-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fe6ec-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6ec-172">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fe6ec-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fe6ec-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fe6ec-173">See Also</span></span>

[<span data-ttu-id="fe6ec-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fe6ec-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fe6ec-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fe6ec-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fe6ec-176">JET_LS</span><span class="sxs-lookup"><span data-stu-id="fe6ec-176">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="fe6ec-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fe6ec-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fe6ec-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fe6ec-178">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fe6ec-179">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="fe6ec-179">JetSetLS</span></span>](./jetsetls-function.md)
