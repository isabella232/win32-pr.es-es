---
description: Desmonta el dispositivo PCI especificado para que se pueda asignar.
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: Método DismountAssignableDevice de la clase Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 53036cd09113430d1045c8e9eae7a8d782b35960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687850"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="ebb28-103">Método DismountAssignableDevice de la \_ clase AssignableDeviceService de MSVM</span><span class="sxs-lookup"><span data-stu-id="ebb28-103">DismountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="ebb28-104">Desmonta el dispositivo PCI especificado para que se pueda asignar.</span><span class="sxs-lookup"><span data-stu-id="ebb28-104">Dismounts the specified PCI device so that it can be assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebb28-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebb28-105">Syntax</span></span>


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ebb28-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ebb28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebb28-107">*DismountSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ebb28-107">*DismountSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebb28-108">Instancia insertada de un objeto de datos de configuración que especifica el dispositivo PCI que se va a desmontar.</span><span class="sxs-lookup"><span data-stu-id="ebb28-108">Embedded instance of a setting data object that specifies the PCI device to dismount.</span></span>

</dd> <dt>

<span data-ttu-id="ebb28-109">*DismountedDeviceInstancePath* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ebb28-109">*DismountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebb28-110">Cadena que contiene la ruta de acceso de la instancia del dispositivo al dispositivo desmontado.</span><span class="sxs-lookup"><span data-stu-id="ebb28-110">String containing the device instance path to the dismounted device.</span></span>

</dd> <dt>

<span data-ttu-id="ebb28-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ebb28-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebb28-112">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="ebb28-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebb28-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebb28-113">Return value</span></span>

<span data-ttu-id="ebb28-114">Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="ebb28-114">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ebb28-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="ebb28-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="ebb28-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="ebb28-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="ebb28-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="ebb28-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="ebb28-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="ebb28-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ebb28-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ebb28-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="ebb28-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ebb28-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="ebb28-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ebb28-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ebb28-128">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="ebb28-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ebb28-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebb28-129">Requirements</span></span>



| <span data-ttu-id="ebb28-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebb28-130">Requirement</span></span> | <span data-ttu-id="ebb28-131">Value</span><span class="sxs-lookup"><span data-stu-id="ebb28-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb28-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebb28-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ebb28-133">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="ebb28-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ebb28-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebb28-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ebb28-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ebb28-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ebb28-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ebb28-136">Namespace</span></span><br/>                | <span data-ttu-id="ebb28-137">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ebb28-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ebb28-138">MOF</span><span class="sxs-lookup"><span data-stu-id="ebb28-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebb28-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebb28-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebb28-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ebb28-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebb28-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ebb28-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ebb28-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebb28-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb28-143">**MSVM \_ AssignableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="ebb28-143">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




