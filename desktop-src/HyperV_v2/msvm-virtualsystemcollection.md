---
description: Representa una colección de sistemas virtuales.
ms.assetid: acf51beb-1103-43a4-8dc5-1a7f2a0482be
title: Msvm_VirtualSystemCollection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCollection
- Msvm_VirtualSystemCollection.CollectionID
- Msvm_VirtualSystemCollection.ElementName
- Msvm_VirtualSystemCollection.LastApplyConsistencyLevel
- Msvm_VirtualSystemCollection.LastApplyVirtualMachineIds
- Msvm_VirtualSystemCollection.LastApplyTime
- Msvm_VirtualSystemCollection.FailedOverReplicationType
- Msvm_VirtualSystemCollection.ReplicationMode
- Msvm_VirtualSystemCollection.ReplicationState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a9746356744f2743a8d6656ef4c61044223be113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423691"
---
# <a name="msvm_virtualsystemcollection-class"></a><span data-ttu-id="3fa13-103">MSVM \_ VirtualSystemCollection (clase)</span><span class="sxs-lookup"><span data-stu-id="3fa13-103">Msvm\_VirtualSystemCollection class</span></span>

<span data-ttu-id="3fa13-104">Representa una colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="3fa13-104">Represents a collection of virtual systems.</span></span>

