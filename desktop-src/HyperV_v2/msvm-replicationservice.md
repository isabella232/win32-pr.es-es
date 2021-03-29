---
description: Administra la replicación de una máquina virtual.
ms.assetid: 0335fb94-5f2b-43be-bfb4-bc6811c5b507
title: Msvm_ReplicationService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService
- Msvm_ReplicationService.InstanceID
- Msvm_ReplicationService.Caption
- Msvm_ReplicationService.Description
- Msvm_ReplicationService.ElementName
- Msvm_ReplicationService.InstallDate
- Msvm_ReplicationService.Name
- Msvm_ReplicationService.OperationalStatus
- Msvm_ReplicationService.StatusDescriptions
- Msvm_ReplicationService.Status
- Msvm_ReplicationService.HealthState
- Msvm_ReplicationService.CommunicationStatus
- Msvm_ReplicationService.DetailedStatus
- Msvm_ReplicationService.OperatingStatus
- Msvm_ReplicationService.PrimaryStatus
- Msvm_ReplicationService.EnabledState
- Msvm_ReplicationService.OtherEnabledState
- Msvm_ReplicationService.RequestedState
- Msvm_ReplicationService.EnabledDefault
- Msvm_ReplicationService.TimeOfLastStateChange
- Msvm_ReplicationService.AvailableRequestedStates
- Msvm_ReplicationService.TransitioningToState
- Msvm_ReplicationService.SystemCreationClassName
- Msvm_ReplicationService.SystemName
- Msvm_ReplicationService.CreationClassName
- Msvm_ReplicationService.PrimaryOwnerName
- Msvm_ReplicationService.PrimaryOwnerContact
- Msvm_ReplicationService.StartMode
- Msvm_ReplicationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86e9140e2fe9b047c57c762be2e0fba048511993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277383"
---
# <a name="msvm_replicationservice-class"></a><span data-ttu-id="c404f-103">MSVM \_ ReplicationService (clase)</span><span class="sxs-lookup"><span data-stu-id="c404f-103">Msvm\_ReplicationService class</span></span>

<span data-ttu-id="c404f-104">Administra la replicación de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c404f-104">Manages the replication for a virtual machine.</span></span>

<span data-ttu-id="c404f-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c404f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c404f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c404f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Replica Service";
  string   Description = "Replication Service";
  string   ElementName;
  datetime InstallDate;
  string   Name = "replicasvc";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ReplicationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="c404f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c404f-107">Members</span></span>

<span data-ttu-id="c404f-108">La clase **MSVM \_ ReplicationService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c404f-108">The **Msvm\_ReplicationService** class has these types of members:</span></span>

