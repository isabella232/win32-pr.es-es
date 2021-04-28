---
description: 'Método ModifyResourceSettings de la clase Msvm_VirtualSystemManagementService: modifica la configuración de recursos virtuales.'
ms.assetid: 3fb2a65f-9f40-4eb9-99e8-8fe1451427d9
title: Método ModifyResourceSettings de la Msvm_VirtualSystemManagementService clase
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
ms.openlocfilehash: 09ca0bb9fea02b6acc5599d9f907b1e60fdbd9ec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119343"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="ebaf7-103">Método ModifyResourceSettings de la clase Msvm \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="ebaf7-103">ModifyResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ebaf7-104">Modifica la configuración de recursos virtuales.</span><span class="sxs-lookup"><span data-stu-id="ebaf7-104">Modifies virtual resource settings.</span></span> <span data-ttu-id="ebaf7-105">Cuando se aplica a partes de una configuración de máquina virtual actual, como efecto secundario, se pueden modificar los recursos de la máquina virtual activa.</span><span class="sxs-lookup"><span data-stu-id="ebaf7-105">When applied to parts of a current virtual machine configuration, as a side effect, the resources of the active virtual machine may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebaf7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebaf7-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ebaf7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ebaf7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebaf7-108">*ResourceSettings* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ebaf7-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebaf7-109">Matriz de cadenas que contienen una instancia incrustada de una clase derivada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), que contienen los aspectos modificados de los recursos virtuales existentes.</span><span class="sxs-lookup"><span data-stu-id="ebaf7-109">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="ebaf7-110">La **propiedad InstanceID** de cada instancia identifica la configuración del recurso virtual que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="ebaf7-110">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="ebaf7-111">*ResultingResourceSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ebaf7-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebaf7-112">Matriz de referencias a instancias de objetos derivados de [**\_ ResourceAllocationSettingData de CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que representan aspectos virtuales de los recursos virtuales modificados.</span><span class="sxs-lookup"><span data-stu-id="ebaf7-112">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="ebaf7-113">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ebaf7-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebaf7-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ebaf7-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebaf7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebaf7-115">Return value</span></span>

<span data-ttu-id="ebaf7-116">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ebaf7-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ebaf7-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="ebaf7-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ebaf7-118">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="ebaf7-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ebaf7-119">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="ebaf7-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ebaf7-120">**Tiempo de** espera (3)</span><span class="sxs-lookup"><span data-stu-id="ebaf7-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ebaf7-121">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="ebaf7-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ebaf7-122">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="ebaf7-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ebaf7-123">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="ebaf7-123">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ebaf7-124">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ebaf7-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ebaf7-125">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="ebaf7-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ebaf7-126">**Método reservado** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="ebaf7-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ebaf7-127">**Específico del** proveedor (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="ebaf7-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ebaf7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebaf7-128">Requirements</span></span>



| <span data-ttu-id="ebaf7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebaf7-129">Requirement</span></span> | <span data-ttu-id="ebaf7-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ebaf7-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebaf7-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebaf7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ebaf7-132">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="ebaf7-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ebaf7-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebaf7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ebaf7-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ebaf7-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ebaf7-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ebaf7-135">Namespace</span></span><br/>                | <span data-ttu-id="ebaf7-136">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="ebaf7-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ebaf7-137">MOF</span><span class="sxs-lookup"><span data-stu-id="ebaf7-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebaf7-138"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebaf7-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebaf7-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ebaf7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebaf7-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ebaf7-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ebaf7-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ebaf7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebaf7-142">**ModifyVirtualSystemResources (V1)**</span><span class="sxs-lookup"><span data-stu-id="ebaf7-142">**ModifyVirtualSystemResources (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="ebaf7-143">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="ebaf7-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

