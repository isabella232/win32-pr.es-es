---
description: 'Más información acerca de: JetStopServiceInstance (función)'
title: JetStopServiceInstance función)
TOCTitle: JetStopServiceInstance Function
ms:assetid: d8d3d047-91d6-4054-b3e1-44174666900e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294108(v=EXCHG.10)
ms:contentKeyID: 32765723
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopServiceInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b2e3307f13a63d00cbbaf33f491750bbfcdb9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715025"
---
# <a name="jetstopserviceinstance-function"></a><span data-ttu-id="e69fb-103">JetStopServiceInstance función)</span><span class="sxs-lookup"><span data-stu-id="e69fb-103">JetStopServiceInstance Function</span></span>


<span data-ttu-id="e69fb-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e69fb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopserviceinstance-function"></a><span data-ttu-id="e69fb-105">JetStopServiceInstance función)</span><span class="sxs-lookup"><span data-stu-id="e69fb-105">JetStopServiceInstance Function</span></span>

<span data-ttu-id="e69fb-106">La función **JetStopServiceInstance** prepara una instancia para la terminación.</span><span class="sxs-lookup"><span data-stu-id="e69fb-106">The **JetStopServiceInstance** function prepares an instance for termination.</span></span>

<span data-ttu-id="e69fb-107">**Windows XP:**  **JetStopServiceInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e69fb-107">**Windows XP:**  **JetStopServiceInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="e69fb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e69fb-108">Parameters</span></span>

<span data-ttu-id="e69fb-109">*repetición*</span><span class="sxs-lookup"><span data-stu-id="e69fb-109">*instance*</span></span>

<span data-ttu-id="e69fb-110">Instancia en ejecución que se va a usar para la llamada de API.</span><span class="sxs-lookup"><span data-stu-id="e69fb-110">The running instance to use for the API call.</span></span>

### <a name="return-value"></a><span data-ttu-id="e69fb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e69fb-111">Return Value</span></span>

<span data-ttu-id="e69fb-112">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="e69fb-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e69fb-113">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e69fb-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e69fb-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e69fb-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="e69fb-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e69fb-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e69fb-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e69fb-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e69fb-117">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e69fb-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e69fb-118">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e69fb-118">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e69fb-119">El parámetro de instancia especificado tiene un valor no válido (no una instancia que se está ejecutando actualmente).</span><span class="sxs-lookup"><span data-stu-id="e69fb-119">The specified instance parameter has an invalid value (not an instance that is currently running).</span></span></p>
<p><span data-ttu-id="e69fb-120"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e69fb-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e69fb-121">Si esta función se ejecuta correctamente, se prepara para una finalización futura.</span><span class="sxs-lookup"><span data-stu-id="e69fb-121">If this function succeeds, it prepares for a future termination.</span></span> <span data-ttu-id="e69fb-122">Entre los pasos necesarios para preparar una terminación se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e69fb-122">The steps taken to prepare for a termination include the following:</span></span>

  - <span data-ttu-id="e69fb-123">Detenga la desfragmentación con conexión si se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="e69fb-123">Stop online defragmentation if it is running.</span></span>

  - <span data-ttu-id="e69fb-124">Iniciar una limpieza del almacén de versiones.</span><span class="sxs-lookup"><span data-stu-id="e69fb-124">Start a version store clean-up.</span></span>

  - <span data-ttu-id="e69fb-125">Reduzca la profundidad del punto de control iniciando el vaciado de las páginas desfasadas en el administrador de búfer.</span><span class="sxs-lookup"><span data-stu-id="e69fb-125">Reduce the checkpoint depth by starting to flush dirty pages in the buffer manager.</span></span>

  - <span data-ttu-id="e69fb-126">Evite las llamadas futuras a la mayoría de las funciones para esa instancia.</span><span class="sxs-lookup"><span data-stu-id="e69fb-126">Prevent future calls to most functions for that instance.</span></span>

<span data-ttu-id="e69fb-127">Si se produce un error en esta función, no se realizará ninguno de los pasos para preparar la finalización de una instancia, por lo que no se producirá ningún cambio en el estado de la instancia.</span><span class="sxs-lookup"><span data-stu-id="e69fb-127">If this function fails, none of the steps to prepare for an instance termination will be taken, so no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e69fb-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e69fb-128">Remarks</span></span>

<span data-ttu-id="e69fb-129">Esta función reduce el trabajo que tendrá que hacer la instancia cuando termine, pero no finalizará la instancia.</span><span class="sxs-lookup"><span data-stu-id="e69fb-129">This function will reduce the work the instance will have to do when terminated but will not terminate the instance.</span></span> <span data-ttu-id="e69fb-130">Como resultado, esta función es simplemente una optimización y no es obligatoria para su uso.</span><span class="sxs-lookup"><span data-stu-id="e69fb-130">As a result, this function is just an optimization and is not mandatory to use.</span></span> <span data-ttu-id="e69fb-131">Tenga en cuenta que la cantidad de trabajo realizado en preparación fue inferior en Windows 2000 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e69fb-131">Note that the amount of work done in preparation was less in Windows 2000 and Windows XP.</span></span> <span data-ttu-id="e69fb-132">Una vez que la función se ejecuta correctamente, las funciones de llamada que ya no se permiten devolverán JET_errClientRequestToStopJetService.</span><span class="sxs-lookup"><span data-stu-id="e69fb-132">Once the function succeeds, calling functions that are no longer allowed will return JET_errClientRequestToStopJetService.</span></span> <span data-ttu-id="e69fb-133">Las funciones que todavía se permiten después de esta llamada son: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) y [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="e69fb-133">Functions that are still allowed after this call are: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="e69fb-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e69fb-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e69fb-135"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e69fb-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e69fb-136">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e69fb-136">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e69fb-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e69fb-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e69fb-138">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e69fb-138">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e69fb-139"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e69fb-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e69fb-140">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="e69fb-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e69fb-141"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="e69fb-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e69fb-142">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e69fb-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e69fb-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e69fb-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e69fb-144">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e69fb-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e69fb-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e69fb-145">See Also</span></span>

[<span data-ttu-id="e69fb-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e69fb-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e69fb-147">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e69fb-147">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="e69fb-148">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="e69fb-148">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="e69fb-149">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="e69fb-149">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="e69fb-150">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="e69fb-150">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="e69fb-151">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="e69fb-151">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="e69fb-152">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="e69fb-152">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="e69fb-153">JetRollback</span><span class="sxs-lookup"><span data-stu-id="e69fb-153">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="e69fb-154">JetTerm</span><span class="sxs-lookup"><span data-stu-id="e69fb-154">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="e69fb-155">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="e69fb-155">JetTerm2</span></span>](./jetterm2-function.md)
