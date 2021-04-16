---
description: Recupera información sobre una instantánea de VHD dentro de un archivo de VHD set.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Método GetVHDSnapshotInformation de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 85ea18e2be5329345ba49f4956307c4b29134ed6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666613"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="e1484-103">Método GetVHDSnapshotInformation de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="e1484-103">GetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="e1484-104">Recupera información sobre una instantánea de VHD dentro de un archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="e1484-104">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1484-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1484-105">Syntax</span></span>


```mof
uint32 GetVHDSnapshotInformation(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotIds[],
  [in]  uint32              AdditionalInformation[],
  [out] string              SnapshotInformation[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e1484-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1484-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1484-107">*VHDSetPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1484-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1484-108">Una ruta de acceso completa que especifica la ubicación del archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="e1484-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="e1484-109">*SnapshotIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1484-109">*SnapshotIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1484-110">Una lista de GUID que representan los identificadores de instantánea de cada instantánea para la que se solicita información.</span><span class="sxs-lookup"><span data-stu-id="e1484-110">A list of GUIDs representing the Snapshot Ids of each Snapshot for which information is being requested.</span></span> <span data-ttu-id="e1484-111">Si este parámetro es NULL, se recuperará la información de todas las instantáneas.</span><span class="sxs-lookup"><span data-stu-id="e1484-111">If this parameter is NULL, information for all Snapshots will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="e1484-112">*AdditionalInformation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1484-112">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1484-113">Una matriz que especifica la información adicional que se debe recopilar sobre cada instantánea de VHD.</span><span class="sxs-lookup"><span data-stu-id="e1484-113">An array specifying what additional information should be gathered about each VHD Snapshot.</span></span> <span data-ttu-id="e1484-114">Cada entrada de la matriz es un tipo de información adicional.</span><span class="sxs-lookup"><span data-stu-id="e1484-114">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="e1484-115">Si este parámetro es NULL, no se recuperará información adicional.</span><span class="sxs-lookup"><span data-stu-id="e1484-115">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e1484-116">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e1484-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e1484-117">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e1484-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

<span data-ttu-id="e1484-118">**Rutas** de acceso primarias (2)</span><span class="sxs-lookup"><span data-stu-id="e1484-118">**Parent Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e1484-119">*SnapshotInformation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e1484-119">*SnapshotInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1484-120">Si es correcto, una matriz de información sobre cada instantánea solicitada.</span><span class="sxs-lookup"><span data-stu-id="e1484-120">If successful, an array of information about each requested snapshot.</span></span> <span data-ttu-id="e1484-121">Cada elemento es una instancia incrustada de [**MSVM \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span><span class="sxs-lookup"><span data-stu-id="e1484-121">Each element is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1484-122">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e1484-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1484-123">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="e1484-123">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1484-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1484-124">Return value</span></span>

<span data-ttu-id="e1484-125">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e1484-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e1484-126">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="e1484-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-127">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e1484-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-128">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="e1484-128">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-129">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e1484-129">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-130">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="e1484-130">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-131">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e1484-131">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-132">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="e1484-132">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-133">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e1484-133">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-134">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e1484-134">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-135">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="e1484-135">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-136">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e1484-136">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-137">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="e1484-137">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-138">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e1484-138">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e1484-139">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="e1484-139">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e1484-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1484-140">Requirements</span></span>



| <span data-ttu-id="e1484-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1484-141">Requirement</span></span> | <span data-ttu-id="e1484-142">Value</span><span class="sxs-lookup"><span data-stu-id="e1484-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1484-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1484-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e1484-144">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1484-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e1484-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1484-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e1484-146">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e1484-146">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e1484-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e1484-147">Namespace</span></span><br/>                | <span data-ttu-id="e1484-148">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e1484-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e1484-149">MOF</span><span class="sxs-lookup"><span data-stu-id="e1484-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1484-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1484-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1484-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1484-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1484-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e1484-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e1484-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1484-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1484-154">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="e1484-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




