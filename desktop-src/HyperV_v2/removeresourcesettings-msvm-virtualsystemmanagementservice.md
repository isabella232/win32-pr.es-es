---
description: Quita la configuración de recursos virtuales de una configuración de máquina virtual.
ms.assetid: 74d9a70a-5258-4e4b-8131-b25513d11a4b
title: Método RemoveResourceSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 20a7c9fb10e4f7a6356e47f8c743266095de2042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666601"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="d8ea3-103">Método RemoveResourceSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="d8ea3-103">RemoveResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="d8ea3-104">Quita la configuración de recursos virtuales de una configuración de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8ea3-104">Removes virtual resource settings from a virtual machine configuration.</span></span> <span data-ttu-id="d8ea3-105">Cuando se aplica a partes de una configuración de máquina virtual actual, es posible que se elimine la máquina virtual activa.</span><span class="sxs-lookup"><span data-stu-id="d8ea3-105">When applied to parts of a current virtual machine configuration, the active virtual machine may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ea3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8ea3-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d8ea3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8ea3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8ea3-108">*ResourceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8ea3-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8ea3-109">Una matriz de referencias a instancias de la [**clase \_ ResourceAllocationSettingData de CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , donde cada instancia representa la configuración de un recurso virtual dentro de una configuración de máquina virtual que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="d8ea3-109">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual machine configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="d8ea3-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d8ea3-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8ea3-111">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d8ea3-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8ea3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8ea3-112">Return value</span></span>

<span data-ttu-id="d8ea3-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d8ea3-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d8ea3-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="d8ea3-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d8ea3-115">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="d8ea3-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d8ea3-116">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="d8ea3-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d8ea3-117">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="d8ea3-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d8ea3-118">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="d8ea3-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d8ea3-119">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="d8ea3-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d8ea3-120">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="d8ea3-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d8ea3-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d8ea3-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d8ea3-122">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d8ea3-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d8ea3-123">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="d8ea3-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d8ea3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8ea3-124">Requirements</span></span>



| <span data-ttu-id="d8ea3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8ea3-125">Requirement</span></span> | <span data-ttu-id="d8ea3-126">Value</span><span class="sxs-lookup"><span data-stu-id="d8ea3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ea3-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8ea3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d8ea3-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8ea3-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d8ea3-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8ea3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d8ea3-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8ea3-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8ea3-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d8ea3-131">Namespace</span></span><br/>                | <span data-ttu-id="d8ea3-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d8ea3-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d8ea3-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d8ea3-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8ea3-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8ea3-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8ea3-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d8ea3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8ea3-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8ea3-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8ea3-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8ea3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ea3-138">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="d8ea3-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