-   [<span data-ttu-id="c404f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c404f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c404f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c404f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c404f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c404f-111">Methods</span></span>

<span data-ttu-id="c404f-112">La clase **MSVM \_ ReplicationService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c404f-112">The **Msvm\_ReplicationService** class has these methods.</span></span>



| <span data-ttu-id="c404f-113">Método</span><span class="sxs-lookup"><span data-stu-id="c404f-113">Method</span></span>                                                                                                 | <span data-ttu-id="c404f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c404f-114">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c404f-115">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="c404f-115">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="c404f-116">Agrega una entrada de autorización a un servidor.</span><span class="sxs-lookup"><span data-stu-id="c404f-116">Adds an authorization entry to a server.</span></span><br/>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="c404f-117">**ChangeReplicationModeToPrimary**</span><span class="sxs-lookup"><span data-stu-id="c404f-117">**ChangeReplicationModeToPrimary**</span></span>](changereplicationmodetoprimary-msvm-replicationservice.md)       | <span data-ttu-id="c404f-118">Cambia la relación de replicación extendida a la relación principal de una máquina virtual de réplica.</span><span class="sxs-lookup"><span data-stu-id="c404f-118">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="c404f-119">La máquina virtual de réplica debe estar en un estado de conmutación por error confirmada.</span><span class="sxs-lookup"><span data-stu-id="c404f-119">The replica virtual machine must be in a failover committed state.</span></span><br/> <span data-ttu-id="c404f-120">**Windows 8.1:** Este método no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c404f-120">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="c404f-121">**CommitFailover**</span><span class="sxs-lookup"><span data-stu-id="c404f-121">**CommitFailover**</span></span>](commitfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="c404f-122">Confirma la instantánea de recuperación que el método [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) ha usado para una conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="c404f-122">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="c404f-123">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="c404f-123">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="c404f-124">Crea una nueva relación de replicación para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c404f-124">Creates a new replication relationship for a virtual machine.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="c404f-125">**GetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="c404f-125">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)                   | <span data-ttu-id="c404f-126">Recupera las estadísticas de replicación de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c404f-126">Retrieves replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="c404f-127">**GetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="c404f-127">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)               | <span data-ttu-id="c404f-128">Recupera las estadísticas de replicación asociadas a la relación de replicación especificada de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c404f-128">Retrieves the replication statistics that are associated with specified replication relationship of the virtual machine.</span></span><br/> <span data-ttu-id="c404f-129">**Windows 8.1:** Este método no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c404f-129">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                    |
| [<span data-ttu-id="c404f-130">**GetSystemCertificates**</span><span class="sxs-lookup"><span data-stu-id="c404f-130">**GetSystemCertificates**</span></span>](getsystemcertificates-msvm-replicationservice.md)                         | <span data-ttu-id="c404f-131">Recupera los certificados del sistema en un sistema host.</span><span class="sxs-lookup"><span data-stu-id="c404f-131">Retrieves the system certificates on a host system.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="c404f-132">**ImportInitialReplica**</span><span class="sxs-lookup"><span data-stu-id="c404f-132">**ImportInitialReplica**</span></span>](importinitialreplica-msvm-replicationservice.md)                           | <span data-ttu-id="c404f-133">Importa la replicación inicial de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c404f-133">Imports the initial replication for a virtual machine.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="c404f-134">**InitiateFailback**</span><span class="sxs-lookup"><span data-stu-id="c404f-134">**InitiateFailback**</span></span>](initiatefailback-msvm-replicationservice.md)                                   | <span data-ttu-id="c404f-135">Inicia la conmutación por recuperación para una máquina virtual de recuperación.</span><span class="sxs-lookup"><span data-stu-id="c404f-135">Initiates the failback for a recovery virtual machine.</span></span> <span data-ttu-id="c404f-136">Es decir, establece la conmutación por error de la máquina virtual en una aplicación o una imagen coherente con bloqueos.</span><span class="sxs-lookup"><span data-stu-id="c404f-136">That is, sets the failover for the virtual machine to an app or crash consistent image.</span></span><br/> <span data-ttu-id="c404f-137">**Windows 8.1:** Este método no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c404f-137">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                              |
| [<span data-ttu-id="c404f-138">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="c404f-138">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)                                   | <span data-ttu-id="c404f-139">Inicia una conmutación por error para una máquina virtual en una imagen de punto de replicación estándar o de aplicación.</span><span class="sxs-lookup"><span data-stu-id="c404f-139">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="c404f-140">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="c404f-140">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="c404f-141">Modifica una entrada de autorización en un servidor.</span><span class="sxs-lookup"><span data-stu-id="c404f-141">Modifies an authorization entry on a server.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="c404f-142">**ModifyReplicationSettings**</span><span class="sxs-lookup"><span data-stu-id="c404f-142">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)                 | <span data-ttu-id="c404f-143">Modifica la configuración de replicación de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c404f-143">Modifies the replication settings for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="c404f-144">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="c404f-144">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)                         | <span data-ttu-id="c404f-145">Modifica la configuración del servicio réplica de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="c404f-145">Modifies the settings for the Hyper-V Replica service.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="c404f-146">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="c404f-146">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="c404f-147">Quita la entrada de autorización de un servidor.</span><span class="sxs-lookup"><span data-stu-id="c404f-147">Removes the authorization entry from a server.</span></span><br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="c404f-148">**RemoveReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="c404f-148">**RemoveReplicationRelationship**</span></span>](removereplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="c404f-149">Quita una relación de replicación de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c404f-149">Removes a virtual machine replication relationship.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="c404f-150">**RemoveReplicationRelationshipEx**</span><span class="sxs-lookup"><span data-stu-id="c404f-150">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)     | <span data-ttu-id="c404f-151">Quita la relación de replicación de la máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="c404f-151">Removes the specified virtual machine replication relationship.</span></span> <span data-ttu-id="c404f-152">En el caso de una máquina virtual de réplica, no se puede quitar la replicación principal si está habilitada la replicación extendida.</span><span class="sxs-lookup"><span data-stu-id="c404f-152">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span><br/> <span data-ttu-id="c404f-153">**Windows 8.1:** Este método no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c404f-153">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>     |
| [<span data-ttu-id="c404f-154">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c404f-154">**RequestStateChange**</span></span>](msvm-replicationservice-requeststatechange.md)                               | <span data-ttu-id="c404f-155">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="c404f-155">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="c404f-156">**ResetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="c404f-156">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)               | <span data-ttu-id="c404f-157">Restablece las estadísticas de replicación de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c404f-157">Resets the replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="c404f-158">**ResetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="c404f-158">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)           | <span data-ttu-id="c404f-159">Restablece las estadísticas de replicación que están asociadas a la relación de replicación especificada de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c404f-159">Resets replication statistics that are associated with the specified replication relationship of a virtual machine.</span></span><br/> <span data-ttu-id="c404f-160">**Windows 8.1:** Este método no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c404f-160">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                         |
| [<span data-ttu-id="c404f-161">**Vuelve a sincronizar.**</span><span class="sxs-lookup"><span data-stu-id="c404f-161">**Resynchronize**</span></span>](resynchronize-msvm-replicationservice.md)                                         | <span data-ttu-id="c404f-162">Realiza una operación de resincronización en la máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="c404f-162">Performs a resynchronization operation on the specified virtual machine.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="c404f-163">**ReverseReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="c404f-163">**ReverseReplicationRelationship**</span></span>](reversereplicationrelationship-msvm-replicationservice.md)       | <span data-ttu-id="c404f-164">Vuelve a replicar una máquina virtual conmutada por error en el servidor principal.</span><span class="sxs-lookup"><span data-stu-id="c404f-164">Replicates a failed-over virtual machine back to the primary server.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="c404f-165">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="c404f-165">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="c404f-166">Revierte la conmutación por error actual para una máquina virtual descartando el disco de conmutación por error actual.</span><span class="sxs-lookup"><span data-stu-id="c404f-166">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="c404f-167">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="c404f-167">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="c404f-168">Establece la entrada de autorización de replicación para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c404f-168">Sets the replication authorization entry for a virtual machine.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="c404f-169">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="c404f-169">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md) | <span data-ttu-id="c404f-170">Configura las opciones de IP del adaptador de red que se van a aplicar a una máquina virtual después de una conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="c404f-170">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="c404f-171">**StartReplication**</span><span class="sxs-lookup"><span data-stu-id="c404f-171">**StartReplication**</span></span>](startreplication-msvm-replicationservice.md)                                   | <span data-ttu-id="c404f-172">Inicia la replicación de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c404f-172">Starts the replication of a virtual machine.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="c404f-173">**StartService**</span><span class="sxs-lookup"><span data-stu-id="c404f-173">**StartService**</span></span>](msvm-replicationservice-startservice.md)                                           | <span data-ttu-id="c404f-174">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="c404f-174">Starts the service.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="c404f-175">**StopService**</span><span class="sxs-lookup"><span data-stu-id="c404f-175">**StopService**</span></span>](msvm-replicationservice-stopservice.md)                                             | <span data-ttu-id="c404f-176">detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="c404f-176">Stops the service.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="c404f-177">**TestReplicaSystem**</span><span class="sxs-lookup"><span data-stu-id="c404f-177">**TestReplicaSystem**</span></span>](testreplicasystem-msvm-replicationservice.md)                                 | <span data-ttu-id="c404f-178">Crea una nueva réplica de una máquina virtual con la instantánea especificada con fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="c404f-178">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="c404f-179">**TestReplicationConnection**</span><span class="sxs-lookup"><span data-stu-id="c404f-179">**TestReplicationConnection**</span></span>](testreplicationconnection-msvm-replicationservice.md)                 | <span data-ttu-id="c404f-180">Comprueba si la replicación se puede habilitar desde el sistema host actual al sistema de recuperación especificado.</span><span class="sxs-lookup"><span data-stu-id="c404f-180">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span><br/>                                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="c404f-181">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c404f-181">Properties</span></span>

