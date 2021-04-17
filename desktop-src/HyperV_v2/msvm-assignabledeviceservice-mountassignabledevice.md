---
description: Monta el dispositivo PCI especificado para que lo pueda usar el sistema del equipo host.
ms.assetid: 2a07174e-c221-4c04-81b8-5968aa67e235
title: Método MountAssignableDevice de la clase Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.MountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: df5f8a337fbf4baf47a4f695322944ed0b97e82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667829"
---
# <a name="mountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="68956-103">Método MountAssignableDevice de la \_ clase AssignableDeviceService de MSVM</span><span class="sxs-lookup"><span data-stu-id="68956-103">MountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="68956-104">Monta el dispositivo PCI especificado para que lo pueda usar el sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="68956-104">Mounts the specified PCI device so that it can be used by the host computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="68956-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68956-105">Syntax</span></span>


```mof
uint32 MountAssignableDevice(
  [in]  string              DeviceInstancePath,
  [in]  string              DeviceLocationPath,
  [out] string              MountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="68956-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68956-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68956-107">*DeviceInstancePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68956-107">*DeviceInstancePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68956-108">Cadena que contiene la ruta de acceso de la instancia de dispositivo a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68956-108">String containing the device instance path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="68956-109">*DeviceLocationPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68956-109">*DeviceLocationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68956-110">Cadena que contiene la ruta de acceso de la ubicación del dispositivo a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68956-110">String containing the device location path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="68956-111">*MountedDeviceInstancePath* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="68956-111">*MountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68956-112">Cadena que contiene la ruta de acceso de la instancia del dispositivo al dispositivo montado.</span><span class="sxs-lookup"><span data-stu-id="68956-112">String containing the device instance path to the mounted device.</span></span>

</dd> <dt>

<span data-ttu-id="68956-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="68956-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68956-114">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="68956-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68956-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68956-115">Return value</span></span>

<span data-ttu-id="68956-116">Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="68956-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="68956-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="68956-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="68956-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="68956-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="68956-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="68956-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="68956-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="68956-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="68956-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="68956-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="68956-122">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="68956-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="68956-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="68956-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="68956-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="68956-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="68956-125">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="68956-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="68956-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="68956-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="68956-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="68956-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="68956-128">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="68956-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="68956-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="68956-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="68956-130">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="68956-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="68956-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68956-131">Requirements</span></span>



| <span data-ttu-id="68956-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="68956-132">Requirement</span></span> | <span data-ttu-id="68956-133">Value</span><span class="sxs-lookup"><span data-stu-id="68956-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68956-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68956-134">Minimum supported client</span></span><br/> | <span data-ttu-id="68956-135">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="68956-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="68956-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68956-136">Minimum supported server</span></span><br/> | <span data-ttu-id="68956-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="68956-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="68956-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68956-138">Namespace</span></span><br/>                | <span data-ttu-id="68956-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="68956-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="68956-140">MOF</span><span class="sxs-lookup"><span data-stu-id="68956-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68956-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68956-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="68956-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68956-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68956-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68956-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="68956-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="68956-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68956-145">**MSVM \_ AssignableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="68956-145">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




