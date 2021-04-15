---
description: 'Más información acerca de: JetIntersectIndexes (función)'
title: Función JetIntersectIndexes
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bdffa6f21a65ae7f438f87ea0d8d2adf4aed6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696219"
---
# <a name="jetintersectindexes-function"></a><span data-ttu-id="98ff0-103">Función JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="98ff0-103">JetIntersectIndexes Function</span></span>


<span data-ttu-id="98ff0-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="98ff0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetintersectindexes-function"></a><span data-ttu-id="98ff0-105">Función JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="98ff0-105">JetIntersectIndexes Function</span></span>

<span data-ttu-id="98ff0-106">La función **JetIntersectIndexes** calcula la intersección entre varios conjuntos de entradas de índice de distintos índices secundarios en la misma tabla.</span><span class="sxs-lookup"><span data-stu-id="98ff0-106">The **JetIntersectIndexes** function computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="98ff0-107">Esta operación es útil para buscar el conjunto de registros de una tabla que coinciden con dos o más criterios que se pueden expresar mediante intervalos de índice.</span><span class="sxs-lookup"><span data-stu-id="98ff0-107">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span>

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="98ff0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98ff0-108">Parameters</span></span>

<span data-ttu-id="98ff0-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="98ff0-109">*sesid*</span></span>

<span data-ttu-id="98ff0-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="98ff0-110">The session to use for this call.</span></span>

<span data-ttu-id="98ff0-111">*rgindexrange*</span><span class="sxs-lookup"><span data-stu-id="98ff0-111">*rgindexrange*</span></span>