<span data-ttu-id="c404f-182">La clase **MSVM \_ ReplicationService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c404f-182">The **Msvm\_ReplicationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c404f-183">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="c404f-183">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-184">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c404f-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c404f-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-186">Indica los valores posibles para el parámetro *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="c404f-186">Indicates the possible values for the *RequestedState* parameter.</span></span> <span data-ttu-id="c404f-187">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="c404f-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c404f-188">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c404f-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-191">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c404f-191">A short description of the object.</span></span> <span data-ttu-id="c404f-192">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de réplica de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="c404f-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Replica Service".</span></span>

</dd> <dt>

<span data-ttu-id="c404f-193">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c404f-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-194">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c404f-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-196">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="c404f-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c404f-197">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="c404f-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c404f-198">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c404f-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c404f-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c404f-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="c404f-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="c404f-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="c404f-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="c404f-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c404f-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="c404f-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c404f-206">)</span><span class="sxs-lookup"><span data-stu-id="c404f-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c404f-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c404f-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c404f-210">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="c404f-210">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c404f-211">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="c404f-211">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c404f-212">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ ReplicationService".</span><span class="sxs-lookup"><span data-stu-id="c404f-212">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ReplicationService".</span></span>

</dd> <dt>

<span data-ttu-id="c404f-213">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c404f-213">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-216">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c404f-216">A description of the object.</span></span> <span data-ttu-id="c404f-217">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de replicación".</span><span class="sxs-lookup"><span data-stu-id="c404f-217">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service".</span></span>

