---
description: Crea una nueva réplica de una máquina virtual con la instantánea especificada con fines de prueba.
ms.assetid: 447f3c8f-8c57-4874-9466-91c6aea533bc
title: Método TestReplicaSystem de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicaSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 029130e619aa36d0aa9b9c1c85a877fb26e1b22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912570"
---
# <a name="testreplicasystem-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="b656a-103">Método TestReplicaSystem de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="b656a-103">TestReplicaSystem method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="b656a-104">Crea una nueva réplica de una máquina virtual con la instantánea especificada con fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="b656a-104">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b656a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b656a-105">Syntax</span></span>


```mof
uint32 TestReplicaSystem(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b656a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b656a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b656a-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b656a-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b656a-108">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se debe probar la replicación.</span><span class="sxs-lookup"><span data-stu-id="b656a-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be tested.</span></span>

</dd> <dt>

<span data-ttu-id="b656a-109">*SnapshotSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b656a-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b656a-110">Referencia a una instancia [**de \_ VirtualSystemSettingData de CIM**](/previous-versions//cc136954(v=vs.85)) que representa la instantánea utilizada para crear el sistema de conmutación por error de prueba.</span><span class="sxs-lookup"><span data-stu-id="b656a-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used to create the test failover system.</span></span> <span data-ttu-id="b656a-111">Si este parámetro es **null**, la conmutación por error se realizará en el momento dado más reciente.</span><span class="sxs-lookup"><span data-stu-id="b656a-111">If this parameter is **Null**, the failover is to be performed off the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="b656a-112">*ResultingSystem* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b656a-112">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b656a-113">Si una máquina virtual se define correctamente, recibe una referencia a una instancia de la [**clase \_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual de prueba recién definida.</span><span class="sxs-lookup"><span data-stu-id="b656a-113">If a virtual machine is successfully defined, receives a reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly defined test virtual machine.</span></span> <span data-ttu-id="b656a-114">Cuando este sistema ya no sea necesario, debe destruirlo llamando al método [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b656a-114">When this system is no longer needed, destroy it by calling the [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b656a-115">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b656a-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b656a-116">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b656a-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b656a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b656a-117">Return value</span></span>

<span data-ttu-id="b656a-118">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b656a-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b656a-119">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="b656a-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-120">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b656a-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-121">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="b656a-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-122">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="b656a-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-123">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="b656a-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-124">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="b656a-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-125">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="b656a-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-126">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b656a-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-127">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b656a-127">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-128">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="b656a-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-129">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b656a-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-130">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="b656a-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-131">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b656a-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b656a-132">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="b656a-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b656a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b656a-133">Requirements</span></span>



| <span data-ttu-id="b656a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b656a-134">Requirement</span></span> | <span data-ttu-id="b656a-135">Value</span><span class="sxs-lookup"><span data-stu-id="b656a-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b656a-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b656a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b656a-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b656a-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b656a-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b656a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b656a-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b656a-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b656a-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b656a-140">Namespace</span></span><br/>                | <span data-ttu-id="b656a-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b656a-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b656a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b656a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b656a-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b656a-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b656a-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b656a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b656a-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b656a-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b656a-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="b656a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b656a-147">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="b656a-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

