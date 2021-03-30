---
description: 'Más información acerca de: JetStopServiceInstance2 (función)'
title: JetStopServiceInstance2 función)
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810358"
---
# <a name="jetstopserviceinstance2-function"></a><span data-ttu-id="b485e-103">JetStopServiceInstance2 función)</span><span class="sxs-lookup"><span data-stu-id="b485e-103">JetStopServiceInstance2 Function</span></span>


<span data-ttu-id="b485e-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b485e-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="b485e-105">La función **JetStopServiceInstance2** prepara una instancia antes de la suspensión y prepara una instancia después de la reanudación.</span><span class="sxs-lookup"><span data-stu-id="b485e-105">The **JetStopServiceInstance2** function prepares an instance prior to Suspend, and prepares an instance after Resume.</span></span> <span data-ttu-id="b485e-106">Suspender y reanudar son Estados de ejecución del modelo de ciclo de vida de aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="b485e-106">Suspend and Resume are execution states of the Windows Store App lifecycle model.</span></span>

<span data-ttu-id="b485e-107">La función **JetStopServiceInstance2** se presentó en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b485e-107">The **JetStopServiceInstance2** function was introduced in Windows 8.</span></span>

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a><span data-ttu-id="b485e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b485e-108">Parameters</span></span>

<span data-ttu-id="b485e-109">*repetición*</span><span class="sxs-lookup"><span data-stu-id="b485e-109">*instance*</span></span>

