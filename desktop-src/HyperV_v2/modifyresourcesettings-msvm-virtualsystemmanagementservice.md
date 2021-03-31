---
description: Modifica la configuración de recursos virtuales.
ms.assetid: 3fb2a65f-9f40-4eb9-99e8-8fe1451427d9
title: Método ModifyResourceSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 872e81926f717671b741a89c9bf954e452803b36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911681"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a920e-103">Método ModifyResourceSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="a920e-103">ModifyResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a920e-104">Modifica la configuración de recursos virtuales.</span><span class="sxs-lookup"><span data-stu-id="a920e-104">Modifies virtual resource settings.</span></span> <span data-ttu-id="a920e-105">Cuando se aplica a partes de una configuración de máquina virtual actual, como efecto secundario, se pueden modificar los recursos de la máquina virtual activa.</span><span class="sxs-lookup"><span data-stu-id="a920e-105">When applied to parts of a current virtual machine configuration, as a side effect, the resources of the active virtual machine may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="a920e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a920e-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a920e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a920e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a920e-108">*ResourceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a920e-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a920e-109">Matriz de cadenas que contiene una instancia incrustada de una clase derivada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), que contiene los aspectos modificados de los recursos virtuales existentes.</span><span class="sxs-lookup"><span data-stu-id="a920e-109">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="a920e-110">La propiedad **InstanceID** de cada instancia identifica la configuración de recursos virtuales que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="a920e-110">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="a920e-111">*ResultingResourceSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a920e-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a920e-112">Una matriz de referencias a instancias de objetos derivados de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que representan aspectos virtuales de los recursos virtuales modificados.</span><span class="sxs-lookup"><span data-stu-id="a920e-112">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="a920e-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a920e-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a920e-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a920e-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a920e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a920e-115">Return value</span></span>

<span data-ttu-id="a920e-116">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a920e-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a920e-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="a920e-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a920e-118">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="a920e-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a920e-119">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="a920e-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a920e-120">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="a920e-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a920e-121">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="a920e-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a920e-122">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="a920e-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a920e-123">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="a920e-123">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a920e-124">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a920e-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a920e-125">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a920e-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a920e-126">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a920e-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a920e-127">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="a920e-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a920e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a920e-128">Requirements</span></span>



| <span data-ttu-id="a920e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a920e-129">Requirement</span></span> | <span data-ttu-id="a920e-130">Value</span><span class="sxs-lookup"><span data-stu-id="a920e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a920e-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a920e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a920e-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a920e-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a920e-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a920e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a920e-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a920e-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a920e-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a920e-135">Namespace</span></span><br/>                | <span data-ttu-id="a920e-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a920e-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a920e-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a920e-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a920e-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a920e-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a920e-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a920e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a920e-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a920e-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a920e-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="a920e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a920e-142">**ModifyVirtualSystemResources (V1)**</span><span class="sxs-lookup"><span data-stu-id="a920e-142">**ModifyVirtualSystemResources (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="a920e-143">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a920e-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

