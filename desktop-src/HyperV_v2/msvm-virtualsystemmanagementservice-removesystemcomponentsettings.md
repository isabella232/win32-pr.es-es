---
description: Quita la configuración de componentes genéricos de una configuración de sistema virtual.
ms.assetid: 54ddb960-65b7-409d-ad80-f3685562a1a1
title: Método RemoveSystemComponentSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93ef7b794b901212fad72a1fcdf6223d8344b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686584"
---
# <a name="removesystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="67c66-103">Método RemoveSystemComponentSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="67c66-103">RemoveSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="67c66-104">Quita la configuración de componentes genéricos de una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="67c66-104">Removes generic component settings from a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="67c66-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67c66-105">Syntax</span></span>


```mof
uint32 RemoveSystemComponentSettings(
  [in]  Msvm_SystemComponentSettingData REF ComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="67c66-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67c66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67c66-107">*ComponentSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="67c66-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67c66-108">Matriz de [**MSVM \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) que hace referencia a la configuración del componente que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="67c66-108">Array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the component settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="67c66-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="67c66-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67c66-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67c66-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67c66-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67c66-111">Return value</span></span>

<span data-ttu-id="67c66-112">Devuelve 0 o 4096 en caso de éxito; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="67c66-112">Returns 0 or 4096 on a success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="67c66-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="67c66-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="67c66-114">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="67c66-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="67c66-115">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="67c66-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="67c66-116">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="67c66-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="67c66-117">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="67c66-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="67c66-118">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="67c66-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="67c66-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="67c66-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="67c66-120">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="67c66-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="67c66-121">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="67c66-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="67c66-122">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="67c66-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="67c66-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67c66-123">Requirements</span></span>



| <span data-ttu-id="67c66-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="67c66-124">Requirement</span></span> | <span data-ttu-id="67c66-125">Value</span><span class="sxs-lookup"><span data-stu-id="67c66-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c66-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67c66-126">Minimum supported client</span></span><br/> | <span data-ttu-id="67c66-127">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="67c66-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="67c66-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67c66-128">Minimum supported server</span></span><br/> | <span data-ttu-id="67c66-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="67c66-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="67c66-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="67c66-130">Namespace</span></span><br/>                | <span data-ttu-id="67c66-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="67c66-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="67c66-132">MOF</span><span class="sxs-lookup"><span data-stu-id="67c66-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67c66-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67c66-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67c66-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67c66-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67c66-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67c66-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67c66-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="67c66-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c66-137">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="67c66-137">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

