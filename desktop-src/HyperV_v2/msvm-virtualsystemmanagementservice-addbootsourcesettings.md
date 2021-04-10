---
description: Agrega orígenes de arranque a una configuración de sistema virtual cuando se aplica a un &\# 0034; estado&\# 0034; configuración del sistema virtual.
ms.assetid: 2d091554-73d4-47c6-a0c2-97644fc9abe9
title: Método AddBootSourceSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e20a1184e11113ba25ac060ec19dab5d2391b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153889"
---
# <a name="addbootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="9acf0-103">Método AddBootSourceSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="9acf0-103">AddBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="9acf0-104">Agrega orígenes de arranque a una configuración de sistema virtual cuando se aplica a una configuración de sistema virtual "State".</span><span class="sxs-lookup"><span data-stu-id="9acf0-104">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="9acf0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9acf0-105">Syntax</span></span>


```mof
uint32 AddBootSourceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           BootSourceSettings[],
  [out] CIM_SettingData              REF ResultingBootSourceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9acf0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9acf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9acf0-107">*AffectedConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9acf0-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9acf0-108">Un [**\_ VirtualSystemSettingData de CIM**](cim-virtualsystemsettingdata.md) que contiene la configuración afectada.</span><span class="sxs-lookup"><span data-stu-id="9acf0-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="9acf0-109">*BootSourceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9acf0-109">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9acf0-110">Una matriz que contiene la configuración de origen de arranque.</span><span class="sxs-lookup"><span data-stu-id="9acf0-110">An array containing the boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="9acf0-111">*ResultingBootSourceSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9acf0-111">*ResultingBootSourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9acf0-112">Si se ejecuta correctamente, devuelve un [**\_ SettingData de CIM**](cim-settingdata.md) con la configuración de origen de arranque resultante.</span><span class="sxs-lookup"><span data-stu-id="9acf0-112">On success, returns a [**CIM\_SettingData**](cim-settingdata.md) with the resulting boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="9acf0-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9acf0-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9acf0-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9acf0-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9acf0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9acf0-115">Return value</span></span>

<span data-ttu-id="9acf0-116">Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="9acf0-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="9acf0-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="9acf0-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9acf0-118">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="9acf0-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9acf0-119">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="9acf0-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9acf0-120">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="9acf0-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9acf0-121">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="9acf0-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9acf0-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9acf0-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9acf0-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="9acf0-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9acf0-124">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="9acf0-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="9acf0-125">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="9acf0-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9acf0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9acf0-126">Requirements</span></span>



| <span data-ttu-id="9acf0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9acf0-127">Requirement</span></span> | <span data-ttu-id="9acf0-128">Value</span><span class="sxs-lookup"><span data-stu-id="9acf0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9acf0-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9acf0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9acf0-130">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="9acf0-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9acf0-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9acf0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9acf0-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9acf0-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9acf0-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9acf0-133">Namespace</span></span><br/>                | <span data-ttu-id="9acf0-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9acf0-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9acf0-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9acf0-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9acf0-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9acf0-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9acf0-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9acf0-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9acf0-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9acf0-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9acf0-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="9acf0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9acf0-140">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="9acf0-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

