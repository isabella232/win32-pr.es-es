---
description: Modifica la configuración de recursos de un conmutador virtual.
ms.assetid: 1ae2456f-921c-4ea6-b3fb-7065110063fb
title: Método ModifyResourceSettings de la clase Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f40044b20389914281ad4f651019f3e8dc6b6148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688061"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="d8bb4-103">Método ModifyResourceSettings de la \_ clase VirtualEthernetSwitchManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="d8bb4-103">ModifyResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="d8bb4-104">Modifica la configuración de recursos de un conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="d8bb4-104">Modifies resource settings for a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8bb4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8bb4-105">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d8bb4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8bb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8bb4-107">*ResourceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8bb4-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bb4-108">Matriz de cadenas que contiene una instancia incrustada de una clase derivada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), que contiene los aspectos modificados de los recursos virtuales existentes.</span><span class="sxs-lookup"><span data-stu-id="d8bb4-108">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="d8bb4-109">La propiedad **InstanceID** de cada instancia identifica la configuración de recursos virtuales que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="d8bb4-109">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="d8bb4-110">*ResultingResourceSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d8bb4-110">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bb4-111">Una matriz de referencias a instancias de objetos derivados de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que representan aspectos virtuales de los recursos virtuales modificados.</span><span class="sxs-lookup"><span data-stu-id="d8bb4-111">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="d8bb4-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d8bb4-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bb4-113">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d8bb4-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8bb4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8bb4-114">Return value</span></span>

<span data-ttu-id="d8bb4-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d8bb4-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d8bb4-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="d8bb4-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d8bb4-117">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="d8bb4-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d8bb4-118">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="d8bb4-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d8bb4-119">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="d8bb4-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d8bb4-120">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="d8bb4-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d8bb4-121">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="d8bb4-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d8bb4-122">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="d8bb4-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d8bb4-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d8bb4-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d8bb4-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="d8bb4-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d8bb4-125">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d8bb4-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d8bb4-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="d8bb4-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d8bb4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8bb4-127">Requirements</span></span>



| <span data-ttu-id="d8bb4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8bb4-128">Requirement</span></span> | <span data-ttu-id="d8bb4-129">Value</span><span class="sxs-lookup"><span data-stu-id="d8bb4-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8bb4-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8bb4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d8bb4-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8bb4-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d8bb4-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8bb4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d8bb4-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8bb4-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8bb4-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d8bb4-134">Namespace</span></span><br/>                | <span data-ttu-id="d8bb4-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d8bb4-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d8bb4-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d8bb4-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8bb4-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8bb4-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8bb4-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d8bb4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8bb4-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8bb4-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8bb4-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8bb4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8bb4-141">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="d8bb4-141">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="d8bb4-142">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="d8bb4-142">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="d8bb4-143">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="d8bb4-143">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

