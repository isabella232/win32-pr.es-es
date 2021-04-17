---
description: Recupera información acerca de un archivo de VHD set.
ms.assetid: efdfd4c6-b762-4369-add3-e152652c6802
title: Método GetVHDSetInformation de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSetInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cdcf4a354e6d6b47b6a67c071daf8883905f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686941"
---
# <a name="getvhdsetinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="aaa73-103">Método GetVHDSetInformation de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="aaa73-103">GetVHDSetInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="aaa73-104">Recupera información acerca de un archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="aaa73-104">Retrieves information about a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa73-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aaa73-105">Syntax</span></span>


```mof
uint32 GetVHDSetInformation(
  [in]  string              VHDSetPath,
  [in]  uint32              AdditionalInformation[],
  [out] string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="aaa73-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aaa73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa73-107">*VHDSetPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aaa73-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa73-108">Una ruta de acceso completa que especifica la ubicación del archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="aaa73-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="aaa73-109">*AdditionalInformation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aaa73-109">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa73-110">Una matriz que especifica la información adicional que se debe recopilar sobre el archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="aaa73-110">An array specifying what additional information should be gathered about the VHD Set file.</span></span> <span data-ttu-id="aaa73-111">Cada entrada de la matriz es un tipo de información adicional.</span><span class="sxs-lookup"><span data-stu-id="aaa73-111">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="aaa73-112">Si este parámetro es NULL, no se recuperará información adicional.</span><span class="sxs-lookup"><span data-stu-id="aaa73-112">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aaa73-113">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="aaa73-113">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aaa73-114">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aaa73-114">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Paths"></span><span id="paths"></span><span id="PATHS"></span>

<span data-ttu-id="aaa73-115">**Rutas** de acceso (2)</span><span class="sxs-lookup"><span data-stu-id="aaa73-115">**Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="aaa73-116">*Información* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aaa73-116">*Information* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa73-117">Si se realiza correctamente, este objeto contiene la información del archivo de conjunto de VHD solicitado.</span><span class="sxs-lookup"><span data-stu-id="aaa73-117">If successful, this object contains the information for the requested VHD Set file.</span></span> <span data-ttu-id="aaa73-118">Se trata de una instancia incrustada de [**MSVM \_ VHDSetInformation**](msvm-vhdsetinformation.md).</span><span class="sxs-lookup"><span data-stu-id="aaa73-118">This is an embedded instance of [**Msvm\_VHDSetInformation**](msvm-vhdsetinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="aaa73-119">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aaa73-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa73-120">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="aaa73-120">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaa73-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aaa73-121">Return value</span></span>

<span data-ttu-id="aaa73-122">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="aaa73-122">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="aaa73-123">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="aaa73-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="aaa73-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-125">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="aaa73-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-126">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="aaa73-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-127">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="aaa73-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-128">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="aaa73-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-129">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="aaa73-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-130">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="aaa73-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-131">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="aaa73-131">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-132">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="aaa73-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-133">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="aaa73-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-134">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="aaa73-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-135">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="aaa73-135">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="aaa73-136">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="aaa73-136">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="aaa73-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aaa73-137">Requirements</span></span>



| <span data-ttu-id="aaa73-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaa73-138">Requirement</span></span> | <span data-ttu-id="aaa73-139">Value</span><span class="sxs-lookup"><span data-stu-id="aaa73-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa73-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aaa73-140">Minimum supported client</span></span><br/> | <span data-ttu-id="aaa73-141">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="aaa73-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="aaa73-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aaa73-142">Minimum supported server</span></span><br/> | <span data-ttu-id="aaa73-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="aaa73-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="aaa73-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aaa73-144">Namespace</span></span><br/>                | <span data-ttu-id="aaa73-145">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="aaa73-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aaa73-146">MOF</span><span class="sxs-lookup"><span data-stu-id="aaa73-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aaa73-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aaa73-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aaa73-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aaa73-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaa73-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aaa73-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aaa73-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="aaa73-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaa73-151">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="aaa73-151">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




