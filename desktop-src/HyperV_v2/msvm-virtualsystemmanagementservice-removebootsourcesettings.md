---
description: 'Método RemoveBootSourceSettings de la clase Msvm_VirtualSystemManagementService: quita la configuración de recursos virtuales de una configuración del sistema virtual.'
ms.assetid: 0deb7719-e605-4ba5-9bb2-037d0cafee24
title: Método RemoveBootSourceSettings de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5407e56b761dd545d20b89e0a28742f9c542b15a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109403"
---
# <a name="removebootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="730a4-103">Método RemoveBootSourceSettings de la clase Msvm \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="730a4-103">RemoveBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="730a4-104">Quita la configuración de recursos virtuales de una configuración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="730a4-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="730a4-105">Cuando se aplica a partes de una configuración del sistema virtual "actual", como efecto secundario se pueden quitar los recursos del sistema virtual activo.</span><span class="sxs-lookup"><span data-stu-id="730a4-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="730a4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="730a4-106">Syntax</span></span>


```mof
uint32 RemoveBootSourceSettings(
  [in]  CIM_SettingData REF BootSourceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="730a4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="730a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="730a4-108">*BootSourceSettings* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="730a4-108">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="730a4-109">Referencia a una matriz de [**Valores \_ de CIMData**](cim-settingdata.md) que describen la configuración de origen de arranque que se quitará.</span><span class="sxs-lookup"><span data-stu-id="730a4-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the boot source settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="730a4-110">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="730a4-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="730a4-111">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="730a4-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="730a4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="730a4-112">Return value</span></span>

<span data-ttu-id="730a4-113">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="730a4-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="730a4-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="730a4-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="730a4-115">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="730a4-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="730a4-116">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="730a4-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="730a4-117">**Tiempo de** espera (3)</span><span class="sxs-lookup"><span data-stu-id="730a4-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="730a4-118">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="730a4-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="730a4-119">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="730a4-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="730a4-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="730a4-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="730a4-121">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="730a4-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="730a4-122">**Método reservado** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="730a4-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="730a4-123">**Específico del** proveedor (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="730a4-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="730a4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="730a4-124">Requirements</span></span>



| <span data-ttu-id="730a4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="730a4-125">Requirement</span></span> | <span data-ttu-id="730a4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="730a4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="730a4-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="730a4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="730a4-128">Windows 10 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="730a4-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="730a4-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="730a4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="730a4-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="730a4-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="730a4-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="730a4-131">Namespace</span></span><br/>                | <span data-ttu-id="730a4-132">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="730a4-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="730a4-133">MOF</span><span class="sxs-lookup"><span data-stu-id="730a4-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="730a4-134"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="730a4-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="730a4-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="730a4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="730a4-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="730a4-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="730a4-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="730a4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="730a4-138">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="730a4-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

