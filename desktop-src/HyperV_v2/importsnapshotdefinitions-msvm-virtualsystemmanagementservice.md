---
description: Busca en la carpeta especificada cualquier archivo de definición de instantánea asociado al sistema de equipo planeado especificado y crea una nueva instantánea en el sistema del equipo planeado para cada archivo de definición asociado en esta ubicación.
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Método ImportSnapshotDefinitions de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9ebb36b030786ab88eab899190afcc7f3022286a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908451"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="184fc-103">Método ImportSnapshotDefinitions de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="184fc-103">ImportSnapshotDefinitions method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="184fc-104">Busca en la carpeta especificada cualquier archivo de definición de instantánea asociado al sistema de equipo planeado especificado y crea una nueva instantánea en el sistema del equipo planeado para cada archivo de definición asociado en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="184fc-104">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span>

## <a name="syntax"></a><span data-ttu-id="184fc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="184fc-105">Syntax</span></span>


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="184fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="184fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="184fc-107">*PlannedSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="184fc-107">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184fc-108">Referencia a un objeto [**\_ PlannedComputerSystem de MSVM**](msvm-plannedcomputersystem.md) que representa la máquina virtual planeada que hace referencia a las instantáneas que se van a importar.</span><span class="sxs-lookup"><span data-stu-id="184fc-108">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned virtual machine which references the snapshots to be imported.</span></span>

</dd> <dt>

<span data-ttu-id="184fc-109">*SnapshotFolder* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="184fc-109">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184fc-110">Ruta de acceso completa a la carpeta donde se pueden encontrar las configuraciones de instantáneas para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="184fc-110">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span>

</dd> <dt>

<span data-ttu-id="184fc-111">*ImportedSnapshots* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="184fc-111">*ImportedSnapshots* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="184fc-112">Si la operación se completa de forma sincrónica, una matriz de referencias a las instancias de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representan las instantáneas que se importaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="184fc-112">If the operation completes synchronously, an array of references to the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances representing the snapshots which were successfully imported.</span></span>

</dd> <dt>

<span data-ttu-id="184fc-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="184fc-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="184fc-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="184fc-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="184fc-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="184fc-115">Return value</span></span>

<span data-ttu-id="184fc-116">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="184fc-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="184fc-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="184fc-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="184fc-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="184fc-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="184fc-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="184fc-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-122">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="184fc-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="184fc-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="184fc-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-125">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="184fc-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="184fc-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="184fc-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-128">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="184fc-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="184fc-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="184fc-130">**Archivo en uso** (32779)</span><span class="sxs-lookup"><span data-stu-id="184fc-130">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="184fc-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="184fc-131">Requirements</span></span>



| <span data-ttu-id="184fc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="184fc-132">Requirement</span></span> | <span data-ttu-id="184fc-133">Value</span><span class="sxs-lookup"><span data-stu-id="184fc-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="184fc-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="184fc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="184fc-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="184fc-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="184fc-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="184fc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="184fc-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="184fc-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="184fc-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="184fc-138">Namespace</span></span><br/>                | <span data-ttu-id="184fc-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="184fc-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="184fc-140">MOF</span><span class="sxs-lookup"><span data-stu-id="184fc-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="184fc-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="184fc-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="184fc-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="184fc-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="184fc-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="184fc-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="184fc-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="184fc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="184fc-145">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="184fc-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

