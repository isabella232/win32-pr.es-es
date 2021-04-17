---
description: 'Más información acerca de: JetGetThreadStats (función)'
title: JetGetThreadStats función)
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85d45021910f818f297cd0bc9829580a18b7a296
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705451"
---
# <a name="jetgetthreadstats-function"></a><span data-ttu-id="31d8a-103">JetGetThreadStats función)</span><span class="sxs-lookup"><span data-stu-id="31d8a-103">JetGetThreadStats Function</span></span>


<span data-ttu-id="31d8a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="31d8a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetthreadstats-function"></a><span data-ttu-id="31d8a-105">JetGetThreadStats función)</span><span class="sxs-lookup"><span data-stu-id="31d8a-105">JetGetThreadStats Function</span></span>

<span data-ttu-id="31d8a-106">La función **JetGetThreadStats** recupera información de rendimiento del motor de base de datos para el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="31d8a-106">The **JetGetThreadStats** function retrieves performance information from the database engine for the current thread.</span></span> <span data-ttu-id="31d8a-107">Se pueden usar varias llamadas para recopilar estadísticas que reflejen la actividad del motor de base de datos en este subproceso entre esas llamadas.</span><span class="sxs-lookup"><span data-stu-id="31d8a-107">Multiple calls can be used to collect statistics that reflect the activity of the database engine on this thread between those calls.</span></span>

<span data-ttu-id="31d8a-108">**Windows Vista:**  **JetGetThreadStats** se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="31d8a-108">**Windows Vista:**  **JetGetThreadStats** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="31d8a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31d8a-109">Parameters</span></span>

<span data-ttu-id="31d8a-110">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="31d8a-110">*pvResult*</span></span>

<span data-ttu-id="31d8a-111">Búfer de salida que recibe los datos de las estadísticas del subproceso.</span><span class="sxs-lookup"><span data-stu-id="31d8a-111">The output buffer which receives the thread statistics data.</span></span> <span data-ttu-id="31d8a-112">El búfer contiene una estructura de [JET_THREADSTATS](./jet-threadstats-structure.md) después de una llamada correcta.</span><span class="sxs-lookup"><span data-stu-id="31d8a-112">The buffer contains a [JET_THREADSTATS](./jet-threadstats-structure.md) structure after a successful call.</span></span>

<span data-ttu-id="31d8a-113">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="31d8a-113">*cbMax*</span></span>

<span data-ttu-id="31d8a-114">Tamaño máximo en bytes del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="31d8a-114">The maximum size in bytes of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="31d8a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31d8a-115">Return Value</span></span>

<span data-ttu-id="31d8a-116">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="31d8a-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="31d8a-117">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="31d8a-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31d8a-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="31d8a-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="31d8a-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="31d8a-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31d8a-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="31d8a-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="31d8a-121">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="31d8a-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d8a-122">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="31d8a-122">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="31d8a-123">No se pudo realizar la operación porque el búfer de salida proporcionado era demasiado pequeño para contener los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="31d8a-123">The operation failed because the provided output buffer was too small to contain the requested data.</span></span> <span data-ttu-id="31d8a-124">La función <strong>JetGetThreadStats</strong> devolverá este error cuando el búfer de salida sea demasiado pequeño para contener la versión más pequeña de la estructura <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> compatible con el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="31d8a-124">The <strong>JetGetThreadStats</strong> function will return this error when the output buffer is too small to contain the smallest version of the <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> structure supported by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="31d8a-125">Si se ejecuta correctamente, el búfer de salida contendrá una estructura [JET_THREADSTATS](./jet-threadstats-structure.md) que contiene las estadísticas del motor de base de datos para el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="31d8a-125">On success, the output buffer will contain a [JET_THREADSTATS](./jet-threadstats-structure.md) structure that contains database engine statistics for the current thread.</span></span>

<span data-ttu-id="31d8a-126">En caso de error, el estado del búfer de salida es indefinido.</span><span class="sxs-lookup"><span data-stu-id="31d8a-126">On failure, the state of the output buffer is undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31d8a-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31d8a-127">Remarks</span></span>

