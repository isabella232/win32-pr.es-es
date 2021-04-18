---
description: 'Más información acerca de: JetRenameColumn (función)'
title: JetRenameColumn función)
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ab2dee1895e4148bb2ea0600464d7e9c4a6a358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707020"
---
# <a name="jetrenamecolumn-function"></a><span data-ttu-id="4c3f7-103">JetRenameColumn función)</span><span class="sxs-lookup"><span data-stu-id="4c3f7-103">JetRenameColumn Function</span></span>


<span data-ttu-id="4c3f7-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4c3f7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenamecolumn-function"></a><span data-ttu-id="4c3f7-105">JetRenameColumn función)</span><span class="sxs-lookup"><span data-stu-id="4c3f7-105">JetRenameColumn Function</span></span>

<span data-ttu-id="4c3f7-106">La función **JetRenameColumn** se puede usar para cambiar el nombre de una columna existente en una tabla.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-106">The **JetRenameColumn** function can be used to change the name of an existing column on a table.</span></span>

<span data-ttu-id="4c3f7-107">**Windows XP:**  **JetRenameColumn** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-107">**Windows XP:**  **JetRenameColumn** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="4c3f7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c3f7-108">Parameters</span></span>

<span data-ttu-id="4c3f7-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="4c3f7-109">*sesid*</span></span>

<span data-ttu-id="4c3f7-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-110">The session to use for this call.</span></span>

<span data-ttu-id="4c3f7-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="4c3f7-111">*tableid*</span></span>

<span data-ttu-id="4c3f7-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-112">The cursor to use for this call.</span></span>

<span data-ttu-id="4c3f7-113">*szName*</span><span class="sxs-lookup"><span data-stu-id="4c3f7-113">*szName*</span></span>

<span data-ttu-id="4c3f7-114">Nombre actual de la columna cuyo nombre se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-114">The current name of the column that will be renamed.</span></span>

<span data-ttu-id="4c3f7-115">*szNameNew*</span><span class="sxs-lookup"><span data-stu-id="4c3f7-115">*szNameNew*</span></span>

<span data-ttu-id="4c3f7-116">Nombre nuevo de la columna a la que se va a cambiar el nombre.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-116">The new name for the column that will be renamed.</span></span>

<span data-ttu-id="4c3f7-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="4c3f7-117">*grbit*</span></span>

<span data-ttu-id="4c3f7-118">Este parámetro debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-118">This parameter must be 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="4c3f7-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c3f7-119">Return Value</span></span>