</dd> <dt>

<span data-ttu-id="c404f-218">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c404f-218">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-219">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c404f-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-221">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="c404f-221">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c404f-222">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="c404f-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c404f-223">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c404f-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c404f-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="c404f-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="c404f-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="c404f-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="c404f-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="c404f-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="c404f-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c404f-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="c404f-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c404f-232">)</span><span class="sxs-lookup"><span data-stu-id="c404f-232">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c404f-233">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c404f-233">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-234">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-236">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="c404f-236">A display name for the object.</span></span> <span data-ttu-id="c404f-237">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c404f-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c404f-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="c404f-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-239">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c404f-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-241">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c404f-241">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="c404f-242">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="c404f-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="c404f-243">Value</span><span class="sxs-lookup"><span data-stu-id="c404f-243">Value</span></span>                                                                        | <span data-ttu-id="c404f-244">Significado</span><span class="sxs-lookup"><span data-stu-id="c404f-244">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="c404f-245"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c404f-245"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c404f-246">habilitado</span><span class="sxs-lookup"><span data-stu-id="c404f-246">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c404f-247">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c404f-247">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-248">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c404f-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-250">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c404f-250">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c404f-251">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="c404f-251">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="c404f-252">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="c404f-252">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="c404f-253">Value</span><span class="sxs-lookup"><span data-stu-id="c404f-253">Value</span></span>                                                                        | <span data-ttu-id="c404f-254">Significado</span><span class="sxs-lookup"><span data-stu-id="c404f-254">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="c404f-255"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c404f-255"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c404f-256">habilitado</span><span class="sxs-lookup"><span data-stu-id="c404f-256">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c404f-257">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c404f-257">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-258">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c404f-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-260">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="c404f-260">The current health of the element.</span></span> <span data-ttu-id="c404f-261">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c404f-261">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="c404f-262">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="c404f-262">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="c404f-263">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="c404f-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="c404f-264">Value</span><span class="sxs-lookup"><span data-stu-id="c404f-264">Value</span></span>                                                                        | <span data-ttu-id="c404f-265">Significado</span><span class="sxs-lookup"><span data-stu-id="c404f-265">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="c404f-266"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c404f-266"><dt>5</dt></span></span> </dl> | <span data-ttu-id="c404f-267">El estado de mantenimiento es normal.</span><span class="sxs-lookup"><span data-stu-id="c404f-267">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c404f-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c404f-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-269">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c404f-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-271">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c404f-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="c404f-272">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c404f-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c404f-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c404f-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-274">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c404f-276">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="c404f-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c404f-277">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="c404f-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c404f-278">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c404f-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c404f-279">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c404f-279">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-280">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c404f-282">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="c404f-282">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c404f-283">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="c404f-283">The label by which the object is known.</span></span> <span data-ttu-id="c404f-284">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en "replicasvc".</span><span class="sxs-lookup"><span data-stu-id="c404f-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "replicasvc".</span></span>

