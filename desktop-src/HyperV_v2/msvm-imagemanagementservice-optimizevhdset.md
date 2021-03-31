---
description: Optimiza un archivo de VHD set para que use menos espacio en disco.
ms.assetid: 2d2f4531-5d2d-4334-bcc2-d3d3c15b1f46
title: Método OptimizeVHDSet de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.OptimizeVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c360dcd8acf0a4721b8921cd2ca914c34002d078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908133"
---
# <a name="optimizevhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="9dca6-103">Método OptimizeVHDSet de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="9dca6-103">OptimizeVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="9dca6-104">Optimiza un archivo de VHD set para que use menos espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="9dca6-104">Optimizes a VHD Set file to use less disk space.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dca6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9dca6-105">Syntax</span></span>


```mof
uint32 OptimizeVHDSet(
  [in]  string              VHDSetPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9dca6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9dca6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dca6-107">*VHDSetPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9dca6-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dca6-108">Una ruta de acceso completa que especifica la ubicación del archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="9dca6-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="9dca6-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9dca6-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9dca6-110">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="9dca6-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dca6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9dca6-111">Return value</span></span>

<span data-ttu-id="9dca6-112">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="9dca6-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="9dca6-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="9dca6-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="9dca6-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="9dca6-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="9dca6-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="9dca6-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="9dca6-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="9dca6-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="9dca6-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="9dca6-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="9dca6-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="9dca6-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="9dca6-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="9dca6-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="9dca6-126">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="9dca6-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9dca6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dca6-127">Requirements</span></span>



| <span data-ttu-id="9dca6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dca6-128">Requirement</span></span> | <span data-ttu-id="9dca6-129">Value</span><span class="sxs-lookup"><span data-stu-id="9dca6-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dca6-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dca6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9dca6-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="9dca6-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9dca6-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dca6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9dca6-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9dca6-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9dca6-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9dca6-134">Namespace</span></span><br/>                | <span data-ttu-id="9dca6-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9dca6-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9dca6-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9dca6-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9dca6-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9dca6-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9dca6-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9dca6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dca6-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9dca6-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9dca6-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="9dca6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dca6-141">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="9dca6-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




