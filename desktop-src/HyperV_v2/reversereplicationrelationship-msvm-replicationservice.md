---
description: Vuelve a replicar una máquina virtual conmutada por error en el servidor principal.
ms.assetid: 21806a66-85b4-4d9e-8a50-52d2b1933b67
title: Método ReverseReplicationRelationship de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ReverseReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 25ab0c754c5139b0b3419db74162a8ac0495cf1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687474"
---
# <a name="reversereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="bf4cd-103">Método ReverseReplicationRelationship de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="bf4cd-103">ReverseReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="bf4cd-104">Vuelve a replicar una máquina virtual conmutada por error en el servidor principal.</span><span class="sxs-lookup"><span data-stu-id="bf4cd-104">Replicates a failed-over virtual machine back to the primary server.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf4cd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf4cd-105">Syntax</span></span>


```mof
uint32 ReverseReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bf4cd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf4cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf4cd-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bf4cd-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf4cd-108">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se debe invertir la replicación.</span><span class="sxs-lookup"><span data-stu-id="bf4cd-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be reversed.</span></span>

</dd> <dt>

<span data-ttu-id="bf4cd-109">*ReplicationSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bf4cd-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf4cd-110">Una representación de cadena de una instancia de la clase [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define la configuración de replicación.</span><span class="sxs-lookup"><span data-stu-id="bf4cd-110">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="bf4cd-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bf4cd-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf4cd-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bf4cd-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf4cd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf4cd-113">Return value</span></span>

<span data-ttu-id="bf4cd-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bf4cd-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bf4cd-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="bf4cd-128">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="bf4cd-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bf4cd-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf4cd-129">Requirements</span></span>



| <span data-ttu-id="bf4cd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf4cd-130">Requirement</span></span> | <span data-ttu-id="bf4cd-131">Value</span><span class="sxs-lookup"><span data-stu-id="bf4cd-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf4cd-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf4cd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bf4cd-133">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf4cd-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bf4cd-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf4cd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bf4cd-135">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf4cd-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf4cd-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bf4cd-136">Namespace</span></span><br/>                | <span data-ttu-id="bf4cd-137">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bf4cd-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bf4cd-138">MOF</span><span class="sxs-lookup"><span data-stu-id="bf4cd-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf4cd-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf4cd-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf4cd-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf4cd-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf4cd-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bf4cd-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bf4cd-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf4cd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf4cd-143">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="bf4cd-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