<span data-ttu-id="31d8a-128">La información proporcionada por dos llamadas consecutivas de esta API está pensada para calcular el gasto de cualquier otra operación del motor de base de datos en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="31d8a-128">The information provided by two consecutive calls of this API are intended to be used to compute the expense of any other database engine operations on the current thread.</span></span> <span data-ttu-id="31d8a-129">Por lo general, esto se realiza tomando antes y después de leer las estadísticas y restar el recuento después del recuento anterior para obtener el número neto de operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="31d8a-129">Generally, this is done by taking a before and after reading of the statistics and subtracting the after count from the before count to get the net count of operations performed.</span></span>

<span data-ttu-id="31d8a-130">Por ejemplo, una aplicación podría llamar a **JetGetThreadStats** una vez para obtener una lectura inicial de las estadísticas para el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="31d8a-130">For example, an application could call **JetGetThreadStats** once to get an initial reading of the statistics for the current thread.</span></span> <span data-ttu-id="31d8a-131">Después, podría llamar a la función [JetMove](./jetmove-function.md) con el parámetro *cRow* establecido en JET_MoveNext para moverse a la entrada de índice siguiente en un índice.</span><span class="sxs-lookup"><span data-stu-id="31d8a-131">It could then call the [JetMove](./jetmove-function.md) function with the *cRow* parameter set to JET_MoveNext to move to the next index entry on an index.</span></span> <span data-ttu-id="31d8a-132">A continuación, podría llamar a **JetGetThreadStats** de nuevo para obtener otra lectura de las estadísticas del subproceso.</span><span class="sxs-lookup"><span data-stu-id="31d8a-132">It could then call **JetGetThreadStats** again to get another reading of the thread's statistics.</span></span> <span data-ttu-id="31d8a-133">A continuación, podría restar el contador cPageReferenced de la segunda lectura del primer.</span><span class="sxs-lookup"><span data-stu-id="31d8a-133">It could then subtract the cPageReferenced counter from the second reading from the first.</span></span> <span data-ttu-id="31d8a-134">El resultado sería el número de páginas de base de datos a las que hace referencia el motor de base de datos para realizar la operación [JetMove](./jetmove-function.md) .</span><span class="sxs-lookup"><span data-stu-id="31d8a-134">The result would be the number of database pages referenced by the database engine to perform the [JetMove](./jetmove-function.md) operation.</span></span>

<span data-ttu-id="31d8a-135">Las estadísticas de cada subproceso se acumulan durante la vigencia de ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="31d8a-135">The statistics for each thread are accumulated for the lifetime of that thread.</span></span> <span data-ttu-id="31d8a-136">Las estadísticas se restablecen si el archivo DLL del motor de base de datos se descarga del proceso de host.</span><span class="sxs-lookup"><span data-stu-id="31d8a-136">The statistics are reset if the database engine's DLL is unloaded from the host process.</span></span>

<span data-ttu-id="31d8a-137">La estructura de [JET_THREADSTATS](./jet-threadstats-structure.md) probablemente se expandirá en el futuro para contener más estadísticas.</span><span class="sxs-lookup"><span data-stu-id="31d8a-137">The [JET_THREADSTATS](./jet-threadstats-structure.md) structure will likely be expanded in the future to contain more statistics.</span></span> <span data-ttu-id="31d8a-138">Las nuevas estadísticas se agregarán al final de la estructura y se pueden recuperar con un mayor tamaño del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="31d8a-138">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="31d8a-139">La presencia de estadísticas adicionales se puede inferir con un valor de cbStruct mayor.</span><span class="sxs-lookup"><span data-stu-id="31d8a-139">The presence of additional statistics can be inferred by a larger cbStruct value.</span></span>

#### <a name="requirements"></a><span data-ttu-id="31d8a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31d8a-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31d8a-141"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="31d8a-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="31d8a-142">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="31d8a-142">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d8a-143"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="31d8a-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="31d8a-144">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="31d8a-144">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31d8a-145"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="31d8a-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="31d8a-146">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="31d8a-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31d8a-147"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="31d8a-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="31d8a-148">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="31d8a-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31d8a-149"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="31d8a-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="31d8a-150">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="31d8a-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="31d8a-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="31d8a-151">See Also</span></span>

[<span data-ttu-id="31d8a-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="31d8a-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="31d8a-153">JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="31d8a-153">JET_THREADSTATS</span></span>](./jet-threadstats-structure.md)  
[<span data-ttu-id="31d8a-154">JetMove</span><span class="sxs-lookup"><span data-stu-id="31d8a-154">JetMove</span></span>](./jetmove-function.md)
