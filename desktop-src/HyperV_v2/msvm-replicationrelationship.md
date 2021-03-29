---
description: Representa el estado de replicación de una relación de replicación.
ms.assetid: F11EFF86-5CC9-4310-8254-B310C54B561D
title: Msvm_ReplicationRelationship (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationRelationship
- Msvm_ReplicationRelationship.InstanceID
- Msvm_ReplicationRelationship.ReplicationState
- Msvm_ReplicationRelationship.ReplicationHealth
- Msvm_ReplicationRelationship.FailedOverReplicationType
- Msvm_ReplicationRelationship.LastReplicationType
- Msvm_ReplicationRelationship.LastApplicationConsistentReplicationTime
- Msvm_ReplicationRelationship.LastReplicationTime
- Msvm_ReplicationRelationship.LastApplyTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04665f96f4ec77501ee0b161d816c84943ca2c98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652713"
---
# <a name="msvm_replicationrelationship-class"></a><span data-ttu-id="b1420-103">MSVM \_ ReplicationRelationship (clase)</span><span class="sxs-lookup"><span data-stu-id="b1420-103">Msvm\_ReplicationRelationship class</span></span>

<span data-ttu-id="b1420-104">Representa el estado de replicación de una relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="b1420-104">Represents replication status for a replication relationship.</span></span> <span data-ttu-id="b1420-105">Dado que puede tener varias replicaciones para cada máquina virtual de réplica, puede usar esta clase para identificar cada relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="b1420-105">Because you can have multiple replications for each replica virtual machine, you can use this class to identify each replication relationship.</span></span>

<span data-ttu-id="b1420-106">La siguiente sintaxis se simplifica desde el código MOF e incluye estas propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b1420-106">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1420-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1420-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationRelationship : CIM_ManagedSystemElement
{
  string   InstanceID;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  datetime LastApplicationConsistentReplicationTime;
  datetime LastReplicationTime;
  datetime LastApplyTime;
};
```

## <a name="members"></a><span data-ttu-id="b1420-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b1420-108">Members</span></span>

<span data-ttu-id="b1420-109">La clase **MSVM \_ ReplicationRelationship** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b1420-109">The **Msvm\_ReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="b1420-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1420-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1420-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1420-111">Properties</span></span>

<span data-ttu-id="b1420-112">La clase **MSVM \_ ReplicationRelationship** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b1420-112">The **Msvm\_ReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1420-113">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="b1420-113">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1420-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1420-116">El tipo de conmutación por error que se realizó para la relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="b1420-116">The type of failover that was performed for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b1420-117">**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="b1420-117">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="b1420-118">**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="b1420-118">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="b1420-119">**Coherente** con la aplicación (2)</span><span class="sxs-lookup"><span data-stu-id="b1420-119">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="b1420-120">**Planeada** (3)</span><span class="sxs-lookup"><span data-stu-id="b1420-120">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1420-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b1420-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1420-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1420-124">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span><span class="sxs-lookup"><span data-stu-id="b1420-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="b1420-125">Identifica la relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="b1420-125">Identifies replication relationship.</span></span> <span data-ttu-id="b1420-126">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b1420-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="b1420-127">Esta propiedad tiene este formato:</span><span class="sxs-lookup"><span data-stu-id="b1420-127">This property has this format:</span></span>

<span data-ttu-id="b1420-128">**Microsoft: <vmid> \\ HVR \\<0/1>**</span><span class="sxs-lookup"><span data-stu-id="b1420-128">**Microsoft:<vmid>\\HVR\\<0/1>**</span></span>

<span data-ttu-id="b1420-129">0 indica principal y 1 indica [replicación extendida](#extended-replication).</span><span class="sxs-lookup"><span data-stu-id="b1420-129">0 indicates primary and 1 indicates [extended replication](#extended-replication).</span></span>

</dd> <dt>

<span data-ttu-id="b1420-130">**LastApplicationConsistentReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="b1420-130">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-131">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1420-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1420-133">Fecha y hora en que se recibe la última replicación coherente con la aplicación durante la recuperación de la relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="b1420-133">The date and time at which the last application consistent replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="b1420-134">**LastApplyTime**</span><span class="sxs-lookup"><span data-stu-id="b1420-134">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-135">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1420-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1420-137">Fecha y hora en que se aplica la última replicación durante la recuperación de la relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="b1420-137">The date and time at which the last replication is applied on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="b1420-138">**LastReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="b1420-138">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-139">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1420-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1420-141">Fecha y hora en que se recibió la última replicación durante la recuperación de la relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="b1420-141">The date and time at which the last replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="b1420-142">**LastReplicationType**</span><span class="sxs-lookup"><span data-stu-id="b1420-142">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-143">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1420-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1420-145">El tipo de la última replicación que se recibió para la relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="b1420-145">The type of the last replication that was received for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b1420-146">**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="b1420-146">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="b1420-147">**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="b1420-147">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="b1420-148">**Coherente** con la aplicación (2)</span><span class="sxs-lookup"><span data-stu-id="b1420-148">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="b1420-149">**Planeada** (3)</span><span class="sxs-lookup"><span data-stu-id="b1420-149">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1420-150">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="b1420-150">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1420-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1420-153">Mantenimiento de la replicación de la relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="b1420-153">Replication health for the replication relationship.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b1420-154">**No aplicable** (0)</span><span class="sxs-lookup"><span data-stu-id="b1420-154">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="b1420-155">**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="b1420-155">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b1420-156">**ADVERTENCIA** (2)</span><span class="sxs-lookup"><span data-stu-id="b1420-156">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="b1420-157">**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="b1420-157">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1420-158">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="b1420-158">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1420-159">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1420-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1420-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1420-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1420-161">Estado de replicación de la relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="b1420-161">Replication state for the replication relationship.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b1420-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="b1420-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="b1420-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Listo para la replicación** (1)</span><span class="sxs-lookup"><span data-stu-id="b1420-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="b1420-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Esperando para completar la replicación inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="b1420-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="b1420-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="b1420-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="b1420-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicación sincronizada completa** (4)</span><span class="sxs-lookup"><span data-stu-id="b1420-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="b1420-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recuperado** (5)</span><span class="sxs-lookup"><span data-stu-id="b1420-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="b1420-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Confirmado** (6)</span><span class="sxs-lookup"><span data-stu-id="b1420-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="b1420-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendido** (7)</span><span class="sxs-lookup"><span data-stu-id="b1420-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="b1420-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (8)</span><span class="sxs-lookup"><span data-stu-id="b1420-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="b1420-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Esperando para iniciar la resincronización** (9)</span><span class="sxs-lookup"><span data-stu-id="b1420-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="b1420-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>Volver a **sincronizar** (10)</span><span class="sxs-lookup"><span data-stu-id="b1420-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="b1420-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resincronización suspendida** (11)</span><span class="sxs-lookup"><span data-stu-id="b1420-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="b1420-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Conmutación por error en curso** (12)</span><span class="sxs-lookup"><span data-stu-id="b1420-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="b1420-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Conmutación por recuperación en curso** (13)</span><span class="sxs-lookup"><span data-stu-id="b1420-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="b1420-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Conmutación por recuperación completada** (14)</span><span class="sxs-lookup"><span data-stu-id="b1420-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="b1420-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Actualización de disco en curso** (15)</span><span class="sxs-lookup"><span data-stu-id="b1420-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b1420-178">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b1420-178">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="b1420-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Actualización de disco crítica** (16)</span><span class="sxs-lookup"><span data-stu-id="b1420-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b1420-180">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b1420-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1420-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (17)</span><span class="sxs-lookup"><span data-stu-id="b1420-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b1420-182">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b1420-182">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="b1420-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Reasignar la replicación en curso** (18)</span><span class="sxs-lookup"><span data-stu-id="b1420-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b1420-184">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b1420-184">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="b1420-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Preparado para la replicación de sincronización** (19)</span><span class="sxs-lookup"><span data-stu-id="b1420-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b1420-186">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b1420-186">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="b1420-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Preparado para la replicación inversa de grupo** (20)</span><span class="sxs-lookup"><span data-stu-id="b1420-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b1420-188">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b1420-188">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="b1420-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**FireDrill en curso** (21)</span><span class="sxs-lookup"><span data-stu-id="b1420-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b1420-190">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b1420-190">This property was added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1420-191">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1420-191">Remarks</span></span>

### <a name="extended-replication"></a><span data-ttu-id="b1420-192">Replicación extendida</span><span class="sxs-lookup"><span data-stu-id="b1420-192">Extended replication</span></span>

<span data-ttu-id="b1420-193">La característica de replicación de Hyper-V en Windows 8 permite que las máquinas virtuales que se ejecutan en un servidor de Hyper-V en el sitio principal se repliquen eficazmente en otro servidor de Hyper-V en el sitio secundario.</span><span class="sxs-lookup"><span data-stu-id="b1420-193">The Hyper-V replication feature in Windows 8 allows virtual machines that run on a Hyper-V server at the primary site to be efficiently replicated to another Hyper-V server at the secondary site.</span></span>

<span data-ttu-id="b1420-194">La característica de replicación de Hyper-V de Windows 8.1 permite a un usuario extender la relación de replicación desde el sitio secundario en adelante a un tercer sitio.</span><span class="sxs-lookup"><span data-stu-id="b1420-194">The Hyper-V replication feature in Windows 8.1 enables a user to extend the replication relationship from the secondary site onwards to a third site.</span></span> <span data-ttu-id="b1420-195">El tercer sitio puede ser un host de Hyper-V aprovisionado previamente como un servidor de recuperación o un proveedor de replicación externo.</span><span class="sxs-lookup"><span data-stu-id="b1420-195">The third site can be a Hyper-V host pre-provisioned as a recovery server or external replication provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1420-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1420-196">Requirements</span></span>



| <span data-ttu-id="b1420-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1420-197">Requirement</span></span> | <span data-ttu-id="b1420-198">Value</span><span class="sxs-lookup"><span data-stu-id="b1420-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1420-199">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1420-199">Minimum supported client</span></span><br/> | <span data-ttu-id="b1420-200">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b1420-200">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b1420-201">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1420-201">Minimum supported server</span></span><br/> | <span data-ttu-id="b1420-202">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1420-202">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b1420-203">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b1420-203">Namespace</span></span><br/>                | <span data-ttu-id="b1420-204">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b1420-204">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b1420-205">MOF</span><span class="sxs-lookup"><span data-stu-id="b1420-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1420-206"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1420-206"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1420-207">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1420-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1420-208"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b1420-208"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b1420-209">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1420-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1420-210">**ManagedSystemElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b1420-210">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="b1420-211">**ManagedSystemElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b1420-211">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