</dd> <dt>

<span data-ttu-id="c404f-285">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c404f-285">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-286">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c404f-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-288">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="c404f-288">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c404f-289">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="c404f-289">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c404f-290">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c404f-290">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c404f-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c404f-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="c404f-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="c404f-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="c404f-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="c404f-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="c404f-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="c404f-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="c404f-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="c404f-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="c404f-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="c404f-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="c404f-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="c404f-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="c404f-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="c404f-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="c404f-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="c404f-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c404f-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="c404f-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c404f-310">)</span><span class="sxs-lookup"><span data-stu-id="c404f-310">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c404f-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c404f-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-312">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c404f-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c404f-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-314">Una matriz que contiene los Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="c404f-314">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="c404f-315">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c404f-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="c404f-316">El valor en el índice cero será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c404f-316">The value at index zero will be one of the following values.</span></span>



| <span data-ttu-id="c404f-317">Value</span><span class="sxs-lookup"><span data-stu-id="c404f-317">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="c404f-318">Significado</span><span class="sxs-lookup"><span data-stu-id="c404f-318">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="c404f-319"><dt>**Aceptar**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c404f-319"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                  | <span data-ttu-id="c404f-320">El servicio de replicación está funcionando con normalidad.</span><span class="sxs-lookup"><span data-stu-id="c404f-320">The replication service is operating normally.</span></span><br/>                                                                     |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span><dl> <span data-ttu-id="c404f-321"><dt>**Error**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c404f-321"><dt>**Error**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="c404f-322">Uno o más agentes de escucha de red de replicación no se están ejecutando.</span><span class="sxs-lookup"><span data-stu-id="c404f-322">One or more replication network listeners are not running.</span></span> <span data-ttu-id="c404f-323">Compruebe que la configuración del servicio de replicación sea válida.</span><span class="sxs-lookup"><span data-stu-id="c404f-323">Verify that the replication service settings are valid.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c404f-324">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="c404f-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-327">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="c404f-327">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="c404f-328">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="c404f-328">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="c404f-329">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="c404f-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c404f-330">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="c404f-330">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-331">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c404f-333">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="c404f-333">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c404f-334">Cualquier información sobre cómo se puede alcanzar el propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="c404f-334">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="c404f-335">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c404f-335">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c404f-336">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="c404f-336">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-337">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c404f-339">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="c404f-339">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="c404f-340">Nombre del propietario principal del servicio, si se ha definido uno.</span><span class="sxs-lookup"><span data-stu-id="c404f-340">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="c404f-341">El propietario principal es el contacto de soporte inicial para el servicio.</span><span class="sxs-lookup"><span data-stu-id="c404f-341">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="c404f-342">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c404f-342">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c404f-343">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c404f-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-344">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c404f-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-346">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="c404f-346">Provides high level status information.</span></span> <span data-ttu-id="c404f-347">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c404f-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="c404f-348">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="c404f-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c404f-349">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c404f-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c404f-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c404f-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-351"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="c404f-351"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="c404f-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="c404f-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c404f-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c404f-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="c404f-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c404f-356">)</span><span class="sxs-lookup"><span data-stu-id="c404f-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c404f-357">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c404f-357">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-358">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c404f-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-360">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="c404f-360">The last requested or desired state for the element.</span></span> <span data-ttu-id="c404f-361">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="c404f-361">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="c404f-362">Esta propiedad se proporciona para comparar el último estado solicitado y el actual para un elemento.</span><span class="sxs-lookup"><span data-stu-id="c404f-362">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="c404f-363">Una instancia concreta de la [**clase \_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir la propiedad **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="c404f-363">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="c404f-364">Si esto ocurre, se usa el valor 12 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="c404f-364">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="c404f-365">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="c404f-365">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="c404f-366">Value</span><span class="sxs-lookup"><span data-stu-id="c404f-366">Value</span></span>                                                                         | <span data-ttu-id="c404f-367">Significado</span><span class="sxs-lookup"><span data-stu-id="c404f-367">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="c404f-368"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="c404f-368"><dt>12</dt></span></span> </dl> | <span data-ttu-id="c404f-369">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="c404f-369">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c404f-370">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="c404f-370">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-371">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c404f-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-373">Indica si el servicio se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="c404f-373">Indicates whether the service is currently running.</span></span> <span data-ttu-id="c404f-374">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="c404f-374">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="c404f-375">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="c404f-375">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-376">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c404f-378">Calificadores: **MaxLen** (10)</span><span class="sxs-lookup"><span data-stu-id="c404f-378">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="c404f-379">Un valor de cadena que indica si el servicio se inicia automáticamente por un sistema, un sistema operativo o se inicia solo después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c404f-379">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="c404f-380">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c404f-380">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c404f-381">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c404f-381">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-382">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-384">Indica el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="c404f-384">Indicates the status of the element.</span></span> <span data-ttu-id="c404f-385">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en "OK".</span><span class="sxs-lookup"><span data-stu-id="c404f-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="c404f-386">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c404f-386">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-387">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c404f-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c404f-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-389">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c404f-389">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c404f-390">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c404f-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c404f-391">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c404f-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-392">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c404f-394">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="c404f-394">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c404f-395">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c404f-395">The scoping system's creation class name.</span></span> <span data-ttu-id="c404f-396">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="c404f-396">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="c404f-397">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c404f-397">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-398">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c404f-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c404f-400">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="c404f-400">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c404f-401">Nombre NetBIOS del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="c404f-401">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="c404f-402">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="c404f-402">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c404f-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="c404f-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-404">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c404f-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-406">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="c404f-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c404f-407">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c404f-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c404f-408">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="c404f-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c404f-409">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c404f-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c404f-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c404f-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c404f-411">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="c404f-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c404f-412">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="c404f-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c404f-413">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c404f-413">Requirements</span></span>



| <span data-ttu-id="c404f-414">Requisito</span><span class="sxs-lookup"><span data-stu-id="c404f-414">Requirement</span></span> | <span data-ttu-id="c404f-415">Value</span><span class="sxs-lookup"><span data-stu-id="c404f-415">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c404f-416">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c404f-416">Minimum supported client</span></span><br/> | <span data-ttu-id="c404f-417">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c404f-417">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c404f-418">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c404f-418">Minimum supported server</span></span><br/> | <span data-ttu-id="c404f-419">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c404f-419">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c404f-420">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c404f-420">Namespace</span></span><br/>                | <span data-ttu-id="c404f-421">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c404f-421">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c404f-422">MOF</span><span class="sxs-lookup"><span data-stu-id="c404f-422">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c404f-423"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c404f-423"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c404f-424">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c404f-424">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c404f-425"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c404f-425"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

