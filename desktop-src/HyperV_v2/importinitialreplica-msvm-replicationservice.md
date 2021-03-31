---
description: Importa la replicación inicial de una máquina virtual.
ms.assetid: 151211fe-e58e-4fd4-87cd-cdb2ad55c0b1
title: Método ImportInitialReplica de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ImportInitialReplica
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b60ab10c6387127c294a472c9e1e86be7fd84146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155548"
---
# <a name="importinitialreplica-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="014ef-103">Método ImportInitialReplica de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="014ef-103">ImportInitialReplica method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="014ef-104">Importa la replicación inicial de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="014ef-104">Imports the initial replication for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="014ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="014ef-105">Syntax</span></span>


```mof
uint32 ImportInitialReplica(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 InitialReplicationImportLocation,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="014ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="014ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="014ef-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="014ef-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="014ef-108">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se debe importar la replicación inicial.</span><span class="sxs-lookup"><span data-stu-id="014ef-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the initial replication should be imported.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-109">*InitialReplicationImportLocation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="014ef-109">*InitialReplicationImportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="014ef-110">Ruta de acceso completa del directorio desde el que se va a importar la replicación inicial.</span><span class="sxs-lookup"><span data-stu-id="014ef-110">The fully qualified path of the directory from which the initial replication is to be imported.</span></span> <span data-ttu-id="014ef-111">No puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="014ef-111">This cannot be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="014ef-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="014ef-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="014ef-113">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="014ef-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="014ef-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="014ef-114">Return value</span></span>

<span data-ttu-id="014ef-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="014ef-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="014ef-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="014ef-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="014ef-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="014ef-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="014ef-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="014ef-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="014ef-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="014ef-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="014ef-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="014ef-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="014ef-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="014ef-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="014ef-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="014ef-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="014ef-129">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="014ef-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="014ef-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="014ef-130">Requirements</span></span>



| <span data-ttu-id="014ef-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="014ef-131">Requirement</span></span> | <span data-ttu-id="014ef-132">Value</span><span class="sxs-lookup"><span data-stu-id="014ef-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="014ef-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="014ef-133">Minimum supported client</span></span><br/> | <span data-ttu-id="014ef-134">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="014ef-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="014ef-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="014ef-135">Minimum supported server</span></span><br/> | <span data-ttu-id="014ef-136">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="014ef-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="014ef-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="014ef-137">Namespace</span></span><br/>                | <span data-ttu-id="014ef-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="014ef-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="014ef-139">MOF</span><span class="sxs-lookup"><span data-stu-id="014ef-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="014ef-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="014ef-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="014ef-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="014ef-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="014ef-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="014ef-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="014ef-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="014ef-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="014ef-144">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="014ef-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