<span data-ttu-id="3fa13-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3fa13-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fa13-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fa13-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCollection : CIM_CollectionOfMSEs
{
  string   CollectionID;
  string   ElementName;
  uint16   LastApplyConsistencyLevel;
  String   LastApplyVirtualMachineIds[];
  DateTime LastApplyTime;
  uint16   FailedOverReplicationType;
  uint16   ReplicationMode;
  uint16   ReplicationState;
};
```

## <a name="members"></a><span data-ttu-id="3fa13-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3fa13-107">Members</span></span>

<span data-ttu-id="3fa13-108">La clase **MSVM \_ VirtualSystemCollection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3fa13-108">The **Msvm\_VirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="3fa13-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3fa13-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3fa13-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3fa13-110">Properties</span></span>

<span data-ttu-id="3fa13-111">La clase **MSVM \_ VirtualSystemCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3fa13-111">The **Msvm\_VirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3fa13-112">**Recopilación**</span><span class="sxs-lookup"><span data-stu-id="3fa13-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa13-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3fa13-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fa13-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3fa13-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fa13-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3fa13-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3fa13-116">Identificación única del objeto de colección.</span><span class="sxs-lookup"><span data-stu-id="3fa13-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="3fa13-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3fa13-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa13-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3fa13-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fa13-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3fa13-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fa13-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="3fa13-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="3fa13-121">Nombre definido por el usuario para la colección.</span><span class="sxs-lookup"><span data-stu-id="3fa13-121">An user-defined name for the collection.</span></span> <span data-ttu-id="3fa13-122">Tenga en cuenta que no se garantiza que sea único.</span><span class="sxs-lookup"><span data-stu-id="3fa13-122">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="3fa13-123">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="3fa13-123">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa13-124">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3fa13-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fa13-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3fa13-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fa13-126">Tipo de conmutación por error que se realizó para la colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="3fa13-126">Type of failover that was performed for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="3fa13-127">Agregado en Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="3fa13-127">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="3fa13-128">**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="3fa13-128">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="3fa13-129">**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="3fa13-129">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="3fa13-130">**Planeada** (2)</span><span class="sxs-lookup"><span data-stu-id="3fa13-130">**Planned** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3fa13-131">**LastApplyConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="3fa13-131">**LastApplyConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa13-132">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3fa13-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fa13-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3fa13-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fa13-134">Nivel de coherencia de la última diferencia aplicada.</span><span class="sxs-lookup"><span data-stu-id="3fa13-134">Consistency level of the last applied delta.</span></span>

> [!Note]  
> <span data-ttu-id="3fa13-135">Agregado en Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="3fa13-135">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3fa13-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3fa13-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="3fa13-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coherente** con la aplicación (1)</span><span class="sxs-lookup"><span data-stu-id="3fa13-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3fa13-138">La última diferencia aplicada indica un momento dado en el que el sistema virtual estaba en un estado coherente con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3fa13-138">The last applied delta indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="3fa13-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coherencia de bloqueos** (2)</span><span class="sxs-lookup"><span data-stu-id="3fa13-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3fa13-140">La última diferencia aplicada indica un momento dado en el que el sistema virtual se encontraba en un estado coherente con el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="3fa13-140">The last applied delta indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>

<span data-ttu-id="3fa13-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Coherencia de bloqueos de grupo** (3)</span><span class="sxs-lookup"><span data-stu-id="3fa13-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Group Crash Consistent** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3fa13-142">La última diferencia aplicada indica un momento dado en el que el grupo tenía un estado coherente con el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="3fa13-142">The last applied delta indicates a point in time when the group was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3fa13-143">**LastApplyTime**</span><span class="sxs-lookup"><span data-stu-id="3fa13-143">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa13-144">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3fa13-144">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="3fa13-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3fa13-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fa13-146">La hora a la que se aplica la última replicación en la recuperación de la colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="3fa13-146">The time at which the last replication is applied on recovery for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="3fa13-147">Agregado en Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="3fa13-147">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="3fa13-148">**LastApplyVirtualMachineIds**</span><span class="sxs-lookup"><span data-stu-id="3fa13-148">**LastApplyVirtualMachineIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa13-149">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3fa13-149">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="3fa13-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3fa13-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fa13-151">Matriz de identificadores de máquina virtual que se aplicaron correctamente en el último ciclo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="3fa13-151">Array of Virtual Machine Ids which were successfully applied in last apply cycle.</span></span>

> [!Note]  
> <span data-ttu-id="3fa13-152">Agregado en Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="3fa13-152">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="3fa13-153">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="3fa13-153">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa13-154">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3fa13-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fa13-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3fa13-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fa13-156">Tipo de replicación para la colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="3fa13-156">Replication type for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="3fa13-157">Agregado en Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="3fa13-157">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="3fa13-158">**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="3fa13-158">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="3fa13-159">**Principal** (1)</span><span class="sxs-lookup"><span data-stu-id="3fa13-159">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="3fa13-160">**Réplica** (2)</span><span class="sxs-lookup"><span data-stu-id="3fa13-160">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="3fa13-161">**Réplica de prueba** (3)</span><span class="sxs-lookup"><span data-stu-id="3fa13-161">**Test Replica** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3fa13-162">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="3fa13-162">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa13-163">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3fa13-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fa13-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3fa13-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fa13-165">Estado de replicación de la colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="3fa13-165">Replication state for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="3fa13-166">Agregado en Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="3fa13-166">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3fa13-167">**Deshabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="3fa13-167">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="3fa13-168">**Listo para la replicación** (1)</span><span class="sxs-lookup"><span data-stu-id="3fa13-168">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="3fa13-169">**Esperando para completar la replicación inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="3fa13-169">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="3fa13-170">**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="3fa13-170">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_initiated"></span><span id="failover_initiated"></span><span id="FAILOVER_INITIATED"></span>

<span data-ttu-id="3fa13-171">**Conmutación por error iniciada** (4)</span><span class="sxs-lookup"><span data-stu-id="3fa13-171">**Failover initiated** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="3fa13-172">**Recuperado** (5)</span><span class="sxs-lookup"><span data-stu-id="3fa13-172">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="3fa13-173">**Confirmado** (6)</span><span class="sxs-lookup"><span data-stu-id="3fa13-173">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="3fa13-174">**Suspendido** (7)</span><span class="sxs-lookup"><span data-stu-id="3fa13-174">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="3fa13-175">**Crítico** (8)</span><span class="sxs-lookup"><span data-stu-id="3fa13-175">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="3fa13-176">**Esperando para iniciar la resincronización** (9)</span><span class="sxs-lookup"><span data-stu-id="3fa13-176">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="3fa13-177">Volver a **sincronizar** (10)</span><span class="sxs-lookup"><span data-stu-id="3fa13-177">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned_failover_initiatedRepurpose_initiatedTest_failover_initiatedPartially_enabled"></span><span id="planned_failover_initiatedrepurpose_initiatedtest_failover_initiatedpartially_enabled"></span><span id="PLANNED_FAILOVER_INITIATEDREPURPOSE_INITIATEDTEST_FAILOVER_INITIATEDPARTIALLY_ENABLED"></span>

<span data-ttu-id="3fa13-178">**Conmutación por error InitiatedRepurpose initiatedTest** de conmutación por error initiatedPartially habilitada (11)</span><span class="sxs-lookup"><span data-stu-id="3fa13-178">**Planned failover initiatedRepurpose initiatedTest failover initiatedPartially enabled** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_disabled"></span><span id="partially_disabled"></span><span id="PARTIALLY_DISABLED"></span>

<span data-ttu-id="3fa13-179">**Parcialmente deshabilitado** (12)</span><span class="sxs-lookup"><span data-stu-id="3fa13-179">**Partially disabled** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_recovered"></span><span id="partially_recovered"></span><span id="PARTIALLY_RECOVERED"></span>

<span data-ttu-id="3fa13-180">**Parcialmente recuperado** (13)</span><span class="sxs-lookup"><span data-stu-id="3fa13-180">**Partially recovered** (13)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3fa13-181">(14)</span><span class="sxs-lookup"><span data-stu-id="3fa13-181">(14)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3fa13-182">(15)</span><span class="sxs-lookup"><span data-stu-id="3fa13-182">(15)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3fa13-183">(16)</span><span class="sxs-lookup"><span data-stu-id="3fa13-183">(16)</span></span>


<span data-ttu-id="3fa13-184"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3fa13-184"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="3fa13-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fa13-185">Requirements</span></span>



| <span data-ttu-id="3fa13-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fa13-186">Requirement</span></span> | <span data-ttu-id="3fa13-187">Value</span><span class="sxs-lookup"><span data-stu-id="3fa13-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa13-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fa13-188">Minimum supported client</span></span><br/> | <span data-ttu-id="3fa13-189">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="3fa13-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3fa13-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fa13-190">Minimum supported server</span></span><br/> | <span data-ttu-id="3fa13-191">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3fa13-191">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3fa13-192">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3fa13-192">Namespace</span></span><br/>                | <span data-ttu-id="3fa13-193">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3fa13-193">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3fa13-194">MOF</span><span class="sxs-lookup"><span data-stu-id="3fa13-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fa13-195"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fa13-195"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fa13-196">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3fa13-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fa13-197"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3fa13-197"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3fa13-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fa13-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa13-199">**CollectionOfMSEs de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3fa13-199">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

