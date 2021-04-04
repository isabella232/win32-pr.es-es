---
description: Establece los datos de configuración de la máquina inicial de las máquinas virtuales.
ms.assetid: 0f174d29-ddb2-4a8c-b664-926245573778
title: Método SetInitialMachineConfigurationData de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetInitialMachineConfigurationData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08028358d6bb53406abe15c88e0acd02e748d387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808785"
---
# <a name="setinitialmachineconfigurationdata-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="05aac-103">Método SetInitialMachineConfigurationData de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="05aac-103">SetInitialMachineConfigurationData method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="05aac-104">Establece los datos de configuración de la máquina inicial de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="05aac-104">Sets a VM's initial machine configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="05aac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05aac-105">Syntax</span></span>


```mof
uint32 SetInitialMachineConfigurationData(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  uint8                  ImcData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="05aac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05aac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05aac-107">*TargetSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05aac-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05aac-108">Referencia al sistema del equipo virtual en el que se van a establecer los datos de IMC.</span><span class="sxs-lookup"><span data-stu-id="05aac-108">A reference to the virtual computer system on which the IMC data will be set.</span></span>

</dd> <dt>

<span data-ttu-id="05aac-109">*IMCDATA* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05aac-109">*ImcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05aac-110">Datos de IMC que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="05aac-110">The IMC data to set.</span></span> <span data-ttu-id="05aac-111">Los primeros cuatro bytes deben ser la longitud de la matriz en orden Big-Endian</span><span class="sxs-lookup"><span data-stu-id="05aac-111">The first four bytes must be the length of the array in big-endian order</span></span>

</dd> <dt>

<span data-ttu-id="05aac-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="05aac-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05aac-113">Parámetro opcional para supervisar el progreso de la operación, que se utiliza si el método no se pudo ejecutar sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="05aac-113">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="05aac-114">Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.</span><span class="sxs-lookup"><span data-stu-id="05aac-114">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05aac-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05aac-115">Return value</span></span>

<span data-ttu-id="05aac-116">Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="05aac-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="05aac-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="05aac-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="05aac-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="05aac-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="05aac-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="05aac-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="05aac-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="05aac-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="05aac-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="05aac-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="05aac-122">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="05aac-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="05aac-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="05aac-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="05aac-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="05aac-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="05aac-125">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="05aac-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="05aac-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="05aac-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="05aac-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="05aac-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="05aac-128">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="05aac-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="05aac-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="05aac-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="05aac-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05aac-130">Requirements</span></span>



| <span data-ttu-id="05aac-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="05aac-131">Requirement</span></span> | <span data-ttu-id="05aac-132">Value</span><span class="sxs-lookup"><span data-stu-id="05aac-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05aac-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05aac-133">Minimum supported client</span></span><br/> | <span data-ttu-id="05aac-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="05aac-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="05aac-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05aac-135">Minimum supported server</span></span><br/> | <span data-ttu-id="05aac-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="05aac-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="05aac-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="05aac-137">Namespace</span></span><br/>                | <span data-ttu-id="05aac-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="05aac-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="05aac-139">MOF</span><span class="sxs-lookup"><span data-stu-id="05aac-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05aac-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05aac-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="05aac-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="05aac-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05aac-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="05aac-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="05aac-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="05aac-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05aac-144">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="05aac-144">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




