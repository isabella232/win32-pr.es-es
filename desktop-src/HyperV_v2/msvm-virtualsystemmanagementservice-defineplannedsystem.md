---
description: Define un sistema virtual planeado.
ms.assetid: f129554b-e43e-4c3a-8418-d5d810f4c4b5
title: Método DefinePlannedSystem de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefinePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d5e9fa8a49e86850d044216a3d95e3d4dd756fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540299"
---
# <a name="defineplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="128b2-103">Método DefinePlannedSystem de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="128b2-103">DefinePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="128b2-104">Define un sistema virtual planeado.</span><span class="sxs-lookup"><span data-stu-id="128b2-104">Defines a planned virtual system.</span></span>

<span data-ttu-id="128b2-105">La entrada que no se ha especificado completamente puede rellenarse con valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="128b2-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="128b2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="128b2-106">Syntax</span></span>


```mof
uint32 DefinePlannedSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="128b2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="128b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="128b2-108">*Configuración* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="128b2-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="128b2-109">La configuración del sistema para el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="128b2-109">The system settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="128b2-110">*ResourceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="128b2-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="128b2-111">La configuración de recursos del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="128b2-111">The resource settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="128b2-112">*ReferenceConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="128b2-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="128b2-113">Un [**\_ VirtualSystemSettingData de CIM**](cim-virtualsystemsettingdata.md) que contiene la configuración de referencia.</span><span class="sxs-lookup"><span data-stu-id="128b2-113">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the reference configuration.</span></span>

</dd> <dt>

<span data-ttu-id="128b2-114">*ResultingSystem* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="128b2-114">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="128b2-115">Un [**\_ ComputerSystem de CIM**](cim-computersystem.md) que contiene el sistema resultante.</span><span class="sxs-lookup"><span data-stu-id="128b2-115">A [**CIM\_ComputerSystem**](cim-computersystem.md) containing the resulting system.</span></span>

</dd> <dt>

<span data-ttu-id="128b2-116">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="128b2-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="128b2-117">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="128b2-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="128b2-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="128b2-118">Return value</span></span>

<span data-ttu-id="128b2-119">Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="128b2-119">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="128b2-120">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="128b2-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="128b2-121">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="128b2-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="128b2-122">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="128b2-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="128b2-123">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="128b2-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="128b2-124">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="128b2-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="128b2-125">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="128b2-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="128b2-126">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="128b2-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="128b2-127">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="128b2-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="128b2-128">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="128b2-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="128b2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="128b2-129">Requirements</span></span>



| <span data-ttu-id="128b2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="128b2-130">Requirement</span></span> | <span data-ttu-id="128b2-131">Value</span><span class="sxs-lookup"><span data-stu-id="128b2-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="128b2-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="128b2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="128b2-133">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="128b2-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="128b2-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="128b2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="128b2-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="128b2-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="128b2-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="128b2-136">Namespace</span></span><br/>                | <span data-ttu-id="128b2-137">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="128b2-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="128b2-138">MOF</span><span class="sxs-lookup"><span data-stu-id="128b2-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="128b2-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="128b2-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="128b2-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="128b2-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="128b2-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="128b2-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="128b2-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="128b2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="128b2-143">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="128b2-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

