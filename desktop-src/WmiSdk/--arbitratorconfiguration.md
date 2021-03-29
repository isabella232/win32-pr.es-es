---
description: Limita los recursos internos que usan las operaciones iniciadas por los clientes WMI.
ms.assetid: e877899d-2f5e-4468-8c47-055fd4d16f56
ms.tgt_platform: multiple
title: __ArbitratorConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ArbitratorConfiguration
- Root.__ArbitratorConfiguration.OutstandingTasksTotal
- Root.__ArbitratorConfiguration.OutstandingTasksPerUser
- Root.__ArbitratorConfiguration.TaskThreadsTotal
- Root.__ArbitratorConfiguration.TaskThreadsPerUser
- Root.__ArbitratorConfiguration.QuotaRetryCount
- Root.__ArbitratorConfiguration.QuotaRetryWaitInterval
- Root.__ArbitratorConfiguration.TotalUsers
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerTask
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerUser
- Root.__ArbitratorConfiguration.TotalCacheMemory
- Root.__ArbitratorConfiguration.TotalCacheDiskPerTask
- Root.__ArbitratorConfiguration.TotalCacheDiskPerUser
- Root.__ArbitratorConfiguration.TotalCacheDisk
- Root.__ArbitratorConfiguration.TemporarySubscriptionsPerUser
- Root.__ArbitratorConfiguration.PermanentSubscriptionsPerUser
- Root.__ArbitratorConfiguration.PollingInstructionsPerUser
- Root.__ArbitratorConfiguration.PollingMemoryPerUser
- Root.__ArbitratorConfiguration.TemporarySubscriptionsTotal
- Root.__ArbitratorConfiguration.PermanentSubscriptionsTotal
- Root.__ArbitratorConfiguration.PollingInstructionsTotal
- Root.__ArbitratorConfiguration.PollingMemoryTotal
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 906164d6d715ed70bccecf61fba767ada622c74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277514"
---
# <a name="__arbitratorconfiguration-class"></a><span data-ttu-id="f3b90-103">\_\_Clase ArbitratorConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3b90-103">\_\_ArbitratorConfiguration class</span></span>

<span data-ttu-id="f3b90-104">La clase **\_ \_ ArbitratorConfiguration** es una clase de configuración que limita los recursos internos que usan las operaciones iniciadas por los clientes WMI.</span><span class="sxs-lookup"><span data-stu-id="f3b90-104">The **\_\_ArbitratorConfiguration** class is a configuration class that limits the internal resources that are used by operations initiated by WMI clients.</span></span> <span data-ttu-id="f3b90-105">Se trata de una clase singleton que reside en el \\ espacio de nombres raíz.</span><span class="sxs-lookup"><span data-stu-id="f3b90-105">This is a singleton class that resides in the \\root namespace.</span></span> <span data-ttu-id="f3b90-106">La clase se genera internamente, por lo que no hay ningún archivo MOF para ella.</span><span class="sxs-lookup"><span data-stu-id="f3b90-106">The class is internally generated so there is no MOF file for it.</span></span>

<span data-ttu-id="f3b90-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f3b90-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f3b90-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f3b90-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b90-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3b90-109">Syntax</span></span>

``` syntax
[singleton]
class __ArbitratorConfiguration : __SystemClass
{
  uint32 OutstandingTasksTotal;
  uint32 OutstandingTasksPerUser;
  uint32 TaskThreadsTotal;
  uint32 TaskThreadsPerUser;
  uint32 QuotaRetryCount;
  uint32 QuotaRetryWaitInterval;
  uint32 TotalUsers;
  uint32 TotalCacheMemoryPerTask;
  uint32 TotalCacheMemoryPerUser;
  uint32 TotalCacheMemory;
  uint32 TotalCacheDiskPerTask;
  uint32 TotalCacheDiskPerUser;
  uint32 TotalCacheDisk;
  uint32 TemporarySubscriptionsPerUser;
  uint32 PermanentSubscriptionsPerUser;
  uint32 PollingInstructionsPerUser;
  uint32 PollingMemoryPerUser;
  uint32 TemporarySubscriptionsTotal;
  uint32 PermanentSubscriptionsTotal;
  uint32 PollingInstructionsTotal;
  uint32 PollingMemoryTotal;
};
```

