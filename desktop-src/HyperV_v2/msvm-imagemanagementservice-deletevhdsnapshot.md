---
description: Elimina una entrada de instantánea de VHD dentro de un archivo de VHD set.
ms.assetid: 37d55a5f-209d-42ce-8f69-8b494055e263
title: Método DeleteVHDSnapshot de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.DeleteVHDSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5c7f3f115825aedb3a21a8f33326a712c52e0780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686942"
---
# <a name="deletevhdsnapshot-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="edb21-103">Método DeleteVHDSnapshot de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="edb21-103">DeleteVHDSnapshot method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="edb21-104">Elimina una entrada de instantánea de VHD dentro de un archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="edb21-104">Deletes a VHD Snapshot entry within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb21-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edb21-105">Syntax</span></span>


```mof
uint32 DeleteVHDSnapshot(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotId,
  [in]  boolean             PersistReferenceSnapshot,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="edb21-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edb21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb21-107">*VHDSetPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edb21-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb21-108">Cadena que contiene la ruta de acceso al archivo del conjunto de VHD que contiene la instantánea en cuestión.</span><span class="sxs-lookup"><span data-stu-id="edb21-108">String containing the path to the VHD Set file containing the snapshot in question.</span></span>

</dd> <dt>

<span data-ttu-id="edb21-109">*SnapshotId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edb21-109">*SnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb21-110">Un GUID que representa el identificador de la instantánea para la entrada de instantánea de VHD que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="edb21-110">A GUID representing the Snapshot ID for the VHD Snapshot entry to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="edb21-111">*PersistReferenceSnapshot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edb21-111">*PersistReferenceSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb21-112">Indica si se debe conservar o no un registro de instantánea de solo referencia después de que se elimine la instantánea.</span><span class="sxs-lookup"><span data-stu-id="edb21-112">Whether or not a reference-only snapshot record should be persisted after the snapshot is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="edb21-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="edb21-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edb21-114">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="edb21-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb21-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edb21-115">Return value</span></span>

<span data-ttu-id="edb21-116">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="edb21-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="edb21-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="edb21-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="edb21-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="edb21-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="edb21-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="edb21-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-122">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="edb21-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="edb21-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="edb21-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-125">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="edb21-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="edb21-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="edb21-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-128">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="edb21-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="edb21-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="edb21-130">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="edb21-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="edb21-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edb21-131">Requirements</span></span>



| <span data-ttu-id="edb21-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="edb21-132">Requirement</span></span> | <span data-ttu-id="edb21-133">Value</span><span class="sxs-lookup"><span data-stu-id="edb21-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edb21-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edb21-134">Minimum supported client</span></span><br/> | <span data-ttu-id="edb21-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="edb21-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="edb21-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edb21-136">Minimum supported server</span></span><br/> | <span data-ttu-id="edb21-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="edb21-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="edb21-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="edb21-138">Namespace</span></span><br/>                | <span data-ttu-id="edb21-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="edb21-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="edb21-140">MOF</span><span class="sxs-lookup"><span data-stu-id="edb21-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edb21-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="edb21-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="edb21-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="edb21-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edb21-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="edb21-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="edb21-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="edb21-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb21-145">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="edb21-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