<span data-ttu-id="b485e-110">Instancia de de destino.</span><span class="sxs-lookup"><span data-stu-id="b485e-110">The target instance.</span></span> <span data-ttu-id="b485e-111">El tipo de datos **JET_INSTANCE** es un identificador de la instancia de la base de datos que se va a usar para una llamada a la API de jet.</span><span class="sxs-lookup"><span data-stu-id="b485e-111">The **JET_INSTANCE** data type is a handle to the instance of the database to use for a call to the JET API.</span></span> <span data-ttu-id="b485e-112">Este identificador se obtiene cuando se crea una instancia de la base de datos mediante una llamada a las funciones [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)o [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="b485e-112">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="b485e-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b485e-113">*grbit*</span></span>

<span data-ttu-id="b485e-114">Grupo de bits que especifica uno o más de los valores enumerados y definidos en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b485e-114">A group of bits that specifies one or more of the values listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b485e-115">Value</span><span class="sxs-lookup"><span data-stu-id="b485e-115">Value</span></span></p></th>
<th><p><span data-ttu-id="b485e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b485e-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b485e-117">JET_bitStopServiceAll</span><span class="sxs-lookup"><span data-stu-id="b485e-117">JET_bitStopServiceAll</span></span></p></td>
<td><p><span data-ttu-id="b485e-118">Detiene todos los servicios del motor de almacenamiento extensible (ESE) para la instancia especificada.</span><span class="sxs-lookup"><span data-stu-id="b485e-118">Stops all Extensible Storage Engine (ESE) services for the specified instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b485e-119">JET_bitStopServiceBackgroundUserTasks</span><span class="sxs-lookup"><span data-stu-id="b485e-119">JET_bitStopServiceBackgroundUserTasks</span></span></p></td>
<td><p><span data-ttu-id="b485e-120">Detiene las tareas de mantenimiento en segundo plano especificadas por el cliente que se reinician (por ejemplo, la desfragmentación de árbol B +).</span><span class="sxs-lookup"><span data-stu-id="b485e-120">Stops restartable client-specified background maintenance tasks (B+ Tree Defrag, for example).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b485e-121">JET_bitStopServiceQuiesceCaches</span><span class="sxs-lookup"><span data-stu-id="b485e-121">JET_bitStopServiceQuiesceCaches</span></span></p></td>
<td><p><span data-ttu-id="b485e-122">Quiesces todas las cachés desfasadas en el disco.</span><span class="sxs-lookup"><span data-stu-id="b485e-122">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="b485e-123">Este valor es asincrónico y se puede cancelar.</span><span class="sxs-lookup"><span data-stu-id="b485e-123">This value is asynchronous and can be canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b485e-124">JET_bitStopServiceResume</span><span class="sxs-lookup"><span data-stu-id="b485e-124">JET_bitStopServiceResume</span></span></p></td>
<td><p><span data-ttu-id="b485e-125">Reanuda las operaciones StopService emitidas previamente. es decir, reinicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="b485e-125">Resumes previously issued StopService operations; that is, it restarts the service.</span></span> <span data-ttu-id="b485e-126">Este valor se puede combinar con el parámetro <em>grbits</em> para reanudar servicios específicos o con JET_bitStopServiceAll para reanudar todos los servicios detenidos previamente.</span><span class="sxs-lookup"><span data-stu-id="b485e-126">This value can be combined with the <em>grbits</em> parameter to resume specific services, or with JET_bitStopServiceAll to Resume all previously stopped services.</span></span> <span data-ttu-id="b485e-127">Este bit solo se puede usar para reanudar StopServiceBackgroundUserTasks y JET_bitStopServiceQuiesceCaches.</span><span class="sxs-lookup"><span data-stu-id="b485e-127">This bit can only be used to resume StopServiceBackgroundUserTasks and JET_bitStopServiceQuiesceCaches.</span></span> <span data-ttu-id="b485e-128">Si anteriormente llamó a con JET_bitStopServiceAll, se producirá un error al intentar usar JET_bitStopServiceResume.</span><span class="sxs-lookup"><span data-stu-id="b485e-128">If you previously called with JET_bitStopServiceAll, an attempt to use JET_bitStopServiceResume will fail.</span></span> <span data-ttu-id="b485e-129">Si no se llama al segundo paso de reanudación, la aplicación tendrá un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="b485e-129">If the second resume step does not get called, the application will have degraded performance.</span></span> <span data-ttu-id="b485e-130">En esta situación, el punto de comprobación se mantiene en cero.</span><span class="sxs-lookup"><span data-stu-id="b485e-130">In this situation the checkpoint is kept at zero.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="b485e-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b485e-131">Return value</span></span>

<span data-ttu-id="b485e-132">Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="b485e-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="b485e-133">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b485e-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b485e-134">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b485e-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="b485e-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="b485e-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b485e-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b485e-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b485e-137">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b485e-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="b485e-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b485e-138">Remarks</span></span>

<span data-ttu-id="b485e-139">Esta función permite que una aplicación JET mueva la memoria caché de la base de datos a un estado limpio o casi limpio (con la e/s de sistema operativo inactiva), de modo que, si la aplicación se terminara, la recuperación sería rápida.</span><span class="sxs-lookup"><span data-stu-id="b485e-139">This function allows a JET application to move the database cache to a clean or nearly clean state (with the operating system I/O idle), such that if the application were to be terminated, recovery would be quick.</span></span> <span data-ttu-id="b485e-140">Este enfoque es preferible a la terminación de JET llamando a las funciones [JetTerm](./jetterm-function.md) o [JetDetachDatabase](./jetdetachdatabase-function.md) , de modo que en el escenario más común, la aplicación no se suspenda y, posteriormente, la aplicación tenga la memoria caché completa y esté lista para funcionar lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="b485e-140">This approach is preferred over terminating JET by calling the [JetTerm](./jetterm-function.md) or [JetDetachDatabase](./jetdetachdatabase-function.md) functions, so that in the more common scenario, the application is just unsuspended, and later the application has the whole cache and is ready to go as soon as possible.</span></span>

<span data-ttu-id="b485e-141">Si esta función se ejecuta correctamente, prepara la caché de base de datos para una suspensión inminente.</span><span class="sxs-lookup"><span data-stu-id="b485e-141">If this function succeeds, it prepares the database cache for an imminent suspension.</span></span> <span data-ttu-id="b485e-142">Esta función pone en cola el trabajo en un subproceso de trabajo en segundo plano y vuelve al autor de la llamada inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b485e-142">This function queues work to a background worker thread and returns to the caller immediately.</span></span> <span data-ttu-id="b485e-143">Se debe llamar a la función en función de la VisibilityNotice de PLM en lugar de llamar a desde el controlador de eventos de suspensión de la aplicación para asegurarse de que JET tiene tiempo para vaciar los búferes sucios antes de que un PLM se suspenda/finalice el proceso.</span><span class="sxs-lookup"><span data-stu-id="b485e-143">The function should be called based on the PLM VisibilityNotice as opposed to calling from the application's suspension event handler to ensure that JET has time to flush dirty buffers before PLM suspends/terminates the process.</span></span> <span data-ttu-id="b485e-144">Internamente, JET desencadena una distribución inmediata del mantenimiento del punto de comprobación en el cambio de configuración (actualización de puntos de comprobación o este nuevo bit de caché de inactividad).</span><span class="sxs-lookup"><span data-stu-id="b485e-144">Internally, JET triggers an immediate dispatch of checkpoint maintenance upon configuration change (either checkpoint update or this new quiesce caches bit).</span></span> <span data-ttu-id="b485e-145">Para obtener más información sobre los eventos de VisibilityNotice, vea [clase VisibilityChangedEventArgs](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span><span class="sxs-lookup"><span data-stu-id="b485e-145">For more information about VisibilityNotice events, see [VisibilityChangedEventArgs class](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span></span>

<span data-ttu-id="b485e-146">Se debe llamar dos veces a esta función.</span><span class="sxs-lookup"><span data-stu-id="b485e-146">This function must be called twice.</span></span> <span data-ttu-id="b485e-147">Se llama después de que la aplicación reciba el aviso de suspensión del sistema operativo, pero antes de que la aplicación se haya suspendido.</span><span class="sxs-lookup"><span data-stu-id="b485e-147">It is called after the application receives the suspension notice from the operating system, but before the application has been suspended.</span></span> <span data-ttu-id="b485e-148">Después, se vuelve a llamar después de que el sistema operativo reanude la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b485e-148">Then it is called again after the operating system resumes the application.</span></span> <span data-ttu-id="b485e-149">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b485e-149">For example:</span></span>

<span data-ttu-id="b485e-150">Cuando se llama a Suspend: JET_ERR JET_API JetStopServiceInstance2 (instancia, JET_bitStopServiceQuiesceCaches);</span><span class="sxs-lookup"><span data-stu-id="b485e-150">When called to Suspend: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches);</span></span>