## <a name="members"></a><span data-ttu-id="f3b90-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f3b90-110">Members</span></span>

<span data-ttu-id="f3b90-111">La clase **\_ \_ ArbitratorConfiguration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f3b90-111">The **\_\_ArbitratorConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="f3b90-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3b90-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3b90-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3b90-113">Properties</span></span>

<span data-ttu-id="f3b90-114">La clase **\_ \_ ArbitratorConfiguration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f3b90-114">The **\_\_ArbitratorConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3b90-115">**OutstandingTasksPerUser**</span><span class="sxs-lookup"><span data-stu-id="f3b90-115">**OutstandingTasksPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-116">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-118">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-118">Unused.</span></span> <span data-ttu-id="f3b90-119">Número de tareas iniciadas por el usuario pendientes al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b90-119">Number of outstanding user initiated tasks at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-120">**OutstandingTasksTotal**</span><span class="sxs-lookup"><span data-stu-id="f3b90-120">**OutstandingTasksTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-121">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-123">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-123">Unused.</span></span> <span data-ttu-id="f3b90-124">Número total de tareas pendientes en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="f3b90-124">Total number of outstanding tasks at any time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-125">**PermanentSubscriptionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="f3b90-125">**PermanentSubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-126">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-128">Número de suscripciones permanentes permitidas para un usuario determinado al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b90-128">Number of permanent subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-129">**PermanentSubscriptionsTotal**</span><span class="sxs-lookup"><span data-stu-id="f3b90-129">**PermanentSubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-132">Número total de suscripciones permanentes permitidas para todos los usuarios al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b90-132">Total number of permanent subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-133">**PollingInstructionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="f3b90-133">**PollingInstructionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-136">Número de consultas de eventos de sondeo permitidas para un usuario determinado al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b90-136">Number of polling event queries allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-137">**PollingInstructionsTotal**</span><span class="sxs-lookup"><span data-stu-id="f3b90-137">**PollingInstructionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-138">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-140">Número total de instrucciones de sondeo permitidas para todos los usuarios al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b90-140">Total number of polling instructions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-141">**PollingMemoryPerUser**</span><span class="sxs-lookup"><span data-stu-id="f3b90-141">**PollingMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-142">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-144">La cantidad de consultas de eventos de sondeo de memoria, emitidas por un usuario determinado, puede consumir al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b90-144">Amount of memory polling event queries, issued by a particular user, can consume at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-145">**PollingMemoryTotal**</span><span class="sxs-lookup"><span data-stu-id="f3b90-145">**PollingMemoryTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-148">La cantidad total de memoria que sondea las consultas de eventos para todos los usuarios combinados puede realizarse en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="f3b90-148">Total amount of memory that polling event queries, for all users combined, can consumer at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-149">**QuotaRetryCount**</span><span class="sxs-lookup"><span data-stu-id="f3b90-149">**QuotaRetryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-150">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-152">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-152">Unused.</span></span> <span data-ttu-id="f3b90-153">Número de infracciones de cuota permitidas antes de que se cancele una tarea.</span><span class="sxs-lookup"><span data-stu-id="f3b90-153">Number of quota violations permitted before a task is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-154">**QuotaRetryWaitInterval**</span><span class="sxs-lookup"><span data-stu-id="f3b90-154">**QuotaRetryWaitInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-155">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-157">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-157">Unused.</span></span> <span data-ttu-id="f3b90-158">Retraso introducido en la ejecución de la tarea en cada infracción de cuota.</span><span class="sxs-lookup"><span data-stu-id="f3b90-158">Delay introduced into the task execution on each quota violation.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-159">**TaskThreadsPerUser**</span><span class="sxs-lookup"><span data-stu-id="f3b90-159">**TaskThreadsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-160">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-162">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-162">Unused.</span></span> <span data-ttu-id="f3b90-163">Número máximo de subprocesos de tarea asociados a un usuario determinado en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="f3b90-163">Maximum number of task threads associated with a particular user t any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-164">**TaskThreadsTotal**</span><span class="sxs-lookup"><span data-stu-id="f3b90-164">**TaskThreadsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-165">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-167">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-167">Unused.</span></span> <span data-ttu-id="f3b90-168">Número máximo de subprocesos de tareas.</span><span class="sxs-lookup"><span data-stu-id="f3b90-168">Maximum number of task threads.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-169">**TemporarySubscriptionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="f3b90-169">**TemporarySubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-170">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-172">Número de suscripciones temporales permitidas para un usuario determinado al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b90-172">Number of temporary subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-173">**TemporarySubscriptionsTotal**</span><span class="sxs-lookup"><span data-stu-id="f3b90-173">**TemporarySubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-174">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-176">Número total de suscripciones temporales permitidas para todos los usuarios al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b90-176">Total number of temporary subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-177">**TotalCacheDisk**</span><span class="sxs-lookup"><span data-stu-id="f3b90-177">**TotalCacheDisk**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-178">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-180">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-180">Unused.</span></span> <span data-ttu-id="f3b90-181">Total de caché de disco asociada a todos los usuarios al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b90-181">Total disk cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-182">**TotalCacheDiskPerTask**</span><span class="sxs-lookup"><span data-stu-id="f3b90-182">**TotalCacheDiskPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-183">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-185">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-185">Unused.</span></span> <span data-ttu-id="f3b90-186">Memoria caché de disco total asociada a una tarea determinada en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="f3b90-186">Total disk cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-187">**TotalCacheDiskPerUser**</span><span class="sxs-lookup"><span data-stu-id="f3b90-187">**TotalCacheDiskPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-188">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-190">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-190">Unused.</span></span> <span data-ttu-id="f3b90-191">Total de memoria caché de disco asociada a un usuario determinado al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b90-191">Total disk cache associated with a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-192">**TotalCacheMemory**</span><span class="sxs-lookup"><span data-stu-id="f3b90-192">**TotalCacheMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-193">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-195">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-195">Unused.</span></span> <span data-ttu-id="f3b90-196">Memoria caché total asociada a todos los usuarios al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b90-196">Total memory cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-197">**TotalCacheMemoryPerTask**</span><span class="sxs-lookup"><span data-stu-id="f3b90-197">**TotalCacheMemoryPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-198">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-200">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-200">Unused.</span></span> <span data-ttu-id="f3b90-201">Memoria caché total asociada a una tarea determinada en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="f3b90-201">Total memory cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-202">**TotalCacheMemoryPerUser**</span><span class="sxs-lookup"><span data-stu-id="f3b90-202">**TotalCacheMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-203">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-205">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-205">Unused.</span></span> <span data-ttu-id="f3b90-206">Memoria caché total asociada a un usuario determinado en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="f3b90-206">Total memory cache associated with a particular user at anyone time.</span></span>

