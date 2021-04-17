---
description: Proporciona estadísticas de replicación para una máquina virtual.
ms.assetid: 52d944a7-9309-4b56-97b7-e050a9501c57
title: Msvm_ReplicationStatistics (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationStatistics
- Msvm_ReplicationStatistics.InstanceID
- Msvm_ReplicationStatistics.Caption
- Msvm_ReplicationStatistics.Description
- Msvm_ReplicationStatistics.ElementName
- Msvm_ReplicationStatistics.StartStatisticTime
- Msvm_ReplicationStatistics.EndStatisticTime
- Msvm_ReplicationStatistics.ReplicationSuccessCount
- Msvm_ReplicationStatistics.ReplicationSize
- Msvm_ReplicationStatistics.MaxReplicationSize
- Msvm_ReplicationStatistics.ReplicationLatency
- Msvm_ReplicationStatistics.ReplicationMissCount
- Msvm_ReplicationStatistics.MaxReplicationLatency
- Msvm_ReplicationStatistics.NetworkFailureCount
- Msvm_ReplicationStatistics.ReplicationFailureCount
- Msvm_ReplicationStatistics.PendingReplicationSize
- Msvm_ReplicationStatistics.ApplicationConsistentSnapshotFailureCount
- Msvm_ReplicationStatistics.ReplicationHealth
- Msvm_ReplicationStatistics.LastTestFailoverTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f18501c2da875a9c3514549271fbc91620abef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687779"
---
# <a name="msvm_replicationstatistics-class"></a><span data-ttu-id="43264-103">MSVM \_ ReplicationStatistics (clase)</span><span class="sxs-lookup"><span data-stu-id="43264-103">Msvm\_ReplicationStatistics class</span></span>

<span data-ttu-id="43264-104">Proporciona estadísticas de replicación para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="43264-104">Provides replication statistics for a virtual machine.</span></span> <span data-ttu-id="43264-105">Estas estadísticas cubren la duración especificada por las propiedades **MonitoringStartTime** y **MonitoringInterval** de la clase [**MSVM \_ ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="43264-105">These statistics cover the duration specified by the **MonitoringStartTime** and **MonitoringInterval** properties of the [**Msvm\_ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) class.</span></span>

<span data-ttu-id="43264-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="43264-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="43264-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43264-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationStatistics : CIM_ManagedElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime StartStatisticTime;
  datetime EndStatisticTime;
  uint32   ReplicationSuccessCount;
  uint64   ReplicationSize;
  uint64   MaxReplicationSize;
  uint32   ReplicationLatency;
  uint32   ReplicationMissCount;
  uint32   MaxReplicationLatency;
  uint32   NetworkFailureCount;
  uint32   ReplicationFailureCount;
  uint64   PendingReplicationSize;
  uint32   ApplicationConsistentSnapshotFailureCount;
  uint32   ReplicationHealth;
  datetime LastTestFailoverTime;
};
```

## <a name="members"></a><span data-ttu-id="43264-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="43264-108">Members</span></span>

<span data-ttu-id="43264-109">La clase **MSVM \_ ReplicationStatistics** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="43264-109">The **Msvm\_ReplicationStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="43264-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43264-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43264-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43264-111">Properties</span></span>

<span data-ttu-id="43264-112">La clase **MSVM \_ ReplicationStatistics** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="43264-112">The **Msvm\_ReplicationStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43264-113">**ApplicationConsistentSnapshotFailureCount**</span><span class="sxs-lookup"><span data-stu-id="43264-113">**ApplicationConsistentSnapshotFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43264-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43264-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-116">Número total de errores de instantáneas de VSS.</span><span class="sxs-lookup"><span data-stu-id="43264-116">The total number of VSS snapshot failures.</span></span>

</dd> <dt>

<span data-ttu-id="43264-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="43264-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43264-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43264-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-120">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="43264-120">A short description of the object.</span></span> <span data-ttu-id="43264-121">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="43264-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="43264-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="43264-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43264-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43264-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-125">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="43264-125">A description of the object.</span></span> <span data-ttu-id="43264-126">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="43264-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="43264-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="43264-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43264-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43264-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-130">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="43264-130">A display name for the object.</span></span> <span data-ttu-id="43264-131">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="43264-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="43264-132">**EndStatisticTime**</span><span class="sxs-lookup"><span data-stu-id="43264-132">**EndStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-133">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43264-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43264-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-135">Hora, en UTC, en la que el servicio de réplica de Hyper-V dejó de recopilar datos de estadísticas de replicación.</span><span class="sxs-lookup"><span data-stu-id="43264-135">The time, in UTC, when the Hyper-V Replica service stopped gathering replication statistics data.</span></span> <span data-ttu-id="43264-136">En este momento, se inicia un nuevo ciclo de estadísticas de replicación.</span><span class="sxs-lookup"><span data-stu-id="43264-136">At this time, a new replication statistics cycle starts.</span></span>

</dd> <dt>

<span data-ttu-id="43264-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="43264-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43264-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43264-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43264-140">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="43264-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="43264-141">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="43264-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="43264-142">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="43264-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="43264-143">**LastTestFailoverTime**</span><span class="sxs-lookup"><span data-stu-id="43264-143">**LastTestFailoverTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-144">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43264-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43264-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-146">Indica la última vez que se creó un sistema de réplica de prueba para una máquina virtual habilitada para la replicación en el servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="43264-146">Indicates the last time a test replica system was created for a replication enabled virtual machine on the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="43264-147">**MaxReplicationLatency**</span><span class="sxs-lookup"><span data-stu-id="43264-147">**MaxReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-148">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43264-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43264-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-150">Cantidad máxima de tiempo que se tarda en completar un único ciclo de replicación, en segundos.</span><span class="sxs-lookup"><span data-stu-id="43264-150">The maximum amount of time taken to complete a single replication cycle, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="43264-151">**MaxReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="43264-151">**MaxReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-152">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="43264-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="43264-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-154">Número máximo de datos de replicación transferidos al sistema del host de recuperación, en bytes.</span><span class="sxs-lookup"><span data-stu-id="43264-154">Maximum replication data transferred to the recovery host system, in bytes.</span></span> <span data-ttu-id="43264-155">Representa el tamaño máximo de los datos de replicación enviados a través de un solo ciclo para este intervalo.</span><span class="sxs-lookup"><span data-stu-id="43264-155">This represents the maximum size of replication data sent over a single cycle for this interval.</span></span>

</dd> <dt>

<span data-ttu-id="43264-156">**NetworkFailureCount**</span><span class="sxs-lookup"><span data-stu-id="43264-156">**NetworkFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43264-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43264-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-159">El número total de errores de red encontrados para el canal de replicación con el sistema de host de recuperación.</span><span class="sxs-lookup"><span data-stu-id="43264-159">The total number of network errors encountered for the replication channel with recovery host system.</span></span>

</dd> <dt>

<span data-ttu-id="43264-160">**PendingReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="43264-160">**PendingReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-161">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="43264-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="43264-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-163">Tamaño de los datos para una replicación pendiente, en bytes.</span><span class="sxs-lookup"><span data-stu-id="43264-163">The size of the data for a pending replication, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="43264-164">**ReplicationFailureCount**</span><span class="sxs-lookup"><span data-stu-id="43264-164">**ReplicationFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-165">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43264-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43264-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-167">Número total de errores de replicación.</span><span class="sxs-lookup"><span data-stu-id="43264-167">The total number of replication failures.</span></span> <span data-ttu-id="43264-168">Esto incluye errores de operación de replicación.</span><span class="sxs-lookup"><span data-stu-id="43264-168">This includes errors for replication operation.</span></span>

</dd> <dt>

<span data-ttu-id="43264-169">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="43264-169">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-170">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43264-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43264-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-172">Mantenimiento de la replicación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="43264-172">The replication health for the virtual machine.</span></span> <span data-ttu-id="43264-173">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="43264-173">This will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="43264-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (0)</span><span class="sxs-lookup"><span data-stu-id="43264-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not applicable** (0)</span></span>
</dt> <dt>

<span data-ttu-id="43264-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="43264-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok** (1)</span></span>
</dt> <dt>

<span data-ttu-id="43264-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (2)</span><span class="sxs-lookup"><span data-stu-id="43264-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (2)</span></span>
</dt> <dt>

<span data-ttu-id="43264-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="43264-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Critical** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="43264-178">**ReplicationLatency**</span><span class="sxs-lookup"><span data-stu-id="43264-178">**ReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-179">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43264-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43264-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-181">Latencia total de replicación mientras se transfieren los datos al sistema host de recuperación, en segundos.</span><span class="sxs-lookup"><span data-stu-id="43264-181">Total replication latency while transferring the data to the recovery host system, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="43264-182">**ReplicationMissCount**</span><span class="sxs-lookup"><span data-stu-id="43264-182">**ReplicationMissCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-183">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43264-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43264-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-185">El número de ciclos de replicación que faltan.</span><span class="sxs-lookup"><span data-stu-id="43264-185">The number of missed replication cycles.</span></span> <span data-ttu-id="43264-186">Esto puede deberse a una gran carga de trabajo, problemas de red o errores de replicación.</span><span class="sxs-lookup"><span data-stu-id="43264-186">This can be because of heavy workload, network issues, or replication errors.</span></span>

</dd> <dt>

<span data-ttu-id="43264-187">**ReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="43264-187">**ReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-188">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="43264-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="43264-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-190">La cantidad total de datos de replicación transferidos al sistema host de recuperación, en bytes.</span><span class="sxs-lookup"><span data-stu-id="43264-190">The total amount of replication data transferred to the recovery host system, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="43264-191">**ReplicationSuccessCount**</span><span class="sxs-lookup"><span data-stu-id="43264-191">**ReplicationSuccessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-192">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43264-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43264-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-194">El número total de replicaciones correctas de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="43264-194">The total number of successful replications for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="43264-195">**StartStatisticTime**</span><span class="sxs-lookup"><span data-stu-id="43264-195">**StartStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43264-196">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43264-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43264-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43264-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43264-198">Hora, en UTC, a la que el servicio de réplica de Hyper-V empezó a recopilar datos de estadísticas de replicación.</span><span class="sxs-lookup"><span data-stu-id="43264-198">The time, in UTC, when the Hyper-V Replica service started gathering replication statistics data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43264-199">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43264-199">Requirements</span></span>



| <span data-ttu-id="43264-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="43264-200">Requirement</span></span> | <span data-ttu-id="43264-201">Value</span><span class="sxs-lookup"><span data-stu-id="43264-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43264-202">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43264-202">Minimum supported client</span></span><br/> | <span data-ttu-id="43264-203">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="43264-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="43264-204">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43264-204">Minimum supported server</span></span><br/> | <span data-ttu-id="43264-205">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="43264-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43264-206">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="43264-206">Namespace</span></span><br/>                | <span data-ttu-id="43264-207">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="43264-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="43264-208">MOF</span><span class="sxs-lookup"><span data-stu-id="43264-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43264-209"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43264-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="43264-210">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="43264-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43264-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="43264-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

