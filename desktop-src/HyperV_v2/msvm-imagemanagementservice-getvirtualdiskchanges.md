---
description: Recupera una lista de cambios en la región especificada de un disco virtual desde el identificador de Change Tracking resistente o el identificador de la instantánea de VHDSet proporcionado.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Método GetVirtualDiskChanges de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55a9cb9a63e05e002f99984a306566c50d9e1d7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686940"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="e93c4-103">Método GetVirtualDiskChanges de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="e93c4-103">GetVirtualDiskChanges method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="e93c4-104">Recupera una lista de cambios en la región especificada de un disco virtual desde el identificador de Change Tracking resistente o el identificador de la instantánea de VHDSet proporcionado.</span><span class="sxs-lookup"><span data-stu-id="e93c4-104">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span>

## <a name="syntax"></a><span data-ttu-id="e93c4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e93c4-105">Syntax</span></span>


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e93c4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e93c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e93c4-107">*Ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e93c4-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e93c4-108">Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="e93c4-108">A fully-qualified path that specifies the location of the Virtual Hard Disk file.</span></span>

</dd> <dt>

<span data-ttu-id="e93c4-109">*LimitId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e93c4-109">*LimitId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e93c4-110">Un identificador de Change Tracking resistente o un identificador de instantánea de conjunto de VHD que indica la línea de base de los cambios en el disco virtual.</span><span class="sxs-lookup"><span data-stu-id="e93c4-110">A Resilient Change Tracking Id or VHD Set Snapshot Id indicating the baseline for changes in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="e93c4-111">*TargetSnapshotId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e93c4-111">*TargetSnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e93c4-112">Un identificador de instantánea de VHDSet que indica la instantánea que se va a comparar con la línea de base al detenerse los cambios en el disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="e93c4-112">A VHDSet Snapshot Id indicating the snapshot to compare to the baseline when determing changes in the virtual hard disk.</span></span> <span data-ttu-id="e93c4-113">Este parámetro solo es válido para los archivos de VHD set.</span><span class="sxs-lookup"><span data-stu-id="e93c4-113">This parameter is only valid for VHD Set files.</span></span>

</dd> <dt>

<span data-ttu-id="e93c4-114">*Byteoffset (* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e93c4-114">*ByteOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e93c4-115">Desplazamiento de bytes de la región del disco virtual para el que se van a consultar los cambios.</span><span class="sxs-lookup"><span data-stu-id="e93c4-115">The byte offset of the region in the virtual disk to query changes for.</span></span>

</dd> <dt>

<span data-ttu-id="e93c4-116">*ByteLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e93c4-116">*ByteLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e93c4-117">Longitud de bytes de la región del disco virtual para la que se van a consultar los cambios.</span><span class="sxs-lookup"><span data-stu-id="e93c4-117">The byte length of the region in the virtual disk to query changes for.</span></span> <span data-ttu-id="e93c4-118">Debe ser menor que el tamaño del disco virtual.</span><span class="sxs-lookup"><span data-stu-id="e93c4-118">This must be less than the size of the Virtual Disk.</span></span>

</dd> <dt>

<span data-ttu-id="e93c4-119">*ProcessedByteLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e93c4-119">*ProcessedByteLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e93c4-120">Longitud total de bytes que se procesó.</span><span class="sxs-lookup"><span data-stu-id="e93c4-120">The total byte length that was processed.</span></span> <span data-ttu-id="e93c4-121">Puede ser igual a ByteLength o Less.</span><span class="sxs-lookup"><span data-stu-id="e93c4-121">This may be equal to ByteLength or less.</span></span>

</dd> <dt>

<span data-ttu-id="e93c4-122">*ChangedByteOffsets* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e93c4-122">*ChangedByteOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e93c4-123">La lista de desplazamientos de bytes en el disco virtual que indica el principio de cada intervalo modificado.</span><span class="sxs-lookup"><span data-stu-id="e93c4-123">The list of byte offsets into the virtual disk indicating the beginning of each changed range.</span></span>

</dd> <dt>

<span data-ttu-id="e93c4-124">*ChangedByteLengths* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e93c4-124">*ChangedByteLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e93c4-125">La lista de longitudes de bytes de los intervalos modificados en el disco virtual.</span><span class="sxs-lookup"><span data-stu-id="e93c4-125">The list of byte lengths of the changed ranges in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="e93c4-126">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e93c4-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e93c4-127">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="e93c4-127">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e93c4-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e93c4-128">Return value</span></span>

<span data-ttu-id="e93c4-129">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e93c4-129">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e93c4-130">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="e93c4-130">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-131">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e93c4-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-132">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="e93c4-132">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-133">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e93c4-133">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-134">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="e93c4-134">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-135">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e93c4-135">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-136">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="e93c4-136">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-137">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e93c4-137">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-138">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e93c4-138">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-139">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="e93c4-139">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-140">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e93c4-140">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-141">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="e93c4-141">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-142">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e93c4-142">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e93c4-143">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="e93c4-143">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e93c4-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e93c4-144">Requirements</span></span>



| <span data-ttu-id="e93c4-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="e93c4-145">Requirement</span></span> | <span data-ttu-id="e93c4-146">Value</span><span class="sxs-lookup"><span data-stu-id="e93c4-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e93c4-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e93c4-147">Minimum supported client</span></span><br/> | <span data-ttu-id="e93c4-148">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e93c4-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e93c4-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e93c4-149">Minimum supported server</span></span><br/> | <span data-ttu-id="e93c4-150">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e93c4-150">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e93c4-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e93c4-151">Namespace</span></span><br/>                | <span data-ttu-id="e93c4-152">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e93c4-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e93c4-153">MOF</span><span class="sxs-lookup"><span data-stu-id="e93c4-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e93c4-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e93c4-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e93c4-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e93c4-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e93c4-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e93c4-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e93c4-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="e93c4-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e93c4-158">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="e93c4-158">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




