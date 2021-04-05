---
description: Agrega recursos a una configuración de máquina virtual.
ms.assetid: e2878b60-dc8c-48fb-b163-29457a96d130
title: Método AddResourceSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b35379e0fe3925bbf0f7c4d753f77d1d207199b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909842"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="1d2fc-103">Método AddResourceSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="1d2fc-103">AddResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="1d2fc-104">Agrega recursos a una configuración de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1d2fc-104">Adds resources to a virtual machine configuration.</span></span> <span data-ttu-id="1d2fc-105">Cuando se aplica a una configuración de máquina virtual de "estado", como efecto secundario, los recursos se agregan a la máquina virtual activa.</span><span class="sxs-lookup"><span data-stu-id="1d2fc-105">When applied to a "state" virtual machine configuration, as a side effect, resources are added to the active virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d2fc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d2fc-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1d2fc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d2fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d2fc-108">*AffectedConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1d2fc-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2fc-109">Referencia a un objeto [**\_ VirtualSystemSettingData de CIM**](/previous-versions//cc136954(v=vs.85)) que representa la configuración de máquina virtual afectada.</span><span class="sxs-lookup"><span data-stu-id="1d2fc-109">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the affected virtual machine configuration.</span></span>

</dd> <dt>

<span data-ttu-id="1d2fc-110">*ResourceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1d2fc-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2fc-111">Matriz de cadenas que contiene una instancia incrustada de la [**clase \_ ResourceAllocationSettingData de CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que describe los aspectos virtuales de un recurso virtual que se va a agregar a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1d2fc-111">An array of strings that contain one embedded instance of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that describes the virtual aspects of a virtual resource to be added to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1d2fc-112">*ResultingResourceSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1d2fc-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2fc-113">Una matriz de referencias a las instancias de la clase [**\_ ResourceAllocationSettingData de CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que representa los aspectos virtuales de los recursos virtuales agregados.</span><span class="sxs-lookup"><span data-stu-id="1d2fc-113">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that represents virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="1d2fc-114">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1d2fc-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2fc-115">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d2fc-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d2fc-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d2fc-116">Return value</span></span>

<span data-ttu-id="1d2fc-117">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1d2fc-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1d2fc-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="1d2fc-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1d2fc-119">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="1d2fc-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1d2fc-120">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="1d2fc-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1d2fc-121">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="1d2fc-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1d2fc-122">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="1d2fc-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1d2fc-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1d2fc-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1d2fc-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="1d2fc-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1d2fc-125">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="1d2fc-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1d2fc-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="1d2fc-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1d2fc-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d2fc-127">Requirements</span></span>



| <span data-ttu-id="1d2fc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d2fc-128">Requirement</span></span> | <span data-ttu-id="1d2fc-129">Value</span><span class="sxs-lookup"><span data-stu-id="1d2fc-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2fc-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d2fc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1d2fc-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d2fc-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1d2fc-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d2fc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1d2fc-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d2fc-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d2fc-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1d2fc-134">Namespace</span></span><br/>                | <span data-ttu-id="1d2fc-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1d2fc-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1d2fc-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1d2fc-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d2fc-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d2fc-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d2fc-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d2fc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d2fc-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d2fc-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1d2fc-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d2fc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d2fc-141">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="1d2fc-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

