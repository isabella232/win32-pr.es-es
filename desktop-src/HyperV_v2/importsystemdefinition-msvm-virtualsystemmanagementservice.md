---
description: Crea un nuevo sistema de equipo planeado basado en la definición de máquina virtual especificada.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Método ImportSystemDefinition de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb38ab343a3d92fabd1dc44ed100d2d2f7f7bf01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687199"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="bb2db-103">Método ImportSystemDefinition de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="bb2db-103">ImportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="bb2db-104">Crea un nuevo sistema de equipo planeado basado en la definición de máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="bb2db-104">Creates a new planned computer system based on the specified virtual machine definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb2db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb2db-105">Syntax</span></span>


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bb2db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb2db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb2db-107">*SystemDefinitionFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb2db-107">*SystemDefinitionFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb2db-108">Ruta de acceso completa al archivo de definición del sistema (. XML o. exp) que representa la máquina virtual que se va a importar.</span><span class="sxs-lookup"><span data-stu-id="bb2db-108">The fully qualified path to the system definition file (.xml or .exp) representing the virtual machine which is to be imported.</span></span> <span data-ttu-id="bb2db-109">El sistema host o la plataforma de virtualización no deben usar el archivo de definición.</span><span class="sxs-lookup"><span data-stu-id="bb2db-109">The definition file must not already be in use by the host system or the virtualization platform.</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-110">*SnapshotFolder* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb2db-110">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb2db-111">Ruta de acceso completa a la carpeta donde se pueden encontrar las configuraciones de instantáneas para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bb2db-111">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span> <span data-ttu-id="bb2db-112">Se buscará en esta carpeta para buscar las instantáneas a las que hace referencia la definición de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bb2db-112">This folder will be searched in order to locate any snapshots referenced by the virtual machine definition.</span></span> <span data-ttu-id="bb2db-113">Todas las instantáneas a las que se hace referencia que no se encuentren en esta ubicación se deben eliminar con el método [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) o importarse mediante el método [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) antes de realizar el sistema planeado del equipo.</span><span class="sxs-lookup"><span data-stu-id="bb2db-113">Any referenced snapshots not found in this location must be deleted using the [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) method, or imported using the [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) method prior to realizing the planned computer system.</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-114">*GenerateNewSystemIdentifier* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb2db-114">*GenerateNewSystemIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb2db-115">Indica si se debe reutilizar el identificador único de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bb2db-115">Indicates whether to reuse the unique identifier for the virtual machine.</span></span> <span data-ttu-id="bb2db-116">Si este parámetro es **true**, se genera un nuevo identificador de sistema.</span><span class="sxs-lookup"><span data-stu-id="bb2db-116">If this parameter is **True**, then a new system identifier is generated.</span></span> <span data-ttu-id="bb2db-117">Si este parámetro es **false**, se usa el identificador del sistema existente.</span><span class="sxs-lookup"><span data-stu-id="bb2db-117">If this parameter is **False**, then the existing system identifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-118">*ImportedSystem* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bb2db-118">*ImportedSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb2db-119">Si la operación se completa de forma sincrónica, se trata de una referencia a un objeto [**\_ PlannedComputerSystem de MSVM**](msvm-plannedcomputersystem.md) que representa la máquina virtual importada.</span><span class="sxs-lookup"><span data-stu-id="bb2db-119">If the operation completes synchronously, a reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the imported virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="bb2db-120">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bb2db-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb2db-121">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb2db-121">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb2db-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb2db-122">Return value</span></span>

<span data-ttu-id="bb2db-123">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bb2db-123">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bb2db-124">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="bb2db-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-125">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="bb2db-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-126">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="bb2db-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-127">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="bb2db-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-128">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="bb2db-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-129">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="bb2db-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-130">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="bb2db-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-131">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="bb2db-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-132">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="bb2db-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-133">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="bb2db-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-134">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="bb2db-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-135">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="bb2db-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-136">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="bb2db-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="bb2db-137">**Archivo en uso** (32779)</span><span class="sxs-lookup"><span data-stu-id="bb2db-137">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bb2db-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb2db-138">Requirements</span></span>



| <span data-ttu-id="bb2db-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb2db-139">Requirement</span></span> | <span data-ttu-id="bb2db-140">Value</span><span class="sxs-lookup"><span data-stu-id="bb2db-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb2db-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb2db-141">Minimum supported client</span></span><br/> | <span data-ttu-id="bb2db-142">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb2db-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bb2db-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb2db-143">Minimum supported server</span></span><br/> | <span data-ttu-id="bb2db-144">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb2db-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb2db-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bb2db-145">Namespace</span></span><br/>                | <span data-ttu-id="bb2db-146">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bb2db-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bb2db-147">MOF</span><span class="sxs-lookup"><span data-stu-id="bb2db-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb2db-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb2db-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb2db-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb2db-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb2db-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb2db-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb2db-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb2db-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb2db-152">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="bb2db-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

