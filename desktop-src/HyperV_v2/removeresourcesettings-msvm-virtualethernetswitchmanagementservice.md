---
description: Quita la configuración de recursos virtuales de una configuración de conmutador virtual.
ms.assetid: 9992ebcd-8891-42ef-be7e-154f336e37f8
title: Método RemoveResourceSettings de la clase Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9e82117b14ab9975b069e5b340ba9ec504ae65ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082197"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="35729-103">Método RemoveResourceSettings de la \_ clase VirtualEthernetSwitchManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="35729-103">RemoveResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="35729-104">Quita la configuración de recursos virtuales de una configuración de conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="35729-104">Removes virtual resource settings from a virtual switch configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="35729-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35729-105">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="35729-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35729-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35729-107">*ResourceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35729-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35729-108">Una matriz de referencias a instancias de la [**clase \_ ResourceAllocationSettingData de CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , donde cada instancia representa la configuración de un recurso virtual dentro de una configuración de conmutador virtual que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="35729-108">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual switch configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="35729-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="35729-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35729-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="35729-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35729-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35729-111">Return value</span></span>

<span data-ttu-id="35729-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="35729-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="35729-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="35729-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="35729-114">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="35729-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="35729-115">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="35729-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="35729-116">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="35729-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="35729-117">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="35729-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="35729-118">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="35729-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="35729-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="35729-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="35729-120">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="35729-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="35729-121">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="35729-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="35729-122">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="35729-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="35729-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35729-123">Requirements</span></span>



| <span data-ttu-id="35729-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="35729-124">Requirement</span></span> | <span data-ttu-id="35729-125">Value</span><span class="sxs-lookup"><span data-stu-id="35729-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35729-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35729-126">Minimum supported client</span></span><br/> | <span data-ttu-id="35729-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="35729-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="35729-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35729-128">Minimum supported server</span></span><br/> | <span data-ttu-id="35729-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="35729-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35729-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35729-130">Namespace</span></span><br/>                | <span data-ttu-id="35729-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="35729-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="35729-132">MOF</span><span class="sxs-lookup"><span data-stu-id="35729-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35729-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35729-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35729-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35729-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35729-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35729-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="35729-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="35729-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35729-137">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="35729-137">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="35729-138">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="35729-138">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="35729-139">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="35729-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

