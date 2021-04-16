---
description: Edita una entrada de instantánea de VHD dentro de un archivo de conjunto de VHD. Si el ID. de instantánea en cuestión ya existe, la entrada de instantánea existente se sobrescribirá con la nueva entrada. De lo contrario, la nueva entrada se agregará al archivo del conjunto de VHD.
ms.assetid: dd14960d-3fb8-4d47-986f-fbbbb08eb37d
title: Método SetVHDSnapshotInformation de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 54f5ac23cdf8f49532a05eee3fd23293715cd02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666609"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="8be86-105">Método SetVHDSnapshotInformation de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="8be86-105">SetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="8be86-106">Edita una entrada de instantánea de VHD dentro de un archivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="8be86-106">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="8be86-107">Si el ID. de instantánea en cuestión ya existe, la entrada de instantánea existente se sobrescribirá con la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="8be86-107">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="8be86-108">De lo contrario, la nueva entrada se agregará al archivo del conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="8be86-108">Otherwise, the new entry will be added to the VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8be86-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8be86-109">Syntax</span></span>


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8be86-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8be86-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be86-111">*Información* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8be86-111">*Information* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8be86-112">Información de instantánea de VHD que se va a cambiar o agregar en el archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="8be86-112">VHD Snapshot Information to be changed or added in the VHD Set file.</span></span> <span data-ttu-id="8be86-113">La cadena es una instancia incrustada de [**MSVM \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span><span class="sxs-lookup"><span data-stu-id="8be86-113">The string is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="8be86-114">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8be86-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8be86-115">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="8be86-115">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be86-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8be86-116">Return value</span></span>

<span data-ttu-id="8be86-117">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8be86-117">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="8be86-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="8be86-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="8be86-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="8be86-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="8be86-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="8be86-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-123">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="8be86-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-124">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="8be86-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-125">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="8be86-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-126">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="8be86-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="8be86-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="8be86-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-129">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="8be86-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-130">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="8be86-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="8be86-131">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="8be86-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8be86-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8be86-132">Requirements</span></span>



| <span data-ttu-id="8be86-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8be86-133">Requirement</span></span> | <span data-ttu-id="8be86-134">Value</span><span class="sxs-lookup"><span data-stu-id="8be86-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8be86-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8be86-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8be86-136">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="8be86-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8be86-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8be86-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8be86-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8be86-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8be86-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8be86-139">Namespace</span></span><br/>                | <span data-ttu-id="8be86-140">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8be86-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8be86-141">MOF</span><span class="sxs-lookup"><span data-stu-id="8be86-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8be86-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8be86-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8be86-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8be86-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8be86-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8be86-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8be86-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="8be86-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be86-146">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="8be86-146">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




