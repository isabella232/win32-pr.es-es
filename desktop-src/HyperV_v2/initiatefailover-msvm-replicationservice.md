---
description: Inicia una conmutación por error para una máquina virtual en una imagen de punto de replicación estándar o de aplicación.
ms.assetid: cd7e9398-c234-4637-906d-69b46ebf3f51
title: Método InitiateFailover de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f05a9b126028b741782d253ac12b79f9f88e1e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360507"
---
# <a name="initiatefailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="2dacb-103">Método InitiateFailover de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="2dacb-103">InitiateFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="2dacb-104">Inicia una conmutación por error para una máquina virtual en una imagen de punto de replicación estándar o de aplicación.</span><span class="sxs-lookup"><span data-stu-id="2dacb-104">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dacb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2dacb-105">Syntax</span></span>


```mof
uint32 InitiateFailover(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2dacb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2dacb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dacb-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2dacb-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dacb-108">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se va a iniciar una conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="2dacb-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failover.</span></span>

</dd> <dt>

<span data-ttu-id="2dacb-109">*SnapshotSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2dacb-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dacb-110">Referencia a una instancia [**de \_ VirtualSystemSettingData de CIM**](/previous-versions//cc136954(v=vs.85)) que representa la instantánea que se usa para la conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="2dacb-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used for the failover.</span></span> <span data-ttu-id="2dacb-111">Si este parámetro es **null**, la conmutación por error se realizará en el momento dado más reciente.</span><span class="sxs-lookup"><span data-stu-id="2dacb-111">If this parameter is **Null**, the failover is to be performed to the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="2dacb-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2dacb-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dacb-113">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2dacb-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dacb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2dacb-114">Return value</span></span>

<span data-ttu-id="2dacb-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2dacb-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2dacb-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="2dacb-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="2dacb-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="2dacb-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="2dacb-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="2dacb-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="2dacb-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="2dacb-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="2dacb-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="2dacb-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="2dacb-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="2dacb-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="2dacb-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="2dacb-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2dacb-129">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="2dacb-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2dacb-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dacb-130">Requirements</span></span>



| <span data-ttu-id="2dacb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dacb-131">Requirement</span></span> | <span data-ttu-id="2dacb-132">Value</span><span class="sxs-lookup"><span data-stu-id="2dacb-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dacb-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dacb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2dacb-134">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2dacb-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2dacb-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dacb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2dacb-136">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2dacb-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2dacb-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2dacb-137">Namespace</span></span><br/>                | <span data-ttu-id="2dacb-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2dacb-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2dacb-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2dacb-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2dacb-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2dacb-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2dacb-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2dacb-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dacb-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2dacb-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2dacb-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="2dacb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dacb-144">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="2dacb-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="2dacb-145">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="2dacb-145">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="2dacb-146">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="2dacb-146">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