<span data-ttu-id="4c3f7-120">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4c3f7-121">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4c3f7-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c3f7-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4c3f7-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="4c3f7-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c3f7-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c3f7-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4c3f7-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4c3f7-125">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c3f7-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4c3f7-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4c3f7-127">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c3f7-128">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="4c3f7-128">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="4c3f7-129">Esta columna especificada no existe para esta tabla.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-129">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c3f7-130">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="4c3f7-130">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="4c3f7-131">Uno de los nombres de objeto especificados no era válido.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-131">One of the specified object names was invalid.</span></span> <span data-ttu-id="4c3f7-132">Todos los nombres de objeto deben cumplir el mismo conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-132">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="4c3f7-133">Estas reglas son:</span><span class="sxs-lookup"><span data-stu-id="4c3f7-133">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="4c3f7-134">Los nombres de objeto deben estar compuestos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-134">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="4c3f7-135">Los nombres de objeto deben tener al menos un carácter de longitud.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-135">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="4c3f7-136">Los nombres de objeto no pueden superar JET_cbNameMost (64) caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-136">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="4c3f7-137">Los nombres de objeto no pueden comenzar con un espacio: los nombres de objeto no pueden contener caracteres de control ASCII (de 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="4c3f7-137">Object names may not begin with a space - object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="4c3f7-138">Los nombres de objeto no pueden contener un carácter de exclamación (!), punto (.), corchete de apertura ([) o corchete de cierre (]).</span><span class="sxs-lookup"><span data-stu-id="4c3f7-138">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="4c3f7-139">Una vez validada, solo se usará la parte de la cadena hasta el primer espacio (si existe) para el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-139">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="4c3f7-140">Esto significa que los nombres de objeto no pueden contener un espacio.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-140">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c3f7-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4c3f7-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4c3f7-142">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="4c3f7-143">Esto puede ocurrir para <strong>JetRenameColumn</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="4c3f7-143">This can happen for <strong>JetRenameColumn</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="4c3f7-144"><em>szName</em> es NULL.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-144"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="4c3f7-145"><em>szNameNew</em> es NULL.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-145"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c3f7-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4c3f7-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4c3f7-147">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="4c3f7-148">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c3f7-149">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="4c3f7-149">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="4c3f7-150">Esta operación solo se puede realizar cuando la sesión no está dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-150">This operation may only be performed when the session is not currently inside a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c3f7-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4c3f7-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4c3f7-152">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c3f7-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4c3f7-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4c3f7-154">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c3f7-155">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4c3f7-155">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4c3f7-156">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-156">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="4c3f7-157">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c3f7-158">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4c3f7-158">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4c3f7-159">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-159">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c3f7-160">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="4c3f7-160">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="4c3f7-161">No se puede realizar una actualización mientras esté dentro del ámbito de una transacción de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-161">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="4c3f7-162">Una transacción de solo lectura es una transacción que se ha iniciado mediante una llamada a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-162">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="4c3f7-163">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-163">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4c3f7-164">Si se ejecuta correctamente, el nombre de la columna especificada en la tabla asociada al cursor se cambia de forma permanente al nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-164">On success, the name of the specified column in the table associated with the cursor is permanently changed to the new name.</span></span> <span data-ttu-id="4c3f7-165">También se actualizarán los índices que hagan referencia a esa columna.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-165">Any indexes that reference that column will also be updated.</span></span>

<span data-ttu-id="4c3f7-166">En caso de error, no se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-166">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4c3f7-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c3f7-167">Remarks</span></span>

<span data-ttu-id="4c3f7-168">La operación de cambio de nombre de columna es poco habitual porque, a diferencia de otras operaciones de esquema, no se lleva a cabo como una transacción.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-168">The column rename operation is unusual because, unlike other schema operations, it is not carried out as a transaction.</span></span> <span data-ttu-id="4c3f7-169">Cuando se cambia el nombre de una columna de una tabla determinada en una sesión, cualquier otra sesión que use esa tabla verá el cambio inmediatamente, incluso si se encuentran en una transacción que impediría que esa sesión pudiera ver cualquier otro cambio realizado por la sesión que realiza la operación de cambio de nombre.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-169">When a column in a given table is renamed in one session then any other session using that table will see the change immediately, even if they are in a transaction that would prevent that session from seeing any other change made by the session doing the rename operation.</span></span>

<span data-ttu-id="4c3f7-170">El ID. de columna de una columna no se ve afectado por la operación de cambio de nombre.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-170">The column ID of a column is not affected by the rename operation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4c3f7-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c3f7-171">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c3f7-172"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4c3f7-172"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4c3f7-173">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-173">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c3f7-174"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4c3f7-174"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4c3f7-175">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-175">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c3f7-176"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4c3f7-176"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4c3f7-177">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-177">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c3f7-178"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="4c3f7-178"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4c3f7-179">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-179">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c3f7-180"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4c3f7-180"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4c3f7-181">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-181">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c3f7-182"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4c3f7-182"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4c3f7-183">Se implementa como <strong>JetRenameColumnW</strong> (Unicode) y <strong>JetRenameColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4c3f7-183">Implemented as <strong>JetRenameColumnW</strong> (Unicode) and <strong>JetRenameColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4c3f7-184">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4c3f7-184">See Also</span></span>

[<span data-ttu-id="4c3f7-185">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4c3f7-185">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4c3f7-186">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4c3f7-186">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4c3f7-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4c3f7-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4c3f7-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4c3f7-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4c3f7-189">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="4c3f7-189">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)