<span data-ttu-id="b485e-151">Cuando se reanude: JET_ERR JET_API JetStopServiceInstance2 (instancia, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);</span><span class="sxs-lookup"><span data-stu-id="b485e-151">When Resumed: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches|JET_bitStopServiceResume );</span></span>

#### <a name="requirements"></a><span data-ttu-id="b485e-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b485e-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b485e-153"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b485e-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b485e-154">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b485e-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b485e-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b485e-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b485e-156">Requiere Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b485e-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b485e-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b485e-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b485e-158">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="b485e-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b485e-159"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="b485e-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b485e-160">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b485e-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b485e-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b485e-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b485e-162">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b485e-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b485e-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="b485e-163">See also</span></span>

[<span data-ttu-id="b485e-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b485e-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b485e-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b485e-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="b485e-166">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="b485e-166">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="b485e-167">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b485e-167">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="b485e-168">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="b485e-168">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="b485e-169">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="b485e-169">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="b485e-170">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="b485e-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="b485e-171">JetRollback</span><span class="sxs-lookup"><span data-stu-id="b485e-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="b485e-172">JetTerm</span><span class="sxs-lookup"><span data-stu-id="b485e-172">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="b485e-173">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="b485e-173">JetTerm2</span></span>](./jetterm2-function.md)
