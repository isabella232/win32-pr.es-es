---
description: Actualiza el sistema virtual.
ms.assetid: 4b24aac9-b7b9-460f-9227-fd3c1e960191
title: Método UpgradeSystemVersion de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.UpgradeSystemVersion
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4c34b33da14d8718f2c2414de3aea3079672bbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686581"
---
# <a name="upgradesystemversion-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a734d-103">Método UpgradeSystemVersion de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="a734d-103">UpgradeSystemVersion method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a734d-104">Actualiza el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="a734d-104">Upgrades the virtual system.</span></span>

<span data-ttu-id="a734d-105">Cuando se aplica a la configuración del sistema de una configuración de sistema virtual "actual"</span><span class="sxs-lookup"><span data-stu-id="a734d-105">When applied to the system settings of a "current" virtual system configuration</span></span>

## <a name="syntax"></a><span data-ttu-id="a734d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a734d-106">Syntax</span></span>


```mof
uint32 UpgradeSystemVersion(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 UpgradeSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a734d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a734d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a734d-108">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a734d-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a734d-109">Referencia a un [**\_ ComputerSystem de CIM**](cim-computersystem.md) que representa el sistema del equipo virtual que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="a734d-109">A reference to a [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual computer system to be upgraded.</span></span>

</dd> <dt>

<span data-ttu-id="a734d-110">*UpgradeSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a734d-110">*UpgradeSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a734d-111">Los datos de configuración de actualización.</span><span class="sxs-lookup"><span data-stu-id="a734d-111">The upgrade setting data.</span></span>

</dd> <dt>

<span data-ttu-id="a734d-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a734d-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a734d-113">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a734d-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a734d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a734d-114">Return value</span></span>

<span data-ttu-id="a734d-115">Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="a734d-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a734d-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="a734d-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a734d-117">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="a734d-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a734d-118">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="a734d-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a734d-119">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="a734d-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a734d-120">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="a734d-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a734d-121">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="a734d-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a734d-122">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="a734d-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a734d-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a734d-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a734d-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a734d-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a734d-125">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a734d-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a734d-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="a734d-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a734d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a734d-127">Requirements</span></span>



| <span data-ttu-id="a734d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a734d-128">Requirement</span></span> | <span data-ttu-id="a734d-129">Value</span><span class="sxs-lookup"><span data-stu-id="a734d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a734d-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a734d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a734d-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="a734d-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a734d-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a734d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a734d-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a734d-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a734d-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a734d-134">Namespace</span></span><br/>                | <span data-ttu-id="a734d-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a734d-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a734d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="a734d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a734d-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a734d-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a734d-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a734d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a734d-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a734d-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a734d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a734d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a734d-141">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a734d-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