</dd> <dt>

<span data-ttu-id="f3b90-207">**TotalUsers**</span><span class="sxs-lookup"><span data-stu-id="f3b90-207">**TotalUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b90-208">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3b90-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b90-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3b90-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3b90-210">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="f3b90-210">Unused.</span></span> <span data-ttu-id="f3b90-211">Número máximo de usuarios conectados.</span><span class="sxs-lookup"><span data-stu-id="f3b90-211">Maximum number of connected users.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3b90-212">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3b90-212">Remarks</span></span>

<span data-ttu-id="f3b90-213">**\_ \_ ArbitratorConfiguration** se hereda de [**\_ \_ SystemClass**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="f3b90-213">**\_\_ArbitratorConfiguration** is inherited from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b90-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3b90-214">Requirements</span></span>



| <span data-ttu-id="f3b90-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3b90-215">Requirement</span></span> | <span data-ttu-id="f3b90-216">Value</span><span class="sxs-lookup"><span data-stu-id="f3b90-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f3b90-217">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3b90-217">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b90-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3b90-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f3b90-219">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3b90-219">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b90-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3b90-220">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f3b90-221">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f3b90-221">Namespace</span></span><br/>                | <span data-ttu-id="f3b90-222">Root</span><span class="sxs-lookup"><span data-stu-id="f3b90-222">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f3b90-223">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3b90-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b90-224">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="f3b90-224">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="f3b90-225">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="f3b90-225">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