<span data-ttu-id="98ff0-112">Puntero a una matriz de estructuras de [JET_IndexRange](./jet-indexrange-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="98ff0-112">A pointer to an array of [JET_IndexRange](./jet-indexrange-structure.md) structures.</span></span> <span data-ttu-id="98ff0-113">Cada estructura incluye una [JET_TABLEID](./jet-tableid.md) que se ha configurado para contener uno de los intervalos de índice que se van a intersectar.</span><span class="sxs-lookup"><span data-stu-id="98ff0-113">Each structure includes a [JET_TABLEID](./jet-tableid.md) that has been set up to hold one of the index ranges to be intersected.</span></span> <span data-ttu-id="98ff0-114">Para obtener más información, vea [JET_IndexRange](./jet-indexrange-structure.md).</span><span class="sxs-lookup"><span data-stu-id="98ff0-114">For more information, see [JET_IndexRange](./jet-indexrange-structure.md).</span></span>

<span data-ttu-id="98ff0-115">*cindexrange*</span><span class="sxs-lookup"><span data-stu-id="98ff0-115">*cindexrange*</span></span>

<span data-ttu-id="98ff0-116">El número de estructuras [JET_IndexRange](./jet-indexrange-structure.md) en la matriz contenida en el parámetro *rgindexrange* .</span><span class="sxs-lookup"><span data-stu-id="98ff0-116">The number of [JET_IndexRange](./jet-indexrange-structure.md) structures in the array that is contained in the *rgindexrange* parameter.</span></span>

<span data-ttu-id="98ff0-117">*precordlist*</span><span class="sxs-lookup"><span data-stu-id="98ff0-117">*precordlist*</span></span>

<span data-ttu-id="98ff0-118">Puntero a una estructura de [JET_RECORDLIST](./jet-recordlist-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="98ff0-118">Pointer to a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="98ff0-119">Esta estructura se rellenará con información suficiente para atravesar la tabla temporal con los resultados de **JetIntersectIndexes**.</span><span class="sxs-lookup"><span data-stu-id="98ff0-119">This structure will be populated with enough information to traverse the temporary table with the results from **JetIntersectIndexes**.</span></span>

<span data-ttu-id="98ff0-120">Búfer de salida que recibe una estructura de [JET_RECORDLIST](./jet-recordlist-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="98ff0-120">The output buffer that receives a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="98ff0-121">La estructura contiene una descripción del conjunto de resultados de la intersección.</span><span class="sxs-lookup"><span data-stu-id="98ff0-121">The structure contains a description of the result set of the intersection.</span></span>

<span data-ttu-id="98ff0-122">*grbit*</span><span class="sxs-lookup"><span data-stu-id="98ff0-122">*grbit*</span></span>

<span data-ttu-id="98ff0-123">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="98ff0-123">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="98ff0-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98ff0-124">Return Value</span></span>

<span data-ttu-id="98ff0-125">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="98ff0-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="98ff0-126">Para obtener más información sobre los errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="98ff0-126">For more information about ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98ff0-127">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="98ff0-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="98ff0-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="98ff0-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98ff0-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="98ff0-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="98ff0-130">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="98ff0-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98ff0-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="98ff0-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="98ff0-132">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="98ff0-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98ff0-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="98ff0-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="98ff0-134">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="98ff0-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="98ff0-135"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="98ff0-135"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98ff0-136">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="98ff0-136">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="98ff0-137">Una de las opciones solicitadas no era válida, se usó de forma incorrecta o no se implementó.</span><span class="sxs-lookup"><span data-stu-id="98ff0-137">One of the options requested was invalid, used incorrectly, or not implemented.</span></span></p>
<p><span data-ttu-id="98ff0-138"><strong>JetIntersectIndexes</strong> devuelve este error cuando:</span><span class="sxs-lookup"><span data-stu-id="98ff0-138">This error is returned by <strong>JetIntersectIndexes</strong> when:</span></span></p>
<p><span data-ttu-id="98ff0-139">El <em>grbit</em> contenido en la estructura <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> a la que apunta cualquier elemento de la matriz <em>rgindexrange</em> no es igual a JET_bitRecordInIndex.</span><span class="sxs-lookup"><span data-stu-id="98ff0-139">The <em>grbit</em> contained in the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure pointed to by any element in the <em>rgindexrange</em> array is not equal to JET_bitRecordInIndex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98ff0-140">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="98ff0-140">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="98ff0-141">Uno de los parámetros proporcionados contiene un valor inesperado o un valor incoherente cuando se combina con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="98ff0-141">One of the parameters provided contains an unexpected value or a value that is inconsistent when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="98ff0-142">Este error lo devuelve <strong>JetIntersectIndexes</strong> por las razones siguientes:</span><span class="sxs-lookup"><span data-stu-id="98ff0-142">This error is returned by <strong>JetIntersectIndexes</strong> for of the following reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="98ff0-143">El parámetro <em>precordlist</em> es NULL.</span><span class="sxs-lookup"><span data-stu-id="98ff0-143">The <em>precordlist</em> parameter is NULL.</span></span></p></li>
<li><p><span data-ttu-id="98ff0-144">El miembro <strong>cbStruct</strong> de la estructura <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> especificada en el parámetro <em>precordlist</em> no es igual que el tamaño de la estructura <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="98ff0-144">The <strong>cbStruct</strong> member of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure specified in the <em>precordlist</em> parameter is not equal to size of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="98ff0-145">El parámetro <em>cindexrange</em> es cero.</span><span class="sxs-lookup"><span data-stu-id="98ff0-145">The <em>cindexrange</em> parameter is zero.</span></span></p></li>
<li><p><span data-ttu-id="98ff0-146">El parámetro <em>cindexrange</em> es mayor que 64.</span><span class="sxs-lookup"><span data-stu-id="98ff0-146">The <em>cindexrange</em> parameter is greater than 64.</span></span></p></li>
<li><p><span data-ttu-id="98ff0-147">El miembro <strong>cbStruct</strong> de cualquier elemento de la matriz especificado por el parámetro <em>rgindexrange</em> no es igual que el tamaño de la estructura <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> .</span><span class="sxs-lookup"><span data-stu-id="98ff0-147">The <strong>cbStruct</strong> member for any element in the array specified by the <em>rgindexrange</em> parameter is not equal to the size of the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="98ff0-148">Los elementos de la matriz <em>rgindexrange</em> contienen <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s de tablas diferentes.</span><span class="sxs-lookup"><span data-stu-id="98ff0-148">The elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s from different tables.</span></span></p></li>
<li><p><span data-ttu-id="98ff0-149">Un elemento de la matriz <em>rgindexrange</em> contiene un <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> que no está situado en un índice secundario.</span><span class="sxs-lookup"><span data-stu-id="98ff0-149">An element in the <em>rgindexrange</em> array contains a <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> that is not positioned on a secondary index.</span></span></p></li>
<li><p><span data-ttu-id="98ff0-150">Uno o varios de los elementos de la matriz <em>rgindexrange</em> contienen <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>que se colocan en el mismo índice secundario.</span><span class="sxs-lookup"><span data-stu-id="98ff0-150">One or more of the elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s positioned on the same secondary index.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98ff0-151">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="98ff0-151">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="98ff0-152">El identificador de sesión no es válido o hace referencia a una sesión cerrada.</span><span class="sxs-lookup"><span data-stu-id="98ff0-152">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="98ff0-153">Este error no se devuelve en todas las circunstancias.</span><span class="sxs-lookup"><span data-stu-id="98ff0-153">This error is not returned under all circumstances.</span></span> <span data-ttu-id="98ff0-154">Los identificadores se validan solo en función del mejor esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="98ff0-154">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98ff0-155">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="98ff0-155">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="98ff0-156">No es posible completar la operación porque no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="98ff0-156">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98ff0-157">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="98ff0-157">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="98ff0-158">No se pudo realizar la operación porque el motor no pudo asignar los recursos necesarios para abrir un nuevo cursor.</span><span class="sxs-lookup"><span data-stu-id="98ff0-158">The operation failed because the engine could not allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="98ff0-159">Los recursos de cursor se configuran mediante una llamada a <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxCursors</em> especificado en el parámetro <em>paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="98ff0-159">Cursor resources are configured by calling <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxCursors</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98ff0-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="98ff0-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="98ff0-161">No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</span><span class="sxs-lookup"><span data-stu-id="98ff0-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="98ff0-162"><strong>JetIntersectIndexes</strong> puede devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host está demasiado fragmentado.</span><span class="sxs-lookup"><span data-stu-id="98ff0-162"><strong>JetIntersectIndexes</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="98ff0-163">El administrador de tablas temporales asignará siempre un fragmento de 1 MB de espacio de direcciones para cada tabla temporal creada independientemente de la cantidad de datos que se van a almacenar.</span><span class="sxs-lookup"><span data-stu-id="98ff0-163">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span> <span data-ttu-id="98ff0-164"><strong>JetIntersectIndexes</strong> creará una tabla temporal para cada <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> especificada en el parámetro <em>rgindexrange</em> y una tabla temporal para la salida en <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="98ff0-164"><strong>JetIntersectIndexes</strong> will create one temporary table for each <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> specified in the <em>rgindexrange</em> parameter, and one temporary table for the output in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98ff0-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="98ff0-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="98ff0-166">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="98ff0-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98ff0-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="98ff0-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="98ff0-168">No es válido utilizar la misma sesión desde más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="98ff0-168">It is illegal to use the same session from more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="98ff0-169"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="98ff0-169"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98ff0-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="98ff0-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="98ff0-171">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="98ff0-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98ff0-172">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="98ff0-172">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="98ff0-173">No se pudo realizar la operación porque el motor no pudo asignar los recursos necesarios para almacenar en caché los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="98ff0-173">The operation failed because the engine could not allocate the resources required to cache the indices of the table.</span></span> <span data-ttu-id="98ff0-174">El número de índices cuyo esquema se puede almacenar en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxOpenTables</em> especificado en el parámetro <em>paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="98ff0-174">The number of indices whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98ff0-175">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="98ff0-175">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="98ff0-176">No se pudo realizar la operación porque el motor no pudo asignar los recursos necesarios para almacenar en caché el esquema de la tabla.</span><span class="sxs-lookup"><span data-stu-id="98ff0-176">The operation failed because the engine could not allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="98ff0-177">El número de tablas cuyo esquema se puede almacenar en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxOpenTables</em> especificado en el parámetro <em>paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="98ff0-177">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98ff0-178">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="98ff0-178">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="98ff0-179">No se pudo realizar la operación porque el motor no pudo asignar los recursos necesarios para crear una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="98ff0-179">The operation failed because the engine could not allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="98ff0-180">Los recursos de tabla temporal se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con JET_paramMaxTemporaryTables especificado en el parámetro <em>paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="98ff0-180">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with JET_paramMaxTemporaryTables specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="98ff0-181">Si se ejecuta correctamente, se devuelve una nueva tabla temporal que contiene los marcadores de los registros que coinciden con los criterios representados por cada una de las descripciones del intervalo de índices de entrada.</span><span class="sxs-lookup"><span data-stu-id="98ff0-181">On success, a new temporary table is returned that contains the bookmarks of the records that match the criteria represented by each of the input index range descriptions.</span></span>

<span data-ttu-id="98ff0-182">En caso de error, no se creará la tabla temporal que contiene los resultados.</span><span class="sxs-lookup"><span data-stu-id="98ff0-182">On failure, the temporary table containing the results will not be created.</span></span> <span data-ttu-id="98ff0-183">Se puede cambiar el estado de la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="98ff0-183">The state of the temporary database may be changed.</span></span> <span data-ttu-id="98ff0-184">El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="98ff0-184">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span> <span data-ttu-id="98ff0-185">Se puede cambiar la posición actual del [JET_TABLEID](./jet-tableid.md)s proporcionado a esta función.</span><span class="sxs-lookup"><span data-stu-id="98ff0-185">The current position of the [JET_TABLEID](./jet-tableid.md)s provided to this function may be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="98ff0-186">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98ff0-186">Remarks</span></span>

<span data-ttu-id="98ff0-187">**JetIntersectIndexes** se puede usar para filtrar de forma eficaz los registros de una tabla mediante varios criterios si esos criterios se pueden expresar en términos de los índices secundarios de esa tabla.</span><span class="sxs-lookup"><span data-stu-id="98ff0-187">**JetIntersectIndexes** can be used to efficiently filter the records in a table by multiple criteria if those criteria can be expressed in terms of the secondary indices over that table.</span></span> <span data-ttu-id="98ff0-188">Por ejemplo, supongamos que tiene una tabla muy grande que contiene personas.</span><span class="sxs-lookup"><span data-stu-id="98ff0-188">For example, consider that you have a very large table containing people.</span></span> <span data-ttu-id="98ff0-189">La tabla puede tener columnas para el ID. de usuario, el nombre, el apellido, etc.</span><span class="sxs-lookup"><span data-stu-id="98ff0-189">The table can have columns for their user id, first name, last name, and so on.</span></span> <span data-ttu-id="98ff0-190">Supongamos que cada una de estas columnas se indexa por separado y que el índice principal de la tabla está por encima del identificador de usuario. Si desea buscar todos los usuarios cuyo nombre comienza por un y cuyo apellido empieza por G, debe realizar los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="98ff0-190">Suppose that each of these columns is indexed separately and that the primary index of the table is over user id. If you wanted to find everyone whose first name starts with an A and whose last name starts with G, you would perform the following steps:</span></span>

1.  <span data-ttu-id="98ff0-191">Abra un nuevo cursor en la tabla y establezca ese cursor para usar el índice sobre la columna "First Name".</span><span class="sxs-lookup"><span data-stu-id="98ff0-191">Open a new cursor on the table, and set that cursor to use the index over the "first name" column.</span></span> <span data-ttu-id="98ff0-192">A continuación, configure un intervalo de índice para todas las personas cuyo "First Name" comenzó con "A" y cree un [JET_IndexRange](./jet-indexrange-structure.md) struct que contenga este cursor.</span><span class="sxs-lookup"><span data-stu-id="98ff0-192">Then setup an index range for all people whose "first name" started with 'A', and build a [JET_IndexRange](./jet-indexrange-structure.md) struct that contains this cursor.</span></span>

2.  <span data-ttu-id="98ff0-193">Repita el paso 1 con un nuevo cursor en el índice "Last Name" para todas las personas cuyo "Last Name" comenzó con "G".</span><span class="sxs-lookup"><span data-stu-id="98ff0-193">Repeat step 1 with a new cursor on the "last name" index for all people whose "last name" started with 'G'.</span></span>

3.  <span data-ttu-id="98ff0-194">Pase estos criterios a **JetIntersectIndexes** para calcular el resultado en una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="98ff0-194">Pass these criteria to **JetIntersectIndexes** to compute the result into a temporary table.</span></span>

4.  <span data-ttu-id="98ff0-195">Recorra la tabla temporal y recupere cada uno de los registros que pasan los criterios por marcador.</span><span class="sxs-lookup"><span data-stu-id="98ff0-195">Traverse the temporary table and retrieve each of the records that pass the criteria by bookmark.</span></span>

<span data-ttu-id="98ff0-196">La tabla temporal que contiene el conjunto de resultados es una tabla simple con una columna que contiene el marcador de cada registro que pasó todos los criterios usados para calcular la intersección.</span><span class="sxs-lookup"><span data-stu-id="98ff0-196">The temporary table containing the result set is a simple table with one column that contains the bookmark of each record that passed all the criteria used to compute the intersection.</span></span> <span data-ttu-id="98ff0-197">El conjunto de resultados se ordena en el mismo orden que el índice principal y no contiene entradas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="98ff0-197">The result set is sorted in the same order as the primary index and contains no duplicate entries.</span></span> <span data-ttu-id="98ff0-198">La aplicación puede enumerar los resultados de la intersección enumerando las filas de la tabla temporal, recuperando el marcador de cada resultado mediante [JetRetrieveColumn](./jetretrievecolumn-function.md)y, a continuación, visitando el registro en la base de datos llamando a [JetGotoBookmark](./jetgotobookmark-function.md) con ese marcador en un cursor situado en el índice principal.</span><span class="sxs-lookup"><span data-stu-id="98ff0-198">The application can enumerate the results of the intersection by enumerating the rows in the temporary table, retrieving the bookmark for each result using [JetRetrieveColumn](./jetretrievecolumn-function.md), and then visiting the record in the database by calling [JetGotoBookmark](./jetgotobookmark-function.md) with that bookmark on a cursor positioned on the primary index.</span></span>

<span data-ttu-id="98ff0-199">La tabla temporal devuelta por **JetIntersectIndexes** solo se puede examinar en una dirección hacia delante.</span><span class="sxs-lookup"><span data-stu-id="98ff0-199">The temporary table returned by **JetIntersectIndexes** can only be scanned in a forward direction.</span></span> <span data-ttu-id="98ff0-200">También debe cerrarse a través de [JetCloseTable](./jetclosetable-function.md) cuando se haya completado el examen.</span><span class="sxs-lookup"><span data-stu-id="98ff0-200">It should also be closed via [JetCloseTable](./jetclosetable-function.md) when the scan has been completed.</span></span> <span data-ttu-id="98ff0-201">Para obtener más información acerca de las tablas temporales y cómo funcionan, vea [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="98ff0-201">For more information about temporary tables and how they work, see [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

<span data-ttu-id="98ff0-202">**JetIntersectIndexes** suele ser una manera eficaz y cómoda de filtrar registros en función de varios criterios indexados.</span><span class="sxs-lookup"><span data-stu-id="98ff0-202">**JetIntersectIndexes** is generally an efficient and convenient way to filter records based on multiple indexed criteria.</span></span> <span data-ttu-id="98ff0-203">Sin embargo, hay algunas sugerencias importantes que deben seguirse para maximizar la utilidad de esta característica.</span><span class="sxs-lookup"><span data-stu-id="98ff0-203">However, there are some important tips that should be followed to maximize the usefulness of this feature.</span></span> <span data-ttu-id="98ff0-204">Si sabe que uno de los criterios es tan restrictivo que el intervalo de índice resultante tiene muy pocos registros, probablemente sea mejor recorrer ese intervalo de índice y filtrar los registros en el nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="98ff0-204">If you know that one of the criteria is so restrictive that the resulting index range has very few records then it is probably better to simply walk that index range and filter the records at the application level.</span></span> <span data-ttu-id="98ff0-205">Además, si sabe que tiene criterios que son mucho menos restrictivos que otros criterios de la intersección, puede considerar la posibilidad de quitar esos criterios de la intersección de forma mucho menos restrictiva.</span><span class="sxs-lookup"><span data-stu-id="98ff0-205">Further, if you know that you have criteria that are much less restrictive than other criteria in your intersection then you might consider dropping those much less restrictive criteria from the intersection.</span></span> <span data-ttu-id="98ff0-206">Por último, si sabe que uno de los criterios no es estrictamente restrictivo, de modo que el intervalo de índice resultante es casi tan grande como el índice principal, es improbable que la intersección con ese intervalo de índice se beneficie (reduzca el tamaño del) del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="98ff0-206">Finally, if you know that one of the criteria is not at all restrictive such that the resulting index range is almost as large as the primary index then it is unlikely that intersecting with that index range will benefit (reduce the size of) the result set.</span></span> <span data-ttu-id="98ff0-207">En todos los casos, debe seleccionar los criterios de una manera que tomará el menor número posible de entradas de índice en la entrada y generará el conjunto más específico de marcadores en la salida para obtener el máximo rendimiento.</span><span class="sxs-lookup"><span data-stu-id="98ff0-207">In all cases, you should be selecting criteria in a manner that will take the fewest possible index entries on input and generate the most specific set of bookmarks on output for maximum performance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="98ff0-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98ff0-208">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98ff0-209"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="98ff0-209"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="98ff0-210">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="98ff0-210">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98ff0-211"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="98ff0-211"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="98ff0-212">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="98ff0-212">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98ff0-213"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="98ff0-213"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="98ff0-214">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="98ff0-214">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98ff0-215"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="98ff0-215"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="98ff0-216">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="98ff0-216">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98ff0-217"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="98ff0-217"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="98ff0-218">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="98ff0-218">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="98ff0-219">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98ff0-219">See Also</span></span>

[<span data-ttu-id="98ff0-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="98ff0-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="98ff0-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="98ff0-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="98ff0-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="98ff0-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="98ff0-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="98ff0-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="98ff0-224">JET_IndexRange</span><span class="sxs-lookup"><span data-stu-id="98ff0-224">JET_IndexRange</span></span>](./jet-indexrange-structure.md)  
[<span data-ttu-id="98ff0-225">JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="98ff0-225">JET_RECORDLIST</span></span>](./jet-recordlist-structure.md)  
[<span data-ttu-id="98ff0-226">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="98ff0-226">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="98ff0-227">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="98ff0-227">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="98ff0-228">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="98ff0-228">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
