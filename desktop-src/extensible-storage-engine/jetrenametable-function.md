---
description: 'Más información acerca de: JetRenameTable (función)'
title: JetRenameTable función)
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 624b194a1cad836b8927e6e7e4b8490fcad250b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361352"
---
# <a name="jetrenametable-function"></a><span data-ttu-id="a15b8-103">JetRenameTable función)</span><span class="sxs-lookup"><span data-stu-id="a15b8-103">JetRenameTable Function</span></span>


<span data-ttu-id="a15b8-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a15b8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenametable-function"></a><span data-ttu-id="a15b8-105">JetRenameTable función)</span><span class="sxs-lookup"><span data-stu-id="a15b8-105">JetRenameTable Function</span></span>

<span data-ttu-id="a15b8-106">La función **JetRenameTable** se puede usar para cambiar el nombre de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="a15b8-106">The **JetRenameTable** function can be used to change the name of an existing table.</span></span>

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a><span data-ttu-id="a15b8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a15b8-107">Parameters</span></span>

<span data-ttu-id="a15b8-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a15b8-108">*sesid*</span></span>

<span data-ttu-id="a15b8-109">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="a15b8-109">The session to use for this call.</span></span>

<span data-ttu-id="a15b8-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="a15b8-110">*dbid*</span></span>

<span data-ttu-id="a15b8-111">Base de datos que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="a15b8-111">The database to use for this call.</span></span>

<span data-ttu-id="a15b8-112">*szName*</span><span class="sxs-lookup"><span data-stu-id="a15b8-112">*szName*</span></span>

<span data-ttu-id="a15b8-113">Nombre actual de la tabla a la que se va a cambiar el nombre.</span><span class="sxs-lookup"><span data-stu-id="a15b8-113">The current name of the table that will be renamed.</span></span>

<span data-ttu-id="a15b8-114">*szNameNew*</span><span class="sxs-lookup"><span data-stu-id="a15b8-114">*szNameNew*</span></span>

<span data-ttu-id="a15b8-115">El nuevo nombre de la tabla a la que se va a cambiar el nombre.</span><span class="sxs-lookup"><span data-stu-id="a15b8-115">The new name for the table that will be renamed.</span></span>

### <a name="return-value"></a><span data-ttu-id="a15b8-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a15b8-116">Return Value</span></span>

<span data-ttu-id="a15b8-117">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="a15b8-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a15b8-118">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a15b8-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a15b8-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a15b8-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="a15b8-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a15b8-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a15b8-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a15b8-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a15b8-122">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a15b8-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a15b8-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a15b8-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a15b8-124">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a15b8-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a15b8-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a15b8-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a15b8-126">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="a15b8-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a15b8-127">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a15b8-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a15b8-128">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="a15b8-128">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="a15b8-129">La base de datos especificada no era válida.</span><span class="sxs-lookup"><span data-stu-id="a15b8-129">The specified database was invalid.</span></span></p>
<p><span data-ttu-id="a15b8-130">Este error solo se devuelve en Windows 2000 cuando se intenta realizar una operación de cambio de nombre de tabla en la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="a15b8-130">This error is only returned in Windows 2000 when a table rename operation is attempted on the temporary database.</span></span> <span data-ttu-id="a15b8-131">En este caso, se devuelve JET_errInvalidDatabaseId en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a15b8-131">JET_errInvalidDatabaseId is returned for this case in later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a15b8-132">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="a15b8-132">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="a15b8-133">El identificador de base de datos especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="a15b8-133">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a15b8-134">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="a15b8-134">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="a15b8-135">Uno de los nombres de objeto especificados no era válido.</span><span class="sxs-lookup"><span data-stu-id="a15b8-135">One of the specified object names was invalid.</span></span> <span data-ttu-id="a15b8-136">Todos los nombres de objeto deben cumplir el mismo conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="a15b8-136">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="a15b8-137">Estas reglas son:</span><span class="sxs-lookup"><span data-stu-id="a15b8-137">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="a15b8-138">Los nombres de objeto deben estar compuestos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="a15b8-138">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="a15b8-139">Los nombres de objeto deben tener al menos un carácter de longitud.</span><span class="sxs-lookup"><span data-stu-id="a15b8-139">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="a15b8-140">Los nombres de objeto no pueden superar JET_cbNameMost (64) caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="a15b8-140">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="a15b8-141">Los nombres de objeto no pueden comenzar con un espacio.</span><span class="sxs-lookup"><span data-stu-id="a15b8-141">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="a15b8-142">Los nombres de objeto no pueden contener caracteres de control ASCII (de 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="a15b8-142">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="a15b8-143">Los nombres de objeto no pueden contener un signo de exclamación (!), punto (.), corchete de apertura ([) o corchete de cierre (]) una vez validados, solo se usará la parte de la cadena hasta el primer espacio (si existe) para el nombre de objeto.</span><span class="sxs-lookup"><span data-stu-id="a15b8-143">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character - once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="a15b8-144">Esto significa que los nombres de objeto no pueden contener un espacio.</span><span class="sxs-lookup"><span data-stu-id="a15b8-144">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a15b8-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a15b8-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a15b8-146">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="a15b8-146">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="a15b8-147">Esto puede ocurrir para <strong>JetRenameTable</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="a15b8-147">This can happen for <strong>JetRenameTable</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="a15b8-148"><em>szName</em> es NULL.</span><span class="sxs-lookup"><span data-stu-id="a15b8-148"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="a15b8-149"><em>szNameNew</em> es NULL.</span><span class="sxs-lookup"><span data-stu-id="a15b8-149"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a15b8-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a15b8-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a15b8-151">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a15b8-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a15b8-152">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="a15b8-152">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="a15b8-153">Esta tabla especificada no existe para esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="a15b8-153">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a15b8-154">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a15b8-154">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a15b8-155">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a15b8-155">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a15b8-156">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a15b8-156">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a15b8-157">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="a15b8-157">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="a15b8-158">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a15b8-158">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a15b8-159">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a15b8-159">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a15b8-160">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a15b8-160">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a15b8-161">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="a15b8-161">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="a15b8-162">No se puede realizar una actualización mientras esté dentro del ámbito de una transacción de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a15b8-162">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="a15b8-163">Una transacción de solo lectura es una transacción que se ha iniciado mediante una llamada a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="a15b8-163">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="a15b8-164">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a15b8-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a15b8-165">Si se ejecuta correctamente, el nombre de la tabla especificada en la base de datos determinada se cambia permanentemente al nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="a15b8-165">On success, the name of the specified table in the given database is permanently changed to the new name.</span></span>

<span data-ttu-id="a15b8-166">En caso de error, no se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a15b8-166">On failure, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a15b8-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a15b8-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a15b8-168"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a15b8-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a15b8-169">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a15b8-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a15b8-170"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a15b8-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a15b8-171">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a15b8-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a15b8-172"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a15b8-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a15b8-173">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="a15b8-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a15b8-174"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="a15b8-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a15b8-175">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a15b8-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a15b8-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a15b8-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a15b8-177">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a15b8-177">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a15b8-178"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a15b8-178"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a15b8-179">Se implementa como <strong>JetRenameTableW</strong> (Unicode) y <strong>JetRenameTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a15b8-179">Implemented as <strong>JetRenameTableW</strong> (Unicode) and <strong>JetRenameTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a15b8-180">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a15b8-180">See Also</span></span>

[<span data-ttu-id="a15b8-181">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="a15b8-181">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="a15b8-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a15b8-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a15b8-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a15b8-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a15b8-184">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="a15b8-184">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)
