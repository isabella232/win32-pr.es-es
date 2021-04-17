---
description: Restablece las estadísticas de replicación de una máquina virtual y actúa en la relación de replicación principal de la máquina virtual.
ms.assetid: da4b60f8-6964-45af-8412-935234c7c0ff
title: Método ResetReplicationStatistics de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8407e20cb38c9aecac26ab0bcee99ce0c8a6be2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687523"
---
# <a name="resetreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="ed212-103">Método ResetReplicationStatistics de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="ed212-103">ResetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="ed212-104">Restablece las estadísticas de replicación de una máquina virtual y actúa en la relación de replicación principal de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ed212-104">Resets the replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="ed212-105">A partir de Windows 8.1, se recomienda no usar **ResetReplicationStatistics** para restablecer las estadísticas de replicación.</span><span class="sxs-lookup"><span data-stu-id="ed212-105">Starting with Windows 8.1, we recommend not to use **ResetReplicationStatistics** anymore to reset replication statistics.</span></span> <span data-ttu-id="ed212-106">En su lugar, use [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="ed212-106">Instead, use [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ed212-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed212-107">Syntax</span></span>


```mof
uint32 ResetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ed212-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed212-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed212-109">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed212-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed212-110">Referencia a una instancia de la clase [**de \_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se van a restablecer las estadísticas de replicación.</span><span class="sxs-lookup"><span data-stu-id="ed212-110">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to reset the replication statistics for.</span></span>

</dd> <dt>

<span data-ttu-id="ed212-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ed212-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed212-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ed212-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed212-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed212-113">Return value</span></span>

<span data-ttu-id="ed212-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ed212-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ed212-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="ed212-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="ed212-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="ed212-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="ed212-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="ed212-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="ed212-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="ed212-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ed212-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ed212-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="ed212-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ed212-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="ed212-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ed212-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ed212-128">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="ed212-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ed212-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed212-129">Requirements</span></span>



| <span data-ttu-id="ed212-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed212-130">Requirement</span></span> | <span data-ttu-id="ed212-131">Value</span><span class="sxs-lookup"><span data-stu-id="ed212-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed212-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed212-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ed212-133">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed212-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ed212-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed212-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ed212-135">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed212-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed212-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ed212-136">Namespace</span></span><br/>                | <span data-ttu-id="ed212-137">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ed212-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ed212-138">MOF</span><span class="sxs-lookup"><span data-stu-id="ed212-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed212-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed212-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed212-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed212-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed212-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ed212-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ed212-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed212-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed212-143">**GetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="ed212-143">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="ed212-144">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="ed212-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

