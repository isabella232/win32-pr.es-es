---
description: Convierte un archivo de disco duro virtual mediante la creación de un nuevo archivo del conjunto de VHD junto con el disco duro virtual existente.
ms.assetid: 04ae723e-e3c5-4640-a0e5-0e1b75bb2e6d
title: Método ConvertVirtualHardDiskToVHDSet de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDiskToVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6113a14f321ff7319f8be15767621db3a7e833de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002930"
---
# <a name="convertvirtualharddisktovhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="324f6-103">Método ConvertVirtualHardDiskToVHDSet de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="324f6-103">ConvertVirtualHardDiskToVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="324f6-104">Convierte un archivo de disco duro virtual mediante la creación de un nuevo archivo del conjunto de VHD junto con el disco duro virtual existente.</span><span class="sxs-lookup"><span data-stu-id="324f6-104">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="324f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="324f6-105">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDiskToVHDSet(
  [in]  string              VirtualHardDiskPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="324f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="324f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="324f6-107">*VirtualHardDiskPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="324f6-107">*VirtualHardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="324f6-108">Cadena que contiene la ruta de acceso al archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="324f6-108">String containing the path to the virtual hard disk file.</span></span> <span data-ttu-id="324f6-109">El nuevo archivo del conjunto de VHD tendrá el mismo nombre de archivo, pero con. Extensión de VHD.</span><span class="sxs-lookup"><span data-stu-id="324f6-109">The new VHD Set file will have the same filename but with the .VHDS extension.</span></span>

</dd> <dt>

<span data-ttu-id="324f6-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="324f6-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="324f6-111">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="324f6-111">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="324f6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="324f6-112">Return value</span></span>

<span data-ttu-id="324f6-113">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="324f6-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="324f6-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="324f6-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-115">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="324f6-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-116">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="324f6-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-117">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="324f6-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-118">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="324f6-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-119">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="324f6-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-120">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="324f6-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-121">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="324f6-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-122">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="324f6-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-123">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="324f6-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-124">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="324f6-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-125">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="324f6-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-126">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="324f6-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="324f6-127">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="324f6-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="324f6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="324f6-128">Requirements</span></span>



| <span data-ttu-id="324f6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="324f6-129">Requirement</span></span> | <span data-ttu-id="324f6-130">Value</span><span class="sxs-lookup"><span data-stu-id="324f6-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="324f6-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="324f6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="324f6-132">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="324f6-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="324f6-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="324f6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="324f6-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="324f6-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="324f6-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="324f6-135">Namespace</span></span><br/>                | <span data-ttu-id="324f6-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="324f6-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="324f6-137">MOF</span><span class="sxs-lookup"><span data-stu-id="324f6-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="324f6-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="324f6-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="324f6-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="324f6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="324f6-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="324f6-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="324f6-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="324f6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="324f6-142">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="324f6-142">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




